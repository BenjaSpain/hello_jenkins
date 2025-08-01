
Jenkinsfile (Declarative Pipeline)

/* Requires the Docker Pipeline plugin */
pipeline {
    agent { docker { image 'python:3.13.5-alpine3.22' } }
    stage ('build') {
        steps {
            timeout(time: 1, unit: 'MINUTES') {
                retry(2) {
                    sh 'python --version'
                }
            }
        }
    }
}

