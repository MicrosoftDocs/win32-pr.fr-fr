---
title: Zones de liste
description: Avec une zone de liste, les utilisateurs peuvent sélectionner un ensemble de valeurs présentées dans une liste qui est toujours visible.
ms.assetid: 620e9ff9-b367-446b-9e97-9c9d6d14f4bb
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 0f1fe5a0c804e1c0b5b2636b4c7747caa9fb1049
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127234959"
---
# <a name="list-boxes"></a>Zones de liste

> [!NOTE]
> ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Avec une zone de liste, les utilisateurs peuvent sélectionner un ensemble de valeurs présentées dans une liste qui est toujours visible. Avec une zone de liste à sélection unique, les utilisateurs sélectionnent un élément dans une liste de valeurs s’excluant mutuellement. Avec une zone de liste à sélection multiple, les utilisateurs sélectionnent zéro, un ou plusieurs éléments dans une liste de valeurs.

![capture d’écran de la zone de liste à sélection unique ](images/ctrl-list-boxes-image1.png)

Zone de liste à sélection unique classique.

> [!Note]  
> Les instructions relatives à la [disposition](vis-layout.md) et aux [vues de liste](ctrl-list-views.md) sont présentées dans des articles distincts.

 

## <a name="is-this-the-right-control"></a>Est-ce le contrôle approprié ?

Pour vous décider, posez-vous les questions suivantes :

-   **La liste présente-t-elle des données plutôt que des options de programme ?** Dans les deux cas, une zone de liste est un choix approprié, quel que soit le nombre d’éléments. En revanche, les cases d' [option](ctrl-radio-buttons.md) ou les [cases à cocher](ctrl-check-boxes.md) ne conviennent que pour un petit nombre d’options de programme.
-   **Les utilisateurs doivent-ils modifier les affichages, les regrouper, les trier par colonnes ou modifier la largeur et l’ordre des colonnes ?** Dans ce cas, utilisez plutôt un [mode liste](ctrl-list-views.md) .
-   **Le contrôle doit-il être une source de glissement ou une cible de déplacement ?** Dans ce cas, utilisez plutôt un mode liste.
-   **Les éléments de la liste doivent-ils être copiés ou collés à partir du presse-papiers ?** Dans ce cas, utilisez plutôt un mode liste.

**Listes à sélection unique**

-   **Le contrôle est-il utilisé pour choisir une option dans une liste de valeurs s’excluant mutuellement ?** Si ce n’est pas le cas, utilisez un autre contrôle. Pour choisir plusieurs options, utilisez une liste à sélection multiple standard, une liste de cases à cocher, un générateur de listes ou une liste ajouter/supprimer à la place.
-   **Existe-t-il une option par défaut recommandée pour la plupart des utilisateurs dans la plupart des cas ?** L’option sélectionnée est-elle beaucoup plus importante que l’affichage des alternatives ? Si c’est le cas, envisagez d’utiliser une [liste déroulante](/windows/desktop/uxguide/ctrl-drop) si vous ne souhaitez pas encourager les utilisateurs à apporter des modifications en masquant les alternatives.

![capture d’écran de la qualité la plus élevée comme bouton par défaut ](images/ctrl-list-boxes-image2.png)

Dans cet exemple, la qualité de couleur la plus élevée est le meilleur choix pour la plupart des utilisateurs. par conséquent, une liste déroulante est un bon choix pour minimiser les alternatives.

-   **La liste requiert-elle une interaction constante ?** Dans ce cas, utilisez une liste à sélection unique pour simplifier l’interaction.

![capture d’écran de la liste des options telles que le texte brut ](images/ctrl-list-boxes-image3.png)

Dans cet exemple, les utilisateurs modifient en permanence l’élément sélectionné dans la liste éléments affichés pour définir les couleurs de premier plan et d’arrière-plan. Dans ce cas, l’utilisation d’une liste déroulante serait très fastidieuse.

