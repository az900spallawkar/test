pipeline {

   agent  any
        options {
                timestamps ()
                ansiColor('xterm')
            }
    stages {
        stage('checkout') {
            steps {
                    
                   git "https://github.com/az900spallawkar/awx-test.git"
                         
                }
            }
            stage('AWX test') {
            steps {
               ansibleTower inventory: 'awx-nginx-saziya', jobTemplate: 'awx-jenkins-saziya', jobType: 'run', throwExceptionWhenFail: false, towerCredentialsId: 'jenkinsAWX', towerLogLevel: 'full', towerServer: 'AWX'
            }
        }
    }

  }
