---
title: Icônes (concepts de base de la conception)
description: Les icônes sont des représentations sous forme d’objets, qui sont importantes non seulement pour des raisons esthétiques dans le cadre de l’identité visuelle d’un programme, mais également pour des raisons utilitaire comme raccourci pour la communication de la signification que les utilisateurs perçoivent presque instantanément.
ms.assetid: 6f88cb32-ecfe-4e6e-a41b-31891cf510cf
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: ad788338adc81bd9bc796412eebf4bef87ceca2b7a3855e024702a3e1bb23e49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119841856"
---
# <a name="icons-design-basics"></a>Icônes (concepts de base de la conception)

> [!NOTE]
> ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Les icônes sont des représentations sous forme d’objets, qui sont importantes non seulement pour des raisons esthétiques dans le cadre de l’identité visuelle d’un programme, mais également pour des raisons utilitaire comme raccourci pour la communication de la signification que les utilisateurs perçoivent presque instantanément. Windows Vista introduit un nouveau style de iconographie qui offre un niveau de détail et de sophistication plus élevé pour Windows.

**Remarque :** Les instructions relatives aux [icônes standard](vis-std-icons.md) sont présentées dans un article distinct.

## <a name="design-concepts"></a>Principes de conception

Aero est le nom de l’expérience utilisateur de Windows Vista, représentant les valeurs incorporées dans la conception de l’esthétique, ainsi que la vision de l’interface utilisateur. Aero correspond à : authentique, énergétique, réfléchissant et ouvert. Aero a pour but d’établir une conception qui est à la fois professionnelle et merveilleux. Aero esthétique crée une expérience de haute qualité et élégante qui facilite la productivité des utilisateurs et même les lecteurs d’une réponse émotionnelle.

Windows les icônes Vista diffèrent des icônes de style Windows XP des manières suivantes :

-   Le style est plus réaliste qu’Illustrator, mais pas très réaliste. Les icônes sont des images symboliques qu’il convient d’obtenir de meilleures performances que les icônes photoréalistes !
-   Les icônes ont une taille maximale de 256x256 pixels, ce qui les rend adaptés aux affichages haute résolution (points par pouce). Ces icônes haute résolution permettent une haute qualité visuelle dans les affichages de liste avec de grandes icônes.
-   Dans la mesure du possible, les icônes de documents fixes sont remplacées par des miniatures du contenu, ce qui facilite l’identification et la recherche des documents.
-   Les icônes de barre d’outils présentent moins de détails et aucune perspective, afin d’optimiser les tailles les plus petites et l’aspect visuel.

Icônes bien conçues :

-   Améliorez la communication visuelle de votre programme.
-   Affectez fortement l’impression générale des utilisateurs de la conception visuelle de votre programme, et réagissez à l’adéquation.
-   Améliorez la convivialité en facilitant l’identification, l’apprentissage et la recherche de programmes, d’objets et d’actions.

les images suivantes décrivent ce qui rend le style Aero de iconographie dans Windows Vista différent de celui utilisé dans Windows XP.

![images des icônes de verrouillage et de clé](images/vis-icons-image1.png)

les icônes Windows Vista (le verrou et la clé à gauche) sont authentiques, nettes et détaillées. Elles sont rendues plutôt que dessinées, mais ne sont pas complètement photoréalistes.

![images d’icônes de bloc-notes terrestre et en spirale](images/vis-icons-image2.png)

les icônes Windows Vista (les deux à gauche) sont professionnelles et magnifiques, avec une attention particulière aux détails qui améliorent la qualité de production des icônes.

![images du bloc-notes, du verrou, du moniteur et du papier](images/vis-icons-image3.png)

ces icônes Windows Vista montrent un équilibre optique et une précision perçue en perspective et en détails. Cela leur permet d’avoir une grande taille ou de petite taille, de proximité ou de distance. En outre, ce style de iconographie fonctionne pour les écrans haute résolution.

![image d’une icône de routeur sans fil](images/vis-icons-image4.png)![image d’une feuille d’icône de papier](images/vis-icons-image5.png)![image d’une grande icône de flèche droite verte](images/vis-icons-image6.png)

Ces exemples illustrent différents types d’icônes, y compris un objet en trois dimensions en perspective, une icône avant (plat) et une icône de barre d’outils.

