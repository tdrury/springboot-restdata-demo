pipeline { 
    agent {
        docker { image '3.5-jdk-8-alpine' }
    }
    stages { 
        stage('Build') { 
            steps { 
               sh "mvn clean install"
            }
        }
    }
}
