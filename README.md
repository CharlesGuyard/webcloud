# Projet WEBCLOUD du 26/01/2017

# INSTRUCTION DE DÉPLOIEMENT

Projet d'Architecture des Systèmes d'Informations fait par Nicolas DELTHEIL & Charles GUYARD.

Clé SSH: 8d:7d:15:26:77:d4:f2:83:fa:16:e5:e2:5f:d2:9b:90 Mot de passe: isep2017

# Cours du 09/12/2016

Lignes de commande:

    ls /etc man ls find /etc/ -name “*conf” -type f ls /etc/apache2/ telnet localhost:80 apt-get upgrade

Regex : expression régulière, une chaîne de caractères, que l’on appelle parfois un motif, qui décrit, selon une syntaxe précise, un ensemble de chaînes de caractères possibles.

SAAS: Software as a service PAAS: Platform CAAS: Computer IAAS: Infrastructure Exemple: Gmail

Cloud:

Ubuntu = distribution= façon de construire un système d’exploitation

Questions :

Evaluation Individuelle: Créer un dépôt de code sur Github, créer un mini site web (index.html + permettre de le déployer)…? But: Automatisation du déploiement → une ligne de commande qui envoie le fichier zip

Services auxquels on peut faire appel : Digital ocean (on crée une MV; Attention payant 5$ par mois environ), Debian 8, Ubuntu 16,

Login du Prof sur Github: bzg

Nom du dépôt: webcloud

READ ME.md: on accepte lors de la création du dépôt.

SSH Secure Shell

Clé publique :

    /home/[user]/.ssh/id_rsa.pub

utiliser ssh-keygen

Instructions pour l’utilisateur :

Il faut que la personne soit sur Debian 8 ou Ubuntu 16 (Bien penser à implémenter les mises à jour dans les instructions :

Commande pour le devoir : apt-get update upgrade install nginx /etc/init.d/nginx start cp index.html vers le répertoire dans lequel nginx va chercher le site web.

Il faut que tu te connectes sur le ssh root@[adresse.ip] Tu arrives dans le root et là tu fais 2 commandes : 1°) ~$ git clone https://github.com/[user]/webcloud

Dans ce dépôt il y aura les instructions pour pouvoir lancer le script et créer un site web

2°) ~$ ./init shell pour exécuter un script que l’on aura préparé

    init.sh cp index.html

Pré requis pour la suite :

Installer NGINX sur sa VM. lancer le ssh serveur web init.d/nginx blabla

N.B : Lorsqu’on travaille ces lignes de commande et ce projet, au lieu de prendre ses notes sur google docs, les prendre sur GitHub pour qu’il voit ce qu’on fait.

# Cours du 06/01/2017

    apt-get update
    pt-get upgrade 
    apt-get install nginux 
    17806207030
    srd/var/www/html
    nano index html 

    ns cron

    cd (répertoire user)
    nano date sh
    #!/bin/bash
    echo `date`
    Ctrl+ O (enregistrer)
    Ctrl+ x (sortir)
    chmod +x date sh
    ./date sh 

# Cours du 16/01/2017

    permissions

r=read 4, w=write 2, x=executer 1 choown : changer l’utilisateur chmod : changer les permisions du fichier

stdin/stdout/stderr

entrée standard : stdin sortie standard : stdout

cron : lancer des taches à des periodes régulières

    Pipe

rediriger la sortie standards et en faire l’entrée standard du prochain programme

   organosation sys fichiers unix
    script de deploiement : script bash dans compte git, cloner ça et se connecter en ssh à une adresse IP pour executer le code en bash qui va sur la machine distante : mettre à journ installer un serveur,copier un fichier index html

        drwx------   5 charlesguyard  staff   170 20 fév  2016 Applications
        drwx------+ 10 charlesguyard  staff   340 16 jan 09:22 Desktop
        drwx------+ 12 charlesguyard  staff   408 10 jan 13:49 Documents
        drwx------+ 13 charlesguyard  staff   442 16 jan 09:21 Downloads
        drwx------@  7 charlesguyard  staff   238 15 jan 13:27 Dropbox
        drwx------@  9 charlesguyard  staff   306 15 jan 13:27 Google Drive
        drwx------@ 71 charlesguyard  staff  2414 31 déc 14:56 Library
        drwx------+  4 charlesguyard  staff   136  7 oct 21:30 Movies
        drwx------+  8 charlesguyard  staff   272 19 sep 21:28 Music
        drwx------+ 20 charlesguyard  staff   680 28 déc 14:15 Pictures
        drwxr-xr-x+  6 charlesguyard  staff   204 11 oct  2015 Public
        -rw-r--r--   1 charlesguyard  staff     0 16 jan 10:20 fichier.txt
        drwxr-xr-x   4 charlesguyard  staff   136 13 jan 14:17 git
        -rw-r--r--   1 charlesguyard  staff     0 16 jan 10:21 test.sh


    MacBook-Pro-de-CharlesG-4:~ charlesguyardl$ chmod 764
    usage:  chmod [-fhv] [-R [-H | -L | -P]] [-a | +a | =a  [i][# [ n]]] mode|entry file ...
        chmod [-fhv] [-R [-H | -L | -P]] [-E | -C | -N | -i | -I] file ...

#!/bin/sh

  echo -n "Entrez un nom de fichier: " read file if [ -e "$file" ]; then echo "Le fichier existe!" else echo "Le fichier n'existe pas, du moins n'est pas dans le répertoire d'exécution du script" fi exit 0

github -> deploy.sh ->

# !/bin/bash
remplacer « xxxx » par l’adresse IP de notre droplet

        tail –n +3 « $ø »    ssh root@xxxx.xxxx   ; exit 
        set –ev

uptate les serveurs

        apt –get update 

send the list of process to /var/ww/index.html

    ps>w/html/index.html
