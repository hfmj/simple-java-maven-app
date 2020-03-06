pipeline {
    agent {
        docker {
            image 'maven:3-alpine' 
            args '-v /volume1/docker/docker-in-docker/m2:/root/.m2' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
