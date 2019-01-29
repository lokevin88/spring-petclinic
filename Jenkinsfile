pipeline {
    agent any
    triggers {
      pollSCM('* * * * *')
    }
    stages {
        stage('BUILD') {
            steps {
                sh 'mvn clean install package -Dmaven.test.skip=true'
            }
        }
        stage('TEST') {
            steps {
                sh 'mvn clean test -fn'
            }
        }
    }
}
