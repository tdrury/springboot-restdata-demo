pipeline { 
    agent {
        docker { image 'maven:3.5-jdk-8-alpine' }
    }
    stages { 
        stage('Build') { 
            steps { 
               sh "mvn clean install"
            }
        }
        stage('Results') {
            junit 'target/**/*.xml'
            archiveArtifacts artifacts: 'target/*.jar'
        }
    }
}
