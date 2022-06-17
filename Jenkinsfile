pipeline {
    agent { label 'linux-node' }
 

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven3.8.5') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : '3.8.5') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven3.8.5') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
