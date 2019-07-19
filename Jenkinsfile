#!groovyâ€‹

pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git credentialsId: 'my-git-secret', branch: 'master',  url: 'https://github.com:vijaysreenivas/java.git'
            }
        }
        stage('Build') {
            steps {
                openshiftBuild bldCfg: 'java-base-builder', checkForTriggeredDeployments: 'false', namespace: 'data', showBuildLogs: 'true', verbose: 'true', waitTime: '30', waitUnit: 'min'
            }
        }
		}
		}
