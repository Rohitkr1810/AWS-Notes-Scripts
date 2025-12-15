## create a bucket
aws s3 mb s3://rohit-bucket-policy-example

## create bucket policies
aws s3api put-bucket-policy --bucket rohit-bucket-policy-example --policy file://policy.json

## in the other cross account
aws s3 ls s3://rohit-bucket-policy-example
touch test.txt
aws s3 cp test.txt s3://rohit-bucket-policy-example
aws s3 ls s3://rohit-bucket-policy-example
