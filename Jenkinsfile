node {
    stage("Warm up"){
        echo("Hello")
    }
    stage("Building image"){
        sh 'ls'
        sh 'docker build .'
        sh 'docker image ls'
    }
}