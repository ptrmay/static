pipeline{
     agent any
     stages {
         stage('Upload to AWS') {
             steps {
                 withAWS(credentials:'MyCredentials'){
			s3Upload(file:'index.html', bucket:'jenkinsbucketaws')
		}
             }
         }
      }
}
