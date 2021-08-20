---
title: Barre des tâches
description: La barre des tâches est le point d’accès pour les programmes affichés sur le bureau. avec les nouvelles fonctionnalités de la barre des tâches de Windows 7, les utilisateurs peuvent fournir des commandes, accéder aux ressources et afficher l’état du programme directement à partir de la barre des tâches.
ms.assetid: c00e558a-313f-4741-a4b2-7d738f4544fa
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 86b63e5f3b3dc1e8cecba78cbb1599c305d738250d92f76055596226c9028727
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117854106"
---
# <a name="taskbar"></a>Barre des tâches

> [!NOTE]
> ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

La barre des tâches est le point d’accès pour les programmes affichés sur le bureau. avec les nouvelles fonctionnalités de la barre des tâches de Windows 7, les utilisateurs peuvent fournir des commandes, accéder aux ressources et afficher l’état du programme directement à partir de la barre des tâches.

La barre des tâches est le point d’accès pour les programmes affichés sur le bureau, même si le programme est réduit. De tels programmes ont été considérés comme ayant une présence sur le bureau. Avec la barre des tâches, les utilisateurs peuvent afficher les fenêtres primaires ouvertes et certaines fenêtres secondaires sur le bureau, et passer rapidement de l’une à l’autre.

![capture d’écran de la barre des tâches avec les fonctionnalités appelées ](images/winenv-taskbar-image1.png)

la barre des tâches Microsoft Windows.

Les contrôles de la barre des tâches sont appelés boutons de la barre des tâches. lorsqu’un programme crée une fenêtre principale (ou une fenêtre secondaire avec certaines caractéristiques), Windows ajoute un bouton de barre des tâches pour cette fenêtre et le supprime lorsque cette fenêtre se ferme.

les programmes conçus pour Windows 7 peuvent tirer parti de ces nouvelles fonctionnalités de bouton de la barre des tâches :

-   les listes de raccourcis fournissent un accès rapide aux destinations fréquemment utilisées (comme les fichiers, les dossiers et les liens) et aux commandes via un menu contextuel accessible à partir du bouton de la barre des tâches du programme et de menu Démarrer élément même si le programme n’est pas en cours d’exécution.
-   Les barres d’outils miniatures fournissent un accès rapide aux commandes fréquemment utilisées pour une fenêtre particulière. Les barres d’outils miniatures s’affichent dans la miniature du bouton de la barre des tâches.
-   Les icônes de superposition affichent la modification de l’État sur l’icône du bouton de la barre des tâches du programme.
-   Les barres de progression affichent la progression des tâches de longue durée sur le bouton de la barre des tâches du programme.
-   Les boutons de la barre des tâches sous-fenêtre permettent aux utilisateurs d’utiliser des miniatures de bouton de la barre des tâches pour basculer directement vers les onglets de fenêtre, les fenêtres de projet, les fenêtres enfants MDI et les fenêtres secondaires.
-   Les boutons épinglés de la barre des tâches permettent aux utilisateurs d’épingler des boutons de programme à la barre des tâches pour fournir un accès rapide aux programmes même lorsqu’ils ne sont pas exécutés.

Techniquement, la barre des tâches s’étend de la barre entière du bouton Démarrer à la zone de notification. en règle générale, toutefois, la barre des tâches fait uniquement référence à la zone contenant les boutons de la barre des tâches. Pour les configurations à plusieurs moniteurs, une seule analyse a une barre des tâches et cette analyse est l’analyse par défaut.

**Remarque :** Les instructions relatives au [Bureau](winenv-desktop.md), à la [zone de notification](winenv-notification.md)et à la gestion des [fenêtres](win-window-mgt.md) sont présentées dans des articles distincts.

## <a name="is-this-the-right-user-interface"></a>S’agit-il de l’interface utilisateur appropriée ?

les programmes conçus pour Windows 7 peuvent tirer parti de ces fonctionnalités du bouton de barre des tâches. Posez-vous les questions clés suivantes pour déterminer s’il convient ou non de les utiliser :

**Listes de raccourcis**

-   **Les utilisateurs doivent-ils souvent Démarrer de nouvelles tâches à l’aide de votre programme ?** Dans ce cas, envisagez de fournir une liste de raccourcis. Les listes de raccourcis peuvent être utilisées à d’autres fins, mais la plupart des scénarios impliquent le démarrage d’une nouvelle tâche.
-   **Les utilisateurs ont souvent besoin d’accéder aux fichiers, dossiers, liens ou autres ressources utilisés récemment ou fréquemment.** Si c’est le cas, envisagez de fournir une liste de raccourcis pour accéder à ces ressources utiles.

    ![capture d’écran de la barre des tâches avec Internet Explorer ](images/winenv-taskbar-image2.png)

    dans cet exemple, Windows Internet Explorer utilise une liste de raccourcis pour présenter les pages fréquemment visitées.

-   **Les utilisateurs ont souvent besoin d’un accès rapide à un petit nombre de commandes de votre programme lors de l’utilisation d’autres programmes, même si votre programme n’est pas en cours d’exécution ?** Dans ce cas, envisagez de fournir une liste de raccourcis avec ces commandes fréquemment utilisées. Ces commandes doivent fonctionner même si votre programme n’est pas en cours d’exécution et doivent s’appliquer à l’ensemble du programme, et non à une fenêtre spécifique. Vous pouvez également fournir une barre d’outils miniatures pour les commandes qui s’appliquent à une fenêtre spécifique.

    ![capture d’écran de la barre des tâches avec pense-bête ](images/winenv-taskbar-image3.png)

    dans cet exemple, l’accessoire de Pense-bêtes permet aux utilisateurs de créer rapidement une note lors de l’utilisation d’autres programmes.

