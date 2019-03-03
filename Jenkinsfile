node {
  env.JAVA_HOME="/usr/lib/jvm/java-8-oracle/jre"
  env.M2_HOME="/usr/share/maven"
  env.PATH="${env.JAVA_HOME}:${env.M2_HOME}/bin:${env.PATH}"

  stage('SCM clone'){
  git url: 'https://github.com/ksuresh123/Maven_project1.git'
                    }
  stage('Copying'){
  dir('/var/lib/jenkins/workspace/project2') {
  sh 'java -version'
  
  sh 'mvn --version'
  sh 'mvn clean install'

 }
}
} 
