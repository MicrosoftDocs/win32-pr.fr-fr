---
title: Curseurs (concepts de base de la conception)
description: Avec un curseur, les utilisateurs peuvent choisir parmi une plage de valeurs continue.
ms.assetid: dee70fbc-6f18-43c7-9d41-4e97eac41e53
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 7ff9791ab49c338e4c11e014a3e996771571add9
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104556300"
---
# <a name="sliders-design-basics"></a>Curseurs (concepts de base de la conception)

> [!NOTE]
> Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Avec un curseur, les utilisateurs peuvent choisir parmi une plage de valeurs continue. Un curseur a une barre qui affiche la plage et un indicateur qui affiche la valeur actuelle. Les graduations facultatives affichent des valeurs.

![figure qui illustre la barre, le curseur et les graduations ](images/ctrl-sliders-image1.png)

Curseur classique.

> [!Note]  
> Les instructions relatives à la [disposition](vis-layout.md) sont présentées dans un article distinct.

 

## <a name="is-this-the-right-control"></a>Est-ce le contrôle approprié ?

Utilisez un curseur lorsque vous souhaitez que vos utilisateurs puissent **définir des valeurs contiguës définies (telles que le volume ou la luminosité) ou une plage de valeurs discrètes (telles que les paramètres de résolution d’écran).**

Un curseur représente un bon choix lorsque vous savez que les utilisateurs considèrent la valeur comme une quantité relative, et non comme une valeur numérique. Par exemple, dans le cas du volume, ils le régleront sur faible ou moyen, et pas sur 2 ou 5.

Pour vous décider, posez-vous les questions suivantes :

-   **Le paramètre s’apparente-t-il à une quantité relative ?** Si ce n’est pas le cas, utilisez des [cases d’option](ctrl-radio-buttons.md)ou une liste [déroulante](/windows/desktop/uxguide/ctrl-drop) ou [à sélection unique](ctrl-list-boxes.md).
-   **Le paramètre est-il une valeur numérique exacte connue ?** Si c’est le cas, utilisez des [zones de texte numériques](ctrl-text-boxes.md).
-   **Un utilisateur va-t-il bénéficier d’un feedback instantané sur l’effet des modifications apportées aux paramètres ?** Si tel est le cas, utilisez un curseur. Par exemple, les utilisateurs choisissent plus facilement une couleur lorsqu’ils voient immédiatement le résultat des modifications qu’ils ont apportées aux valeurs de teinte, de saturation ou de luminosité.
-   **Le paramètre a-t-il une plage de quatre valeurs ou plus ?** Si ce n’est pas le cas, utilisez des cases d’option.
-   **L’utilisateur peut-il changer la valeur ?** Les curseurs sont pour l’interaction utilisateur. Si un utilisateur ne peut pas modifier la valeur, utilisez plutôt une [zone de texte](ctrl-text-boxes.md) en lecture seule.

Si un curseur ou une zone de texte numérique est possible, utilisez une zone de texte numérique si :

-   l’espace de l’écran est réduit ;
-   Il est probable qu’un utilisateur préfère utiliser le clavier.

Utilisez un curseur si :

-   les utilisateurs bénéficieront d’un résultat instantané.

## <a name="guidelines"></a>Consignes

-   **Utilisez une orientation naturelle.** Par exemple, si le curseur représente une valeur du monde réelle qui est normalement affichée à la verticale (telle que la température), utilisez une orientation verticale.
-   **Orientez le curseur pour refléter la culture de vos utilisateurs.** Par exemple, les cultures occidentales se lisent de gauche à droite, donc pour les curseurs horizontaux, placez l’extrémité inférieure de la plage à gauche et l’extrémité supérieure à droite. Pour les cultures qui lisent de droite à gauche, effectuez l’inverse.
-   **Dimensionnez le contrôle afin qu’un utilisateur puisse facilement définir la valeur souhaitée.** Pour les paramètres ayant des valeurs distinctes, assurez-vous que l’utilisateur peut facilement sélectionner n’importe quelle valeur à l’aide de la souris.
-   **Envisagez d’utiliser une échelle non linéaire si la plage de valeurs est importante et que les utilisateurs sélectionneront probablement des valeurs à une extrémité de la plage.** Par exemple, la valeur de temps peut être 1 minute, 1 heure, 1 jour ou 1 mois.
-   **Chaque fois que cela est possible, donnez des commentaires immédiats pendant ou après qu’un utilisateur a fait une sélection.** Par exemple, le contrôle du volume Microsoft Windows émet un signal sonore pour indiquer le volume audio qui en résulte.
-   **Utilisez des étiquettes pour afficher les différentes valeurs de la plage.**

    **Exception :** Si le curseur est orienté verticalement et que l’étiquette supérieure est maximale, haute, plus ou équivalente, vous pouvez omettre les autres étiquettes, car la signification est claire.

    ![figure d’un curseur vertical ](images/ctrl-sliders-image2.png)

    Dans cet exemple, l’orientation verticale du curseur rend les étiquettes de plage inutiles.