-   **Le paramètre ressemble-t-il à une quantité relative ? Les utilisateurs pourraient-ils tirer parti des commentaires instantanés** sur l’effet des modifications de paramètres ? Si c’est le cas, envisagez plutôt d’utiliser un [curseur](ctrl-sliders.md) .
-   **Existe-t-il une relation hiérarchique importante entre les éléments de la liste ?** Dans ce cas, utilisez plutôt un contrôle [Tree View](ctrl-tree-views.md) .
-   **L’espace à l’écran est-il d’un niveau Premium ?** Dans ce cas, utilisez une liste déroulante à la place, car l’espace utilisé par l’écran est fixe et indépendant du nombre d’éléments de liste.

**Listes de sélection multiple standard et listes de cases à cocher**

-   **La sélection multiple est-elle essentielle pour la tâche ou couramment utilisée ?** Dans ce cas, utilisez une liste de cases à cocher pour rendre la sélection multiple évidente, surtout si vos utilisateurs cibles ne sont pas avancés. De nombreux utilisateurs ne se rendent pas compte qu’une liste de sélection multiple standard prend en charge la sélection multiple. Utilisez une liste à sélection multiple standard si les cases à cocher attirent trop l’attention sur une sélection multiple ou entraînent une trop grande encombrement de l’écran.
-   **La stabilité de la sélection multiple est-elle importante ?** Dans ce cas, utilisez une liste de cases à cocher, un générateur de listes ou une liste ajouter/supprimer, car le fait de cliquer sur modifie un seul élément à la fois. Avec une liste de sélection multiple standard, il est très facile de supprimer toutes les sélections, même par accident.
-   **Le contrôle est-il utilisé pour choisir zéro élément ou plus dans une liste de valeurs ?** Si ce n’est pas le cas, utilisez un autre contrôle. Pour choisir un élément, utilisez une liste à sélection unique à la place.

**Listes préliminaires**

-   **Les options sont-elles plus faciles à sélectionner avec des images qu’avec du texte seul ?** Dans ce cas, utilisez une liste d’aperçu.

**Répertorier les générateurs et ajouter/supprimer des listes**

-   **Le contrôle est-il utilisé pour choisir zéro élément ou plus dans une liste de valeurs ?** Si ce n’est pas le cas, utilisez un autre contrôle. Pour choisir un élément, utilisez une liste à sélection unique à la place.
-   **L’ordre des éléments sélectionnés est-il important ?** Si c’est le cas, les modèles List Builder et Add/Remove List prennent en charge l’ordre, contrairement aux autres modèles à sélection multiple.
-   **Est-il important pour les utilisateurs de voir un résumé de tous les éléments sélectionnés ?** Si c’est le cas, les modèles List Builder et Add/Remove List affichent uniquement les éléments sélectionnés, contrairement aux autres modèles à sélection multiple.
-   **Les choix possibles sont-ils sans contrainte ?** Dans ce cas, utilisez une liste ajouter/supprimer afin que les utilisateurs puissent choisir des valeurs qui ne sont pas actuellement dans la liste.
-   **L’ajout d’une valeur à la liste nécessite-t-elle une boîte de dialogue spécialisée pour le choix des objets ?** Dans ce cas, utilisez une liste ajouter/supprimer et affichez la boîte de dialogue lorsque les utilisateurs cliquent sur Ajouter.
-   **L’espace à l’écran est-il d’un niveau Premium ?** Dans ce cas, utilisez plutôt une liste ajouter/supprimer, car elle utilise moins d’espace à l’écran en n’apparaissant pas toujours dans le jeu d’options.

Pour les zones de liste, **le nombre d’éléments de la liste n’est pas un facteur de choix du contrôle** , car ils sont mis à l’échelle de plusieurs milliers d’éléments jusqu’à un pour les listes à sélection unique (et aucune pour les listes à sélection multiple). Étant donné que les zones de liste peuvent être utilisées pour les données, le nombre d’éléments peut ne pas être connu à l’avance.

**Remarque :** Parfois, un contrôle qui ressemble à une zone de liste est implémenté à l’aide d’une vue liste et vice versa. Dans ce cas, appliquez les instructions en fonction de l’utilisation, et non de l’implémentation.

## <a name="usage-patterns"></a>Modèles d’usage

Les zones de liste ont plusieurs modèles d’utilisation :




