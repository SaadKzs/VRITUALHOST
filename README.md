Etapes pour faire un virtual host
Créer les dossiers utiles (LOG) : 
/var/log/apache2/www et /var/log/apache2/blog
/var/www/html/www et /var/www/html/blog
Dans les dossiers www et blog du point 2 il faut faire les index.html


Faire les conf virtual host :
Aller dans etc/apache2/sites-available
Copier la conf existante 000-default-conf : cp 000-default-conf www-woodytoys-lab.conf et cp 000-default-conf blog-woodytoys-lab.conf
Changer les endroits dans les nouvelles conf (blog et www) ou c'est necessaire comme ServerName(le nom du site web ex : toto.woodytoys.lab, DocumentRoot (Mettre le chemin vers l'index.html) etc
Les lancer avec la commande a2ensite blog-woodytoys-lab.conf et a2ensite blog-woodytoys-lab.conf


Aller dans le SOA dans la config woodytoys.lab et ajouter la ligne blog.woodytoys.lab.    IN   CNAME    www.woodytoys.lab.


Tout restart le SOA et le APACHE

Tester sur le client avec links http://www.woodytoys.lab et links http://blog.woodytoys.lab
