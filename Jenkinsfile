stage 'pull updates'

def dockerImages = ['jenkins:latest','ubuntu:latest','ubuntu:15.04','ubuntu:14.04','centos:centos7','nginx:latest','tomcat:8-jre8']
def stepsForParallel = [:]

for (int i = 0; i < dockerImages.size(); i++) {
  stepsForParallel[dockerImages.get(i)] = node { docker.image(dockerImages.get(i)).pull() }
}

parallel stepsForParallel

