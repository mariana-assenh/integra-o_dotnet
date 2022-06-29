pipeline{
    agent {label 'servidor_plss'}
    triggers{
        pollSCM '* * * * *'
    }
    stages{
        stage('Build'){
            steps{
                script{
                    bat "dotnet restore App1/App1.csproj"
                    bat "dotnet build App1/App1.csproj"        
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
