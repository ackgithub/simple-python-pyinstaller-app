pipeline {
    agent { 
        node { 
            label 'docker' 
        } 
    }
    stages {
        stage('Build') { 
            agent {
                node {
                    label 'docker' 
                }
                docker {
                    image 'python:2-alpine' 
                }
            }
            steps {
                sh 'python -m py_compile sources/add2vals.py sources/calc.py' 
            }
        }
    }
}
