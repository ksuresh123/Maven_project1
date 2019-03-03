node {
stage 'checkout'
git url: 'https://github.com/ksuresh123/Maven_project1.git'

stage 'build'
def mvnhome = tool 'M3'
sh "${mvnhome}/bin/mvn clean package"
}
