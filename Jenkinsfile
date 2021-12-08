pipeline {
    agent {node {label "Jose"}}
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
                docker cp "/root/workspace/se_Jose_Multibranch_BranchIngles/target/sparkjava-hello-world-1.0.war" tomcat_eng:"/usr/local/tomcat/webapps"
                '''
            
          }  
        }
    }
}
