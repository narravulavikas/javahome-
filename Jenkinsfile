
node {
   // This is to demo github action	
   def mvn = tool (name: 'M3', type: 'maven') + '/bin/mvn'
   stage('SCM Checkout'){
    // Clone repo
	git branch: 'master',  
	url: 'https://github.com/narravulavikas/javahome-.git'
   
   }
   
	
   stage('Mvn Package'){
	   // Build using maven
	   def mvn = tool (name: 'M3', type: 'maven') + '/bin/mvn'
	   sh "${mvn} package"
   }
   
}
