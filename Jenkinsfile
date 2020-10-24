node {
	stage ('Scm Checkout'){
		git 'https://github.com/seshidhark/my-app.git'
	}
	stage ('Compile-package'){
		def mvnhome = tool name: 'maven-3', type: 'maven'
		sh "${mvnhome}/bin/mvn package"
	}
	stage ('Email Notification'){
		mail bcc: '', body: '''Hi Welcome To  Jenkins email alerts 
               Thanks 
               SeshidharDevops ''', cc: '', from: '', replyTo: '', subject: 'Jenkins Job', to: 'seshidharka@gmail.com'
	}
	stage ('Slcak Notfication'){
		slackSend channel: 'jenkinspipeline', color: 'Green', message: 'jenkinspipeline', tokenCredentialId: 'slack-demo-testing', username: 'mychurchtalk'
	}
}
