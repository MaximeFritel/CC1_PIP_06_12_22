# CC1_PIP_06_12_22
Maxime Fritel
CC1 PIP
regarder les images pour voir les captures d'écran

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
trouvé
aws kinesis delete-stream --stream-name Maxime-Fritel-stock-input-stream --region "eu-north-1"


Question 4.2
aws kinesis create-stream --stream-name Maxime-Fritel-stock-input-stream --region "eu-north-1" --shard-count 1

Question 5
modification du fichier stock.py 

lors de l'execution il y a une erreur et je suppose que c'est parce qu'on n'a pas les permissions pour écrire dans le data stream

Pour résoudre le problème il faut lui donner la permission

j'execute les commande suivante trouver sur https://docs.aws.amazon.com/streams/latest/dev/writing-with-agents.html

sudo yum install –y aws-kinesis-agent
sudo yum install –y https://s3.amazonaws.com/streaming-data-agent/aws-kinesis-agent-latest.amzn1.noarch.rpm



