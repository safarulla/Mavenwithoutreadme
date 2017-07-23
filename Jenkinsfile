pipeline {
  agent any
  stages {
    stage('stage1') {
      steps {
        parallel(
          "stage1": {
            sh 'echo "Hello world from stage 1 pipeline"'
            
          },
          "Stage2": {
            sh '''echo "Hello This is stage2 step1"
echo "Hello This is stage2 step2"'''
            
          }
        )
      }
    }
    stage('stage3serial') {
      steps {
        sh 'echo "stage3 step1 parallel"'
      }
    }
  }
}