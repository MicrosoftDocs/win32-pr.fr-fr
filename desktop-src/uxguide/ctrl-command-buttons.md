---
title: Boutons de commande
description: Avec un bouton de commande, les utilisateurs lancent une action immédiate.
ms.assetid: 0e2ff31a-657b-4e4c-afee-2a6bd742f46c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 32c8c16cef275e1fefe44e579105515d3e61c497
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "103761294"
---
# <a name="command-buttons"></a>Boutons de commande

> [!NOTE]
> Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Avec un bouton de commande, les utilisateurs lancent une action immédiate.

![capture d’écran du bouton de commande OK ](images/ctrl-command-buttons-image1.png)

Bouton de commande standard.

Le bouton de commande par défaut est appelé quand les utilisateurs appuient sur la touche entrée. Il est assigné par le développeur, mais n’importe quel bouton de commande devient la valeur par défaut lorsque l’onglet utilisateurs y est associé.

> [!Note]  
> Les instructions relatives à la [disposition](vis-layout.md) sont présentées dans un article distinct.

 

## <a name="is-this-the-right-control"></a>Est-ce le contrôle approprié ?

Pour vous décider, posez-vous les questions suivantes :

-   **Le bouton de commande est-il utilisé pour lancer une action immédiate ?** Si ce n’est pas le cas, utilisez un autre contrôle.
-   **Un lien serait-il un meilleur choix ?** Utilisez un lien si :
    -   L’action consiste à accéder à une autre page, fenêtre ou rubrique d’aide. **Exception**: la navigation dans l’Assistant utilise les boutons de commande précédent et suivant.
    -   La commande est incorporée dans un corps de texte.
    -   La commande est secondaire par nature. Autrement dit, il n’est pas lié à l’objectif principal de la fenêtre. Dans ce cas, un lien ou un bouton de commande léger est approprié.
    -   La commande fait partie d’un menu ou d’un groupe de liens connexes.
    -   L’étiquette est longue, composée de cinq mots ou plus, donnant ainsi un aspect maladroit à un bouton de commande.
-   **Une combinaison de cases d’option et de boutons de commande génériques peut-elle être un meilleur choix ?** Les cases d’option sont souvent utilisées conjointement avec les boutons de commande génériques (OK, annuler) à la place d’un ensemble de boutons de commande spécifiques lorsque l’une des conditions suivantes est vraie :
    -   Il existe au moins cinq actions possibles.
    -   Les utilisateurs doivent afficher des informations supplémentaires avant de prendre une décision.
    -   Les utilisateurs doivent interagir avec les choix (par exemple, pour afficher des informations supplémentaires) avant de prendre une décision.
    -   Les utilisateurs affichent les choix en tant qu’options au lieu de commandes différentes.

        **Correct :** ![ capture d’écran de la boîte de dialogue, des cases d’option et du texte ](images/ctrl-command-buttons-image2.png)

        Dans cet exemple, les cases d’option sont combinées avec les boutons OK et annuler pour fournir des informations supplémentaires sur les options.

        **Incorrect :** ![ capture d’écran d’un message avec des boutons de commande ](images/ctrl-command-buttons-image3.png)

        Dans cet exemple, les boutons de commande ne compliquent que les utilisateurs à prendre une décision informée.

## <a name="design-concepts"></a>Principes de conception

**Utilisation de ellipses**

Alors que les boutons de commande sont utilisés pour les actions immédiates, des informations supplémentaires peuvent être nécessaires pour exécuter l’action. **Indiquez une commande qui nécessite des informations supplémentaires (y compris la confirmation) en ajoutant des points de suspension à la fin de l’étiquette du bouton**.

![capture d’écran du bouton de commande imprimer avec des ellipses ](images/ctrl-command-buttons-image4.png)

Dans cet exemple, la page... commande affiche une boîte de dialogue Imprimer pour recueillir plus d’informations.

![capture d’écran du bouton de commande Imprimer, pas de ellipse ](images/ctrl-command-buttons-image5.png)

