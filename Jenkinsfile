pipeline{
    agent any
    stages {
        stage("first"){
            steps {
                sh "curl -d component=org.springframework.samples:spring-petclinic http://sonar:9000/api/components/show > metrics.json"
                sh "curl -d component=org.springframework.samples:spring-petclinic -d metricKeys=ncloc,complexity,violations >> metrics.json"
                timestamps {
                      logstash{ 
                       cat metrics.json
                      }
                  
                }
            }
        }
    }
}
