
def randomResult = new java.util.Random().nextInt(18)
def analysisStatus = 'OK'
def jsonResult = null

pipeline {
    agent any
    stages {
      stage('Checkout'){
          steps {
            cleanWs notFailBuild: true
            #checkout([$class: 'GitSCM', branches: [[name: '*/develop']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/agcandil-atsistemas/ci-pipelines.git']]])
            #sh 'pwd'
            #echo 'Commit to relaunch job'
            #sh 'git checkout develop'
            #sh 'echo " " >> file.log'
            #sh 'git add -A'
            #sh 'git commit -m "AutoCommit"'
            #sh 'git push origin develop'
            script {
              if (randomResult == 11){
                analysisStatus = 'KO'
              }
              jsonResult = "{\"full_message\": \"Build finished $analysisStatus\", \"buildNumber\": $BUILD_NUMBER, \"message\": \"Build finished $analysisStatus\", \"host\":\"jenkins\", \"facility\":\"test\", \"buildResult\":\"$analysisStatus\", \"type\":\"CI\",\"step\":\"Checkout\"}"
            }
            echo 'Json Result: ' + jsonResult
            sh "echo -n '$jsonResult' | nc -4u -w1 localhost 12201"
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
            jsonResult = "{\"full_message\": \"Build finished $analysisStatus\", \"buildNumber\": $BUILD_NUMBER, \"message\": \"Build finished $analysisStatus\", \"host\":\"jenkins\", \"facility\":\"test\", \"buildResult\":\"$analysisStatus\", \"type\":\"CI\",\"step\":\"Build\"}"
          }
          echo 'Json Result: ' + jsonResult
          sh "echo -n '$jsonResult' | nc -4u -w1 localhost 12201"
          script {
            if (analysisStatus == 'KO') {
              error 'error in Build'
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
            jsonResult = "{\"full_message\": \"Build finished $analysisStatus\", \"buildNumber\": $BUILD_NUMBER, \"message\": \"Build finished $analysisStatus\", \"host\":\"jenkins\", \"facility\":\"test\", \"buildResult\":\"$analysisStatus\", \"type\":\"CI\",\"step\":\"Quality\"}"
          }
          echo 'Json Result: ' + jsonResult
          sh "echo -n '$jsonResult' | nc -4u -w1 localhost 12201"
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
            jsonResult = "{\"full_message\": \"Build finished $analysisStatus\", \"buildNumber\": $BUILD_NUMBER, \"message\": \"Build finished $analysisStatus\", \"host\":\"jenkins\", \"facility\":\"test\", \"buildResult\":\"$analysisStatus\", \"type\":\"CI\",\"step\":\"Publish\"}"
          }
          echo 'Json Result: ' + jsonResult
          sh "echo -n '$jsonResult' | nc -4u -w1 localhost 12201"
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
            jsonResult = "{\"full_message\": \"Build finished $analysisStatus\", \"buildNumber\": $BUILD_NUMBER, \"message\": \"Build finished $analysisStatus\", \"host\":\"jenkins\", \"facility\":\"test\", \"buildResult\":\"$analysisStatus\", \"type\":\"CI\",\"step\":\"DockerBuild\"}"
          }
          echo 'Json Result: ' + jsonResult
          sh "echo -n '$jsonResult' | nc -4u -w1 localhost 12201"
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
            jsonResult = "{\"full_message\": \"Build finished $analysisStatus\", \"buildNumber\": $BUILD_NUMBER, \"message\": \"Build finished $analysisStatus\", \"host\":\"jenkins\", \"facility\":\"test\", \"buildResult\":\"$analysisStatus\", \"type\":\"CI\",\"step\":\"DockerPublish\"}"
          }
          echo 'Json Result: ' + jsonResult
          sh "echo -n '$jsonResult' | nc -4u -w1 localhost 12201"
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
            jsonResult = "{\"full_message\": \"Build finished $analysisStatus\", \"buildNumber\": $BUILD_NUMBER, \"message\": \"Build finished $analysisStatus\", \"host\":\"jenkins\", \"facility\":\"test\", \"buildResult\":\"$analysisStatus\", \"type\":\"CI\",\"step\":\"Deploy\"}"
          }
          echo 'Json Result: ' + jsonResult
          sh "echo -n '$jsonResult' | nc -4u -w1 localhost 12201"
          script {
            if (analysisStatus == 'KO') {
              error 'error in Deploy'
            }
          }
          echo 'Deploy status: ' + randomResult
        }
      }
    }
    post {
        always {
            echo 'I will always say Hello again!'
            script {
              jsonResult = "{\"full_message\": \"Build finished $analysisStatus\", \"buildNumber\": $BUILD_NUMBER, \"message\": \"Build finished $analysisStatus\", \"host\":\"jenkins\", \"facility\":\"test\", \"buildResult\":\"$analysisStatus\", \"type\":\"CI\",\"step\":\"Summary\"}"
            }
            echo 'Json Result: ' + jsonResult
            sh "echo -n '$jsonResult' | nc -4u -w1 localhost 12201"
        }
    }
}
