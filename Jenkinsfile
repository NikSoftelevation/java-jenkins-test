pipeline {
    agent any
    stages {
        stage('Compile') {
            steps {
                script {
                    def javaHome = tool name: 'JDK', type: 'jdk'
                    if (isUnix()) {
                        sh "${javaHome}/bin/javac Test.java"
                    } else {
                        bat "${javaHome}\\bin\\javac Test.java"
                    }
                }
            }
        }
        stage('Run') {
            steps {
                script {
                    def javaHome = tool name: 'JDK', type: 'jdk'
                    if (isUnix()) {
                        sh "${javaHome}/bin/java Test" // Replace with the actual class name if different
                    } else {
                        bat "${javaHome}\\bin\\java Test" // Replace with the actual class name if different
                    }
                }
            }
        }
    }
}
