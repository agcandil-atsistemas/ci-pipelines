
def randomResult = new java.util.Random().nextInt(25)
def analysisStatus = 'OK'
def jsonResult = null

pipeline {
    agent any
    stages {
      stage('Checkout'){
          steps {
            cleanWs notFailBuild: true
            checkout([$class: 'GitSCM', branches: [[name: '*/develop']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/agcandil-atsistemas/ci-pipelines.git']]])
            script {
              if (randomResult == 11){
                analysisStatus = 'KO'
              }
            }
            script {
              if (analysisStatus == 'KO') {
                error 'error in Checkout'
              }
            }
            echo 'checkout status: ' + randomResult
          }
      }
      stage('Build') {
        steps {
          script {
            analysisStatus = 'OK'
            if (randomResult == 12){
              analysisStatus = 'KO'
            }
          }
          script {
            if (analysisStatus == 'KO') {
              error 'error in Build'
            }
          }
          echo 'Build status: ' + randomResult
        }
      }
      stage('Test') {
        steps {
          script {
            analysisStatus = 'OK'
            if (randomResult == 13){
              analysisStatus = 'KO'
            }
          }
          script {
            if (analysisStatus == 'KO') {
              error 'error in Tests'
            }
          }
          echo 'Tests status: ' + randomResult
        }
      }
      stage('Quality') {
        steps {
          script {
            analysisStatus = 'OK'
            if (randomResult == 14){
              analysisStatus = 'KO'
            }
          }
          script {
            if (analysisStatus == 'KO') {
              error 'error in Quality'
            }
          }
          echo 'Quality status: ' + randomResult
        }
      }
      stage('Publish in Nexus') {
        steps {
          script {
            analysisStatus = 'OK'
            if (randomResult == 15){
              analysisStatus = 'KO'
            }
          }
          script {
            if (analysisStatus == 'KO') {
              error 'error in Publish'
            }
          }
          echo 'Publish status: ' + randomResult
        }
      }
      stage('Deploy') {
        steps {
          script {
            analysisStatus = 'OK'
            if (randomResult == 16){
              analysisStatus = 'KO'
            }
          }
          script {
            if (analysisStatus == 'KO') {
              error 'error in Deploy'
            }
          }
          echo 'Deploy status: ' + randomResult
        }
      }
      stage('ATDD') {
        steps {
          script {
            analysisStatus = 'OK'
            if (randomResult == 17){
              analysisStatus = 'KO'
            }
          }
          script {
            if (analysisStatus == 'KO') {
              error 'error in ATDD'
            }
          }
          echo 'ATDD status: ' + randomResult
        }
      }
    }
    post {
        always {
            echo 'I will always say Hello again!'
          }
    }
}
