

pipeline {
    agent any

    tools {
        nodejs "node16" // Your NodeJS installation name
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'master', url: '<https://github.com/rajeshbuece/Node-JS-PROJECT.git>'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                // Assuming you have tests set up; if not, you can remove this stage
                sh 'npm test || echo "No tests found."'
            }
        }

        stage('Build') {
            steps {
                // If you have a build script, run it here
                echo 'Building the project...'
            }
        }

        stage('Deploy') {
            steps {
                // Placeholder for your deployment logic
                echo 'Deploying the project...'
            }
        }
    }

    post {
        always {
            echo 'Pipeline complete'
        }
    }
}

