pipeline{
     agent any
     stages {
         stage('Upload to AWS') {
             steps {
                 withAWS(credentials:'AKIAXTHO5UUMAWPAB24F'){
			s3Upload(file:'index.html', bucket:'jenkinsbucketaws')
		}
             }
         }
      }
}
