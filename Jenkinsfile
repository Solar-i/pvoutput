pipeline {
    agent {
        docker {
            image 'python:3.7.5-buster:latest'
        }
    }
    stages {
        stage ('Test') {
            steps {
                sh "pip install pipenv"
                sh "pipenv install --dev && pipenv run pytest"
            }
        }
        // stage ('Build') {
        //     agent any
        //     steps {
        //         sh "pip install pipenv"
        //         sh "pipenv install --dev && pipenv run python setup.py sdist bdist_wheel"
        //     }
        // }
    }
}