-   **Promouvez-vous des fonctionnalités nouvelles, uniques ou difficiles à trouver ?** Dans ce cas, n’utilisez pas de listes de raccourcis parce qu’elles ne sont pas prévues à cet effet. Au lieu de cela, améliorez la détectabilité de ces commandes directement dans le programme.

**Barres d’outils miniatures**

Toutes les conditions suivantes s’appliquent-elles ?

-   **Les commandes s’appliquent-elles à une fenêtre spécifique ?** Les barres d’outils miniatures sont destinées aux commandes qui s’appliquent aux tâches existantes, tandis que les commandes de liste de raccourcis permettent de démarrer de nouvelles tâches.
-   **Les utilisateurs doivent-ils interagir rapidement avec une tâche en cours d’exécution lors de l’utilisation d’autres programmes ?** Dans ce cas, les barres d’outils miniatures sont un bon choix. Les barres d’outils miniatures peuvent présenter sept commandes au maximum, mais cinq commandes au maximum sont généralement préférées.
-   **Les commandes sont-elles immédiates ?** Autrement dit, les utilisateurs n’ont pas besoin d’une entrée supplémentaire ? Les barres d’outils miniatures doivent avoir des commandes immédiates pour être efficaces, tandis que les listes de raccourcis fonctionnent mieux avec les commandes qui nécessitent une entrée supplémentaire.

    **Incorrect :**

    ![capture d’écran de la barre des tâches avec des fenêtres superposées ](images/winenv-taskbar-image4.png)

    Les commandes qui requièrent des entrées supplémentaires ne fonctionnent pas correctement sur les barres d’outils miniatures.

-   **Les commandes sont-elles directes ?** Autrement dit, les utilisateurs peuvent-ils interagir avec eux à l’aide d’un simple clic ? Les barres d’outils doivent avoir des commandes directes efficaces.
-   **Les commandes sont-elles bien représentées par des icônes ?** Les commandes de la barre d’outils miniatures sont présentées à l’aide d’icônes et non d’étiquettes de texte.

    **Incorrect :**

    ![capture d’écran de la commande miniature avec icône ](images/winenv-taskbar-image5.png)

    Dans cet exemple, la commande n’est pas bien représentée par des icônes.

**Icônes de superposition**

-   **Le programme a-t-il une « présence du Bureau » ?** Si ce n’est pas le cas, utilisez plutôt une icône de zone de notification. dans ce cas, envisagez d’utiliser une icône de superposition au lieu de placer l’état sur l’icône de la zone de notification pour les programmes conçus pour Windows 7. Cela permet de s’assurer que l’icône sera toujours visible (en cas d’utilisation de grandes icônes) et consolide le programme avec son état dans un même emplacement.
-   **L’icône de superposition s’affiche-t-elle temporairement pour afficher un changement d’État ?** Dans ce cas, une icône de superposition peut être appropriée, en fonction des facteurs suivants :
    -   **L’État est-il utile et pertinent lors de l’utilisation d’autres programmes ?** Si ce n’est pas le cas, affichez les informations dans les [barres d’État](ctrl-status-bars.md) du programme ou dans une autre zone d’État du programme.

        ![capture d’écran de la barre d’état de la fenêtre Internet Explorer ](images/winenv-taskbar-image7.png)

        Dans cet exemple, la barre d’État est utilisée car l’État n’est pas utile lors de l’utilisation d’autres programmes.

    -   **L’état indique-t-il la progression ?** Dans ce cas, utilisez la barre de progression du bouton de la barre des tâches à la place.
    -   **L’État est-il critique ? L’action immédiate est-elle nécessaire ?** Dans ce cas, affichez les informations d’une manière qui exige une attention et qui ne peuvent pas être ignorées facilement, par exemple une [boîte de dialogue](win-dialog-box.md).

**Barres de progression**

-   **Les commentaires sur la progression sont-ils utiles et pertinents lors de l’utilisation d’autres programmes ?** Autrement dit, les utilisateurs risquent-ils de surveiller la progression lors de l’utilisation d’autres programmes, et de modifier leur comportement en conséquence ? Un tel état utile et pertinent est généralement affiché à l’aide d’une boîte de dialogue de progression non modale ou d’une page de progression dédiée, mais pas d’un pointeur occupé, d’un indicateur d’activité ou d’une barre de progression sur une barre d’État. Si l’État n’est pas utile lors de l’utilisation d’autres programmes, il vous suffit d’afficher les commentaires de progression directement dans le programme lui-même.

    **Correct :**

    ![capture d’écran de la boîte de dialogue Copier avec la barre de progression ](images/winenv-taskbar-image8.png)

    **Incorrect :**

    ![capture d’écran de la barre de progression sur le bouton de la barre des tâches ](images/winenv-taskbar-image9.png)

    Dans l’exemple incorrect, la barre de progression du bouton de la barre des tâches n’est pas très utile.

-   **La tâche est-elle continue ?** Si la tâche ne se termine jamais, il n’est pas nécessaire d’afficher sa progression. Les analyses antivirus qui ne sont pas lancées par les utilisateurs et l’indexation des fichiers sont des exemples de tâches continues.

    **Incorrect :**

    ![capture d’écran de l’icône de progression d’une tâche continue ](images/winenv-taskbar-image10.png)

    Dans cet exemple, une tâche continue n’a pas besoin d’afficher la progression.

**Barres des tâches de la sous-fenêtre**

-   **Votre programme contient-il des onglets, des fenêtres de projet, des fenêtres MDI enfants ou des fenêtres secondaires que les utilisateurs souhaitent souvent basculer directement ?** Dans ce cas, il peut être approprié d’attribuer à ces fenêtres leurs propres miniatures de boutons de la barre des tâches.

## <a name="design-concepts"></a>Principes de conception

