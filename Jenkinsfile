pipeline {
    agent any
    triggers { 
        cron( env.BRANCH_NAME == 'main' && env.GIT_URL.contains('infra') == 'true' ? '0 1 * * 1' : '')
    }
    stages {
        stage('github url') {
            steps {
                echo "${env.GIT_URL}"
            }
        }
    }
}
