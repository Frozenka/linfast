LINFAST est un script shell pour faciliter le téléchargement de la dernière version de l'outil d'audit de sécurité linpeas.sh et son exécution simplifié sur une machine cible.

Oui c'est pour les fainéants exactement ! :D 

![til](https://github.com/Frozenka/linfast/blob/dd63823495bd278ef91ab498b112e085041aa882/La%20commande%20est%20automatiquement%20copi%C3%A9e%20dans%20votre%20presse-papiers..gif)


Utilisation :
Pour utiliser le script, exécutez simplement le fichier linfast.sh avec les droits d'administrateur en spécifiant éventuellement l'interface réseau souhaitée (par défaut, l'interface tun0 est utilisée pour les CTF) :

 **Le script va automatiquement copier la commande pour télécharger linpeas sur la machine distante dans votre presse-papiers.**

`sudo ./linfast.sh -i <interface>`

Le script affichera l'adresse IP de l'interface spécifiée et téléchargera automatiquement la dernière version de linpeas.sh depuis GitHub. Il lancera également un serveur web local pour que vous puissiez accéder au fichier téléchargé depuis la machine cible. La commande wget pour télécharger le fichier sera copiée dans le presse-papier pour faciliter le téléchargement du fichier sur la machine cible.

Une fois que vous avez terminé d'utiliser linpeas.sh, vous pouvez arrêter le serveur web en utilisant Ctrl+C. Le script supprime également automatiquement le fichier linpeas.sh lors de l'arrêt du serveur web.

Options
LINFAST prend en charge l'option -i pour spécifier l'interface réseau à utiliser.


-i <interface> : Utiliser l'interface réseau spécifiée (par défaut : tun0)

Dépendances
LINFAST utilise les outils suivants :

- curl pour télécharger le fichier linpeas.sh depuis GitHub
- python3 pour lancer un serveur web local et servir le fichier linpeas.sh
- LINFAST vérifiera si xclip est installé et installera automatiquement le paquet si nécessaire pour copier la commande wget dans le presse-papier.

Avertissement
>LINFAST est un script de preuve de concept et ne doit être utilisé que dans un environnement contrôlé et autorisé. Les auteurs des scripts ne sont pas responsables de >l'utilisation abusive ou illégale de l'outil.

Lien du Git Linpeas : https://github.com/carlospolop/PEASS-ng/
--------------------------------------------------------------------------------------
  

LINFAST :
LINFAST is a shell script to facilitate the download and execution of the latest version of the security auditing tool linpeas.sh on a target machine.
Yes, it's for the lazy ones indeed! :D
  
Usage
To use the script, simply execute the linfast.sh file with administrator rights, optionally specifying the desired network interface (by default, the tun0 interface is used for CTFs):
  
  The script will automatically copy the command to download linpeas on the remote machine to your clipboard.

`sudo ./linfast.sh -i <interface>`

The script will display the IP address of the specified interface and automatically download the latest version of linpeas.sh from GitHub. It will also launch a local web server so that you can access the downloaded file from the target machine. The wget command to download the file will be copied to the clipboard to facilitate the download of the file to the target machine.

Once you're finished using linpeas.sh, you can stop the web server using Ctrl+C. The script will also automatically remove the linpeas.sh file when the web server is stopped.

Options
LINFAST supports the -i option to specify the network interface to use.


-i <interface> : Use the specified network interface (default: tun0)
Dependencies
LINFAST uses the following tools:

- curl to download the linpeas.sh file from GitHub
- python3 to launch a local web server and serve the linpeas.sh file
- LINFAST will check if xclip is installed and will automatically install the package if necessary to copy the wget command to the clipboard.

Disclaimer
>LINFAST is a proof-of-concept script and should only be used in a controlled and authorized environment. The authors of the script are not responsible for the misuse or illegal use of the tool.
  
  Link Git Linpeas : https://github.com/carlospolop/PEASS-ng/
