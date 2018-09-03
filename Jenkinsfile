node{
   stage('SCM Checkout'){
     git 'https://github.com/moolegovardhan/SampleProject'
   }
   stage('Compile-Package'){
      // Get maven home path
      def mvnHome =  tool name: 'Maven', type: 'maven'   
      sh "${mvnHome}/bin/mvn package"
   }
}
