pipeline{
    agent any
    stages{
        stage('build'){
            steps{
                script{
                    echo "Build in progress"
                }
            }
        }
        stage('test'){
            steps{
                script{
                    echo "test in progress"
                }
            }
        }
    }
    post {
        success {
            slackSend channel: '#ci_cd', message: "started ${env.JOB_NAME} ${env.BUILD_NUMBER} (<${env.BUILD_URL}|Open>)", teamDomain: 'hossam-6vy2951', tokenCredentialId: 'slack-notification'
        }
        failure {
            slackSend channel: '#ci_cd', message: '"started ${env.JOB_NAME} ${env.BUILD_NUMBER} (<${env.BUILD_URL}|Open>)"', teamDomain: 'hossam-6vy2951', tokenCredentialId: 'slack-notification'
        }
    }
    

}