pipeline {
  agent { label 'linux' }
    stages {
      stage('GetInstances') {
        steps {
          sh "aws ec2 describe-instances --region us-east-1"
        }
      stage('CreateInstance') {
        steps {
          sh "aws ec2 run-instances --image-id ami-009d6802948d06e52 --count 1 --instance-type t2.micro --key-name pairkedar --security-group-ids sg-6c5f6020 --subnet-d3880eb4 --region us-east-1"
        }
      }
    }
}