### <a name="using-jump-lists-and-thumbnail-toolbars-effectively"></a>Utilisation efficace des listes de raccourcis et des barres d’outils miniatures

Les listes de raccourcis et les barres d’outils miniatures aident les utilisateurs à accéder aux ressources et à exécuter des commandes plus efficacement. Toutefois, lorsque vous concevez la manière dont votre programme prend en charge ces fonctionnalités, n’améliorez pas l’efficacité de l’octroi. Si les utilisateurs ne peuvent pas prédire avec précision la fonctionnalité qui a la commande dont ils ont besoin, ou si elles doivent vérifier plusieurs emplacements, les utilisateurs finissent par cesser d’utiliser ces fonctionnalités.

Les listes de raccourcis et les barres d’outils miniatures fonctionnent de façon plus efficace quand elles sont :

-   **Clairement différenciées.** Les utilisateurs savent quand Rechercher une destination ou une commande dans une liste de raccourcis, et quand regarder dans une barre d’outils miniatures. Il y a un objectif clair pour chacun d’entre eux, de sorte que les utilisateurs confondent rarement le contenu des deux. En règle générale, les listes de raccourcis sont utilisées pour démarrer de nouvelles tâches, tandis que les barres d’outils miniatures sont utilisées pour interagir avec les tâches en cours d’exécution lors de l’utilisation d’autres programmes.
-   **Adapté.** Les destinations et les commandes proposées sont celles dont les utilisateurs ont besoin. Si les utilisateurs ne sont pas susceptibles d’avoir besoin d’un événement, il n’est pas inclus. N’utilisez pas le nombre maximal d’éléments s’ils ne sont pas nécessaires.
-   **Prédictible.** Les destinations et les commandes proposées sont celles que les utilisateurs s’attendent à trouver. Les utilisateurs doivent rarement regarder dans plusieurs emplacements.
-   **Bien organisé.** Les utilisateurs peuvent trouver ce qu’ils recherchent rapidement. Ils utilisent des étiquettes descriptives mais concises, ainsi que des icônes appropriées pour faciliter la reconnaissance.

Veillez à effectuer des recherches utilisateur pour vous assurer que vous avez le droit. Si vous constatez que vous ne pouvez pas concevoir des listes de raccourcis et des barres d’outils miniatures pour atteindre ces objectifs, envisagez d’en fournir une seule. Il est préférable de disposer d’une méthode prévisible pour fournir des commandes que deux plus confuses.

## <a name="guidelines"></a>Consignes

### <a name="taskbar-buttons"></a>Boutons de la barre des tâches

-   **faites apparaître les types de fenêtres suivants dans la barre des tâches (pour Windows 7, à l’aide d’une miniature de bouton de la barre des tâches) :**
    -   Fenêtres principales (y compris les boîtes de dialogue sans propriétaires)
    -   Feuilles de propriétés
    -   Boîtes de dialogue de progression non modales
    -   Assistants
-   **pour Windows 7, utilisez les miniatures de bouton de la barre des tâches pour regrouper les types de fenêtres suivants avec le bouton de la barre des tâches de la fenêtre principale à partir duquel il a été lancé** Chaque programme (plus précisément, chaque programme perçu comme un programme distinct) doit avoir un seul bouton de la barre des tâches.

    -   Fenêtres secondaires
    -   Onglets de l’espace de travail
    -   Project windows
    -   fenêtres enfants MDI

    **Correct :**

    ![capture d’écran de l’Explorateur Windows et de la barre de progression ](images/winenv-taskbar-image11.png)

    Dans cet exemple, une fenêtre secondaire est regroupée avec le bouton de la barre des tâches de la fenêtre principale.

    **Incorrect :**

    ![capture d’écran de l’Explorateur Windows et du panneau de configuration ](images/winenv-taskbar-image12.png)

    dans cet exemple, le panneau de configuration n’est pas regroupé correctement avec l’explorateur de Windows. Les utilisateurs perçoivent ces derniers comme des programmes distincts.

    **Incorrect :**

    ![capture d’écran du programme, de la barre de progression et d’une barre des tâches ](images/winenv-taskbar-image13.png)

    dans cet exemple, Sauvegarde Windows utilise de manière incorrecte deux boutons de la barre des tâches pour un seul programme.

-   La **restauration d’une fenêtre principale doit également restaurer toutes ses fenêtres secondaires,** même si ces fenêtres secondaires possèdent leurs propres boutons de la barre des tâches. Lors de la restauration, placez les fenêtres secondaires au-dessus de la fenêtre principale.
-   **pour Windows 7, les programmes qui ont normalement une présence sur le bureau peuvent afficher temporairement un bouton de barre des tâches pour afficher l’état.** Procédez ainsi uniquement si votre programme est normalement affiché sur le bureau et que les utilisateurs interagissent fréquemment avec lui. Un programme qui s’exécute normalement sans présence du Bureau doit utiliser son icône de zone de notification, bien qu’il ne soit pas toujours visible.

    **Incorrect :**

    ![capture d’écran du bouton de la barre des tâches du centre de synchronisation Windows ](images/winenv-taskbar-image14.png)

    dans cet exemple, Windows centre de synchronisation utilise incorrectement un bouton temporaire de la barre des tâches pour afficher l’état. Elle doit utiliser son icône de zone de notification à la place.

### <a name="icons"></a>Icônes

