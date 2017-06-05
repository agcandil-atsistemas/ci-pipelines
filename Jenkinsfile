
def randomResult = new java.util.Random().nextInt(18)

node {
    cleanWs notFailBuild: true
    stage('Checkout'){
        def analysisStatus = 'OK'
        if (randomResult == 11){
          analysisStatus = 'KO'
        }
        def jsonResult = "{\"full_message\": \"Build finished $analysisStatus\", \"buildNumber\": $BUILD_NUMBER, \"message\": \"Build finished $analysisStatus\", \"host\":\"jenkins\", \"facility\":\"test\", \"buildResult\":\"$analysisStatus\", \"type\":\"CI\",\"step\":\"Checkout\"}"
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
      }
      def jsonResult = "{\"full_message\": \"Build finished $analysisStatus\", \"buildNumber\": $BUILD_NUMBER, \"message\": \"Build finished $analysisStatus\", \"host\":\"jenkins\", \"facility\":\"test\", \"buildResult\":\"$analysisStatus\", \"type\":\"CI\",\"step\":\"Build\"}"
      echo 'Json Result: ' + jsonResult
      sh "echo -n '$jsonResult' | nc -4u -w1 localhost 12201"
      if (analysisStatus == 'KO') {
        error 'error in Build'
      }
      echo 'Build status: ' + randomResult
    }
    stage('Quality') {
      def analysisStatus = 'OK'
      if (randomResult == 13){
        analysisStatus = 'KO'
      }
      def jsonResult = "{\"full_message\": \"Build finished $analysisStatus\", \"buildNumber\": $BUILD_NUMBER, \"message\": \"Build finished $analysisStatus\", \"host\":\"jenkins\", \"facility\":\"test\", \"buildResult\":\"$analysisStatus\", \"type\":\"CI\",\"step\":\"Quality\"}"
      echo 'Json Result: ' + jsonResult
      sh "echo -n '$jsonResult' | nc -4u -w1 localhost 12201"
      if (analysisStatus == 'KO') {
      }
      error 'error in Quality'
      echo 'Quality status: ' + randomResult
    }
    stage('Publish in Nexus') {
      def analysisStatus = 'OK'
      if (randomResult == 14){
        analysisStatus = 'KO'
      }
      def jsonResult = "{\"full_message\": \"Build finished $analysisStatus\", \"buildNumber\": $BUILD_NUMBER, \"message\": \"Build finished $analysisStatus\", \"host\":\"jenkins\", \"facility\":\"test\", \"buildResult\":\"$analysisStatus\", \"type\":\"CI\",\"step\":\"Publish\"}"
      echo 'Json Result: ' + jsonResult
      sh "echo -n '$jsonResult' | nc -4u -w1 localhost 12201"
      if (analysisStatus == 'KO') {
        error 'error in Publish'
      }
      echo 'Publish status: ' + randomResult
    }
    stage('Build Docker Image') {
      def analysisStatus = 'OK'
      if (randomResult == 15){
        analysisStatus = 'KO'
      }
      def jsonResult = "{\"full_message\": \"Build finished $analysisStatus\", \"buildNumber\": $BUILD_NUMBER, \"message\": \"Build finished $analysisStatus\", \"host\":\"jenkins\", \"facility\":\"test\", \"buildResult\":\"$analysisStatus\", \"type\":\"CI\",\"step\":\"DockerBuild\"}"
      echo 'Json Result: ' + jsonResult
      sh "echo -n '$jsonResult' | nc -4u -w1 localhost 12201"
      if (analysisStatus == 'KO') {
        error 'error in DockerBuild'
      }
      echo 'DockerBuild status: ' + randomResult
    }
    stage('Publish Docker Image') {
      def analysisStatus = 'OK'
      if (randomResult == 16){
        analysisStatus = 'KO'
      }
      def jsonResult = "{\"full_message\": \"Build finished $analysisStatus\", \"buildNumber\": $BUILD_NUMBER, \"message\": \"Build finished $analysisStatus\", \"host\":\"jenkins\", \"facility\":\"test\", \"buildResult\":\"$analysisStatus\", \"type\":\"CI\",\"step\":\"DockerPublish\"}"
      echo 'Json Result: ' + jsonResult
      if (analysisStatus == 'KO') {
        error 'error in DockerPublish'
        sh "echo -n '$jsonResult' | nc -4u -w1 localhost 12201"
      }
      echo 'DockerPublish status: ' + randomResult
    }
    stage('Deploy') {
      def analysisStatus = 'OK'
      if (randomResult == 17){
        analysisStatus = 'KO'
      }
      def jsonResult = "{\"full_message\": \"Build finished $analysisStatus\", \"buildNumber\": $BUILD_NUMBER, \"message\": \"Build finished $analysisStatus\", \"host\":\"jenkins\", \"facility\":\"test\", \"buildResult\":\"$analysisStatus\", \"type\":\"CI\",\"step\":\"Deploy\"}"
      echo 'Json Result: ' + jsonResult
      sh "echo -n '$jsonResult' | nc -4u -w1 localhost 12201"
      if (analysisStatus == 'KO') {
        error 'error in Deploy'
      }
      echo 'Deploy status: ' + randomResult
    }
    stage('Clean') {
      echo 'Clean status: OK'
    }
}
