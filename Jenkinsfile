// pipeline {
//     agent any
//
//     stages {
//         stage('Hello') {
//             steps {
//                 echo 'Hello World'
//             }
//         }
//     }
// }


pipeline {
    agent any

    environment{
      ENV_URL = "pipeline.google.com"
}
    stages {

        stage('one') {
            steps {
              addShortText background: '', borderColor: '', color: '', link: '', text: 'ONE'
              sh '''
                echo Hello1
                echo Hello2
              '''
            }
        }
        stage("two") {
            steps {
                echo "two"
            }
        }

    }
}
