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
                sh "docker build -t ${IMAGE_REFERENCE} ."
            }
        }
        stage("Push"){
            when {
                branch "main"
            }
            steps{
                sh "docker push ${IMAGE_REFERENCE}"
            }
        }
    }
    
}
