node {
	stage("clone the projects"){
		git branch: 'main', url: 'https://github.com/mukesh0312/spring-petclinic.git'
	}

	stage("mvn clean the projects"){
		sh 'mvn clean'
	}

	stage("mvn test the projects"){
		sh 'mvn test'
	}

	stage("mvn test the projects"){
		sh 'mvn package' 
	}

	stage("mvn test the projects"){
		sh 'mvn install' 
	}

	stage("test the projects"){
		junit stdioRetention: '', testResults: '**/surefire-reports/*.xml'
	}

        stage("archive the artifactes"){
        	archiveArtifacts artifacts: '**/*.jar', followSymlinks: false
	}
}
