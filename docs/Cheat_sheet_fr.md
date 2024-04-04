# GitHub CLI

# Cheat-sheet des commandes ```gh```

### **authentification**

Se connecter à un compte GitHub:

- ```gh auth login```  
  
Retirer l'authentification à un compte GitHub

- ```gh auth logout``` : 

### **Gestion des dépôt**

Créer un dépôt :

- ```gh repo create [<name>] [flags]``` 

    Options | Description 
    --- | --- 
    ```-p```, ``` --template <repository>``` | Baser le dépôt sur une template
    ```-t```, ``` --team <name>``` | Autoriser l'accès à un groupe ou une organisation
    ```-c```, ``` --clone``` | Cloner le dépôt dans le dossier courant
<br>

Fork un dépôt:

- ```gh repo fork [<repository>] [flags]``` 

Cloner un dépôt : 

- ```gh repo clone <repository> [<directory>]``` 

Voir un dépôt :

- ```gh repo view [<repository>] [flags]``` 

    Options | Description 
    --- | --- 
    ```-b```, ``` --branch <string>``` | Voir une branche du dépôt
    ```-w```, ``` --web``` | Ouvrir un dépôt dans l'explorateur web
<br>

### **Gestion des issues**

Créer une issue :

- ```gh issue create [flags]``` 

    Options | Description 
    --- | --- 
    ```-t```, ``` --title <string>``` | Donner un titre
    ```-l```, ``` --label <name>``` | Ajouter un label par nom
    ```-a```, ``` --assignee <login>``` | Assigner quelqun par leur login. Utiliser "@me" pour l'assigner à soit même
<br>

Lister les issues :

- ```gh issue list [flags]``` 

    Options | Description 
    --- | --- 
    ```-a```, ``` --assignee <string>``` | Filtrer par personne assignée
    ```-A```, ``` --author <string>``` | Filtrer par auteur
    ```-s```, ``` --state <string> (default "open")``` | Filtrer par statut: {open\|closed\|all}
    ```-l```, ``` --label <strings>``` | Filtrer par label
<br>

Afficher le status des issues qui te concerne :

- ```gh issue status``` 

Voir une issue spécifique :

- ```gh issue view {<number> | <url>} [flags]``` 
  
    Options | Description 
    --- | --- 
    ```-c```, ``` --comments``` | Voir les commentaires d'une issue
<br>

Fermer une issue :

- ```gh issue close {<number> | <url>} [flags]```

    Options | Description 
    --- | --- 
    ```-c```, ``` --comment <string>``` | laisser un commentaire de clôture
    ```-r```, ``` --reason <string>``` | Raison de la clôture
<br>

Reouvir une issue :

- ```gh issue reopen {<number> | <url>} [flags]```
 
    Options | Description 
    --- | --- 
    ```-c```, ``` --comment <string>``` | Laisser un commentaire de réouverture
<br>

### **Gestion des pull requests**

Créer une pull request :

- ```gh pr create [flags]``` 

    Options | Description 
    --- | --- 
    ```-B```, ``` --base <branch>``` | La branche dans laquelle vous voulez merge votre code
    ```-f```, ``` --fill``` | Utiliser les infos du commit pour le titre et corps
    ```-l```, ``` --label <name>``` | Ajouter un label par nom
<br>

Lister les pulls request :

- ```gh pr list [flags]``` 

    Options | Description 
    --- | --- 
    ```-a```, ``` --assignee <string>``` | Filtrer par personne assignée
    ```-A```, ``` --author <string>``` | Filtrer par auteur
    ```-s```, ``` --state <string> (default "open")``` | Filtrer par Statut: {open\|closed\|merged\|all}
    ```-l```, ``` --label <strings>``` | Filter par label
<br>

Afficher le status des pull request qui te concerne :

- ```gh pr status``` 
  
Voir une pull request spécifique :

- ```gh pr view {<number> | <url> | <branch>} [flags]```

    Options | Description 
    --- | --- 
    ```-c```, ``` --comments``` | Voir les commentaire d'une pull request
<br>

Voir les détails d'une pull request :

- ```gh pr checkout {<number> | <url> | <branch>}``` 

Merge une pull request :

- ```gh pr merge {<number> | <url> | <branch>}```  

Voir les changements dans une pull request :

- ```gh pr diff {<number> | <url> | <branch>} [flags]``` 

Fermer une pull request :

- ```gh pr close {<number> | <url> | <branch>} [flags]``` 

    Options | Description 
    --- | --- 
    ```-c```, ``` --comment <string>``` | Leave a closing comment
    ```-d```, ``` --delete-branch``` | Supprimer la branche locale et distante aprés la fermeture
<br>

Réouvrir une pull request :

- ```gh pr reopen {<number> | <url> | <branch>} [flags]``` 

    Options | Description 
    --- | --- 
    ```-c```, ``` --comment <string>``` | Laisser un commentaire de réouverture
  
<br>

### **Gestion des workflows**

Lister les fichier workflow , cachant les désactiver par défaut :

- ```gh workflow list [flags]``` 

    Options | Description 
    --- | --- 
    ```-a```, ``` --all``` | Inclure les workflows désactivés

Voir une résumé d'un workflow :

-```gh workflow view [<workflow-id> | <workflow-name> | <filename>] [flags]``` 

Execute un workflow :

- ```gh workflow run [<workflow-id> | <workflow-name>]``` 

Active un workflow, lui permetant d'être exécuté :

- ```gh workflow enable [<workflow-id> | <workflow-name>]``` 

Désactive un workflow, l'empéchant d'être exéctué :

- ```gh workflow disable [<workflow-id> | <workflow-name>]```

<br>
