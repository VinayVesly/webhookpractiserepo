pipeline {
    agent {
        label 'dev_slave1'
    }
    environment {
        project = "caleston"
    }

    stages {
        stage('Build') {
            steps {
                echo "Printing the variable $project"
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploy running on EC2 agent"
            }
        }
    }
    post {
        success {
            echo "print this after success build"
        }
    }
}

