pipeline {
    agent any 
        stages  {
        
            
            stage('basic test') {
                agent {
                    docker{
                        image 'google/cloud-sdk'
                    }
                }

            
            steps {
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
