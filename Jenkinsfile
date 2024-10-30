pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                nodejs('NodeJS'){
                    echo 'Building Application'
                    sh 'npm install'
                }
            }
        }
    }
}
        
