---
title: Listes déroulantes et zones de liste déroulante
description: Avec une liste déroulante ou une zone de liste déroulante, les utilisateurs font un choix parmi une liste de valeurs s’excluant mutuellement.
ms.assetid: dbe88cf1-7946-4343-bc16-ce12be7ce205
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: ce9cbcac3495022edbb398bcbd78b35ac5265150
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524573"
---
# <a name="drop-down-lists--combo-boxes"></a>Listes déroulantes & zones de liste déroulante

> [!NOTE]
> Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Avec une liste déroulante ou une zone de liste déroulante, les utilisateurs font un choix parmi une liste de valeurs s’excluant mutuellement. Les utilisateurs peuvent choisir une seule et unique option. Avec une liste déroulante standard, les utilisateurs sont limités aux choix de la liste, mais avec une zone de liste modifiable, ils peuvent entrer un choix qui ne figure pas dans la liste.

![capture d’écran de la zone de liste déroulante heure de rappel ](images/ctrl-drop-image1.png)

Zone de liste déroulante classique.

Les termes suivants sont importants à connaître lors de la lecture de cet article :

-   Une zone de liste standard est une zone contenant une liste de plusieurs éléments, avec plusieurs éléments visibles.
-   Une liste déroulante est une liste dans laquelle l’élément sélectionné est toujours visible, et les autres sont visibles à la demande en cliquant sur un bouton de liste déroulante.
-   Une zone de liste modifiable est une combinaison d’une zone de liste standard ou d’une liste déroulante et d’une [zone de texte](ctrl-text-boxes.md)modifiable, ce qui permet aux utilisateurs d’entrer une valeur qui ne figure pas dans la liste.
    -   Une liste déroulante modifiable est une combinaison d’une liste déroulante et d’une zone de texte modifiable.
    -   Une zone de liste modifiable est une combinaison d’une zone de liste standard et d’une zone de texte modifiable.

> [!Note]  
> Les instructions relatives à la [disposition](vis-layout.md) sont présentées dans un article distinct.

 

## <a name="is-this-the-right-control"></a>Est-ce le contrôle approprié ?

Pour vous décider, posez-vous les questions suivantes :

-   **Le contrôle est-il utilisé pour choisir une option dans une liste de valeurs s’excluant mutuellement ?** Si ce n’est pas le cas, utilisez un autre contrôle. Pour choisir plusieurs options, utilisez une [liste à sélection multiple standard](ctrl-list-boxes.md), une liste de cases à cocher, un générateur de listes ou une liste ajouter/supprimer à la place.
-   **Les options sont-elles disponibles ?** Dans ce cas, utilisez un [bouton de menu](ctrl-command-buttons.md) ou un bouton partagé à la place. Utilisez les listes déroulantes et les zones de liste déroulante pour les objets (noms) ou les attributs (adjectifs), mais pas pour les commandes (verbes).
-   **La liste présente-t-elle des données plutôt que des options de programme ?** Dans les deux cas, une liste déroulante ou une zone de liste déroulante est un choix approprié. En revanche, les [cases d’option](ctrl-radio-buttons.md) ne conviennent qu’à un petit nombre d’options de programme.

**Listes déroulantes**

-   **Existe-t-il une option par défaut recommandée pour la plupart des utilisateurs dans la plupart des cas ?** L’option sélectionnée est-elle beaucoup plus importante que l’affichage des alternatives ? Envisagez d’utiliser une liste déroulante si vous ne souhaitez pas encourager les utilisateurs à apporter des modifications en masquant les alternatives. Si ce n’est pas le cas, envisagez des cases d’option, une liste à sélection unique ou une zone de liste modifiable, ce qui donne plus d’importance aux choix alternatifs.

    ![capture d’écran de la qualité la plus élevée comme bouton par défaut ](images/ctrl-drop-image2.png)

    Dans cet exemple, la qualité de couleur la plus élevée est le meilleur choix pour la plupart des utilisateurs. par conséquent, une liste déroulante est un bon choix pour minimiser les alternatives.

-   **Voulez-vous attirer l’attention sur l’option ?** Dans ce cas, envisagez des cases d’option, une liste à sélection unique ou une zone de liste modifiable, qui tend à attirer davantage l’attention en tirant de l’espace à l’écran. Étant donné que les listes déroulantes sont compactes, elles sont de bons choix pour les options que vous souhaitez souligner.
-   **L’espace à l’écran est-il d’un niveau Premium ?** Dans ce cas, utilisez une liste déroulante, car l’espace à l’écran utilisé est fixe et indépendant du nombre de choix.
-   **Existe-t-il d’autres listes déroulantes dans la fenêtre ?** Dans ce cas, envisagez d’utiliser une liste déroulante pour la cohérence.

