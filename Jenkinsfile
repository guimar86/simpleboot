pipeline{
    agent any
    stages{
        stage("Build"){
            steps{

                maven("maven-3.8.4"){
                sh "mvn build"
                sh "mvn clean install"
            }

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