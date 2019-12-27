pipeline {
  agent any
  stages {
    stage('Source') { 
      steps {
		checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/VanisriMurigipudi/jenkins2-course-spring-boot.git']]])
      }
    }
    stage('Compile') { 
      tools {
        // Specify Tool Name from your global tool configuration
		jdk 'JDK8'
        maven 'maven-3'
      }
      steps {
	      // Some Step
	      powershell label: '', script: 'mvn -f spring-boot-samples/spring-boot-sample-atmosphere/pom.xml clean package'
      }
    }
  }
}


