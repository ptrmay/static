pipeline{
     agent any
     stages {
         stage("Lint HTML"){
             steps {
                 tidy -q -e *.html
                }
             }
         stage('Upload to AWS') {
             steps {
                 withAWS(credentials:'MyCredentials'){
			s3Upload(file:'index.html', bucket:'jenkinsbucketaws')
		}
             }
         }
      }
}
