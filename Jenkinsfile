pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'rm -rf build'
                sh 'mkdir build' 
                sh 'touch build/test.txt'
                sh 'echo "start" > build/test.txt'
            }
        }
        stage('Test') {
            steps {
                sh 'test -f build/test.txt' 
                sh 'grep "start" build/test.txt'
            }
        }
    }
}
