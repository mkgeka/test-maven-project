def loadValuesYaml(){
  def valuesYaml = readYaml (file: 'config.yml')
  return valuesYaml;
}

pipeline {
  agent {
    label "master"
  }
  stages {
    stage('CICD Initialize') {
      steps {
        script{
          valuesYaml = loadValuesYaml()
          println valuesYaml.getClass()
        }
      }
    }
    stage('Deploy') {
      steps {
        echo valuesYaml.deploy
      }
    }
  }
}