**Listes déroulantes modifiables**

Outre les principes fournis uniquement pour les listes déroulantes, les éléments suivants s’appliquent également :

-   **Les choix possibles sont-ils limités ?** Dans ce cas, utilisez plutôt une liste déroulante normale. Les zones de liste modifiable sont destinées à une entrée sans contrainte, dans laquelle les utilisateurs peuvent avoir besoin d’entrer une valeur qui ne se trouve pas actuellement dans la liste. Étant donné que l’entrée n’est pas contrainte, si les utilisateurs entrent du texte qui n’est pas valide, vous devez gérer l’erreur avec un message d’erreur.
-   **Pouvez-vous énumérer les choix les plus probables à l’avance**? Si ce n’est pas le cas, utilisez plutôt une zone de texte.
-   **La liste déroulante est-elle utilisée pour répertorier les entrées d’utilisateur précédentes ?** À moins que les utilisateurs aient besoin d’examiner la liste complète des entrées précédentes, utilisez plutôt une zone de texte avec l’option de saisie semi-automatique.

    ![capture d’écran de la boîte de dialogue exécuter avec une liste déroulante ](images/ctrl-drop-image3.png)

    Dans cet exemple, les utilisateurs peuvent avoir besoin de passer en revue leur entrée précédente. une liste déroulante modifiable est donc un bon choix.

    ![capture d’écran d’Outlook pour la ligne et la saisie semi-automatique ](images/ctrl-drop-image4.png)

    Dans cet exemple, une zone de texte avec saisie semi-automatique est un bon choix.

-   **Les utilisateurs auront-ils besoin d’aide pour sélectionner des valeurs valides ?** Dans ce cas, utilisez une zone de texte avec un [bouton Parcourir](ctrl-command-buttons.md) à la place.

    ![capture d’écran d’Outlook pour la ligne et le bouton Parcourir ](images/ctrl-drop-image5.png)

    Dans cet exemple, les utilisateurs peuvent cliquer sur « to » pour les aider à sélectionner des valeurs valides.

-   **Est-il important d’encourager les utilisateurs à passer en revue les choix alternatifs ou d’inviter des modifications ?** Dans ce cas, envisagez d’utiliser une zone de liste modifiable à la place. Avec une liste déroulante modifiable, les utilisateurs n’ont pas connaissance des alternatives tant que la liste n’est pas supprimée.
-   **Les utilisateurs doivent-ils localiser rapidement un élément dans une grande liste ?** (Win32 uniquement) Dans ce cas, utilisez une zone de liste déroulante, car les utilisateurs peuvent sélectionner un élément en tapant son nom complet. En revanche, la liste déroulante Win32 sélectionne les éléments uniquement en fonction du dernier caractère tapé (par conséquent, la saisie de « juin » dans une liste de mois correspond à novembre, et non à juin). Dans ce cas, utilisez une zone de liste modifiable même si les choix possibles sont limités.

**Zones de liste modifiables**

-   **Les choix possibles sont-ils limités ?** Dans ce cas, utilisez une liste de sélection unique ou une liste déroulante normale à la place. Les zones de liste modifiable sont destinées à une entrée sans contrainte, où les utilisateurs peuvent avoir besoin d’entrer une valeur qui n’est pas actuellement dans la liste. Étant donné que l’entrée n’est pas contrainte, si les utilisateurs entrent du texte qui n’est pas valide, vous devez gérer l’erreur avec un message d’erreur.
-   **Pouvez-vous énumérer les choix les plus probables à l’avance ?** Si ce n’est pas le cas, utilisez plutôt une zone de texte.
-   **Est-il important d’encourager les utilisateurs à passer en revue les choix alternatifs ou d’inviter des modifications ?** Si ce n’est pas le cas, envisagez plutôt une liste déroulante modifiable.
-   **Voulez-vous attirer l’attention sur l’option ?** Si ce n’est pas le cas, envisagez plutôt une liste déroulante modifiable. Étant donné que les listes déroulantes sont compactes, elles sont de bons choix pour les options que vous souhaitez souligner.
-   **L’espace à l’écran est-il d’un niveau Premium ?** Dans ce cas, utilisez une liste déroulante modifiable, car l’espace à l’écran utilisé est fixe et indépendant du nombre de choix.