En revanche, dans cet exemple, la commande Imprimer imprime une seule copie d’un document sur l’imprimante par défaut sans aucune autre intervention de l’utilisateur.

L' **utilisation correcte des ellipses est importante pour indiquer que les utilisateurs peuvent effectuer des choix supplémentaires avant d’effectuer l’action, ou même annuler complètement l’action**. Le signal visuel fourni par des points de suspension permet aux utilisateurs d’explorer vos logiciels sans crainte.

**Cela ne signifie pas que vous devez utiliser des points de suspension chaque fois qu’une action affiche une autre fenêtre** uniquement lorsque des informations supplémentaires sont requises pour effectuer l’action. Par conséquent, **n’importe quel bouton de commande dont le verbe implicite est « afficher une autre fenêtre » ne prend pas de points de suspension**, comme avec les commandes à propos de, avancé, aide (ou tout autre lien de commande vers une rubrique d’aide), des options, des propriétés ou des paramètres.

En règle générale, les ellipses sont utilisées dans les interfaces utilisateur pour indiquer l’inexhaustivité. Les commandes qui affichent d’autres fenêtres ne sont pas incomplètes. elles doivent afficher une autre fenêtre et des informations supplémentaires ne sont pas nécessaires pour effectuer leur action. Cette approche élimine l’encombrement à l’écran dans les situations où les ellipses ont peu de valeur.

**Remarque :** Lorsque vous déterminez si un bouton de commande a besoin de points de suspension, n’utilisez pas le besoin d' [élever les privilèges](winenv-uac.md) en tant que facteur. L’élévation n’est pas nécessaire pour exécuter une commande (au lieu de cela, il s’agit d’une autorisation) et le besoin d’élévation est indiqué par la protection de la sécurité.

**Si vous n’avez qu’une seule chose...** Utilisez une étiquette concise, spécifique et concise qui décrit clairement l’action effectuée par le bouton de commande et utilisez des points de suspension quand cela est approprié.

## <a name="usage-patterns"></a>Modèles d’usage

Les boutons de commande ont plusieurs modèles d’utilisation :



