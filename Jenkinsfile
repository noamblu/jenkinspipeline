pipeline{
    agent any
    stages {
        stage("build") {
            sh 'mvn clean package'
        }
        post {
            success {
                echo "Now Archiving..."
                archiveArtifacts artifacts: "**/target/*.war"
            }
        }
    }
}