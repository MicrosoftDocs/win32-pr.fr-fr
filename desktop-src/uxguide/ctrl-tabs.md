---
title: Tabulations
description: Les onglets permettent de présenter des informations connexes sur des pages étiquetées distinctes.
ms.assetid: d90228ce-aa95-4359-be8e-ea2014d71ae6
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b2649862885e55bdfe10fdca7f34b7618d976a38
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104550209"
---
# <a name="tabs"></a>Tabulations

> [!NOTE]
> Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Les onglets permettent de présenter des informations connexes sur des pages étiquetées distinctes.

![capture d’écran de cinq onglets ](images/ctrl-tabs-image1.png)

Ensemble classique d’onglets.

Les onglets sont généralement associés à des fenêtres de propriétés (et vice versa), mais les onglets peuvent être utilisés dans n’importe quel type de fenêtre.

Les contrôles onglet représentent les dossiers à onglets utilisés pour organiser les informations dans les armoires de classement qui se trouvent généralement dans le États-Unis. (Les dossiers Manille ne sont pas utilisés dans le monde entier.)

> [!Note]  
> Les instructions relatives à la [disposition](vis-layout.md), aux [menus d’onglet](cmd-menus.md), aux [boîtes de dialogue](win-dialog-box.md)et aux fenêtres de [Propriétés](win-property-win.md) sont présentées dans des articles distincts.

 

## <a name="is-this-the-right-control"></a>Est-ce le contrôle approprié ?

Pour vous décider, posez-vous les questions suivantes :

-   **Les contrôles peuvent-ils s’ajuster à une seule page de taille raisonnable ?** Dans ce cas, utilisez une seule page.
-   **Existe-t-il un seul onglet ?** Dans ce cas, utilisez une seule page.
-   **Les onglets sont-ils liés les uns aux autres de façon évidente ?** Si ce n’est pas le cas, envisagez de fractionner les informations en différentes fenêtres d’informations associées.
-   **S’ils sont utilisés pour les paramètres, les paramètres sur des pages différentes sont-ils totalement indépendants ?** La modification d’un paramètre d’une page affecte-t-elle les paramètres des autres pages ? Si elles ne sont pas indépendantes, utilisez des pages de tâches ou un [Assistant](win-wizards.md) à la place.
-   **Les onglets sont-ils principalement des pairs les uns des autres, ou existe-t-il une relation hiérarchique ?** Si vous utilisez une hiérarchie, envisagez d’utiliser la divulgation progressive ou les [boîtes de dialogue](win-dialog-box.md) enfants pour afficher les informations connexes.
-   **Les onglets sont-ils utilisés pour afficher les étapes d’une tâche ?** Vous pouvez utiliser des « onglets » pour afficher les étapes d’une tâche uniquement si elles sont présentées comme des étapes, et qu’il existe un autre moyen évident d’accéder à l’étape de texte, comme un bouton suivant. Sinon, si les étapes sont requises, utilisez des pages dans un workflow de page ou un [Assistant](win-wizards.md). Si les étapes sont facultatives, affichez plutôt les étapes facultatives à l’aide de [boîtes de dialogue](win-dialog-box.md) modales.
-   **Les onglets présentent-ils des vues différentes des mêmes données ?** Dans ce cas, envisagez d’utiliser un [bouton partagé](ctrl-command-buttons.md) ou une [liste déroulante](/windows/desktop/uxguide/ctrl-drop) pour modifier les affichages. Bien que les onglets puissent être utilisés efficacement pour modifier les vues, les alternatives sont plus légères.

## <a name="usage-patterns"></a>Modèles d’usage

Les onglets ont plusieurs modèles d’utilisation :



