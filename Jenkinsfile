pipeline {
    agent any 
    stages {
        stage('Stage 1') {
            steps {
                echo 'Hello world!' 
            }
        }
        stage('cat README'){
            when {
                branch "dev"
            }
            steps {
                sh '''
                    cat README.md
                    '''
            }
        }
    }
}
