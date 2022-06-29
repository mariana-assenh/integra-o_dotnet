pipeline{
    agent any
    stages{
        stage('Build'){
            step{
                script{
                    bat "dotnet restore api1/api1.csproj"
                    bat "dotnet build api1/api1.csproj"        
                }
            }
        }
    }
}
