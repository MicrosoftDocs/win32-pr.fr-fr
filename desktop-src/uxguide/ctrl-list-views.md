---
title: Affichages de liste
description: Avec un affichage de liste, les utilisateurs peuvent afficher et interagir avec une collection d’objets de données, à l’aide d’une sélection unique ou d’une sélection multiple.
ms.assetid: 62a7bfc8-96a9-450d-9db9-ec9dab6687b7
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: c3c823b23c03f29ac6b80e10df79eac36653f2e4
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "103761282"
---
# <a name="list-views"></a>Affichages de liste

> [!NOTE]
> Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Avec un affichage de liste, les utilisateurs peuvent afficher et interagir avec une collection d’objets de données, à l’aide d’une sélection unique ou d’une sélection multiple.

![capture d’écran de l’affichage de liste avec en-têtes de colonnes ](images/ctrl-list-views-image1.png)

Affichage de liste classique.

Les affichages de liste offrent plus de flexibilité et de fonctionnalités que les zones de liste. Contrairement aux zones de liste, elles prennent en charge la modification des vues, des regroupements, de plusieurs colonnes avec des en-têtes, le tri par colonnes, la modification de la largeur et de l’ordre des colonnes, la source du glissement ou la cible de déplacement, ainsi que la copie des données vers et depuis le presse-papiers.

> [!Note]  
> Les instructions relatives à la [disposition](vis-layout.md) et aux [zones de liste](ctrl-list-boxes.md) sont présentées dans des articles distincts.

 

## <a name="is-this-the-right-control"></a>Est-ce le contrôle approprié ?

Un affichage de liste est plus qu’une zone de liste fonctionnelle plus flexible : ses fonctionnalités supplémentaires entraînent une utilisation différente. Le tableau suivant présente la comparaison.



|                             |                                           |                                                                                                                                               |
|-----------------------------|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
|                             | **Zones de liste**<br/>                 | **Affichages de liste**<br/>                                                                                                                     |
| **Type de données**<br/>    | Options de données et de programme.<br/> | Données uniquement.<br/>                                                                                                                         |
| **Contents**<br/>     | Étiquettes uniquement.<br/>                   | Étiquettes et données auxiliaires, éventuellement dans plusieurs colonnes.<br/>                                                                           |
| **Interaction**<br/>  | Utilisé pour effectuer des sélections.<br/>    | Peut être utilisé pour effectuer des sélections, mais souvent utilisé pour afficher et interagir avec les données. Peut être une source de glissement ou une cible de déplacement.<br/> |
| **Présentation**<br/> | Des.<br/>                         | Les utilisateurs peuvent modifier les affichages, les regrouper, les trier par colonnes et modifier la largeur et l’ordre des colonnes.<br/>                                                |



 

Pour déterminer s’il s’agit du bon contrôle, posez-vous les questions suivantes :

-   **La liste présente-t-elle des données plutôt que des options de programme ?** Si ce n’est pas le cas, envisagez plutôt d’utiliser une zone de liste.
-   **Les utilisateurs doivent-ils modifier les affichages, les regrouper, les trier par colonnes ou modifier la largeur et l’ordre des colonnes ?** Dans le cas contraire, utilisez une zone de liste à la place.
-   **Le contrôle doit-il être une source de glissement ou une cible de déplacement ?** Dans ce cas, utilisez un mode liste.
-   **Les éléments de la liste doivent-ils être copiés ou collés à partir du presse-papiers ?** Dans ce cas, utilisez un mode liste.

### <a name="check-box-list-views"></a>Affichages de liste de cases à cocher

-   **Le contrôle est-il utilisé pour choisir zéro élément ou plus dans une liste de données ?** Pour choisir un élément, utilisez une sélection unique à la place.
-   **La sélection multiple est-elle essentielle pour la tâche ou couramment utilisée ?** Dans ce cas, utilisez une vue de liste de cases à cocher pour rendre la sélection multiple évidente, surtout si vos utilisateurs cibles ne sont pas avancés. Si ce n’est pas le cas, utilisez un affichage de liste à sélection multiple standard si les cases à cocher attirent trop l’attention sur une sélection multiple ou entraînent une trop grande encombrement de l’écran.
-   **La stabilité de la sélection multiple est-elle importante ?** Dans ce cas, utilisez une liste de cases [à cocher](ctrl-list-boxes.md), un générateur de listes ou une liste ajouter/supprimer, car le fait de cliquer sur modifie un seul élément à la fois. Avec une liste de sélection multiple standard, il est très facile de supprimer toutes les sélections, même par accident.