## <a name="guidelines"></a>Consignes

### <a name="perspective"></a>Perspective

-   **les icônes dans Windows Vista sont soit à trois dimensions et affichées dans la perspective en tant qu’objets solides, soit en tant qu’objets à deux dimensions affichés en mode droit.** Utilisez des icônes plates pour les fichiers et pour les objets qui sont en fait plats, comme des documents ou des morceaux de papier.

    ![images de l’ordinateur 3D et du papier plat et 2D ](images/vis-icons-image7.png)

    Icônes 3D et plat typiques.

-   **Les objets en trois dimensions sont représentés dans la perspective sous forme d’objets solides, vus à partir d’une vue de bas niveau des oiseaux avec deux points de fuite.**

    ![image du bloc-notes avec des lignes présentant une perspective](images/vis-icons-image8.png)

    Cet exemple montre les points de perspective et de fuite typiques des icônes 3D.

-   **Dans les plus petites tailles, la même icône peut passer du point de vue au niveau droit.** Avec une taille de 16x16 pixels et plus petite, les icônes de rendu sont accessibles en ligne (frontal). Pour les grandes icônes, utilisez la perspective.

    -   **Exception :** Les icônes de barre d’outils sont toujours frontales, même dans des tailles supérieures.

    ![image d’un ordinateur 3D de grande taille et d’un petit ordinateur 2D ](images/vis-icons-image9.png)

    Cet exemple montre comment la même icône est traitée différemment, en fonction de la taille.

### <a name="light-source"></a>Source de lumière

-   **La source de lumière pour les objets dans la grille de perspective est supérieure, légèrement devant et légèrement à gauche de l’objet.**
-   **La source de lumière diffuse les ombres légèrement à l’arrière et à droite de la base de l’objet.**
-   **Tous les rayons de lumière sont parallèles et frappent l’objet le long du même angle (comme le soleil).** L’objectif est d’avoir une apparence d’éclairage uniforme pour toutes les icônes et tous les effets de Spotlight. Les rayons de lumière parallèle produisent des ombres qui ont toutes la même longueur et densité, fournissant une Unity supplémentaire sur plusieurs icônes.

### <a name="shadows"></a>Ombres

**Général**

-   **Utilisez les ombres pour élever visuellement les objets à partir de l’arrière-plan, et pour faire apparaître les objets 3D à la terre, plutôt que de les dissocier de façon difficile.**
-   **Utilisez une plage d’opacité de 30-50% pour les ombres.** Parfois, un niveau différent d’ombre doit être utilisé, en fonction de la forme ou de la couleur d’une icône.
-   **Estompez ou raccourcissez l’ombre si nécessaire pour éviter qu’elle ne soit rognée par la taille de la zone d’icône.**
-   **N’utilisez pas d’ombres dans les icônes à 24x24 ou de taille inférieure.**

    ![images d’icônes 3D avec des ombres ](images/vis-icons-image10.png)

    Ombres d’icônes typiques.

**Icônes à deux dimensions**

-   Les **icônes plates sont généralement utilisées pour les icônes de fichiers et les objets réels plats,** tels qu’un document ou une feuille de papier.
-   **L’éclairage de l’icône à deux dimensions provient de l’angle supérieur gauche à 130 degrés.**
-   **Les icônes plus petites (par exemple, 16x16 et 32x32) sont simplifiées pour des raisons de lisibilité.** Toutefois, si elles contiennent une réflexion dans l’icône (souvent simplifiée), elles peuvent avoir une ombre portée étroite. Les plages d’ombre portée dans l’opacité sont comprises entre 30-50%.
-   **Les effets de couche peuvent être utilisés pour les icônes plates, mais doivent être comparés à d’autres icônes plates.** les ombres des objets varient quelque peu, en fonction de ce qui est le mieux adapté et le plus cohérent dans la taille définie et avec les autres icônes dans Windows Vista. Dans certains cas, il peut même s’avérer nécessaire de modifier les ombres. Cela est particulièrement vrai lorsque des objets sont disposés sur d’autres.
-   **Une plage subtile de couleurs peut être utilisée pour obtenir le résultat souhaité.** Shadows Help Objects assiste dans l’espace. La couleur influe sur le poids perçu de l’ombre et peut déformer l’image si elle est trop lourde.

