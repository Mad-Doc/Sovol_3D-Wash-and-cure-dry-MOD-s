# Sovol_3D-Wash-and-cure-dry-MOD-s

ceci est mon projet complet de modification d'une ancienne station de nettoyage resine 3D  basée sur une vielle station Sovol 3D SL2 !

vous trouverez ici , le code sous arduino IDE + libraire spécifique pour la gesion du moteur pas a pas sur STM8 en lien que j'ai crée spécifiquement 
pour le projet , attention elle ne gere le moteur pas a pas uniquement en vitesse et pas en position !, une version "position" est prévue mais il vous 
faudras patienter ! 

le but est d'utilisé au maximum la base d'origine , a savoir le moteur le boitier et bien entendu le pcb + le stm8 !
quelque modification sont a faire sur le pcb (principalement une inversion du signal step/dir du stm vers le A4988 du a un soucis avec 
la libraire stm8 sduino de géré certain port timer... ) modifier la valeur de pas du A4988 qui est en pas entier d'origine , en 1/8eme de pas
, permet d'avoir une rotation plus fluide en mode CURE et Dry ! 

ajout de deux mosfet sur les sortie PA1 et PA2 (originalement le Xtal, mais non présent donc on soude directement sur les pad libre du pcb

PA1 sert pour commander les LED UV, et PA2 sert a commander les ventillateur pour le mode DRY (si pas besoin de ce mode vous pouvez le désactiver)

il resteras apres le plus "dur" c'est a dire la fabrication d'une potence pour fixé le plateau en mode WASH (d'origine fixé sur le panier dans le bac)
et fixé les led et ventillo !
ma version a ete faite dans un bout d'alu rectangulaire (tube) usiné sur machine outils et peinte en noir , vous pouvez vous en inspiré si vous voulez :) 

pour le mode Cure , il faut crée un plateau rotatif que j'ai désigné , le STL est fournis , ainsi que le stl du spacer au cas ou vous voudriez faire comme moi
+ le stl du cabochon du haut pour fermé le tube ! a imprimé en ABS par exemple (attention au plastique sensible au UV ! )

quelque photo dans le repertoire photo vous montrerons la réalisation afin de vous insipré si besoin ! 

la programmation du stm8 est assez simple , il vous faut au préalable un STlinkv2.0 correctement installer sur votre pc , arduino nano , et sduino en libraire
! choisir stm8s103f6 et stlinkv2.0 , et bien entendu bancher le gnd , le nrst et swin (rien d'autre! ) entre la carte du sovol et le stlink mettre la station sovol en route et lancer l'upload via arduino ide ! je ne vais pas refaire un enieme tuto , on en trouve plein sur le net :) 

ce dépot sera modifier en temps et en heures pour completer ce qui manque et ce , par manque de temps dans l'immédiat 