> [!Note]  
> Parfois, un contrôle ressemblant à un affichage de liste est implémenté à l’aide d’une zone de liste, et vice versa. Dans ce cas, appliquez les instructions en fonction de l’utilisation, et non de l’implémentation.

 

## <a name="usage-patterns"></a>Modèles d’usage

Toutes les vues prennent en charge la sélection unique, où les utilisateurs peuvent sélectionner un seul élément à la fois, et plusieurs sélections, où les utilisateurs peuvent sélectionner n’importe quel nombre d’éléments, y compris aucun. Les affichages de liste prennent en charge le [mode de sélection étendue](glossary.md), où la sélection peut être étendue en faisant glisser ou en appuyant sur Maj + clic ou Ctrl + clic pour sélectionner respectivement des groupes de valeurs contiguës ou non adjacentes. Contrairement aux zones de liste, elles ne prennent pas en charge le [mode de sélection multiple](glossary.md), où le fait de cliquer sur un élément fait basculer son état de sélection indépendamment des touches Maj et Ctrl.

### <a name="standard-list-view"></a>Mode liste standard

Le contrôle List View prend en charge cinq vues standard :



|                                                                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Vignette**<br/> chaque élément apparaît sous la forme d’une icône moyenne, avec une étiquette et des détails facultatifs à droite. <br/>                                                                                                                         | ![capture d’écran des miniatures avec titres et détails ](images/ctrl-list-views-image2.png)<br/> L’affichage en mosaïque affiche des icônes moyennes avec des étiquettes et des détails facultatifs sur la droite.<br/>                                                                                                                                                                |
| **Grande icône**<br/> chaque élément apparaît sous la forme d’une icône très grande, grande ou moyenne avec une étiquette au-dessous.<br/>                                                                                                                      | ![capture d’écran de la grande vue de liste de miniatures ](images/ctrl-list-views-image3.png)<br/> Affichage de grande icône affiche chaque élément sous la forme d’une grande icône avec une étiquette au-dessous.<br/>                                                                                                                                                                              |
| **Petite icône**<br/> chaque élément apparaît sous la forme d’une petite icône avec une étiquette à droite.<br/>                                                                                                                                           | ![capture d’écran de la petite vue de liste de miniatures ](images/ctrl-list-views-image4.png)<br/> Affichage des petites icônes affiche chaque élément sous la forme d’une petite icône avec son étiquette à droite.<br/>                                                                                                                                                                        |
| **Liste**<br/> chaque élément apparaît sous la forme d’une petite icône avec une étiquette à droite.<br/>                                                                                                                                                 | en mode liste, cette vue commande les éléments dans les colonnes et utilise une barre de défilement horizontale. en revanche, les modes d’affichage des icônes ordonnent les éléments dans les lignes et utilisent une barre de défilement verticale. <br/> ![capture d’écran de la vue liste en mode liste ](images/ctrl-list-views-image5.png)<br/> Mode liste affiche chaque élément sous la forme d’une petite icône avec son étiquette à droite.<br/> |
| **Détails**<br/> chaque élément apparaît sous la forme d’une ligne dans un format tabulaire. la colonne la plus à gauche contient l’icône et l’étiquette facultatives de l’élément, et les colonnes suivantes contiennent des informations supplémentaires, telles que des propriétés d’élément.<br/> | en outre, des colonnes peuvent être ajoutées ou supprimées, réorganisées et redimensionnées. les lignes peuvent être regroupées, triées par colonne. <br/> ![capture d’écran de l’affichage des listes en mode Détails ](images/ctrl-list-views-image6.png)<br/> Mode Détails affiche chaque élément sous la forme d’une ligne dans un tableau.<br/>                                                              |



 

