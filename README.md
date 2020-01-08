# clever-tap
assignment

aws cloudformation create-stack --template-body file://$PWD/infra/vpc.yml --stack-name vpc

aws cloudformation create-stack --template-body file://$PWD/infra/iam.yml --stack-name iam --capabilities CAPABILITY_IAM

aws cloudformation create-stack --template-body file://$PWD/infra/app-cluster.yml --stack-name app-cluster

# Edit the api.yml to update Image tag/URL under Task > ContainerDefinitions and,
aws cloudformation create-stack --template-body file://$PWD/infra/api.yml --stack-name api
