pipeline{
    agent any

    stages{

        stage("sonar quality status"){
            agent {label 'docker'}
            steps{
                script{
                    withSonarQubeEnv(credentialsId: 'sonar-token') {
                        sh "mvn clean package sonar:sonar  "
                    }
                }
            }
        }
    }
}
