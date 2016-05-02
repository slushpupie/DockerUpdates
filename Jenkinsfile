stage 'pull updates'
parallel 'updates' {
node("docker") {
  docker.image('jenkins:latest').pull()
}
node("docker") {
  docker.image('ubuntu:latest').pull()
}
node("docker") {
  docker.image('ubuntu:15.04').pull()
}
node("docker") {
  docker.image('ubuntu:14.04').pull()
}
node("docker") {
  docker.image('centos:centos7').pull()
}
node("docker") {
  docker.image('nginx:latest').pull()
}
node("docker") {
  docker.image('tomcat:8-jre8').pull()
}
}
