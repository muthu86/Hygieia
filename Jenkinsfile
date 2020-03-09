pipeline { 
    agent any  
    stages { 
        stage('checkout') { 
            steps { 
               checkout scm
            }
        }
        stage('Build backend') {
            steps {
                
               sh "mvn clean install"
        }
    }
        
        stage('NPM Build') {
            
            steps {
            
            dir('/Hygieia/UI') {
             sh "npm install"   
            }
            }
            
        }
        
    }
}
