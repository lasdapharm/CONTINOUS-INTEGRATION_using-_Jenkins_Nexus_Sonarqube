pipeline {
    agent any
    tools {
        maven "MAVEN3"
        jdk "OracleJDK8"
    }

    environment {
        SNAP-REPO = 'vprofile-snapshot'
        NEXUS-USER = 'admin'
        NEXUS-PASS = 'admin123'
        RELEASE-REPO = 'vprofile-release'
        CENTRAL-REPO = 'vpro-maven-central'
        NEXUSIP = '172.31.15.153'
        NEXUSPORT = '8081'
        NEXUS-GRP-REPO = 'vpro-maven-group'
        NEXUS-LOGIN = 'nexuslogin'
    }

    stages {
        stage('Build'){
            steps{
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
    }
}