pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
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