Pour les listes déroulantes, **le nombre d’éléments dans la liste n’est pas un facteur de choix du contrôle** , car ils sont mis à l’échelle de milliers d’éléments jusqu’à un. Les listes déroulantes modifiables sont mises à l’échelle de milliers d’éléments jusqu’à aucun, car les utilisateurs peuvent entrer une valeur qui ne figure pas dans la liste. Étant donné que les listes déroulantes peuvent être utilisées pour les données, le nombre d’éléments peut ne pas être connu à l’avance et peut-être ne pas être garanti. **Incluez toujours au moins trois éléments dans les zones de liste modifiables pour justifier l’espace d’écran supplémentaire.**

## <a name="usage-patterns"></a>Modèles d’usage

Les listes déroulantes et les zones de liste déroulante ont plusieurs modèles d’utilisation :



|   Usage     |    Exemple   |
|-------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Liste déroulante **liste** déroulante standard, avec un ensemble fixe de valeurs prédéterminées. <br/>                                 | une fois fermé, seul l’élément sélectionné est visible. Quand les utilisateurs cliquent sur le bouton de liste déroulante, toutes les options deviennent visibles. pour modifier la valeur, les utilisateurs ouvrent la liste et cliquent sur une autre valeur.<br/> ![capture d’écran de la liste déroulante, options masquées ](images/ctrl-drop-image6.png)<br/> dans cet exemple, la liste est dans son état normal.<br/> ![capture d’écran de la liste déroulante, options affichées ](images/ctrl-drop-image7.png)<br/> Dans cet exemple, la liste a été déroulée.<br/> |
| Liste déroulante d’aperçu une liste déroulante qui affiche un **Aperçu** des résultats de la sélection pour aider les utilisateurs à choisir.<br/>             | ![capture d’écran des options de couleur et de texte ](images/ctrl-drop-image8.png)<br/> Dans ces exemples, les listes déroulantes affichent un aperçu des résultats de la sélection.<br/>                                                                                                                                                                                                                                                                                                                                           |
| Liste déroulante **modifiable** une zone de liste déroulante, qui permet aux utilisateurs d’entrer une valeur qui ne figure pas dans la liste déroulante.<br/> | ![aa511458. dropdownlists27 (en-US, MSDN. 10) .png](images/ctrl-drop-image9.png)![capture d’écran de la zone de liste déroulante de taille de police modifiable ](images/ctrl-drop-image10.png)<br/> Exemples d’une liste déroulante modifiable dans les modes modifier et déroulant.<br/> Utilisez ce contrôle lorsque vous souhaitez donner la flexibilité d’une zone de texte, mais que vous souhaitez aider les utilisateurs en fournissant une liste pratique des choix possibles.<br/>                                                                                                   |
| **Zones de liste modifiables** zone de liste modifiable standard, qui permet aux utilisateurs d’entrer une valeur qui ne figure pas dans la liste toujours visible. <br/> | ![capture d’écran de la liste déroulante des options de police ](images/ctrl-drop-image11.png)<br/> Dans ces exemples, les zones de liste modifiables sont toujours affichées.<br/> Ce contrôle est un meilleur choix que la liste déroulante modifiable lorsqu’il est important d’encourager les utilisateurs à passer en revue les choix alternatifs ou d’inviter des modifications.<br/>                                                                                                                                                                      |



 

## <a name="guidelines"></a>Consignes

### <a name="general"></a>Généralités

-   **N’utilisez pas la modification d’une liste déroulante ou d’une zone de** liste déroulante pour :
    -   Exécuter des commandes.
    -   Affichez d’autres fenêtres, telles qu’une boîte de dialogue pour recueillir davantage d’entrées.
    -   Afficher dynamiquement d’autres contrôles en rapport avec le contrôle sélectionné (les[lecteurs d’écran](inter-accessibility.md) ne peuvent pas détecter de tels événements).

### <a name="presentation"></a>Présentation

