pipeline {
    agent any
    stages {
        stage('SCM Checkout')  {
            steps {
                git credentialsId: 'githuncredentails', url: 'https://github.com/rohit0503/dojo.git'
            }
        }
        stage('Change Permission')  {
            steps {
                sh label: '', chmod -R 755 ${WORKSPACE}/start.sh'
            }
        }
        stage('Run ansible script') {
            steps {
                sh label: '', script: '${WORKSPACE}/start.sh'
            }
        }
        
    }

}
