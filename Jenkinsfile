pipeline {
  agent any
  stages {
    stage('Lint HTML') {
      steps {
        tidy -q -e *.html
      }
    }
    stage('Upload to AWS') {
      steps {
        withAWS(region:'us-west-1',credentials:'aws-static'){
          s3Upload(file:'index.html', bucket:'zhan430website', path:'')
        }
      }
    }
  }
}
