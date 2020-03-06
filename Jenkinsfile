pipeline {
    agent {
        docker {
            image 'maven:3-alpine' 
            args '-v ~/.m2:/var/maven/.m2 --rm -e MAVEN_CONFIG=/var/maven/.m2}
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
