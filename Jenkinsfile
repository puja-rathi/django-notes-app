@Library("shared") _
pipeline {
    agent {label "vinod"}

    stages {
        stage("hello"){
            steps{
                script{
                    hello()
                }
            }
        }
        stage('codeCloning') {
            steps {
                script{
                    clone("https://github.com/puja-rathi/django-notes-app.git", "main")
                }
                
            }
        }
        stage('build') {
            steps {
                
                echo 'code build!!'
                sh "docker build -t notes-app:latest ."
                 echo 'code build succeed!!'
            }
        }
        stage('push') {
            steps {
               
                echo 'code pushed!!'
            }
        }
        stage('deploy') {
            steps {
                // sh "docker run -d -p 8000:8000 notes-app:latest"
                echo 'code deployed!!'
            }
        }
    }
}
