pipeline{
    agent {label 'servidor_plss'}
    triggers{
        pollSCM '* * * * *'
    }
    
    enviroment{
        //CAMINHO DO CSPROJ
        CSPROJAPP1 = "App1/App1.csproj"
        CSPROJAPP2 = "App2/App2.csproj"
        CSPROJAPP3 = "App3/App3.csproj"
        //CAMINHO DA ENTREGA
        PUBLISHAPP1 = 
            
        PUBLISHAPP2 =
        PUBLISHAPP3 =
        
    }
    stages('VERIFICANDO ALTERAÇÕES'){
        when{
            branch{'main'
            }
        }
        stage('BUILD APP1'){
            steps{
                script{
                    bat "dotnet restore ${CSPROJAPP1}"
                    bat "dotnet build ${CSPROJAPP1}"        
                }
            }
        }
        stage('DEPLOY APP1'){
            steps{
                script{
                    bat "dotnet publish ${CSPROJAPP1} -c Release -o c:\\plss\\app1"
                }
                
                stage('BUILD APP2'){
            steps{
                script{
                    bat "dotnet restore ${CSPROJAPP2}"
                    bat "dotnet build ${CSPROJAPP2}"        
                }
            }
        }
        stage('DEPLOY APP2'){
            steps{
                script{
                    bat "dotnet publish ${CSPROJAPP2} -c Release -o c:\\plss\\app1"
                }
                
                stage('BUILD APP3'){
            steps{
                script{
                    bat "dotnet restore ${CSPROJAPP3}"
                    bat "dotnet build ${CSPROJAPP3}"        
                }
            }
        }
        stage('DEPLOY APP3'){
            steps{
                script{
                    bat "dotnet publish ${CSPROJAPP3} -c Release -o c:\\plss\\app1"
                }
            }
        }
    }
}
