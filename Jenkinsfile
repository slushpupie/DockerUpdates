stage 'pull updates'
node("docker") {
  ["jenkins:latest","ubuntu:15.04","ubuntu:14.04","tomcat:8-jre8","nginx:latest","centos:centos7"].each { 
    echo "Pulling ${it}"
    docker.image(it).pull()
  }
  docker.image('jenkins:latest').pull()
  docker.image('ubuntu:latest').pull()
  docker.image('ubuntu:15.04').pull()
  docker.image('ubuntu:14.04').pull()
  docker.image('nginx:latest').pull()
  docker.image('centos:centos7').pull()
}
