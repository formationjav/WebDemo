Installer Python (à partir de python.org) : ceci devrait aussi installer pip[3]
Ajouter le répertoire bin de Python au Path
Vérifier l’installation en ouvrant un terminal de commande Windows (cmd) et taper les commandes suivantes pour faire afficher les versions :

* python -V

* pip -V

Ensuite installer le Robot Framework en utilisant pip :

* pip install robotframework

Pour les tests de la web app, la librarie Selenium est requise :

* pip install robotframework-seleniumlibrary

* La librairie Selenium a besoin des pilotes web (webdrivers) qui doivent alors être installés séparément
 pour chaque fureteur que l’on souhaite utiliser en test. 
 Pour le fureteur Chrome, télécharger le pilote ici : https://sites.google.com/a/chromium.org/chromedriver/downloads.
Il s’agit simplement de décompresser le fichier.exe et le copier dans un répertoire qui est ajouté au Path.

**  pip install webdrivermanager

**  webdrivermanager firefox chrome --linkpath /usr/local/bin
*  Add du PATH  OS /usr/local/bin

** robot --variable BROWSER:Chrome login_tests

### Running tests
The test cases are located in the login_tests directory. They can be executed using the robot command:

robot login_tests
