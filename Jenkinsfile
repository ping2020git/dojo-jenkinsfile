pipeline {
    agent any
    stages {
        stage('SCM Checkout')  {
            steps {
                git credentialsId: 'githuncredentails', url: 'https://github.com/rohit0503/dojo.git'
            }
        } 
        stage('Run ansible script') {
            steps {
                sh label: '', script: '/home/start.sh'
            }
        }
        
    }

}
