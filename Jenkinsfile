node {

    checkout scm

    docker.withRegistry('https://registry.hub.docker.com', 'dockerHub') {

        def customImage = docker.build("rupsdan/dockerwebapp123")

        /* Push the container to the custom Registry */
        customImage.push()
    }
}
