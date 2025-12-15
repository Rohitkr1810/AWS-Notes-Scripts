## create a bucket

aws s3 mb s3://metadata-fun-alkfjoru

## create a file

echo "Hello Mars" >> hello.txt

## upload file with metadata
aws s3api put-object --bucket metadata-fun-alkfjoru --key hello.txt --body hello.txt --metadata Planet=Mars

## get head object
aws s3api head-object --bucket metadata-fun-alkfjoru --key hello.txt

## empty the bucket