|                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Boutons de commande standard** Vous pouvez utiliser les boutons de commande standard pour lancer une action immédiate.<br/>                                                           | ![capture d’écran du bouton de commande standard (gris) ](images/ctrl-command-buttons-image6.png)<br/> Bouton de commande standard.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Boutons de commande par défaut** Le bouton de commande par défaut dans une fenêtre indique le bouton de commande qui sera activé lorsque les utilisateurs appuient sur la touche entrée.<br/>       | ![capture d’écran du bouton de commande par défaut (bleu) ](images/ctrl-command-buttons-image7.png)<br/> Bouton de commande par défaut.<br/> Un bouton de commande devient la valeur par défaut lorsque l’utilisateur clique sur l’onglet utilisateurs. Si le focus d’entrée se trouve sur un contrôle qui n’est pas un bouton de commande, le bouton de commande avec l’attribut de bouton par défaut devient la valeur par défaut. Un seul bouton de commande dans une fenêtre peut être la valeur par défaut.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Boutons de commande légers** Un bouton de commande léger est similaire à un bouton de commande standard, sauf que son cadre de bouton s’affiche uniquement au pointage de la souris. <br/> | ![capture d’écran de l’un des deux boutons d’impression sélectionnés ](images/ctrl-command-buttons-image8.png)<br/> Dans cet exemple, la commande a une apparence très légère (semblable à un [lien](ctrl-links.md)) jusqu’à ce que l’utilisateur pointe sur la commande, à partir de laquelle il est dessiné à l’aide d’un cadre de bouton.<br/> Vous pouvez utiliser des boutons de commande légers dans les cas où vous utilisez un bouton de commande standard, mais vous souhaitez éviter d’avoir toujours affiché le cadre du bouton. Les boutons de commande légers sont idéaux pour les commandes que vous souhaitez souligner et l’utilisation d’un lien n’est pas appropriée.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Boutons de menu** Utilisez un bouton de menu lorsque vous avez besoin d’un menu pour un petit ensemble de commandes associées.<br/>                                                                 | ![capture d’écran du bouton de menu Format et de ses commandes ](images/ctrl-command-buttons-image9.png)<br/> Bouton de menu avec un petit ensemble de commandes associées.<br/> Utilisez un bouton de menu quand une barre de menus est indésirable, par exemple dans une boîte de dialogue, une barre d’outils ou une autre fenêtre qui n’a pas de barre de menus. Un triangle pointant vers le bas indique que lorsque vous cliquez sur le bouton, un menu s’affiche.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Boutons partagés** Utilisez un bouton partagé pour consolider un ensemble de variations d’une commande, en particulier lorsque l’une des commandes est utilisée la plupart du temps.<br/>          | ![capture d’écran du bouton Ouvrir le fractionnement sans commande ](images/ctrl-command-buttons-image10.png)<br/> bouton partagé réduit.<br/> à l’instar d’un bouton de menu, un seul triangle pointant vers le bas indique que cliquer sur la partie la plus à droite du bouton entraîne la suppression d’un menu.<br/> ![capture d’écran du bouton Ouvrir Split avec des commandes ](images/ctrl-command-buttons-image11.png)<br/> bouton partagé déplacé.<br/> dans cet exemple, un bouton partagé est utilisé pour consolider six variantes de la commande Open. la commande Open standard est utilisée la plupart du temps, de sorte que les utilisateurs n’ont généralement pas besoin de voir les autres commandes. l’utilisation d’un bouton partagé permet d’économiser une quantité importante d’espace à l’écran, tout en fournissant des choix puissants.<br/> Contrairement à un bouton de menu, le fait de cliquer sur la partie gauche du bouton effectue l’action directement sur l’étiquette. les boutons fractionnés sont efficaces dans les situations où l’action suivante avec un outil spécifique est susceptible d’être identique à la dernière action. dans ce cas, l’étiquette est remplacée par la dernière action, comme avec un sélecteur de couleurs :<br/> ![capture d’écran du bouton remplir le fractionnement sans commande ](images/ctrl-command-buttons-image12.png)<br/> Dans cet exemple, l’étiquette est remplacée par la dernière action.<br/> |
| **Boutons Parcourir** Utilisez un bouton Parcourir pour afficher une boîte de dialogue qui permet aux utilisateurs de sélectionner une valeur valide.<br/>                                                           | les boîtes de dialogue lancées par un bouton Parcourir aident les utilisateurs à sélectionner des fichiers, des dossiers, des ordinateurs, des utilisateurs, des couleurs, etc. ils sont généralement combinés avec un contrôle sans contrainte, tel qu’une zone de texte. elles sont généralement nommées parcourir, autres, ou plus, et ont toujours des points de suspension pour indiquer que des informations supplémentaires sont requises. <br/> ![capture d’écran de la zone de texte avec le bouton Parcourir ](images/ctrl-command-buttons-image13.png)<br/> une zone de texte avec un bouton Parcourir.<br/> pour les fenêtres qui possèdent de nombreux boutons Parcourir, vous pouvez utiliser une version abrégée :<br/> ![capture d’écran d’un bouton de navigation rapide avec ellipses ](images/ctrl-command-buttons-image14.png)<br/> Bouton de navigation rapide.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Boutons de divulgation progressive** Utilisez un bouton de divulgation progressive pour afficher ou masquer les options rarement utilisées.<br/>                                            | le masquage des options rarement utilisées jusqu’à ce qu’elles soient nécessaires est appelé Divulgation progressive. les guillemets doubles sont utilisés pour indiquer la divulgation progressive, et ils pointent dans la direction dans laquelle la révélation ou le masquage aura lieu : <br/> ![capture d’écran du bouton avec les flèches vers la droite et la droite ](images/ctrl-command-buttons-image15.png)<br/> une fois que vous avez cliqué sur le bouton, son étiquette change pour indiquer que le clic suivant aura l’effet inverse :<br/> ![capture d’écran du bouton avec les flèches’inférieur’et gauche ](images/ctrl-command-buttons-image16.png)<br/> Pour plus d’informations et d’exemples, consultez [contrôles de divulgation progressif](ctrl-progressive-disclosure-controls.md). <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Boutons directionnels** Utilisez un bouton directionnel pour indiquer la direction dans laquelle une action aura lieu.<br/>                                               | dans ce cas, un chevron simple est utilisé à la place d’un double Chevron : <br/> ![capture d’écran des boutons de direction droite et gauche ](images/ctrl-command-buttons-image17.png)<br/> Un bouton directionnel indique la direction de l’action.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="guidelines"></a>Consignes

