pipeline {
    agent any 
        stages  {
        
            
            stage('basic test') {
                agent {
                    docker{
                        image 'google/cloud-sdk:latest'
                        args '-u 1000:1000'
                    }
                }
                steps{
                // Use withCredentials to expose the service account key
                withCredentials([
                    // The ID must match the ID you gave in Jenkins Credentials
                    // Make sure to replace 'gcp-service-account-key' with your actual credential ID
                    // The 'GOOGLE_APPLICATION_CREDENTIALS' environment variable is automatically set by Jenkins.
                    // This variable points to a temporary file containing the JSON key.
                    googleServiceAccountKey('gcp-service-account-key')]) {
                    sh 'gcloud auth activate-service-account --key-file=$GOOGLE_APPLICATION_CREDENTIALS'
                    // You can also set a default project if you haven't already
                    //sh 'gcloud config set project YOUR_PROJECT_ID' // Replace YOUR_PROJECT_ID
                    sh 'gcloud compute zones list'
                }
            
            
                    sh '''
                    echo "hello Champ"
                    gcloud version
                    gcloud compute zones list
                    echo "Welcome to GCP"
                    '''
                }
            }

        }
    }


}
