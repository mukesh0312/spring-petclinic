node {
    stage ('source cod') {
        git branch: 'main', url: 'https://github.com/mukesh0312/spring-petclinic.git'
    }
    
    stage ('build the code') {
        sh 'mvn compile'
    }
}