-   **Concevez votre icône de programme pour qu’elle s’affiche dans la barre des tâches.** Assurez-vous qu’il est explicite et qu’il reflète sa fonction et la vôtre. Faites-le distinct, rendez-le spécial et assurez-vous qu’il s’affiche correctement dans toutes les tailles d’icône. Consacrez le temps nécessaire pour le faire. Suivez les [instructions relatives aux icônes de style Aero](vis-icons.md).
-   **Si votre programme utilise des icônes de superposition, concevez l’icône de base de votre programme pour gérer les superpositions.** Les icônes de superposition s’affichent dans le coin inférieur droit. vous devez donc concevoir l’icône afin que la zone puisse être masquée.

    ![capture d’écran des icônes et avec une superposition inférieure droite ](images/winenv-taskbar-image15.png)

    Dans cet exemple, l’icône du bouton de la barre des tâches du programme ne contient pas d’informations importantes dans la partie inférieure droite.

-   **N’utilisez pas de superpositions dans l’icône de base de votre programme,** que votre programme utilise ou non des icônes de superposition. L’utilisation d’une superposition dans l’icône de base sera déroutante, car les utilisateurs devront déterminer qu’ils ne communiquent pas l’État.

    **Incorrect :**

    ![capture d’écran de l’icône de base avec la superposition ](images/winenv-taskbar-image16.png)

    Dans cet exemple, l’icône de base du programme semble être affichée sur État.

Pour obtenir des instructions générales et des exemples, consultez [icônes](vis-icons.md).

### <a name="overlay-icons"></a>Icônes de superposition

-   **Utilisez les icônes de superposition pour indiquer un État utile et pertinent uniquement.** Considérez l’affichage d’une icône de superposition comme une interruption potentielle du travail de l’utilisateur. la modification de l’État doit donc être suffisamment importante pour mériter une interruption potentielle.

    **Incorrect :**

    ![capture d’écran de trois icônes de superposition ](images/winenv-taskbar-image17.png)

    Dans ces exemples, l’icône de superposition n’est pas suffisamment importante pour justifier une interruption potentielle.

-   **Utilisez les icônes de superposition pour l’état temporaire.** Les icônes de superposition perdent leur valeur si elles s’affichent constamment, de sorte que l’état normal du programme ne doit pas afficher d’icône. Supprimer l’icône de superposition lorsque l’icône :

    -   Concerne **un problème :** Supprimez l’icône une fois que le problème a été résolu.
    -   **Signale une nouveauté :** Supprimez l’icône une fois que l’utilisateur a activé le programme.

    **Exception :** Votre programme peut afficher constamment une icône de recouvrement si les utilisateurs ont toujours besoin de connaître leur état.

    ![capture d’écran de Live Messenger avec icône de superposition ](images/winenv-taskbar-image18.png)

    dans cet exemple, Windows Live Messenger affiche toujours une icône de superposition afin que les utilisateurs puissent toujours vérifier leur présence signalée.

-   **N’affiche pas d’icône pour indiquer qu’un problème a été résolu.** Au lieu de cela, il suffit de supprimer toute icône précédente indiquant un problème. Supposons que les utilisateurs s’attendent normalement à ce que votre programme s’exécute sans problème.
-   **Affichez les icônes de superposition ou de zone de notification, mais jamais les deux à la fois.** Votre programme peut prendre en charge les deux mécanismes de compatibilité descendante, mais si votre programme affiche l’État à l’aide d’icônes de superposition, il ne doit pas non plus utiliser les icônes de la zone de notification pour l’État.

    **Incorrect :**

    ![capture d’écran de la barre des tâches avec l’icône affichée deux fois ](images/winenv-taskbar-image19.png)

    Dans cet exemple, l’icône de nouvelle messagerie s’affiche de manière redondante.

-   **Ne pas faire clignoter le bouton de la barre des tâches pour attirer l’attention sur un changement d’État.** Cela serait trop gênant. Permet aux utilisateurs de découvrir eux-mêmes les icônes de superposition.
-   **Préférer les icônes de superposition standard pour indiquer l’État ou les modifications d’État.** Utilisez les icônes de superposition standard suivantes : 

    | Overlay | État |
    |---------------------------------------------------------------------------------------------------|----------------------------------|
    | ![capture d’écran de petite icône d’avertissement ](images/winenv-taskbar-image20.png)<br/>               | Avertissement<br/>               |
    | ![capture d’écran de l’icône d’erreur de petite taille ](images/winenv-taskbar-image21.png)<br/>                 | Erreur<br/>                 |
    | ![capture d’écran de la petite icône désactivée/déconnectée ](images/winenv-taskbar-image22.png)<br/> | Désactivé/déconnecté<br/> |
    | ![capture d’écran de la petite icône bloquée/hors connexion ](images/winenv-taskbar-image23.png)<br/>       | Bloqué/hors connexion<br/>       |

    

     

-   **Pour les icônes de superposition personnalisées, choisissez une conception facilement reconnaissable.** Utilisez des icônes de couleur complète de 16x16 pixels de haute qualité. Préférer les icônes avec des contours distinctifs sur les icônes de forme carrée ou rectangulaire. Appliquez également les autres [règles d’icônes de style Aero](vis-icons.md) .
-   **Gardez la conception des icônes de superposition personnalisées en toute simplicité.** N’essayez pas de communiquer des idées complexes, inconnues ou abstraites. Si vous ne voyez pas une icône personnalisée appropriée, utilisez une icône d’icône d’erreur ou d’avertissement standard à la place, le cas échéant. Ces icônes peuvent être utilisées efficacement pour communiquer de nombreux types d’État.
-   **Ne modifiez pas l’État trop fréquemment.** Les icônes de superposition ne doivent pas apparaître bruyantes, instables ou à la demande. L’œil étant sensible aux modifications apportées au champ de vision du périphérique, les changements d’État doivent être subtils.
    -   **Ne modifiez pas l’icône rapidement.** Si l’État sous-jacent change rapidement, l’icône se reflète sur l’état de haut niveau.

        **Incorrect :**

        ![capture d’écran de l’icône de superposition dans deux États ](images/winenv-taskbar-image24.png)

        Dans cet exemple, l’icône de superposition à variation rapide nécessite une attention.

    -   **N’utilisez pas les animations.** Cela est trop gênant.
    -   **Ne pas faire clignoter l’icône.** Cela est trop gênant. Si un événement requiert une attention immédiate, utilisez plutôt une boîte de dialogue. Si l’événement nécessite une attention, utilisez une notification.

