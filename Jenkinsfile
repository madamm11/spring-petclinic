pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'echo "Hello World"'
                echo 'Hello again'
            }
        }
		
		stage('Build') {
    steps {
        withMaven(maven: 'maven', mavenSettingsConfig: 'MavenSettingsXML.xml') {
            bat 'mvn -DskipTests clean package'
        }
    }
}
    }
}