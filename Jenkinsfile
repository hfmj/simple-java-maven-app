pipeline {
    agent {
        docker {
            image 'maven:3.6.1-alpine' 
            args ' -u root -v /volume1/docker/jenkinsci/home:/root'}
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
