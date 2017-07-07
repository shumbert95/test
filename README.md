#Script de migration KWO#


##Exécution du script :##


php init.php core/app.migrate date_start=%YYYY-mm-dd%

Note : si aucune date n’est remplie, tous les dossiers seront alors migré


##Nomenclature des dossiers de migration :##


Dossier racine : « /lib/core/cli/updates »

Dans lequel se trouvent les dossiers : « letter », « string », « snippet », « sql » et « parameter »

Dans lesquels se trouvent des dossiers datés, exemple :  « 20170510 » (YYYYmmdd)

Chacun des dossiers datés comportent un fichier CSV nommé comme le dossier parent (exemple: « letter.csv », « string.csv » , …)


##Contenu des fichiers CSV :##


CSV | Col 1  | Col 2 | Col 3 | Col 4 | Col 5
--- | --- | --- | --- | --- | ---
snippet.csv  | code | contenu | - | - | -
string.csv  | code | contenu | - | - | -
letter.csv  | code | sujet | contenu | from_email | from_name
parameter.csv  | code | valeur | type (1=TYPE_SINGLE, 2=TYPE_SET, 3=TYPE_HASH) | - | -
sql.csv  | requete | - | - | - | -