pipeline {
    agent { 
        docker {
            image 'docker:dind'
            args '-v /var/run/docker.sock:/var/run/docker.sock -v /var/run/dbus/system_bus_socket:/var/run/dbus/system_bus_socket -e HOME=${workspace}'
        }
    }
    stages {
        stage('build') {
            steps {
                script {
                    docker.build("my-app:latest")
                }
            }
        }
    }
}
