pipeline {
    agent {
        node {
            label 'nodejs'
        }
    }
    
    stages {
        stage ('clone') {
            steps {
               echo "Hello git clone"
            }
        }
        stage ('build') {
            steps {
                echo "Hello samplesteps for building"
            }
        }
        stage ('test') {
            steps {
                echo "Hello sammple steps under testing"
            }
        }
    }
}
