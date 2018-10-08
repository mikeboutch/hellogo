pipeline {
    agent any
    stages {
        stage('init'){
            steps{
                setVerYMX()
            }
        }
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