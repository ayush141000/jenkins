pipeline {
    agent any 
        stages  {
        
            
            stage('basic test') {

            
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
