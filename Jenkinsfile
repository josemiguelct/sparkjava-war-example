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
                echo "hola"
                '''
            
          }  
        }
    }
}