-   **Triez les éléments de liste dans un ordre logique**, par exemple, en regroupant les options très liées, en plaçant d’abord les options les plus courantes ou en utilisant l’ordre alphabétique. Triez les noms dans l’ordre alphabétique, les nombres dans l’ordre numérique et les dates dans l’ordre chronologique. Les listes avec 12 éléments ou plus doivent être triées par ordre alphabétique pour faciliter la recherche d’éléments.

    **Correct :** ![ capture d’écran de la liste déroulante logique ](images/ctrl-drop-image12.png)

    Dans cet exemple, les éléments de liste sont triés en fonction de leur relation spatiale.

    **Incorrect :** ![ capture d’écran de la liste déroulante désorganisée ](images/ctrl-drop-image13.png)

    Dans cet exemple, un grand nombre d’éléments de liste doivent être triés par ordre alphabétique.

    **Correct :** ![ capture d’écran de la liste déroulante par ordre alphabétique ](images/ctrl-drop-image14.png)

    Dans cet exemple, les éléments de liste sont triés par ordre alphabétique, à l’exception de l’option qui représente tous les éléments.

-   **Placez les options qui représentent tout ou aucune au début de la liste, quel que soit l’ordre de tri des éléments restants.**
-   **Placez les méta-options entre parenthèses.**

    ![Capture d’écran montrant une liste déroulante avec l’option « (aucun) » sélectionnée.](images/ctrl-drop-image15.png)

    Dans cet exemple, « (None) » est une méta-option, car il ne s’agit pas d’une valeur valide pour le choix. elle décrit plutôt que l’option elle-même n’est pas utilisée.

-   **Lors de la désactivation d’une liste déroulante ou d’une zone de liste déroulante, désactivez également les étiquettes et les boutons de commande associés.**

### <a name="drop-down-lists"></a>Listes déroulantes

-   Quand une liste déroulante unique est utilisée pour modifier l’affichage d’un contrôle associé, **Modifiez la vue immédiatement sur la sélection au lieu de demander un bouton de commande distinct.** Utilisez un bouton de commande distinct uniquement si la liste prend beaucoup de temps à restituer. Toutefois, les en-têtes de liste et les [boutons de menu](ctrl-command-buttons.md) sont les contrôles préférés à cet effet.
-   Les **éléments de liste vides n’utilisent pas** **les options méta à la place**. Les utilisateurs ne savent pas comment interpréter les éléments vides, alors que la signification des méta-options est explicite.

    **Correct :** ![ capture d’écran de la liste déroulante avec aucun sélectionné ](images/ctrl-drop-image16.png)

    **Incorrect :** ![ capture d’écran de la liste déroulante avec l’option vide sélectionnée ](images/ctrl-drop-image17.png)

    Dans l’exemple incorrect, la signification de l’option Blank n’est pas claire.

### <a name="preview-drop-down-lists"></a>Listes déroulantes d’aperçu

-   **Utilisez des aperçus dans les éléments de liste lorsqu’il est préférable de les afficher avec des images plutôt que de les décrire à l’aide de texte seul.**

    ![capture d’écran de la liste déroulante des polices prévisualisées ](images/ctrl-drop-image18.png)

    Dans cet exemple, la version préliminaire explique les options bien meilleures que le texte seul.

-   **N’utilisez pas d’icônes inutiles et inutilisables dans les aperçus**.

    **Incorrect :** ![ capture d’écran de la liste déroulante des étiquettes avec des icônes ](images/ctrl-drop-image19.png)

    Dans cet exemple, les icônes d’aperçu ne sont pas nécessaires, car elles ne communiquent aucune information.

### <a name="combo-boxes"></a>Zones de liste modifiable

-   **Lorsque vous le pouvez, limitez la longueur du texte d’entrée.** Par exemple, si l’entrée valide est un nombre compris entre 0 et 999, utilisez une zone de liste déroulante limitée à trois caractères.
-   **S’il existe de nombreuses options possibles, concentrez le contenu de la liste sur les options les plus probables**. Étant donné que les utilisateurs peuvent entrer des valeurs qui ne figurent pas dans la liste, les zones de liste modifiable n’ont pas besoin de répertorier tous les choix, mais uniquement les choix probables ou un échantillon représentatif.

    ![capture d’écran de la liste déroulante des tailles de police ](images/ctrl-drop-image10.png)

    Dans cet exemple, un grand nombre de choix valides ne sont pas listés, par exemple, 15, ou des polices de demi-taille telles que 9,5.

### <a name="default-values"></a>Valeurs par défaut