### <a name="list-view-variations"></a>Variations du mode liste



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Sélecteur de colonnes</strong><br/> Les affichages de listes comportent parfois autant de colonnes qu’il n’est pas pratique de les afficher toutes. Dans ce cas, la meilleure approche consiste à afficher les colonnes les plus utiles par défaut et à autoriser les utilisateurs à ajouter ou supprimer des colonnes en fonction des besoins. <br/></td>
<td><img src="images/ctrl-list-views-image7.png" alt="Screen shot of list view with Column Chooser menu " /><br/> Cliquez avec le bouton droit sur l’en-tête de colonne pour afficher un menu contextuel qui permet aux utilisateurs d’ajouter ou de supprimer des colonnes.<br/> <img src="images/ctrl-list-views-image8.png" alt="Screen shot of Choose Details dialog box " /><br/> Cliquez sur plus dans le menu contextuel de l’en-tête de colonne pour afficher la boîte de dialogue Choisir les colonnes, qui permet aux utilisateurs d’ajouter ou de supprimer des colonnes, ainsi que de les réorganiser.<br/></td>
</tr>
<tr class="even">
<td><strong>Vue de la liste de cases à cocher</strong><br/> Permet aux utilisateurs de sélectionner plusieurs éléments.<br/></td>
<td>Les affichages de liste de sélection multiple ont exactement la même apparence que les affichages de liste à sélection unique, de sorte qu’il n’y a aucun indice visuel qu’ils prennent en charge la sélection multiple. Une vue de liste de cases à cocher peut être utilisée pour indiquer clairement que plusieurs sélections sont possibles. Par conséquent, ce modèle doit être utilisé pour les tâches où la sélection multiple est essentielle ou couramment utilisée.<br/> <img src="images/ctrl-list-views-image9.png" alt="Screen shot of dialog box with several check boxes " /><br/> Dans cet exemple, une petite vue d’icône utilise des cases à cocher, car la sélection multiple est essentielle à la tâche.<br/></td>
</tr>
<tr class="odd">
<td><strong>Affichages de listes avec groupes</strong><br/> Organisez les données en groupes.<br/></td>
<td>Alors que les vues de détails prennent souvent en charge le tri des données par l’une des colonnes, les vues de liste permettent aux utilisateurs d’organiser les éléments en groupes. Voici quelques-uns des avantages du regroupement :<br/>
<ul>
<li>Comme les groupes fonctionnent dans tous les affichages (à l’exception de la liste), par exemple, les utilisateurs peuvent regrouper une grande vue d’icônes supplémentaires d’albums par artiste.</li>
<li>Les groupes peuvent être des collections de haut niveau, qui sont souvent plus explicites que le regroupement des données directement. Par exemple, l’Explorateur Windows regroupe les dates dans aujourd’hui, hier, la semaine dernière, plus tôt cette année et il y A longtemps.</li>
</ul>
<img src="images/ctrl-list-views-image10.png" alt="Screen shot of list view with several data groups " /><br/> Dans cet exemple, le centre d’accueil Windows affiche des éléments groupés en mode liste.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a>Consignes

### <a name="presentation"></a>Présentation

-   **Triez les éléments de liste dans un ordre logique.** Triez les noms dans l’ordre alphabétique, les nombres dans l’ordre numérique et les dates dans l’ordre chronologique.
-   **Le cas échéant, autorisez les utilisateurs à modifier l’ordre de tri.** Le tri des utilisateurs est important si la liste contient de nombreux éléments ou s’il existe des scénarios où les éléments sont trouvés plus efficacement à l’aide d’un ordre de tri autre que celui par défaut.
-   **Utilisez l’attribut toujours afficher la sélection** afin que les utilisateurs puissent facilement déterminer l’élément sélectionné, même si le contrôle n’a pas le focus.
-   **Évitez de présenter des vues de liste vides.** Si les utilisateurs créent une liste, initialisez la liste avec des instructions ou des exemples d’éléments dont les utilisateurs peuvent avoir besoin.

    ![capture d’écran de la boîte de dialogue Rechercher avec des instructions ](images/ctrl-list-views-image11.png)

    Dans cet exemple, la liste de recherche affiche initialement des instructions.

-   **Si les utilisateurs peuvent modifier des affichages, regrouper, Trier par colonnes ou modifier des colonnes, ainsi que leurs largeurs et leur ordre, rendez ces paramètres persistants pour qu’ils prennent effet lors de la prochaine affichage de la liste.** Les rendre persistantes en fonction de la liste, par utilisateur.