### <a name="taskbar-button-flashing"></a>Bouton de la barre des tâches clignotant

-   **Utilisez le bouton de la barre des tâches clignotant avec modération pour demander à l’utilisateur de continuer à exécuter une tâche en cours.** Il est difficile pour les utilisateurs de se concentrer lorsqu’un bouton de la barre des tâches clignote. Supposons donc qu’ils interrompent ce qu’ils font pour s’arrêter. Si le clignotement d’un bouton de la barre des tâches est préférable au vol de l’entrée, les boutons de la barre des tâches clignotent toujours très intrusif. Assurez-vous que l’interruption est justifiée, par exemple pour indiquer que l’utilisateur doit enregistrer les données avant de fermer une fenêtre. Les programmes inactifs devraient rarement nécessiter une action immédiate. Ne pas faire clignoter le bouton de la barre des tâches si la seule chose que l’utilisateur doit faire est d’activer le programme, de lire un message ou de voir une modification de l’État.
-   **Si aucune action immédiate n’est requise, envisagez les solutions suivantes :**
    -   Utilisez une [notification de réussite d’action](mess-notif.md) pour indiquer qu’une tâche est terminée.
    -   Ne rien faire. Attendez-vous à ce que les utilisateurs participent au problème la prochaine fois qu’ils activeront le programme. C’est souvent le meilleur choix.
-   **Si un programme inactif requiert une attention immédiate, le bouton de la barre des tâches clignote pour attirer l’attention et le garder en surbrillance.** Ne rien faire d’autre : ne restaurez pas ou n’activez pas la fenêtre et ne jouez aucun effet sonore. Au lieu de cela, respectez la sélection de l’état de la fenêtre de l’utilisateur et laissez l’utilisateur activer la fenêtre quand elle est prête.
-   **Pour les fenêtres secondaires qui possèdent un bouton de la barre des tâches, flashez son bouton à la place du bouton de la barre des tâches de la fenêtre principale.** Cela permet aux utilisateurs d’assister directement à la fenêtre.
-   **Pour les fenêtres secondaires qui n’ont pas de bouton de la barre des tâches, flashez le bouton de la barre des tâches de la fenêtre principale et placez la fenêtre secondaire sur toutes les autres fenêtres de ce programme.** Les fenêtres secondaires qui requièrent votre attention doivent être les plus haut pour s’assurer que les utilisateurs les voient.
-   **Clignoter un seul bouton de la barre des tâches pour une fenêtre à la fois.** Le clignotement de plusieurs boutons est inutile et trop gênant.
-   **Supprimez la mise en surbrillance du bouton de la barre des tâches lorsque le programme devient actif.**
-   **Lorsque le programme devient actif, assurez-vous qu’il y a un événement évident à faire.** En général, cet objectif est obtenu en affichant une boîte de dialogue qui pose une question ou lance une action.

### <a name="quick-launch-shortcuts"></a>Raccourcis de lancement rapide

-   **Placez les raccourcis de programme dans la zone lancement rapide uniquement si les utilisateurs s’y abonnent.** étant donné que le lancement rapide a été supprimé de Windows 7, les programmes conçus pour Windows 7 ne doivent pas ajouter de raccourcis de programme à la zone de lancement rapide, ni fournir des options pour le faire.

### <a name="jump-lists"></a>Listes de raccourcis

**Concevez**

-   **Concevez des listes de raccourcis pour répondre aux objectifs de vos utilisateurs pour leurs tâches quotidiennes.** Vous devez :
    -   **L’objectif de votre programme.** Réfléchissez à ce que les utilisateurs sont les plus susceptibles de faire ensuite. Pour les programmes de création de documents, les utilisateurs sont susceptibles de revenir aux documents récemment utilisés. Pour les programmes qui affichent du contenu existant, les utilisateurs peuvent souhaiter accéder aux ressources qu’ils utilisent fréquemment. Pour les autres programmes, les utilisateurs peuvent être amenés à effectuer des tâches qu’ils n’ont pas encore effectuées, par exemple lire de nouveaux messages, regarder de nouvelles vidéos ou vérifier leur prochaine réunion.
    -   **Ce que les utilisateurs s’intéressent le plus.** Réfléchissez à la raison pour laquelle les utilisateurs peuvent utiliser la liste de raccourcis au lieu d’autres moyens. Par exemple, les utilisateurs sont plus susceptibles de se soucier des destinations qu’ils ont explicitement identifiées comme importantes (par exemple, des adresses Web placées dans la barre de liens ou dans les favoris, ou tapées). Ils sont moins susceptibles de se soucier de ceux obtenus indirectement ou avec un minimum d’effort (tels que les adresses Web visitées par la redirection ou en cliquant sur les liens).

        **Correct :**

        ![capture d’écran de la liste de raccourcis avec un lien vers une cible ](images/winenv-taskbar-image25.png)

        **Incorrect :**

        ![capture d’écran de la liste de raccourcis avec cinq liens vers la cible ](images/winenv-taskbar-image26.png)

        Dans l’exemple incorrect, la liste de raccourcis contient de nombreuses destinations sur lesquelles les utilisateurs ne peuvent pas se soucier.

