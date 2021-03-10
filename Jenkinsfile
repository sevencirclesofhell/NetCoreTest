pipeline {
    agent any
    stages {
	stage('Scm checkout') {
		steps {
			checkout scm
		}
	}
	stage('Restore packages') {
		steps {
			sh "dot net restore NetCoreTest\\NetCoreTest\\NetCoreTest.sln"
		}
	}
	stage('Clean solution') {
		steps {
			sh "dot net clean NetCoreTest\\NetCoreTest\\NetCoreTest.sln"
    		}
   	}
        stage('Build Soltuon') {
            steps {
                sh "dot net bild NetCoreTest\\NetCoreTest\\NetCoreTest.sln --configuraiton release"
            }
        }
    }
}
