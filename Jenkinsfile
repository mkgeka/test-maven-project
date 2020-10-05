@Library('test-pipeline-library') _
import com.example.*

pipeline {
    agent any

    stages {
        new Pipeline(this, "config.yml").execute()
}
