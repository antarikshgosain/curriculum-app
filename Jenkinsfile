pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/antarikshgosain/curriculum-app', branch: 'master')
      }
    }

    stage('Log') {
      steps {
        sh 'ls -la'
      }
    }

    stage('stats') {
      steps {
        sh '''df -h
free -m
lsblk'''
      }
    }

  }
}