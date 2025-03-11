pipeline {
    agent any

    triggers {
        githubPullRequest {
            orgWhitelist(['your-github-username'])
            allowMembersOfWhitelistedOrgsAsAdmin()
        }
    }

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/your-username/hello-jenkins-ios.git', branch: 'main'
            }
        }
        stage('Build') {
            steps {
                sh '''
                xcodebuild clean build \
                -project HelloJenkins.xcodeproj \
                -scheme HelloJenkins \
                -sdk iphonesimulator
                '''
            }
        }
    }
}
