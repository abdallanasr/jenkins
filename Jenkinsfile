pipeline {
    agent any

    environment {
        JAVA_HOME = "/usr/lib/jvm/java-17-openjdk"
        PATH = "${JAVA_HOME}/bin:${env.PATH}"
    }

    stages {

        stage('Check Java') {
            steps {
                sh '''
                    echo "JAVA_HOME=$JAVA_HOME"
                    java -version
                    javac -version
                '''
            }
        }

        stage('Build') {
            steps {
                sh '''
                    echo "Start Build"
                    # mvn clean package
                '''
            }
        }
    }
}