pipeline {
    agent any

    stages {
        stage("Build") {
            steps {
                sh "mvn compile"
            }
        }

        stage("Test") {
            steps {
                wrap([$class: 'Xvfb', debug: true, displayName: 29, displayNameOffset: 0, timeout: 10])
                }
            }
        }

        stage("Publish") {
            steps {
                testNG()
            }
        }
    }
}
