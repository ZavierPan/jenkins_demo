pipeline {
    agent any

    stages {
        stage('Test') {
            steps {
                echo "Testing.."
                echo "Current branch: ${env.GIT_BRANCH}" // 改用 GIT_BRANCH 來檢查
            }
        }
        stage("Build"){
            when {
                expression { env.GIT_BRANCH == 'origin/main' }
            }
            steps{
                echo "Building.."
            }
        }
        stage("Deploy"){
            when {
                expression { env.GIT_BRANCH == 'origin/main' }
            }
            steps{
                echo "Deploying.."
            }
        }
    }
}
