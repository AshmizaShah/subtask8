pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Define your build steps here
            }
        }
    }

    post {
        success {
            emailext subject: 'Build Success Notification',
                      body: 'Your build was successful. Congratulations!',
                      to: 'ashmizashah143@gmail.com'
        }
        failure {
            emailext subject: 'Build Failure Notification',
                      body: 'Your build has failed. Please investigate.',
                      to: 'ashmizashah143@gmail.com'
        }
    }
}
