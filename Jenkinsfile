pipeline {
    agent any

    stages {
        stage('Test') {
            steps {
                echo "Testing.."
                echo "Current branch: ${env.BRANCH_NAME}"
            }
        }
        stage("Build"){
            when {
                expression { env.BRANCH_NAME == 'main' }
            }
            steps{
                echo "Building.."
            }
        }
        stage("Deploy"){
            when {
                expression { env.BRANCH_NAME == 'main' }
            }
            steps{
                echo "Deploying.."
            }
        }
    }
}
