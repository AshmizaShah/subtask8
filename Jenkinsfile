pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                // Add your build steps here
            }
        }
    }

    post {
        success {
            emailext(
                subject: "Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]' succeeded",
                body: "The job has completed successfully.",
                to: 'ashmizashah143@gmail.com'
            )
        }
        failure {
            emailext(
                subject: "Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]' failed",
                body: "The job has failed. Please check the logs.",
                to: 'ashmizashah143@gmail.com'
            )
        }
    }
}

