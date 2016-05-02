parallel 'update': {
  ["jenkins:latest"].each { imageName ->
    node("docker") {
      docker.image(imageName).pull()
    }
  }
}
