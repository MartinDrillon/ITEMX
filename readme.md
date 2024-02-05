<h1 align="center">ITEMX</h1>

***

ITEMX est un clavier en deux parties de 46 touches fonctionnant avec [ZMK](https://github.com/zmkfirmware/zmk) et utilisant une SEEED XIAO BLE comme microcontrolleur. Il a été entièrement conçu avec [Ergogen](https://github.com/ergogen/ergogen).

C’est la quatrième itération d’un projet dont le but est de créer un clavier ergonomique ayant 5 touches de pouces par main et utilisant une répartitions des caractères adaptés du [BÉPO](https://bepo.fr/wiki/Accueil). 

_Bien que cette version soit parfaitement fonctionnelle, il demeure quelques défauts. Une cinquième version devrait voir le jour prochainement._

***
![ITEMX3](/docs/images/key3.png)

![ITEMX](/docs/images/ITEMX1.JPG)

![ITEMX2](/docs/images/ITEMX2.JPG)
***

Ce clavier fonctionne avec une disposition dérivée du BÉPO. Pour être exact, il s’agit d’une adaptation du travail de Kawamashi publié [ici](https://forum.bepo.fr/viewtopic.php?id=1696). Après presque deux ans d’utilisation, il ne fait aucun doute pour moi que cette disposition est très largement supérieure à l’azerty pour la frappe du français (et de tout type de language), autant en terme de confort que de rapidité. Le seul avantage indéniable à l’azerty est celui de l’habitude et de la relative difficulté à apprendre une nouvelle disposition.

Sa particularité, par rapport à d’autres claviers ergonomiques ([KYRIA](https://github.com/foostan/crkbd), [LILY58](https://github.com/kata0510/Lily58)...) dont il s’inspire, est d’avoir au total 10 touches de pouces toutes accessibles en déplaçant uniquement le doigt et non l’ensemble de la main (touch typing). Une touche de pouce spécifique peut être attribuée pour chaque modifiers de base (shift, ctrl, alt pour la mains gauche et shift, altgr, win pour la droite) en plus de quelques caractères fréquents. Cela permet d’utiliser la moitié gauche du clavier comme un macropad lors de l’utilisation de logiciels de DAO/CAO nécessitant un usage intensif de combinaison à base de schift, ctrl, alt, alt+ctrl plus simplement qu’avec l’usage de mod-tap, hold-tap, homerows mods... (voir la documentation de [ZMK](https://zmk.dev/docs) sur les comportements possibles)

***

## DISPOSITION DES CARACTÈRES

**Niveau de base**

![BASE](/docs/images/1x/base.png)

**Cumbo**

![CUMBO](/docs/images/1x/cumbo.png)

**Sym**

![SYM](/docs/images/1x/sym.png)

**Nav**

_Visualisation à venir._

***

## UTILISATION DU BÉPO AVEC ZMK

Contrairement à QMK, ZMK ne propose pas de fichier à inclure dans le ficher keymap pour le faire correspondre au driver clavier qu’utilise votre ordinateur (ici le [fichier](https://github.com/qmk/qmk_firmware/blob/master/quantum/keymap_extras/keymap_bepo.h) QMK permettant d’écrire un keymap en BÉPO). Sans rentrer dans les détails techniques, sans celui-ci, lorsque votre ordinateur utilise un driver BÉPO, le keycodes &kp Z est traduit en B et &kp B en k.

J’ai donc créer le fichier équivalent pour ZMK : [keys_bepo.h](https://github.com/MartinDrillon/zmk-config-ITEMX/blob/main/config/keys_bepo.h). Son but est de définir un second keycode plus lisible pour les caractères spécifiques au BÉPO. Lorsqu’il est inclu au keymap, il sera possible d’uliliser ou bien &kp Z ou bien &kp BP_B pour taper B sur un ordinateur utilisant un driver BÉPO. La liste de tout ces codes se trouvent dans le fichier en question. 

Voici le repository à copier si vous souhaitez créer votre propre keymap pour ce clavier ou vous en inspirer : [ZMK](https://github.com/MartinDrillon/zmk-config-ITEMX).

***

## AMÉLIORATION PRÉVUE SUR LA VERSION À VENIR

- Modification du placement des touches de pouces.
- Faciliter la construction, en particulier au niveau de l’intégration de la XIAO SEEE.
- Amélioration du design de la coque. 
- Publication d’un guide de construction adapté. 