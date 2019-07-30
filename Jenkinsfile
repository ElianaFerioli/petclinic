pipeline{
    agent any
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
