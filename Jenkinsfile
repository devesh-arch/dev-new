node{
   stage('SCM Checkout'){
     git 'https://bitbucket.org/devesh16/devops/src/master/'
	 }
   stage('Compile-Package'){
     def mvnHome = tool name: 'maven3', type: 'maven'
     sh "${mvnHome}/bin/mvn package"
     }
   stage('Email Notification'){
    mail bcc: '', body: '''Hi,
    Welcome to Jenkins email notification.
    Thanks''', cc: '', from: '', replyTo: '', subject: 'Jenkins Job', to: 'devjisuperhit@gmail.com'
    }	 
}