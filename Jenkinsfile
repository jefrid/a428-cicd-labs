node {
    stage('Install Node.js and npm') {
        def nodejsVersion = '20.10.0' 
        sh "curl -o /tmp/nodejs.tar.gz https://nodejs.org/dist/v${nodejsVersion}/node-v${nodejsVersion}-linux-x64.tar.gz && tar -C /usr/local --strip-components 1 -xzf /tmp/nodejs.tar.gz"

        sh 'node -v'
        sh 'npm -v'
    }
    stage('Build') {
        sh 'npm install'
    }
    stage('Test') {
        sh './jenkins/scripts/test.sh'
    }
}