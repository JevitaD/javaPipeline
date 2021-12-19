pipeline{
agent {
  label 'Slave_label'
}
stages {
  stage('Gitcheckout') {
    steps {
     git branch: 'main', url: 'https://github.com/JevitaD/javaPipeline'
    }
  }
  stage('build') {
    steps {
      sh 'cd /home/ubuntu/jenkins/workspace/Java_pipeline'
	  sh 'mvn clean install'
    }
  }
  stage('deploy') {
    steps {
      sh 'sudo cp /target/*.war /opt/*.56/webapps'
    }
  }
}
}
