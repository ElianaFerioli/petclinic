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
	        step([$class: 'InfluxDbPublisher',
                customData: null,
                customDataMap: null,
                customPrefix: null,
                //jenkinsEnvParameterTag: 'KEY=' + env.BUILD_NUMBER,
                jenkinsEnvParameterField: 'environment=preproduction',
                measurementName: 'prueba_jenkins',// OPTIONAL, custom fields
                target: 'prueba_jenkins'])
		} 
    }
}