-   **Utilisez des graduations lorsque les utilisateurs doivent connaître la valeur approximative du paramètre.**
-   **Utilisez des graduations et une étiquette de valeur lorsque les utilisateurs doivent connaître la valeur exacte du paramètre de leur choix.** Utilisez toujours une étiquette de valeur si un utilisateur doit connaître les unités pour avoir un sens du paramètre.

    ![figure du curseur qui indique le nombre de pixels sélectionnés ](images/ctrl-sliders-image3.png)

    Dans cet exemple, une étiquette est utilisée pour indiquer clairement la valeur sélectionnée.

-   **Pour les curseurs orientés horizontalement, placez les graduations sous le curseur.** Pour les curseurs orientés verticalement, placez les graduations à droite pour les cultures occidentales ; pour les cultures qui lisent de droite à gauche, effectuez l’inverse.
-   **Placez l’étiquette de valeur complètement sous le contrôle Slider afin que la relation soit claire.**

    **Incorrect :**

    ![figure d’une étiquette qui est plus longue que son curseur ](images/ctrl-sliders-image4.png)

    Dans cet exemple, l’étiquette de la valeur n’est pas alignée sous le curseur.

-   **Lorsque vous désactivez un curseur, désactivez également les étiquettes associées.**
-   **N’utilisez pas à la fois un curseur et une zone de texte numérique pour le même paramètre.** Utilisez uniquement le contrôle le plus approprié.

    **Exception :** Utilisez les deux contrôles lorsque l’utilisateur a besoin de commentaires immédiats et de la possibilité de définir une valeur numérique exacte.

-   **N’utilisez pas un curseur comme indicateur de progression.**
-   **Ne modifiez pas la taille par défaut de l’indicateur de curseur.**

    **Incorrect :**

    ![figure du curseur plus petit que la valeur par défaut ](images/ctrl-sliders-image5.png)

    Dans cet exemple, une taille plus petite que la valeur par défaut est utilisée.

    **Correct :**

    ![Figure représentant le curseur par défaut ](images/ctrl-sliders-image6.png)

    Dans cet exemple, la taille par défaut est utilisée.

-   **N’étiquetez pas toutes les graduations.**

## <a name="recommended-sizing-and-spacing"></a>Dimensionnement et espacement recommandés

![figure du dimensionnement et de l’espacement de curseur recommandés ](images/ctrl-sliders-image7.png)

Dimensionnement et espacement recommandés pour les curseurs.

## <a name="labels"></a>Étiquettes

### <a name="slider-labels"></a>Étiquettes de curseur

-   Utilisez une étiquette de texte statique se terminant par un signe deux-points, ou une étiquette de zone de groupe sans ponctuation finale.
-   Attribuez une clé d’accès unique à chaque étiquette. Pour connaître les instructions d’affectation, consultez [clavier](inter-keyboard.md).
-   Utilisez les majuscules comme pour les phrases.
-   Placez l’étiquette du curseur à gauche du curseur ou au-dessus et alignée sur le bord gauche du curseur (ou sur son identificateur de plage de gauche, le cas échéant).

### <a name="range-labels"></a>Étiquettes de plage

-   Étiquetez les deux extrémités de la plage du curseur, à moins que cela ne soit pas nécessaire avec une orientation verticale.
-   Utilisez uniquement Word, si possible, pour chaque étiquette.
-   N’utilisez pas de ponctuation finale.
-   Veillez à ce que ces étiquettes soient descriptives et balancées. Exemples : Maximum/Minimum, Plus/Moins, Bas/Haut, Faible/Fort.
-   Utilisez les majuscules comme pour les phrases.
-   N’affectez pas de clés d’accès.

### <a name="value-labels"></a>Étiquettes de valeur

-   Si vous nécessitez une étiquette de valeur, affichez-la sous le curseur.
-   Centrez le texte relatif au contrôle et ajoutez les unités (telles que pixels).

    ![figure de l’étiquette centrée sous le curseur ](images/ctrl-sliders-image8.png)

    Dans cet exemple, l’étiquette de valeur est centrée sous le curseur et comprend les unités.

## <a name="documentation"></a>Documentation

Lorsque vous faites référence à des curseurs :

-   Utilisez le texte d’étiquette exact, y compris sa mise en majuscules, et incluez le curseur de mot. N’incluez pas le trait de soulignement ou le signe deux-points.
-   Pour décrire l’interaction de l’utilisateur, utilisez Move.
-   Dans la mesure du possible, mettez en forme l’étiquette à l’aide de texte en gras. Sinon, placez l’étiquette entre guillemets uniquement si nécessaire pour éviter toute confusion.

Exemple : pour augmenter la résolution de l’écran, déplacez le curseur **résolution d’écran** vers la droite.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Glossaire](glossary.md)
</dt> </dl>

 

 