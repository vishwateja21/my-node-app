pipeline{
    agent any
    stage{
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
        
