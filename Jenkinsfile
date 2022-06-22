pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World from testing branch!'
            }
        }
        stage('Build') {
            steps {
                echo 'Building'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing'
                input('Do you want to proceed? ')
            }
        }
        stage('No Main') {
            when {
                not {
                    branch "main"
                }
            }
            steps {
                echo 'On the testing branch!'
            }
        }
    }
}