![capture d’écran de la boîte de dialogue avec l’ombre portée activée ](images/vis-icons-image11.png)![capture d’écran de l’icône de papier avec ombre portée étroite ](images/vis-icons-image12.png)

L’option ombre portée de la boîte de dialogue style de couche et une ombre type pour une icône à deux dimensions.

**Icônes de base de l’icône à plat**



| Caractéristique                              | Plage                                                         |
|-------------------------------|----------------------------------------------------------|
| Couleur<br/>              | Noir<br/>                                         |
| Mode de fusion<br/>         | Multiplier<br/>                                      |
| Opacity<br/>            | 22-50%, en fonction de la couleur de l’élément<br/> |
| Angle<br/>              | 120-130 (utiliser la lumière globale)<br/>                    |
| Distance<br/>           | 3 pour 256x256, allant jusqu’à 1 pour 32x32<br/>    |
| Spread<br/>             | 0<br/>                                             |
| Taille<br/>               | 7 pour 256x256, allant jusqu’à 2 pour 32x32<br/>    |



 

**Icônes en trois dimensions**

-   Créer des ombres pour les icônes 3D au cas par cas, avec un effort pour tenir dans une plage de la distance de coulée et de la discontinuation pour une transparence complète. Créez les images d’une taille légèrement inférieure à la taille globale des icônes pour permettre l’espace pour une ombre portée (pour les tailles qui en auront besoin). Assurez-vous que l’ombre ne se termine pas brusquement au bord de l’icône.

![Illustration de la création d’ombres dans Photoshop](images/vis_icons_image13.jpeg)

![Illustration de quatre objets avec des ombres variables](images/vis_icons_image14.jpeg)

Ces exemples aident à illustrer les variations créées en fonction de la forme et de la position de l’objet lui-même. L’ombre doit parfois être discontinue ou réduite pour éviter qu’elle ne soit rognée par la taille de la zone d’icône.

### <a name="color-and-saturation"></a>Couleur et saturation

-   **les couleurs sont généralement moins saturées qu’elles n’étaient Windows XP.**
-   **Utilisez des dégradés pour créer une image plus réaliste.**
-   **Bien qu’il n’existe pas de palette de couleurs spécifique pour les icônes standard, n’oubliez pas qu’elles doivent fonctionner correctement ensemble dans de nombreux contextes et thèmes.** Préférer l’ensemble de couleurs standard ; ne recolorez pas les icônes standard, telles que les icônes d’avertissement, car cela perturbe la capacité des utilisateurs à interpréter la signification. Pour plus d’instructions, consultez [Color](vis-color.md).
-   Les **fichiers icône requièrent également des versions de palette 8 bits et 4 bits** pour prendre en charge le paramètre par défaut dans un bureau à distance. Ces fichiers peuvent être créés par le biais d’un processus de traitement par lots, mais ils doivent être examinés, car certains nécessitent une retouche pour une meilleure lisibilité.

    ![capture d’écran de la boîte de dialogue Sélecteur de couleurs ](images/vis-icons-image15.png)

    Il n’existe aucune restriction de palette de couleurs stricte. Seule la saturation complète (en haut à droite) est évitée.

-   Niveaux de bits : conception ICO pour 32 bits (alpha inclus) + 8 bits + 4 bits (à l’inversion automatique de pixel en pixels uniquement la plus critique). Seule une copie 32 bits de l’image de pixels 256x256 doit être incluse, et seule l’image de pixel 256x256 doit être compressée pour réduire la taille du fichier. plusieurs outils d’icône offrent la compression pour Windows Vista.
-   Niveaux de bits : barres d’outils 24 bits + alpha (masque 1 bit), 8 bits et 4 bits.
-   Barres d’outils ou fichiers AVI : utilisez magenta (R255 G0 B255) comme couleur de transparence de l’arrière-plan.

### <a name="size-requirements"></a>Exigences de taille

**Général**

