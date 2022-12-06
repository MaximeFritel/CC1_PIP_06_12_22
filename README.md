# CC1_PIP_06_12_22
Maxime Fritel
CC1 PIP

Question 1 :
Création terraform modification des fichiers key_pair, main et provider
Terraform plan
Terraform apply
Question 2 :
ssh -i "Maxime-Fritel-key.pem" ec2-user@ec2-13-50-15-86.eu-north-1.compute.amazonaws.com
sudo yum install -y python
sudo yum install -y pip
sudo pip install boto3
scp -i Maxime-Fritel-key.pem stock.py ec2-user@ec2-13-50-15-86.eu-north-1.compute.amazonaws.com:~

Question 3
Console AWS

Question 4.1
aws kinesis delete-stream --stream-name Maxime-Fritel-stock-input-stream
problème de région par défaut qui n'est pas la bonne
Question 4.2
