pipeline {
    agent any
    triggers { 
        cron(env.BRANCH_NAME == 'main' ? 'H */2 * * *' : '')
    }
    stages {
        stage('github url') {
            steps {
                echo "${env.GIT_URL}"
            }
        }
    }
}