| Étiquette | Valeur |
|--------|-------|
| <strong>Listes à sélection unique</strong> Autoriser les utilisateurs à sélectionner un élément à la fois. <br /> | <img src="images/ctrl-list-boxes-image4.png" alt="Screen shot of list box with one item selected " /><br /> Dans cet exemple, les utilisateurs ne peuvent sélectionner qu’un seul élément d’affichage.<br /> | 
| <strong>Listes de sélection multiple standard</strong> Autorisez les utilisateurs à sélectionner n’importe quel nombre d’éléments, y compris aucun.<br /> | Les listes de sélection multiple standard ont exactement la même apparence que les listes à sélection unique, de sorte qu’il n’y a pas d’indication visuelle qu’une zone de liste prend en charge la sélection multiple. Étant donné que les utilisateurs doivent découvrir cette possibilité, ce modèle de liste est idéal pour les tâches où la sélection multiple n’est pas essentielle et est rarement utilisée. <br /> Il existe deux modes de sélection multiple différents : <a href="glossary.md">multiple</a> et <a href="glossary.md">étendu</a>. Le <strong>mode de sélection étendue</strong> est de loin le plus courant, où la sélection peut être étendue en faisant glisser ou en appuyant sur Maj + clic et Ctrl + clic pour sélectionner les groupes de valeurs contiguës et non adjacentes, respectivement. Dans le <strong>mode de sélection multiple</strong>, le fait de cliquer sur un élément fait basculer son état de sélection indépendamment des touches Maj et Ctrl. Étant donné ce comportement inhabituel, le mode de sélection multiple est déconseillé et vous devez utiliser des listes de cases à cocher à la place.<br /><img src="images/ctrl-list-boxes-image5.png" alt="Screen shot of list box with several items selected " /><br /> Dans cet exemple, les utilisateurs peuvent sélectionner n’importe quel nombre d’éléments à l’aide du mode de sélection multiple.<br /> | 
| <strong>Listes de cases à cocher</strong> Comme les zones de liste à sélection multiple standard, les listes déroulantes permettent aux utilisateurs de sélectionner n’importe quel nombre d’éléments, y compris aucun.<br /> | Contrairement aux listes à sélection multiple standard, les cases à cocher indiquent clairement que plusieurs sélections sont possibles. Utilisez ce modèle de liste pour les tâches où la sélection multiple est essentielle ou couramment utilisée. <br /><img src="images/ctrl-list-boxes-image6.png" alt="Screen shot of Toolbars check-box list " /><br /> Dans cet exemple, les utilisateurs sélectionnent généralement plus d’un élément afin qu’une liste de cases à cocher soit utilisée.<br /> Étant donné cette indication claire de la sélection multiple, vous pouvez supposer que les listes de cases à cocher sont préférables aux listes à sélection multiple standard. En pratique, peu de tâches nécessitent une sélection multiple ou l’utilisent de manière intensive. l’utilisation d’une liste de cases à cocher dans de tels cas attire trop bien la sélection. Par conséquent, <strong>les listes de sélection multiple standard sont beaucoup plus courantes.</strong><br /> | 
| <strong>Listes préliminaires</strong> Peut être une sélection unique ou multiple, mais elles affichent un aperçu de l’effet de la sélection plutôt que du texte uniquement.<br /> | <img src="images/ctrl-list-boxes-image7.png" alt="Screen shot of Window Color options preview " /><br /> Dans cet exemple, un aperçu de chaque option montre clairement l’effet du choix, ce qui est plus efficace que l’utilisation de texte seul.<br /> | 
| <strong>Répertorier les générateurs</strong> Autorisez les utilisateurs à créer une liste de choix en ajoutant un élément à la fois et en définissant éventuellement l’ordre de la liste.<br /> | Un générateur de listes se compose de deux listes à sélection unique : la liste à gauche est un ensemble fixe d’options et la liste à droite est la liste en cours de génération. Deux boutons de commande sont disponibles entre les listes : <br /><ul><li>Bouton <strong>Ajouter</strong> qui déplace l’option actuellement sélectionnée vers la liste en cours de génération, insérée avant l’élément sélectionné. (Le fait de double-cliquer sur un élément d’option a le même effet.)</li><li>Bouton <strong>supprimer</strong> qui supprime l’élément sélectionné de la liste compilée et le retourne à la liste d’options. (Le fait de double-cliquer sur un élément dans la liste générée a le même effet.) La liste générée peut éventuellement avoir des commandes <strong>monter</strong> et <strong>descendre pour</strong> trier les éléments de la liste.</li></ul><img src="images/ctrl-list-boxes-image8.png" alt="Screen shot of Toolbar buttons list builder " /><br /> Dans cet exemple, un générateur de listes est utilisé pour créer une barre d’outils en sélectionnant des éléments dans un ensemble d’options disponibles et en définissant leur ordre.<br /> | 
| <strong>Ajouter/supprimer des listes</strong> Autorisez les utilisateurs à créer une liste de choix en ajoutant un ou plusieurs éléments à la fois, et en définissant éventuellement l’ordre de la liste (comme les générateurs de listes).<br /> | Contrairement à un générateur de listes, si vous cliquez sur <strong>Ajouter</strong> , une boîte de dialogue s’affiche et vous permet de sélectionner les éléments à ajouter à la liste. L’utilisation d’une boîte de dialogue distincte permet d’obtenir une flexibilité significative dans le choix des éléments. vous pouvez utiliser un sélecteur d’objet spécialisé ou même une boîte de dialogue commune. En comparaison avec le générateur de listes, cette variation est plus compacte, mais nécessite un peu plus de travail pour ajouter des éléments. <br /><img src="images/ctrl-list-boxes-image9.png" alt="Screen shot of Menu contents list " /><br /> Dans cet exemple, les utilisateurs peuvent ajouter ou supprimer des outils dans un menu, ainsi que définir l’ordre.<br /> Tandis que les modèles List Builder et Add/Remove list sont beaucoup plus lourds que les autres listes à sélection multiple, ils offrent deux avantages uniques :<br /><ul><li>Les utilisateurs contrôlent l’ordre de la liste, à la fois lors de la génération de la liste et après.</li><li>Les utilisateurs peuvent consulter un résumé des éléments sélectionnés, ce qui peut être un avantage significatif si le nombre de choix est important.</li></ul>Leurs inconvénients sont qu’ils nécessitent beaucoup plus d’espace à l’écran et peuvent être difficiles à utiliser lors de la création d’une grande liste d’éléments à partir de zéro. Par conséquent, il est préférable de créer des listes courtes ou de modifier des listes qui existent déjà.<br /> | 




 

