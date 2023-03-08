pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                 withCredentials([string(credentialsId: 'snyk', variable: 'MY_SECRET')]) {
                    sh '''
                        ./script1.sh
                    '''
                }
            }
        }
    }
}
