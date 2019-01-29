pipeline {
    agent any
    triggers {
      pollSCM('* * * * *')
    }
    stages {
        stage('BUILD') {
            steps {
                sh 'mvn install package -Dmaven.test.skip=true'
            }
        }
    }
}
