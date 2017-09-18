Le script R permet de créer automatiquement les tables SQL Brut à partir d'un répertoire HDFS. 
Le script parcourt l'ensemble des sous-dossiers du répertoire, pour créer les tables brutes Hive associées au fichier .gz de chaque sous-dossier.
Le nom des table est donné par le nom du sous répertoire.

Pour lancer le script :
- il faut uploader "Create_Table_Hive.tar" directement sur la plate-forme
- ajouter cette commande :

        Rscript Create_Table.R "http://IP_HDFS:PORT_HDFS/webhdfs/v1" "jdbc:hive2://IP_HIVE:PORT_HIVE/;ssl=false" "USER_HDFS" "PWD_HDFS" "NAME_BDD" "PATH_DIRECTORY" "SEPARATOR_FILE" "QUOTE_FILE"