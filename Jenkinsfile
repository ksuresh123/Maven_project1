node {
  env.JAVA_HOME="/usr/lib/jvm/java-8-oracle"
  env.M2_HOME="/usr/share/maven"
  env.PATH="${env.JAVA_HOME}/bin:${env.M2_HOME}/bin:${env.PATH}"

  stage('SCM clone'){
  git url: 'https://github.com/ksuresh123/Maven_project1.git'
                    }
  stage('Build'){
  dir('/var/lib/jenkins/workspace/project2') {
  sh 'java -version'
  
  sh 'mvn --version'
  sh 'mvn clean install'

 }
}
  stage('Docker image'){
  sh 'docker build -t image3 .'      
    
  }
  stage('Login'){
  withCredentials([usernamePassword( credentialsId: 'jenkins-docker1', usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD')]) {

docker.withRegistry('', 'jenkins-docker1') {
  sh "docker login -u ${USERNAME} -p ${PASSWORD}" 
}
  }
  }

  
 } 
