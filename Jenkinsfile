pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                echo 'Building...'
                sh '''
                uptime
                ls -l
                id
                '''
            }
        }
    }
}