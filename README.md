# Build template recipes for site data

## DEPLOY RECIPES and DEPLOY CODE

Deploy the recipes to generate the data.

The code gets a version on deploy, the manifests get MD5s, and the original data gets an MD5. If the code / manifest / data
combined checksum is different, we need to re-run the generation of the data. Code updates
should be infrequent.

## TODO

TRAVIS-CI deploy to a bucket when the build is OK
Create cloudformation template for buckets / users
Users - one for the travis job, one for the lambda function. Deployment of lambda function controlled elsewhere.