## <a name="guidelines"></a>Consignes

### <a name="presentation"></a>Présentation

-   **Triez les éléments de liste dans un ordre logique,** par exemple en regroupant les options associées, en plaçant d’abord les éléments les plus fréquemment utilisés ou en utilisant l’ordre alphabétique. Triez les noms dans l’ordre alphabétique, les nombres dans l’ordre numérique et les dates dans l’ordre chronologique. Les listes avec 12 éléments ou plus doivent être triées par ordre alphabétique pour faciliter la recherche d’éléments.

**Correct :** ![ capture d’écran de l’alignement (gauche, Centre, droite) ](images/ctrl-list-boxes-image10.png)

Dans cet exemple, les éléments de la zone de liste sont triés en fonction de leur relation spatiale.

**Incorrect :** ![ capture d’écran de la liste désorganisée ](images/ctrl-list-boxes-image11.png)

Dans cet exemple, un grand nombre d’éléments de liste doivent être triés par ordre alphabétique.

**Correct :** ![ capture d’écran de la liste alphabétique ](images/ctrl-list-boxes-image12.png)

Dans cet exemple, les éléments de la liste sont plus faciles à trouver, car ils sont triés par ordre alphabétique. toutefois, l’élément « tous les Windows produits » se trouve au début de la liste, quel que soit son ordre de tri.

-   **Placez les options qui représentent tout ou aucune au début de la liste**, quel que soit l’ordre de tri des éléments restants.
-   **Placez les méta-options entre parenthèses.**

![capture d’écran de la liste déroulante avec aucun sélectionné ](images/ctrl-list-boxes-image13.png)

Dans cet exemple, « (None) » est une méta-option, car il ne s’agit pas d’une valeur valide pour le choix. elle indique plutôt que l’option elle-même n’est pas utilisée.

-   **Les éléments de liste vides n’utilisent pas les options méta à la place.** Les utilisateurs ne savent pas comment interpréter les éléments vides, alors que la signification des méta-options est explicite.

