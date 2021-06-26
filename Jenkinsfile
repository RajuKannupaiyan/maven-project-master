pipeline{
    agent any
    stages{
        stage("build"){
            steps{
                bat 'mvn clean package'
                bat 'docker build . -t tomcat webapp:${env.BUILD_ID}'
            }
        }
    }
}