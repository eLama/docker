node('docker') {
    env.TAG = nvl(env.TAG, "latest")
    env.IMAGE_NAME = "${env.DOCKER_REGISTRY}/weblate:${env.TAG}"

    stage('Build') {
        sh "docker build --tag ${env.IMAGE_NAME} ."
    }

    stage('Push') {
        sh "docker push ${env.IMAGE_NAME}"
    }
}
