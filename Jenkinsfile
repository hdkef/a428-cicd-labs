node {

    env.NODEJS_HOME = "${tool 'Node 18.x'}"
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
}