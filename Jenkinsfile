pipeline {
    agent any
    parameters {
        string(name: 'MESSAGE', defaultValue: 'Hello World', description: 'Message to print')
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/nivedita-how/rep1.git'
            }
        }
        stage('Run PowerShell Script') {
            steps {
                pwsh """
                    Write-Host "Running h1.ps1 with MESSAGE='${params.MESSAGE}'"
                    .\\h1.ps1
                """
            }
        }
    }
}
