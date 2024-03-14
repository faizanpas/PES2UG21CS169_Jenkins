pipeline {
    agent any

    stage('Build') {
        steps {
            build 'PES2UG21CS169-1'
            sh "g++ jenkins_pipeline.cpp -o output"
        }
    }

    stage('Test') {
        steps {
            sh "./output"
        }
    }

    stage('Deploy') {
        steps {
            echo 'Deployment step'
        }
    }

    post {
        failure {
            // Display an error message if the pipeline fails
            echo "Pipeline failed"
        }
    }
}

