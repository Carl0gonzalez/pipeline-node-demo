pipeline {
  agent any
  tools {
    nodejs 'NodeJS_20'
  }
  stages {
    stage('Clonar') {
      steps {
        git 'https://github.com/brayandiazc/pipeline-node-demo.git'
      }
    }
    stage('Instalar dependencias') {
      steps {
        sh 'npm install'
      }
    }
    stage('Pruebas') {
      steps {
        sh 'npm test'
      }
    }
  }
  post {
    success {
      echo "🎉 Pipeline Node ejecutado con éxito"
    }
    failure {
      echo "💥 Falló el pipeline"
    }
  }
}