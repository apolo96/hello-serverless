pipeline{
    agent any
    stages{
        stage('build'){
            steps{
                sh "npm install"
            }
        }
        stage('deploy'){
            steps{
                nodejs(nodeJSInstallationName: 'nodejs'){
                    withAWS(credetials: 'aws-credentials'){
                        sh "serverless deploy"
                    }
                }
                
            }
        } 
    }
}