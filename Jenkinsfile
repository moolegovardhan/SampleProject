pipeline{
	agent any
	stages{
	stage('SCM Checkout'){
   checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'git-creds', url: 'https://github.com/moolegovardhan/SampleProject.git']]])

   }
   stage('Compile-Package'){
       def mvnHome = tool name: 'Maven', type: 'maven'
       bat '${mvnHome}/bin/mvn package'
   }
}
}