-   **Ne rendez pas les destinations trop précises.** Le fait de rendre les destinations trop étroites et spécifiques peut entraîner une redondance, avec plusieurs façons de passer au même emplacement. Par exemple, au lieu de répertorier les pages Web individuelles, il est préférable de répertorier les pages d’hébergement de niveau supérieur. au lieu de répertorier les chansons, listez les albums.

    **Correct :**

    ![capture d’écran de la liste de liens organisée par groupes ](images/winenv-taskbar-image27.png)

    **Incorrect :**

    ![capture d’écran de la liste de raccourcis organisée par chansons ](images/winenv-taskbar-image28.png)

    Dans l’exemple incorrect, l’affichage des chansons dans une liste de raccourcis le remplit avec un seul album.

-   **Ne remplissez pas tous les emplacements de liste de raccourcis disponibles si vous n’en avez pas besoin.** Focus de la liste de raccourcis contenu sur les éléments les plus utiles si votre programme n’a que trois éléments utiles, fournissez uniquement trois éléments. Plus il y a d’éléments dans une liste de raccourcis, plus l’effort requis pour trouver un élément spécifique est élevé.

    ![capture d’écran de la liste de raccourcis avec une commande ](images/winenv-taskbar-image29.png)

    dans cet exemple, le Pense-bêtes accessoire fournit une seule commande de liste de raccourcis, car c’est tout ce qui est nécessaire.

-   **Fournissez des info-bulles uniquement lorsque cela est nécessaire pour aider les utilisateurs à comprendre les éléments de la liste de raccourcis.** Évitez les info-bulles redondantes, car il s’agit d’une gêne inutile. Pour plus d’informations sur les info-bulles, consultez info-bulles [et info-bulles](ctrl-tooltips-and-infotips.md).

    **Incorrect :**

    ![capture d’écran de la liste de raccourcis avec une info-bulle redondante ](images/winenv-taskbar-image30.png)

    Dans cet exemple, l’info-bulle de la liste de raccourcis est redondante.

**Fonctionnalités de liste de raccourcis et fonctionnalités de programme**

-   **Ne rendez pas les destinations et les commandes disponibles uniquement par le biais de listes de raccourcis.** Les mêmes destinations et commandes doivent être disponibles directement à partir du programme lui-même.
-   **Utilisez des noms cohérents pour les destinations et les étiquettes des commandes.** Les éléments de la liste de raccourcis doivent être étiquetés de la même façon que les éléments équivalents accessibles directement à partir du programme.
-   **Autorisez votre programme à gérer les destinations et les commandes même lorsque le programme n’est pas en cours d’exécution.** Cela est nécessaire pour une expérience cohérente, fiable et pratique.

**Regroupement**

-   **Fournissez au moins un et trois groupes au minimum.** Les éléments de la liste de raccourcis sont toujours regroupés pour étiqueter leur rôle. Le fait de disposer de plus de trois groupes rend les éléments plus difficiles à trouver.
-   **Utilisez les noms de groupes standard, le cas échéant.** Les noms de groupes standard sont familiers et faciles à comprendre pour les utilisateurs.

    les commandes reçoivent le nom du groupe de tâches, qui est assigné par Windows et ne peuvent donc pas être modifiés.

    **Correct :**

    ![capture d’écran de la liste de liens avec le nom de groupe récent ](images/winenv-taskbar-image31.png)

    **Incorrect :**

    ![capture d’écran de la liste de liens avec le nom du groupe d’historique ](images/winenv-taskbar-image32.png)

    Récent est le nom de groupe le plus approprié, car il est familier, et la distinction subtile entre l’histoire et les récents n’est pas la solution la plus intéressante.

**Commandes**

-   **Fournir un ensemble fixe de commandes indépendamment de l’état d’exécution du programme, du document actif ou de l’utilisateur actuel.** Les commandes doivent s’appliquer à l’ensemble du programme, et non à une fenêtre ou un document spécifique. Cela est nécessaire pour une expérience cohérente, fiable et pratique. Les commandes ne doivent pas être supprimées ou désactivées.

    **Exceptions :** Vous pouvez remplacer ou supprimer des commandes dans les cas suivants :

    -   Un ensemble de commandes s’excluant mutuellement partagent un emplacement de commande unique, à condition qu’une seule commande s’applique toujours.
    -   Les commandes ne s’appliquent pas tant que des fonctionnalités spécifiques n’ont pas été utilisées, à condition que les commandes s’appliquent toujours.

    **Incorrect :**

    ![capture d’écran de la liste de raccourcis avec la tâche d’impression ](images/winenv-taskbar-image33.png)

    Dans cet exemple, Print n’est pas une bonne commande de liste de raccourcis, car elle dépend du document actif.

    **Correct :**

    ![capture d’écran de la liste de raccourcis avec la connexion et la déconnexion ](images/winenv-taskbar-image34.png)

    Dans cet exemple, les commandes de connexion et de déconnexion sont mutuellement exclusives. En outre, les séparateurs sont utilisés pour regrouper les commandes associées.

-   **Utilisez les étiquettes de commande standard suivantes, le cas échéant.** Les étiquettes de commande standard sont plus faciles à comprendre pour les utilisateurs.
-   **Présentez les commandes dans un ordre logique.** Les commandes courantes incluent par fréquence d’utilisation ou par ordre d’utilisation. Placez les commandes étroitement liées les unes à côté des autres. Dans le groupe tâches, placez les séparateurs entre les groupes de commandes associées, si nécessaire.
-   **Ne fournissez pas de commandes pour ouvrir ou fermer le programme.** Ces commandes sont intégrées à toutes les listes de raccourcis.

**Icônes de commande**

-   **Dans le groupe tâches, fournissez une icône de commande uniquement lorsqu’elle aide les utilisateurs à comprendre, reconnaître ou différencier les commandes,** en particulier lorsqu’il existe une icône établie pour la commande utilisée dans le programme.

    -   **Exception :** Si votre programme utilise les deux destinations (qui ont toujours des icônes) et les commandes, envisagez de fournir des icônes pour toutes les commandes si vous n’y parvenez pas.

    **Incorrect :**

    ![capture d’écran de l’utilisation incohérente des icônes dans la liste de raccourcis ](images/winenv-taskbar-image35.png)

    Dans cet exemple, Internet Explorer doit fournir des icônes pour toutes les commandes afin d’éviter une apparence maladroite.