### <a name="interaction"></a>Interaction

-   **Utilisez un simple clic pour sélectionner l’élément de liste sur lequel l’utilisateur pointe. Exception :** pour le modèle de liste de liens de commande, un simple clic sélectionne l’élément et ferme la fenêtre ou accède à la page suivante.
-   **Envisagez de fournir un comportement de double-clic.** Double-cliquez sur doit avoir le même effet que la sélection d’un élément et l’exécution de sa commande par défaut.
-   **Effectuez un double-clic sur le comportement redondant.** Il doit toujours y avoir un bouton de commande ou une commande de menu contextuel qui a le même effet.
-   Si un élément de liste requiert une explication supplémentaire, **fournissez l’explication dans une** [info-bulle](ctrl-tooltips-and-infotips.md). Utilisez des phrases complètes et terminez la ponctuation.

    ![capture d’écran de la vue liste avec l’info-bulle du clavier ](images/ctrl-list-views-image12.png)

    Dans cet exemple, une info-bulle est utilisée pour fournir des informations supplémentaires.

-   **Fournissez des menus contextuels des commandes appropriées.** Ces commandes incluent couper, copier, coller, supprimer ou supprimer, renommer et propriétés.
-   **Si les utilisateurs peuvent modifier l’ordre de tri et le regroupement, fournissez des menus contextuels Trier par et regrouper par.** Le premier clic sur un nom de colonne trie ou regroupe la liste dans l’ordre croissant de cette colonne, le deuxième clic trie ou regroupe dans l’ordre décroissant. Utilisez la commande précédente (d’une autre colonne) comme clé secondaire.

    ![capture d’écran de l’affichage de liste avec le menu « Trier par » ](images/ctrl-list-views-image13.png)

    Dans cet exemple, le menu contextuel Trier par modifie l’ordre de tri. Cliquer sur nom une fois trie par nom dans l’ordre croissant. Le fait de cliquer à nouveau sur nom effectue un tri par nom dans l’ordre décroissant.

-   **Rendez l’en-tête de colonne de la vue liste accessible à l’aide du clavier.**
    -   **Développeurs :** Pour ce faire, vous pouvez définir le focus sur le contrôle d’en-tête de colonne. Cette fonctionnalité est une nouveauté de Windows Vista.
-   **Lorsque vous désactivez un mode liste, désactivez également les étiquettes et les boutons de commande associés.**
-   **Évitez le défilement horizontal.** Le mode liste utilise le défilement horizontal. Ce mode est généralement le plus compact, mais le défilement horizontal est généralement plus difficile à utiliser que le défilement vertical. Utilisez plutôt la vue petite icône si la compacité n’est pas importante. Toutefois, le mode liste est un bon choix lorsqu’il existe de nombreux éléments triés par ordre alphabétique et un espace d’écran suffisant pour un contrôle large.

    **Acceptable:**

    ![capture d’écran d’un contrôle en mode liste étendu ](images/ctrl-list-views-image14.png)

    Dans cet exemple, le mode liste est utilisé, car il existe de nombreux éléments et une grande quantité d’espace écran disponible pour un contrôle large.

### <a name="multiple-selection-lists"></a>Listes à sélection multiple

-   **Envisagez d’afficher le nombre d’éléments sélectionnés sous la liste**, en particulier si les utilisateurs sont susceptibles de sélectionner plusieurs éléments. Ces informations fournissent non seulement des commentaires utiles, mais indiquent clairement que le mode liste prend en charge la sélection multiple.

    ![capture d’écran de la liste des cinq miniatures sélectionnées ](images/ctrl-list-views-image15.png)

    Dans cet exemple, le nombre d’éléments sélectionnés est affiché sous la liste.

-   Au lieu d’utiliser le nombre d’éléments sélectionnés, vous pouvez également fournir d’autres mesures de sélection qui peuvent être plus explicites, telles que les ressources requises pour les sélections.

    ![capture d’écran de la boîte de dialogue montrant l’espace disque ](images/ctrl-list-views-image16.png)

    Dans cet exemple, l’espace disque requis pour installer les composants est plus significatif que le nombre de composants sélectionnés.

