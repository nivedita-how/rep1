pipeline {
  agent { label 'linux' }
  parameters {
    string(name: 'MESSAGE', defaultValue: 'Hello World', description: 'Message to print')
  }
  stages {
    stage('Checkout') {
      steps {
        git branch: 'main', url: 'https://github.com/nivedita-how/rep1.git'
      }
    }
    stage('Run') {
      steps {
        pwsh "./h1.ps1 -Message \"${params.MESSAGE}\""
      }
    }
  }
}
