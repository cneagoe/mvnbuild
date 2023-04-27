node {
    stage('checkout'){
        checkout scm
    }
    stage('mvn build') {
        sh "mvn clean install" 
        sh "ls ./target" 
    }
    stage('artifact creation'){
        archiveArtifacts artifacts: 'target/*.jar', followSymlinks: false
    }
      properties([
        [$class: 'CopyArtifactPermissionProperty', projectNames: 'deployjar'], 
        [$class: 'RebuildSettings', autoRebuild: false, rebuildDisabled: false], 
        pipelineTriggers([])])
}