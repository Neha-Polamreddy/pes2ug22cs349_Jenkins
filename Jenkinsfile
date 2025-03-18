pipeline {
    agent any  // Runs pipeline on any available agent

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ new.cpp -o PES2UG22CS349' // Compile new.cpp and generate PES2UG22CS349 executable
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './PES2UG22CS349' // Run the compiled executable
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying Application...'  // Simulated deployment step
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'  // Display failure message if any stage fails
        }
    }
}
