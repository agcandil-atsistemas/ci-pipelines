
def randomResult = new java.util.Random().nextInt(35)
def analysisStatus = 'OK'

pipeline {
    agent any
    stages {
      stage('Build') {
        steps {
          echo "branch name: $BRANCH_NAME"
          script {
            analysisStatus = 'OK'
            if (randomResult == 11){
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
      stage('UnitTest') {
        steps {
          script {
            analysisStatus = 'OK'
            if (randomResult == 12){
              analysisStatus = 'KO'
            }
          }
          script {
            if (analysisStatus == 'KO') {
              error 'error in UnitTest'
            }
          }
          echo 'Build status: ' + randomResult
        }
      }
      stage('Quality') {
        steps {
          script {
            analysisStatus = 'OK'
            if (randomResult == 13){
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
            if (randomResult == 14){
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
      stage('Build Docker Image') {
        steps {
          script {
            analysisStatus = 'OK'
            if (randomResult == 15){
              analysisStatus = 'KO'
            }
          }
          script {
            if (analysisStatus == 'KO') {
              error 'error in DockerBuild'
            }
          }
          echo 'DockerBuild status: ' + randomResult
        }
      }
      stage('Publish Docker Image') {
        steps {
          script {
            analysisStatus = 'OK'
            if (randomResult == 16){
              analysisStatus = 'KO'
            }
          }
          script {
            if (analysisStatus == 'KO') {
              error 'error in DockerPublish'
            }
          }
          echo 'DockerPublish status: ' + randomResult
        }
      }
      stage('Deploy') {
        steps {
          script {
            analysisStatus = 'OK'
            if (randomResult == 17){
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
            if (randomResult == 18){
              analysisStatus = 'KO'
            }
          }
          script {
            if (analysisStatus == 'KO') {
              error 'error in ATDD'
            }
          }
          echo 'Deploy status: ' + randomResult
        }
      }
    }
    post {
        always {
            echo 'I will always say Hello again!'
        }
    }
}
