pipeline {
    agent any 
    stages{
        stage('clean Workspace'){
            steps {
                deleteDir()
            }
        }
  
    stage('Build'){
        agent {
            docker {
                image 'node:22-alpine'
                reuseNode true
            }
        }
        steps{
            sh '''
            ls -la
            node --version
            npm --version
            

            ls -la
            '''
        }
    }
}
  }