Octocat
Dossier de rendu : https://rendu-svn.etna-alternance.net/v2/2020_Prep'ETNA_FDI-DEVC_5_0-1417/Octocat/moriss_a

Nom du binaire: octocat

Fonction autorisées:

getchar();
my_putchar();
open();
read();
close();
malloc();
Cours associés: Vidéos Piscine C + Vidéos de cours associées au projet

Le projet octocat est un projet où vous allez découvrir (ou non) l'Existence d'un nouvel animal : l'octocat

L'image d'un octocat
Le projet en lui même peut-être réalisé rapidement. Toutefois, une partie de la notation portera sur la manière dont vous vous êtes approprié le sujet et donc sur les bonus que vous aurez réalisé.
Le projet octocat consiste à réaliser un jeu de labyrinthe.

Le joueur devra mener son personnage de l'entrée du labyrinthe jusqu'à la sortie. (captain obvious: on vous parle d'octocat depuis le début. Le personnage sera donc... un octocat.)

Vous devrez réaliser plusieurs modes de jeu (vous êtes libres d'en créer autant d'autres que vous voudrez ^_^)

Ces deux modes de jeux auront la particularité de pouvoir être joués de deux manières différentes :

Mode Casu
Le mode casu est un mode de jeu où le joueur effectue un déplacement par tour.

A chaque tour, le joueur effectue une entrée et cela le fait se déplacer d'une case dans cette direction.

Il est demandé au joueur de rejouer tant qu'il n'a pas atteint la sortie.

Si celui-ci rencontre un mur, la partie s'arrête.

Exemple

                [...]
                ####
                #
                8 ##
                ## #
                player ? : d

                ####
                #
                 8##
                ## #
                player ? : w

                ####
                #8
                  ##
                ## #
                player ? : d

                ####
                # 8
                  ##
                ## #
                player ? : w

                Vous vous êtes pris un mur...
                Rejouer ? (o/N)

                [...]
            
Mode Hardcore
Le mode Hardcore est un mode de jeu où le joueur entre, sur l'entrée standard, tout le trajet qu'il veut effectuer en une seule fois.

Celui-ci doit entrer l'itinéraire menant à la sortie sans rencontrer de mur sur le trajet.

Si l'itinéraire ne mène pas jusqu'à la sortie, il est signalé au joueur qu'il s'est perdu et qu'il s'est fait mangé par un Grievers

Comme dans le mode casu, si celui-ci rencontre un mur, il tombe KO (et cela lui est signalé bien entendu).

Exemple


                000000000000000
                8  00     00 00
                00 00 000 00 00
                00 00 00     00
                00    000000 00
                00000     00
                000000000000000
                player ? : ddsssdddwwwddddssdddssdd

                YOU DID IT!!! YOU'RE OUT \o/
            
Bonus
Comme dit plus haut, une partie de la notation portera sur les bonus. N'hésitez donc pas et rendez votre jeu original !

Voici une petite liste pour ceux qui n'aurait pas d'idée ;-P

Nom	Feature
Multimap	Pouvoir jouer sur plusieurs map (à charger depuis un fichier externe ?)
Mode Blind	Un mode où le joueur ne voit pas la map (il doit se prendre des murs et recommencer encore et encore)
Mode Octoview	Un mode où le joueur ne voit que les 8 cases autours de lui
Highscore, de la couleur et de l'ascii art... Surprenez nous !!!

La correction s'effectuant à distance, vous devrez réaliser un fichier README (ou README.md pour les plus téméraires) qui présentera et expliquera tout bonus que vous aurez réalisés.
Astuce de développement
Rassurez-vous, ce n'est pas une nouvelle partie qui ajoute de la complexité au projet mais une liste de bonnes pratiques afin de vous facilitez la vie.

Version : Faites des messages de commit clair et précis. Si en plus vous tenez à jour votre README (en indiquant les modifications entre les versions), vous pourrez plus facilement travailler à plusieurs sur votre dépôt SVN.
Mettez également des tags de versions dans vos messages de commit (exemple : "[v1]", "[v1.1]", "[v2]" en début de message de commit). Changez le premier chiffre de la version quand ce que vous avez fait peut casser le code de vos binômes.
Exemple : Dans la v1 du projet, la map est un char[10][10] avec les valeurs en dur dans le code. Dans la v1.4, la map est lu dans un fichier externe et toujours stocké dans un char** mais dans la v2.0 elle est ensuite stocké dans une liste chainée. Le binôme sait donc qu'il y a eu un changement majeur et qu'il faut lire le message de commit ou le readme parce que ce qu'il est en train de faire ne va peut-être plus fonctionner.

Bloc Fonctionnel : Nous ne reviendrons jamais assez dessus, mais faites des gros bloc indépendant dans votre programme.
L'exemple de version précédent ne pose du coup aucun problème. Le bloc "gestion de la map" et "lecture de l'entrée utilisateur" peuvent très bien être developpés en parallèle sans que l'un n'influe sur l'autre. Deux personnes différentes peuvent donc s'occuper chacun d'une partie.
