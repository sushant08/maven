pipeline {
    /* A Declarative pipeline */
    agent any
    stages{
        stage('Build'){
            steps {
                sh 'mvn clean package'
            }
            post {
                success {
                    echo "Archiving artifact.."
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}
