{
    agent:any
    stages{
        stage("A"){
            steps{
                sh "mvn build"
                sh "mvn clean install"
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