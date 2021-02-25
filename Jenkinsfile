node{
	stage('Pull'){
		git url: 'https://github.com/cabral85/udemy-aula-deploy.git'
	}
	stage('Build'){
		sh "/u01/maven/bin/mvn clean package -DskipTests"
	}
	stage('Move'){
		sh "cp -rf target/testeweb.war /data"
	}
	stage('Deploy'){
		sh "/u01/scripts/script_curl.sh"
	}
}