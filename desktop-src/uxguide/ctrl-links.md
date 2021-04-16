---
title: Liens
description: Avec un lien, les utilisateurs peuvent accéder à une autre page, fenêtre ou rubrique d’aide. afficher une définition ; lancer une commande ; ou choisissez une option.
ms.assetid: a23748e4-b2dd-4b9f-9a7c-ff6533922c8c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 521f96146de535210d79814b375499ea34399179
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104551810"
---
# <a name="links"></a>Liens

> [!NOTE]
> Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Avec un *lien*, les utilisateurs peuvent accéder à une autre page, fenêtre ou rubrique d’aide. afficher une définition ; lancer une commande ; ou choisissez une option. Un lien est un texte ou un graphique qui indique qu’il est possible de cliquer, généralement en s’affichant à l’aide des [couleurs système du lien](vis-color.md)visité ou non visité. Traditionnellement, les liens sont également soulignés, mais cette approche est souvent inutile et ne présente pas de privilège pour réduire l’encombrement visuel.

Lorsque les utilisateurs pointent sur un lien, le texte du lien apparaît comme souligné (si ce n’était pas déjà fait) et la forme du pointeur devient une [main](inter-mouse.md).

Un lien de texte est le contrôle cliquez sur le poids le plus clair et est souvent utilisé pour réduire la complexité visuelle d’une conception.

> [!Note]  
> Les instructions relatives aux [liens de commande](ctrl-command-links.md) et à la [mise en page](vis-layout.md) sont présentées dans des articles distincts.

 

## <a name="is-this-the-right-control"></a>Est-ce le contrôle approprié ?

Pour vous décider, posez-vous les questions suivantes :

-   **Lien utilisé pour accéder à une autre page, fenêtre ou rubrique d’aide ; afficher une définition ; lancer une commande ; ou choisir une option ?** Si ce n’est pas le cas, utilisez un autre contrôle.
-   **Un bouton de commande sera-t-il un meilleur choix ?** Utilisez un [bouton de commande](ctrl-command-buttons.md) si :
    -   Le contrôle lance une action immédiate, y compris l’affichage d’une fenêtre, et cette commande est associée à l’objectif principal de la fenêtre.
    -   Une fenêtre s’affiche pour regrouper les entrées ou faire des choix, même s’il s’agit d’une commande secondaire.
    -   L’étiquette est concise, constituée de quatre mots ou moins, ce qui évite l’apparition difficile des boutons longs.
    -   La commande n’est pas Inline.
    -   Le contrôle apparaît dans un groupe d’autres boutons de commande associés.
    -   L’action est destructrice ou irréversible. Étant donné que les utilisateurs associent des liens avec la navigation (et la possibilité de les sauvegarder), les liens ne sont pas appropriés pour les commandes qui ont des conséquences significatives.
    -   De même, dans un [Assistant](win-wizards.md) ou un [Workflow de tâche](glossary.md), la commande représente un engagement. Dans ces fenêtres, les boutons de commande suggèrent un engagement, tandis que les liens suggèrent la navigation vers l’étape suivante.

## <a name="design-concepts"></a>Principes de conception

**Rendre les liens reconnus**

Les liens n' [offrent](glossary.md)pas d’offre, ce qui signifie que **leurs propriétés visuelles ne suggèrent pas la manière dont elles sont utilisées** et sont comprises uniquement par l’expérience. Les liens sans souligné et les couleurs système de lien s’affichent sous forme de texte normal. la seule façon de déterminer leur comportement provient de leur présentation, de leur contexte ou de la position du pointeur dessus.

Étonnamment, ce manque d’offre est souvent une motivation pour l’utilisation des liens, car ils s’affichent tellement légers, réduisant ainsi la complexité visuelle d’une conception. Les liens éliminent le cadre visuellement lourd utilisé par les [boutons de commande](ctrl-command-buttons.md) et la bordure utilisés par d’autres contrôles. Par exemple, même si vous pouvez utiliser des boutons de commande pour rendre les commandes primaires évidentes, vous pouvez choisir des liens pour les commandes secondaires afin de les mettre en évidence.

