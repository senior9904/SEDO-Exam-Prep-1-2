pipeline{
    agent any

    stages{
       
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

/*
Configure Jenkins multibranch pipeline to build the application and execute all of the tests when changes are pushed to the feature and main branches
 */