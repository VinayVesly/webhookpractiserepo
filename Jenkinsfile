pipeline {
    agent {
        label 'dev_slave1'
    }

    parameters {
        choice(name: 'ENV', choices: ['dev', 'qa', 'prod'], description: 'Select environment')
        string(name: 'BRANCH', defaultValue: 'main', description: 'Git branch')
        booleanParam(name: 'DEPLOY', defaultValue: true, description: 'Deploy application')
    }

    stages {
        stage('Build') {
            steps {
                echo "Building from branch: ${params.BRANCH}"
            }
        }

        stage('Deploy') {
            when {
                expression { params.DEPLOY }
            }
            steps {
                echo "Deploying to ${params.ENV}"
            }
        }
    }
}
