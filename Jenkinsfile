// pipeline {
//     agent any
//
//     options {
//       ansiColor('xterm')
// //       pipline syntax
// }
//
//     environment{
//       ENV_URL = "pipeline.google.com"
//       SSH_CRED = credentials("SSH")
// }
//
// triggers {
//   pollSCM('*/2 * * * *')
// }
//
// tools {
//   maven 'maven-3.8.5'
// }
//
//  parameters {
//         string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
//         text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
//         booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
//         choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
//         password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
//     }
//
//     stages {
//
//         stage('one') {
//           when {
//             environment name: 'CHOICE', value: 'One'
//           }
//
//             steps {
// //               addShortText background: '', borderColor: '', color: '', link: '', text: 'ONE'
//               sh '''
//                 echo Hello1
//                 echo Hello2
//                 echo ENV_URL = ${ENV_URL}
//               '''
//             }
//         }
//
//       stage("two") {
//
//         when {
//           environment name: 'CHOICE', value: 'Two'
//         }
//             options {
//                 ansiColor('xterm')
//         }
//
//          environment{
//             ENV_URL = "stage.google.com"
//         }

//        input {
//                  message "Should we continue?"
//                  ok "Yes, we should."
//                  submitter "alice,bob"
//                  parameters {
//                      string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
//                  }
//              }


//            steps {
//                echo "two"
//                sh 'echo ENV_URL = ${ENV_URL}'
//                echo '\033[34mHello\033[0m \033[33mcolorful\033[0m \033[35mworld!\033[0m'
//                sh 'echo -e "\\e[31mHello "'
//                sh 'mvn --version'
// //                sh 'terraform apply -auto-approve'
//            }
//       }
//   }

//   post {
//     always {
//       cleanWs()
//         sh 'echo post'
//       }
//   }
// }


pipeline{
  agents{
    node { label 'workstation'} // Agent node name
    //label 'ansible' //Agent  labels
    }


  stages {
    stages('parallel') {
      parallel{

        stage('one'){
          steps{
            sh 'sleep 10'
          }
        }


         stage('one'){
            steps{
              sh 'sleep 10'
            }
         }


         stage('one'){
            steps{
               sh 'sleep 10'
            }
         }
      }
    }
  }
}