**Destinations**

-   **Fournissez un ensemble dynamique de destinations spécifiques à l’utilisateur actuel, mais indépendantes de l’état d’exécution du programme ou du document actif.** Comme nous l’avons vu précédemment, assurez-vous qu’ils sont adaptés à l’objectif de votre programme, que les utilisateurs s’intéressent le plus et ont le niveau de spécificité approprié.
-   **Quand cela est approprié, utilisez une liste de destination « automatique ».** les destinations automatiques sont gérées par Windows, mais votre programme contrôle les destinations spécifiques qui sont transmises.
    -   Envisagez l’utilisation de récents pour les programmes de création de documents où les utilisateurs sont susceptibles de revenir aux destinations récemment utilisées.

        ![capture d’écran de la liste de liens avec le nom de groupe « récent » ](images/winenv-taskbar-image36.png)

        dans cet exemple, Windows Bloc-notes utilise des destinations récentes.

    -   Envisagez d’utiliser fréquemment pour les programmes qui affichent le contenu existant, où les utilisateurs sont susceptibles de revenir à des éléments qu’ils utilisent souvent. Les destinations fréquentes sont triées par ordre de fréquence, les plus fréquentes en premier.

        ![capture d’écran de la liste de liens avec un nom de groupe fréquent ](images/winenv-taskbar-image37.png)

        dans cet exemple, Windows Explorer utilise des destinations fréquentes.

    -   À utiliser fréquent si récent se traduirait par de nombreuses destinations inutiles. Les listes fréquentes sont plus stables et le meilleur choix lorsque les utilisateurs accèdent à de nombreuses destinations différentes, mais ne sont pas susceptibles de revenir à des listes rarement utilisées.

        **Incorrect :**

        ![capture d’écran de la liste de raccourcis contenant plusieurs éléments récents ](images/winenv-taskbar-image38.png)

        l’utilisation de récents dans Windows Internet Explorer entraînerait de nombreuses destinations inutiles.

    -   Si les options récentes ou fréquentes sont des choix également appropriés, utilisez récent, car cette approche est plus facile à comprendre et est plus prévisible pour les utilisateurs.
    -   Si vous utilisez récent et que le programme a un équivalent dans le menu fichier, faites en sorte que les listes aient le même contenu dans le même ordre. Pour les utilisateurs, ceux-ci doivent apparaître dans les mêmes listes.

-   **Si nécessaire, utilisez une liste de destination personnalisée.** Votre programme dispose d’un contrôle total sur le contenu et l’ordre de tri d’une liste de destination personnalisée, et peut par conséquent baser la liste sur tous les facteurs.
    -   Créez des versions personnalisées de récentes ou fréquentes si elles sont appropriées, mais la gestion automatique ne fonctionne pas correctement pour votre programme. Par exemple, votre programme peut avoir besoin d’effectuer le suivi d’un grand nombre de facteurs au-delà des commandes Open file. Dans ce cas, utilisez le même nom (récent ou fréquent) et l’ordre de tri, car les utilisateurs ne sont pas conscients de la différence.
    -   Dans le cas contraire, utilisez un autre type de destination pour mieux répondre aux objectifs de votre utilisateur. Souvent, ces listes aident les utilisateurs à effectuer des tâches qu’ils n’ont pas encore effectuées, telles que lire de nouveaux messages, regarder de nouvelles vidéos ou vérifier leur prochaine réunion.

        ![capture d’écran de la liste de liens avec le nom de groupe « nouveau » ](images/winenv-taskbar-image39.png)

        dans cet exemple, Windows Media Center répertorie les émissions enregistrées récemment que l’utilisateur n’a pas encore vues.

    -   Choisissez un ordre de tri qui correspond au modèle mental de l’utilisateur de la liste. Par exemple, une liste de style de tâche aurait la première chose à faire répertoriée. S’il n’existe aucun modèle mental clair, triez la liste de destination dans l’ordre alphabétique.

-   **N’utilisez pas plusieurs listes de destinations qui fournissent différentes vues des mêmes données.** Au lieu de cela, plusieurs listes de destinations doivent avoir principalement des données différentes pour prendre en charge les scénarios de différence. Par exemple, vous pouvez fournir une liste récente ou une liste fréquente, mais pas les deux. Le fait de faire en sorte que des éléments se chevauchent, mais déroutant si des éléments qui se chevauchent sont supprimés.

    **Incorrect :**

    ![capture d’écran de la liste de liens avec des éléments de groupe répétés ](images/winenv-taskbar-image40.png)

    Dans cet exemple, il est inutile de fournir différentes vues des mêmes destinations.

    **Correct :**

    ![capture d’écran de la liste de liens avec des tâches bien organisées ](images/winenv-taskbar-image41.png)

    Dans cet exemple, les listes de destination ont des données différentes pour différentes tâches.

-   **Si votre programme a une commande pour effacer les données pour la confidentialité, effacez également les listes destinations.** Les listes de destination peuvent contenir des données sensibles.

### <a name="thumbnail-toolbars"></a>Barres d’outils miniatures

**Interaction**

-   **Fournissez jusqu’à sept des commandes les plus importantes et fréquemment utilisées qui s’appliquent à la fenêtre affichée dans la miniature.** Ne vous inquiétez pas de fournir autant de commandes que vous le pouvez si votre programme n’a que trois commandes importantes fréquemment utilisées.

    **Incorrect :**

    ![capture d’écran d’un trop grand nombre de commandes dans la barre d’outils ](images/winenv-taskbar-image42.png)

    Dans cet exemple, la barre d’outils miniatures comporte des commandes qui ne sont pas importantes.

