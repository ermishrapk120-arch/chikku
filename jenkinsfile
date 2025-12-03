pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "Building..."
            }
        }

        stage('Tests') {
            when {
                branch 'master'
            }
            parallel {
                stage('Test1') {
                    steps {
                        echo "Running Test 1"
                    }
                }
                stage('Test2') {
                    steps {
                        echo "Running Test 2"
                    }
                }
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying..."
            }
        }
    }
}
