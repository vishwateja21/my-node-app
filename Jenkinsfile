pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                nodejs('NodeJs'){
                    echo 'Building Application'
                    sh 'npm install'
                }
            }
        }
    }
}
        
