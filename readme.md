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
![ITEMX2](/docs/images/ITEMX2.png)
***

## DISPOSITION DES CARACTÈRES

La particularité de ce clavier, par rapport à d’autres claviers ergonomiques de ce genre ([KYRIA](https://github.com/foostan/crkbd), [LILY58](https://github.com/kata0510/Lily58)) dont il s’inspire, est d’avoir au total 10 touches de pouces toutes accessibles en déplaçant uniquement le doigt et non l’ensemble de la main (touch typing).

Le principe qui dicte cette configuration physique est le suivant : À condition d’avoir une touche accessible en touch typing, il est toujours plus simple de donner un imput par une simple pression d’un doigt plutôt que d’avoir recours à une combinaisons (mod-tap, hold-tap, homerows mods... voir la documentation de [ZMK](https://zmk.dev/docs) sur les comportements possibles). Cettre rêgle est d’autant plus importante lorsque l’imput de base joue lui-même régulièrement un rôle dans une combinaison. En conséquence, toutes les configurations alternative à l’utilisation d’une touche dédiée uniquement à un modifier entrainent systématiquement soit des compliquations, soit des erreurs de frappe occasionelles, soit les deux. Cela peut être concédé à la pureté d’un clavier extrèmement minimaliste quand on en a un usage de bureautique standard mais n’est pas fonctionnel lorsqu’il s’agit de maîtriser des outils digitaux complexes. 

Sur ce clavier, il est possible d’attribuer une touche de pouce par modifiers de base(shift, ctrl, alt pour la mains gauche et shift, altgr, win pour la droite) en plus de quelques caractères très fréquemment utilisé. Cela permet à la fois d’utiliser la moitié gauche du clavier comme un macropad lors de l’utilisation de logiciels de DAO/CAO nécessitant un usage intensif de combinaison à base de schift, ctrl, alt, alt+ctrl... et de rapidifier la frappe, pusique les pouces entrent en jeu. 

Cela nous ammène sur le deuxième point crucial de ce clavier : il utilise une disposition dérivée du BÉPO. Pour être exact, il s’agit d’une adaptation du travail de Kawamashi publié [ici](https://forum.bepo.fr/viewtopic.php?id=1696). Après presque deux ans d’utilisation, il ne fait aucun doute pour moi que cette disposition est très largement supérieure à l’azerty pour la frappe du français (indirectement de l’anglais aussi), autant en terme de confort que de rapidité de frappe. Le seul avantage indéniable à l’azerty est celui de l’habitude et de la relative difficulté à apprendre une nouvelle disposition.

Cette disposition possède plus de caractère directement invoqué que l’azerty (é, è, ê, à, ç ayant chacun une touche dédiée). Paradoxalement, ce clavier possède beaucoup moins de touches qu’un clavier classique (46 contre 62 pour les plus petits claviers standard, mais toutes sont accesible en touch typing). Cela renforce la nécessité de déplacer certains caractères sous les pouces. L’usage de plusieurs layers et de cumbos pour les caractères les plus fréquents reste bien entendu nécessaire. 

**Niveau de base**

Ce niveau me semble presque complètement abouti. La ponctuation sera peut être légèrement modifié dans le futur : les caractères shifté pourront être remplacés par des cumbos supplémentaires. Quelques légères modifications pourraient être effectué par un usager souhaitant taper occasionnellement en anglais. 
![BASE](/docs/images/1x/BASE.png)

**Cumbo**

Afin de renforcer la possibilité d’utiliser la partie gauche du clavier comme un macropad, les cumbos invoquant des raccourcis claviers classique (ctrl+z/c/v...) se situent sous la main gauche. Les cumbos invoquant des caractères spéciaux sont à droite. À noter que dans le cas d’un utilisateur gaucher, il faudrait les inversers, ainsi d’ailleur que les modifiers placé sous les pouces gauches et droits.
![CUMBO](/docs/images/1x/CUMBO.png)

Cette partie de la disposition me semble plus personnelle et peux faire l’objet de changement régulier.

**Sym**

![SYM](/docs/images/1x/CUMBO.png)


## NOTE SUR LA CONSTRUCTION

Si vous souhaitez réaliser vous-même ce clavier, il vous faudra télécharger les fichiers gebers et les envoyer à un fabriquant tel que JLCPCB ou PCBWAY. N’hésitez pas à me contacter pour des instructions plus détaillés. Je vous conseille cependant d’attendre la publication de la version suivante. 
Mauvais matériel pour impression 3d 
BOM => lien vers une spreadsheet ? 
License 

## AMÉLIORATION PRÉVUE SUR LA VERSION À VENIR