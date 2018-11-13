properties([pipelineTriggers([githubPush()])])
node('linux') {
    git url: 'https://github.com/palj9691/infrastructure-pipeline.git', branch: 'master'
    stage('Test') {
        sh "env"
    }
}
stage ("GetInstances") {

    sh "aws ec2 describe-instances --region us-east-1"
}

stage ("CreateInstance") {
    sh "aws ec2 run-instances --image-id ami-013be31976ca2c322 --count 1 --instance-type t2.micro --key-name TestPractice1 --security-group-ids sg-0709a8356685f2e72 
    -- subnet-id subnet-08c0adad213cb8aad --region us-east-1"

}
