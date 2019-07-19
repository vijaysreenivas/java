#!groovyâ€‹

pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com:manepallipavankumar/java.git'
            }
        }
        stage('Build') {
            steps {
                openshiftBuild bldCfg: 'java-base-builder', checkForTriggeredDeployments: 'false', namespace: 'data', showBuildLogs: 'true', verbose: 'true', waitTime: '30', waitUnit: 'min'
            }
        }
		}
		}
