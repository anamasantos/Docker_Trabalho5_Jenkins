pipeline{
    agent{ label "linux"}
    stages{
        stage("build"){
            steps{
                git url: 'https://github.com/anamasantos/Docker_Trabalho5_Jenkins', branch: 'main' 

                sh """
                    docker build -t ola_mundo .
                """
            }
        }
        stage("run"){
            steps{
                 sh """
                    docker run -rm ola_mundo
                """
            }
        }
    }
}