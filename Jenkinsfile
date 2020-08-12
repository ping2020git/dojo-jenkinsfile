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
                sh label: '', script: '${WORKSPACE}/deploy_k8s/start.sh'
            }
        }
        
    }

}
