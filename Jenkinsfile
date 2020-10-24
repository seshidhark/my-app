node {
	stage ('Scm Checkout'){
		git 'https://github.com/seshidhark/my-app.git'
	}
	stage ('Compile-package'){
		def mvnhome = tool name: 'maven-3', type: 'maven'
		sh "${mvnhome}/bin/mvn package"
	}
}
