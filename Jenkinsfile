
stages {
        stage('Deploy k8s Tools') {
            stages {
                stage('Checkout git repo') {
                    steps {
                        deleteDir()
                        git branch: "https://github.com/rohit0503/dojo.git", credentialsId: "${env.GIT_CREDS}" , url: "${ANSIBLE_REPO}"
                        sshagent(['zoran-adop-key']) {
                            sh 'chmod +x scripts/*.sh'
                            sh 'scripts/prepare_env.sh'
                        }
                    }            
                 }
