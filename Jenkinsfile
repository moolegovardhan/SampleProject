node{
   stage('SCM Checkout'){
     git 'https://github.com/moolegovardhan/SampleProject'
   }
   stage('Compile-Package'){
      // Get maven home path
      def mvnHome =  tool name: 'Maven', type: 'maven'   
      bat "${mvnHome}/bin/mvn package"
   }
}
