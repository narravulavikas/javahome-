
node {
   // This is to demo github action	
   stage('SCM Checkout'){
    // Clone repo
	git branch: 'master',  
	url: 'https://github.com/narravulavikas/javahome-.git'
   
   }
   
	
   stage('Mvn Package'){
	   // Build using maven
	   def mvn = tool (name: 'M3', type: 'maven') + '/bin/mvn'
	   sh "${mvn} clean package"
   }

	stage('archive'){
	   sh 'bin/makeindex'
	   archiveArtifacts 'index.jsp'
   }
   
}