-   **Sélectionnez le niveau de sécurité le plus sûr (pour éviter la perte de données ou l’accès au système) et l’option la plus sécurisée par défaut.** Si la sécurité et la sécurité ne sont pas des facteurs, sélectionnez l’option la plus probable ou la plus pratique.
    -   **Exception :** Affichez une valeur par défaut vide si le contrôle représente une propriété dans un [État mixte](glossary.md), qui se produit lors de l’affichage d’une propriété pour plusieurs objets qui n’ont pas le même paramètre.

## <a name="prompts"></a>Invites

Une invite est une étiquette ou une brève instruction placée à l’intérieur d’une liste déroulante modifiable en tant que valeur par défaut. Contrairement au texte statique, les invites disparaissent de l’écran une fois que les utilisateurs ont tapé un texte dans la zone de liste déroulante ou qu’il obtient le focus d’entrée.

![capture d’écran d’une zone de recherche ](images/ctrl-drop-image20.png)

Invite classique.

Utilisez une invite dans les cas suivants :

-   L’espace à l’écran est d’une qualité telle que l’utilisation d’une étiquette ou d’une instruction n’est pas souhaitable, par exemple dans une barre d’outils.
-   L’invite est principalement destinée à identifier l’objectif de la liste de manière compacte. Il ne doit pas s’agir d’informations essentielles que les utilisateurs doivent voir lors de l’utilisation de la zone de liste modifiable.

N’utilisez pas les invites uniquement pour demander aux utilisateurs de sélectionner un nom dans la liste ou de cliquer sur les boutons. Par exemple, les invites comme sélectionner une option ou entrer un nom de fichier, puis cliquer sur Envoyer ne sont pas nécessaires.

Quand vous utilisez des invites :

-   Dessinez le texte de l’invite en italique gris et en texte réel en noir normal. Le texte de l’invite ne doit pas être confondu avec du texte réel.
-   Conservez le texte de l’invite concis. Vous pouvez utiliser des fragments au lieu de phrases entières.
-   Utilisez la mise [en majuscules de style phrase](glossary.md).
-   N’utilisez pas de ponctuation de fin ni de points de suspension.
-   Le texte de l’invite ne doit pas être modifiable et doit disparaître une fois que les utilisateurs ont cliqué dans ou sur l’onglet dans la zone de texte.
    -   **Exception :** L’invite s’affiche si la zone de texte a le focus d’entrée par défaut et disparaît uniquement une fois que l’utilisateur a commencé à taper.
-   Le texte d’invite est restauré si la zone de texte est toujours vide lorsqu’il perd le focus d’entrée.

**Incorrect :** ![ capture d’écran de six listes déroulantes modifiables](images/ctrl-drop-image21.png)

Dans cet exemple, l’espace à l’écran n’est pas à un niveau Premium. une fois qu’une liste déroulante modifiable est remplie, il est difficile pour les utilisateurs de se souvenir de leur rôle. et le texte d’invite est modifiable et dessiné de la même façon que le texte réel.

## <a name="recommended-sizing-and-spacing"></a>Dimensionnement et espacement recommandés

![capture d’écran de la liste déroulante et des spécifications ](images/ctrl-drop-image22.png)

Dimensionnement et espacement recommandés pour les listes déroulantes et les zones de liste déroulante.

-   **Choisissez une largeur appropriée pour les données valides les plus longues.** Les listes déroulantes ne peuvent pas faire l’objet d’un défilement horizontalement, de sorte que les utilisateurs ne voient que ce qui est visible dans le contrôle. (Notez, toutefois, que la fonctionnalité de défilement automatique peut être activée pour les zones de liste déroulante.)
-   **Incluez 30 pour cent supplémentaires** (jusqu’à 200 pour cent pour du texte plus petit) pour tout texte (mais pas les nombres) qui sera localisé.
-   **Choisissez une longueur de liste qui élimine le défilement vertical inutile.** Étant donné que les listes déroulantes sont affichées à la demande, leurs listes doivent afficher jusqu’à 30 éléments. Les zones de liste modifiables (celles qui n’ont pas de bouton déroulant) doivent afficher entre 3 et 12 éléments.

## <a name="labels"></a>Étiquettes

**Étiquettes de contrôle**

-   Écrivez l’étiquette sous la forme d’un mot ou d’une expression, et non pas en tant que phrase, et terminez-la par un signe deux-points. **Exceptions :**
    -   Listes déroulantes modifiables avec des invites à l’emplacement où l’espace est à un niveau Premium.
    -   Si une liste déroulante ou une zone de liste déroulante est subordonnée à une case d’option ou à une case à cocher et qu’elle est introduite par son étiquette se terminant par un signe deux-points, ne placez pas d’étiquette supplémentaire sur le contrôle.
