pipeline {
  agent any
  stages {
    stage('Upload to AWS') {
      steps {
        withAWS(region:'us-west-2'){
        }
        withAWS(credentials:'jenkins'){
        }
        s3Upload(file:'index.html', bucket:'zhan430website', path:'zhan430/static/index.html')
      }
    }
  }
}
