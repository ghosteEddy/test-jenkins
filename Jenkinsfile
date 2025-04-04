node {
    stage("Warm up"){
        echo("Hello")
    }
    stage("check workpath"){
        sh 'pwd'
        sh 'ls -al'
    }
    stage("Building image"){

        sh 'docker build -t .'
        sh 'docker image ls'
    }
}