node ('local'){
    stage ('clone the code'){
        git branch: 'main', url: 'https://github.com/mukesh0312/spring-petclinic.git'
    }
    
    stage ('compile'){
        sh 'mvn compile'
    }
    
    stage ('test'){
        sh 'mvn test'
    }
    
    stage ('package'){
        sh 'mvn package'
    }
    
    stage ('test result'){
        junit stdioRetention: '', testResults: '**/surefire-reports/*.xml'
    }
    
    stage ('build package'){
        archiveArtifacts artifacts: '**/*.jar', followSymlinks: false
    }
}
