pipeline {
    agent any
    stages{
        stage("Pull Image") {
            steps{
                app=docker.build("project", "-f project.Dockerfile .")
            }
        }
        stage("Run Image") {
            steps{
                app.run("-dit","--name my-running-app","-p 8080:80")
            }
        }
    }
}
