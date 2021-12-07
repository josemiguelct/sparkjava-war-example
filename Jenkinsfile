pipeline {
    agent {node {label "NodoJose"}}
    stages {
        stage('primeros pasos') {
            steps {
                sh '''
                echo "hola"
                '''
            }
        }
         stage('build') {
            steps {
                sh '''
                mvn clean install
                '''
            }
         }
          stage('deploy') {
            steps {
                sh '''
                docker cp "/root/workspace/Jose_Pipeline/target/sparkjava-hello-world-1.0.war" laughing_pare:"/usr/local/tomcat/webapps"
                '''
            
          }  
        }
    }
}
