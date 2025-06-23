pipeline {
    agent any

    parameters {
        choice(name: 'environment', choices: ['dev', 'staging', 'prod'], description: 'Select the environment')
    }

    stages {
        stage('Show Selected Environment') {
            steps {
                echo "You selected: ${params.environment}"
            }
        }

        stage('Deploy Based on Environment') {
            steps {
                script {
                    if (params.environment == 'dev') {
                        echo "Deploying to Development environment"
                        // Your dev deployment logic
                    } else if (params.environment == 'staging') {
                        echo "Deploying to Staging environment"
                        // Your staging deployment logic
                    } else if (params.environment == 'prod') {
                        echo "Deploying to Production environment"
                        // Your prod deployment logic
                    } else {
                        error("Unknown environment selected!")
                    }
                }
            }
        }
    }
}