-   portez **une attention particulière aux icônes de visibilité élevée,** telles que les icônes d’application principales, les icônes de fichier qui peuvent apparaître dans Windows Explorer et les icônes qui apparaissent dans le Menu démarrer ou sur le bureau.
    -   **Icônes d’application et éléments du panneau de configuration :** Le jeu complet comprend 16x16, 32x32, 48 et 256x256 (échelle de code comprise entre 32 et 256). Le format de fichier. ico est requis. Pour le mode classique, le jeu complet est 16x16, 24x24, 32x32, 48 et 64x64.
    -   **Options de l’icône d’élément de liste :** Utilisez des miniatures dynamiques ou des icônes de fichier du type de fichier (par exemple, .doc); ensemble complet.
    -   **Icônes de barre d’outils :** 16x16, 24x24, 32x32. Notez que les icônes de barre d’outils sont toujours plates, pas en 3D, même à la taille 32 x 32.
    -   **Icônes de la boîte de dialogue et de l’Assistant :** 32x32 et 48.
    -   **Superpositions :** Code Shell principal (par exemple, un raccourci) 10x10 (pour 16x16), 16x16 (pour 32x32), 24x24 (pour 48), 128 x 128 (pour 256x256). Notez que certains d’entre eux sont légèrement plus petits, mais proches de cette taille, en fonction de la forme et de l’équilibre optique.
    -   **Zone lancement rapide :** Les icônes sont redimensionnées à partir de 48 dans les superpositions dynamiques Alt + Tab, mais pour une version plus claire, ajoutez un 40 x 40 au fichier. ico.
    -   **Icônes de bulles :** 32x32 et 40 x 40.
    -   **Tailles supplémentaires :** Celles-ci sont utiles pour être disponibles en tant que ressources pour créer d’autres fichiers (par exemple, annotations, bandes de barre d’outils, superpositions, résolutions élevées et cas spéciaux) : 128 x 128, 96x96, 64x64, 40 x 40, 24x24, 22x22, 14x14, 10x10 et... Vous pouvez utiliser les formats de fichier. ico, .png, .bmp ou autres, selon le code de cette zone.

**Pour les résolutions élevées**

-   Windows Vista cible 96 ppp et 120 ppp.

Les tableaux suivants présentent des exemples de rapports de mise à l’échelle appliqués à deux tailles d’icône courantes. Notez que toutes ces tailles ne doivent pas être incluses dans le fichier. ico. Le code met à l’échelle les plus grandes.



| ppp                   | Taille d'icône                         | Facteur d’échelle                            |
|--------------------|--------------------------|-----------------------------|
| 96<br/>      | 16x16<br/>         | 1,0 (100%)<br/>       |
| 120<br/>     | 20 x 20<br/>         | 1,25 (125%)<br/>      |
| 144<br/>     | 24 x 24<br/>         | 1,5 (150%)<br/>       |
| 192<br/>     | 32x32<br/>         | 2,0 (200%)<br/>       |



 



| ppp                   | Taille d'icône                         | Facteur d’échelle                            |
|--------------------|--------------------------|-----------------------------|
| 96<br/>      | 32x32<br/>         | 1,0 (100%)<br/>       |
| 120<br/>     | 40 x 40<br/>         | 1,25 (125%)<br/>      |
| 144<br/>     | 48 x 48<br/>         | 1,5 (150%)<br/>       |
| 192<br/>     | 64 x 64<br/>         | 2,0 (200%)<br/>       |



 

**tailles de fichier. ico (standard)**

![Diagramme qui affiche différentes icônes de routeur de taille standard.](images/vis-icons-image16.png)

**tailles de fichier. ico (cas particuliers)**

![illustration d’icônes de routeur de tailles différentes ](images/vis-icons-image17.png)

**Annotations et superpositions**

-   Les annotations sont placées dans le coin inférieur droit de l’icône et doivent remplir 25% de la zone d’icône.
    -   **Exception :** les icônes 16x16 prennent des annotations 10x10.
-   N’utilisez pas plusieurs annotations sur une icône.
-   Les superpositions s’affichent dans le coin inférieur gauche de l’icône et doivent remplir 25% de la zone d’icône.
    -   **Exception :** les icônes 16x16 prennent des superpositions 10x10.

### <a name="level-of-detail"></a>Niveau de détail

