node {
    stage("Warm up"){
        echo("Hello")
    }
    stage("Building image"){
        sh 'docker build .'
        sh 'docker image ls'
    }
}