|                                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Surface de fenêtre dynamique**<br/> comme les barres de défilement, les onglets peuvent être utilisés pour augmenter la surface d’exposition de la fenêtre et afficher les informations connexes.<br/>                                                    | Avec ce modèle, l’utilisation d’onglets est conceptuellement similaire au placement de toutes les informations sur les onglets de manière linéaire sur une surface à défilement unique, avec les étiquettes d’onglets comme en-têtes. <br/> ![capture d’écran de cinq onglets ](images/ctrl-tabs-image1.png)<br/> Dans cet exemple, les onglets augmentent efficacement la surface d’exposition de la fenêtre.<br/>                          |
| **Plusieurs vues**<br/> comme les boutons partagés ou les listes déroulantes, les onglets peuvent être utilisés pour afficher différentes vues des mêmes informations ou associées. <br/>                                           | ![capture d’écran des onglets conception, fractionnement et aperçu ](images/ctrl-tabs-image2.png)<br/> Dans cet exemple, les onglets changent d’affichages dans un document.<br/>                                                                                                                                                                                                         |
| **Documents multiples**<br/> comme pour plusieurs fenêtres, les onglets peuvent être utilisés pour afficher différents documents dans une seule fenêtre. <br/>                                                                   | ![capture d’écran de trois onglets pour différents documents ](images/ctrl-tabs-image3.png)<br/> ![Figure des onglets pour les différents mois ](images/ctrl-tabs-image4.png)<br/> Dans ces exemples, les onglets affichent différents documents dans une seule fenêtre d’application.<br/>                                                                                       |
| **Options exclusives**<br/> comme les cases d’option, les onglets peuvent être utilisés pour présenter plusieurs choix exclusifs. dans ce modèle, seul l’onglet sélectionné s’applique et tous les autres onglets sont ignorés. <br/> | ![capture d’écran des onglets emplacement, données et messages ](images/ctrl-tabs-image5.png)<br/> Dans cet exemple, les onglets sont utilisés (de façon incorrecte) comme substituts des cases d’option.<br/> **Ce modèle n’est pas recommandé** , car il utilise un comportement non standard. Les onglets se comportent comme un paramètre plutôt que simplement un moyen de naviguer dans la fenêtre. <br/> |



 

**Si vous n’avez qu’une seule chose...**

Assurez-vous que les informations figurant dans les onglets sont liées, mais que les paramètres sur les différentes pages sont indépendants. Le dernier onglet sélectionné ne doit pas avoir de signification particulière.

## <a name="guidelines"></a>Consignes

### <a name="general"></a>Général

-   **Utilisez des tabulations horizontales si :**
    -   La fenêtre a sept onglets ou moins.
    -   **Tous les onglets s’ajustent sur une seule ligne, même lorsque l’interface utilisateur est localisée.**
-   **Utilisez des tabulations verticales si :**
    -   La fenêtre de propriétés comporte huit onglets ou plus.
    -   **L’utilisation de tabulations horizontales nécessitera plusieurs lignes.**

        ![capture d’écran de la fenêtre de propriétés avec onze options ](images/ctrl-tabs-image6.png)

        Dans cet exemple, les onglets verticaux prennent en charge huit onglets ou plus.

-   **N’imbriquez pas d’onglets ou combinez des onglets horizontaux avec des tabulations verticales.** Au lieu de cela, réduisez le nombre d’onglets, utilisez uniquement des tabulations verticales ou utilisez un autre contrôle comme une liste déroulante.
-   **Ne pas faire défiler les onglets horizontaux.** Le défilement horizontal n’est pas facilement détectable. Toutefois, vous pouvez faire défiler verticalement les onglets.

    **Incorrect :**

    ![capture d’écran de l’étiquette de tabulation horizontale tronquée ](images/ctrl-tabs-image7.png)

    Dans cet exemple, les onglets horizontaux défilent.

-   Pour les onglets d’une fenêtre ou d’un volet redimensionnable, placez une barre de défilement, si nécessaire, sur la page, et non sur la fenêtre ou le volet. Les onglets doivent toujours être visibles et ne pas défiler hors de l’affichage.

    ![capture d’écran de la page d’onglets verticale avec la barre de défilement ](images/ctrl-tabs-image8.png)

    Dans cet exemple, la page d’onglets contient la barre de défilement, et non le volet.