-   16x16 la plupart de ces icônes sont toujours largement utilisées et, par conséquent, importantes.
-   Les détails d’une icône de cette taille doivent clairement afficher le point clé de l’icône.
-   À mesure qu’une icône devient plus petite, la transparence et des détails spéciaux trouvés dans des tailles supérieures doivent être sacrifiés pour simplifier et faire le point.
-   Les attributs et les couleurs doivent être exagérés et utilisés pour mettre en évidence les formes clés.

    ![illustration d’un grand nombre et de deux petits périphériques ](images/vis-icons-image18.png)

    À 16x16, l’icône du périphérique audio portable peut facilement être confondu avec un téléphone portable, de sorte que l’oreille est un détail visuel clé à afficher.

-   L’augmentation simple de la taille de 256x256 ne fonctionne pas.
-   Toutes les tailles ont besoin d’un niveau de détail approprié ; plus la taille de l’icône est petite, plus vous avez besoin de faire exagéré les détails de la définition.

    ![illustration de téléphones cellulaires avec des détails clairs ](images/vis-icons-image19.png)

    ![illustration de téléphones cellulaires avec des détails flous ](images/vis-icons-image20.png)

### <a name="icon-development"></a>Développement d’icônes

**Conception et production d’icônes**

-   **Embauchez un concepteur graphique expérimenté.** Pour obtenir de superbes graphiques, images et icônes fonctionnent avec des experts. L’expérience dans les illustrations à l’aide d’images vectorielles ou de programmes 3D est recommandée.
-   **Envisagez de faire une série d’itérations,** des croquis concept initial, des simulacres contextuels, à la révision de production finale et à l’ajustement et à la fin des icônes dans le produit de travail.
-   **La création d’une icône de réflexion peut être coûteuse.** Rassemblez tous les détails et exigences existants, tels que : l’ensemble complet des icônes nécessaires ; la fonction principale et la signification de chaque ; les familles ou les clusters de l’ensemble que vous souhaitez voir apparaître ; exigences de la personnalisation ; les noms de fichiers exacts ; formats d’image utilisés dans votre code ; et la taille requise. Assurez-vous que vous pouvez tirer le meilleur parti de votre temps avec le concepteur.
-   **N’oubliez pas que le concepteur n’est peut-être pas familier avec votre produit. fournissez des informations fonctionnelles, des captures d’écran et des sections Spec, le cas échéant.**
-   **Planifiez les évaluations géopolitiques et juridiques appropriées.**
-   **Mappez une période et une communication régulière.**

**De l’esquisse du concept à la fin du produit**

![illustration du développement des croquis des téléphones cellulaires ](images/vis-icons-image21.png)

-   Créer des croquis concept.
-   Essayez le concept dans différentes tailles.
-   Affichez en 3D si nécessaire.
-   Testez les tailles sur différentes couleurs d’arrière-plan.
-   Évaluez les icônes dans le contexte de l’interface utilisateur réelle.
-   Produire un fichier. ico final ou d’autres formats de ressources graphiques.

**outils**

-   **Crayon et papier :** Idées initiales du concept, listées et esquissées.
-   **Max Studio 3D :** Rendu des objets 3D en perspective.
-   **Adobe Photoshop :** Esquissez et itérez, effectuez une simulation en contexte et finalisez les détails.
-   **Adobe Illustrator/Macromedia Freehand :** Esquissez et itérez, finaliser les détails.
-   **Vidéo gamani gif :** Générez le fichier. ico (avec compression si nécessaire).
-   **Icône Axialis Workshop :** Générez le fichier. ico (avec compression si nécessaire).
-   Microsoft Visual Studio ne prend pas en charge les icônes Windows Vista (il n’y a pas de prise en charge du canal alpha ou de plus de 256 couleurs).

**Production**

> [!TIP]
> Procédez comme suit pour créer un fichier. ico unique qui contient plusieurs tailles d’image et de profondeur de couleur.

**Étape 1 : conceptualise**

-   Utilisez les concepts établis dans la mesure du possible, pour garantir la cohérence des significations de l’icône et sa pertinence pour d’autres utilisations.
-   Déterminez comment l’icône s’affiche dans le contexte de l’interface utilisateur et comment elle peut fonctionner dans le cadre d’un ensemble d’icônes.
-   Si vous modifiez une icône existante, déterminez si la complexité peut être réduite.
-   Tenez compte de l’impact culturel de vos graphiques. Évitez d’utiliser des lettres, des mots, des mains ou des visages dans les icônes. Décrit les représentations des personnes ou des utilisateurs de façon générique, si nécessaire.
-   Si vous combinez plusieurs objets en une seule image dans une icône, réfléchissez à la façon dont l’image est mise à l’échelle en taille plus petite. N’utilisez pas plus de trois objets dans une icône (deux est préférable). Pour la taille 16x16, envisagez de supprimer des objets ou de simplifier l’image afin d’améliorer la reconnaissance.
-   n’utilisez pas l’indicateur Windows dans les icônes.

