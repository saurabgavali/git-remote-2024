pipeline {
agent any
parameters {
choice(name: 'EnvironmentName', choices: ['dev', 'qa', 'test', 'prod'],
description: 'Enter the Environment to be used.')
}
stages {
stage('Build') {
steps {
echo 'Building..'
echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
}
}
stage('Test') {
steps {
echo 'Testing..'
echo "${params.EnvironmentName} is value retrieved!"
}
}
stage('Deploy') {
steps {
echo 'Deploying....'
}
}
}
}
