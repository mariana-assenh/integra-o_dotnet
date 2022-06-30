pipeline{
    agent {label 'servidor_plss'}
    triggers{
        pollSCM '* * * * *'
    }
    stages{
        stage('Build'){
            steps{
                script{
                    bat "dotnet restore App3/App3.csproj"
                    bat "dotnet build App3/App3.csproj"        
                }
            }
        }
        stage('Deploy'){
            steps{
                script{
                    bat "dotnet publish App3/App3.csproj -c Release -o c:\\plss\\app3"
                }
            }
        }
    }
}
