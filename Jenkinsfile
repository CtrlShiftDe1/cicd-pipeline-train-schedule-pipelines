pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
              sh './gradlew build --no-daemon'
              archiveArtifacts artifact: 'dist/trainSchedule.zip'
            }
        }
        stage('Deploy') {
            steps {
              input message: 'Deploy now?'
                echo 'Deploying....(this doesnt actually do anything)'

            }
        }
    }
}
