pipeline {
    agent none
    environment {
        project = caleston
    }

    stages {
        stage('Build') {
            agent {
                label 'docker'
            }
            steps {
                echo "Printing the variable $project"
            }
        }

        stage('Deploy') {
            agent {
                label 'ec2-agent'
            }
            steps {
                echo "Deploy running on EC2 agent"
            }
        }
    }
}