-   **Assurez-vous que les onglets ressemblent à des onglets et non à un autre type de contrôle.**

    **Incorrect :**

    ![capture d’écran de la fenêtre avec boutons pour les onglets ](images/ctrl-tabs-image9.png)

    Dans cet exemple, ces onglets ressemblent à des boutons de commande.

### <a name="interaction"></a>Interaction

-   **Lorsque les contrôles s’appliquent uniquement à une page, placez-les dans la bordure de la page à onglets.**
-   **Lorsque les contrôles s’appliquent à la totalité de la fenêtre, placez-les en dehors de la page à onglets.**
-   **N’affectez pas d’effets à la modification des onglets.** Les onglets doivent être accessibles dans n’importe quel ordre. La modification de l’onglet actuel ne doit jamais avoir d’effets secondaires, appliquer des paramètres ou générer un message d’erreur.
-   **N’affectez pas une signification spéciale au dernier onglet sélectionné.** La sélection de l’onglet est pour la navigation la dernière sélection de l’onglet de l’utilisateur n’est pas un paramètre.
-   **Ne rendez pas les paramètres sur une page dépendants des paramètres d’autres pages.** Placez à la place tous les paramètres dépendants sur la même page.
-   **Si les utilisateurs sont susceptibles de démarrer avec le dernier onglet affiché, rendez l’onglet persistant et sélectionnez-le par défaut.** Rendez les paramètres persistants en fonction de la fenêtre, par utilisateur. Dans le cas contraire, sélectionnez la première page par défaut.

### <a name="icons"></a>Icônes

-   **Ne placez pas d’icônes sur les onglets.** Les icônes ajoutent généralement un encombrement visuel inutile, consomment de l’espace à l’écran et n’améliorent souvent pas la compréhension des utilisateurs. Ajoutez uniquement des icônes qui facilitent la compréhension, telles que les symboles standard.

    **Incorrect :**

    ![capture d’écran de la fenêtre avec des icônes sur les onglets ](images/ctrl-tabs-image10.png)

    Dans cet exemple, les icônes ajoutent un encombrement visuel et ne permettent pas d’améliorer la compréhension des utilisateurs.

    **Exception :** Vous pouvez utiliser des icônes clairement identifiables si l’espace est insuffisant pour afficher des étiquettes explicites :

    **Correct :**

    ![capture d’écran d’onglets avec des icônes et des étiquettes abrégées ](images/ctrl-tabs-image11.png)

    Dans cet exemple, la fenêtre est tellement étroite que les icônes communiquent mieux les onglets que les étiquettes.

-   **N’utilisez pas de logos de produit pour les graphiques d’onglets.** Les onglets ne sont pas destinés à la [personnalisation](exper-branding.md).

### <a name="dynamic-window-surface-pattern"></a>Modèle de surface de fenêtre dynamique

-   **N’utilisez pas de barres de défilement sur les pages d’onglets.** Les tabulations fonctionnent de la même façon que les barres de défilement pour augmenter la zone effective d’une fenêtre. Un mécanisme doit suffire.
-   **Utilisez des étiquettes d’onglet concises.** Utilisez un ou deux mots qui décrivent clairement le contenu de la page. Les étiquettes plus longues consomment de l’espace à l’écran, en particulier lorsque les étiquettes sont localisées.
-   **Utilisez des étiquettes d’onglet explicites et explicites.** Évitez les étiquettes d’onglet génériques qui peuvent s’appliquer à n’importe quel onglet, tel que général, avancé ou paramètres.
-   **Si un onglet ne s’applique pas au contexte actuel et que les utilisateurs ne l’attendent pas, supprimez-le.** Cela simplifie l’interface utilisateur et les utilisateurs ne le manquent pas.

    **Incorrect :**

    ![capture d’écran de la fenêtre options avec le nom de l’onglet grisé ](images/ctrl-tabs-image12.png)

    Dans cet exemple, l’onglet emplacements des fichiers est désactivé de manière incorrecte lorsque Microsoft Word est utilisé comme éditeur de courrier électronique. Au lieu de désactiver cet onglet, vous devez le supprimer, car les utilisateurs ne s’attendent pas à afficher ou à modifier les emplacements des fichiers dans ce contexte.

