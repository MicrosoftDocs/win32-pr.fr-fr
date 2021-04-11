---
title: Barres d’État (notions de base sur la conception)
description: Une barre d’État est une zone en bas d’une fenêtre principale qui affiche des informations sur l’état de la fenêtre active (par exemple, ce qui est affiché et comment), les tâches en arrière-plan (telles que l’impression, l’analyse et la mise en forme), ou d’autres informations contextuelles (telles que la sélection et l’état du clavier).
ms.assetid: 09dc03d9-d730-4f03-86a8-7b39d9a55369
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 8f65d104f59cd0aec0c242d623f83c410c22f48d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104211183"
---
# <a name="status-bars-design-basics"></a>Barres d’État (notions de base sur la conception)

> [!NOTE]
> Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Une barre d’État est une zone en bas d’une fenêtre principale qui affiche des informations sur l’état de la fenêtre active (par exemple, ce qui est affiché et comment), les tâches en arrière-plan (telles que l’impression, l’analyse et la mise en forme), ou d’autres informations contextuelles (telles que la sélection et l’état du clavier).

Les barres d’État indiquent généralement l’État par le biais du texte et des icônes, mais elles peuvent également avoir des indicateurs de progression, ainsi que des menus pour les commandes et les options relatives à l’État.

![capture d’écran de la barre d’état standard ](images/ctrl-status-bars-image1.png)

Barre d’état standard.

> [!Note]  
> Les instructions relatives à la [zone de notification](winenv-notification.md) sont présentées dans un article distinct.

 

## <a name="is-this-the-right-user-interface"></a>S’agit-il de l’interface utilisateur appropriée ?

Pour vous décider, posez-vous les questions suivantes :

-   **L’État est-il pertinent lorsque les utilisateurs utilisent activement d’autres programmes ?** Dans ce cas, utilisez une [icône de zone de notification](winenv-notification.md).
-   **L’élément d’État a-t-il besoin d’afficher des notifications ?** Si c’est le cas, vous devez utiliser une icône de zone de notification.
-   **La fenêtre est-elle une fenêtre principale ?** Si ce n’est pas le cas, n’utilisez pas de barre d’État. Les boîtes de dialogue, les assistants, les panneaux de contrôle et les feuilles de propriétés ne doivent pas avoir de barres d’État.
-   **Les informations sont-elles principalement l’État ?** Si ce n’est pas le cas, n’utilisez pas de barre d’État. Les barres d’État ne doivent pas être utilisées comme une [barre de menus](cmd-menus.md) ou une [barre d’outils](cmd-toolbars.md)secondaire.
-   **Les informations expliquent-elles comment utiliser le contrôle sélectionné ?** Dans ce cas, affichez les informations en regard du contrôle associé à l’aide d’une explication supplémentaire ou d’une étiquette d’instruction à la place.
-   **L’État est-il utile et pertinent ? Autrement dit, les utilisateurs risquent-ils de modifier leur comportement en raison de ces informations ?** Si ce n’est pas le cas, n’affichez pas l’État ou placez-le dans un fichier journal.
-   **L’État est-il critique ? L’action immédiate est-elle nécessaire ?** Dans ce cas, affichez les informations dans un formulaire qui requiert votre attention et qui ne peut pas être ignoré facilement, comme une [boîte de dialogue](win-dialog-box.md) ou dans la fenêtre principale elle-même.

    ![capture d’écran de la barre d’État « erreur de certificat » rouge ](images/ctrl-status-bars-image2.png)

    Barre d’adresses rouge dans Windows Internet Explorer.

-   **Le programme est-il principalement destiné aux utilisateurs débutants ?** Les utilisateurs inexpérimentés ne connaissant généralement pas les barres d’État, reconsidérez l’utilisation des barres d’État dans ce cas.

## <a name="design-concepts"></a>Principes de conception

Les barres d’État sont un excellent moyen de fournir des informations d’État sans interrompre les utilisateurs ou rompre leur Flow. Toutefois, les barres d’État sont faciles à ignorer. C’est pourquoi, en fait, beaucoup d’utilisateurs ne remarquent pas du tout des barres d’État.

La solution à ce problème n’est pas de demander l’attention de l’utilisateur à l’aide d’icônes criarde, d’animation ou de clignotement, mais de la conception de cette limitation. Pour ce faire, vous pouvez :

-   **S’assurer que les informations d’État sont utiles et pertinentes.** Si ce n’est pas le cas, ne fournissez pas de barre d’État.
-   **N’utilisez pas de barres d’État pour obtenir des informations essentielles.** Les utilisateurs ne doivent jamais savoir ce qui se trouve dans la barre d’État. Si les utilisateurs doivent le voir, ne le placez pas dans une barre d’État.

**Si vous n’avez qu’une seule chose...**

Assurez-vous que les informations sur la barre d’État sont utiles et pertinentes, mais pas essentielles.

## <a name="usage-patterns"></a>Modèles d’usage

Les barres d’État ont plusieurs modèles d’utilisation :



|                                                                                                                                    |                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **État de la fenêtre active**<br/> Afficher la source de ce qui est affiché avec tous les modes d’affichage <br/>              | ![capture d’écran d’une barre d’État « emplacement » ](images/ctrl-status-bars-image3.png)<br/> Dans cet exemple, la barre d’état affiche le chemin d’accès au document.<br/>                                                         |
| **Progression**<br/> Affiche la progression des tâches en arrière-plan, soit avec une barre de progression ou une animation arrêtée. <br/> | ![capture d’écran de la barre d’État avec la barre de progression ](images/ctrl-status-bars-image4.png)<br/> Dans cet exemple, la barre d’État comprend une barre de progression pour afficher le chargement de la page Web dans une fenêtre Internet Explorer.<br/> |
| **Informations contextuelles**<br/> Affichez des informations contextuelles sur ce que l’utilisateur fait actuellement. <br/>              | ![capture d’écran de la barre d’état montrant le nombre de pixels ](images/ctrl-status-bars-image5.png)<br/> Dans cet exemple, Microsoft Paint affiche la taille de la sélection en pixels.<br/>                                           |



 

