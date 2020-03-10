pipeline{
    agent none
    stages{
        stage('checkout') {
            agent {
                label "master"
            }
            steps {
                git changelog: false, poll: false, url: 'https://github.com/hfmj/simple-java-maven-app.git'
            }
        }

        stage('Build') { 
            agent{
                label "maven-agent"
            }
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }

        }
    }
}