-   Pour les affichages de liste de cases à cocher, s’il y a un grand nombre d’éléments et si vous en sélectionnez ou en désactivant tous, vous pouvez ajouter des boutons de commande Sélectionner tout et effacer tout.
-   **Utilisez les cases à cocher à état mixte pour indiquer la sélection partielle des éléments d’un conteneur.** L’État mixte n’est pas utilisé comme troisième État pour un élément individuel.

### <a name="changing-views"></a>Modification des vues

Si les utilisateurs peuvent modifier des affichages :

-   **Choisissez l’affichage le plus pratique par défaut.** Toutes les modifications apportées par les utilisateurs doivent être rendues persistantes en fonction de la liste, par utilisateur.
-   **Modifiez l’affichage à l’aide d’un bouton partagé, d’un bouton de menu ou d’une liste déroulante.** Lorsque cela est possible, utilisez un [bouton partagé](ctrl-command-buttons.md) sur la barre d’outils et modifiez l’étiquette du bouton pour refléter l’affichage actuel.

    ![capture d’écran de la liste avec le bouton fractionner les affichages ](images/ctrl-list-views-image17.png)

    Dans cet exemple, un bouton partagé sur la barre d’outils est utilisé pour modifier les affichages.

-   **Fournissez un menu contextuel d’affichage.**

    ![capture d’écran de la liste avec le menu contextuel « View » ](images/ctrl-list-views-image18.png)

Dans cet exemple, un menu contextuel d’affichage est utilisé pour modifier les affichages.

### <a name="details-views"></a>Vues de détails

-   **Envisagez d’utiliser la vue vignettes pour améliorer la lisibilité.**

    **Acceptable:**

    ![capture d’écran de la liste des détails avec des colonnes étroites ](images/ctrl-list-views-image19.png)

    Dans cet exemple, il y a trop de données et la fenêtre, la liste et les colonnes sont trop petites, ce qui rend difficile la lecture des éléments de la liste.

    **Conseillé**

    ![capture d’écran de la liste des détails avec des données dans des groupes ](images/ctrl-list-views-image20.png)

    Dans cet exemple, l’affichage en mosaïque affiche les données sans troncation.

-   **Choisissez des largeurs de colonne par défaut appropriées pour les données les plus longues.** Les affichages de liste tronquent automatiquement les longues données avec des ellipses, de sorte que les largeurs de colonne sont appropriées si le nombre de ellipses affichées par défaut est réduit. Si les utilisateurs peuvent redimensionner des colonnes, préférez d’autres solutions :

    -   Ajuster la largeur de chaque colonne en fonction de ses données.
    -   Dimensionnez la largeur du contrôle en fonction de ses colonnes, ainsi que des barres de défilement probables.
    -   Si nécessaire, utilisez le défilement horizontal.
    -   Avoir des données tronquées uniquement pour les éléments de taille inhabituelles ou en dernier recours.

    Si les données de taille normale doivent être tronquées par défaut, rendez la fenêtre et la vue de liste redimensionnables. Incluez 30 pour cent supplémentaires (jusqu’à 200 pour cent pour du texte plus petit) pour tout texte (mais pas les nombres) qui sera localisé.

    **Incorrect :**

    ![capture d’écran des colonnes de liste avec des données tronquées ](images/ctrl-list-views-image21.png)

    Dans cet exemple, la plupart des données sont tronquées. Les nombreuses ellipses indiquent clairement que les largeurs de contrôle et de colonne sont trop petites pour les données.

    **Incorrect :**

    ![capture d’écran d’une liste d’une colonne avec des données tronquées ](images/ctrl-list-views-image22.png)

    Dans cet exemple, les données sont tronquées sans raison.

-   **Choisissez un ordre de colonne par défaut approprié.** En règle générale, ordonnez les colonnes comme suit :

    -   Tout d’abord, le nom de l’élément ou les données d’identification.
    -   Ensuite, d’autres données utiles pour différencier les éléments de la liste.
    -   Ensuite, les données les plus utiles (de préférence de longueur réduite ou de longueur fixe).
    -   Les données suivantes, moins utiles (plutôt que courtes ou de longueur fixe).
    -   Données de longueur variable de type Last, long.

    Long, longueur variable : les données sont placées dans les dernières colonnes pour réduire le besoin de défilement horizontal. Au sein de ces catégories, placez les informations associées ensemble dans une séquence logique.

