@Library('test-pipeline-library') _
import com.example.*

pipeline {
    agent any

    stages {
        stage('Clone sources') {
            steps {
                git url: 'https://github.com/Brialius/test-maven-project.git'
            }
        }
    }
}
new Pipeline(this, "config.yml").execute()
