node {
    stage('download') {
    git branch: 'dev', url: 'https://github.com/venkat9822891/code.git'
     }
    stage('covertartifact') {
    sh 'mvn package'
    }
    stage('deployment') {
    deploy adapters: [tomcat9(credentialsId: '2af07f25-37b9-4aa9-8cc3-65a401b5b732', path: '', url: 'http://172.31.10.58:8080')], contextPath: '/dev-app', war: '**/*.war'
    } 
}