**Incorrect :** ![ capture d’écran de la liste déroulante avec l’option vide sélectionnée ](images/ctrl-list-boxes-image14.png)

Dans cet exemple, la signification de l’élément vide n’est pas claire.

**Correct :** ![ capture d’écran de la liste déroulante avec aucun sélectionné ](images/ctrl-list-boxes-image13.png)

Dans cet exemple, la méta-option « (aucune) » est utilisée à la place.

### <a name="interaction"></a>Interaction

-   **Envisagez de fournir un comportement de double-clic.** Un double-clic doit avoir le même effet que la sélection d’un élément et l’exécution de sa commande par défaut.
-   **Effectuez un double-clic sur le comportement redondant.** Il doit toujours y avoir un bouton de commande ou une commande de menu contextuel qui a le même effet.
-   **Si les utilisateurs ne peuvent rien faire avec les éléments sélectionnés, n’autorisez pas la sélection.**

**Correct :** ![ capture d’écran de la liste des modifications de l’Assistant terminée ](images/ctrl-list-boxes-image15.png)

Cette zone de liste affiche une liste en lecture seule des modifications. la sélection n’est pas nécessaire.

-   **Lorsque vous désactivez une zone de liste, désactivez également les étiquettes et les boutons de commande associés.**
-   **N’utilisez pas la modification de l’élément sélectionné dans une zone de liste pour :**
    -   Exécuter des commandes.
    -   Affichez d’autres fenêtres, telles qu’une boîte de dialogue pour recueillir davantage d’entrées.
    -   Afficher dynamiquement d’autres contrôles en rapport avec le contrôle sélectionné (les lecteurs d’écran ne peuvent pas détecter de tels événements). **Exception :** Vous pouvez modifier dynamiquement le texte statique utilisé pour décrire l’élément sélectionné.

**Acceptable :** ![ capture d’écran des détails de l’élément de liste sélectionné ](images/ctrl-list-boxes-image16.png)

Dans cet exemple, la modification de l’élément sélectionné modifie la description.

-   **Évitez le défilement horizontal.** Les listes multicolonnes reposent sur le défilement horizontal, ce qui est généralement plus difficile à utiliser que le défilement vertical. Les listes multicolonnes qui nécessitent un défilement horizontal peuvent être utilisées lorsque vous avez un grand nombre d’éléments triés par ordre alphabétique et un espace d’écran suffisant pour un contrôle étendu.

**Acceptable :** ![ capture d’écran de la liste des dossiers dans l’Explorateur Windows ](images/ctrl-list-boxes-image17.png)

Dans cet exemple, plusieurs colonnes nécessitant un défilement horizontal sont utilisées, car il existe de nombreux éléments et un espace d’écran disponible suffisant pour un contrôle large.

### <a name="multiple-selection-lists"></a>Listes à sélection multiple

-   **Envisagez d’afficher le nombre d’éléments sélectionnés sous la liste, en** particulier si les utilisateurs sont susceptibles de sélectionner plusieurs éléments. Ces informations fournissent non seulement des commentaires utiles, mais indiquent clairement que la zone de liste prend en charge la sélection multiple.

![capture d’écran de la zone de liste avec quatre éléments sélectionnés ](images/ctrl-list-boxes-image5.png)

Dans cet exemple, le nombre d’éléments sélectionnés est affiché sous la liste.

-   Vous pouvez fournir d’autres mesures de sélection qui peuvent être plus explicites, telles que les ressources requises pour les sélections.

![capture d’écran de la liste de cases à cocher des fonctionnalités Windows ](images/ctrl-list-boxes-image18.png)

Dans cet exemple, l’espace disque requis pour installer les composants est plus significatif que le nombre d’éléments sélectionnés.

-   S’il peut y avoir un grand nombre d’éléments de liste et si vous en sélectionnez ou en désactivant tous, vous pouvez ajouter des boutons de commande Sélectionner tout et effacer tout.
-   Pour les listes à sélection multiple standard, n’utilisez pas le mode de sélection multiple car ce mode de sélection est déconseillé. Pour un comportement équivalent, utilisez plutôt une liste de cases à cocher.

