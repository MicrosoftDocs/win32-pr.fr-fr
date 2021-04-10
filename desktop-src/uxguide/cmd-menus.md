---
title: Menus (concepts de base de la conception)
description: Les menus sont des listes hiérarchiques de commandes ou d’options disponibles pour les utilisateurs dans le contexte actuel.
ms.assetid: 3772ff8e-8057-476d-b62b-efbd5e07907f
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 8054a01e4198f3592a34ae09635dd60f392da1eb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104211184"
---
# <a name="menus-design-basics"></a>Menus (concepts de base de la conception)

> [!NOTE]
> Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Les menus sont des listes hiérarchiques de commandes ou d’options disponibles pour les utilisateurs dans le contexte actuel.

Les menus déroulants sont des menus affichés à la demande au clic ou au survol de la souris. Elles sont normalement masquées et constituent donc un moyen efficace de conserver de l’espace à l’écran. Un sous-menu ou un menu en cascade est un menu secondaire affiché à la demande à partir d’un menu. Elles sont indiquées par une flèche à la fin de l’étiquette du sous-menu. Un élément de menu est une commande ou une option individuelle au sein d’un menu.

Les menus sont souvent affichés à partir d’une barre de menus, qui est une liste de catégories de menus étiquetées généralement située près du haut d’une fenêtre. En revanche, un menu contextuel s’interrompt lorsque les utilisateurs cliquent avec le bouton droit sur un objet ou une zone de fenêtre qui prend en charge un menu contextuel.

![capture d’écran de la barre de menus avec menu et sous-menu ](images/cmd-menus-image1.png)

Barre de menus classique affichant un menu déroulant et un sous-menu.

> [!Note]  
> Les instructions relatives aux [boutons de commande](ctrl-command-buttons.md), aux [barres d’outils](cmd-toolbars.md)et au [clavier](inter-keyboard.md) sont présentées dans des articles distincts.

 

## <a name="usage-patterns"></a>Modèles d’usage

Les menus ont plusieurs modèles d’utilisation :



|                                                                                                                                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Barres de menus**<br/> une barre de menus affiche les commandes et les options dans les menus déroulants. <br/>                                               | les barres de menus sont très courantes et faciles à trouver, ainsi qu’une utilisation efficace de l’espace. <br/> ![capture d’écran de la barre de menus avec le menu déroulant ](images/cmd-menus-image2.png)<br/> Barre de menus de Windows Mail.<br/>                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Menus de la barre d’outils**<br/> barre de menus implémentée en tant que barre d’outils. <br/>                                                                   | les menus de la barre d’outils sont des barres d’outils constituées principalement de commandes dans les [boutons de menu](ctrl-command-buttons.md) et les boutons partagés, avec seulement quelques commandes directes, le cas échéant. <br/> ![capture d’écran du menu déroulant de la barre d’outils ](images/cmd-menus-image3.png)<br/> Menu de barre d’outils dans la Galerie de photos Windows.<br/> Pour obtenir des instructions sur ce modèle, consultez [barres d’outils](cmd-toolbars.md).<br/>                                                                                                                                                                                                             |
| **Menus d’onglets**<br/> boutons dans les onglets qui affichent un petit ensemble de commandes et d’options relatives à un onglet dans un menu déroulant. <br/> | les onglets avec des menus ressemblent à des onglets ordinaires, à l’exception de leur partie inférieure, avec un bouton avec flèche déroulante. le fait de cliquer sur le bouton affiche un menu déroulant au lieu de sélectionner l’onglet. <br/> ![capture d’écran du menu d’onglets avec le menu déroulant ](images/cmd-menus-image4.png)<br/> Les menus d’onglets sont utilisés dans le lecteur Windows Media.<br/>                                                                                                                                                                                                                                                                                           |
| **Boutons de menu**<br/> boutons de commande qui affichent un petit ensemble de commandes associées dans un menu déroulant. <br/>                       | les [boutons de menu](ctrl-command-buttons.md) se présentent comme des boutons de commande ordinaires, sauf s’ils contiennent une flèche déroulante. le fait de cliquer sur le bouton affiche un menu déroulant au lieu d’exécuter une commande.<br/> les [boutons partagés](ctrl-command-buttons.md) sont similaires aux boutons de menu, à ceci près qu’ils sont des variantes d’une commande et qu’un clic sur la partie gauche du bouton effectue l’action directement sur l’étiquette.<br/> ![capture d’écran du bouton de menu avec des commandes déroulantes ](images/cmd-menus-image5.png)<br/> Bouton de menu avec un petit ensemble de commandes associées.<br/> |
| **Menu contextuels**<br/> menus déroulants qui affichent un petit ensemble de commandes et d’options liées au contexte actuel. <br/>       | liste déroulante des menus contextuels quand les utilisateurs cliquent avec le bouton droit sur un objet ou une zone de fenêtre qui prend en charge un menu contextuel. <br/> ![capture d’écran du menu contextuel affichant les commandes ](images/cmd-menus-image6.png)<br/> menu contextuel à partir de l’Explorateur Windows.<br/> Si les menus contextuels sont le meilleur choix de menu, mais que vous avez besoin d’une solution adaptée à tous les utilisateurs, vous pouvez utiliser un bouton de liste déroulante de menu. <br/> ![capture d’écran de la photo avec le bouton de menu déroulant ](images/cmd-menus-image7.png)<br/> Menu contextuel rendu visible avec un bouton déroulant de menu.<br/>                                                   |
| **Menus du volet des tâches**<br/> petit ensemble de commandes liées à l’objet ou au mode de programme sélectionné. <br/>                              | Contrairement aux menus contextuels, ils s’affichent automatiquement dans un volet de fenêtre, plutôt que sur demande. <br/> ![capture d’écran de la photo avec le menu du volet Office à droite ](images/cmd-menus-image8.png)<br/> Menu du volet des tâches de la visionneuse de la Galerie de photos Windows.<br/>                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="is-this-the-right-user-interface"></a>S’agit-il de l’interface utilisateur appropriée ?

