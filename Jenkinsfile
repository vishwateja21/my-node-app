pipeline {
    agent any
    tools {
        nodejs 'NodeJS' 
        maven 'Maven' // Name of Maven installation in Jenkins
    }
    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from GitHub
                git url: 'https://github.com/vishwateja21/my-node-app.git', branch: 'master'
            }
        }
        stage('Install Dependencies') {
            steps {
                // Ensure 'npm install' runs from the correct directory
                dir('my-node-app') {
                    bat 'npm install'
                }
            }
        }
        stage('Build with Maven') {
            steps {
                // Ensure Maven is run in the correct directory
                dir('my-node-app') {
                    bat 'mvn clean package'
                }
            }
        }
        stage('Run Selenium Tests') {
            steps {
                // Ensure tests are run from the correct directory
                dir('my-node-app') {
                    bat 'mvn test -Dtest=YourSeleniumTestClass'
                }
            }
        }
    }
    post {
        success {
            echo 'Build and tests were successful!'
        }
        failure {
            echo 'Build or tests failed!'
        }
        always {
            echo 'Cleaning up...'
        }
    }
}
