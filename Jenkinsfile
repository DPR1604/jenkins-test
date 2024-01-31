pipeline {
    agent any
    stages {
        stage('Hello') {
            steps {
                echo "hello from Jenkinsfile"
		sh 'env'
            }
        }
    }
    post {
        always {
            discordSend link: env.BUILD_URL, result: currentBuild.currentResult, title: JOB_NAME, webhookURL: '${DISCORD_WEBHOOK}'
        }
    }
}
