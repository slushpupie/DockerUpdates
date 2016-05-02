parallel 'update': {
  ["jenkins:latest"].each { 
    node("docker") {
      docker.image(it).pull()
    }
  }
}
