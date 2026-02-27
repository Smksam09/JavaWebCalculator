pipeline {
    agent any

    stages {
        stage('Git-checkout') {
            steps {
                echo 'I am cloning the repository'
				checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/prudhvisurya996/JavaWebCalculator.git']])
            }
        }
		stage('validate') {
            steps {
                echo 'I am running mvn validate'
				sh 'mvn validate'
            }
        }
		stage('complie') {
            steps {
                echo 'I am running mvn compile'
				sh 'mvn compile'
            }
        }
		stage('test') {
            steps {
                echo 'I am running mvn test'
				sh 'mvn test'
            }
        }
		stage('package') {
            steps {
                echo 'I am running mvn package'
				sh 'mvn package'
            }
        }

    }
}
