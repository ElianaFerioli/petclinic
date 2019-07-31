pipeline{
    agent any
    libraries {
	  lib('test@master')
    }
    stages {
        stage("first"){
            steps {
                echo "hola"
            }
        }
    }
    post { 
		always { 				
			influxDbPublisher(selectedTarget: 'prueba_jenkins')
		} 
    }
}
