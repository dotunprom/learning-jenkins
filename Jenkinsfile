pipeline {
    agent any

    options {
      ansiColor('xterm')
//       pipline syntax
}

    environment{
      ENV_URL = "pipeline.google.com"
      SSH_CRED = credentials("SSH")
}
    stages {

        stage('one') {
            steps {
//               addShortText background: '', borderColor: '', color: '', link: '', text: 'ONE'
              sh '''
                echo Hello1
                echo Hello2
                echo ENV_URL = ${ENV_URL}
              '''
            }
        }


      stage("two") {
         environment{
            ENV_URL = "stage.google.com"
         }
           steps {
               echo "two"
               sh 'echo ENV_URL = ${ENV_URL}'
               echo '\033[34mHello\033[0m \033[33mcolorful\033[0m \033[35mworld!\033[0m'
               sh 'echo -e "\\e[Hello "'
//                sh 'terraform apply -auto-approve'
           }
       }

    }
}
