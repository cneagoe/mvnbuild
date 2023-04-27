node {
    stage('checkout'){
        checkout scm
    }
    stage('mvn build') {
        sh "mvn clean install" 
        sh "ls ./target" 
    }
    stage('artifact creation'){
        archiveArtifacts artifacts: './target/*.jar', followSymlinks: false
    }
}