## <a name="guidelines"></a>Consignes

### <a name="general"></a>Général

-   Envisagez de fournir une commande Afficher la barre d’État si seuls certains utilisateurs auront besoin des informations sur la barre d’État. Masque la barre d’État par défaut si la plupart des utilisateurs n’en ont pas besoin.
-   N’utilisez pas la barre d’État pour expliquer les éléments de barre de menus. Ce modèle d’aide n’est pas détectable.

### <a name="presentation"></a>Présentation

-   Désactivez l’État modal qui ne s’applique pas. L’État modal comprend les États du clavier et du document.
-   Supprimez l’état non modal qui ne s’applique pas.
-   Présenter les informations d’État dans l’ordre suivant : état de la fenêtre active ; avancement et des informations contextuelles.

### <a name="icons"></a>Icônes

-   Choisissez des conceptions d’icônes d’État facilement reconnaissables. Préférer les icônes avec des contours uniques sur les icônes de forme carrée ou rectangulaire.
-   Utilisez la quantités du rouge pur, du jaune et du vert uniquement pour communiquer les informations d’État. Dans le cas contraire, ces icônes sont confuses.

    **Correct :**

    ![capture d’écran de la barre d’État avec des icônes bleues ](images/ctrl-status-bars-image6.png)

    **Incorrect :**

    ![capture d’écran de la barre d’État avec une icône rouge ](images/ctrl-status-bars-image7.png)

    Dans l’exemple incorrect, l’icône rouge suggère involontairement une erreur, créant une confusion.

-   Utilisez des variantes d’icône ou des superpositions pour indiquer l’État ou les changements d’État. Utilisez les variations d’icône pour afficher les modifications de quantités ou de forces. Pour les autres types d’État, utilisez ces superpositions standard : 

    |                                                                                               |                                  |
    |-----------------------------------------------------------------------------------------------|----------------------------------|
    | **Overlay**<br/>                                                                        | **État**<br/>            |
    | ![capture d’écran de l’icône d’avertissement ](images/ctrl-status-bars-image8.png)<br/>                | Avertissement<br/>               |
    | ![capture d’écran de l’icône d’erreur ](images/ctrl-status-bars-image9.png)<br/>                  | Error<br/>                 |
    | ![capture d’écran de l’icône désactivée/déconnectée ](images/ctrl-status-bars-image10.png)<br/> | Désactivé/déconnecté<br/> |
    | ![capture d’écran de l’icône bloquée/hors connexion ](images/ctrl-status-bars-image11.png)<br/>       | Bloqué/hors connexion<br/>       |

    

     

-   Ne modifiez pas l’État trop fréquemment. Les icônes de la barre d’État ne doivent pas apparaître comme bruyants, instables ou à la demande. L’œil étant sensible aux modifications apportées au champ de vision du périphérique, les changements d’État doivent être subtils.
-   Pour les icônes qui fournissent des informations d’État importantes, préférez des étiquettes sur place.
-   Les icônes de la barre d’État sans étiquette doivent avoir des info-bulles.

Pour plus d’informations, consultez [icônes](vis-icons.md).

### <a name="interaction"></a>Interaction

-   Créer une zone de barre d’État interactive pour permettre aux utilisateurs d’accéder directement aux commandes et options associées.
    -   Utilisez un contrôle qui ressemble et se comporte comme un [bouton de menu](ctrl-command-buttons.md) ou un bouton partagé. Ces zones de barre d’État doivent avoir une flèche déroulante pour indiquer qu’elles sont interactives.
    -   Affichez le menu en cliquant avec le bouton gauche sur souris enfoncé, et non pas sur la souris.
    -   Ne prenez pas en charge le clic droit ou le double-clic. Les utilisateurs n’attendent pas ces interactions dans une barre d’État, donc ils ne peuvent pas les essayer.
-   Affichez les info-bulles au survol.

## <a name="text"></a>Texte

-   En règle générale, utilisez des étiquettes concises. Coupez tout texte qui peut être éliminé.
-   Préférer des fragments de phrase, sans ponctuation finale. Utilisez des phrases entières (avec ponctuation de fin) uniquement lorsque les fragments de phrase ne sont pas beaucoup plus courts.
-   Pour les étiquettes de progression facultatives, indiquez ce que fait l’opération avec une étiquette qui commence par un verbe (formulaire gerund) et se termine par des points de suspension. Par exemple : « copie... ». Cette étiquette peut changer dynamiquement si l’opération comporte plusieurs étapes ou s’il traite plusieurs objets.
-   N’utilisez pas la couleur, le gras ou l’italique pour mettre en surbrillance le texte de la barre d’État.
-   Pour obtenir des indications sur les formulations d’info-bulle, consultez [info-bulles et info-bulles](ctrl-tooltips-and-infotips.md).

## <a name="documentation"></a>Documentation

Reportez-vous aux barres d’État sous forme de barres d’État, de lignes d’État et d’autres variations. Exemple : « le numéro de page actuel est affiché dans la barre d’État. »

 

