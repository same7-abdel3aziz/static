pipeline {
    agent any
        stage('Upload to AWS') {
            steps {
                withAWS(region:'us-east-2',credentials:'Jenkins') {
                    s3Upload(pathStyleAccessEnabled:true, payloadSigningEnabled: true, file:'index.html', bucket:'jenkinsam')
                }
            }
        }
    }
}
