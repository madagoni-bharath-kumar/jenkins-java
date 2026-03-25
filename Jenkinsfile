pipeline {
    agent any

    tools {
        maven 'Maven'
    }

    stages {
        stage('Clone Code') {
            steps {
                git 'https://github.com/madagonibharath/jenkins-java-lab.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Run') {
            steps {
                sh 'java -jar target/hello-app-1.0.jar'
            }
        }
    }
}
