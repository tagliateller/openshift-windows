az group create --name originwinrg --location eastus

az group deployment create -g originwinrg --name originwincluster --template-uri https://raw.githubusercontent.com/tagliateller/openshift-origin/master/3.11/azure/twonode.json --parameters @./azuredeploy.parameters.3.11.local.json --no-wait