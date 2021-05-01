# P10_OC_PROJECT
AWS P10 PROJECT

## Getting Started
Instructions:

Installez un serveur WordPress (le site de l’entreprise) sur AWS en utilisant :

RDS pour le stockage de la base de données

S3 pour le stockage des médias (via le plugin amazon-web-services)

EC2 et Docker pour le serveur web

ELB pour distribuer les requêtes sur les instances EC2

CloudFormation pour automatiser la création de l’infrastructure

Tous les éléments de votre infrastructure publique devront être répartis sur plusieurs zones de disponibilité (multi-AZ). Vous utiliserez le service ELB pour la répartition des requêtes vers les différentes zones de disponibilité (AZ).

Vous monterez une instance EC2 destinée à héberger l’application intranet sur un sous-réseau privé. Dans le cadre de ce cours, le contenu de l’intranet sera une simple page web HTML.

En local sur votre machine, vous créerez deux machines virtuelles Linux : une pour le serveur de fichiers et une pour le serveur VPN.

Vous établirez une liaison VPN entre votre serveur VPN local et le sous-réseau privé AWS via une instance EC2.

Vous mettrez en place de l’auto-scaling sur les instances EC2 pour augmenter le nombre de machines dès que la charge CPU des serveurs atteint 80% en moyenne sur 5 minutes et 

Vous veillerez à être informé par un mail à chaque fois que l'événement survient.

Vous évaluerez les coûts de votre infrastructure AWS à partir de différentes hypothèses d'usage que vous formulerez.

### Prerequisites

L'utilisation du programme nécessite l'acquisition d'un compte Amazon AWS.

Les scripts ont été conçus avec le langage YAML

## Installing & Using

1- Connectez vous à votre console AWS

2- Déployez les scripts dans Cloudformation


## Running the tests

Chaque élément de l'infrastructure a été testé manuellement avant de procéder à leur automatisation

Les instances ec2 ont étés configurés avec une AMI Amazon Linux

La connexion Site to Site a été  établie entre la passerelle VPN AWS et une machine virtuelle PFSENSE 

Le site Wordpress a été installé dans un container Docker via l'image offcielle : https://hub.docker.com/_/wordpress

le plugin WP Offload Media permet la copie automatique des fichiers du site Wordpress vers le bucket S3 : https://fr.wordpress.org/plugins/amazon-s3-and-cloudfront/
## Versioning

Version 1.0 

## Authors

Jean - Samuel BOURGUIT 

Etudiant OpenClassrooms , parcours AIC (Administrateur Infrastuture et Cloud)

## License
    Apache License
    Version 2.0, January 2004
    http://www.apache.org/licenses/
https://www.apache.org/licenses/LICENSE-2.0.txt

