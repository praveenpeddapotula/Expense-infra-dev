pipeline {
    agent {
        label 'AGENT-1'
    }
    options {
        timeout(time: 30, unit: 'MINUTES')
        disableConcurrentBuilds()
        ansiColor('xterm')
    }
    stages {
        stage('Init') {
            steps {
               sh """
                ls -ltr
               """
            }
        }
        stage('Plan') {
            steps{
                sh 'echo this is plan stage'
            }
        }
        stage('Deploy') {
           steps{
            sh 'echo this is deploy stage'
           }
            }
    

        stage('Destroy') {
            steps{
                sh''
            }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
        success { 
            echo 'I will run when pipeline is success'
        }
        failure { 
            echo 'I will run when pipeline is failure'
        }
    }
}
}