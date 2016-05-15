stage 'pull updates'

def dockerImages = ['jenkins:latest','ubuntu:latest','ubuntu:15.04','ubuntu:14.04','centos:centos7','nginx:latest','tomcat:8-jre8']
def stepsForParallel = [:]

for (int i = 0; i < dockerImages.size(); i++) {
  stepsForParallel[dockerImages.get(i)] = transformIntoStep(dockerImages.get(i))
}

parallel stepsForParallel


def transformIntoStep(image) {
    // We need to wrap what we return in a Groovy closure, or else it's invoked
    // when this method is called, not when we pass it to parallel.
    // To do this, you need to wrap the code below in { }, and either return
    // that explicitly, or use { -> } syntax.
    return {
        node('node') {
            docker.image(image).pull()
        }
    }
}