Pour vous décider, posez-vous les questions suivantes :

### <a name="menu-bars"></a>Barres de menus

Les conditions suivantes s’appliquent :

-   La fenêtre est-elle une fenêtre principale ?
-   Existe-t-il un grand nombre d’éléments de menu ?
-   Existe-t-il plusieurs catégories de menu ?
-   La plupart des éléments de menu s’appliquent-ils à l’ensemble du programme et à la fenêtre principale ?
-   Le menu doit-il fonctionner pour tous les utilisateurs ?

Dans ce cas, envisagez d’utiliser une barre de menus.

### <a name="toolbar-menus"></a>Menus de la barre d’outils

Les conditions suivantes s’appliquent :

-   La fenêtre est-elle une fenêtre principale ?
-   La fenêtre a-t-elle une barre d’outils ?
-   Existe-t-il quelques catégories de menu ?
-   Le menu doit-il fonctionner pour tous les utilisateurs ?

Dans ce cas, envisagez d’utiliser un menu de barre d’outils au lieu de ou en plus d’une barre de menus.

### <a name="tab-menus"></a>Menus d’onglets

Les conditions suivantes s’appliquent :

-   La fenêtre est-elle une fenêtre principale ?
-   La fenêtre possède-t-elle des onglets, où chaque onglet est utilisé pour un ensemble de tâches dédié (par opposition à l’utilisation d’onglets pour afficher des vues différentes) ?
-   Existe-t-il une catégorie de menu qui s’applique à chaque onglet ?
-   Existe-t-il plusieurs commandes et options, mais uniquement un petit ensemble pour chaque onglet ?

Dans ce cas, envisagez d’utiliser un menu d’onglets à la place d’une barre de menus.

### <a name="context-menu"></a>Menu contextuel

Les conditions suivantes s’appliquent :

-   Existe-t-il un petit ensemble de commandes et d’options contextuelles qui s’appliquent à l’objet sélectionné ou à la région de fenêtre ?
-   Ces éléments de menu sont-ils redondants ?
-   Les utilisateurs cibles connaissent-ils les menus contextuels ?

Dans ce cas, envisagez de fournir des menus contextuels pour les objets et les régions de fenêtre qui en ont besoin.

Pour les programmes basés sur un navigateur, les menus du volet des tâches constituent une solution plus courante pour les commandes contextuelles. Actuellement, les utilisateurs attendent des menus contextuels dans les programmes basés sur le navigateur comme génériques et non utiles.

### <a name="task-pane-menu"></a>Menu du volet des tâches

Les conditions suivantes s’appliquent :

-   La fenêtre est-elle une fenêtre principale ?
-   Existe-t-il un petit ensemble de commandes et d’options contextuelles qui s’appliquent à l’objet sélectionné ou au mode programme ?
-   Existe-t-il quelques catégories de menu ?
-   Le menu doit-il fonctionner pour tous les utilisateurs ?

Dans ce cas, envisagez d’utiliser un menu de volet de tâches au lieu d’un menu contextuel.

## <a name="design-concepts"></a>Principes de conception

Des menus efficaces qui favorisent une expérience utilisateur optimale :

-   Utilisez une présentation de commande qui correspond à votre type de programme, aux types de fenêtres, à l’utilisation de la commande et aux utilisateurs cibles.
-   Sont bien organisés, à l’aide de l’organisation de menu standard, le cas échéant.
-   Utilisez efficacement des barres de menus, des barres d’outils et des menus contextuels.
-   Utilisez les icônes efficacement.
-   Utilisez les touches d’accès rapide et les touches de raccourci de manière efficace.

**Si vous n’avez qu’une seule chose...**

Choisissez une présentation de commande qui correspond à votre type de programme, aux types de fenêtres, à l’utilisation de la commande et aux utilisateurs cibles.

## <a name="guidelines"></a>Consignes

### <a name="general"></a>Général

