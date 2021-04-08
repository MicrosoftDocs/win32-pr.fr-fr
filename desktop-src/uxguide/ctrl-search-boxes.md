---
title: Zones de recherche
description: Avec une zone de recherche, les utilisateurs peuvent localiser rapidement des objets ou du texte spécifiques dans un grand ensemble de données en filtrant ou en mettant en surbrillance les correspondances.
ms.assetid: e2d77b36-e001-403c-9b66-2d136c394a24
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: e9d1fca8fdb96b17098cee79fd5b62ecd7ab7531
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "103953326"
---
# <a name="search-boxes"></a>Zones de recherche

> [!NOTE]
> Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Avec une zone de recherche, les utilisateurs peuvent localiser rapidement des objets ou du texte spécifiques dans un grand ensemble de données en filtrant ou en mettant en surbrillance les correspondances. Il n’existe pas de contrôle de recherche standard, mais vous devez vous efforcer de faire en sorte que les fonctionnalités de recherche de votre programme soient cohérentes avec celles de Windows.

Il existe deux types de recherche :

-   **Recherche instantanée**, où les résultats s’affichent immédiatement au fur et à mesure de la nature de l’utilisateur. L’utilisateur ne doit pas cliquer sur le bouton pour que le symbole de recherche de la loupe apparaisse sous la forme d’un graphique et non d’un bouton.

    ![Capture d’écran montrant une zone de recherche instantanée avec une légende « prompt » pointant vers la zone de recherche et une légende « symbole de recherche » pointant sur le graphique de la loupe.](images/ctrl-search-boxes-image1.png)

    Zone de recherche classique utilisant la recherche instantanée. La recherche est exécutée automatiquement sur chaque séquence de touches.

-   **Recherche régulière**, où une recherche est effectuée quand l’utilisateur clique sur le bouton de recherche. Le symbole de recherche de la loupe est affiché sur un bouton.

    ![capture d’écran d’une zone de recherche normale ](images/ctrl-search-boxes-image2.png)

    Zone de recherche classique utilisant la recherche standard. Les utilisateurs cliquent sur un bouton pour effectuer la recherche.

    Vous pouvez fournir l’un ou les deux types d’options de recherche pour vos utilisateurs.

## <a name="is-this-the-right-control"></a>Est-ce le contrôle approprié ?

Pour vous décider, posez-vous les questions suivantes :

-   **Les objets spécifiques sont-ils difficiles à trouver ?** Ceci peut se produire quand :
    -   Il y a de nombreux objets.
    -   Les objets ne se trouvent pas dans un emplacement unique. La recherche est particulièrement utile pour rechercher des objets dans des arborescences.
    -   Les données de recherche sont difficiles à trouver (par exemple, les métadonnées).
-   **Les utilisateurs doivent-ils Rechercher du texte spécifique dans des documents ?**
-   **Votre fonctionnalité retourne-t-elle les résultats de recherche pertinents dans un délai de cinq secondes ?** Si ce n’est pas le cas, vous pouvez fournir une fonctionnalité de recherche, mais utilisez une autre conception qui fournit des commentaires visibles pour les recherches de longue durée, telles qu’une boîte de dialogue de recherche.

## <a name="design-concepts"></a>Principes de conception

La recherche est une première étape essentielle dans de nombreux scénarios : les utilisateurs doivent trouver des objets avant de pouvoir les utiliser. Les utilisateurs enregistrent de plus en plus d’objets sur des disques durs de plus en plus volumineux, mais la navigation pour les objets n’est pas très adaptée. La recherche doit être une partie simple, cohérente et fiable de l’expérience utilisateur.

Zones de recherche dans Windows :

-   Faisant partie de toutes les fenêtres de l’Explorateur, elles sont faciles à trouver et à reconnaître.
-   Avoir une apparence et un comportement cohérents.
-   Sont efficaces et rapides, ce qui donne des résultats instantanés en mode de recherche instantanée.

Une zone de recherche est utilisée dans les fenêtres à ces emplacements :

-   Explorateurs
-   Expériences (Microsoft Windows Media Player, Galerie de photos Windows, Windows Internet Explorer)
-   Menu Démarrer (pour rechercher des programmes et des fichiers récents)
-   Page d’emplacement du panneau de configuration (pour rechercher des éléments et des tâches dans le panneau de configuration)
-   Aide (pour rechercher des rubriques d’aide pertinentes)

