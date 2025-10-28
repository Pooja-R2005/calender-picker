pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/yourname/CalendarPicker.git'
            }
        }
        stage('Build and Run Java') {
            steps {
                bat 'javac CalendarPicker.java'
                bat 'java CalendarPicker'
            }
        }
        stage('Deploy HTML') {
            steps {
                bat 'mkdir output'
                bat 'copy index.html output\\index.html'
            }
        }
    }
}
