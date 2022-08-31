pipeline{
    agent {label 'master'}
    triggers{
        pollSCM '* * * * *'
    }
    
    enviroment{
        //CAMINHO DO CSPROJ
        CSPROJAPP1 = "App1/App1.csproj"
        CSPROJAPP2 = "App2/App2.csproj"
        CSPROJAPP3 = "App3/App3.csproj"
        //CAMINHO DA ENTREGA
        PUBLISHAPP1 = "/testemari/endentrega/app1"   
        PUBLISHAPP2 = "/testemari/endentrega/app2"
        PUBLISHAPP3 = "/testemari/endentrega/app3"
        
    }
    stages('VERIFICANDO ALTERAÇÕES'){
       // When{
       //     branch{''
       //     }
        }
        stage('BUILD APP1'){
            steps{
                script{
                    sh "dotnet restore ${CSPROJAPP1}"
                    sh "dotnet build ${CSPROJAPP1}"        
                }
            }
        }
        stage('DEPLOY APP1'){
            steps{
                script{
                    sh "dotnet publish ${CSPROJAPP1} -c Release -o ${PUBLISHAPP1}"
                }
            }
        }
                
        stage('BUILD APP2'){
            steps{
                script{
                    sh "dotnet restore ${CSPROJAPP2}"
                    sh "dotnet build ${CSPROJAPP2}"        
                }
            }
        }
        stage('DEPLOY APP2'){
            steps{
                script{
                    sh "dotnet publish ${CSPROJAPP2} -c Release -o ${PUBLISHAPP2}"
                }
            }
        }
        stage('BUILD APP3'){
            steps{
                script{
                    sh "dotnet restore ${CSPROJAPP3}"
                    sh "dotnet build ${CSPROJAPP3}"        
                }
            }
        }
        stage('DEPLOY APP3'){
            steps{
                script{
                    sh "dotnet publish ${CSPROJAPP3} -c Release -o ${PUBLISHAPP3}"
                }
            }
        }
    }

