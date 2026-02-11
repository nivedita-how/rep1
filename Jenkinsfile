pipeline {
  agent any
  parameters {
    string(name: 'MESSAGE', defaultValue: 'Hello World', description: 'Message to print')
  }
  stages {
    stage('Checkout') {
      steps {
        git branch: 'main', url: 'https://github.com/nivedita-how/rep1.git'
      }
    }
    stage('Sanity: pwsh available?') {
      steps {
        sh 'pwsh --version || (echo "pwsh not found" && exit 1)'
      }
    }
    stage('Run h1.ps1') {
      steps {
        // Run with PowerShell 7 on Linux
        pwsh './h1.ps1 -Message "${params.MESSAGE}"'
      }
    }
  }
}
