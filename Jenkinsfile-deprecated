node {

    env.NODEJS_HOME = "${tool 'Node 16.x'}"
    env.PATH="${env.NODEJS_HOME}/bin:${env.PATH}"
    sh 'npm --version'

    stage('Install Dependencies') {
        // Run npm install
        sh 'npm install'
    }

    stage('Run Tests') {
        // Run npm test
        sh 'npm test'
    }
    stage('Deploy') {
        sh './jenkins/scripts/deliver.sh'
        input message: 'Finished using the website? (Click "Proceed" to continue)'
        sh './jenkins/scripts/kill.sh'
    }
}