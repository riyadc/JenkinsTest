pipeline {
    agent any

    stages {
        stage('Verify branch') {
            steps {
                echo "$GIT_BRANCH"
            }
        }
        
        stage('Docker build') {
            steps {
                sh('docker images -a')
                sh("""
                docker images -a
                docker build -t jenkins-pipeline .
                docker images -a
                """)
            }
        }

    }
}
