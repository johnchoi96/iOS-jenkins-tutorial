pipeline {
    agent any
    triggers {
        pipelineTriggers([
            githubPullRequest()
        ])
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
            }
        }
    }
}
