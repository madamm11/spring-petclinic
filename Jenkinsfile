pipeline {
    agent any

    environment {
        MAVEN_INSTALLATION = 'maven'
        MAVEN_SETTINGS_CONFIG = 'MavenSettingsXML'
    }

    stages {
        stage('Build') {
            steps {
                withMaven(maven: MAVEN_INSTALLATION, mavenSettingsConfig: MAVEN_SETTINGS_CONFIG) {
                    bat 'mvn -DskipTests clean package'
                }
            }
        }

        stage('Test') {
            steps {
                withMaven(maven: MAVEN_INSTALLATION, mavenSettingsConfig: MAVEN_SETTINGS_CONFIG) {
                    bat 'mvn test'
                }
            }
        }
    }
}