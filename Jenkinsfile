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
                bat "go clean"
                bat "go build hello.go"
            }
        }
        stage('Package Chocolatey'){
            steps{
                bat "choco pack --version ${env.JOB_VERSION}"   
            }
        }
        stage('Archive') {
            steps{
               archiveArtifacts("*.exe")
               archiveArtifacts("*.nupkg")
            }
        }
    }
}