-   **Le cas échéant, autorisez les utilisateurs à ajouter et à supprimer des colonnes, ainsi que de modifier l’ordre.** Affichez les colonnes les plus utiles par défaut. Pour cela, vous devez utiliser l’attribut glisser-déplacer d’en-tête.
-   Choisissez un alignement adapté aux données. Utilisez les règles suivantes :
    -   Aligner à droite les nombres, les devises et les heures.
    -   Aligne à gauche le texte, les ID (même si numériques) et les dates.
-   Pour les en-têtes de colonne pouvant être triés, **le premier clic sur un en-tête trie la liste dans l’ordre croissant de la colonne, le deuxième clic trie dans l’ordre décroissant.** Utilisez l’ordre de tri précédent (d’une autre colonne) comme clé de tri secondaire.

    ![capture d’écran de la liste des détails avec données triées ](images/ctrl-list-views-image23.png)

    Dans cet exemple, le nom de la colonne a été cliqué en premier, puis la colonne Type. Par conséquent, le type par ordre croissant est la clé de tri principale et le nom par ordre croissant est le réplica secondaire.

-   **Utilisez l’attribut de sélection de ligne complète** afin que les utilisateurs puissent facilement déterminer les éléments sélectionnés dans toutes les colonnes.
-   **N’utilisez pas d’en-tête de colonne triable, sauf si les données peuvent être triées.**
-   **N’utilisez pas d’en-tête de colonne s’il n’existe qu’une seule colonne et qu’il n’est pas nécessaire d’inverser le tri.** Utilisez plutôt une étiquette pour identifier les données.

    **Incorrect :**

    ![capture d’écran de la liste avec étiquette dans l’en-tête de colonne ](images/ctrl-list-views-image24.png)

    **Correct :**

    ![capture d’écran de la liste avec l’étiquette au-dessus du contrôle ](images/ctrl-list-views-image25.png)

    Dans l’exemple correct, une étiquette est utilisée à la place d’un en-tête de colonne.

## <a name="recommended-sizing-and-spacing"></a>Dimensionnement et espacement recommandés

![capture d’écran de la taille et de l’espacement des listes ](images/ctrl-list-views-image26.png)

Dimensionnement et espacement recommandés pour les affichages de liste.

-   **Choisissez une hauteur de mode liste qui affiche un nombre entier d’éléments.** Évitez de tronquer les éléments verticalement.
-   **Choisissez une taille de vue de liste qui élimine les défilements verticaux et horizontaux inutiles dans toutes les vues prises en charge.** Les affichages de liste doivent afficher entre 3 et 20 éléments. Envisagez de rendre un affichage de liste légèrement plus grand si vous supprimez une barre de défilement. Les listes contenant potentiellement de nombreux éléments doivent afficher au moins cinq éléments pour faciliter le défilement en affichant plus d’éléments à la fois et en rendant la barre de défilement plus facile à positionner.
-   **Si les utilisateurs tirent parti de la taille de la liste, faites en sorte que la vue liste et la fenêtre parente soient redimensionnables.** Cela permet aux utilisateurs d’ajuster la taille de la vue de liste en fonction des besoins. Toutefois, les vues de liste redimensionnables doivent afficher au moins trois éléments.

## <a name="labels"></a>Étiquettes

### <a name="control-labels"></a>Étiquettes de contrôle