### <a name="general"></a>Général

-   **Afficher un pointeur occupé si le résultat d’un clic sur un bouton de commande n’est pas instantané.** Sans commentaires, les utilisateurs peuvent supposer que le clic n’a pas eu lieu et cliquer à nouveau sur.
-   Si le même bouton de commande apparaît dans plusieurs fenêtres, **essayez d’utiliser le même texte d’étiquette et la même clé d’accès, et recherchez-le à peu près au même endroit dans chaque fenêtre lorsque cela est possible.**
-   **Pour les boutons de commande avec des étiquettes de texte, utilisez une largeur de bouton minimale et la hauteur du bouton de commande standard.** Pour plus d’informations, consultez [dimensionnement et espacement recommandés](#recommended-sizing-and-spacing).
-   Pour chaque fenêtre, **faites en sorte que les boutons de commande aient la même largeur**. Si ce n’est pas pratique, limitez le nombre de différentes largeurs pour les boutons de commande avec des étiquettes de texte à deux.
-   Lorsqu’un autre contrôle interagit avec un bouton de commande, tel qu’une zone de texte avec un bouton Parcourir, **Indiquez la relation en plaçant le bouton de commande à l’un des trois emplacements suivants :**
    -   À droite et aligné en haut avec l’autre contrôle.
    -   Sous et alignés à gauche avec l’autre contrôle.
    -   Centré verticalement entre les contrôles qui interopèrent (tels que les boutons ajouter et supprimer entre deux zones de liste d’interopérabilité).
-   Si plusieurs boutons de commande interagissent avec le même contrôle, **les empilent verticalement à droite et alignés en haut avec l’autre contrôle, ou les placent horizontalement à gauche sous le contrôle.**
-   Lorsque les boutons de commande sont subordonnés à d’autres contrôles, **Utilisez l’emplacement ci-dessus et désactivez le bouton de commande subordonné jusqu’à ce que le contrôle supérieur soit sélectionné.**
-   **N’utilisez pas de boutons de commande étroits, courts ou longs avec des étiquettes de texte** , car ils ont tendance à paraître non professionnels. Essayez d’utiliser les largeurs et hauteurs par défaut.

**Correct :** ![ capture d’écran du bouton de taille par défaut OK ](images/ctrl-command-buttons-image18.png)

Dans cet exemple, la taille du bouton est standard et semble Professional.

**Incorrect :** ![ capture d’écran du bouton abrégé OK ](images/ctrl-command-buttons-image19.png)

Dans cet exemple, le bouton est trop petit.

**Incorrect :** ![ capture d’écran du bouton OK de grande taille ](images/ctrl-command-buttons-image20.png)

Dans cet exemple, le bouton a trop d’espace autour de l’étiquette.

-   **Évitez de combiner des étiquettes de texte et des graphiques sur les boutons de commande.** La combinaison de texte et de graphiques ajoute généralement un encombrement visuel inutile et n’améliore pas la compréhension de l’utilisateur. Envisagez de combiner du texte et des graphiques uniquement lorsque le graphique contribue à la compréhension, par exemple lorsqu’il s’agit d’un symbole standard pour la commande ou qu’il aide les utilisateurs à visualiser les résultats de la commande. Sinon, préférez du texte, mais utilisez du texte ou des graphiques.

**Correct :** ![ capture d’écran de la commande pivot avec une flèche courbée ](images/ctrl-command-buttons-image21.png)

Dans cet exemple, le graphique en forme de flèche aide les utilisateurs à visualiser les résultats de la commande.

**Correct :** ![ capture d’écran de la barre d’adresses avec des icônes et du texte ](images/ctrl-command-buttons-image22.png)

Dans cet exemple, les symboles standard sont combinés au texte pour faciliter la compréhension

**Incorrect :** ![ capture d’écran du bouton avec l’icône x et annuler ](images/ctrl-command-buttons-image23.png)

Dans cet exemple, le graphique Cancel n’ajoute rien au texte.

-   **N’utilisez pas de boutons de commande pour définir l’État**. Utilisez des cases d’option ou des cases à cocher à la place. Les boutons de commande sont uniquement destinés aux actions de lancement.

### <a name="split-buttons"></a>Boutons partagés

-   **Définissez la commande la plus probable comme comportement par défaut**. S’il existe plusieurs commandes probables, choisissez-en une qui ne nécessite pas d’informations supplémentaires.
-   **Si la commande la plus probable est la dernière sélection de l’utilisateur, remplacez l’étiquette du bouton par la dernière sélection.**
-   **Affichez la commande par défaut en gras dans le menu**. Cela permet aux utilisateurs de trouver plus facilement la commande par défaut, en particulier lorsque la commande par défaut est dynamique ou lorsque le bouton partagé utilise un graphique au lieu d’une étiquette de texte.

### <a name="default-values"></a>Valeurs par défaut

-   Ajoutez un bouton de commande par défaut dans chaque boîte de dialogue. **Sélectionnez le niveau de sécurité le plus sûr (pour empêcher la perte de données ou l’accès au système) et la commande la plus sécurisée est la valeur par défaut**. Si la sécurité et la sécurité ne sont pas des facteurs, sélectionnez la commande la plus probable ou la plus pratique.
-   **Ne définissez pas une action destructrice sur le bouton de commande par défaut** , sauf si vous avez un moyen simple d’annuler la commande.

## <a name="recommended-sizing-and-spacing"></a>Dimensionnement et espacement recommandés

![diagramme des dimensions de bouton en pixels et de dlu ](images/ctrl-command-buttons-image24.png)

Dimensionnement et espacement recommandés pour les boutons de commande.

## <a name="labels"></a>Étiquettes

-   Étiquetez chaque bouton de commande.
-   Si le bouton a une étiquette graphique uniquement, affectez sa propriété Name à une étiquette de texte appropriée. Cela permet aux produits de technologie d’assistance tels que les lecteurs d’écran de fournir aux utilisateurs des informations alternatives sur le graphique.

    ![capture d’écran des boutons monter, descendre et copier ](images/ctrl-command-buttons-image25.png)

    Cet exemple montre les boutons graphiques. en interne, ces boutons sont étiquetés précédent, suivant et copier.

-   Pour les boutons de navigation courts (étiquetés « ... »), l’étiquette interne doit être Browse.
-   Attribuez une [clé d’accès](glossary.md)unique. Pour obtenir des instructions, consultez [clavier](inter-keyboard.md).

    **Exceptions :**

    -   N’affectez pas de touches d’accès aux boutons OK et annuler, car la touche entrée est la touche d’accès pour le bouton par défaut (qui est généralement le bouton OK) et la touche Échap est la touche d’accès pour annuler. Cela rend les autres clés d’accès plus faciles à assigner.
    -   N’affectez pas de touches d’accès rapide à des boutons de navigation courts (étiquetés « ... »), car ils ne peuvent pas être attribués de manière unique.

-   Préférer des étiquettes spécifiques à des étiquettes génériques. Idéalement, les utilisateurs ne doivent pas lire d’autres éléments pour comprendre l’étiquette. Les utilisateurs sont beaucoup plus susceptibles de lire des étiquettes de bouton de commande que du texte statique.

    -   **Exception :** Ne renommez pas le bouton Annuler si la signification de l’annulation n’est pas ambiguë. Les utilisateurs ne doivent pas avoir à lire tous les boutons pour déterminer le bouton qui annule une action. Toutefois, renommez annuler s’il n’est pas clair que l’action est annulée, par exemple lorsqu’il y a plusieurs actions en attente.

    **Acceptable:**

    ![Capture d’écran montrant les boutons OK et annuler.](images/ctrl-command-buttons-image26.png)

    Dans cet exemple, OK et annuler sont des étiquettes acceptables, mais non spécifiques.

    **Conseillé**

    ![capture d’écran des boutons de gravure de CD et d’annulation ](images/ctrl-command-buttons-image27.png)

    Dans cet exemple, la gravure de CD est plus spécifique que OK.

    **Incorrect :**

    ![capture d’écran des boutons CD de gravure et ne pas graver ](images/ctrl-command-buttons-image28.png)

    Dans cet exemple, Cancel doit être utilisé au lieu de ne pas graver de CD.

-   Démarrer des étiquettes avec un verbe impératif et décrire clairement l’action effectuée par le bouton. N’utilisez pas de ponctuation finale.
    -   **Exception :** Les étiquettes standard suivantes sont acceptables sans verbes : avancé, précédent, détails, suivant, moins, plus, nouveau, suivant, non, OK, options, précédent, propriétés, paramètres et oui.
-   Bien que les étiquettes courtes soient préférées, utilisez suffisamment de texte pour expliquer suffisamment la commande. Utilisez un objet direct (un nom après le verbe) lorsque l’objet n’est pas visible à partir du contexte. Idéalement, les utilisateurs ne doivent pas lire d’autres éléments pour comprendre l’étiquette.

    **Acceptable:**

    ![capture d’écran du bouton avec ajouter une étiquette ](images/ctrl-command-buttons-image29.png)

    Dans cet exemple, une étiquette abrégée est acceptable si sa signification en contexte est facilement visible.

    **Mieux :** (si ajouter n’est pas clair)

    ![capture d’écran du bouton avec l’étiquette Ajouter des éléments ](images/ctrl-command-buttons-image30.png)

    Dans cet exemple, l’ajout d’un nom au verbe contribue à la compréhension des utilisateurs.

    **Meilleure :** (si l’ajout ou l’ajout d’éléments n’est pas clair)

    ![capture d’écran du bouton avec ajouter les éléments sélectionnés ](images/ctrl-command-buttons-image31.png)

    Dans cet exemple, l’étiquette est explicite.

-   Utilisez la mise [en majuscules de style phrase](glossary.md). Cela est plus approprié pour Windows [Tone](text-style-tone.md)[tonal](https://msdn.microsoft.com/library/windows/desktop/aa974175.aspx) et l’utilisation de courtes expressions pour les boutons de commande.
    -   **Exception :** Pour les applications héritées, vous pouvez utiliser la mise en [majuscules de style titre](glossary.md) si nécessaire pour éviter de mélanger les styles de mise en majuscules.
-   N’utilisez pas maintenant dans les étiquettes de bouton de commande car le caractère immédiat de la commande peut être pris pour l’autorisation.

    -   **Exception :** Si nécessaire, utilisez-les maintenant pour différencier les commandes qui démarrent une tâche des commandes qui exécutent immédiatement une tâche.

    ![capture d’écran du bouton avec l’étiquette de téléchargement ](images/ctrl-command-buttons-image32.png)

    Dans cet exemple, le fait de cliquer sur le bouton de commande permet d’accéder à une fenêtre ou une page qui permet aux utilisateurs de télécharger.

    ![capture d’écran du bouton avec l’étiquette Télécharger maintenant ](images/ctrl-command-buttons-image33.png)

    Dans cet exemple, le fait de cliquer sur le bouton de commande effectue le téléchargement.

    Une seule commande dans un workflow de tâches doit être étiquetée avec maintenant. Ainsi, par exemple, une commande **Download Now** ne doit jamais être suivie d’une autre commande **Download Now** .

-   N’utilisez pas ultérieurement dans les étiquettes de bouton de commande si elle implique une action qui ne se produira pas. Par exemple, n’utilisez pas installer plus tard (contrairement à l’option Installer maintenant) à moins que cette commande ne s’installe ultérieurement. Utilisez plutôt l’installation ou l’annulation.

    **Incorrect :**

    ![capture d’écran du redémarrage maintenant et du redémarrage ultérieur ](images/ctrl-command-buttons-image34.png)

    Dans cet exemple, le redémarrage ultérieur implique de manière incorrecte que la commande redémarre automatiquement à un moment ultérieur.

-   Utilisez un bouton Avancé uniquement pour les options qui sont pertinentes pour les utilisateurs expérimentés ou qui nécessitent une connaissance avancée des utilisateurs. N’utilisez pas de bouton avancé pour les fonctionnalités qui sont considérées comme technologiques avancées. Par exemple, la fonctionnalité d’agrafage d’une imprimante n’est pas une option avancée, mais son système de gestion des couleurs est.

    **Incorrect :** (si les options ne sont pas vraiment avancées)

    ![capture d’écran du bouton avec l’étiquette avancée ](images/ctrl-command-buttons-image35.png)

    Dans cet exemple, la configuration avancée est trompeuse.

    **Correct :**

    ![capture d’écran du bouton avec plus d’options d’étiquette ](images/ctrl-command-buttons-image36.png)

    Dans cet exemple, l’étiquette est plus spécifique et précise.

-   Pour les boutons de commande qui ouvrent d’autres fenêtres, choisissez une étiquette qui utilise tout ou partie du texte de la barre de titre de la fenêtre secondaire. Par exemple, un bouton de commande intitulé parcourir peut ouvrir une boîte de dialogue intitulée Rechercher un dossier. L’utilisation de la même terminologie tout au long de la tâche permet de garder les utilisateurs orientés.
-   Lorsque vous posez une question, utilisez des étiquettes qui correspondent à la question. N’utilisez pas OK/Annuler pour répondre aux questions oui/non.

    **Correct :**

    ![capture d’écran des boutons Oui et non ](images/ctrl-command-buttons-image37.png)

    Dans cet exemple, les boutons répondent à la question.

    **Incorrect :**

    ![capture d’écran des boutons OK et annuler ](images/ctrl-command-buttons-image38.png)

    Dans cet exemple, les boutons ne répondent pas à la question.

-   Terminez l’étiquette par des points de suspension si la commande nécessite des informations supplémentaires pour s’exécuter.

    -   **Exception :** Les étiquettes graphiques n’acceptent pas de points de suspension.

    **Correct :** (si une boîte de dialogue Options d’impression s’affiche)

    ![capture d’écran du bouton imprimer avec des ellipses ](images/ctrl-command-buttons-image39.png)

    Dans cet exemple, après avoir cliqué sur le bouton, la boîte de dialogue Options d’impression s’affiche et requiert plus d’informations de la part de l’utilisateur.

-   N’utilisez pas de points de suspension lorsque l’exécution de l’action réussit simplement à afficher une autre fenêtre. Les commandes suivantes ne prennent jamais de points de suspension : à propos de, avancé, options, propriétés, aide.

    **Incorrect :**

    ![capture d’écran du bouton options avec ellipses ](images/ctrl-command-buttons-image40.png)

    Dans cet exemple, une fois que vous avez cliqué sur le bouton, la boîte de dialogue Options s’affiche, mais les informations de l’utilisateur ne sont pas requises.

-   En cas d’ambiguïté (par exemple, l’étiquette de commande n’a pas de verbe), choisissez en fonction de l’action utilisateur la plus probable. Si la simple consultation de la fenêtre est une action courante, n’utilisez pas de points de suspension.

    **Correct :**

    Couleurs supplémentaires...

    Informations sur la version

    Dans le premier exemple, les utilisateurs vont probablement choisir une couleur, de sorte que l’utilisation d’une ellipse est correcte. Dans le deuxième exemple, les utilisateurs vont probablement afficher les informations de version, ce qui rend les ellipses inutiles.

-   Pour les boutons de navigation, utilisez des boutons de navigation courts (étiquetés « ... ») lorsqu’il y a plus de deux boutons de navigation dans une fenêtre. Utilisez toujours la version abrégée lorsque vous souhaitez afficher un bouton Parcourir dans une grille.
-   Pour les boutons directionnels, utilisez un chevron simple et faites-le point dans la direction dans laquelle l’action a lieu.

Le tableau suivant présente certaines étiquettes de bouton de commande courantes et leur utilisation.



|                             |                                                                                                              |                             |
|-----------------------------|--------------------------------------------------------------------------------------------------------------|-----------------------------|
| **Étiquette du bouton**<br/> | **Signification**<br/>                                                                                       | **Clé d’accès**<br/>   |
| **Précédent**<br/>         | Dans les assistants et les flux de tâches, accédez à la page précédente.<br/>                                               | 'B'<br/>              |
| **Parcourir...**<br/>    | Affiche une boîte de dialogue pour rechercher un fichier ou un objet.<br/>                                                | « B » ou « r »<br/>       |
| **Options**<br/>      | Affichez les options disponibles pour la personnalisation d’un programme par les utilisateurs.<br/>                                 | 'O'<br/>              |
| **Pause**<br/>        | Dans les boîtes de dialogue en cours, interrompez la tâche.<br/>                                                       | P<br/>              |
| **Personnaliser**<br/>  | Personnaliser une expérience principale cruciale pour l’identification personnelle de l’utilisateur avec un programme.<br/> | P<br/>              |
| **Préférences**<br/>  | N’utilisez pas. Utilisez à la place des options.<br/>                                                                   | Non applicable.<br/>  |
| **Propriétés**<br/>   | Affichez les attributs et les paramètres d’un objet.<br/>                                                | « P » ou « r » en premier<br/> |
| **Save**<br/>         | Enregistrer un groupe de paramètres ou enregistrer un fichier ou un objet en utilisant son nom actuel.<br/>                        | X<br/>              |
| **Enregistrer sous...**<br/>   | Enregistrer un fichier ou un objet à l’aide d’un nom spécifié.<br/>                                                     | Deuxième « a »<br/>       |
| **Paramètres**<br/>     | N’utilisez pas. Utilisez à la place des options.<br/>                                                                   | Non applicable.<br/>  |
| **Résoudre les problèmes**<br/> | N’utilisez pas. Utilisez un lien d’aide spécifique à la place.<br/>                                                      | Non applicable.<br/>  |



 

Pour obtenir des instructions sur les étiquettes de bouton de validation (OK, annuler, oui/non, fermer, arrêter, appliquer, suivant, terminer, terminé), consultez texte de l' [interface utilisateur](text-ui.md).

## <a name="documentation"></a>Documentation

Lorsque vous faites référence à des boutons de commande :

-   Utilisez le texte exact de l’étiquette, y compris sa mise en majuscules, mais n’incluez pas le trait de soulignement ou les points de suspension. N’incluez pas le bouton Word.
-   Pour décrire l’interaction de l’utilisateur, utilisez le clic.
-   Dans la mesure du possible, mettez en forme l’étiquette à l’aide de texte en gras. Sinon, placez l’étiquette entre guillemets uniquement si nécessaire pour éviter toute confusion.

Exemple : cliquez sur **Imprimer** pour imprimer le document.

 

