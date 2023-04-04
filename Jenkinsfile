pipeline {
  agent {
    node {  
      label 'jen'
      customWorkspace 'checking mirroring   '
    }
  }
    stages {
        stage('build') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/staging']], extensions: [], gitTool: 'eow2', userRemoteConfigs: [[credentialsId: 'connection', url: 'ssh://git@pm.aspirantlabs.com:39976/root/test.git']]])
            }
        }
        stage('deploy') {
            steps {
               sh "pwd"
               sh "echo testing value"
            }
        }
}
}
