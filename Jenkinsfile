pipeline{
    agent any
    def mvnTool="maven-3.8.4"
    stages{
        stage("Build"){
            steps{
                sh " ${mvnTool}/bin/ mvn build"
                sh "${mvnTool}/bin/ mvn clean install"
                
            }
        
            post{
                always{
                    cleanWs()
                }
                success{
                    echo "====++++A executed successfully++++===="
                }
                failure{
                    echo "====++++A execution failed++++===="
                }
        
            }
        }
    }
}