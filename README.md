# CSV_sqlite_C_HowTo
Traitements de CSV en C avec sqlite3

## Outils nécessaires sous Windows
- Installer Notepad++ : https://notepad-plus-plus.org/download 
- Installer le plugins NppExec pour Notepad++ : https://sourceforge.net/projects/npp-plugins/files/NppExec/
  - Copier NppExec.dll dans le répertoire ./plugins de l'installation de Notepad++)
  - NppExec permet de compiler à partir de Notepad++ (touche F6). Le script suivant est nécessaire. 
  Il est modifiable en fonction des options de compilsation désirées : 
  >npp_save  
  cd  "$(CURRENT_DIRECTORY)"  
  gcc  "$(FILE_NAME)" sqlite3.c -o $(NAME_PART) -g -lm  
  NPP_RUN  $(NAME_PART)  
- Compilateur GCC MinGW pour Windows : https://osdn.net/projects/mingw/releases/
  - Installer (par exemple dans `c:\MinGW`)
  - configurer le PATH `c:\MinGW`
- sqlite3 : https://www.sqlite.org/download.html
  - Dans un répertoire (par exemple c:\sqlite) placer `sqlite3.def`, `sqlite3.dll` 
  (Precompiled Binaries for Windows 32-bit) et `sqlite3.c` (amalgamation)
  - Placer les fichiers `sqlite3.h` et `sqlite3ext.h` du pack amalgamation dans le répertoire `./include` 
  du compilateur GCC. Ils sont nécessaires pour la compilation avec sqlite.
  - Configurer le PATH `c:\sqlite`
- Installer sqlite Studio : https://sqlitestudio.pl

## Outils nécessaires sous Windows
- Travailler à partir de fichiers CSV encodage ANSI
  - Pour les fichiers Excel, les exporter en CSV (séparateur ;)
- Importer les fichiers CSV à l'aide de sqlite Studio
  - menu `tools` `import`
  - Dans les options, sélectionner `CSV`, texte codé `system`, séparateur `;`
  - Vérifier le bon import : Un export CSV doit permettre de générer le fichier source à l'identique

## Code C
- Exemples d'utilisation sqlite en C ici : https://www.tutorialspoint.com/sqlite/sqlite_c_cpp.htm
- L'écriture des fichiers en C sera faite en encodage UTF8 (sans BOM) (par défaut, c'est le cas, mais il vaut mieux vérifier)

  


