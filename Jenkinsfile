pipeline {
    agent any

    stages {
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage("Build"){
            when {
                branch "main"
            }
            steps{
                echo "Building.."
            }
        }
        stage("Deploy"){
            when {
                branch "main"
            }
            steps{
                echo "Deploying.."
            }
        }
    }
    
}
