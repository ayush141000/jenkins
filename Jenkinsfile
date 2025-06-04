pipeline {
    agent any 
        stages  {
            agent {
        docker {
            image 'google/cloud-sdk:latest' // or a specific version like 'google/cloud-sdk:449.0.0-alpine'
            args '-u 1000:1000' // Optional: run as a specific user to match Jenkins user if needed
        }
            }
            stage('basic test') {
            steps {
                sh '''
                echo "hello Champ"
                gcloud version
                echo "Welcome to GCP"
                '''
            }
        }
    }


}
