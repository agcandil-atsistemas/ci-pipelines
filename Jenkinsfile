
def randomResult = new java.util.Random().nextInt(18)

node {
    stage('Checkout'){
        def analysisStatus = 'OK'
        if (randomResult == 11){
          analysisStatus = 'KO'
          error 'error in Checkout'
        }

        echo 'checkout status: ' + randomResult
    }
    stage('Build') {
      def analysisStatus = 'OK'
      if (randomResult == 12){
        analysisStatus = 'KO'
        error 'error in Checkout'
      }

      echo 'Build status: ' + analysisStatus
    }
    stage('Quality') {
      def analysisStatus = 'OK'
      if (randomResult == 13){
        analysisStatus = 'KO'
        error 'error in Checkout'
      }

      echo 'Quality status: ' + analysisStatus
    }
    stage('Publish in Nexus') {
      def analysisStatus = 'OK'
      if (randomResult == 14){
        analysisStatus = 'KO'
        error 'error in Checkout'
      }

      echo 'Nexus status: ' + analysisStatus
    }
    stage('Build Docker Image') {
      def analysisStatus = 'OK'
      if (randomResult == 15){
        analysisStatus = 'KO'
        error 'error in Checkout'
      }

      echo 'Build Docker status: ' + analysisStatus
    }
    stage('Publish Docker Image') {
      def analysisStatus = 'OK'
      if (randomResult == 16){
        analysisStatus = 'KO'
        error 'error in Checkout'
      }

      echo 'Publish Docker status: ' + analysisStatus
    }
    stage('Deploy') {
      def analysisStatus = 'OK'
      if (randomResult == 17){
        analysisStatus = 'KO'
        error 'error in Checkout'
      }

      echo 'Deploy status: ' + analysisStatus
    }
    stage('Clean') {
      echo 'Clean status: OK' 
    }
}
