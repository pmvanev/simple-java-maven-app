pipeline {
    agent {
        docker {
            image 'maven:3-alpine' 
            args '-v /root/.m2:/root/.m2 --env https_proxy=http://wwwproxy.sandia.gov --env HTTPS_PROXY=http://wwwproxy.sandia.gov' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
