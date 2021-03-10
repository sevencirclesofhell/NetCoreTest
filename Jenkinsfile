pipeline {
    agent any
    stages {
	
		stage('Restore packages'){
			steps {
				bat "dot net restore NetCoreTest\\NetCoreTest\\NetCoreTest.sln"
			}
		}
		stage('Clean solution'){
			steps {
				bat "dot net clean NetCoreTest\\NetCoreTest\\NetCoreTest.sln"
			}
		}
        stage('Build Soltuon') {
            steps {
                bat "dot net bild NetCoreTest\\NetCoreTest\\NetCoreTest.sln --configuraiton release"
            }
        }
    }
}
