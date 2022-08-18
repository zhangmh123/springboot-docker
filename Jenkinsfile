pipeline {
    agent {
        docker {
            image 'maven:3.5.3-alpine'
            args '-v /root/.m2:/root/.m2'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
    }
}
// pipeline{
//
//   agent any
//   tools {
//       maven '3.8.6'
//    }
//   stages{
//
//         stage("build"){
//           steps{
//                echo 'building the application'
//                sh 'mvn clean package'
//           }
//         }
//
//       stage("test"){
//           steps{
//                 echo 'testing the application'
//           }
//       }
//
//       stage("deploy"){
//             steps{
//                 echo 'deploying the application'
//             }
//       }
//
//   }
//
// }