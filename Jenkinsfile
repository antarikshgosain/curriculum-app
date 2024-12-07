pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/antarikshgosain/curriculum-app', branch: 'master')
      }
    }

    stage('Log') {
      parallel {
        stage('Log') {
          steps {
            sh 'ls -la'
          }
        }

        stage('FE unit testing') {
          steps {
            sh '''cd curriculum-front
npm i
npm run test:unit'''
          }
        }

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