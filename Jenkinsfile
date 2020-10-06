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
    stage('test') {
      steps {
        echo valuesYaml.test
      }
    }
    stage('build') {
      steps {
        echo valuesYaml.build
      }
    }
    stage('Deploy') {
      steps {
        echo valuesYaml.deploy
      }
    }
  }
}
