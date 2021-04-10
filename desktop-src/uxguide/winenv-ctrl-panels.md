---
title: Panneaux de contrôle
description: Utilisez les éléments du panneau de configuration pour aider les utilisateurs à configurer les fonctionnalités au niveau du système et à effectuer les tâches associées. Les programmes qui ont une interface utilisateur doivent être configurés directement à partir de leur interface utilisateur.
ms.assetid: 845325ef-9f1d-4aa7-a5b0-685fac74a9f8
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: dde41544f2bf8c920365f160f71dce7e88d89b81
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "103953317"
---
# <a name="control-panels"></a>Panneaux de contrôle

> [!NOTE]
> Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Utilisez les éléments du panneau de configuration pour aider les utilisateurs à configurer les fonctionnalités au niveau du système et à effectuer les tâches associées. Les programmes qui ont une interface utilisateur doivent être configurés directement à partir de leur interface utilisateur.

Avec le panneau de configuration de Microsoft Windows, les utilisateurs peuvent configurer des fonctionnalités au niveau du système et effectuer des tâches associées. Parmi les exemples de configuration de fonctionnalités au niveau du système figurent l’installation et la configuration du matériel et des logiciels, la sécurité, la maintenance du système et la gestion des comptes d’utilisateurs.

Le terme panneau de configuration fait référence à l’ensemble de la fonctionnalité du panneau de configuration Windows. Les panneaux de contrôle individuels sont appelés éléments du panneau de configuration. Un élément du panneau de configuration est considéré comme de niveau supérieur lorsqu’il est directement accessible à partir de la page d’accès du panneau de configuration ou d’une page de catégorie.

![capture d’écran de la catégorie parole du panneau de configuration ](images/winenv-ctrl-panels-image1.png)

Élément classique du panneau de configuration.

La page d’accueil du panneau de configuration est le point d’entrée principal pour tous les éléments du panneau de configuration. Elle répertorie les éléments par catégorie, ainsi que les tâches les plus courantes. Elle s’affiche lorsque les utilisateurs cliquent sur panneau de configuration dans le menu Démarrer.

Une page de catégorie du panneau de configuration répertorie les éléments d’une seule catégorie, ainsi que les tâches les plus courantes. Elle s’affiche lorsque les utilisateurs cliquent sur un nom de catégorie sur la page d’hébergement.

Les éléments du panneau de configuration sont implémentés à l’aide de [flux de tâches](glossary.md) ou de feuilles de propriétés. Pour Windows Vista et versions ultérieures, les flux de tâches sont l’interface utilisateur par défaut.

