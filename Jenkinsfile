
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

	stage('email'){
	   mail bcc: '', body: 'successfully completed the task ', cc: '', from: '', replyTo: '', subject: 'hi there !!!!', to: 'vikasnarravula96@gmail.com'
   }
  
	stage('slack'){
	   slackSend channel: '#projectx', color: 'good ', message: 'hi slack configuration ', teamDomain: 'https://hooks.slack.com/services', tokenCredentialId: 'slack', username: 'vikas narravula'
	
   }
}