-   Toutes les vues de liste ont besoin d’étiquettes. Écrivez l’étiquette sous la forme d’un mot ou d’une expression, et non pas sous forme de phrase, en se terminant par un signe deux-points utilisant du texte statique.
-   Attribuez une [clé d’accès](glossary.md) unique pour chaque étiquette. Pour obtenir des instructions, consultez [clavier](inter-keyboard.md).
-   Utilisez la mise [en majuscules de style phrase](glossary.md).
-   Placez l’étiquette au-dessus du contrôle et alignez l’étiquette avec le bord gauche du contrôle.
-   Pour les affichages de liste à sélection multiple, écrivez l’étiquette qui indique clairement que plusieurs sélections sont possibles. Les étiquettes de vue de liste de cases à cocher peuvent être moins explicites.

    **Correct :**

    ![capture d’écran de l’étiquette : sélectionner un ou plusieurs modules complémentaires ](images/ctrl-list-views-image27.png)

    Dans cet exemple, l’étiquette indique clairement que plusieurs sélections sont possibles.

    **Incorrect :**

    ![capture d’écran de l’étiquette : Modules complémentaires ](images/ctrl-list-views-image28.png)

    Dans cet exemple, l’étiquette ne fournit aucune information sur la sélection multiple.

    **Acceptable:**

    ![capture d’écran de l’étiquette de la liste de cases à cocher : Modules complémentaires ](images/ctrl-list-views-image29.png)

    Dans cet exemple, les cases à cocher indiquent clairement que plusieurs sélections sont possibles, de sorte que l’étiquette n’a pas besoin d’être explicite.

-   Vous pouvez spécifier des unités (secondes, connexions, etc.) entre parenthèses après l’étiquette.

### <a name="heading-labels"></a>Étiquettes d’en-tête

-   Conservez les étiquettes de titre brèves (trois mots ou moins).
-   Utilisez un nom unique ou une expression nominale sans ponctuation finale.
-   Utilisez la mise [en majuscules de style phrase](glossary.md).
-   Alignez l’en-tête de la même façon que les données.

### <a name="group-labels"></a>Étiquettes de groupe

-   Utilisez les étiquettes de groupe suivantes pour les collections de haut niveau :
    -   Noms : utilisez la première lettre de nom ou les plages de lettres.
    -   Tailles : non spécifié, 0 Ko, 0-10 Ko, 10-100 Ko, 100 Ko-1 Mo, 1-16 Mo, 16-128 Mo
    -   Dates : aujourd’hui, hier, dernière semaine, plus tôt cette année et il y a longtemps.
-   Sinon, les étiquettes de groupe utilisent le texte exact des données regroupées, y compris la mise en majuscules et la ponctuation.

### <a name="data-text"></a>Texte de données

-   Utilisez la mise [en majuscules de style phrase](glossary.md).

### <a name="instructional-text"></a>Texte d’instructions

-   Si vous devez ajouter du texte d’instructions sur un mode liste, ajoutez-le au-dessus de l’étiquette. Utilisez des phrases complètes avec la ponctuation finale.
-   Utilisez la mise [en majuscules de style phrase](glossary.md).
-   Les informations supplémentaires qui sont utiles, mais pas nécessaires, doivent être courtes. Placez ces informations entre parenthèses entre l’étiquette et le signe deux-points ou sans les parenthèses sous le contrôle.

## <a name="documentation"></a>Documentation

Lorsque vous faites référence à des affichages de liste :

-   Utilisez le texte d’étiquette exact, y compris sa mise en majuscules, mais n’incluez pas le trait de soulignement ou le signe deux-points, et incluez la liste de mots. Ne faites pas référence à une zone de liste sous la forme d’une zone de liste, d’un affichage de liste ou d’un champ.
-   Pour les données de liste, utilisez le texte exact, y compris la mise en majuscules.
-   Reportez-vous aux affichages de liste sous forme d’affichages de listes uniquement en programmation et dans une documentation technique. Partout ailleurs, utilisez la liste.
-   Pour décrire l’interaction avec l’utilisateur, utilisez SELECT pour les données, puis cliquez sur pour les en-têtes.
-   Dans la mesure du possible, mettez en forme les options d’étiquette et de liste en texte gras. Sinon, placez l’étiquette et les options entre guillemets uniquement si nécessaire pour éviter toute confusion.

Exemple : dans la liste **programmes et services** , sélectionnez **partage de fichiers et d’imprimantes**.

Lorsque vous faites référence à des cases à cocher en mode liste :

-   Utilisez le texte d’étiquette exact, y compris sa mise en majuscules, et incluez la case à cocher mot. N’incluez pas le trait de soulignement de clé d’accès.
-   Pour décrire l’interaction de l’utilisateur, utilisez sélectionner et effacer.
-   Dans la mesure du possible, mettez en forme l’étiquette à l’aide de texte en gras. Sinon, placez l’étiquette entre guillemets uniquement si nécessaire pour éviter toute confusion.

Exemple : activez la case à cocher **souligner** .

 

