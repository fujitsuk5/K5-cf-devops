node {
    stage 'Deploy Web App On CloudFoundry'
    wrap([$class: 'CloudFoundryCliBuildWrapper',
        cloudFoundryCliVersion: 'Cloud Foundry CLI (built-in)',
        apiEndpoint: 'https://api.uk-1.paas-cf.cloud.global.fujitsu.com',
        skipSslValidation: true,
        credentialsId: 'CF creds',
        organization: 'YssmW1yI',
        space: 'development']) {

           sh 'cf push gameoflife-dev -p gameoflife-web/target/gameoflife.war'
    }
}