**Étape 2 : illustrer**

-   pour illustrer Windows icônes de style Aero, utilisez un outil vectoriel tel que Macromedia Freehand ou Adobe illustrator. Utilisez les caractéristiques de palette et de style décrites précédemment dans cet article.
-   Illustration d’une image à l’aide de FreeHand ou d’Illustrator. Copiez et collez les images vectorielles dans Adobe Photoshop.
-   Créez et utilisez une couche de modèle dans Photoshop pour vous assurer que le travail est effectué dans les régions carrées des tailles régulées.
-   Créez les images d’une taille légèrement inférieure à la taille globale des icônes pour permettre l’espace pour une ombre portée (pour les tailles qui en nécessitent une).
-   Placez les images en bas des carrés, afin que toutes les icônes d’un répertoire soient positionnées de manière cohérente. Évitez de couper les ombres.
-   Si vous ajoutez un autre objet à une image ou à une série, conservez l’objet principal dans une position fixe et placez les images de taille réduite plates à une position fixe, par exemple, en bas à gauche ou en haut à droite selon le cas.

**Étape 3 : créer les images 24 bits**

-   Une fois que vous avez collé les tailles dans Photoshop, vérifiez la lisibilité des images, en particulier à 16 x 16 et plus petites tailles. Pixel-l’utilisation de pourcentages de couleurs peut être nécessaire. Une réduction de la transparence peut également être nécessaire. Il est courant d’éviter les aspects à des tailles plus petites et d’éliminer également les aspects, afin de se concentrer sur le point clé.
-   Les icônes 8 bits s’affichent dans n’importe quel mode de couleur inférieur à 32 bits et n’ont pas le canal alpha 8 bits, donc ils peuvent avoir besoin d’avoir leurs bords ou plus nettoyés, car il n’y a pas d’anticrénelage (les bords peuvent être en escalier et l’image peut être difficile à lire).
-   Dans Photoshop, dupliquez la couche d’images de 24 bits et renommez la couche en images 4 bits. indexez les images 4 bits sur la palette de couleurs Windows 16.
-   Nettoyez les images à l’aide des couleurs de la palette de 16 couleurs uniquement. Les contours créés à partir de versions plus sombres ou plus légères des couleurs de l’objet sont généralement préférables à la couleur grise ou noire.
-   Si vous travaillez sur une image bitmap, assurez-vous que la couleur d’arrière-plan n’est pas utilisée dans l’image elle-même, car cette couleur sera la couleur transparente. Le magenta (R255 G0 B255) est souvent utilisé comme couleur de transparence de l’arrière-plan.

**Étape 4 : créer les images 8 bits et 4 bits**

-   Maintenant que les images 24 bits sont prêtes à être établies en icônes 32 bits, les versions 8 bits doivent être créées.
-   Il s’agit d’un bon moment pour tester des captures d’écran contextuelles. C’est incroyable ce qui peut être découvert en affichant d’autres icônes ou une famille d’icônes en contexte. Cette étape peut vous faire gagner du temps et de l’argent. Il est préférable d’intercepter les problèmes avant que les fichiers ne passent en production et qu’ils soient remis.
-   Ajoutez l’ombre portée à vos images dans des tailles qui en ont besoin.
-   Fusionnez l’ombre portée et les images 24 bits ensemble.
-   Créez un fichier Photoshop pour chaque taille. Copiez et collez l’image appropriée. Enregistrez chaque fichier sous la forme d’un fichier de .psd.
-   Ne fusionnez pas la couche d’image avec la couche d’arrière-plan. Il est utile d’inclure la taille et la profondeur de couleur dans le nom de fichier pendant que vous travaillez, mais le fichier peut finalement avoir besoin d’être renommé.

**Étape 5 : créer le fichier. ico**

