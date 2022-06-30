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
    stages{
       stage('Build'){
            steps{
                script{
                    bat "dotnet restore App2/App2.csproj"
                    bat "dotnet build App2/App2.csproj"
                }
            }
        } 
        stage('Deploy'){
            steps{
                script{
                    bat "dotnet publish App2/App2.csproj -c Release -o c:\\plss\\app2"
                }
            }
        }
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
                    bat "dotnet publish App/App2.csproj -c Release -o c:\\plss\\app3"
                }
            }
        }
    }
    
}
