# Test_minishell

## Test de base
1) Commandes intégrées :
> echo:
<code>
echo Hello World
echo $USER
echo "Hello    World"
</code>

>  cd:
cd /
cd ..
cd -
cd non_existent_directory

> pwd: (plusieurs changements de répertoire)

> export:
export VAR=value
export VAR="value with spaces"
export VAR=value1 VAR2=value2

> unset:
unset VAR
unset VAR (after use in command)

> env:(show environnement variable.)

> exit:
exit
exit 42

2) Redirections :
> redirections de sortie (>):
echo Hello > file.txt
ls > file.txt

> redirections d’entrée (<):
cat < file.txt

> redirections doubles (>>):
echo Hello >> file.txt

3) Pipes :
> pipes (|)
- simple:
ls | grep file
cat file.txt | wc -l

-Multiples:
cat file.txt | grep Hello | wc -l

## Tests avancés
1) Heredoc : (<<)
cat << EOF
1 ligne
2 ligne
...
EOF

2) Signaux : Ctrl+C, Ctrl+D, et Ctrl+\.
Ctrl+C pour interrompre une commande.
Ctrl+D pour envoyer un EOF.
Ctrl+\ pour quitter une commande.

3) Wildcards : (*, ?).
ls *
ls *.txt
echo *


## Tests manuels
> Erreurs de syntaxe :Gestion d'erreurs de syntaxe.
- Erreurs de syntaxe :
echo "unclosed quote
ls | | grep

> Spécificités du OS

