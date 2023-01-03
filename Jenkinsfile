#!groovy
@Library(['jenkins-shared-pipelines@saleforces','jenkins-shared-libraries@saleforces']) _
def appData = [failOnSonar: false]



if (env.BRANCH_NAME == "master" || env.BRANCH_NAME == "integration") 
{
echo "Do nothing"
}
else if (env.BRANCH_NAME == "integration-staging" || env.BRANCH_NAME == "prod-santize") 
{
dev_noBuild(appData)
} else {
	dev_salesforce(appData)
}
