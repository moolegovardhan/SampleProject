pipeline{
		agent any
		stages{
			stage('SCM Checkout'){
     git 'https://github.com/moolegovardhan/SampleProject'
   }
   stage('Compile-Package'){
       def mvnHome = tool name: 'Maven', type: 'maven'
       bat '${mvnHome}/bin/mvn package'
   }
}
			stage('Deploy'){
				steps{
				echo 'Code Deployed'
				}
			}
		}
	}
