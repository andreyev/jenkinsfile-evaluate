timestamps {
  timeout(30) {
    node("BuildOnAws"){
      properties([
        parameters([
          string(defaultValue: '', description: 'XYZ', name: 'JDK'),
        ])
      ])
      checkout scm
      stage('shell') {
        sh '''
          echo "$JDK"
          '''
      }
      stage('eval') {
        evaluate(readFile("./eval.groovy"))
      }
    }
  }
}
