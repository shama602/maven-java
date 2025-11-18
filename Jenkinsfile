pipeline {
    agent any

    tools {
        maven 'Maven3'   // use the Maven installation name from Jenkins
        jdk 'JDK17'      // use the JDK name configured in Jenkins
    }

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', 
                    url: 'https://github.com/shama602/maven-java.git'
            }
        }

        stage('Build with Maven') {
            steps {
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                sh "mvn test"
            }
        }
    }
}
