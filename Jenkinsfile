stage 'pull updates'
node("docker") {
parallel {
  docker.image('jenkins:latest').pull()
  docker.image('ubuntu:latest').pull()
  docker.image('ubuntu:15.04').pull()
  docker.image('ubuntu:14.04').pull()
  docker.image('centos:centos7').pull()
  docker.image('nginx:latest').pull()
  docker.image('tomcat:8-jre8').pull()
}
}
