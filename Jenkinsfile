pipeline{
        agent any
        stages{
            stage('Make Directory'){
                steps{
                    sh "mkdir ~/jenkins-tutorial"
                }
            }
            stage('Make Files'){
                steps{
                    sh "touch ~/jenkins-tutorial/file1 ~/jenkins-tutorial/file2"
                }
            }
                
            stage('Deploy') {
                    steps {
                        sh "sudo docker-compose pull && sudo -E DB_PASSWORD=${DB_PASSWORD} docker-compose up"
                    }
            }
        }
}
