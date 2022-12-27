pipeline {
    agent any
    
    stages {
     
        stage('Maven Build') {
            steps {
                sh "mvn clean package"
            }
        }
        stage('Docker Build') {
            steps {
                sh "docker build -t keethisaddala/pipeline:0.0.2 ."
            }
        }
        stage('Docker push') {
             steps {
                sh "docker login -u keethisaddala -p xxxxxxx"
                sh "docker push keethisaddala/pipeline:0.0.2"
            }
        }
    }
}
    
   
                    
           
  