-   Attribuez une [clé d’accès](glossary.md) unique pour chaque étiquette. Pour obtenir des instructions, consultez [clavier](inter-keyboard.md).
-   Utilisez la mise [en majuscules de style phrase](glossary.md).
-   Placez l’étiquette à gauche ou au-dessus du contrôle, puis alignez l’étiquette sur le bord gauche du contrôle. Si l’étiquette est située à gauche, aligne verticalement le texte de l’étiquette avec le texte du contrôle.

    **Correct :** ![ capture d’écran de l’alignement des étiquettes de liste déroulante ](images/ctrl-drop-image23.png)

    Dans cet exemple, l’étiquette est correctement alignée avec le texte du contrôle.

    **Incorrect :** ![ capture d’écran de la liste déroulante alignée de manière incorrecte ](images/ctrl-drop-image24.png)

    Dans cet exemple, l’étiquette est alignée de manière incorrecte avec le texte du contrôle.

-   Vous pouvez spécifier des unités (secondes, connexions, etc.) entre parenthèses après l’étiquette.
-   Ne définissez pas le contenu de la zone de liste déroulante ou de la zone de liste déroulante (ou son étiquette d’unités) dans une phrase, car cela n’est pas localisable.

**Texte de l’option**

-   Attribuez un nom unique à chaque option.
-   Utilisez la mise [en majuscules de style phrase](glossary.md), sauf si un élément est un nom propre.
-   Écrivez l’étiquette sous la forme d’un mot ou d’une expression, et non pas en tant que phrase, et n’utilisez pas de ponctuation finale.
-   Utilisez une formulation parallèle et essayez de conserver la même longueur pour toutes les options.

**Texte d’instructions**

-   Si vous devez ajouter du texte d’instructions sur une liste déroulante ou une zone de liste déroulante, ajoutez-la au-dessus de l’étiquette. Utilisez des phrases complètes avec la ponctuation finale.
-   Utilisez la mise [en majuscules de style phrase](glossary.md).
-   Les informations supplémentaires qui sont utiles, mais pas nécessaires, doivent être courtes. Placez ces informations entre parenthèses entre l’étiquette et le signe deux-points, ou sans parenthèses sous le contrôle.

    ![capture d’écran de la liste déroulante avec des données ajoutées ](images/ctrl-drop-image25.png)

    Cet exemple montre des informations supplémentaires placées sous le contrôle.

## <a name="documentation"></a>Documentation

Lorsque vous faites référence à des listes déroulantes :

-   Utilisez le texte exact de l’étiquette, y compris sa mise en majuscules, mais n’incluez pas le trait de soulignement ou le signe deux-points ; incluez une liste ou une zone, selon la valeur la plus claire.
-   Pour les options de liste, utilisez le texte exact de l’option, y compris sa mise en majuscules.
-   Pour la programmation et d’autres documents techniques, reportez-vous aux listes déroulantes sous forme de listes déroulantes. Partout ailleurs, utilisez la liste ou la zone, selon la valeur la plus claire.
-   Pour décrire l’interaction de l’utilisateur, utilisez le clic.
-   Dans la mesure du possible, mettez en forme les options d’étiquette et de liste en texte gras. Sinon, placez l’étiquette et les options entre guillemets uniquement si nécessaire pour éviter toute confusion.

Exemple : dans la liste **taille de police** , cliquez sur **grandes polices**.

Lorsque vous faites référence à des zones de liste déroulante :

-   Utilisez le texte exact de l’étiquette, y compris sa mise en majuscules, mais n’incluez pas le trait de soulignement ou le signe deux-points ; incluez le mot zone.
-   Pour les options de liste, utilisez le texte exact de l’option, y compris sa mise en majuscules.
-   Pour la programmation et d’autres documents techniques, reportez-vous aux zones de liste modifiable. Partout ailleurs, utilisez Box.
-   Pour décrire l’interaction de l’utilisateur, utilisez Enter.
-   Dans la mesure du possible, mettez en forme les options d’étiquette et de liste en texte gras. Sinon, placez l’étiquette et les options entre guillemets uniquement si nécessaire pour éviter toute confusion.

Exemple : dans la zone **police** , entrez la police que vous souhaitez utiliser.

 

