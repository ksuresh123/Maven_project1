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
  sh 'docker build -t suresh123456/image8:3 .'      
    
  }
  stage('Upload image to Gitlab reg'){
        withCredentials([[$class: 'StringBinding', credentialsId: 'jenkins-docker1', variable: 'password']]) {
             sh 'docker login -u suresh123456 -p ${password} https://cloud.docker.com/'
        }  
      }  
  
 } 
