pipeline{
    agent 
    {
        label "linux-perm-slave-1"
    }

    stages{
        stage('SCM'){
            steps{
                git branch: 'main', url: 'https://github.com/abhay084/git_with_jenkins.git'
            }
        }
        stage('docker build'){
            steps{
                sh 'docker build -t test_image -f Dockerfile .'
            }
        }

    }
}