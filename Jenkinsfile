pipeline {
    agent any

    stages {
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
                sh "deploy_script.sh nonexistent_file"
             }
           }

    }

    post {
        failure {
            // Display an error message if the pipeline fails
            echo "Pipeline failed"
        }
    }
}