**Développeurs :** Pour savoir comment créer des éléments du panneau de configuration, consultez [éléments du panneau de configuration](/previous-versions//bb776838(v=vs.85)).

**Remarque :** Les instructions relatives aux [feuilles de propriétés](win-property-win.md) sont présentées dans un article distinct.

## <a name="is-this-the-right-user-interface"></a>S’agit-il de l’interface utilisateur appropriée ?

Pour vous décider, posez-vous les questions suivantes :

-   **L’objectif est-il de configurer des fonctionnalités au niveau du système ?** Si ce n’est pas le cas, utilisez un autre point d’intégration. Rendez les fonctionnalités de votre application configurables directement à partir de l’interface utilisateur à l’aide des boîtes de dialogue Options, au lieu d’utiliser le panneau de configuration. Pour les utilitaires qui ne sont pas utilisés pour l’installation, la configuration ou les tâches associées (telles que la résolution des problèmes), utilisez le menu Démarrer comme point d’intégration.
-   **La fonctionnalité au niveau système a-t-elle sa propre interface utilisateur ?** Dans ce cas, l’interface utilisateur est l’emplacement où les utilisateurs doivent apporter des modifications. Par exemple, un utilitaire de sauvegarde système doit être configuré à partir de ses options de programme et non à partir du panneau de configuration.
-   **Les utilisateurs devront-ils changer la configuration souvent ?** Si tel est le cas (par exemple plusieurs fois par semaine), envisagez d’autres solutions, peut-être en plus d’utiliser le panneau de configuration. Par exemple, le paramètre du volume principal Windows peut être configuré directement à partir de son icône dans la zone de notification. Certains paramètres peuvent être configurés automatiquement. Dans l’Explorateur Windows, par exemple, l’onglet compatibilité pour les propriétés de l’application permet à une application d’être exécutée en mode de couleurs 256 au lieu de demander aux utilisateurs de modifier le mode vidéo manuellement.
-   **Les utilisateurs cibles sont-ils des professionnels de l’informatique ?** Dans ce cas, utilisez un composant logiciel enfichable [MMC (Microsoft Management Console)](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) à la place, conçu spécifiquement pour les tâches de gestion du système. Dans certains cas, la meilleure solution consiste à avoir un élément du panneau de configuration pour les utilisateurs généraux et un composant logiciel enfichable MMC pour les professionnels de l’informatique.

    ![capture d’écran de la fenêtre Gestion de l’ordinateur ](images/winenv-ctrl-panels-image2.png)

    Dans cet exemple, le composant logiciel enfichable MMC utilisateurs et groupes locaux fournit une gestion des utilisateurs destinée aux professionnels de l’informatique. D’autres utilisateurs sont plus susceptibles d’utiliser l’élément comptes d’utilisateur dans le panneau de configuration.

-   **La fonctionnalité est-elle une fonctionnalité OEM utilisée uniquement lors de la configuration initiale du système ?** Si c’est le cas, utilisez le centre d’accueil Windows comme point d’intégration.

Les éléments du panneau de configuration sont nécessaires, car de nombreuses fonctionnalités au niveau du système n’ont pas de point d’intégration plus évident ou direct. Toutefois, le panneau de configuration ne doit pas être affiché comme « un seul endroit » pour tous les paramètres de configuration. **Les programmes qui ont une interface utilisateur doivent être configurés directement à partir de leur interface utilisateur au lieu d’utiliser des éléments du panneau de configuration.**

**Incorrect :**

![capture d’écran de l’élément Options Internet du panneau de configuration ](images/winenv-ctrl-panels-image3.png)

Dans cet exemple, Windows Internet Explorer ne doit pas être représenté dans le panneau de configuration, car sa propre interface utilisateur est un meilleur point d’intégration.

### <a name="create-a-new-control-panel-item-or-extend-an-existing-one"></a>Créer un élément du panneau de configuration ou en étendre un existant ?

Pour vous décider, posez-vous les questions suivantes :

-   **Les fonctionnalités peuvent-elles être exprimées en tant que tâches qui peuvent se connecter à un élément existant du panneau de configuration extensible ?** Les éléments suivants du panneau de configuration sont extensibles : appareils Bluetooth, affichage, Internet, clavier, souris, réseau, alimentation, système, sans fil (infrarouge).
-   **Les propriétés et les tâches remplacent-elles les fonctionnalités de l’élément du panneau de configuration extensible existant ?** Si c’est le cas, vous devez étendre l’élément existant du panneau de configuration, car cela aboutit à une expérience utilisateur plus simple. Si ce n’est pas le cas, créez un élément du panneau de configuration.

## <a name="design-concepts"></a>Principes de conception

**Le concept du panneau de configuration est basé sur une métaphore réaliste.** Un panneau de configuration réel est une collection de contrôles (boutons, commutateurs, jauges et affichages) utilisés pour surveiller et contrôler un appareil. Les utilisateurs de ces panneaux de contrôle ont souvent besoin d’une formation pour comprendre comment les utiliser.

Contrairement à leurs équivalents réels, **les conceptions du panneau de configuration Windows sont optimisées pour les premiers utilisateurs.** Les utilisateurs n’effectuent pas très souvent des tâches du panneau de configuration, de sorte qu’ils ne se souviennent généralement pas de leur utilisation et de leur réapprentissage à chaque fois.

Pour concevoir un élément du panneau de configuration qui est utile et facile à utiliser :

-   Vérifiez que les propriétés sont nécessaires.
-   Présenter les propriétés en termes d’objectifs d’utilisateur plutôt que de technologie.
-   Présenter les propriétés au niveau approprié.
-   Concevoir des pages pour des tâches spécifiques.
-   Pages de conception pour les utilisateurs standard et les administrateurs protégés.

Lors de la conception et de l’évaluation des éléments à inclure dans le panneau de configuration, déterminez les tâches courantes effectuées par les utilisateurs et assurez-vous qu’il existe un chemin d’accès clair pour effectuer ces tâches. Les utilisateurs effectuent généralement les types de tâches suivants avec les éléments du panneau de configuration :

-   Configuration initiale
-   Modifications peu fréquentes (pour la plupart des paramètres)
-   Modifications fréquentes (pour quelques paramètres importants)
-   Restauration des paramètres à un état initial ou précédent
-   Résolution des problèmes

**Si vous n’avez qu’une seule chose...**

Concevez des pages du panneau de configuration pour des tâches spécifiques et présentez-les en termes de objectifs d’utilisateur et non de technologie.

## <a name="usage-patterns"></a>Modèles d’usage

Pour les éléments du panneau de configuration, vous pouvez utiliser un tableau de bord de tâches ou une feuille de propriétés. Voici leur modèle d’utilisation :

### <a name="task-flow-patterns"></a>Modèles de déroulement des tâches

Les éléments de déroulement des tâches utilisent une page Hub pour présenter les choix de haut niveau et les pages spoke pour effectuer la configuration réelle.

**Pages Hub**

-   Pages de concentrateur basées sur des tâches. Ces pages Hub présentent les tâches les plus couramment utilisées. Elles sont préférables pour quelques tâches couramment utilisées ou importantes, où les utilisateurs ont besoin de conseils et d’explications supplémentaires. Les pages Hub n’ont pas de bouton valider. Les pages hybrides de concentrateur basé sur des tâches possèdent également des propriétés ou des commandes directement. Les pages de concentrateur hybride sont vivement recommandées lorsque les utilisateurs sont susceptibles d’utiliser le panneau de configuration pour accéder à ces propriétés et commandes.
-   Pages Hub basées sur les objets. Ces pages Hub présentent les objets disponibles à l’aide d’un contrôle List View. Ils sont utilisés plus particulièrement lorsqu’il peut y avoir plusieurs objets. Les pages Hub n’ont pas de bouton valider.

**Pages spoke**

-   Pages de tâche. Ces pages spoke présentent une tâche ou une étape dans une tâche avec une instruction principale spécifique basée sur des tâches. Elles sont mieux utilisées pour les tâches qui tirent parti d’instructions et d’explications supplémentaires.
-   Pages de formulaire. Ces pages spoke présentent une collection de propriétés et de tâches associées basées sur une instruction principale générale. Elles sont préférables pour les fonctionnalités qui ont de nombreuses propriétés et bénéficient d’une présentation directe à une seule page, telle que les propriétés avancées.

### <a name="property-sheet-patterns"></a>Modèles de feuille de propriétés

-   Les feuilles de propriétés sont mieux utilisées dans les éléments hérités avec de nombreux paramètres destinés aux utilisateurs expérimentés. Les nouveaux éléments peuvent obtenir le même effet avec un workflow de tâche à l’aide du modèle de page de formulaire.

## <a name="guidelines"></a>Consignes

### <a name="property-sheet-control-panel-items"></a>Éléments du panneau de configuration de la feuille de propriétés

-   **N’utilisez pas les feuilles de propriétés pour les nouveaux éléments du panneau de configuration.** Utilisez plutôt des flux de tâches pour créer une expérience transparente et tirer pleinement parti de la fonctionnalité de catégorisation et de recherche de la page d’hébergement du panneau de configuration.

### <a name="task-flow-control-panel-items"></a>Éléments du panneau de configuration du déroulement des tâches

**Généralités**

-   **Gardez le contenu et les contrôles les plus importants visibles sans défilement.** Les utilisateurs ne défilent pas pour voir le contenu de la page, sauf s’ils ont une raison de. Vous pouvez toujours afficher les boutons de validation en les plaçant dans une [zone de commande](glossary.md) au lieu de la zone de contenu. Ne divisez pas les pages uniquement pour éviter le défilement.
    -   **Vous pouvez faire défiler verticalement des pages longues,** à condition que les contrôles les plus importants soient visibles sans défilement.
    -   **N’utilisez pas le défilement horizontal.** Au lieu de cela, remaniez le contenu de la page et utilisez le défilement vertical. Les pages peuvent avoir des barres de défilement horizontales uniquement lorsqu’elles sont rendues très étroites.
-   **Pour naviguer entre les pages :**
    -   Utilisez [des liens de tâche](glossary.md) pour démarrer une tâche.
    -   Utilisez les liens de tâches ou le bouton suivant pour accéder à la page suivante dans une tâche à plusieurs étapes.
    -   Utilisez les boutons valider pour effectuer une tâche.
    -   Utilisez le bouton précédent de la barre de menus pour revenir aux pages affichées précédemment. N’ajoutez pas de bouton précédent à la zone de commande.
    -   Utilisez la barre d’adresses pour revenir directement à la page d’affichage du panneau de configuration.
    -   Utilisez les liens Voir aussi dans le volet des tâches pour accéder aux pages des autres éléments du panneau de configuration. Dans le cas contraire, la navigation doit rester au sein d’un seul élément du panneau de configuration.
-   **Placez uniquement la page d’affichage du panneau de configuration dans la barre d’adresses.** Cliquer sur ce lien revient à la page d’hébergement du panneau de configuration, en abandonnant tout travail en cours sans [confirmation](https://msdn.microsoft.com/library/windows/desktop/aa511273.aspx).
-   **Ne placez pas de bouton de commande fermer sur les pages du panneau de configuration.** Les utilisateurs peuvent fermer une fenêtre du panneau de configuration à l’aide du bouton fermer de la barre de titre.

**Boutons et liens de tâche**

-   **Quand une page comporte un petit ensemble d’options fixes, utilisez des liens de tâches à la place d’une combinaison de cases d’option et d’un bouton suivant.** Cela permet aux utilisateurs de sélectionner une réponse d’un simple clic.
-   Vous pouvez placer des liens et des boutons de tâche aux emplacements suivants (par ordre de détectabilité) :
    -   [Zone de commande](glossary.md) (pour les boutons de commande sur les pages spoke uniquement).
    -   [Zone de contenu](glossary.md):
        -   Boutons de commande
        -   Liens de tâches
        -   Autres liens
    -   Liens dans le [volet des tâches](glossary.md) (pages de concentrateur uniquement).
-   **Basez l’emplacement des liens et des boutons de tâche sur l’importance et la nécessité de la découverte.**
    -   **Placez uniquement les boutons de validation dans la zone de commande.**
    -   **Placez les tâches essentielles dans la zone de contenu.** Les boutons de commande ont tendance à attirer la plus grande attention, donc à les réserver pour les commandes que les utilisateurs doivent voir. Les liens de tâche attirent également l’attention, mais les boutons de commande sont inférieurs à.
    -   **Réservez le volet de tâches et les liens bruts pour les tâches secondaires (moins importantes).** Le volet des tâches est la zone la moins détectable d’une page de tâche, et les liens simples ne sont pas aussi visibles que les boutons de commande et les liens de tâche.
-   Pour les liens de tâches présentés dans la zone de contenu :
    -   **S’il y a plus de sept liens, regroupez les liens dans des catégories.** Fournissez des en-têtes pour chacun des groupes.
    -   **Pour moins de sept liens, présentez les liens dans un groupe unique sans titre.**
-   **Présentez les liens de tâche et les boutons dans un ordre logique.** Répertorier les liens de tâches verticalement, les boutons de commande horizontalement.
-   Dans les catégories, **divisez les commandes en groupes associés.** Présentez les groupes de tâches en plaçant le plus couramment utilisé en premier, et au sein de chaque groupe, placez les tâches les plus couramment utilisées. **L’ordre qui en résulte doit suivre à peu près la probabilité d’utilisation, mais également avoir un Flow logique.**
    -   **Exception :** Les liens de tâche qui entraînent tout doivent être placés en premier.
-   **S’il existe de nombreux liens de tâches, donnez aux tâches les plus importantes une apparence plus importante** en utilisant une icône de pixel 24x24 et deux lignes de texte. Pour les tâches moins importantes, utilisez une icône de 16 x 16 pixels ou aucune icône et une seule ligne de texte de lien.

    ![capture d’écran d’éléments avec grandes et petites icônes ](images/winenv-ctrl-panels-image4.png)

    Dans cet exemple, les commandes importantes reçoivent une apparence plus importante.

-   **Avoir une séparation physique claire entre les commandes fréquemment utilisées et les commandes destructrices.** Sinon, les utilisateurs peuvent cliquer sur des commandes destructrices accidentellement. Vous devrez peut-être réorganiser vos commandes assez pour mettre en place des commandes destructrices.
-   **Fournissez le mécanisme permettant d’annuler des commandes directement sur la page.** Les utilisateurs ne doivent pas avoir à naviguer ailleurs pour annuler une erreur.
-   **Pour les liens de tâche, utilisez toutes les icônes de la tâche par défaut ou toutes les icônes personnalisées.** Ne pas les mélanger. Envisagez d’utiliser des icônes personnalisées uniquement si :
    -   Ils aident les utilisateurs à comprendre les tâches.
    -   Ils sont conformes aux normes de l' [icône Aero](vis-icons.md).
    -   Ils ont une apparence discrète.

**Boîtes de dialogue**

Lorsque vous utilisez des flux de tâches, vous souhaitez généralement qu’une tâche passe d’une page à l’autres dans une même fenêtre, mais les circonstances suivantes sont des exceptions. Utilisez les boîtes de dialogue dans les circonstances suivantes :

-   Pour inviter les utilisateurs à entrer un nom d’utilisateur et un mot de passe d’administrateur. Utilisez toujours la boîte de dialogue Gestionnaire d’informations d’identification à cet effet. (Doit être [modal](glossary.md).)
-   Pour confirmer une commande sur place à l’aide d’une boîte de dialogue de tâche ou d’un message. (Doit être modal.)
-   Pour obtenir une entrée pour les commandes sur place, par exemple pour les commandes nouveau, ajouter, enregistrer sous, renommer et imprimer.

    ![capture d’écran de la boîte de dialogue Supprimer les emplacements réseau ](images/winenv-ctrl-panels-image5.png)

    Dans cet exemple, la commande supprimer est exécutée dans une boîte de dialogue au lieu d’une page distincte.

-   Pour effectuer des tâches secondaires autonomes. À l’aide d’une fenêtre secondaire [non modale](glossary.md), ces tâches peuvent être exécutées indépendamment et en dehors du déroulement principal des tâches.

### <a name="hub-pages"></a>Pages Hub

**Généralités**

-   Utilisez les pages de Hub basées sur les tâches lorsque :
    -   **Il existe un petit nombre de tâches couramment utilisées ou importantes.**
    -   **La configuration implique un ou deux objets** (exemples : moniteurs, clavier, souris, contrôleurs de jeu).
    -   **La configuration s’applique à l’ensemble du système** (exemples : date et heure, sécurité, options d’alimentation).
-   Utilisez les pages Hub basées sur les objets lorsque :
    -   **La configuration peut impliquer plusieurs objets** (par exemple : comptes d’utilisateur, connexions réseau, imprimantes).
    -   **La configuration s’applique uniquement à l’objet sélectionné**.
-   **N’utilisez pas de page Hub si l’élément du panneau de configuration comporte une seule page** qui contient toutes les tâches et les propriétés impliquées.

**Listes d’objets**

-   **Répertorier les éléments dans un ordre logique.** Triez les objets nommés par ordre alphabétique, les nombres dans l’ordre numérique et les dates dans l’ordre chronologique.
-   Pour les hubs basés sur des objets, **fournissez des commandes d’affichage des objets dans le volet des tâches si la possibilité de modifier l’affichage est importante pour les tâches**. La possibilité de modifier des affichages est importante s’il existe de nombreux objets et que la présentation par défaut ne fonctionne pas correctement pour tous les scénarios. Les utilisateurs peuvent modifier le mode liste même s’il n’y a pas de commandes explicites dans le menu contextuel du mode liste, mais il est moins détectable.

Pour plus d’instructions sur la présentation des listes d’objets, consultez [affichages en liste](ctrl-list-views.md).

**Interaction**

-   **Ne placez pas de boutons de validation sur les pages Hub.** Les pages Hub sont des points de lancement fondamentaux. Les utilisateurs ne peuvent jamais « valider » les pages de concentrateur qu’ils n’ont jamais effectuées. Les boutons de validation sur les pages Hub rendent les tâches initiées à partir d’un concentrateur confus (les utilisateurs se demandent si ces tâches doivent être validées).
    -   **Exception :** Si la modification d’un paramètre requiert une [élévation](glossary.md), fournissez un bouton appliquer avec une [icône de bouclier de sécurité](winenv-uac.md). Désactivez le bouton valider une fois que des modifications ont été appliquées.
-   **Envisagez de placer les propriétés les plus utiles directement sur les pages de concentrateur.** Ces pages de concentrateurs hybrides sont fortement recommandées lorsque les utilisateurs sont susceptibles d’utiliser le panneau de configuration pour accéder à ces propriétés.

    ![capture d’écran de la page Hub options d’alimentation ](images/winenv-ctrl-panels-image6.png)

    Dans cet exemple, l’élément options d’alimentation du panneau de configuration a les paramètres les plus utiles directement sur la page Hub.

-   **Utilisez un modèle de validation immédiate pour tous les paramètres des pages de concentrateur hybride afin que les modifications soient apportées immédiatement.** Là encore, les utilisateurs ne valident jamais une page Hub. Si un paramètre requiert un bouton valider, ne le placez pas sur une page Hub.
-   **Envisagez de placer des commandes simples à « une étape » directement sur des pages Hub au lieu d’utiliser des liens de navigation.**
-   **Confirmez les commandes sur place dont les effets ne peuvent pas être facilement annulés.** Utilisez une [boîte de dialogue de tâche](win-dialog-box.md) ou une [boîte de message](glossary.md).

    ![capture d’écran de la boîte de dialogue confirmer la suppression ](images/winenv-ctrl-panels-image7.png)

    Dans cet exemple, la commande de suppression est confirmée par une boîte de dialogue.

-   **Pour les pages de Hub basées sur des tâches, Identifiez chaque tâche avec un lien de tâche et une icône.** Vous pouvez également fournir une description facultative pour chaque lien. Toutefois, essayez de rendre les liens de tâche explicites et fournissez des descriptions facultatives uniquement aux liens qui en ont vraiment besoin.

    ![capture d’écran de la page Hub performance Computer ](images/winenv-ctrl-panels-image8.png)

    Dans cet exemple, chaque tâche a un lien de tâche et une icône.

-   **Pour les pages de Hub basées sur les objets, un simple clic sélectionne des objets, et un double-clic sélectionne un objet et navigue vers sa page par défaut.** La page par défaut est généralement une page de propriétés ou une page de concentrateur basée sur des tâches.
-   **Une page de concentrateur basée sur un objet peut naviguer vers un hub basé sur des tâches pour les objets sélectionnés.** Toutefois, ces hubs secondaires doivent être évités, car ils rendent l’élément du panneau de configuration un aspect trop indirect.

**Volets de tâches**

Utilisez les volets des tâches pour présenter des liens vers des commandes, des vues et des éléments du panneau de configuration associés.

-   Pour les volets des tâches dans les hubs basés sur des tâches, présentez les liens dans l’ordre suivant :
    -   **Commandes secondaires**. Présentez les tâches principales uniquement dans la zone de contenu. Utilisez le volet des tâches pour les tâches secondaires et facultatives. Considérez une tâche principale si les utilisateurs doivent la découvrir dans des scénarios importants ; secondaire s’il est acceptable pour les utilisateurs de ne pas le découvrir.
    -   **Voir aussi**. Liens facultatifs qui naviguent vers les éléments associés du panneau de configuration.
-   Pour les volets des tâches dans les hubs basés sur des objets, présentez les liens dans l’ordre suivant :
    -   **Affichages des objets**. Liens facultatifs utilisés pour contrôler la présentation des objets.
    -   **Commandes fixes**. Les commandes indépendantes des objets actuellement sélectionnés.
    -   **Commandes contextuelles**. Les commandes qui dépendent des objets actuellement sélectionnés et ne sont donc pas toujours affichées.
    -   **Voir aussi**. Liens facultatifs qui naviguent vers les éléments associés du panneau de configuration.
-   **N’utilisez pas les volets des tâches dans les pages Spoke.** Contrairement aux pages de concentrateur, les pages spoke doivent être axées sur la réalisation de la tâche. Vous ne souhaitez pas inciter les utilisateurs à quitter l’exécution avant de se terminer.

**Voir également les liens**

-   **Fournissez des liens Voir également dans le volet des tâches pour aider les utilisateurs à trouver les éléments associés du panneau de configuration, ou l’élément approprié du panneau de configuration s’ils n’en ont pas.** Lien vers les éléments que les utilisateurs sont susceptibles d’associer à votre élément du panneau de configuration.

    ![capture d’écran des liens « Voir aussi » du centre de maintenance ](images/winenv-ctrl-panels-image9.png)

    Dans cet exemple, l’élément du panneau de configuration du centre de maintenance est lié à des éléments du panneau de configuration associés.

-   **Lien vers une page de tâche spécifique si c’est ce que les utilisateurs sont plus susceptibles de reconnaître.** Sinon, liez-le à l’ensemble de l’élément du panneau de configuration. Utilisez le nom du panneau de configuration sans ajouter l’expression, panneau de configuration.

### <a name="spoke-pages"></a>Pages spoke

**Généralités**

-   **Utilisez les pages de tâches pour les tâches courantes ou importantes pour lesquelles les utilisateurs ont besoin de conseils et d’explications supplémentaires.**
-   **Utilisez les pages de formulaire pour les fonctionnalités qui ont de nombreux paramètres et tirer parti d’une présentation directe à une seule page.** Les tâches idéales pour ces pages impliquent généralement des modifications évidentes de quelques propriétés simples.
-   **N’utilisez pas les volets des tâches dans les pages Spoke.**

**Interaction**

-   **Essayez de limiter les tâches principales à une seule page.** Si plusieurs pages sont requises, vous pouvez :
    -   **Utilisez des pages spoke intermédiaires pour des étapes supplémentaires ou facultatives.** Les pages spoke intermédiaires sont validées par la page spoke finale.
    -   **Utilisez des fenêtres indépendantes pour les tâches auxiliaires indépendantes.** Les fenêtres indépendantes sont validées de manière autonome et indépendamment de la tâche principale.

Cela permet d’éviter que les boutons de validation de la tâche principale soient clairs et non ambigus. Les utilisateurs doivent toujours être confiants à la compréhension de ce qu’ils sont en cours de validation.

-   **N’utilisez pas les liens Voir également dans un workflow de tâche.** Ces liens vers des éléments associés, mais différents du panneau de configuration. Bien que la navigation vers un autre élément soit acceptable dans les pages Hub, elle n’est pas dans les pages spoke, car cela interrompt la tâche.
-   **N’utilisez pas les pages spoke pour des entrées ou des confirmations simples.** Utilisez plutôt des boîtes de dialogue modales.

**Interaction (pages spoke intermédiaires)**

-   **Utilisez les liens de tâches ou le bouton suivant pour accéder à la page suivante.** La façon de passer à l’étape suivante doit toujours être évidente.
-   **Vous pouvez avoir des liens de navigation vers des étapes de tâche facultatives.** Pour éviter toute confusion lorsque les utilisateurs s’engagent sur la tâche, ces pages supplémentaires doivent être des pages intermédiaires dans le même élément du panneau de configuration. Elles ne doivent pas avoir de boutons de validation, mais doivent être validées lorsque la tâche principale est validée.

**Interaction (pages spoke finales)**

-   **Utilisez les boutons valider pour effectuer une tâche.** Utilisez un [modèle de validation différé](glossary.md) pour les pages spoke, afin que les modifications ne soient pas effectuées jusqu’à ce qu’elles soient explicitement validées (si les utilisateurs naviguent à l’aide de précédent, de fermer ou de la barre d’adresses, les modifications sont abandonnées). Les boutons de validation sont un indice visuel que l’utilisateur est sur le l’achèvement d’une tâche. N’utilisez pas de liens à cet effet.
-   **Ne confirmez pas les boutons de validation (y compris annuler).** Cela peut s’avérer ennuyeux. Exceptions :
    -   L’action a des conséquences significatives et, si elles sont incorrectes, ne sont pas facilement réparable.
    -   L’action peut entraîner une perte significative du temps ou de l’effort de l’utilisateur.
    -   L’action est clairement incohérente avec d’autres actions.
-   **Ne confirmez pas si les utilisateurs abandonnent les modifications** en naviguant à l’aide de précédent, de fermer ou de la barre d’adresses. Toutefois, vous pouvez vérifier si une navigation potentiellement involontaire peut entraîner une perte significative du temps ou de l’effort de l’utilisateur.
-   **N’utilisez pas de liens de commande ou de navigation** (y compris les liens Voir aussi). Sur les dernières pages spoke, les utilisateurs doivent explicitement terminer ou annuler la tâche. Les utilisateurs ne doivent pas être encouragés à naviguer ailleurs, car cela entraînera probablement l’annulation implicite de la tâche.
-   **Lorsque les utilisateurs terminent ou annulent une tâche, ils doivent être renvoyés à la page Hub à partir de laquelle la tâche a été lancée.** S’il n’existe pas de page de ce type, fermez la fenêtre du panneau de configuration à la place. Ne partez pas du principe que les pages spoke sont toujours lancées à partir d’une autre page.
-   **Supprimez les pages « validées » obsolètes de la pile de retour de l’Explorateur Windows** lorsque vous revenez à la page à partir de laquelle la tâche a été lancée. Les utilisateurs ne doivent jamais voir les pages qu’ils ont déjà validées lorsqu’ils cliquent sur le bouton précédent. Les utilisateurs doivent toujours apporter des modifications supplémentaires en réexécutant complètement la tâche au lieu de cliquer sur précédent pour modifier les pages obsolètes.
    -   **Développeurs :** Vous pouvez supprimer ces pages obsolètes à l’aide des API ITravelLog :: FindTravelEntry () et ITravelLogEx ::D eleteEntry ().

**Boutons de validation**

**Remarque :** Les boutons Annuler sont considérés comme des boutons de validation.

-   **Confirmez les tâches à l’aide de boutons de validation qui sont des réponses spécifiques à l’instruction principale, plutôt que des étiquettes génériques telles que OK.** Les étiquettes sur les boutons de validation doivent être logiquement propres. Évitez d’utiliser OK, car il ne s’agit pas d’une réponse spécifique à l’instruction principale et, par conséquent, plus facile à misunderstandr. En outre, OK est généralement utilisé avec les boîtes de dialogue modales et implique de manière incorrecte la fermeture de la fenêtre de l’élément du panneau de configuration.
    -   **Exceptions :**
        -   Utilisez OK pour les pages qui n’ont pas de paramètres.
        -   Utilisez OK lorsque la réponse spécifique est toujours générique, par exemple enregistrer, sélectionner ou choisir, comme lorsque vous modifiez un paramètre spécifique ou une collection de paramètres.
        -   Utilisez OK si la page contient des cases d’option qui sont des réponses à l’instruction principale. Pour conserver le modèle de validation différée, vous ne pouvez pas utiliser de liens de tâches sur une page spoke finale.

            ![capture d’écran des restrictions Web avec le bouton OK ](images/winenv-ctrl-panels-image10.png)

            Dans cet exemple, les cases d’option, pas les boutons de validation, sont des réponses à l’instruction principale.
-   **Fournissez un bouton Annuler pour permettre aux utilisateurs d’abandonner explicitement les modifications.** Tandis que les utilisateurs peuvent abandonner implicitement une tâche en ne confirmant pas leurs modifications, le fait de disposer d’un bouton annuler leur permet de le faire de manière plus fiable.
    -   **Exception :** Ne fournissez pas de bouton Annuler pour les tâches où les utilisateurs ne peuvent pas apporter de modifications. Le bouton OK a le même effet que l’option Annuler dans ce cas.
-   **N’utilisez pas les boutons Fermer, terminer ou terminer la validation.** Ces boutons sont généralement utilisés avec des boîtes de dialogue modales et impliquent de manière incorrecte la fermeture de la fenêtre de l’élément du panneau de configuration. Les utilisateurs peuvent fermer la fenêtre à l’aide du bouton Fermer dans la barre de titre. En outre, les tâches terminées et terminées sont trompeuses, car les utilisateurs sont retournés à la page à partir de laquelle la tâche a été lancée, donc ils ne sont pas vraiment effectués.
-   **Ne désactivez pas les boutons de validation.** Sinon, les utilisateurs doivent déduire la raison pour laquelle les boutons de validation sont désactivés. Il est préférable de laisser les boutons de validation activés et de fournir un message d’erreur utile à chaque fois qu’un problème survient.
-   **Assurez-vous que les boutons de validation s’affichent sur la page sans défilement.** Si la page est longue, vous pouvez rendre les boutons de validation toujours visibles en les plaçant dans une [zone de commande](glossary.md), plutôt que dans la zone de contenu.

    ![capture d’écran de la boîte de dialogue d’exécution automatique ](images/winenv-ctrl-panels-image11.png)

    Dans cet exemple, la taille de la zone de contenu est illimitée, de sorte que les boutons de validation sont placés dans la zone de commande.

-   Aligner à droite les boutons de validation et utiliser cet ordre (de gauche à droite) : les boutons de validation positifs, Cancel et apply.

**Boutons d’aperçu**

-   Assurez-vous que **le bouton Aperçu signifie appliquer les modifications en attente maintenant mais restaurer les paramètres actuels si les utilisateurs quittent la page sans valider les modifications.**
-   **Vous pouvez utiliser les boutons d’aperçu sur n’importe quelle page Spoke.** Les pages Hub n’ont pas besoin de boutons d’aperçu, car elles utilisent un [modèle de validation immédiate](glossary.md).
-   **Envisagez d’utiliser un bouton d’aperçu au lieu d’un bouton appliquer pour les pages du panneau de configuration.** Les boutons d’aperçu sont plus faciles à comprendre et peuvent être utilisés sur n’importe quelle page Spoke.
-   **Ne fournissez un bouton d’aperçu que si la page contient des paramètres (au moins un) avec des effets que les utilisateurs peuvent voir.** Les utilisateurs doivent être en mesure d’afficher un aperçu d’une modification, d’évaluer la modification et d’apporter d’autres modifications en fonction de cette évaluation.
-   **Activez toujours le bouton Aperçu.**

**Aperçus instantanés**

Un élément du panneau de configuration dispose d’un aperçu instantané lorsque l’effet des modifications sur une page spoke peut être consulté immédiatement.

-   **Envisagez d’utiliser l’aperçu instantané pour les paramètres d’affichage dans les cas suivants :**
    -   L’effet est évident, généralement parce qu’il s’applique à l’ensemble de l’analyse.
    -   L’effet peut être appliqué sans délai significatif.
    -   L’effet est sûr et peut être annulé facilement.

        ![capture d’écran de la boîte de dialogue Modifier les paramètres de couleur ](images/winenv-ctrl-panels-image12.png)

        Dans cet exemple, l’effet des paramètres de couleur et d’apparence de Windows est visible immédiatement. Cela permet aux utilisateurs d’apporter des modifications avec un minimum d’effort.

-   **Utilisez enregistrer les modifications et annuler pour les boutons de validation.** « Enregistrer les modifications » conserve les paramètres actuels, tandis que l’annulation rétablit les paramètres d’origine. « Enregistrer les modifications » est utilisé à la place de OK pour clarifier le fait que les modifications prévisualisées n’ont pas encore été appliquées.
-   **Ne fournissez pas de bouton appliquer.** L’aperçu instantané rend l’application inutile.
-   **Restaurez toutes les modifications si les utilisateurs naviguent** à l’aide de précédent, de fermer ou de la barre d’adresses. Pour conserver les modifications, les utilisateurs doivent les valider explicitement.

**Appliquer des boutons**

-   Assurez-vous que **le bouton appliquer signifie appliquer les modifications en attente (effectuées depuis le démarrage de la tâche ou la dernière application), mais rester sur la page actuelle.** Cela permet aux utilisateurs d’évaluer les modifications avant de passer à d’autres tâches.
-   **Utilisez les boutons appliquer uniquement sur les pages spoke finales.** Les boutons d’application ne doivent pas être utilisés sur des pages spoke intermédiaires pour gérer un modèle de validation immédiate.
    -   **Exception :** Vous pouvez utiliser les boutons appliquer sur une page de concentrateur hybride si la modification d’un paramètre requiert une [élévation](glossary.md). Pour plus d’informations, consultez [interaction des pages Hub](#hub-pages).
-   **Ne fournissez un bouton appliquer que si la page contient des paramètres (au moins un) avec des effets que les utilisateurs peuvent évaluer de manière explicite.** En règle générale, les boutons appliquer sont utilisés lorsque les paramètres apportent des modifications visibles. Les utilisateurs doivent pouvoir appliquer une modification, évaluer la modification et apporter d’autres modifications en fonction de cette évaluation.
-   **Activez le bouton appliquer uniquement lorsqu’il existe des modifications en attente.** Sinon, désactivez-la.
-   **Assignez « A » comme clé d’accès.**

### <a name="control-panel-integration"></a>Intégration du panneau de configuration

Pour intégrer votre élément du panneau de configuration à Windows, vous pouvez :

-   **Inscrivez votre élément du panneau de configuration (y compris son nom, sa description et son icône)**, afin que Windows en ait connaissance.
-   Si l’élément du panneau de configuration est de niveau supérieur (voir ci-dessous) :
    -   Associez-le à la **page de catégorie** appropriée.
    -   **Fournissez des liens de tâches (y compris leur nom, leur description, des mots clés et une ligne de commande)** pour indiquer des tâches principales et permettre aux utilisateurs d’accéder directement aux tâches.
-   **Fournissez des termes de recherche** pour aider les utilisateurs à trouver vos liens de tâches à l’aide de la fonctionnalité de recherche du panneau de configuration.

    Notez que vous ne pouvez fournir ces informations que pour des éléments du panneau de configuration individuels que vous ne pouvez pas ajouter ou modifier pour des éléments du panneau de configuration existants que vous étendez.

**Pages de catégorie**

-   **Ajoutez votre élément du panneau de configuration à une page de catégorie uniquement si :**

    -   La plupart des utilisateurs en ont besoin. Exemple : Centre réseau et partage
    -   Elle est utilisée plusieurs fois. Exemple : système
    -   Il fournit des fonctionnalités importantes qui ne sont pas exposées ailleurs. Exemple : imprimantes

    Les éléments du panneau de configuration qui répondent à ces critères sont désignés par le terme « niveau supérieur ».

-   **N’ajoutez pas l’élément du panneau de configuration à une page de catégorie si :**

    -   Il est rarement utilisé ou utilisé pour une configuration unique. Exemple : Centre d’accueil
    -   Elle est destinée aux utilisateurs expérimentés ou aux professionnels de l’informatique. Exemple : gestion des couleurs
    -   Elle ne s’applique pas à la configuration matérielle ou logicielle actuelle. Exemple : Windows SideShow (s’il n’est pas pris en charge par le matériel actuel).

    La suppression de tels éléments du panneau de configuration dans les pages de catégorie rend les éléments de niveau supérieur plus faciles à trouver. Étant donné leur utilisation, ces éléments du panneau de configuration sont suffisamment détectables via la recherche ou des points d’entrée contextuels.

-   **Associez votre élément du panneau de configuration de niveau supérieur à la catégorie sous laquelle les utilisateurs sont les plus susceptibles de le Rechercher.** Cette décision doit reposer sur le test de l’utilisateur.
-   **Envisagez d’associer votre élément du panneau de configuration de niveau supérieur à la deuxième catégorie la plus probable.** Vous devez associer un élément du panneau de configuration à deux catégories si les utilisateurs sont susceptibles de rechercher leurs tâches principales à plusieurs endroits.
-   **N’associez pas votre élément du panneau de configuration à plus de deux catégories.** La valeur de la catégorisation est compromise si les éléments du panneau de configuration apparaissent dans plusieurs catégories.

**Liens de tâches**

-   **Associez l’élément de votre panneau de configuration à ses principales tâches.** Vous pouvez afficher jusqu’à cinq tâches dans une page de catégorie, mais des tâches supplémentaires sont utilisées pour la recherche dans le panneau de configuration. Utilisez la même formulation que pour les liens de tâche, en supprimant éventuellement des mots pour rendre les liens de tâche plus concis.
-   **Préférez que les liens des tâches mènent à différents emplacements de votre élément du panneau de configuration.** Le fait de disposer de plusieurs liens vers le même endroit peut prêter à confusion.

**Termes de recherche**

-   **Enregistrez les termes de recherche de l’élément du panneau de configuration que les utilisateurs sont le plus susceptibles d’utiliser pour le décrire.** Ces termes de recherche doivent inclure :

    -   Fonctionnalités ou objets configurés.
    -   Tâches principales.

    Ces termes de recherche doivent être basés sur le test de l’utilisateur.

-   **Incluez également les synonymes courants pour ces termes de recherche.** Par exemple, l’analyse et l’affichage sont des synonymes, donc les deux mots doivent être inclus.
-   **Inclure des orthographes ou des césures de mots alternatifs.** Par exemple, les utilisateurs peuvent rechercher un site Web et un site Web. Pensez également à fournir des fautes d’orthographe courantes.
-   **Considérez les formes nominales au singulier et au pluriel.** La fonctionnalité de recherche du panneau de configuration ne recherche pas automatiquement les deux formes. fournissez les formulaires pour lesquels les utilisateurs sont susceptibles d’effectuer des recherches.
-   **Utilisez des verbes simples présents.** Si vous inscrivez la connexion en tant que terme de recherche, la fonctionnalité de recherche ne recherchera pas automatiquement les connexions, la connexion et la connexion.
-   **Ne vous inquiétez pas de la casse.** La fonctionnalité de recherche n’est pas sensible à la casse.

### <a name="standard-users-and-protected-administrators"></a>Utilisateurs standard et administrateurs protégés

**De nombreux paramètres requièrent des privilèges d’administrateur pour changer.** Si un processus requiert des privilèges d’administrateur, Windows Vista et les versions ultérieures requièrent des [utilisateurs standard](glossary.md) et des [administrateurs protégés](glossary.md) pour élever leurs privilèges de manière explicite. Cela permet d’empêcher le code malveillant de s’exécuter avec des privilèges d’administrateur.

Pour plus d’informations et d’exemples, consultez [contrôle de compte d’utilisateur](winenv-uac.md).

### <a name="schemes-and-themes"></a>Schémas et thèmes

Un schéma est une collection nommée de paramètres visuels. Un thème est une collection nommée de paramètres dans le système. Des exemples de modèles et de thèmes incluent l’affichage, la souris, le téléphone et le modem, les options d’alimentation et les options audio et audio.

-   **Autoriser les utilisateurs à créer des schémas dans les cas suivants :**

    -   **Les utilisateurs sont susceptibles de modifier les paramètres.**
    -   **Il est très probable que les utilisateurs modifient les paramètres en tant que collection.**

    Les schémas sont utiles lorsque les utilisateurs se trouvent dans un environnement différent, tel qu’un emplacement physique différent (pays/région, fuseau horaire). utilisation de leur ordinateur dans une situation différente (sur batteries, connectées/non ancrées); ou utiliser leur ordinateur pour une fonction différente (présentations, lecture vidéo).

-   **Fournissez au moins un schéma par défaut.** Le schéma par défaut doit être bien nommé et s’appliquer à la plupart des utilisateurs dans la plupart des cas. Les utilisateurs ne doivent pas avoir à créer leur propre schéma.
-   **Fournissez un aperçu ou un** autre mécanisme pour que les utilisateurs puissent voir les paramètres dans le schéma.

    ![capture d’écran de la boîte de dialogue de personnalisation ](images/winenv-ctrl-panels-image13.png)

    Dans cet exemple, l’élément du panneau de configuration de personnalisation affiche un aperçu des paramètres du bureau et de l’apparence.

-   **Fournissez les commandes enregistrer sous et supprimer.** Une commande Rename n’est pas nécessaire pour que les utilisateurs puissent renommer les schémas en enregistrant sous le nom souhaité et en supprimant le schéma d’origine.
-   Si les paramètres ne peuvent pas être appliqués sans schéma, **n’autorisez pas les utilisateurs à supprimer tous les schémas.** Les utilisateurs ne doivent pas avoir à créer leur propre schéma.
-   Si les schémas ne sont pas complètement indépendants (par exemple, les modes d’alimentation dépendent du mode d’opération portable actuel), assurez-vous **qu’il existe un moyen simple de modifier les paramètres qui s’appliquent à tous les schémas.** Par exemple, avec des modes de gestion de l’alimentation, assurez-vous que les utilisateurs peuvent définir ce qui se passe quand le capot d’un ordinateur portable est fermé à un seul emplacement.

### <a name="miscellaneous"></a>Divers

-   **Utilisez les extensions du panneau de configuration pour les fonctionnalités qui remplacent ou étendent les fonctionnalités Windows existantes.** Les éléments suivants du panneau de configuration sont extensibles : appareils Bluetooth, affichage, Internet, clavier, souris, réseau, alimentation, système, sans fil (infrarouge).

### <a name="default-values"></a>Valeurs par défaut

-   **Les paramètres d’un élément du panneau de configuration doivent refléter l’état actuel de la fonctionnalité.** Sinon, cela serait trompeur et peut entraîner des résultats indésirables. Par exemple, si les paramètres reflètent les recommandations mais pas l’état actuel, les utilisateurs peuvent cliquer sur Annuler au lieu d’apporter des modifications, en pensant qu’aucune modification n’est nécessaire.
-   **Choisissez le plus sûr (pour éviter la perte de données ou l’accès au système) et l’état initial le plus sécurisé.** Supposons que la plupart des utilisateurs ne modifieront pas les paramètres.
-   **Si la sécurité et la sécurité ne sont pas des facteurs, choisissez l’état initial le plus probable ou le plus pratique.**

## <a name="text"></a>Texte

### <a name="item-names"></a>Noms d’éléments

-   **Choisissez un nom descriptif qui communique clairement et différencie ce que fait l’élément du panneau de configuration.** La plupart des noms décrivent la fonctionnalité ou l’objet Windows en cours de configuration, et sont affichés dans la vue classique de la page d’affichage du panneau de configuration.
-   **N’incluez pas les mots « paramètres », « options », « propriétés » ou « configuration » dans le nom.** Ceci est implicite, et sa conservation permet aux utilisateurs de les analyser plus facilement.

    **Incorrect :**

    Options d’accessibilité

    Paramètres du modem

    Options d’alimentation

    Options régionales et linguistiques

    **Correct :**

    Accessibilité

    Modem

    Power

    Formats et langues régionaux

    Dans les exemples appropriés, les mots inutiles sont supprimés.

-   **Si l’élément du panneau de configuration configure les fonctionnalités associées, répertorie uniquement les fonctionnalités requises pour identifier l’élément et répertorie les fonctionnalités les plus susceptibles d’être reconnues ou utilisées en premier.**

    **Incorrect :**

    Options des dossiers

    Options de téléphone et de modem

    **Correct :**

    Fichiers et dossiers

    Modem

    Dans les exemples appropriés, les fonctionnalités principales des éléments du panneau de configuration sont préaccentuées.

-   Utilisez la mise [en majuscules du style titre](glossary.md).

### <a name="page-titles"></a>Titres de page

**Remarque :** Comme pour toutes les fenêtres de l’Explorateur, les titres des pages du panneau de configuration sont affichés dans la [barre d’adresses](glossary.md), mais pas dans la barre de titre.

-   **Pour les pages Hub, utilisez le nom de l’élément du panneau de configuration.**
-   **Pour les pages spoke, utilisez un bref résumé de l’objectif de la page.** Utilisez l’instruction principale de la page si elle est concise ; Sinon, utilisez un retraité concis de l’instruction principale.

    ![capture d’écran de la boîte de dialogue Options d’alimentation ](images/winenv-ctrl-panels-image6.png)

    Dans cet exemple, les options d’alimentation sont utilisées pour le titre de la page au lieu de l’instruction principale.

-   Utilisez la mise en majuscules du style titre.

### <a name="task-link-text"></a>Texte du lien vers la tâche

Les indications suivantes s’appliquent aux liens vers les pages de tâches, telles que les liens de tâches de page de catégorie et les liens.

-   **Choisissez des noms de tâches concise qui communiquent clairement et différencient la tâche.** Les utilisateurs ne doivent pas être en mesure de déterminer ce que signifie la tâche ou la manière dont elle diffère des autres tâches.

    **Incorrect :**

    Ajuster les paramètres d’affichage

    **Correct :**

    Résolution de l’écran

    Dans l’exemple correct, le libellé est plus précis.

-   **Conservez la même langue entre les liens de tâche et les pages vers lesquelles elles pointent.** Les utilisateurs ne doivent pas être surpris par la page affichée par un lien.
-   **Pour les pages de tâche, créez l’instruction principale, les boutons de validation et les liens de tâche en tant que jeu de texte associé.**

    **Exemples :**

    

    |                              |                                                       |
    |------------------------------|-------------------------------------------------------|
    | Lien de tâche :<br/>        | Connexion à un réseau sans fil<br/>              |
    | Instruction principale :<br/> | Choisir un réseau auquel se connecter<br/>             |
    | Bouton de validation :<br/>    | Se connecter<br/>                                    |
    | Lien de tâche :<br/>        | Configurer les contrôles parentaux<br/>                   |
    | Instruction principale :<br/> | Choisir un utilisateur et configurer le contrôle parental<br/> |
    | Bouton de validation :<br/>    | Appliquer le contrôle parental<br/>                     |
    | Lien de tâche :<br/>        | Résoudre vos conflits de synchronisation<br/>                |
    | Instruction principale :<br/> | Comment voulez-vous résoudre ce conflit ?<br/>  |
    | Bouton de validation :<br/>    | Résoudre<br/>                                    |

    

     

    Ces exemples illustrent la relation entre le texte du lien de la tâche, l’instruction principale et le texte du bouton de validation.

-   Bien que les tâches commencent souvent par des verbes, **envisagez d’omettre le verbe sur les pages de catégorie s’il s’agit d’un verbe de configuration générique qui ne permet pas de communiquer avec la tâche.**

    **Verbes utiles spécifiques :**

    Ajouter

    Vérification

    Se connecter

    Copier

    Créer

    DELETE

    Déconnecter

    Installer

    Supprimer

    Configurer

    Démarrer

    Arrêter

    Dépannage

    **Verbes génériques, non-aide :**

    Réglage

    Modifier

    Choose

    Configurer

    Modifier

    Gérer

    Ouvrir

    Choisir

    Définissez

    Sélectionnez

    Afficher

    Affichage

-   **Si la tâche configure plusieurs fonctionnalités associées, répertorie uniquement les fonctionnalités qui sont représentatives de l’ensemble.** Omettez les détails qui peuvent être déduits facilement.

    **Incorrect :**

    Volume de haut-parleur, muet, icône de volume

    Haut-parleurs, microphones, MIDI et modèles audio

    **Correct :**

    Volume de haut-parleur

    Haut-parleurs et microphones

    Dans les exemples corrects, seules les fonctionnalités représentatives sont fournies dans le lien de tâche.

-   **Vous devez faire une phrase des tâches en termes de technologie uniquement si les utilisateurs cibles le font également.**

    **Incorrect :**

    Connectoids

    Profondeur de pixel

    ppp

    **Correct :**

    Imprimantes

    Scanneurs

    Souris

    Les exemples corrects sont des termes basés sur la technologie qui sont susceptibles d’être utilisés par les utilisateurs, alors que les exemples incorrects ne le sont pas.

-   Utilisez des noms au pluriel uniquement si le système peut en prendre en charge plusieurs.
-   Utilisez la mise [en majuscules de style phrase](glossary.md).
-   N’utilisez pas de ponctuation finale.

### <a name="main-instructions"></a>Instructions principales

-   **Pour la page Hub, utilisez l’instruction principale pour expliquer l’objectif de l’utilisateur avec l’élément du panneau de configuration.** L’instruction principale doit aider les utilisateurs à déterminer s’ils ont sélectionné l’élément du panneau de configuration approprié. N’oubliez pas que les utilisateurs ont peut-être sélectionné l’élément du panneau de configuration en cas d’erreur et que vous recherchez en fait des paramètres qui font partie d’un autre élément du panneau de configuration.

    **Exemples :**

    Sécuriser votre ordinateur et le maintenir à jour

    Optimisez votre ordinateur pour qu’il soit plus facile à voir, à entendre et à contrôler

-   **Pour les pages spoke, utilisez l’instruction principale pour expliquer comment faire sur la page.** L’instruction doit être une instruction spécifique, une direction impérative ou une question. Les bonnes instructions communiquent l’objectif de l’utilisateur avec la page plutôt que de se concentrer exclusivement sur les mécanismes de manipulation.

    **Incorrect :**

    Sélectionner une tâche de notification

    **Correct :**

    Indiquer comment gérer les informations entrantes

    La version correcte communique mieux l’objectif atteint par la page.

-   **Utilisez des verbes spécifiques chaque fois que cela est possible.** Les verbes spécifiques sont plus significatifs pour les utilisateurs que les verbes génériques.
-   Utilisez la mise [en majuscules de style phrase](glossary.md).
-   **N’incluez pas de périodes finales si l’instruction est une instruction.** Si l’instruction est une question, incluez un point d’interrogation final.

### <a name="supplemental-instructions"></a>Instructions supplémentaires

-   **Pour la page Hub, utilisez les instructions supplémentaires facultatives pour expliquer plus en détail l’objectif de l’élément du panneau de configuration.**
-   **Pour les pages spoke, utilisez l’instruction supplémentaire facultative pour présenter des informations supplémentaires utiles pour comprendre ou utiliser la page.** Vous pouvez fournir des informations plus détaillées et définir la terminologie.
-   Utilisez les phrases complètes et les [majuscules de style de phrase](glossary.md).

### <a name="page-text"></a>Texte de la page

-   **Ne restatez pas l’instruction principale dans la zone de contenu.**
-   **Utilisez le mot « page » pour faire référence à la page elle-même.**
-   **Utilisez la deuxième personne (vous, votre) pour indiquer aux utilisateurs la marche à suivre** dans la zone instructions et contenu principales. Souvent, la deuxième personne est impliquée.

    **Exemple :**

    Choisissez les images que vous souhaitez imprimer.

-   **Utilisez la première personne (I, me, My) pour permettre aux utilisateurs d’indiquer à l’élément du panneau de configuration ce qu’il doit faire** dans la zone de contenu qui répond à l’instruction principale.

    **Exemple :**

    Imprimez les photos sur mon appareil photo.

### <a name="task-links"></a>Liens de tâches

-   **Choisissez un texte de lien concis qui communique clairement et différencie ce que fait le lien de tâche.** Elle doit être explicite et correspondre à l’instruction principale. Les utilisateurs ne doivent pas avoir à déterminer ce que signifie le lien ou la manière dont il diffère des autres liens.
-   **Démarrez toujours les liens de tâche avec un verbe.**
-   Utilisez la mise [en majuscules de style phrase](glossary.md).
-   N’utilisez pas de ponctuation finale.
-   **Si le lien de tâche nécessite une explication supplémentaire, fournissez l’explication dans un contrôle de texte distinct** en utilisant des phrases complètes et en terminant la ponctuation. Toutefois, ajoutez ces explications uniquement si nécessaire n’ajoutez pas d’explications à tous les liens de tâches, car un autre lien de tâche en a besoin.

Pour plus d’informations et d’exemples, consultez [liens](ctrl-command-links.md).

### <a name="commit-buttons"></a>Boutons de validation

-   **Utilisez des étiquettes de bouton de validation spécifiques qui sont logiques et correspondent à l’instruction principale.** Idéalement, les utilisateurs ne doivent pas lire d’autres éléments pour comprendre l’étiquette. Les utilisateurs sont beaucoup plus susceptibles de lire des étiquettes de bouton de commande que du texte statique.
-   **Démarrez toujours les étiquettes de bouton de validation avec un verbe.**
-   **N’utilisez pas fermer, terminer ou terminer.** Ces étiquettes de bouton sont mieux adaptées aux autres types de fenêtres.
-   Utilisez la mise [en majuscules de style phrase](glossary.md).
-   N’utilisez pas de ponctuation finale.
-   Attribuez une [clé d’accès](glossary.md)unique.
    -   **Exception :** N’affectez pas de touches d’accès aux boutons annuler, car ESC est sa clé d’accès. Cela rend les autres clés d’accès plus faciles à assigner.

## <a name="documentation"></a>Documentation

Quand vous faites référence à la page d’hébergement ou aux pages de catégorie du panneau de configuration :

-   Dans la documentation utilisateur, reportez-vous au panneau de configuration, à la mise en majuscules du style titre et à l’omission de l’article précédent.

    **Exemple :**

    Dans le panneau de configuration, ouvrez **Security Center**.

-   Pour la programmation et d’autres documents techniques, reportez-vous à la page d’informations du panneau de configuration et à la page de catégorie du panneau de configuration, sans mettre les mots en majuscules. Un article antérieur est facultatif.

Pour les éléments du panneau de configuration :

-   Quand vous faites référence à un élément du panneau de configuration individuel, utilisez « \[ nom de l’élément du panneau \] de configuration » dans le panneau de configuration ou généralement « élément du panneau de configuration » dans la documentation de l’utilisateur. N’utilisez pas l’applet, le programme ou le panneau de configuration pour faire référence à des éléments individuels du panneau de configuration.
-   Quand vous faites référence à la page Hub d’un élément du panneau de configuration, utilisez la page « nom de l' \[ élément du panneau de configuration principal \] ».
-   Lorsque cela est possible, mettez en forme le nom du panneau de configuration à l’aide du texte gras. Sinon, placez le nom entre guillemets uniquement si nécessaire pour éviter toute confusion.

Exemples :

-   Dans le panneau de configuration, ouvrez contrôle **parental**.
-   Revenez à la page principale de **contrôle parental** .

