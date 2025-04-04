def getRepoName() {
    def gitUrl = sh(script: "git config --get remote.origin.url", returnStdout: true).trim()
    return gitUrl.tokenize('/').last().replaceAll(/\.git$/, '')
}

def getBranchName() {
    def branch = sh(script: "git rev-parse --abbrev-ref HEAD", returnStdout: true).trim()
    return branch
}

node {
    stage("Warm up"){
        echo("Hello")
    }
    stage('Checkout') {
        checkout scm
    }
    stage("check workpath"){
        sh 'pwd'
        sh 'ls -al'
    }
    stage("Building image"){
        def repoName = getRepoName()
        def branch = getBranchName()
        sh 'docker build -t ${repoName}:${branch} .'
        sh 'docker image ls'
    }
}