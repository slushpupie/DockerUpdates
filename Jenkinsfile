stage 'pull updates'
node("docker") {
  ["jenkins:latest","ubuntu:15.04","ubuntu:14.04","tomcat:8-jre8","nginx:latest","centos:centos7"].each { 
    echo "Pulling ${it}"
    docker.image(it).pull()
  }
}
