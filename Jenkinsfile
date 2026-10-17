@Library('jenkins-shared-library@main') _

def configMap = [
    project   : "roboshop",
    component : "shipping"
]

def branchName = env.BRANCH_NAME ?: ''

echo "BRANCH_NAME = ${branchName}"

if (!branchName.equalsIgnoreCase('main')) {
    javaEKSPipeline(configMap)
} else {
    echo "Please proceed with PROD process"
}