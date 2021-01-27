pipeline {
    agent any

    stages {
        stage('Verify branch') {
            steps {
                echo "$GIT_BRANCH"
            }
        }

        stages {
        stage('Docker build') {
            steps {
                pwsh(script: 'docker images -a')
                pwsh(script: """
                docker images -a
                docker build -t jenkins-pipeline .
                docker images -a
                """)
            }
        }


    }
}
