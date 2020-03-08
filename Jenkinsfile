pipeline {
    agent {
        docker {
            image 'maven:3-alpine' 
            args ''}
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