Le défi consiste alors à conserver suffisamment d’indices visuels pour que les utilisateurs puissent reconnaître les liens. L’indication fondamentale est que **les utilisateurs doivent être en mesure de reconnaître des liens par le biais de l’inspection visuelle seule. ils ne doivent pas avoir à pointer vers un objet ou cliquer dessus pour déterminer s’il s’agit d’un lien**.

Les utilisateurs peuvent reconnaître un lien par l’inspection visuelle seule si le lien utilise les [couleurs système de liaison](vis-color.md) et au moins l’une des indications visuelles suivantes :

-   Texte souligné.
-   Graphique ou puce, par exemple avec le modèle de [lien texte avec icône](#usage-patterns) .
-   Positionnement dans une navigation standard, une option ou un emplacement de commande, tel que la [zone de contenu](glossary.md) d’une fenêtre, ou dans une barre de navigation, une barre de menus, une barre d’outils ou un pied de page.

Les utilisateurs peuvent également reconnaître un lien par inspection visuelle avec les indices visuels suivants, mais ces indications ne sont pas suffisantes par elles-mêmes :

-   Texte qui suggère un clic, par exemple une commande commençant par un verbe impératif comme afficher, imprimer, copier ou supprimer.
-   Placement au sein d’un bloc de texte normal.

Bien entendu, les utilisateurs peuvent toujours déterminer un lien via l’interaction en pointant ou en cliquant sur. Si la détection d’un lien n’est pas nécessaire pour des tâches importantes, vous pouvez mettre en évidence ces liens.

![capture d’écran des étiquettes grises sur l’arrière-plan noir ](images/ctrl-links-image1.png)

Dans cet exemple, contactez-nous, les conditions d’utilisation, les marques commerciales et la déclaration de confidentialité sont des liens. Ils sont intentionnellement mis en évidence, car ils ne sont pas requis pour les tâches importantes. La seule indication qu’il s’agit de liens est qu’ils ont un pointeur de souris au pointage et sont positionnés dans une zone de navigation standard au bas de la fenêtre.

**Création de liens spécifiques, pertinents et prévisibles**

Le texte du lien doit indiquer le résultat d’un clic sur le lien.

Des liens spécifiques étant plus intéressants pour les utilisateurs que les liens généraux, **Utilisez des étiquettes de liens qui fournissent des informations descriptives spécifiques sur le résultat d’un clic sur le lien**. Toutefois, assurez-vous que le texte de votre lien n’est pas si spécifique qu’il est trompeur et découragera l’utilisation appropriée.

Les liens concis sont plus susceptibles d’être lus que les liens détaillés. **Éliminez le texte et les détails inutiles.** Les étiquettes de lien n’ont pas besoin d’être complètes.

Pour évaluer le texte de votre lien :

-   Assurez-vous que le texte du lien reflète les scénarios pris en charge par le lien.
-   Assurez-vous que les résultats du lien sont prévisibles. Les utilisateurs ne doivent pas être surpris par les résultats.

**Si vous ne faites que deux choses...**

1. Rendez les liens détectables uniquement par l’inspection visuelle. Les utilisateurs ne doivent pas avoir à interagir avec votre programme pour trouver des liens.

2. Utilisez des liens qui fournissent des informations descriptives spécifiques sur le résultat d’un clic sur le lien, en utilisant autant de texte que nécessaire. Les utilisateurs doivent être en mesure de prédire avec précision le résultat d’un lien à partir de son texte de lien et d’une [info-bulle](ctrl-tooltips-and-infotips.md)facultative.

## <a name="usage-patterns"></a>Modèles d’usage

Les liens ont plusieurs modèles fonctionnels :



|                                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Liens de navigation**<br/> Lien utilisé pour naviguer vers une autre page ou fenêtre. <br/>                                                      | Le fait de cliquer sur le lien permet d’accéder à l’emplacement d’une autre page, comme dans une fenêtre de navigateur ou un Assistant. ou affiche une nouvelle fenêtre. Contrairement aux liaisons de tâches, la navigation n’initie pas de tâche, mais accède simplement à un autre emplacement ou poursuit une tâche déjà en cours. La navigation implique la sécurité, car l’utilisateur peut toujours revenir en arrière.<br/> Actualités<br/> Dans cet exemple, le fait de cliquer sur le lien permet d’accéder à la page titres d’actualité.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Liens de tâches**<br/> Lien utilisé pour initialiser une nouvelle commande. <br/>                                                                        | En cliquant sur le lien, vous exécutez immédiatement une commande ou vous affichez une boîte de dialogue ou une page pour recueillir davantage d’entrées. Contrairement aux liens de navigation, les liens de tâches déclenchent une nouvelle tâche au lieu de poursuivre une tâche existante. Les tâches n’impliquent pas que safetyusers ne puisse pas revenir à l’état précédent avec une commande back. Les liens de tâche sont appelés pour éviter toute confusion avec les [liens de commande](ctrl-command-links.md). <br/> Connexion<br/> Dans cet exemple, un clic sur le lien lance une commande de connexion.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **Liens d’aide**<br/> Lien de texte utilisé pour afficher une rubrique d’aide. <br/>                                                                     | Cliquez sur ce lien pour afficher un article d’aide dans une fenêtre distincte.<br/> Qu’est-ce qu’un mot de passe fort ?<br/> Dans cet exemple, un clic sur le lien affiche une fenêtre d’aide avec la rubrique donnée.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Liens de définition**<br/> lien de texte utilisé pour afficher une définition dans une info-bulle lorsque l’utilisateur clique ou pointe sur le lien. <br/> | ce modèle est utile pour définir des termes qui peuvent ne pas être connus de vos utilisateurs sans ajouter de l’encombrement de l’écran.<br/> ![capture d’écran de l’info-bulle affichée par pointage de la souris ](images/ctrl-links-image2.png)<br/> Dans cet exemple, la définition de l’info-bulle est affichée. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Liens de menu**<br/> ensemble de liens de tâches utilisés pour créer un menu. <br/>                                                                    | étant donné que le contexte du menu indique un ensemble de liens, le texte n’est généralement pas souligné (sauf au survol) et peut ne pas utiliser les couleurs système de la liaison.<br/> ![capture d’écran d’un ensemble de liens ](images/ctrl-links-image3.png)<br/> Dans cet exemple, un ensemble de liens crée un menu.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Liens d’option**<br/> option sélectionnée ou son espace réservé, où le clic sur le lien appelle une commande pour modifier cette option.<br/>       | Contrairement aux liens de texte standard, le lien modifie son texte pour refléter l’option actuellement sélectionnée et est toujours dessiné à l’aide de la couleur de lien non visité. <br/> ![capture d’écran d’une règle dans l’Assistant règles Outlook ](images/ctrl-links-image4.png)<br/> l’exemple de gauche montre une règle de l’Assistant Règles Microsoft Outlook avec des options d’espace réservé. une fois que les utilisateurs cliquent sur les liens et sélectionnent des options, l’exemple de droite met à jour le texte du lien pour afficher les résultats.<br/> l’utilisation de liens d’option est particulièrement appropriée si les options ont un format variable. <br/> ![capture d’écran d’une règle modifiée dans l’Assistant règles ](images/ctrl-links-image5.png)<br/> l’exemple de droite montre que les règles Outlook ont un format variable. <br/> ![capture d’écran de la modification du texte dans la liste déroulante ](images/ctrl-links-image6.png)<br/> L’exemple de gauche montre un lien d’option. Elle devient une liste déroulante lorsqu’elle est sélectionnée, comme indiqué à droite.<br/> |



 

Les liens possèdent également plusieurs modèles de présentation :



|                                                                                                        |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Liens de texte brut**<br/> se compose uniquement de texte. <br/>                                      | Cette présentation est la plus souple, car elle peut être utilisée n’importe où, y compris en [ligne](glossary.md).<br/> ![capture d’écran du texte du lien bleu ](images/ctrl-links-image7.png)<br/> Dans cet exemple, la couleur de texte identifie clairement un lien Inline.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Texte avec liens d’icône**<br/> texte avec une icône précédente qui indique sa fonction.<br/> | étant donné que le graphique fournit une indication visuelle supplémentaire d’un lien, il est plus facile de le reconnaître en tant que lien qu’un lien de texte brut non souligné. ce modèle utilise généralement une icône de 16 x 16 pixels.<br/> ![capture d’écran de la liste de quatre liens avec des icônes ](images/ctrl-links-image8.png)<br/> dans cet exemple, les icônes fournissent une indication visuelle supplémentaire d’un lien.<br/> ![capture d’écran de la commande de lecture avec un petit triangle ](images/ctrl-links-image9.png)<br/> Dans cet exemple, le symbole de lecture triangulaire standard indique que ce texte est une commande.<br/>                                                                                                                                     |
| **Liens graphiques uniquement**<br/> se compose uniquement d’un graphique.<br/>                               | en raison de l’absence de lien de texte, il n’y a pas de couleur ou de soulignement de lien pour indiquer le lien. ces liens dépendent soit de la conception graphique pour suggérer un clic, soit du texte dans le graphique qui suggère une action lorsque les utilisateurs cliquent. les liens graphiques sont parfois dotés d’un effet de pointage avec la souris pour indiquer le lien. Cette approche est utile, mais n’est pas détectable uniquement par l’inspection visuelle.<br/> ![capture d’écran de l’icône avec lien-sélectionner le pointeur de la souris ](images/ctrl-links-image10.png)<br/> Dans cet exemple, le lien n’est pas détectable uniquement par l’inspection visuelle.<br/> **En raison de leurs problèmes potentiels de reconnaissance et de localisation, les liens graphiques uniquement ne sont pas recommandés comme seule façon d’effectuer une tâche.** <br/> |



 

## <a name="guidelines"></a>Consignes

### <a name="interaction"></a>Interaction

-   **Afficher un pointeur occupé si le résultat d’un clic sur un lien n’est pas instantané.** Sans commentaires, les utilisateurs peuvent supposer que le clic n’a pas eu lieu et cliquer à nouveau sur.

### <a name="color"></a>Couleur

-   **Utilisez le thème ou liez les couleurs système des liens visités et non visités.** La signification de ces couleurs est cohérente dans tous les programmes. Si, pour une raison quelconque, les utilisateurs n’aiment pas ces couleurs (peut-être pour des raisons d’accessibilité), ils peuvent les modifier eux-mêmes.
-   **Pour les liens de navigation, utilisez des couleurs différentes pour les liens visités et invisités.** Conservez l’historique des liens visités uniquement pour la durée de l’instance de programme. La couleur visitée est importante pour indiquer où les utilisateurs ont déjà été, ce qui les empêche de revisiter les mêmes pages à plusieurs reprises.
-   **Pour les autres types de liens, n’utilisez pas la couleur de lien visité.** Il n’y a pas suffisamment de valeur pour identifier les commandes « visitées », par exemple.
-   **Ne pas colorer le texte qui n’est pas un lien, car les utilisateurs peuvent supposer qu’il s’agit d’un lien.** Utilisez le gras ou une nuance de gris à l’endroit où vous utiliseriez sinon du texte en couleur.
-   **Exception**: vous pouvez utiliser du texte en couleur si tous les liens sont soulignés ou placés dans des emplacements de navigation ou de commande standard.

    **Incorrect :**

    ![capture d’écran du message de plan d’alimentation avec du texte en bleu ](images/ctrl-links-image11.png)

    Dans cet exemple, le texte bleu est incorrectement utilisé pour le texte qui n’est pas un lien.

-   **Utilisez des couleurs d’arrière-plan qui contrastent avec les couleurs des liens.** La [couleur système](vis-color.md) de la fenêtre est toujours un bon choix.

    **Incorrect :**

    ![capture d’écran du texte du lien bleu sur l’arrière-plan bleu ](images/ctrl-links-image12.png)

    Dans cet exemple, la couleur d’arrière-plan fournit un contraste médiocre avec la couleur de lien.

### <a name="underlining"></a>Le soulignement

-   **Pour les liens nécessaires à l’exécution d’une tâche principale, fournissez des indices visuels afin que les utilisateurs puissent reconnaître les liens uniquement par l’inspection visuelle.** Ces indices incluent le soulignement, les graphiques ou les puces, ainsi que les emplacements de lien standard. Les utilisateurs ne doivent pas avoir besoin de pointer sur un objet ou de cliquer dessus pour déterminer s’il s’agit d’un lien. Utilisez le texte souligné si le lien n’est pas évident dans son contexte.
-   **Ne soulignez pas le texte qui n’est pas un lien, car les utilisateurs peuvent supposer qu’il s’agit d’un lien.** Utilisez l’italique à l’endroit où vous utiliseriez sinon le texte souligné. Réserver le soulignement uniquement pour les liens.
-   **Lorsque vous imprimez, n’imprimez pas les traits de soulignement ou les couleurs de lien.** Les liens imprimés n’ont aucune valeur et sont potentiellement confus.

### <a name="text-with-icon-links"></a>Texte avec liens d’icône

-   **Utilisez l’icône de flèche uniquement pour les liens de commande.** Les liens habituels ne doivent pas utiliser l’icône en forme de flèche, sauf s’ils sont utilisés comme substituts des [liens de commande](ctrl-command-links.md) dans Windows XP.
-   **Placez l’icône à gauche du texte.** L’icône doit mener dans le texte visuellement.

**Correct :**

![capture d’écran de l’icône du texte précédent ](images/ctrl-links-image13.png)

**Incorrect :**

![capture d’écran de l’icône texte suivant ](images/ctrl-links-image14.png)

Dans l’exemple incorrect, l’icône ne mène pas au texte.

-   **Rend le résultat du clic sur l’icône identique au clic sur le texte.** Sinon, cela serait inattendu et confus.

### <a name="graphics-only-links"></a>Liens graphiques uniquement

-   **N’utilisez pas de liens Graphics uniquement.** Les utilisateurs ont difficilement les reconnaître en tant que liens et tout texte dans le graphique (utilisé pour indiquer leur action lorsque l’utilisateur clique dessus) crée un problème de localisation.

### <a name="navigation-links"></a>Liens de navigation

-   **Veillez à ce que les liens de navigation ne nécessitent aucun engagement.** Les utilisateurs doivent toujours être en mesure de revenir à l’état initial, soit à l’aide de retour pour la navigation InPlace, soit en annulant pour fermer une nouvelle fenêtre.
-   **Créer un lien vers du contenu spécifique plutôt que du contenu général.** Par exemple, il est préférable de créer un lien vers la section pertinente d’un document plutôt que d’établir un lien vers le début.
-   **Utilisez un lien uniquement si la matière liée est pertinente, utile et non redondante.** Utilisez la contrainte dans les liens de navigation ne les utilisez pas juste parce que vous pouvez.
-   **Si un lien accède à un site externe, placez l’URL dans l’info-bulle** afin que les utilisateurs puissent déterminer la cible du lien.
-   **Lier uniquement la première occurrence du texte du lien.** Les liens redondants ne sont pas nécessaires et peuvent rendre le texte difficile à lire.

    **Correct :**

    Le dossier images facilite le partage de vos images. Vous pouvez utiliser les tâches dans les images pour envoyer vos images par courrier électronique ou les publier dans un emplacement privé et sécurisé sur le Web. Vous pouvez également imprimer vos images directement à partir du dossier images.

    **Incorrect :**

    Le dossier images facilite le partage de vos images. Vous pouvez utiliser les tâches dans les images pour envoyer vos images par courrier électronique ou les publier dans un emplacement privé et sécurisé sur le Web. Vous pouvez également imprimer vos images directement à partir du dossier images.

    Dans l’exemple approprié, seule la première occurrence du texte approprié est liée.

    **Exceptions :**

    -   **Si une instruction a un lien, placez le lien dans l’instruction.**

        L’utilisation de mots de passe forts est très importante. Pour plus d'informations, consultez Mots de passe forts.

        Dans cet exemple, le lien se trouve dans l’instruction au lieu de la première occurrence.

    -   **Lier aux occurrences ultérieures s’ils sont éloignés de la première.** Par exemple, vous pouvez lier de façon redondante dans différentes sections d’une rubrique d’aide.

### <a name="task-links"></a>Liens de tâches

-   **Utilisez des liens de tâches pour les commandes qui ne sont pas destructrices ou qui sont facilement réversibles.** Étant donné que les utilisateurs associent des liens avec la navigation (et la possibilité de les sauvegarder), les liens ne sont pas appropriés pour les commandes qui ont des conséquences significatives. Les commandes qui affichent une boîte de dialogue ou une confirmation sont un bon choix.

    **Correct :**

    Démarrer

    Arrêter

    **Incorrect :**

    Supprimer le fichier

    Dans l’exemple incorrect, la commande est destructrice.

### <a name="menu-links"></a>Liens de menu

-   **Regroupez les liens de navigation et de tâche associés dans les menus.** Un menu de liens connexes placés dans un emplacement de navigation ou de commande standard facilite la recherche et la compréhension des liens par rapport à ceux qui sont placés séparément.
-   **Pour les menus dépendants de la sélection, supprimez les liens de menu qui ne s’appliquent pas.** Ne les désactivez pas. Cela élimine l’encombrement et les utilisateurs ne manqueront pas de liens nécessitant une sélection.
-   **Pour les menus indépendants de la sélection, désactivez les liens de menu qui ne s’appliquent pas.** Ne les supprimez pas. Cela rend les menus plus stables et de tels liens plus faciles à trouver.

    ![capture d’écran de la boîte de dialogue avec commande de menu grisée ](images/ctrl-links-image15.png)

    Dans cet exemple de Windows Update, une mise à jour est en cours d’exécution, la commande Rechercher les mises à jour est donc désactivée et non supprimée.

### <a name="link-infotips"></a>Lier info-bulles

-   Si un lien requiert une explication supplémentaire, **fournissez l’explication dans une explication supplémentaire dans un contrôle de texte distinct ou une** [info-bulle](ctrl-tooltips-and-infotips.md), mais pas les deux. Utilisez des phrases complètes et terminez la ponctuation. Le fait de fournir les deux est inutile si le texte est identique et confus si le texte est différent.

    ![capture d’écran d’un lien avec du texte supplémentaire ](images/ctrl-links-image16.png)

    Dans cet exemple, une explication supplémentaire fournit des informations supplémentaires sur le lien.

    ![capture d’écran d’un lien avec une info-bulle ](images/ctrl-links-image17.png)

    Dans cet exemple, une info-bulle fournit des informations supplémentaires.

-   **Ne fournissez pas d’info-bulle qui consiste simplement à redéfinir le texte du lien.**

    **Incorrect :**

    ![capture d’écran d’un lien avec une info-bulle redondante ](images/ctrl-links-image18.png)

    Dans cet exemple, l’info-bulle risque de gêner les utilisateurs.

## <a name="text"></a>Texte

-   N’attribuez pas de [clé d’accès](glossary.md). Les liens sont accessibles à l’aide de la touche Tab.
-   **Utilisez des liens qui fournissent des informations descriptives spécifiques sur le résultat d’un clic sur le lien**, en utilisant autant de texte que nécessaire. Le texte du lien doit indiquer le résultat d’un clic sur le lien. **Les utilisateurs doivent être en mesure de prédire avec précision le résultat d’un lien à partir de son texte de lien et d’une info-bulle facultative.**

    **Incorrect :**

    ![capture d’écran d’un lien d’avertissement de sécurité ](images/ctrl-links-image19.png)

    Dans cet exemple, même si le lien semble important, son étiquette est trop générale. Il est plus probable que les utilisateurs cliquent sur un lien plus spécifique.

-   Pour les liens inline :
    -   Conservez la mise en majuscules et la ponctuation du texte.
    -   N’incluez pas de ponctuation de fin dans le lien, sauf si le texte est une question.
    -   Connectez-vous à la partie la plus pertinente du texte et choisissez un texte de lien suffisamment grand pour être facile à cliquer.

        **Correct :**

        Accédez à un groupe de discussion.

        **Incorrect :**

        Accédez à un groupe de discussion.

        Dans ces exemples, « Go » n’est pas la partie la plus pertinente du texte et n’est pas assez grand pour faire un bon point de vue, tandis que « newsgroup » est.

    -   **Évitez de placer deux liens Inline différents à côté les uns des autres.** Les utilisateurs sont susceptibles de croire qu’il s’agit d’un lien unique.

        **Incorrect :**

        Pour plus d’informations, consultez Recommandations pour l’expérience utilisateur.

        Dans cet exemple, « UX » et « Guidelines » sont deux liens différents.

-   Pour les liens indépendants (non inline) :
    -   Utilisez la mise [en majuscules de style phrase](glossary.md).
    -   N’utilisez pas de ponctuation de fin, sauf si le lien est une question.
    -   Utilisez tout le texte comme lien.
-   Utilisez des liens qui sont clairement différenciés des autres liens à l’écran. Les utilisateurs doivent être en mesure de prédire et de faire la distinction avec précision entre les cibles de lien.

    **Incorrect :**

    Rechercher un logiciel antivirus

    Procurez-vous un logiciel antivirus

    **Correct :**

    Comment savoir si un logiciel antivirus est installé

    Installer un logiciel antivirus

    Dans l’exemple incorrect, la distinction entre les deux liens n’est pas claire.

-   N’ajoutez pas de clic ou cliquez ici pour le texte du lien. Cela n’est pas nécessaire, car un lien implique un clic. En outre, cliquez ici, et ici seul, ne communiquez aucune information sur le lien lorsqu’il est lu par un lecteur d’écran.

    **Incorrect :**

    Cliquez ici pour obtenir une description.

    **Correct :**

    Description

    Dans les exemples incorrects, « cliquez ici » va sans dire et ne transmet aucune information sur le lien.

**Liens de navigation**

-   **Démarrez le lien avec un nom et décrivez clairement où se trouve le clic sur le lien.** N’utilisez pas de ponctuation finale. À l’occasion, vous devrez peut-être démarrer des liens de navigation avec un verbe, mais n’utilisez pas de verbes qui réitèrent la navigation qui est déjà impliquée par le fait de lier, comme View, Open ou Go to.
-   **Présente un lien de navigation en tant qu’URL s’il accède à une page Web et que vous vous attendez à ce que les utilisateurs cible rappellent l’URL et la tapent dans un navigateur.** Si possible, concevez ces URL de manière à ce qu’elles soient courtes et faciles à mémoriser.
-   **Si le lien contient une URL vers un site Web commençant par « www », omettez le nom de protocole https://et utilisez le texte en minuscules.**

    **Incorrect :**

    https://www.microsoft.com

    `www.microsoft.com`

    **Correct :**

    microsoft.com

    Dans les exemples incorrects, les termes « https:// » et « www » ne sont pas fournis.

**Liens de tâches**

-   **Démarrez le lien avec un verbe impératif et décrivez clairement la tâche effectuée par le lien.** N’utilisez pas de ponctuation finale.
-   **Mettez fin au lien avec des points de suspension si la commande a besoin d’informations supplémentaires (y compris une confirmation) pour que l’opération aboutisse.** N’utilisez pas de points de suspension lorsque l’exécution de la tâche réussie consiste à afficher une autre fenêtre uniquement lorsque des informations supplémentaires sont nécessaires pour effectuer la tâche.

    Imprimer...

    Dans cet exemple, la page... lien de commande affiche une boîte de dialogue Imprimer pour obtenir plus d’informations.

    Imprimer

    En revanche, dans cet exemple, un lien de commande d’impression imprime une seule copie d’un document sur l’imprimante par défaut sans intervention supplémentaire de l’utilisateur.

    **L’utilisation correcte des ellipses est importante pour indiquer que les utilisateurs peuvent effectuer des choix supplémentaires avant d’effectuer la tâche, ou peuvent annuler entièrement la tâche**. Le signal visuel fourni par des points de suspension permet aux utilisateurs d’explorer vos logiciels sans crainte.

-   **Si nécessaire, mettez fin à un lien de tâche avec « maintenant » pour le distinguer d’un lien de navigation.**

    Télécharger les fichiers

    Télécharger les fichiers maintenant

    Dans cet exemple, l’option « Télécharger des fichiers » permet d’accéder à une page de téléchargement de fichiers, tandis que « télécharger des fichiers maintenant » exécute en fait la commande.

**Liens d’aide**

Pour obtenir des instructions et des exemples, consultez [l’aide](winenv-help.md)de.

**Lier info-bulles**

-   Utilisez des phrases entières et terminez la ponctuation.

Pour obtenir des instructions et des exemples supplémentaires, consultez [info-bulles et info-bulles](ctrl-tooltips-and-infotips.md).

## <a name="documentation"></a>Documentation

Lorsque vous faites référence à des liens :

-   Utilisez le texte de lien exact, y compris sa mise en majuscules, mais n’incluez pas les points de suspension.
-   Pour décrire l’interaction de l’utilisateur, utilisez le clic.
-   Dans la mesure du possible, mettez en forme le texte du lien en gras. Sinon, placez le texte du lien entre guillemets uniquement si nécessaire pour éviter toute confusion.

Exemple : pour démarrer l’analyse, cliquez sur **analyser un ordinateur**.

 

