node{
  def app

    stage('Clone') {
        checkout scm
    }

    stage('Build image') {
        app = docker.build("xavki/hello")
    }

    stage('Run image') {
        docker.image('xavki/hello').withRun('') { c ->
        sh 'docker ps'
    }

    }
    
}
