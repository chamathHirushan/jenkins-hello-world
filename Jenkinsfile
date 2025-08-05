pipeline {
    agent any

    tools {
        maven "M398"
    }

    stages {
        stage('Echo version'){
            steps{
                bat 'echo print maven version'
                bat 'mvn -version'
            }
        }
        
        stage('Build') {
            steps {
                bat "mvn clean package -Dskiptests=true"
            }
        }

        stage('UnitTest') {
            steps {
                bat "mvn test"
            }
        }
    }
}