-   **Si un onglet ne s’applique pas au contexte actuel et que les utilisateurs peuvent s’attendre à ce que :**

    -   Affichez l’onglet.
    -   Désactivez les contrôles sur la page.
    -   Incluez du texte expliquant pourquoi les contrôles sont désactivés.

    Ne désactivez pas l’onglet, car cela n’est pas explicite et interdit l’exploration. Les utilisateurs qui recherchent une valeur spécifique sont obligés d’examiner tous les autres onglets.

    ![capture d’écran de la fenêtre avec les options de l’onglet Affichage grisées ](images/ctrl-tabs-image13.png)

    Dans cet exemple, aucune des options d’affichage ne s’applique en mode lecture. Toutefois, les utilisateurs peuvent s’attendre à ce qu’ils s’appliquent en fonction de l’étiquette d’onglet, de sorte que la page s’affiche, mais les options sont désactivées.

### <a name="multiple-views-and-documents-patterns"></a>Modèles de vues et de documents multiples

-   **Utilisez les noms d’affichage ou de document sur les étiquettes d’onglet.**
-   **Évitez les noms d’onglets trop longs.** Si nécessaire, utilisez une taille de nom maximale ou tronquez l’étiquette d’onglet affichée à l’aide de ellipses. Les étiquettes plus longues consomment de l’espace à l’écran, en particulier lorsque les étiquettes sont localisées.
-   **Si un onglet ne s’applique pas au contexte actuel, supprimez l’onglet.**

### <a name="exclusive-options-pattern"></a>Modèle d’options exclusives

-   **N’utilisez pas ce modèle !** Utilisez à la place des cases d’option ou une liste déroulante.

    **Incorrect :**

    ![capture d’écran de la fenêtre avec deux onglets « créer » ](images/ctrl-tabs-image14.png)

    Dans cet exemple, les onglets sont incorrectement utilisés comme substituts pour les cases d’option.

    **Correct :**

    ![capture d’écran de la fenêtre avec deux cases d’option ](images/ctrl-tabs-image15.png)

    Dans cet exemple, les cases d’option sont correctement utilisées à la place.

## <a name="labels"></a>Étiquettes

-   Étiquetez les onglets en fonction de leur modèle. Utilisez des noms plutôt que des verbes, sans ponctuation finale. Pour plus d’informations, consultez les instructions de modèle précédentes.
-   Utilisez les majuscules comme pour les phrases.
-   N’attribuez pas de clé d’accès. Les onglets sont accessibles par le biais de leurs touches de raccourci (Ctrl + Tab, Ctrl + Maj + Tab, CTRL + PG PRÉC, CTRL + PG suiv). Les choix de clé d’accès sont insuffisants. par conséquent, si vous n’affectez pas de clés d’accès aux onglets, il est plus facile de les affecter à d’autres contrôles.

## <a name="documentation"></a>Documentation

Lorsque vous faites référence à des onglets :

-   Utilisez le texte exact de l’étiquette, y compris sa mise en majuscules, et incluez l’onglet mot.
-   Pour décrire l’interaction de l’utilisateur, utilisez le clic.
-   Dans la mesure du possible, mettez en forme l’étiquette à l’aide de texte en gras. Sinon, placez l’étiquette entre guillemets uniquement si nécessaire pour éviter toute confusion.
-   Étant donné que plusieurs utilisations peuvent être ambiguës, en particulier pour un public international, utilisez l’onglet substantif uniquement pour faire référence uniquement à un contrôle Tab. Pour les autres utilisations, clarifiez la signification avec un descripteur : la touche Tab, un taquet de tabulation ou une marque d’onglet sur la règle.

Exemple : dans le menu **Outils** , cliquez sur **options**, puis sur l’onglet **affichage** .

