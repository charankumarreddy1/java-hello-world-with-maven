pipeline{
    agent any
    stages{
        stage('checkout'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'github access', url: 'https://github.com/charankumarreddy1/java-hello-world-with-maven.git']]])
            }
        }
        stage('installing'){
            steps{
               sh 'mvn clean install'
            }
        }
    }
}
