
def randomResult = new java.util.Random().nextInt(18)

node {
    cleanWs notFailBuild: true
    stage('Checkout'){
        def analysisStatus = 'OK'
        if (randomResult == 11){
          analysisStatus = 'KO'
        }
        def jsonResult = "{\"full_message\": \"Build finished $analysisStatus\", \"buildNumber\": $BUILD_NUMBER, \"message\": \"Build finished $analysisStatus\", \"host\":\"jenkins\", \"facility\":\"test\", \"buildResult\":\"$analysisStatus\", \"type\":\"CI\",\"step\":\"CI\",\"step\":\"Checkout\"}"
        echo 'Json Result: ' + jsonResult
        sh "echo -n '$jsonResult' | nc -4u -w1 localhost 12201"
        if (analysisStatus == 'KO') {
          error 'error in Checkout'
        }
        echo 'checkout status: ' + randomResult
    }
    stage('Build') {
      def analysisStatus = 'OK'
      if (randomResult == 12){
        analysisStatus = 'KO'
        sh 'echo -n \'{"full_message": "Build finished $analysisStatus", "buildNumber": $BUILD_NUMBER, "message": "Build finished $analysisStatus", "host":"jenkins", "facility":"test", "buildResult":"$analysisStatus", "type":"CI","step":"build"}\' | nc -4u -w1 localhost 12201'
        error 'error in Checkout'
      }
      sh 'echo -n \'{"full_message": "Build finished $analysisStatus", "buildNumber": $BUILD_NUMBER, "message": "Build finished $analysisStatus", "host":"jenkins", "facility":"test", "buildResult":"$analysisStatus", "type":"CI","step":"build"}\' | nc -4u -w1 localhost 12201'
      echo 'Build status: ' + analysisStatus
    }
    stage('Quality') {
      def analysisStatus = 'OK'
      if (randomResult == 13){
        analysisStatus = 'KO'
        sh 'echo -n \'{"full_message": "Build finished $analysisStatus", "buildNumber": $BUILD_NUMBER, "message": "Build finished $analysisStatus", "host":"jenkins", "facility":"test", "buildResult":"$analysisStatus", "type":"CI","step":"Quality"}\' | nc -4u -w1 localhost 12201'
        error 'error in Checkout'
      }
      sh 'echo -n \'{"full_message": "Build finished $analysisStatus", "buildNumber": $BUILD_NUMBER, "message": "Build finished $analysisStatus", "host":"jenkins", "facility":"test", "buildResult":"$analysisStatus", "type":"CI","step":"Quality"}\' | nc -4u -w1 localhost 12201'
      echo 'Quality status: ' + analysisStatus
    }
    stage('Publish in Nexus') {
      def analysisStatus = 'OK'
      if (randomResult == 14){
        analysisStatus = 'KO'
        sh 'echo -n \'{"full_message": "Build finished $analysisStatus", "buildNumber": $BUILD_NUMBER, "message": "Build finished $analysisStatus", "host":"jenkins", "facility":"test", "buildResult":"$analysisStatus", "type":"CI","step":"Nexus"}\' | nc -4u -w1 localhost 12201'
        error 'error in Checkout'
      }
      sh 'echo -n \'{"full_message": "Build finished $analysisStatus", "buildNumber": $BUILD_NUMBER, "message": "Build finished $analysisStatus", "host":"jenkins", "facility":"test", "buildResult":"$analysisStatus", "type":"CI","step":"Nexus"}\' | nc -4u -w1 localhost 12201'
      echo 'Nexus status: ' + analysisStatus
    }
    stage('Build Docker Image') {
      def analysisStatus = 'OK'
      if (randomResult == 15){
        analysisStatus = 'KO'
        sh 'echo -n \'{"full_message": "Build finished $analysisStatus", "buildNumber": $BUILD_NUMBER, "message": "Build finished $analysisStatus", "host":"jenkins", "facility":"test", "buildResult":"$analysisStatus", "type":"CI","step":"BuildDocker"}\' | nc -4u -w1 localhost 12201'
        error 'error in Checkout'
      }
      sh 'echo -n \'{"full_message": "Build finished $analysisStatus", "buildNumber": $BUILD_NUMBER, "message": "Build finished $analysisStatus", "host":"jenkins", "facility":"test", "buildResult":"$analysisStatus", "type":"CI","step":"BuildDocker"}\' | nc -4u -w1 localhost 12201'
      echo 'Build Docker status: ' + analysisStatus
    }
    stage('Publish Docker Image') {
      def analysisStatus = 'OK'
      if (randomResult == 16){
        analysisStatus = 'KO'
        sh 'echo -n \'{"full_message": "Build finished $analysisStatus", "buildNumber": $BUILD_NUMBER, "message": "Build finished $analysisStatus", "host":"jenkins", "facility":"test", "buildResult":"$analysisStatus", "type":"CI","step":"PublishDocker"}\' | nc -4u -w1 localhost 12201'
        error 'error in Checkout'
      }
      sh 'echo -n \'{"full_message": "Build finished $analysisStatus", "buildNumber": $BUILD_NUMBER, "message": "Build finished $analysisStatus", "host":"jenkins", "facility":"test", "buildResult":"$analysisStatus", "type":"CI","step":"PublishDocker"}\' | nc -4u -w1 localhost 12201'
      echo 'Publish Docker status: ' + analysisStatus
    }
    stage('Deploy') {
      def analysisStatus = 'OK'
      if (randomResult == 17){
        analysisStatus = 'KO'
        sh 'echo -n \'{"full_message": "Build finished $analysisStatus", "buildNumber": $BUILD_NUMBER, "message": "Build finished $analysisStatus", "host":"jenkins", "facility":"test", "buildResult":"$analysisStatus", "type":"CI","step":"Deploy"}\' | nc -4u -w1 localhost 12201'
        error 'error in Checkout'
      }
      sh 'echo -n \'{"full_message": "Build finished $analysisStatus", "buildNumber": $BUILD_NUMBER, "message": "Build finished $analysisStatus", "host":"jenkins", "facility":"test", "buildResult":"$analysisStatus", "type":"CI","step":"Deploy"}\' | nc -4u -w1 localhost 12201'
      echo 'Deploy status: ' + analysisStatus
    }
    stage('Clean') {
      sh 'echo -n \'{"full_message": "Build finished $analysisStatus", "buildNumber": $BUILD_NUMBER, "message": "Build finished $analysisStatus", "host":"jenkins", "facility":"test", "buildResult":"$analysisStatus", "type":"CI","step":"Clean"}\' | nc -4u -w1 localhost 12201'
      echo 'Clean status: OK'
    }
}
