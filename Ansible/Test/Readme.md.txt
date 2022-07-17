the pem key is in home directory i.e ~/latest-key.pem, as advised by 

https://stackoverflow.com/questions/58483727/amazon-ec2-error-warning-unprotected-private-key-file-even-after-changing-t

cp pem_key.pem ~
cd ~
chmod 400 pem_key.pem

 ansible-playbook aws.yml -i inventory --private-key ~/latest-key.pem

ssh -i "latest-key.pem" ubuntu@ec2-3-88-191-62.compute-1.amazonaws.com