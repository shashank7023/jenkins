pipeline {
    agent any

    stages {
        stage('chrome') {
            steps {
                sh """ #!/bin/bash
                wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
                sudo apt install ./google-chrome-stable_current_amd64.deb -y
                wget https://chromedriver.storage.googleapis.com/2.41/chromedriver_linux64.zip
                sudo apt-get -y install zip
                unzip chromedriver_linux64.zip
                sudo mv chromedriver /usr/bin/chromedriver
                sudo chown root:root /usr/bin/chromedriver
                sudo chmod +x /usr/bin/chromedriver
                """
            }
        }
    }
}
