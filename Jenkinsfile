pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                 withCredentials([string(credentialsId: 'snyk', variable: 'MY_SECRET')]) {
                    sh '''
                        echo $MY_SECRET
                        ./script1.sh
                        ./script2.sh
                    '''
                }
            }
        }
    }
}