### <a name="default-values"></a>Valeurs par défaut

-   **Sélectionnez le niveau de sécurité le plus sûr (pour éviter la perte de données ou l’accès au système) et l’option la plus sécurisée par défaut.** Si la sécurité et la sécurité ne sont pas des facteurs, sélectionnez l’option la plus probable ou la plus pratique.

**Exception :** Ne sélectionnez aucun élément si le contrôle représente une propriété dans un [État mixte](glossary.md), ce qui se produit lors de l’affichage d’une propriété pour plusieurs objets qui n’ont pas le même paramètre.

## <a name="recommended-sizing-and-spacing"></a>Dimensionnement et espacement recommandés

![capture d’écran du dimensionnement et de l’espacement de la zone de liste ](images/ctrl-list-boxes-image19.png)

Dimensionnement et espacement recommandés pour les zones de liste.

-   **Choisissez une largeur de zone de liste appropriée pour les données valides les plus longues.** Les zones de liste standard ne peuvent pas faire l’objet d’un défilement horizontalement, de sorte que les utilisateurs ne voient que ce qui est visible dans le contrôle.
-   **Incluez 30 pour cent supplémentaires** (jusqu’à 200 pour cent pour du texte plus petit) pour tout texte (mais pas les nombres) qui sera localisé.
-   **Choisissez une hauteur de zone de liste qui affiche un nombre entier d’éléments.** Évitez de tronquer les éléments verticalement.
-   **Choisissez une hauteur de zone de liste qui élimine le défilement vertical inutile.** Les zones de liste doivent afficher entre 3 et 20 éléments sans avoir besoin de faire défiler. Envisagez de rendre une zone de liste légèrement plus longue si vous supprimez la barre de défilement verticale. Les listes contenant potentiellement de nombreux éléments doivent afficher au moins cinq éléments pour faciliter le défilement en affichant plus d’éléments à la fois et en rendant la barre de défilement plus facile à positionner.
-   **Si les utilisateurs bénéficient de la taille de la zone de liste, rendez la zone de liste et sa fenêtre parente redimensionnable.** Cela permet aux utilisateurs d’ajuster la taille de la zone de liste en fonction des besoins. Toutefois, les zones de liste redimensionnables doivent afficher au moins trois éléments.

## <a name="labels"></a>Étiquettes

**Étiquettes de contrôle**

-   Toutes les zones de liste requièrent des étiquettes. Écrivez l’étiquette en tant que mot ou expression, pas en tant que phrase ; Utilisez un signe deux-points à la fin de l’étiquette.

**Exception :** Omettez l’étiquette s’il s’agit simplement d’une refonte de l' [instruction principale](glossary.md)d’une boîte de dialogue. Dans ce cas, l’instruction principale prend le signe deux-points (sauf s’il s’agit d’une question) et la clé d’accès.

**Acceptable :** ![ capture d’écran de la liste avec étiquette redondante ](images/ctrl-list-boxes-image20.png)

Dans cet exemple, l’étiquette de la zone de liste REstate simplement l’instruction principale.

**Mieux :** ![ capture d’écran de la liste des sans étiquette redondante ](images/ctrl-list-boxes-image21.png)

Dans cet exemple, l’étiquette redondante est supprimée, de sorte que l’instruction principale prend le signe deux-points et la clé d’accès.

-   Si une zone de liste est subordonnée à une case d’option ou à une case à cocher et qu’elle est introduite par l’étiquette de ce contrôle se terminant par un signe deux-points, ne placez pas d’étiquette supplémentaire sur le contrôle de zone de liste.

![capture d’écran du bouton et de la liste à l’aide de la même étiquette ](images/ctrl-list-boxes-image22.png)

Dans cet exemple, la zone de liste est subordonnée à une case d’option et partage son étiquette.

-   Attribuez une [clé d’accès](glossary.md)unique. Pour obtenir des instructions, consultez [clavier](inter-keyboard.md).
-   Utilisez la mise [en majuscules de style phrase](glossary.md).
-   Placez l’étiquette à gauche ou au-dessus du contrôle, puis alignez l’étiquette sur le bord gauche du contrôle.
    -   Si l’étiquette est située à gauche, aligne verticalement le texte de l’étiquette sur la première ligne de texte dans le contrôle.

