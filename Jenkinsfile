timestamps {
  timeout(30) {
    node("BuildOnAws"){
      properties([
        parameters([
          string(defaultValue: '', description: 'XYZ', name: 'XYZ'),
        ])
      ])
      checkout scm
      stage('Running Selenium') {
        sh '''
          echo "$XYZ"
          '''
      }
    }
  }
}
