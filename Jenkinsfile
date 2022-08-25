pipeline {
     agent any
     stages {
        stage("Build") {
            steps {
                echo "Build Start"
                echo "Build Complete"

            }
        }
        stage("Deploy") {
            steps {
                echo "Deployment Start"
                sh "cd /var/lib/jenkins/jenkins-reactapp-experiment"
                sh "git pull origin master"
                sh "sudo pm2 --name ReactApp start npm -- start"
                echo "Deployment Complete"
            }
        }
    }
}
