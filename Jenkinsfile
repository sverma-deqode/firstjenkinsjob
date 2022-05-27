pipeline {
     agent any
     stages {
        stage("Build") {
            steps {
                sh " npm install"
                sh " npm run build"
            }
        }
        stage("Deploy") {
            steps {
                sh " sudo -A chmod -R 777 /var/www/jenkins-react-app"
                sh " rm -rf /var/www/jenkins-react-app"
                sh " cp -r ${WORKSPACE}/build/ /var/www/jenkins-react-app/"
            }
        }
    }
}
