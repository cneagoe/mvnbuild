node {
    stage('checkout'){
        checkout scm
    }
    stage('Example') {
        sh "mvn clean install" 
        sh "ls ./target" 
    }
}