### <a name="look-and-feel"></a>Apparence

La recherche dans Windows a été considérablement améliorée en prenant en charge la recherche instantanée. Le fait d’avoir des résultats instantanés rend Windows plus puissant et direct.

Dans l’Explorateur Windows et les fenêtres d’application, la recherche se trouve dans l’angle supérieur droit s’il s’agit d’un point d’entrée supplémentaire. Dans ce cas, les utilisateurs recherchent un mécanisme de recherche lorsqu’ils ne trouvent pas ce qu’ils recherchent dans la fenêtre. Toutefois, si Search est le point d’entrée principal, il est centré en haut de la fenêtre.

Le bouton de recherche est connecté visuellement à une zone de recherche. Pour réduire l’espace, une [invite](ctrl-text-boxes.md) facultative est utilisée dans une zone de recherche au lieu d’une étiquette. L’invite peut être une instruction (par exemple, taper pour rechercher) ou indiquer l’étendue de la recherche (par exemple, Rechercher des images).

![capture d’écran d’une zone de recherche instantanée ](images/ctrl-search-boxes-image3.png)

Sans étiquettes et boutons séparés, la recherche instantanée dans Windows a une apparence légère.

L’exécution d’une recherche réussie crée une page virtuelle des résultats de la recherche et l’ajoute à la pile de retour et à la barre d’adresses. Les utilisateurs disposent de plusieurs façons de restaurer la page d’origine et d’effacer une zone de recherche, notamment en cliquant sur précédent, en cliquant sur la page d’origine dans la barre d’adresses, en appuyant sur Échap ou en désactivant la zone de recherche.

Les utilisateurs peuvent également simplement effacer la zone de recherche sans restaurer une page de résultats précédente. En mode de recherche instantanée, un bouton Effacer apparaît une fois que l’utilisateur a commencé à taper. un « x » remplace le symbole de recherche de la loupe. Au survol, le « x » obtient l’apparence d’un bouton et vous pouvez cliquer dessus.

