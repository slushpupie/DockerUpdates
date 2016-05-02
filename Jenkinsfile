stage 'pull updates'
  ["jenkins:latest","ubuntu:15.04","ubuntu:14.04","tomcat:8-jre8","nginx:latest","centos:centos7"].each { 
    node("docker") {
      docker.image(it).pull()
    }
  }
