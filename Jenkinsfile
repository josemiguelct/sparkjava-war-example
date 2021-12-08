pipeline {
    agent {node {label "Jose"}}
    stages {
        stage('primeros pasos') {
            steps {
                sh '''
                echo "hola"
                echo $Parameter
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
                docker cp "/root/workspace/FolderJose/Jose_Pipeline/target/sparkjava-hello-world-1.0.war" frosty_dijkstra:"/usr/local/tomcat/webapps"
                '''
            
          }  
        }
    }
}
