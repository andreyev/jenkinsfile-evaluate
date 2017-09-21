timestamps {
  timeout(30) {
    node("BuildOnAws"){
      properties([
        parameters([
          string(defaultValue: '', description: 'XYZ', name: 'XYZ'),
        ])
      ])
      checkout scm
      stage('shell') {
        sh '''
          echo "$XYZ"
          '''
      }
      stage('eval') {
        evaluate(readFile("./eval.groovy"))
      }
    }
  }
}
