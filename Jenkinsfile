properties([pipelineTriggers([githubPush()])])
node('linux') {
    git url: 'https://github.com/palj9691/infrastructure-pipeline.git', branch: 'master'
    stage('Test') {
        sh "env"
    }
}
