# Standalone
Here are described the steps of how to deploy the [Zeus](https://github.com/dirigiblelabs/zeus) Cloud Management Suite on Standalone server.

## Prerequisites
- Installed Java server - (Tomcat, WildFly, ...).
- Latest version of [Eclipse Dirigible](http://download.eclipse.org/dirigible/).

## Deploy
1. Set the following environment variables:

    `repositoryProviderMaster=git`

    `masterRepositoryGitLocation=https://github.com/dirigiblelabs/zeus_setup.git`

    `masterRepositoryGitBranch=origin/master`

    `masterRepositoryGitTarget=master_git_repository`

2. Deploy the Dirigible _**all-in-one WAR**_ file on the Java server.
3. Start the Java server.

## Access
Open [http://localhost:8080](http://localhost:8080) in your favorite browser.
> **Note:** the port may be different, due to the specific server configurations

## Undeploy
1. Stop the Java server.
2. Undeploy the Dirigible _**all-in-one WAR**_ file.
