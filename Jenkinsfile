pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/nivedita-how/rep1.git'
            }
        }

        stage('Run PowerShell Script') {
            steps {
                // For Windows agents with Windows PowerShell:
                // powershell '.\\h1.ps1'
                // If your agent is Linux or uses PowerShell 7 (pwsh), comment the line above and use:
                pwsh './h1.ps1'
            }
        }
    }
}