-   Choisissez l’application qui répond le mieux aux besoins et aux compétences des artistes. N’oubliez pas que les icônes à utiliser dans un produit d’expédition doivent être créées dans un outil acheté ou sous licence. Cela signifie que les versions d’essai ne peuvent pas être utilisées.
-   les deux produits listés ci-dessous ont été utilisés par des concepteurs qui ont produit des icônes pour Windows Vista, chacun offrant la possibilité d’exporter vers Adobe Photoshop CS.
    -   Gamani Gif Movie Gear : produire un fichier. ico
    -   Icône Axialis Workshop : produire un fichier. ico
-   Visual Studio ne prend pas en charge les icônes Windows Vista (il n’y a pas de prise en charge du canal alpha ou de plus de 256 couleurs). son utilisation n’est donc pas recommandée.
-   Les fichiers icône (format. ico) doivent contenir les versions 4 et 8 bits, ainsi que les versions alpha et de 24 bits.
-   enregistrez les fichiers sous la forme d’une icône de Windows (. ico), quel que soit le programme de création d’icône que vous choisissez d’utiliser.
-   Certaines ressources iconographic peuvent être en fait des bandes bitmap, qui nécessitent également un canal alpha (par exemple, pour les barres d’outils) ou des fichiers .png enregistrés avec transparence. Tous ne sont pas nécessairement au format. ico ; Vérifiez le format pris en charge dans le code.

**Étape 6 : évaluer**

-   Examinez toutes les tailles.
-   Reportez-vous à la famille pour évaluer la ressemblance avec la famille, l’équilibre optique et la distinction.
-   Examinez en contexte pour évaluer les poids et la visibilité relatifs (Assurez-vous qu’aucun ne domine).
-   Tenez compte des cas qui ne peuvent pas être utilisés à l’heure actuelle, mais qui pourraient se trouver dans un avenir proche. Cette icône peut-elle être annotée ou avoir une superposition ?
-   Examinez dans le code.

### <a name="icons-in-the-context-of-list-views-toolbars-and-tree-views"></a>Icônes dans le contexte des affichages de liste, des barres d’outils et des arborescences

**Affichages de liste**

-   pour Windows Vista, utilisez des miniatures pour les fichiers contenant du contenu visuellement distinct à petite échelle, de sorte que les utilisateurs puissent reconnaître directement le fichier qu’ils recherchent. (utilisez l’interface de programmation d’applications de Windows miniatures pour cela.)

    ![capture d’écran de l’Explorateur Windows avec les icônes de dossiers ](images/vis-icons-image22.png)

-   Les superpositions d’icône d’application (non présentées ici) sur les miniatures aident à associer l’application pour le type de fichier, en plus d’afficher l’aperçu du fichier.

**Remarque :** Pour les fichiers sans contenu visuellement distinct, n’utilisez pas de miniatures. Au lieu de cela, utilisez les icônes de fichiers symboliques traditionnelles qui illustrent la représentation d’objet et l’application ou le type associé.

**Barres d'outils**

-   Les icônes qui apparaissent dans une barre d’outils doivent avoir un équilibre optique en taille, en couleur et en complexité.
-   Testez les icônes potentielles dans une capture d’écran contextuel pour éviter les dépassements ou les déséquilibres indésirables.
-   Le test des captures d’écran permet d’éviter facilement des itérations coûteuses dans le code.
-   Examinez également les icônes dans le code. Le mouvement et d’autres facteurs peuvent avoir un impact sur la réussite d’une icône. dans certains cas, des itérations supplémentaires peuvent être nécessaires.

![capture d’écran de la barre d’outils avec petites icônes et étiquettes ](images/vis-icons-image23.png)

Dans l’exemple ci-dessus, le solde optique n’a pas encore été atteint.

![illustration d’icônes sur des arrière-plans différents ](images/vis-icons-image24.png)

Essayez les itérations en contexte.

**Arborescences**

-   Un équilibrage optique est nécessaire pour conserver la hiérarchie dans un contrôle Tree View.
-   Par conséquent, les icônes généralement utilisées dans ce contexte doivent être évaluées à cet emplacement. Parfois, une icône de 16x16 particulière doit être plus petite, car sa forme a une dominance optique par rapport à d’autres.
-   La compensation des déséquilibres optiques est une partie importante de la génération d’icônes de qualité supérieure.

![figure de deux ensembles de dossiers dans l’arborescence ](images/vis-icons-image25.png)

 

