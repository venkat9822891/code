node {
    stage('download') {
    git branch: 'test', url: 'https://github.com/venkat9822891/code.git'
     }
    stage('covertartifact') {
    sh 'mvn package'
    }
    stage('deployment') {
    deploy adapters: [tomcat9(credentialsId: 'e15b8e00-4d0a-4ac6-94b5-85da527a63be', path: '', url: 'http://172.31.2.53:8080')], contextPath: '/test-app', war: '**/*.war'
    } 
}
