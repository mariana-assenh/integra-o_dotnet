pipeline{
    agent {
        label 'servidor_plss'
    }
    stages{
        stage('Build'){
            steps{
                script{
                    bat "dotnet restore api1/api1.csproj"
                    bat "dotnet build api1/api1.csproj"        
                }
            }
        }
        stage('Deploy'){
            steps{
                script{
                    bat "dotnet publish App1/App1.csproj -c Release -o c:\\plss\\app1"
                }
            }
        }
    }
}
