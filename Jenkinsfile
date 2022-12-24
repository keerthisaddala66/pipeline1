pipeline {
    agent any
    stages {
     
        stage('Maven Build') {
            when {
                branch 'develop'
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Tomcat Deploy-Dev') {
            when {
                branch 'develop'
            }
            steps {
                sshagent(['tomcat-creds']) {
                   echo "Deploying to dev"
                }
            }
        }
             stage('Tomcat Deploy-prod') {
            when {
                branch 'main'
            }
            steps {
                echo "Deploying to production"
                    
                }
            }
        }
    }
}
    }
}
