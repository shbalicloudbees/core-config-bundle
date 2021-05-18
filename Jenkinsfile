library 'my-shared-libraries@master'
pipeline {
  agent none
  options {
    buildDiscarder(logRotator(numToKeepStr: '2'))
    skipDefaultCheckout true
  }
  stages {
    stage('Update Config Bundle') {
      when {
        beforeAgent true
        branch 'master'
      }
      steps {
        configBundleUpdate()
      }
    }
  }
}
