pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            steps {
                withAWS(region:'us-east-2',credentials:'jenkins') {
                    s3Upload(pathStyleAccessEnabled:true, payloadSigningEnabled: true, file:'index.html', bucket:'jenkinsam')
            }
        }
    }
}
