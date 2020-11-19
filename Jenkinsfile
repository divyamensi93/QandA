pipeline {
    agent {
        docker {
            image 'maven:3.6.3-openjdk-8'
            args '-v $HOME/.m2:/root/.m2'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean compile'
            }
        }
        stage('Unit test') {
            steps {
                sh 'mvn test'
            }
        }
    }
}
