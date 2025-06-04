pipeline {
    agent any 
        stages  {
            stage('basic test') {
            steps {
                sh '''
                echo "hello Champ"
                sudo apt-get update
                sudo apt-get install apt-transport-https ca-certificates google-cloud-sdk -y
                gcloud version
                echo "Welcome to GCP"
                '''
            }
        }
    }


}
