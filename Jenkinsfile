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
            discord: "Jenkins Test", footer: "Footer Text", link: env.BUILD_URL, result: currentBuild.currentResult, title: JOB_NAME webhookURL: ${DISCORD_WEBHOOK}
        }
    }
}
