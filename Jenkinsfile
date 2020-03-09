pipeline { 
    agent any  
    stages { 
        stage('checkout') { 
            steps { 
               //checkout scm
                echo "check"
            }
        }
        stage('Build backend') {
            steps {
                
               bat "mvn -pl '!UI' clean install"
        }
    }
        
        stage('NPM Build') {
            
            steps {
            
            dir('/Hygieia/UI') {
             bat "npm install"   
            }
            }
            
        }
        
    }
}
