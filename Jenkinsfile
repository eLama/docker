node('docker') {

    stage('Checkout') {
        checkout scm
    }

    stage('Pull') {
        sh "docker-compose pull"
    }

    stage('Run') {
        sh "docker-compose up -d"
    }
}
