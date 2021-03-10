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
			sh 'dotnet restore NetCoreTest/NetCoreTest/NetCoreTest.sln'
		}
	}
	stage('Clean solution') {
		steps {
			sh 'dotnet clean NetCoreTest/NetCoreTest/NetCoreTest.sln'
    		}
   	}
        stage('Build Soltuon') {
            steps {
                sh 'dotnet build NetCoreTest\\NetCoreTest\\NetCoreTest.sln --configuraiton release'
            }
        }
    }
}