![capture d’écran d’une zone de recherche avec une icône’x' ](images/ctrl-search-boxes-image4.png)

L’utilisateur peut effacer la zone de recherche en cliquant sur « x » à l’extrémité droite du contrôle.

En mode de recherche normal, le bouton Effacer est facultatif. Les utilisateurs peuvent le trouver utile, par exemple, si l’exécution d’une recherche prend beaucoup de temps. Les utilisateurs peuvent cliquer sur le « x » pour arrêter la recherche en cours. Si une recherche est déjà terminée, les utilisateurs peuvent cliquer sur le signe « x » pour effacer la zone de recherche.

## <a name="guidelines"></a>Consignes

### <a name="location"></a>Emplacement

-   Pour les fenêtres d’application, recherchez recherche dans l’angle supérieur droit.
-   Pour les fenêtres contextuelles, localisez les recherches où qu’elles soient les plus rationnelles et pratiques.
-   **Exception :** Si la recherche est généralement la première chose que les utilisateurs effectuent dans une fenêtre (le point d’entrée principal), centrez-les en haut de la fenêtre.

### <a name="look"></a>Pench

-   Utilisez les graphiques du bouton de recherche standard. Il existe trois versions :
    -   **Symbole de recherche loupe uniquement (aucun bouton au survol).** Utilisez pour la recherche instantanée.
    -   **Loupe de la loupe avec bouton.** Utilisez le bouton lorsque vous devez cliquer sur le bouton pour démarrer la recherche.
    -   **Loupe de la loupe avec bouton et flèche déroulante.** Ajoutez une flèche déroulante lorsque les utilisateurs peuvent modifier l’étendue ou lorsque d’autres paramètres sont disponibles.
        -   Pour la recherche instantanée, utilisez uniquement une flèche déroulante et affichez un bouton au pointage.
        -   Pour la recherche régulière, affichez la flèche déroulante sur un bouton.

![Figure des zones de recherche instantanée dans différents États ](images/ctrl-search-boxes-image5.png)

Spécifications visuelles pour la recherche instantanée.

![Figure des zones de recherche standard dans différents États ](images/ctrl-search-boxes-image6.png)

Spécifications visuelles pour la recherche régulière.

-   N’utilisez pas d’étiquette. Utilisez à la place une invite facultative. Si les utilisateurs ont tendance à supposer que la recherche est une recherche de fichier générique, utilisez l’invite pour donner l’étendue. Sinon, utilisez le type pour effectuer une recherche ou une expression similaire et concise.

    ![capture d’écran de l’invite « type à rechercher » ](images/ctrl-search-boxes-image7.png)

    ![capture d’écran de l’invite « Rechercher tous les gadgets » ](images/ctrl-search-boxes-image8.png)

    Dans ces exemples, les brèves invites textuelles aident les utilisateurs à utiliser la recherche.

### <a name="interaction"></a>Interaction

-   **Dans le focus d’entrée, sélectionnez automatiquement tout texte entré précédemment.** Cela permet aux utilisateurs d’entrer une nouvelle recherche en tapant ou de modifier la recherche précédente en positionnant le signe insertion à l’aide des touches de direction.

    ![capture d’écran de la zone de recherche avec le texte en surbrillance ](images/ctrl-search-boxes-image9.png)

    Dans cet exemple, le texte précédemment entré est sélectionné dans le focus d’entrée.

-   **Affectez au raccourci clavier de la zone de recherche la valeur Ctrl + E.**

### <a name="functionality"></a>Fonctionnalités

-   **Prenez en charge la recherche instantanée dans la mesure du possible.** Fournissez des recherches régulières et instantanées s’il existe des scénarios dans lesquels les recherches régulières méritent un temps d’attente supplémentaire.
-   Les recherches régulières doivent retourner des résultats pertinents dans un délai de cinq secondes et la recherche instantanée doit retourner les résultats dans les deux secondes. Après ce stade, la fonction de recherche peut continuer à remplir les résultats moins pertinents dans le temps, tant que le programme est réactif et que les utilisateurs peuvent effectuer d’autres tâches. Vous devrez peut-être indexer vos données de recherche pour garantir cette réactivité.
-   Si vous fournissez des modes de recherche standard et instantanée, les résultats de la recherche instantanée doivent être un sous-ensemble des résultats de recherche standard.
-   Toute la recherche est basée sur un préfixe (aucune recherche de sous-chaîne ou de suffixe). L’utilisation de caractères génériques de fin est facultative et n’affecte pas les résultats. Si plusieurs mots sont entrés, utilisez ou en effectuant une recherche.
-   Une recherche réussie ajoute une page virtuelle avec les résultats de la recherche à la pile de retour et à la barre d’adresses. Si plusieurs recherches génèrent une seule page virtuelle, le fait de cliquer sur précédent retourne toujours la page d’origine.
-   Si nécessaire pour la mise à l’échelle, classez les résultats de la recherche par pertinence.
-   Une recherche vide retourne la page d’origine.

## <a name="recommended-sizing-and-spacing"></a>Dimensionnement et espacement recommandés

![figure du dimensionnement et de l’espacement de la zone de recherche instantanée ](images/ctrl-search-boxes-image10.png)

Dimensionnement et espacement recommandés pour la recherche instantanée.

![figure du dimensionnement et de l’espacement de zone de recherche standard ](images/ctrl-search-boxes-image11.png)

Dimensionnement et espacement recommandés pour la recherche régulière.

## <a name="text"></a>Texte

-   Pour la formulation de l’invite dans la zone de recherche, faites-en une instruction (par exemple, tapez pour rechercher) ou indiquez l’étendue de la recherche (par exemple, recherchez des images).
-   Le texte de l’invite doit être Brief. Un mot unique ou une phrase brève doit suffire.
-   Utilisez les majuscules comme pour les phrases.
-   N’utilisez pas de ponctuation de fin ni de points de suspension.

## <a name="documentation"></a>Documentation

-   Reportez-vous à ce contrôle en tant que zone de recherche. Mettre en majuscule la première lettre du premier mot ; ne mettez pas en majuscule la première lettre de la zone.
-   Reportez-vous aux deux types de recherche en tant que recherche instantanée et recherche régulière. Mettre en majuscule la première lettre de la recherche instantanée ; ne mettez pas en majuscule la première lettre de la recherche régulière.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Glossaire](glossary.md)
</dt> </dl>

 

 