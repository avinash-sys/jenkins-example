pipeline {
    agent any
    def mavenHome = tool name:"maven 3.6.3"
    stages {
        stage ('Compile Stage') {

            steps {
                sh "${mavenHome}/bin/mvn clean compile"
                }
        }

        stage ('Testing Stage') {

            steps {
                sh "${mavenHome}/bin/mvn test"
            }
        }


        stage ('Deployment Stage') {
            steps {
                sh "${mavenHome}/bin/mvn deploy"
            }
        }
    }
}
