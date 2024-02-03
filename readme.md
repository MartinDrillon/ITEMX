<h1 align="center">ITEMX</h1>

***

ITEMX est un clavier en deux parties de 46 touches fonctionnant avec ZMK et utilisant une SEEED XIAO BLE comme microcontrolleur. Il a été entièrement conçu avec [Ergogen](https://github.com/ergogen/ergogen).

C’est la quatrième itération d’un projet dont le but est de créer un clavier ergonomique ayant 5 touches de pouces par main et utilisant une répartitions des caractères adaptés du [BÉPO](https://bepo.fr/wiki/Accueil). 

_Bien que cette version soit parfaitement fonctionnelle, il demeure quelques défauts. Une cinquième version devrait voir le jour prochainement._

***

![ITEMX](/docs/images/ITEMX1.JPG)
***
![ITEMX3](/docs/images/key3.png)
***
![ITEMX2](/docs/images/ITEMX2.JPG)
***

Ce clavier fonctionne avec une disposition dérivée du BÉPO. Pour être exact, il s’agit d’une adaptation du travail de Kawamashi publié [ici](https://forum.bepo.fr/viewtopic.php?id=1696). Après presque deux ans d’utilisation, il ne fait aucun doute pour moi que cette disposition est très largement supérieure à l’azerty pour la frappe du français (et de tout type de language), autant en terme de confort que de rapidité. Le seul avantage indéniable à l’azerty est celui de l’habitude et de la relative difficulté à apprendre une nouvelle disposition.

Sa particularité, par rapport à d’autres claviers ergonomiques de ce genre ([KYRIA](https://github.com/foostan/crkbd), [LILY58](https://github.com/kata0510/Lily58)) dont il s’inspire, est d’avoir au total 10 touches de pouces toutes accessibles en déplaçant uniquement le doigt et non l’ensemble de la main (touch typing). Une touche de pouce spécifique peut être attribuée pour chaque par modifiers de base (shift, ctrl, alt pour la mains gauche et shift, altgr, win pour la droite) en plus de quelques caractères très fréquemment utilisés. Cela permet d’utiliser la moitié gauche du clavier comme un macropad lors de l’utilisation de logiciels de DAO/CAO nécessitant un usage intensif de combinaison à base de schift, ctrl, alt, alt+ctrl...

Le principe qui dicte cette configuration physique est le suivant : **À condition d’avoir une touche accessible en touch typing, il est toujours plus simple de donner un imput par la simple pression d’un doigt plutôt que d’avoir recours à une combinaisons** (mod-tap, hold-tap, homerows mods... voir la documentation de [ZMK](https://zmk.dev/docs) sur les comportements possibles). Cettre rêgle est d’autant plus importante lorsque l’imput de base joue lui-même régulièrement un rôle dans une combinaison. Toutes les configurations alternative à l’utilisation d’une touche dédiée uniquement à un modifier entrainent systématiquement soit des compliquations, soit des erreurs de frappe occasionelles, soit les deux.

***

## DISPOSITION DES CARACTÈRES

**Niveau de base**

![BASE](/docs/images/1x/BASE.png)
_La disposition des lettres de base est convaincante et ne devrait pas être changé. Quelques légères modifications pourraient toutefois être effectué par un usager souhaitant taper occasionnellement en anglais. Les signes de ponctuations par contre, en particulier les signes schifté, seront peut-être remplacé par des cumbos dans le futur._ 

***

**Cumbo**

![CUMBO](/docs/images/1x/CUMBO.png)

_Afin de renforcer la possibilité d’utiliser la partie gauche du clavier comme un macropad, les cumbos invoquant des raccourcis claviers classique (ctrl+z/c/v...) se situent sous la main gauche. Les cumbos invoquant des caractères spéciaux sont à droite. À noter que dans le cas d’un utilisateur gaucher, il faudrait les inversers, ainsi d’ailleur que les modifiers placé sous les pouces gauches et droits._
_Cette partie de la disposition me semble plus personnelle et peux faire l’objet de changement régulier._

***

**Sym**

![SYM](/docs/images/1x/CUMBO.png)
_Ce niveau était relativement 
***

## ITEMX AVEC ZMK

[ZMK](https://github.com/MartinDrillon/zmk-config-ITEMX)

**Note sur l’utilisation du bépo avec ZMK**

Contrairement à QMK, ZMK ne propose pas de fichier à inclure dans son keymap pour le faire correspondre au driver clavier qu’utilise votre ordinateur (ici le [fichier](https://github.com/qmk/qmk_firmware/blob/master/quantum/keymap_extras/keymap_bepo.h) qmk permettant d’écrire un keymap en BÉPO). Sans rentrer dans les détails techniques, sans celui-ci, lorsque votre ordinateur utilise un driver BÉPO, le keycodes &kp Z est traduit en B et &kp B en k. Il a donc fallu créer le fichier adapté : [keys_bepo.h](https://github.com/MartinDrillon/zmk-config-ITEMX/blob/main/config/keys_bepo.h). Cela permet d’utiliser un second keycode plus lisible pour les tous caractères spécifiques au bépo. Concrètement, pour taper B sur un ordinateur utilisant un driver BÉPO, il est possible d’écrire dans son keymap ou bien &kp Z ou bien &kp BP_B. Tout ces codes peuvent être retrouvé dans le fichier en question. 

***
## NOTE SUR LA CONSTRUCTION

Si vous souhaitez réaliser vous-même ce clavier, il vous faudra télécharger les fichiers gebers et les envoyer à un fabriquant tel que JLCPCB ou PCBWAY. N’hésitez pas à me contacter pour des instructions plus détaillés. Je vous conseille cependant d’attendre la publication de la version suivante. 
Mauvais matériel pour impression 3d 
BOM => lien vers une spreadsheet ? 
License 

## AMÉLIORATION PRÉVUE SUR LA VERSION À VENIR