node{
  def app

    stage('Clone') {
        checkout scm
    }

    stage('Build image') {
        app = docker.build("xavki/hello")
    }

    stage('Run image') {
				agent {
        	docker {
          	image 'xavki/hello'
					}
				}

    }
    
}
