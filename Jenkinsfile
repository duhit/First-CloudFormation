  
@Library('github.com/releaseworks/jenkinslib') _
pipeline {
    agent any
    stages {
        stage('Submit Stack') {
            steps {
                withCredentials([[$class: 'UsernamePasswordMultiBinding', credentialsId: 'aws-key', usernameVariable: 'AWS_ACCESS_KEY_ID', passwordVariable: 'AWS_SECRET_ACCESS_KEY']]) {
            sh "aws cloudformation create-stack --stack-name ec2-single-instance --template-body file://0-ec2-with-sg-eip.yaml --region 'us-east-1'"
                }
              }
             }
            }
            }
