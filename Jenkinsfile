pipeline {
    agent any
    stages {
       stage('Build'){
           steps{
            bat "go build"
           }
       }
       stage('Archive') {
           steps{
               archiveArtifacts("*.exe")
           }
       }
    }
}