pipeline {
  agent any
  stages {
    stage('Upload to AWS') {
      steps {
        withAWS(region:'us-west-2'){
        }
        withAWS(credentials:'AKIAVWA5WUEKU5F3CDCR'){
        }
        s3Upload(file:'index.html', bucket:'zhan430website', path:'/')
      }
    }
  }
}
