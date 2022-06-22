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
            parallel {
                stage('Unit Tesing') {
                    steps {
                        echo 'Running the unit test..'
                    }
                }
                stage('Integration Testing') {
                    agent any
                    steps {
                        echo 'Riining tentegration test..'
                    }
                }
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
