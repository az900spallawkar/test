pipeline {

   agent  any
        options {
                timestamps ()
                ansiColor('xterm')
            }
    stages {
        stage('checkout') {
            steps {
                    
                   git "https://github.com/az900spallawkar/test.git"
                         
                }
            }
            stage('AWX test') {
            steps {
               ansibleTower( inventory: 'awx-nginx-saziya', templateType: 'job', jobTemplate: 'awx-jenkins-saziya', jobType: 'run', throwExceptionWhenFail: false, towerCredentialsId: '', towerLogLevel: 'full', towerServer: 'AWX')
            }
        }
    }

  }
