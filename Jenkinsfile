timestamps {
  timeout(30) {
    node("BuildOnAws"){
      properties([
        parameters([
          string(defaultValue: '', description: 'XYZ', name: 'JAVA_HOME'),
        ])
      ])
      checkout scm
      stage('shell') {
        sh '''
          echo "JAVA_HOME $JAVA_HOME"
          '''
      }
      stage('eval') {
        evaluate(readFile("./eval.groovy"))
      }
    }
  }
}
