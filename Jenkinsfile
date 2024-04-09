pipeline {
    agent any
    triggers {
        pollSCM 'H 23 * * *'
    }

    stages {
        stage (checkout) {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: 'feature/jenkins-setup']],
                          userRemoteConfigs: [[url: 'https://github.com/markenewcomb/Hazelnut.git']]])
            }
        }
    }
}