pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'echo "Hello World"'
                echo 'Hello again'
            }
        }
		
		stage('Build2') {
    steps {
        withMaven(maven: 'maven', mavenSettingsConfig: 'MavenSettingsXML') {
            bat 'mvn -DskipTests clean package'
        }
    }
	stage('Test') {
    steps {
        withMaven(maven: 'maven', mavenSettingsConfig: 'MavenSettingsXML') {
            bat 'mvn test'
        }
    }
}
}
    }
}