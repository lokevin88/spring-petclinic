pipeline {
    agent any
    triggers {
      pollSCM('* * * * *')
    }
    stages {
        stage('BUILD') {
            steps {
                sh 'mvn clean install package'
            }
        }
        stage('TEST') {
            steps {
                sh 'mvn clean test'
            }
        }
    }
}
