pipeline{
    agent any

    stages{
        stage('Checkout the code'){
            steps{
                git branch: "master", url: 'https://github.com/senior9904/SEDO-Exam-Prep-1-2.git'
            }
           
        }
        stage('Restore dependencies') {
            steps {
            // runs the dotnet restore command to download/restore the required dependencies of the .NET web app
                bat 'dotnet restore' 
            }
        }
        stage('Build') {
            steps {
                 //  dotnet build command to build the .NET web app
                bat 'dotnet build --no-restore'
            }
        }
        stage('Test') {
            steps {
                bat 'dotnet test'
            }
        }
    }
   
}