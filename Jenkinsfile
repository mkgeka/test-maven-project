def loadValuesYaml(){
  def valuesYaml = readYaml (file: 'config.yaml')
  return valuesYaml;
}

pipeline {
  agent {
    label "jenkins-maven"
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