-   **Utilisez des commandes directes et immédiates.** Ces commandes doivent avoir un effet immédiat : cliquer sur la commande ne doit pas afficher de menu déroulant ou de boîte de dialogue pour plus d’informations.

    **Incorrect :**

    ![capture d’écran de la miniature avec le menu déroulant ](images/winenv-taskbar-image43.png)

    Les commandes de la barre d’outils miniatures doivent avoir un effet immédiat.

-   **Désactivez les commandes qui ne s’appliquent pas au contexte actuel, ou qui aboutiront directement à une erreur.** Ne masquez pas ces commandes, car cela rend la présentation de la barre d’outils instable.
-   **Ne faites pas disparaître la miniature quand les utilisateurs cliquent sur une commande s’ils sont susceptibles de passer en revue les résultats ou de cliquer immédiatement sur une autre commande.** Supprimez la miniature des commandes qui indiquent que l’utilisateur est terminé pour l’instant, par exemple avec des commandes qui affichent d’autres fenêtres.

    ![capture d’écran de la miniature du lecteur multimédia avec la commande ](images/winenv-taskbar-image44.png)

    dans cet exemple, le fait de cliquer sur suivant dans Lecteur Windows Media continue d’afficher la miniature parce que les utilisateurs peuvent souhaiter fournir d’autres commandes.

    ![capture d’écran de la miniature avec l’icône de conversation ](images/winenv-taskbar-image45.png)

    dans cet exemple, le fait de cliquer sur conversation dans Windows Live Messenger ignore la miniature, car les utilisateurs sont susceptibles d’envoyer un message.

**Présentation**

-   **Assurez-vous que les icônes de barre d’outils miniature sont conformes aux règles d’icône de style Aero.** Pour chaque commande, fournissez des icônes de couleur complète, 16x16, 20x20 et 24x24 de haute qualité. Les versions plus grandes sont utilisées dans les modes d’affichage haute résolution.
-   **Assurez-vous que les icônes sont clairement visibles par rapport à la couleur d’arrière-plan de la barre d’outils dans les États normal et pointé.** Évaluez toujours les icônes en contexte et dans les modes de contraste élevé.
-   **Choisissez des conceptions d’icône de commande qui communiquent clairement leur effet.** Les icônes de commande bien conçues sont explicites pour aider les utilisateurs à trouver et à comprendre efficacement les commandes.
-   **Choisissez les icônes qui peuvent être reconnaissables et différenciables.** Assurez-vous que les icônes ont des formes et des couleurs distinctives. Cela aide les utilisateurs à trouver rapidement les commandes, même s’ils ne se souviennent pas du symbole d’icône. Après l’utilisation initiale, les utilisateurs ne doivent pas s’appuyer sur les info-bulles pour faire la distinction entre les commandes.
-   **Fournissez une info-bulle pour étiqueter chaque commande.** Une bonne info-bulle étiquette le contrôle sans étiquette désigné. Pour obtenir des instructions et des exemples, consultez [info-bulles et info-bulles](ctrl-tooltips-and-infotips.md).

### <a name="progress-bars"></a>Barres de progression

-   **Suivez les instructions générales de la barre de progression,** y compris le redémarrage ou la sauvegarde en cours, et l’utilisation d’une barre de progression rouge pour indiquer un problème.
-   **Évitez d’utiliser des barres de progression indéterminées.** Les barres de progression indéterminées affichent l’activité, pas la progression. Réservez des barres de progression indéterminées pour les rares cas où les utilisateurs n’ont pas d’activité pour les autorisations.

Pour plus d’instructions, consultez [barres de progression](progress-bars.md).

## <a name="text"></a>Texte

### <a name="window-titles"></a>Titres des fenêtres

Lorsque vous choisissez des titres de fenêtre, tenez compte de l’apparence du titre dans la barre des tâches :

-   Optimisez les titres à afficher sur la barre des tâches en plaçant d’abord les informations distinctives.
-   Pour les boîtes de dialogue de progression non modales, résumez d’abord la progression. Exemple : « 66% terminé ».
-   Évitez les titres de fenêtre qui ont des troncations difficiles.

    **Incorrect :**

    ![capture d’écran du titre qui coupe le nom du programme ](images/winenv-taskbar-image48.png)

    Dans cet exemple, le titre de la fenêtre tronquée a des résultats incertains.

### <a name="jump-list-commands"></a>Commandes de la liste de raccourcis

-   **Démarrer des commandes avec un verbe.**
-   **Utilisez les majuscules comme pour les phrases.**

Pour plus d’informations sur les instructions relatives aux étiquettes de commande, consultez [menus](cmd-menus.md).

## <a name="documentation"></a>Documentation

Lorsque vous faites référence à la barre des tâches :

-   Fait référence à la barre entière en tant que barre des tâches (mot composé unique en minuscules).
-   Reportez-vous aux éléments de la barre des tâches en fonction de leur étiquette, ou généralement sous forme de boutons de la barre des tâches.
-   Lorsque cela est possible, mettez en forme les étiquettes de la barre des tâches à l’aide du texte gras. Sinon, placez l’étiquette entre guillemets uniquement si nécessaire pour éviter toute confusion.
-   Consultez les icônes de superposition sous forme d’icônes de bouton de la barre des tâches. Ne vous y référez pas en tant que notifications, même si leur objectif est de notifier les utilisateurs. Toutefois, vous pouvez indiquer que ces icônes notifient les utilisateurs d’événements spécifiques.

Exemple : l’icône du bouton nouveau message de la barre des tâches vous informe qu’un nouveau message électronique est arrivé.

 