**Correct :** ![ capture d’écran de la liste avec étiquette alignée à gauche au-dessus ](images/ctrl-list-boxes-image23.png)![ de la capture d’écran de la liste avec étiquette alignée sur le texte à gauche ](images/ctrl-list-boxes-image24.png)

Dans ces exemples, l’étiquette en haut est alignée sur le bord gauche de la zone de liste et l’étiquette à gauche s’aligne sur le texte de la zone de liste.

**Incorrect :** ![ capture d’écran de la liste avec étiquette alignée sur le texte au-dessus ](images/ctrl-list-boxes-image25.png)![ de la capture d’écran de la liste avec l’étiquette alignée en haut à gauche ](images/ctrl-list-boxes-image26.png)

Dans ces exemples incorrects, l’étiquette en haut est alignée sur le texte de la zone de liste et l’étiquette à gauche s’aligne sur le haut de la zone de liste.

-   Pour les zones de liste à sélection multiple, utilisez une étiquette qui indique clairement que plusieurs sélections sont possibles. Les étiquettes de liste de cases à cocher peuvent être moins explicites.

**Correct :** ![ capture d’écran de la liste avec sélectionner une ou plusieurs étiquettes ](images/ctrl-list-boxes-image27.png)

Dans cet exemple, l’étiquette indique clairement que plusieurs sélections sont possibles.

**Incorrect :** ![ capture d’écran de la zone de liste avec l’étiquette des modules complémentaires ](images/ctrl-list-boxes-image28.png)

Dans cet exemple, l’étiquette ne fournit aucune information évidente sur la sélection multiple.

**Mieux :** ![ capture d’écran de la liste de cases d’option avec l’étiquette des modules complémentaires ](images/ctrl-list-boxes-image29.png)

Dans cet exemple, les cases à cocher indiquent clairement que plusieurs sélections sont possibles, de sorte que l’étiquette n’a pas besoin d’être explicite.

-   Vous pouvez spécifier des unités (secondes, connexions, etc.) entre parenthèses après l’étiquette.

**Texte de l’option**

-   Attribuez un nom unique à chaque option.
-   Utilisez la mise [en majuscules de style phrase](glossary.md), sauf si un élément est un nom propre.
-   Écrivez l’étiquette sous la forme d’un mot ou d’une expression, et non pas en tant que phrase, et n’utilisez pas de ponctuation finale.
-   Utilisez une formulation parallèle et essayez de conserver la même longueur pour toutes les options.

**Texte d’instructions et de texte supplémentaire**

-   Si vous devez ajouter du texte d’instructions sur une zone de liste, ajoutez-le au-dessus de l’étiquette. Utilisez des phrases complètes avec la ponctuation finale.
-   Utilisez la mise [en majuscules de style phrase](glossary.md).
-   Les informations supplémentaires qui sont utiles, mais pas nécessaires, doivent être courtes. Placez ce texte entre parenthèses entre l’étiquette et le signe deux-points, ou sans parenthèses sous le contrôle.

![capture d’écran de la liste de cases d’option et du texte descriptif ](images/ctrl-list-boxes-image30.png)

Dans cet exemple, le texte supplémentaire est placé sous la liste.

## <a name="documentation"></a>Documentation

Lorsque vous faites référence à des zones de liste :

-   Utilisez le texte exact de l’étiquette, y compris sa mise en majuscules, mais n’incluez pas le trait de soulignement ou le signe deux-points. Incluez la liste de mots. Ne faites pas référence à une zone de liste sous la forme d’une zone de liste ou d’un champ.
-   Pour les éléments de liste, utilisez le texte exact de l’élément, y compris sa mise en majuscules.
-   Dans programmation et autres documents techniques, reportez-vous aux zones de liste en tant que zones de liste. Partout ailleurs, utilisez List.
-   Pour décrire l’interaction de l’utilisateur, utilisez Select.
-   Dans la mesure du possible, mettez en forme les éléments d’étiquette et de liste en texte gras. Sinon, placez l’étiquette et les éléments entre guillemets uniquement si nécessaire pour éviter toute confusion.

Exemple : dans la liste **atteindre** , sélectionnez **signet**.

