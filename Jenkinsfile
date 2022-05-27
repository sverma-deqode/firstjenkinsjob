pipeline {
     agent any
     stages {
        stage("Build") {
            steps {
                sh "sudo apt install npm"
                sh " npm run build"
            }
        }
        stage("Deploy") {
            steps {
                sh " rm -rf /var/www/jenkins-react-app"
                sh " cp -r ${WORKSPACE}/build/ /var/www/jenkins-react-app/"
            }
        }
    }
}