-   **Tous les modèles de menu, à l’exception des barres de menus, ont besoin d’une flèche déroulante pour indiquer la présence d’un menu déroulant.** La présence de menus est sans dire dans une barre de menus, mais pas dans les autres modèles.
-   **Ne modifiez pas les noms des éléments de menu de manière dynamique.** Cela est confus et inattendu. Par exemple, ne modifiez pas l’option mode portrait en mode paysage lors de la sélection. Pour les modes, utilisez à la place des [puces et des coches](#bullets-and-checkmarks) .
    -   **Exception :** Vous pouvez modifier les noms des éléments de menu en fonction des noms d’objets de manière dynamique. Par exemple, les listes de fichiers récemment utilisés ou de noms de fenêtre peuvent être dynamiques.

### <a name="menu-bars"></a>Barres de menus

-   **Éliminez les barres de menus avec au moins trois catégories de menu.** S’il n’y a que quelques commandes, préférez des alternatives plus légères, telles que les menus de la barre d’outils, ou d’autres alternatives directes, comme des boutons de commande et des liens.
-   **N’avez pas plus de 10 catégories de menu.** Un trop grand nombre de catégories de menus est écrasant et rend la barre de menus difficile à utiliser.
-   **Envisagez de masquer la barre de menus** si la barre d’outils ou les commandes directes fournissent presque toutes les commandes nécessaires à la plupart des utilisateurs. Permet aux utilisateurs d’afficher ou de masquer une case à cocher de barre de menus dans un menu de la barre d’outils.

![capture d’écran de la liste d’options avec la barre de menus sélectionnée ](images/cmd-menus-image9.png)

Dans cet exemple, Windows Internet Explorer fournit une option de barre de menus.

Pour plus d’informations, consultez [masquage des barres de menus](#hiding-menu-bars).

### <a name="hiding-menu-bars"></a>Masquer les barres de menus

En règle générale, les barres d’outils fonctionnent bien avec les barres de menus, car elles permettent chacune de se concentrer sur leurs points forts sans compromis.

-   Masque la barre de menus par défaut si la barre de menus est redondante.
-   Masquez la barre de menus au lieu de la supprimer complètement, car les barres de menus sont plus accessibles aux utilisateurs du clavier.
-   Pour restaurer la barre de menus, fournissez une option de coche de barre de menus dans la catégorie de menu vue (pour les barres d’outils principales) ou outils (pour les barres d’outils secondaires). Pour plus d’informations, consultez [menu standard et boutons partagés](cmd-toolbars.md).

### <a name="menu-categories"></a>Catégories de menu

-   **Choisissez des noms de mots uniques pour les catégories de menu.** L’utilisation de plusieurs mots rend la séparation entre les catégories confuse.
-   **Pour les programmes qui créent ou affichent des documents, utilisez les catégories de menu standard** , telles que fichier, Edition, affichage, outils et aide. Cela rend les éléments de menu communs prévisibles et plus faciles à trouver.
-   **Pour les autres types de programmes, pensez à organiser vos commandes et options en catégories naturelles plus utiles,** en fonction de l’objectif de votre programme et de la façon dont les utilisateurs pensent à leurs tâches et objectifs. Ne vous inquiétez pas d’utiliser l’organisation du menu standard si elle ne convient pas à votre programme.
-   **Si vous choisissez d’utiliser des catégories de menu non standard, vous devez choisir des noms de catégories corrects.** Pour plus d’informations, consultez la section [étiquettes](#labels) .
-   **Préférer les catégories de menu orientées tâche sur les catégories génériques.** Les catégories orientées tâche rendent les éléments de menu plus faciles à trouver.

![capture d’écran de la barre de menus avec RIP, Burn et Sync ](images/cmd-menus-image10.png)

Dans cet exemple, le lecteur Windows Media utilise des catégories de menu orientées tâche.

-   **Évitez les catégories de menu avec un ou deux éléments de menu.** Si cela est raisonnable, consolidez-vous avec d’autres catégories de menus, éventuellement à l’aide d’un sous-menu.
-   **Envisagez de placer le même élément de menu dans plusieurs catégories uniquement si :**
    -   L’élément de menu appartient logiquement à plusieurs catégories de menu.
    -   Vous avez des données indiquant que les utilisateurs ont des difficultés à trouver l’élément dans une catégorie de menu unique.
    -   Vous n’avez qu’un ou deux éléments de menu difficiles à trouver dans plusieurs catégories.
-   **Ne placez pas d’autres éléments de menu qui utilisent le même nom dans plusieurs catégories.** Par exemple, vous ne disposez pas d’éléments de menu d’options différents dans plusieurs catégories.
    -   **Exception :** Le modèle de menu d’onglets peut avoir des options différentes et des éléments de menu aide dans chaque menu d’onglets.

![capture d’écran des menus d’onglets avec des éléments de menu répétés ](images/cmd-menus-image11.png)

Dans cet exemple, le lecteur Windows Media possède des options et des éléments de menu aide dans chaque menu d’onglets.

### <a name="menu-item-organization-and-order"></a>Organisation et ordre des éléments de menu

-   **Organisez les éléments de menu en groupes de sept ou moins d’éléments étroitement liés.** Pour ce faire, les sous-menus comptent comme un seul élément de menu dans le menu parent.
-   **Ne placez pas plus de 25 éléments dans un seul niveau d’un menu** (sans compter les sous-menus).
-   **Placez des séparateurs entre les groupes d’un menu.** Un séparateur est une ligne unique qui s’étend sur la largeur du menu.
-   **Dans un menu, placez les groupes dans leur ordre logique.** S’il n’y a pas d’ordre logique, commencez par placer les groupes les plus couramment utilisés.
-   **Dans un groupe, placez les éléments dans leur ordre logique.** S’il n’y a pas d’ordre logique, commencez par placer les éléments les plus couramment utilisés. Placez les éléments numériques (tels que les pourcentages de zoom) dans l’ordre numérique.

### <a name="submenus"></a>Submenus

-   **Évitez d’utiliser des sous-menus inutilement.** Les sous-menus nécessitent davantage d’efforts physiques et rendent généralement les éléments de menu plus difficiles à localiser.
-   **Ne placez pas les éléments de menu fréquemment utilisés dans un sous-menu.** Cela rendrait l’utilisation inefficace de ces commandes. Toutefois, vous pouvez placer les commandes fréquemment utilisées dans un sous-menu s’ils sont généralement accessibles plus directement, par exemple avec une barre d’outils.
-   **Envisagez d’utiliser un sous-menu dans les cas suivants :**
    -   Cela simplifie le menu parent, car il contient de nombreux éléments (20 ou plus), ou le sous-menu fait partie d’un groupe de plus de sept éléments.
    -   Les éléments du sous-menu sont utilisés moins fréquemment que ceux du menu parent.
    -   Le sous-menu contient au moins trois éléments.
    -   Il existe au moins trois commandes qui commencent par le même mot. Dans ce cas, utilisez ce mot comme étiquette de sous-menu.

![capture d’écran du menu « nouveau » avec quatre éléments de sous-menu ](images/cmd-menus-image12.png)

Dans cet exemple, le nouveau sous-menu remplace des commandes distinctes pour les nouveaux messages électroniques, les nouveaux messages de News, les nouveaux dossiers et les nouveaux contacts.

-   **Utilisez au plus trois niveaux de menus.** Autrement dit, vous pouvez avoir un menu principal et au plus deux niveaux de sous-menus. Deux niveaux de sous-menus doivent être rares.

### <a name="presentation"></a>Présentation

-   **Désactivez les éléments de menu qui ne s’appliquent pas au contexte actuel,** au lieu de les supprimer. Cela rend le contenu de la barre de menus stable et plus facile à trouver. **Exceptions :**
    -   Pour les catégories de menu contextuel, **supprimez plutôt que désactiver les éléments de menu contextuel qui ne s’appliquent pas au contexte actuel.** Une catégorie de menu est contextuelle lorsqu’elle est affichée uniquement pour des modes spécifiques, par exemple quand un certain type d’objet est sélectionné. Pour plus d’informations, consultez les instructions [Remove et Disable](#context-menus) pour les menus contextuels.
    -   Si la détermination du moment où un élément de menu doit être désactivé entraîne des problèmes de performances perceptibles, laissez l’élément de menu actif et, si nécessaire, la sélection génèrera un message d’erreur.

### <a name="tab-menus"></a>Menus d’onglets

-   **Chaque menu d’onglets peut avoir des options spécifiques au contexte et des éléments de menu aide.** Cela diffère de tous les autres modèles de menu. Chaque onglet est utilisé pour un ensemble de tâches dédié, de sorte que toute redondance à travers les menus d’onglets ne déroutant pas.

### <a name="context-menus"></a>Menu contextuels

-   **Utilisez les menus contextuels uniquement pour les commandes et les options contextuelles.** Les éléments de menu doivent s’appliquer uniquement à l’objet ou à la région de fenêtre sélectionné (ou cliqué sur), et non à l’ensemble du programme.
-   **Ne rendez pas les commandes disponibles dans les menus contextuels.** Comme les touches de raccourci, les menus contextuels constituent d’autres moyens d’exécuter des commandes et de choisir des options. Par exemple, une commande propriétés est également disponible via la barre de menus ou la touche d’accès Alt + Entrée.
-   **Fournissez des menus contextuels pour tous les objets et régions de fenêtre** qui tirent parti d’un petit ensemble de commandes et d’options contextuelles. De nombreux utilisateurs cliquent avec le bouton droit sur régulièrement et s’attendent à trouver des menus contextuels partout.
-   **Envisagez d’utiliser un bouton de liste déroulante de menu pour les menus contextuels ciblés sur tous les utilisateurs.** Normalement, les menus contextuels conviennent pour les commandes et les options destinées aux utilisateurs expérimentés. Toutefois, vous pouvez utiliser un bouton de liste déroulante de menu dans les cas où les menus contextuels constituent le meilleur choix de menu et que vous devez cibler tous les utilisateurs.

![capture d’écran de la photo avec le bouton de menu déroulant ](images/cmd-menus-image7.png)

Dans cet exemple, un bouton déroulant de menu est utilisé pour afficher un menu contextuel.

**Organisation et ordre des éléments de menu**

-   **Organisez les éléments de menu en groupes de sept ou moins d’éléments étroitement liés.**
-   **Évitez d’utiliser des sous-menus** pour conserver des menus contextuels simples, directs et efficaces.
-   **Ne placez pas plus de 15 éléments dans un menu contextuel.**
-   **Placez des séparateurs entre les groupes d’un menu.** Un séparateur est une ligne unique qui s’étend sur la largeur du menu.
-   **Présenter les éléments de menu dans l’ordre suivant :**

<dl> Commandes principales (les plus fréquemment utilisées)<dl> Ouvrir  
Exécuter  
Lire  
Étendue <separator>  
</dl> </dd> <dd>Commandes secondaires prises en charge par l’objet<dl> <separator>  
</dl> </dd> Commandes de transfert<dl> Couper  
Copier  
Insérer <separator>  
</dl> </dd> <dd>Paramètres d’objet<dl> <separator>  
</dl> </dd> Commandes de l’objet<dl> DELETE  
Renommer <separator>  
Propriétés
</dl> </dd> </dl>

**Présentation**

-   **Affichez la commande par défaut en utilisant le gras.** Lorsque cela est possible, définissez également le premier élément de menu. La commande par défaut est appelée lorsque les utilisateurs double-cliquent ou sélectionnent un objet et appuyez sur entrée.
-   **Supprimez plutôt que désactiver les éléments de menu contextuel qui ne s’appliquent pas au contexte actuel.** Ainsi, les menus contextuels sont contextuels et efficaces.
    -   **Exception :** Désactivez les éléments de menu qui ne s’appliquent pas s’il existe des attentes raisonnables pour qu’elles soient disponibles :
        -   Utilisez toujours les commandes de menu contextuel standard appropriées, telles que couper, copier, coller, supprimer et renommer.
        -   Toujours disposer des commandes qui complètent les jeux associés. Par exemple, s’il y a un arrière, il doit également s’agir d’un transfert. S’il existe une coupe, vous devez toujours copier et coller.

### <a name="bullets-and-checkmarks"></a>Puces et coches

-   **Les éléments de menu qui sont des options peuvent utiliser des puces et des coches.** Les commandes peuvent ne pas l’être.
-   **Utilisez une puce pour choisir une option dans un petit ensemble de choix s’excluant mutuellement.** Il doit toujours y avoir au moins deux puces dans un groupe. Pour plus d’informations, consultez cases d' [option](ctrl-radio-buttons.md).
-   **Utilisez une coche pour activer ou désactiver un paramètre indépendant.** Si les États sélectionnés et désactivés ne sont pas des opposés clairs et non ambigus, utilisez un ensemble de puces à la place. Pour plus d’informations, consultez [cases à cocher](ctrl-check-boxes.md).
-   **Pour un état de coche mixte, affichez un élément de menu sans coche.** L’État mixte est utilisé pour la sélection multiple pour indiquer que l’option est définie pour certains objets, mais pas tous, afin que chaque objet individuel ait l’état sélectionné ou désactivé. L’État mixte n’est pas utilisé comme troisième État pour un élément individuel.
-   **Placez les séparateurs entre les coches ou les puces associées.** Un séparateur est une ligne unique qui s’étend sur la largeur du menu.

### <a name="icons"></a>Icônes

-   **Fournissez des icônes d’élément de menu pour :**
    -   Éléments de menu les plus couramment utilisés.
    -   Éléments de menu dont l’icône est standard et bien connue.
    -   Les éléments de menu dont l’icône montre clairement ce que permet de faire la commande
-   **Si vous utilisez des icônes, ne vous inquiétez pas obligé de les fournir pour tous les éléments de menu.** Les icônes non explicites ne sont pas utiles : elles créent un encombrement visuel et empêchent les utilisateurs de se concentrer sur les éléments de menu importants.

![capture d’écran des éléments de menu avec et sans icônes ](images/cmd-menus-image13.png)

Dans cet exemple, le menu organiser n’a des icônes que pour les éléments de menu les plus couramment utilisés.

-   **Assurez-vous que les icônes de menu sont conformes aux règles d’icône de style Aero.**

Pour plus d’informations et d’exemples, consultez [icônes](vis-icons.md).

### <a name="access-keys"></a>Clés d'accès

-   **Affectez des clés d’accès à tous les éléments de menu.** Aucune exception.
-   **Dans la mesure du possible, affectez des clés d’accès pour les commandes couramment utilisées en fonction des affectations de touches d’accès standard.** Bien que les attributions de clé d’accès cohérentes ne soient pas toujours possibles, elles sont certainement préférées, en particulier pour les commandes fréquemment utilisées.
-   **Pour les éléments de menu dynamiques (tels que les fichiers récemment utilisés), assignez des touches d’accès numérique.**

![capture d’écran des éléments de menu avec des touches d’accès numérique ](images/cmd-menus-image14.png)

Dans cet exemple, le programme Paint dans Windows attribue des clés d’accès numériques aux fichiers récemment utilisés.

-   **Assigner des clés d’accès uniques au sein d’un niveau de menu.** Vous pouvez réutiliser des clés d’accès dans différents niveaux de menu.
-   **Rendez les clés d’accès faciles à trouver :**
    -   Pour les éléments de menu les plus fréquemment utilisés, choisissez caractères au début du premier ou du deuxième mot de l’étiquette, de préférence le premier caractère.
    -   Pour les éléments de menu moins fréquemment utilisés, choisissez des lettres qui sont une consonne distinctive ou une voyelle dans l’étiquette.
-   **Préférer les caractères dont la largeur est large,** par exemple w, m et les majuscules.
-   **Préférez une consonne distinctive ou une voyelle,** telle que « x » dans « Exit ».
-   **Évitez d’utiliser des caractères qui rendent le soulignement difficile à voir,** par exemple (de la plupart des problèmes aux moins problématiques) :
    -   Lettres d’une largeur d’un pixel, comme i et l.
    -   Lettres avec descendants, comme g, j, p, q et y.
    -   Lettres à côté d’une lettre avec un descendant.

Pour obtenir des instructions et des exemples supplémentaires, consultez [clavier](inter-keyboard.md).

### <a name="shortcut-keys"></a>Touches de raccourci

-   **Assignez des touches de raccourci aux éléments de menu les plus fréquemment utilisés.** Les éléments de menu rarement utilisés n’ont pas besoin de touches de raccourci, car les utilisateurs peuvent utiliser des clés d’accès à la place.
-   **Ne définissez pas une touche de raccourci comme seule façon d’effectuer une tâche.** Les utilisateurs doivent également être en mesure d’utiliser la souris ou le clavier avec la touche de tabulation, la flèche et les touches d’accès.
-   **Pour les touches de raccourci connues, utilisez les affectations standard.**
-   **N’affectez pas des significations différentes à des touches de raccourci connues.** Étant donné qu’elles sont mémorisées, les significations incohérentes des raccourcis bien connus sont frustrantes et sujettes aux erreurs. Consultez touches de raccourci clavier Windows pour connaître les touches de raccourci connues utilisées par les programmes Windows.
-   **N’essayez pas d’affecter des touches de raccourci de programme à l’ensemble du système.** Les touches de raccourci de votre programme ne seront effectives que si votre programme a le focus d’entrée.
-   **Documentez toutes les touches de raccourci.** Cela permet aux utilisateurs d’apprendre les affectations de touches de raccourci.
    -   **Exception :** N’affiche pas les affectations de touches de raccourci dans les menus contextuels. Les menus contextuels n’affichent pas les affectations de touches de raccourci car ils sont optimisés pour des raisons d’efficacité.
-   **Pour les affectations de clés non standard :**
    -   **Choisissez les touches de raccourci qui n’ont pas d’attributions standard.** Ne jamais réassigner les touches de raccourci standard.
    -   **Utilisez des affectations de clés non standard de manière cohérente dans votre programme.** N’affectez pas différentes significations dans différentes fenêtres.
    -   **Si possible, choisissez des affectations de touches mnémoniques, en** particulier pour les commandes fréquemment utilisées.
    -   **Utilisez les touches de fonction pour les commandes qui ont un effet à petite échelle,** telles que les commandes qui s’appliquent à l’objet sélectionné. Par exemple, F2 Renomme l’élément sélectionné.
    -   **Utilisez les combinaisons de touches Ctrl pour les commandes qui ont un effet à grande échelle,** telles que les commandes qui s’appliquent à un document entier. Par exemple, CTRL + S enregistre le document actif.
    -   **Utilisez les combinaisons de touches Maj pour les commandes qui étendent ou complètent les actions de la touche de raccourci standard.** Par exemple, la touche de raccourci Alt + Tab parcourt les fenêtres primaires ouvertes, tandis que les touches Alt + Maj + Tab sont placées dans l’ordre inverse. De même, la touche F1 affiche l’aide, tandis que MAJ + F1 affiche l’aide contextuelle.
    -   **N’utilisez pas les caractères suivants pour les touches de raccourci :** @ $ {} \[ \] \\  ~  \| ^ '  < >. Ces caractères nécessitent des combinaisons de touches différentes entre les langages ou sont spécifiques aux paramètres régionaux.
    -   **N’utilisez pas de combinaisons CTRL + ALT,** car Windows interprète cette combinaison dans certaines versions de langage comme une clé AltGR, qui génère des caractères alphanumériques.
-   **Si votre programme affecte de nombreuses touches de raccourci, offre la possibilité de personnaliser les attributions.** Cela permet aux utilisateurs de réassigner les touches de raccourci conflictuelles et de migrer à partir d’autres produits. La plupart des programmes n’attribuent pas suffisamment de touches de raccourci pour avoir besoin de cette fonctionnalité.

Pour obtenir des instructions supplémentaires et des affectations de touches de raccourci standard, consultez [clavier](inter-keyboard.md).

### <a name="standard-menus"></a>Menus standard

-   **Utilisez l’organisation du menu standard pour les programmes qui créent ou affichent des documents.** L’organisation de menu standard rend les éléments de menu communs prévisibles et plus faciles à trouver.
-   **Pour les autres types de programmes, utilisez l’organisation du menu standard uniquement lorsque cela est pertinent pour.** Envisagez d’organiser vos commandes et options en catégories naturelles plus utiles, en fonction de l’objectif de votre programme et de la façon dont les utilisateurs pensent à leurs tâches et objectifs.

**Barres de menus standard**

La structure de la barre de menus standard est la suivante. Cette liste affiche les étiquettes de catégorie de menu et d’élément, leur ordre avec les séparateurs, leurs touches de raccourci et d’accès, ainsi que leurs ellipses.

<dl> Fichier<dl> Nouveau Ctrl + N  
Ouvrir... Ctrl + O  
Fermez <separator>  
Enregistrer Ctrl + S  
Enregistrer sous... <separator>  
Envoyer à <separator>  
Imprimer... Ctrl + P  
Aperçu avant impression  
Mise en page <separator>  
1 <filename> 2 <filename> 3 <filename> ... <separator>  
Quitter ALT + F4 (raccourci généralement non fourni)
</dl> </dd> Edit<dl> Annuler Ctrl + Z  
Rétablir CTRL + Y <separator>  
Couper Ctrl + X  
Copier Ctrl + C  
Coller Ctrl + V <separator>  
Sélectionner tout CTRL + A <separator>  
Delete del (raccourci généralement non fourni) <separator>  
Rechercher... Ctrl + F  
Rechercher suivant F3 (commande généralement non indiquée)  
Remplacer... Ctrl + H  
Atteindre... CTRL + G
</dl> </dd> View<dl> Barres d'outils  
Barre d’État <separator>  
</dl> </dd> Zoom<dl> Zoom avant Ctrl + +  
Zoom arrière CTRL +- <separator>  
Plein écran F11  
Actualiser F5
</dl> </dd> <dd>Outils<dl> ... <separator>  
Options
</dl> </dd> Aide<dl> <program name> aide F1 <separator>  
Obtenir <program name>  
</dl> </dd> </dl>

**Boutons de menu de la barre d’outils standard**

Les boutons de menu de la barre d’outils standard sont les suivants. Cette liste affiche les étiquettes de catégorie de menu et d’élément, leur ordre avec les séparateurs, leurs touches de raccourci et leurs ellipses.

<dl> Outils<dl> Full screenF11 (réassignez la clé d’accès si Find est également utilisé.)  
Les barres d’outils (Notez que la commande de barre de menus est insérée ici). <separator>  
Imprimer...  
Rechercher... <separator>  
Zoom  
Taille du texte <separator>  
Options
</dl> </dd> Organize<dl> Nouveau folderCtrl + N <separator>  
CutCtrl + X  
CopyCtrl + C  
PasteCtrl + V <separator>  
Sélectionner allCtrl + A <separator>  
DeleteDel (raccourci généralement non fourni)  
Renommer <separator>  
Options
</dl> </dd> Page<dl> Nouveau windowCtrl + N <separator>  
Zoom  
Taille du texte
</dl> </dd> </dl>

**Menus contextuels standard**

Le contenu du menu contextuel standard est le suivant. Cette liste affiche les étiquettes d’élément de menu, leur ordre avec les séparateurs, leurs touches d’accès et leurs ellipses. Les menus contextuels n’affichent pas les touches de raccourci.

<dl> Ouvrir  
Exécuter  
Lire  
Modifier  
Imprimer... <separator>  
Couper  
Copier  
Insérer <separator>  
DELETE  
Renommer <separator>  
Verrouiller <object name> (coche)  
Propriétés
</dl>

### <a name="using-ellipses"></a>Utilisation de ellipses

Alors que les commandes de menu sont utilisées pour les actions immédiates, des informations supplémentaires peuvent être nécessaires pour exécuter l’action. **Indiquez une commande qui nécessite des informations supplémentaires (y compris une confirmation) en ajoutant des points de suspension à la fin de l’étiquette.**

![capture d’écran de la commande Imprimer et de la boîte de dialogue Imprimer ](images/cmd-menus-image15.png)

Dans cet exemple, la page... commande affiche une boîte de dialogue Imprimer pour recueillir plus d’informations.

**L’utilisation correcte des ellipses est importante pour indiquer que les utilisateurs peuvent effectuer des choix supplémentaires avant d’effectuer l’action, ou même annuler complètement l’action.** Le signal visuel fourni par des points de suspension permet aux utilisateurs d’explorer vos logiciels sans crainte.

**Cela ne signifie pas que vous devez utiliser des points de suspension chaque fois qu’une action affiche une autre fenêtre** uniquement lorsque des informations supplémentaires sont requises pour effectuer l’action. Par exemple, les commandes sur, avancé, aide, options, propriétés et paramètres doivent afficher une autre fenêtre lorsque vous cliquez dessus, mais ne nécessitent pas d’informations supplémentaires de la part de l’utilisateur. Par conséquent, ils n’ont pas besoin de ellipses.

**En cas d’ambiguïté (par exemple, l’étiquette de commande n’a pas de verbe), choisissez en fonction de l’action utilisateur la plus probable.** Si la simple consultation de la fenêtre est une action courante, n’utilisez pas de points de suspension.

**Correct :**

Couleurs supplémentaires...

Informations sur la version

Dans le premier exemple, les utilisateurs vont probablement choisir une couleur, de sorte que l’utilisation d’une ellipse est correcte. Dans le deuxième exemple, les utilisateurs vont probablement afficher les informations de version, ce qui rend les ellipses inutiles.

> [!Note]  
> Lorsque vous déterminez si une commande de menu a besoin de points de suspension, n’utilisez pas le besoin d' [élever les privilèges](winenv-uac.md) en tant que facteur.

 

L’élévation n’est pas nécessaire pour exécuter une commande (au lieu de cela, il s’agit d’une autorisation) et le besoin d’élévation est indiqué par la protection de la sécurité.

## <a name="labels"></a>Étiquettes

-   **Utilisez les majuscules comme pour les phrases.**
    -   **Exception :** Pour les applications héritées, vous pouvez utiliser la mise en majuscules de style titre si nécessaire pour éviter de mélanger les styles de mise en majuscules.

### <a name="menu-category-names"></a>Noms de catégorie de menu

-   **Utilisez des noms de catégorie de menu qui sont des verbes ou des noms à mot unique.** Une étiquette à plusieurs mots peut être confondue pour les étiquettes de 2 1 mots.
-   **Préférer les noms de menu basés sur un verbe.** Toutefois, omettez le verbe s’il s’agit de créer, afficher, afficher ou gérer. Par exemple, les catégories de menu suivantes n’ont pas de verbes :
    -   Table de charge de travail
    -   Outils
    -   Fenêtre
-   Pour les noms de catégorie non standard, **Utilisez un mot unique et spécifique qui décrit clairement et avec précision le contenu du menu.** Alors que les noms n’ont pas besoin d’être tellement généraux qu’ils décrivent tous les éléments du menu, ils doivent être suffisamment prévisibles pour que les utilisateurs ne soient pas surpris par ce qu’ils recherchent dans le menu.

### <a name="menu-item-names"></a>Noms d’éléments de menu

-   **Utilisez des noms d’élément de menu qui commencent par un verbe, un substantif ou une expression nominale.**
-   **Préférer les noms de menu basés sur un verbe.** Toutefois, omettez le verbe dans les cas suivants :
    -   **Le verbe est créer, afficher, afficher ou gérer.** Par exemple, les commandes suivantes n’ont pas de verbes :
        -   À propos de
        -   Avancé
        -   Plein écran
        -   Nouveau
        -   Options
        -   Propriétés
    -   **Le verbe est le même que le nom de catégorie de menu pour éviter la répétition.** Par exemple, dans la catégorie de menu Insérer, utilisez du texte, une table et une image au lieu d’insérer du texte, d’insérer un tableau et d’insérer une image.
-   **Utilisez des verbes spécifiques.** Évitez les verbes génériques sans aide, tels que change et Manage.
-   **Utilisez des noms singulières pour les commandes qui s’appliquent à un seul objet**, sinon utilisez des noms au pluriel.
-   **Utilisez les modificateurs nécessaires pour faire la distinction entre les commandes similaires.** Exemples : insérer une ligne au-dessus, insérer une ligne en dessous.
-   **Pour les paires de commandes complémentaires, choisissez des noms clairement complémentaires.** Exemples : Add, Remove ; Afficher, masquer ; Insérer, supprimer.
-   **Choisissez des noms d’élément de menu en fonction des objectifs et des tâches de l’utilisateur, et non de la technologie.**

**Correct :**

![capture d’écran du menu de l’extraction avec l’élément de menu Format ](images/cmd-menus-image16.png)

**Incorrect :**

![capture d’écran du menu RIP avec l’élément de menu codec ](images/cmd-menus-image17.png)

Dans l’exemple incorrect, l’élément de menu est basé sur sa technologie.

-   Utilisez les noms d’élément de menu suivants à des fins définies :
    -   **Options** Pour afficher les options du programme.
    -   **Personnaliser** Pour afficher les options de programme spécifiquement liées à la configuration de l’interface utilisateur mécanique.
    -   **Personnaliser** Pour afficher un résumé des paramètres de [personnalisation](glossary.md) couramment utilisés.
    -   **Préférences** N’utilisez pas. Utilisez à la place des options.
    -   **Propriétés** de Pour afficher la fenêtre des propriétés d’un objet.
    -   **Paramètres** N’utilisez pas comme étiquette de menu. Utilisez à la place des options.

### <a name="submenu-names"></a>Noms de sous-menus

-   **Les éléments de menu qui affichent des sous-menus n’ont jamais de points de suspension sur leur étiquette.** La flèche de sous-menu indique qu’une autre sélection est requise.

**Incorrect :**

![capture d’écran d’un nouvel élément de menu avec des points de suspension ](images/cmd-menus-image18.png)

Dans cet exemple, le nouvel élément de menu a des points de suspension.

## <a name="documentation"></a>Documentation

Lorsque vous faites référence à des menus :

-   Dans les commandes qui affichent ou masquent des menus, reportez-vous aux barres de menus. Ne vous y référez pas en tant que menus classiques.
-   Reportez-vous aux menus par leurs étiquettes. Utilisez le texte exact de l’étiquette, y compris sa mise en majuscules, mais n’incluez pas le trait de soulignement ou les points de suspension.
-   Pour faire référence à des catégories de menu, utilisez «» dans le <category name> menu. Si l’emplacement d’un élément de menu est clair dans le contexte, vous n’avez pas besoin de mentionner la catégorie de menu.
-   Pour décrire l’interaction de l’utilisateur entre les éléments de menu, cliquez sur, sans utiliser le menu ou la commande Word. N’utilisez pas Choose, SELECT ou Pick. Ne faites pas référence à un élément de menu en tant qu’élément de menu, sauf dans la documentation technique.
-   Pour décrire la suppression d’une coche d’une option de menu, utilisez la case à cocher cliquez pour supprimer la coche. N’utilisez pas Clear.
-   Reportez-vous aux menus contextuels tels que les menus contextuels.
-   N’utilisez pas la mise en cascade, la liste déroulante ou la fenêtre contextuelle pour décrire les menus, sauf dans la documentation de programmation.
-   Reportez-vous aux éléments de menu non disponibles, non disponibles, grisés, désactivés ou grisés. Utilisez Disabled dans la documentation de programmation.
-   Dans la mesure du possible, mettez en forme les étiquettes à l’aide du texte gras. Dans le cas contraire, placez les étiquettes entre guillemets uniquement si nécessaire pour éviter toute confusion.

Exemples :

-   Dans le menu **fichier** , cliquez sur **Imprimer** pour imprimer le document.
-   Dans le menu **affichage** , pointez sur **barres d’outils**, puis cliquez sur **mise en forme**.

 

