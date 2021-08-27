---
title: Boîtes de dialogue (notions de base sur la conception)
description: Une boîte de dialogue est une fenêtre secondaire qui permet aux utilisateurs d’exécuter une commande, demande aux utilisateurs une question, ou fournit aux utilisateurs des informations ou des commentaires sur la progression.
ms.assetid: 2ded9f30-d45f-4027-a85d-4e7d0e412793
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: dbcf7887a90c7407224bbfbb0c9b316ccb426f76
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880013"
---
# <a name="dialog-boxes-design-basics"></a>Boîtes de dialogue (notions de base sur la conception)

> [!NOTE]
> ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Une boîte de dialogue est une fenêtre secondaire qui permet aux utilisateurs d’exécuter une commande, demande aux utilisateurs une question, ou fournit aux utilisateurs des informations ou des commentaires sur la progression.

![capture d’écran identifiant les éléments de boîte de dialogue ](images/win-dialog-box-image1.png)

Boîte de dialogue classique.

Les boîtes de dialogue se composent d’une barre de titre (pour identifier la commande, la fonctionnalité ou le programme d’où provient une boîte de dialogue), une instruction principale facultative (pour expliquer l’objectif de l’utilisateur avec la boîte de dialogue), plusieurs contrôles dans la zone de contenu (pour présenter les options) et des boutons de validation (pour indiquer comment l’utilisateur veut valider la tâche

Les boîtes de dialogue ont deux types fondamentaux :

-   Les **boîtes de dialogue modales** obligent les utilisateurs à se terminer et à fermer avant de continuer avec la fenêtre propriétaire. Ces boîtes de dialogue sont mieux utilisées pour les tâches critiques ou peu fréquentes qui requièrent l’achèvement avant de continuer.
-   Les **boîtes de dialogue non modales** permettent aux utilisateurs de basculer entre la boîte de dialogue et la fenêtre propriétaire comme vous le souhaitez. Ces boîtes de dialogue sont préférables pour les tâches fréquentes, répétitives et en cours d’utilisation.

**Une boîte de dialogue de tâche est une boîte de dialogue implémentée à l’aide de l’interface de programmation d’applications (API) de la boîte de dialogue tâche.** Ils se composent des parties suivantes, qui peuvent être assemblées dans différentes combinaisons :

-   Une **barre de titre** pour identifier la fonctionnalité de l’application ou du système à partir de laquelle la boîte de dialogue provient.
-   **Instruction principale**, avec une icône facultative, pour identifier l’objectif de l’utilisateur à l’aide de la boîte de dialogue.
-   **Zone de contenu** pour les contrôles et les informations descriptives.
-   **Zone de commande** pour les boutons de validation, notamment un bouton Annuler et des options facultatives, et ne plus afficher cet &lt; élément &gt; .
-   Une **zone de note** pour les explications et l’aide facultatives, en général destinées aux utilisateurs moins expérimentés.

![capture d’écran d’une boîte de dialogue de tâche standard ](images/win-dialog-box-image2.png)

Boîte de dialogue de tâche standard.

**Les boîtes de dialogue de tâches sont recommandées chaque fois que cela est approprié, car elles sont faciles à créer et donnent une apparence cohérente.** les boîtes de dialogue de tâches requièrent Windows Vista ou version ultérieure. elles ne conviennent donc pas aux versions antérieures de Microsoft Windows.

Un volet de tâches est semblable à une boîte de dialogue, à la différence qu’il est présenté dans un volet de fenêtre et non dans une fenêtre distincte. Par conséquent, les volets des tâches ont une apparence plus directe et contextuelle que les boîtes de dialogue. Même si techniquement, ils ne sont pas les mêmes, les **volets des tâches sont similaires aux boîtes de dialogue que leurs instructions sont présentées dans cet article**.

![capture d’écran d’un volet de tâches classique ](images/win-dialog-box-image3.png)

Un volet de tâches classique.

Les [fenêtres de propriétés](win-property-win.md) sont un type spécialisé de boîte de dialogue qui permet d’afficher et de modifier les propriétés d’un objet, d’une collection d’objets ou d’un programme. En outre, les fenêtres de propriétés prennent en charge plusieurs tâches, tandis que les boîtes de dialogue prennent en charge une seule tâche ou étape dans une tâche. Étant donné que leur utilisation est spécialisée, les **fenêtres de propriétés sont couvertes dans un autre ensemble d’instructions**.

Les boîtes de dialogue peuvent avoir des [onglets](ctrl-tabs.md)et, si c’est le cas, elles sont appelées boîtes de dialogue à onglets. Les fenêtres de propriétés sont déterminées par leur présentation de propriétés, et non par l’utilisation d’onglets.

**Remarque :** Les instructions relatives à la [disposition](vis-layout.md), à la [gestion des fenêtres](win-window-mgt.md), aux boîtes de dialogue communes, aux [fenêtres de propriétés](win-property-win.md), aux [assistants](win-wizards.md), aux [confirmations](mess-confirm.md), aux [messages d’erreur](mess-error.md)et aux [messages d’avertissement](mess-warn.md) sont présentées dans des articles distincts.

## <a name="is-this-the-right-user-interface"></a>S’agit-il de l’interface utilisateur appropriée ?

Pour vous décider, posez-vous les questions suivantes :

-   **L’objectif est-il de fournir des informations aux utilisateurs, de poser une question aux utilisateurs ou d’autoriser les utilisateurs à sélectionner des options pour exécuter une commande ou une tâche ?** Si ce n’est pas le cas, utilisez une autre interface utilisateur.
-   **L’objectif est-il d’afficher et de modifier les propriétés d’un objet, d’une collection d’objets ou d’un programme ?** Dans ce cas, utilisez une fenêtre ou une [barre d’outils](cmd-toolbars.md) de [Propriétés](win-property-win.md) à la place.
-   **L’objectif est-il de présenter une collection de commandes ou d’outils ?** Dans ce cas, utilisez une fenêtre de barre d’outils ou de [palette](glossary.md).
-   **L’objectif est-il de vérifier que l’utilisateur souhaite effectuer une action ?** Y a-t-il une bonne raison de ne pas continuer et un risque raisonnable que les utilisateurs ne peuvent parfois pas ? Si c’est le cas, utilisez une [confirmation](mess-confirm.md).
-   **L’objectif est-il de fournir un message d’erreur ou d’avertissement ?** Dans ce cas, utilisez un [message d’erreur](mess-error.md) ou un message d' [Avertissement](mess-warn.md).
-   Est l’objectif de :
    -   Ouvrir des fichiers
    -   Enregistrer les fichiers
    -   Ouvrir des dossiers
    -   Rechercher ou remplacer du texte
    -   Imprimer un document
    -   Sélectionner les attributs d’une page imprimée
    -   Sélectionner une police
    -   Choisir une couleur
    -   Rechercher un fichier, un dossier, un ordinateur ou une imprimante
    -   Rechercher des utilisateurs, des ordinateurs ou des groupes dans Microsoft Active Directory
    -   Demander un nom d’utilisateur et un mot de passe ?

Dans ce cas, utilisez la [boîte de dialogue commune](win-common-dlg.md) appropriée à la place. La plupart de ces boîtes de dialogue courantes sont extensibles.

-   **L’objectif est-il d’effectuer une tâche à plusieurs étapes qui requiert plusieurs fenêtres ?** Si c’est le cas, utilisez à la place un [Assistant](win-wizards.md) ou un [Workflow de tâche](glossary.md) .
-   **L’objectif est d’informer les utilisateurs d’un événement système ou de programme qui n’est pas lié à l’activité de l’utilisateur actuel, qui ne nécessite pas d’action immédiate de l’utilisateur, et les utilisateurs peuvent librement ignorer ?** Si c’est le cas, utilisez une [notification](mess-notif.md) à la place.
-   **L’objectif est-il d’afficher l’état du programme ?** Dans ce cas, utilisez une [barre d’État](ctrl-status-bars.md) à la place.
-   **Serait-il préférable d’utiliser l’interface utilisateur sur place ?** Les boîtes de dialogue peuvent rompre le workflow de l’utilisateur en exigeant une attention particulière. Parfois, cette interruption dans le Flow est justifiée, par exemple lorsque l’utilisateur doit effectuer une action qui est en dehors du contexte actuel. Dans d’autres cas, une meilleure approche consiste à présenter l’interface utilisateur en contexte, soit directement avec l’interface utilisateur sur place (par exemple, un volet de tâches), soit à la demande à l’aide d’une [Divulgation progressive](ctrl-progressive-disclosure-controls.md).
-   **L’objectif est-il d’afficher un problème d’entrée utilisateur non critique ou une condition spéciale ?** Si c’est le cas, utilisez plutôt une [bulle](ctrl-balloons.md) .
-   **Pour les flux de tâches, serait-il préférable d’utiliser une autre page ?** En général, vous souhaitez qu’une tâche passe d’une page à l’autres au sein d’une même fenêtre. Utilisez les boîtes de dialogue pour confirmer les commandes sur place, pour obtenir une entrée pour les commandes sur place, et pour effectuer des tâches secondaires autonomes qui sont meilleures effectuées indépendamment et en dehors du processus principal de tâche.
-   **Pour sélectionner des options, les utilisateurs sont susceptibles de modifier les options ?** Si ce n’est pas le cas, envisagez des alternatives, telles que :
    -   En utilisant les options par défaut sans demander, mais en permettant aux utilisateurs d’apporter des modifications ultérieurement.
    -   Fournir une version avec des options (par exemple, **Imprimer...** dans un menu) ainsi qu’une version sans options (par exemple, **Imprimer** dans la barre d’outils). En règle générale, les commandes de barre d’outils doivent être immédiats et éviter d’afficher des boîtes de dialogue.
-   **Pour sélectionner des options, existe-t-il une méthode plus simple et plus directe pour présenter les options ?** Si c’est le cas, envisagez d’autres solutions, telles que :
    -   Utilisation d’un [bouton partagé](ctrl-command-buttons.md) pour sélectionner les variations d’une commande.
    -   Utilisation d’un sous-menu pour les commandes, les cases à cocher, les cases d’option et les listes simples.

![Capture d’écran montrant un menu et un sous-menu.](images/win-dialog-box-image4.png)

![capture d’écran d’un menu et d’un sous-menu ](images/win-dialog-box-image5.png)

Dans ces exemples, des sous-menus sont utilisés à la place de boîtes de dialogue pour des sélections simples.

## <a name="design-concepts"></a>Principes de conception

En cas d’utilisation correcte, les boîtes de dialogue sont un excellent moyen de fournir de la puissance et de la flexibilité à votre programme. En cas d’utilisation inutilisée, les boîtes de dialogue constituent un moyen simple de gêner les utilisateurs, d’interrompre leur déroulement et de faire en sorte que le programme semble indirect et fastidieux à utiliser. **Les boîtes de dialogue modales demandent une attention aux utilisateurs.** Les boîtes de dialogue sont souvent plus faciles à implémenter que les autres interfaces utilisateur. elles ont donc tendance à être surutilisées.

**Une boîte de dialogue est plus efficace lorsque ses caractéristiques de conception correspondent à son utilisation.** La conception d’une boîte de dialogue est en grande partie déterminée par son objectif (pour offrir des options, poser des questions, fournir des informations ou des commentaires), taper (modale ou non modale) et interaction de l’utilisateur (obligatoire, réponse facultative ou accusé de réception), tandis que son utilisation est déterminée en grande partie par son contexte (utilisateur ou programme initié), probabilité d'

Pour concevoir des boîtes de dialogue efficaces, utilisez efficacement les éléments suivants :

-   Texte de la boîte de dialogue
-   Instructions principales
-   Ne plus afficher cet &lt; élément, &gt; option

**Si vous n’avez qu’une seule chose...**

Assurez-vous que la conception de la boîte de dialogue (déterminée par son rôle, son type et son interaction avec l’utilisateur) correspond à son utilisation (déterminée par son contexte, sa probabilité de l’action de l’utilisateur et la fréquence d’affichage).

## <a name="usage-patterns"></a>Modèles d’usage

Les boîtes de dialogue ont plusieurs modèles d’utilisation :

-   Les boîtes de dialogue de questions (à l’aide de boutons) demandent aux utilisateurs une seule question ou confirment une commande, et utilisent des réponses simples dans les boutons de commande disposés horizontalement.
-   Les boîtes de dialogue de questions (à l’aide des liens de commande) demandent aux utilisateurs une seule question ou sélectionnent une tâche à effectuer, et utilisent des réponses détaillées dans des liens de commande organisés verticalement.
-   Les boîtes de dialogue de choix présentent aux utilisateurs un ensemble de choix, généralement pour spécifier une commande de façon plus complète. Contrairement aux boîtes de dialogue de questions, les boîtes de dialogue de choix peuvent poser plusieurs questions.
-   Les boîtes de dialogue de progression présentent aux utilisateurs des commentaires sur la progression pendant une longue opération (plus de cinq secondes), ainsi qu’une commande pour annuler ou arrêter l’opération.
-   Les boîtes de dialogue d’information affichent les informations demandées par l’utilisateur.

## <a name="guidelines"></a>Consignes

### <a name="general"></a>Général

-   **N’utilisez pas de boîtes de dialogue déroulantes.** N’utilisez pas les boîtes de dialogue qui requièrent l’utilisation d’une barre de défilement pour s’afficher complètement pendant une utilisation normale. Reconcevez plutôt la boîte de dialogue. Envisagez d’utiliser la [Divulgation progressive](ctrl-progressive-disclosure-controls.md) ou les [onglets](ctrl-tabs.md).
-   **N’avez pas de barre de menus ou de barre d’État.** Au lieu de cela, vous pouvez fournir un accès aux commandes et à l’État directement dans la boîte de dialogue elle-même, ou en utilisant des menus contextuels sur les contrôles appropriés.

    -   **Exception :** Les barres de menus sont acceptables lorsqu’une boîte de dialogue est utilisée pour implémenter une fenêtre principale (par exemple, un utilitaire).

    **Incorrect :**

    ![capture d’écran d’une boîte de dialogue avec une barre de menus ](images/win-dialog-box-image6.png)

    Dans cet exemple, l’option Rechercher des certificats est une boîte de dialogue non modale avec une barre de menus.

-   Si une boîte de dialogue nécessite une attention immédiate et que le programme n’est pas actif, **flashez son bouton de la barre des tâches trois fois pour attirer l’attention et laissez-le en surbrillance.** Ne rien faire d’autre : ne restaurez pas ou n’activez pas la fenêtre et ne jouez aucun effet sonore. Au lieu de cela, respectez la sélection de l’état de la fenêtre de l’utilisateur et laissez l’utilisateur activer la fenêtre quand elle est prête.
-   Pour obtenir des instructions et des exemples supplémentaires, consultez [barre des tâches](winenv-taskbar.md).

### <a name="modal-dialog-boxes"></a>Boîtes de dialogue modales

-   **À utiliser pour les tâches critiques ou peu fréquentes qui requièrent l’achèvement avant de continuer.**
-   Utilisez un [modèle de validation différée](glossary.md) pour que les modifications ne prennent pas effet tant qu’elles ne sont pas explicitement validées.
-   **Implémentez à l’aide d’une boîte de dialogue de tâches chaque fois que nécessaire pour obtenir une apparence cohérente.** les boîtes de dialogue de tâches requièrent Windows Vista ou version ultérieure. elles ne conviennent donc pas aux versions antérieures de Windows.

### <a name="modeless-dialog-boxes"></a>Boîtes de dialogue non modales

-   **À utiliser pour les tâches fréquentes, répétitives et en cours d’utilisation.**
-   Utilisez un [modèle de validation immédiate](glossary.md) afin que les modifications prennent effet immédiatement.
-   Pour les boîtes de dialogue non modales, utilisez un bouton de commande fermer explicite dans la boîte de dialogue pour fermer la fenêtre. Pour les deux, utilisez un bouton Fermer dans la barre de titre pour fermer la fenêtre.
-   **Envisagez de rendre les boîtes de dialogue non modales ancrables.** Les boîtes de dialogue non modales ancrables permettent un positionnement plus flexible.

![capture d’écran d’une boîte de dialogue non modale et Ancrable ](images/win-dialog-box-image7.png)

certaines boîtes de dialogue non modales utilisées dans Microsoft Office sont ancrables.

### <a name="multiple-dialog-boxes"></a>Plusieurs boîtes de dialogue

-   **N’affichez pas plus d’une boîte de dialogue de choix appartenant à la fois à partir d’une boîte de dialogue de choix de propriétaire.** L’affichage de plusieurs rend la signification des boutons de validation difficile à comprendre pour les utilisateurs. Vous pouvez afficher d’autres types de boîtes de dialogue (telles que des boîtes de dialogue de questions) si nécessaire.
-   **Pour une séquence de boîtes de dialogue associées, envisagez d’utiliser une boîte de dialogue de plusieurs pages si possible.** Utilisez des boîtes de dialogue individuelles s’ils ne sont pas clairement liés.

### <a name="multi-page-dialog-boxes"></a>Boîtes de dialogue à plusieurs pages

-   Utilisez une boîte de dialogue à plusieurs pages au lieu de boîtes de dialogue individuelles lorsque vous avez la séquence suivante de pages associées :
    -   Une seule page d’entrée (facultatif)
    -   Page de progression
    -   Une seule page de résultats

La page d’entrée est facultative, car la tâche a peut-être été lancée ailleurs. **Cela donne à l’expérience résultante une sensation stable, simple et légère.**

![capture d’écran d’une barre de progression ](images/win-dialog-box-image8.png)

![capture d’écran du message « aucun problème détecté » ](images/win-dialog-box-image9.png)

dans cet exemple, Windows les diagnostics réseau sont constitués de pages de progression et de résultats.

-   **N’utilisez pas de boîte de dialogue à plusieurs pages si la page d’entrée est une boîte de dialogue standard.** Dans ce cas, la cohérence de l’utilisation d’une boîte de dialogue standard est plus importante.
-   **N’utilisez pas les boutons suivant ou précédent et ne disposez pas de plus de trois pages.** Les boîtes de dialogue à plusieurs pages sont destinées aux tâches à étape unique avec des commentaires. Ce ne sont pas des [assistants](win-wizards.md), qui sont utilisés pour les tâches en plusieurs étapes. Les assistants ont une sensation importante et indirecte par rapport aux boîtes de dialogue à plusieurs pages.
-   **Dans la page entrée, utilisez des boutons de commande ou des liens de commande spécifiques pour lancer la tâche.**
-   **Utilisez un bouton Annuler sur les pages d’entrée et de progression et un bouton Fermer dans la page résultats.**

**Développeurs :** Vous pouvez créer des boîtes de dialogue de tâches de plusieurs pages à l’aide du message de [ \_ \_ page de navigation TDM](../controls/tdm-navigate-page.md) .

### <a name="presentation"></a>Présentation

Pour faciliter la recherche et l’accès aux boîtes de dialogue, associez clairement la boîte de dialogue à sa source et travaillez bien avec plusieurs moniteurs :

-   **Affichez initialement les boîtes de dialogue « centrées » en haut de la fenêtre propriétaire.** Pour l’affichage suivant, envisagez de l’afficher à son dernier emplacement (par rapport à la fenêtre propriétaire) si cela est susceptible d’être plus pratique.

![diagramme de la boîte de dialogue centrée sur la fenêtre en arrière-plan ](images/win-dialog-box-image10.png)

Les boîtes de dialogue du centre sont initialement au-dessus de la fenêtre propriétaire.

-   **Si une boîte de dialogue est contextuelle, affichez-la près de l’objet à partir duquel elle a été lancée.** Toutefois, mettez-le hors service (décalage de préférence vers le droite et vers la droite) pour que l’objet ne soit pas couvert par la boîte de dialogue.

![diagramme du décalage de la boîte de dialogue vers le-vers la droite ](images/win-dialog-box-image11.png)

Les propriétés d’un objet s’affichent à côté de l’objet.

-   **Pour les boîtes de dialogue non modales, affichez initialement en haut de la fenêtre propriétaire pour faciliter la recherche.** Si l’utilisateur active la fenêtre propriétaire, cela peut masquer la boîte de dialogue non modale.
-   **Si nécessaire, ajustez l’emplacement initial afin que la boîte de dialogue entière soit visible dans le moniteur cible.** Si une fenêtre redimensionnable est plus grande que le moniteur cible, réduisez-la pour l’ajuster.
-   **Quand une boîte de dialogue est réaffichée, envisagez de l’afficher dans le même État que le dernier accès.** À la fermeture, enregistrez l’analyse utilisée, la taille de la fenêtre, l’emplacement et l’État (agrandie ou restaurée). À l’affichage, restaurez la taille, l’emplacement et l’état de la boîte de dialogue enregistrée à l’aide de l’analyse appropriée. Envisagez également de rendre ces attributs persistants entre les instances de programme pour chaque utilisateur.
-   **Pour les fenêtres redimensionnables, définissez une taille de fenêtre minimale s’il existe une taille au-dessous de laquelle le contenu n’est plus utilisable.** Envisagez de modifier la présentation afin que le contenu soit utilisable à des tailles plus petites.

![capture d’écran des boutons du lecteur multimédia centré ](images/win-dialog-box-image12.png)

dans cet exemple, Lecteur Windows Media modifie son format lorsque la fenêtre devient trop petite pour le format standard.

-   **N’utilisez pas l’attribut Always on.**
    -   **Exception :** À utiliser uniquement lorsqu’une boîte de dialogue implémente une opération essentiellement modale, mais qu’elle doit être interrompue brièvement pour accéder à la fenêtre propriétaire. Par exemple, lorsque vous vérifiez l’orthographe d’un document, les utilisateurs peuvent occasionnellement conserver la boîte de dialogue vérification de l’orthographe et accéder au document pour corriger les erreurs.

Pour plus d’informations et d’exemples, consultez [gestion des fenêtres](win-window-mgt.md).

### <a name="title-bars"></a>Barres de titre

-   **Les boîtes de dialogue n’ont pas d’icônes de barre de titre.** Les icônes de barre de titre sont utilisées comme une distinction visuelle entre les fenêtres [principales](glossary.md) et les [fenêtres secondaires](glossary.md).
    -   **Exception :** Si une boîte de dialogue est utilisée pour implémenter une fenêtre principale (comme un utilitaire) et qu’elle apparaît donc dans la barre des tâches, elle comporte une icône de barre de titre. Dans ce cas, optimisez le titre à afficher dans la barre des tâches en plaçant d’abord les informations distinctives.
-   **Les boîtes de dialogue possèdent toujours un bouton Fermer.** Les boîtes de dialogue non modales peuvent également avoir un bouton réduire. Les boîtes de dialogue redimensionnables peuvent avoir un bouton Agrandir.
-   **Ne désactivez pas le bouton Fermer.** Le fait de disposer d’un bouton Fermer aide les utilisateurs à garder le contrôle en leur permettant de fermer les fenêtres qu’ils ne souhaitent pas.
    -   **Exception :** Pour les boîtes de dialogue de progression, vous pouvez désactiver le bouton Fermer si la tâche doit s’exécuter jusqu’à la fin pour atteindre un état valide ou empêcher la perte de données.
-   **Le bouton fermer de la barre de titre doit avoir le même effet que le bouton Annuler ou fermer** dans la boîte de dialogue. Ne donnez jamais le même effet que OK.
-   Si la légende et l’icône de la barre de titre sont déjà affichées d’une manière bien visible vers le haut de la fenêtre, vous pouvez masquer la légende et l’icône de la barre de titre pour éviter la redondance. Toutefois, vous devez toujours définir en interne un titre approprié pour une utilisation par Windows.

### <a name="interaction"></a>Interaction

-   **Lorsqu’ils sont affichés, les boîtes de dialogue initiées par l’utilisateur doivent toujours prendre le focus.** Les boîtes de dialogue lancées par le programme ne doivent pas prendre le focus, car l’utilisateur peut interagir avec une autre fenêtre. Une telle interaction incorrectement liée à la boîte de dialogue peut avoir des conséquences inattendues.
-   **Affectez le focus d’entrée initial au contrôle que les utilisateurs sont le plus susceptibles d’interagir avec en premier**, ce qui est généralement (mais pas toujours) le premier contrôle interactif. Évitez d’attribuer le focus d’entrée initial à un lien d’aide.
-   **Pour la navigation au clavier, l’ordre des tabulations doit passer dans un ordre logique, généralement de gauche à droite, de haut en bas.** En général, l’ordre de tabulation suit l’ordre de lecture, mais envisagez d’effectuer ces exceptions :

    -   Placez les contrôles les plus couramment utilisés plus tôt dans l’ordre de tabulation.
    -   Placez les liens d’aide en bas d’une boîte de dialogue, après les boutons valider dans l’ordre de tabulation.

    Lorsque vous affectez une commande, supposez que les utilisateurs affichent les boîtes de dialogue pour leur rôle prévu. par exemple, les utilisateurs affichent des boîtes de dialogue de choix pour effectuer des choix, pas pour les consulter, puis cliquer sur Annuler.

-   **Appuyez sur la touche ÉCHAP pour toujours fermer une boîte de dialogue active.** Cela est vrai pour les boîtes de dialogue avec annuler ou fermer, et même si annuler a été renommé en fermer, car les résultats ne peuvent plus être annulés.

**Clés d’accès**

-   **Dans la mesure du possible, assignez des clés d’accès uniques à tous les contrôles interactifs ou à leurs étiquettes.** Les [zones de texte en lecture seule](ctrl-text-boxes.md) sont des contrôles interactifs (parce que les utilisateurs peuvent les faire défiler et copier du texte) pour tirer parti des clés d’accès. **N’affectez pas de clés d’accès à :**
    -   **Boutons OK, annuler et fermer.** Enter et ESC sont utilisés pour leurs clés d’accès. Toutefois, attribuez toujours une clé d’accès à un contrôle qui signifie OK ou annuler, mais qui a une étiquette différente.

        ![capture d’écran de la boîte de dialogue supprimer le fichier ](images/win-dialog-box-image13.png)

        Dans cet exemple, une clé d’accès est assignée au bouton de validation positif.

    -   **Étiquettes de groupe.** Normalement, les contrôles individuels d’un groupe sont affectés à des clés d’accès, de sorte que l’étiquette du groupe n’a pas besoin d’une. Toutefois, en cas de pénurie de clés d’accès, assignez une clé d’accès à l’étiquette de groupe et non aux contrôles individuels.
    -   Les **boutons d’aide génériques,** accessibles via la touche F1.
    -   **Étiquettes de lien.** Il y a souvent trop de liens pour affecter des clés d’accès uniques, et les traits de soulignement souvent utilisés pour signifier des liens masquent les traits de soulignement des touches d’accès. Accédez aux liens avec la touche Tab à la place.
    -   **Noms d’onglets.** Les onglets sont recycles à l’aide des touches CTRL + TAB et Ctrl + Maj + Tab.
    -   **Boutons de navigation étiquetés « ... ».** Il n’est pas possible d’affecter des clés d’accès à ces boutons de navigation de manière unique.
    -   **Contrôles sans étiquette,** tels que les contrôles spin, les boutons de commande graphique et les contrôles de divulgation progressive sans étiquette.
    -   **Texte ou étiquettes statiques sans étiquette pour les contrôles qui ne sont pas interactifs,** tels que les barres de progression.

-   **Dans la mesure du possible, affectez des clés d’accès pour les commandes couramment utilisées en fonction des affectations de touches d’accès standard**. Bien que les attributions de clé d’accès cohérentes ne soient pas toujours possibles, elles sont certainement préférées en particulier pour les boîtes de dialogue fréquemment utilisées.
-   **Affectez d’abord les clés d’accès du bouton de validation pour vous assurer qu’elles ont les attributions de clés standard.** S’il n’existe pas d’affectation de clé standard, utilisez la première lettre du premier mot. Par exemple, les boutons clé d’accès pour Oui et pas de validation doivent toujours être « Y » et « N », quels que soient les autres contrôles de la boîte de dialogue.
-   **Pour faciliter la recherche des clés d’accès, assignez les touches d’accès rapide à un caractère qui apparaît au début de l’étiquette,** idéalement le premier caractère, même s’il existe un mot clé qui apparaît plus tard dans l’étiquette.
-   **Préférer les caractères dont la largeur est large,** par exemple w, m et les majuscules.
-   **Préférez une consonne distinctive ou une voyelle,** telle que « x » en quittant.
-   **Évitez d’utiliser des caractères qui rendent le soulignement difficile à voir,** par exemple (de la plupart des problèmes aux moins problématiques) :
    -   Lettres d’une largeur d’un pixel, comme i et l.
    -   Lettres avec descendants, comme g, j, p, q et y.
    -   Lettres à côté d’une lettre avec un descendant.

Pour obtenir des instructions et des exemples supplémentaires, consultez [clavier](inter-keyboard.md).

### <a name="progress-dialogs"></a>Boîtes de dialogue de progression

Pour les tâches de longue durée, **Supposons que les utilisateurs effectuent une autre opération pendant que la tâche se termine**. Concevez la tâche pour qu’elle s’exécute sans assistance.

-   **Présenter aux utilisateurs une boîte de dialogue de commentaires sur l’avancement si une opération prend plus de cinq secondes pour s’exécuter**, ainsi qu’une commande pour annuler ou arrêter l’opération.
    -   **Exception :** Pour les assistants et les flux de tâches, utilisez une boîte de dialogue modale pour la progression uniquement si la tâche reste sur la même page (par opposition à l’avancement vers une autre page) et que les utilisateurs ne peuvent rien faire en attendant. Dans le cas contraire, utilisez une page de progression ou une progression sur place.
-   Si l’opération est une tâche de longue durée (plus de 30 secondes) et peut être exécutée en arrière-plan, utilisez une boîte de dialogue de progression non modale pour que les utilisateurs puissent continuer à utiliser votre programme en attente.
-   Boîtes de dialogue de progression non modales :
    -   Utilisez un bouton réduire sur la barre de titre.
    -   Sont affichés dans la barre des tâches.
-   Implémentez les boîtes de dialogue de progression non modales afin qu’elles continuent à s’exécuter même si la fenêtre propriétaire est fermée.

![capture d’écran de la boîte de dialogue Copier avec la barre de progression ](images/win-dialog-box-image14.png)

Dans cet exemple, la copie de fichier se poursuit même si la fenêtre propriétaire est fermée.

-   **Fournissez un bouton de commande pour arrêter l’opération si elle prend plus de quelques secondes ou si elle peut ne pas se terminer.** Étiquette le bouton Annuler si l’annulation retourne l’environnement à son état précédent (sans effets secondaires); Sinon, étiquetez l’arrêt du bouton pour indiquer qu’il laisse l’opération partiellement terminée intacte. Vous pouvez modifier l’étiquette du bouton Annuler pour arrêter au milieu de l’opération, à un moment donné, il n’est pas possible de rétablir l’état précédent de l’environnement.

![capture d’écran de la boîte de dialogue avec le bouton Annuler ](images/win-dialog-box-image15.png)

Dans cet exemple, l’arrêt du diagnostic du problème n’a aucun effet secondaire.

-   **Fournissez un bouton de commande pour suspendre l’opération si elle prend plus de plusieurs minutes, et si elle a un effet sur la capacité des utilisateurs à effectuer des tâches.** Cela ne force pas l’utilisateur à choisir entre la fin de la tâche et la réalisation de son travail.
-   **Rassemblez autant d’informations que possible avant de commencer la tâche.**
-   **Si des problèmes récupérables sont détectés, les utilisateurs doivent gérer tous les problèmes détectés à la fin de la tâche.** Si cela ne s’avère pas pratique, les utilisateurs peuvent traiter les problèmes dès qu’ils se produisent.
-   **Ne pas abandonner les tâches suite à des erreurs récupérables.**

![capture d’écran de la boîte de dialogue avec le bouton Réessayer ](images/win-dialog-box-image16.png)

dans cet exemple, Windows Explorer permet aux utilisateurs de poursuivre la tâche après une erreur récupérable.

-   **Signalez les problèmes en mettant la barre de progression en rouge.**

![capture d’écran de la barre de progression et bouton Réessayer ](images/win-dialog-box-image17.png)

Dans cet exemple, un disque amovible a été supprimé au cours d’une copie de fichier.

-   **Si les résultats sont clairement évidents pour les utilisateurs, fermez la boîte de dialogue de progression automatiquement en cas de réussite.** Dans le cas contraire, utilisez uniquement les commentaires pour signaler des problèmes :
    -   Pour afficher les commentaires simples, affichez les commentaires dans la boîte de dialogue de progression, puis modifiez le bouton Annuler pour fermer.
    -   Pour afficher des commentaires détaillés, fermez la boîte de dialogue progression et affichez une boîte de dialogue d’information.

**N’utilisez pas de notification pour les commentaires d’achèvement.** Utilisez une boîte de dialogue de progression ou une [notification de réussite d’action](mess-notif.md), mais pas les deux.

**Temps restant**

-   **Utilisez les formats d’heure suivants.** Commencez par le premier des formats suivants, où la plus grande unité de temps n’est pas égale à zéro, puis passe au format suivant une fois que la plus grande unité de temps devient zéro.

**Pour les barres de progression :**

**Si les informations connexes sont affichées au format deux-points :**

Temps restant : h heures, m minutes

Temps restant : m minutes, s secondes

Temps restant : s secondes

**Si l’espace à l’écran est à un niveau Premium :**

h h, m min restant

m min, s secondes restantes

s secondes restantes

**Sinon :**

h heures, m minutes restantes

m minutes, s secondes restantes

s secondes restantes

**Pour les barres de titre :**

hh : mm restant

mm : SS restant

0 : SS restant

Ce format compact affiche d’abord les informations les plus importantes afin qu’elles ne soient pas tronquées dans la barre des tâches.

-   **Effectuez des estimations précises, mais n’attribuez pas une précision fausse.** Si la plus grande unité est hours, indiquez les minutes (si significatives) mais pas les secondes.

**Incorrect :**

hh heures, mm minutes, SS secondes

-   **Maintenez l’estimation à jour.** Mettre à jour les estimations de temps restant au moins toutes les 5 secondes.
-   **Concentrez-vous sur le temps restant** , car il s’agit des informations que les utilisateurs ont le plus de soin. Indiquez le temps total écoulé uniquement lorsque des scénarios où le temps écoulé est utile (par exemple, lorsque la tâche est susceptible d’être répétée). Si l’estimation du temps restant est associée à une barre de progression, n’avez pas de texte d’achèvement de pourcentage, car ces informations sont transmises par la barre de progression elle-même.
-   **Corriger par programmation.** Utilisez des unités singulières lorsque le nombre est un.

**Incorrect :**

1 minute, 1 seconde

-   **Utilisez les majuscules comme pour les phrases.**

Pour plus d’informations et d’exemples, consultez [barres de progression](progress-bars.md).

### <a name="icons-and-graphics"></a>Icônes et graphiques

**Graphismes**

-   **N’utilisez pas de graphiques de grande taille qui ne servent à rien, au-delà de l’espace de remplissage.** Conservez plutôt l’apparence simple.

**Incorrect :**

![capture d’écran de la boîte de dialogue avec un grand graphique ](images/win-dialog-box-image18.png)

Dans cet exemple, le grand graphique n’a aucun effet.

**Icônes de la barre de titre**

-   **Les boîtes de dialogue n’ont pas d’icônes de barre de titre.**
    -   **Exception :** Si une boîte de dialogue est utilisée pour implémenter une fenêtre principale (comme un utilitaire) et qu’elle apparaît donc dans la barre des tâches, elle comporte une icône de barre de titre.

**Icônes de corps**

-   **Choisissez l’icône de corps en fonction du modèle de conception :**



| Modèle | Icône de corps |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| **Boîtes de dialogue de questions**<br/>      | Programme, fonctionnalité, objet, icône d’avertissement (si une perte potentielle de données ou un accès système), un avertissement de sécurité ou aucun.<br/> |
| **Boîtes de dialogue de choix**<br/>        | Aucun.<br/>                                                                                                           |
| **Boîtes de dialogue de progression**<br/>      | Aucun (mais peut avoir une animation).<br/>                                                                               |
| **Boîtes de dialogue d’information**<br/> | Aucun.<br/>                                                                                                           |



 

-   **Incorrect :**

![capture d’écran de la boîte de dialogue avec icône d’avertissement ](images/win-dialog-box-image19.png)

Dans cet exemple, une icône d’avertissement est utilisée de manière incorrecte pour une question qui n’implique pas la perte potentielle de données ou l’accès au système.

- **Envisagez d’utiliser des icônes pour aider les utilisateurs à reconnaître visuellement les fonctionnalités de votre programme.** Cette technique est particulièrement efficace lorsque les icônes sont facilement reconnaissables et utilisées à plusieurs endroits de votre programme.

![capture d’écran de la boîte de dialogue favoris avec l’icône d’étoile ](images/win-dialog-box-image20.png)

Dans cet exemple, l’icône d’étoile jaune représente les favoris. l’icône est facilement identifiable et est utilisée de manière cohérente tout au long Windows pour représenter les favoris.

-   **Utilisez des icônes pour aider les utilisateurs à reconnaître l’objet en question.**

![capture d’écran de la boîte de dialogue avec l’icône PowerPoint ](images/win-dialog-box-image21.png)

Dans cet exemple, l’icône de l’objet aide les utilisateurs à reconnaître le type de fichier ouvert ou enregistré.

-   **Envisagez d’utiliser des icônes pour vous aider à rendre les fonctionnalités explicites.**

![images des flèches indiquant comment positionner le moniteur ](images/win-dialog-box-image22.png)

Dans cet exemple, ces icônes aident les utilisateurs à visualiser l’effet de leurs fonctionnalités.

-   **Utilisez une icône dans les boîtes de dialogue à propos de Box pour la personnalisation de l’application.**

![capture d’écran de la boîte de dialogue à propos de avec le logo Windows ](images/win-dialog-box-image23.png)

Dans cet exemple, une image bitmap est utilisée dans la zone à propos de pour identifier et marquer l’application.

**Icônes de note**

-   **Si vous avez une note de bas de page, envisagez d’utiliser une icône de note de bas de page pour résumer le sujet du pied de page.**

![capture d’écran de la boîte de dialogue avec icône de note de bas de page ](images/win-dialog-box-image24.png)

Dans cet exemple, l’icône de note de bas de page indique que la question a des implications en matière de sécurité.

-   **N’utilisez pas d’icône de note de bas de page qui répète l’icône de corps.**
-   **N’utilisez pas les icônes standard d’erreur ou d’information.** Les conditions d’erreur doivent être transmises via l’icône de corps et les notes de bas de page sont toujours pour plus d’informations, ce qui rend l’icône d’information redondante. Toutefois, vous pouvez utiliser l’icône d’avertissement standard et le bouclier de sécurité jaune pour alerter les utilisateurs en cas de conséquences risquées.

Pour plus d’informations et d’exemples, consultez [icônes](vis-icons.md).

### <a name="commit-buttons"></a>Boutons de validation

**Remarques :**

-   Ces recommandations ne s’appliquent pas aux boîtes de dialogue de questions à l’aide de liens de commande, car ce modèle utilise des liens de commande au lieu de boutons.
-   \[Faites- \] \[ le et n’effectuez pas \] les réponses positives et négatives, respectivement, à l’instruction principale.

**Général**

-   **Choisissez les boutons valider en fonction du modèle de conception :**

    
| | | <strong>Modèle</strong><br /> | <strong>Boutons de validation</strong><br /> | | <strong>Boîtes de dialogue de questions (à l’aide des boutons)</strong><br /> | L’un des ensembles suivants de commandes concises : oui/non, oui/non/annuler, [do it]/Cancel, [do it]/[do it], [do it]/[do it]/Cancel.<br /> | | <strong>Boîtes de dialogue de questions (à l’aide de liens)</strong><br /> | Annuler.<br /> | | <strong>Boîtes de dialogue de choix</strong><br /> | <ul><li>Boîtes de dialogue modales : OK/Annuler ou [do it]/Cancel</li><li>Boîtes de dialogue non modales : bouton Fermer dans la boîte de dialogue et la barre de titre</li><li>Volet des tâches : bouton Fermer dans la barre de titre</li></ul> | | <strong>Boîtes de dialogue de progression</strong><br /> | Utilisez annuler si retourne l’environnement à son état précédent (sans effet secondaire); Sinon, utilisez arrêter.<br /> | | <strong>Boîtes de dialogue d’information</strong><br /> | Plus.<br /> | 


    

     

-   **Tous les boutons de validation, à l’exception de apply Results, permettent de fermer la fenêtre de boîte de dialogue.**
-   **Ne confirmez pas les boutons de validation.** Cela peut être très ennuyeux. **Exceptions :**

    -   L’action est potentiellement catastrophique.
    -   L’action est clairement incohérente avec d’autres actions.
    -   Si ce n’est pas le cas, l’action peut entraîner une perte significative de données, de temps ou d’effort pour le compte de l’utilisateur.

    Pour obtenir des instructions et des exemples supplémentaires, consultez la rubrique [confirmations](mess-confirm.md).

-   **Ne désactivez pas les boutons de validation. Exceptions**
    -   **Si les utilisateurs doivent s’élever pour apporter une modification, désactivez les boutons de validation positifs jusqu’à ce que l’utilisateur apporte une modification.** Cela empêche les utilisateurs d’élever simplement une fenêtre en les forçant à cliquer sur Annuler.
    -   Pour plus d’exceptions, consultez [désactivation ou suppression de contrôles et attribution de messages d’erreur](#disabling-or-removing-controls-vs-giving-error-messages).
-   **Aligner à droite les boutons de validation sur une seule ligne dans la partie inférieure de la boîte de dialogue,** mais au-dessus de la zone de pied de page. Procédez ainsi, même s’il existe un seul bouton de validation (tel que OK).

    **Incorrect :**

    ![capture d’écran du message avec le bouton centré OK ](images/win-dialog-box-image25.png)

    Dans cet exemple, le bouton OK est incorrectement centré.

-   **Présentez les boutons de validation dans l’ordre suivant :**
    1.  OK/ \[ do it \] /Yes
    2.  \[Ne le faites pas \] /non
    3.  Annuler
    4.  Appliquer (le cas échéant)
    5.  Aide (le cas échéant)
-   **Si vous avez de nombreux boutons de validation associés, consolidez-les à l’aide de boutons partagés**.
-   **Utilisez une séparation claire des boutons valider (qui referment la fenêtre) et tous les autres boutons de commande (tels que avancé).**

**Réponse aux instructions principales**

-   **Utilisez des boutons de validation positifs qui sont des réponses spécifiques à l’instruction principale, plutôt que des étiquettes génériques telles que OK ou oui/non.** Les utilisateurs doivent pouvoir comprendre les options en lisant le texte du bouton seul. **Exceptions :**
    -   Utilisez Close pour les boîtes de dialogue qui n’ont pas de paramètres, comme des boîtes de dialogue d’information. N’utilisez jamais Close pour les boîtes de dialogue qui ont des paramètres.
    -   Utilisez OK lorsque les réponses « spécifiques » sont toujours génériques, telles que enregistrer, sélectionner ou choisir. Utilisez OK lors de la modification d’un paramètre spécifique ou d’une collection de paramètres.
    -   **Pour les boîtes de dialogue héritées sans instruction principale, vous pouvez utiliser des étiquettes génériques telles que OK.** Souvent, ces boîtes de dialogue ne sont pas conçues pour effectuer une tâche spécifique, ce qui empêche les réponses plus spécifiques.
    -   Certaines tâches nécessitent une réflexion plus approfondie et une lecture minutieuse pour les utilisateurs pour prendre des décisions avisées. C’est généralement le cas avec des [confirmations](mess-confirm.md). **Dans ce cas, vous pouvez utiliser des étiquettes de bouton de validation générique pour forcer les utilisateurs à lire les instructions principales et à empêcher les décisions de Hasty.**

        **Correct :**

        ![capture d’écran du message avec les boutons Oui et non](images/win-dialog-box-image26.png)

        Dans cet exemple, l’utilisation de boutons de validation oui/non force les utilisateurs à lire au moins l’instruction principale.

-   **Vous pouvez également ajouter le mot « tout de même » à l’étiquette du bouton validation positive pour indiquer que la boîte de dialogue présente une raison pour ne pas continuer** et que les utilisateurs doivent lire attentivement la boîte de dialogue avant de continuer.

    **Correct :**

    ![capture d’écran du message et bouton désinstaller tout de même ](images/win-dialog-box-image27.png)

    Dans cet exemple, « tout de même » est ajouté à l’étiquette du bouton de validation pour indiquer que les utilisateurs doivent continuer avec soin.

-   **Utilisez CANCEL ou Close pour les boutons de validation négatifs au lieu de réponses spécifiques à l’instruction principale.** Bien souvent, les utilisateurs se rendent compte qu’ils ne souhaitent pas exécuter une tâche une fois qu’ils voient une boîte de dialogue. Si annuler ou fermer ont été réétiquetés pour des réponses spécifiques, les utilisateurs devaient lire avec soin tous les boutons de validation pour déterminer comment annuler. **L’étiquetage de l’annulation et de la fermeture permet une recherche plus facile. Exceptions**
    -   **N’utilisez pas oui/annuler.** Utilisez toujours oui/non en tant que paire.
    -   **Utilisez une réponse spécifique lorsque l’annulation est ambiguë.**
-   **Ne mappez pas les étiquettes génériques à leur signification spécifique avec le texte dans la zone de contenu.** Utilisez plutôt des étiquettes de bouton de validation spécifiques ou une boîte de dialogue de question à l’aide de liens si les étiquettes sont longues.

    **Incorrect :**

    ![capture d’écran du message avec des boutons inclairs ](images/win-dialog-box-image28.png)

    Dans cet exemple, OK est mappé à continue, Cancel est mappé à reste sur la page.

**Boutons Oui et non**

-   **Préférer des réponses spécifiques aux boutons Oui et non.** Bien qu’il n’y ait rien de mal à utiliser Oui et non, les réponses spécifiques peuvent être comprises plus rapidement, ce qui permet une prise de décision efficace. Toutefois, [les confirmations](mess-confirm.md) comportent généralement des boutons Oui et non pour permettre aux utilisateurs de [réfléchir](mess-confirm.md) à la confirmation avant de répondre.
-   **Utilisez les boutons Oui et non uniquement pour répondre à des questions oui ou non.** L’instruction principale doit être naturellement exprimée sous la forme d’une question oui ou non. N’utilisez jamais OK et annuler pour les questions oui ou aucune.

    **Incorrect :**

    ![Capture d’écran montrant un message avec un « OK » pour une question oui-non.](images/win-dialog-box-image29.png)

    **Correct :**

    ![capture d’écran du message avec Oui pour la même question ](images/win-dialog-box-image30.png)

    **Conseillé**

    ![capture d’écran du message avec l’exécution de la même question ](images/win-dialog-box-image31.png)

    Dans ces exemples, les réponses Oui et non sont de bonnes réponses à Oui et aucune question, mais les réponses spécifiques sont encore mieux adaptées.

-   **Vous pouvez considérer l’instruction principale comme une question oui ou non, si les boutons de validation avec une formulation spécifique ne sont pas longs ou maladroits.** Vous pouvez également utiliser des liens de commande pour obtenir des réponses plus longues (cinq mots ou plus) à l’instruction principale.

    **Incorrect :**

    ![capture d’écran du message avec des étiquettes de bouton de mot ](images/win-dialog-box-image32.png)

    **Correct :**

    ![capture d’écran du message avec des étiquettes de bouton Oui/non ](images/win-dialog-box-image33.png)

    La formulation spécifique dans l’exemple incorrect est trop longue, donc l’exemple correct utilise Oui et non.

-   **N’utilisez pas de boutons Oui et non si la signification de la réponse no n’est pas claire.** Dans ce cas, utilisez des réponses spécifiques à la place.

**Boutons OK**

-   **Dans les boîtes de dialogue modales, le fait de cliquer sur OK signifie appliquer les valeurs, effectuer la tâche et fermer la fenêtre.**
-   **N’utilisez pas les boutons OK pour répondre aux questions.**
-   **N’affectez pas de clés d’accès à OK, car entrez est la clé d’accès pour le bouton par défaut.** Cela rend les autres clés d’accès plus faciles à assigner.
-   **Étiquette correcte des boutons OK.** Le bouton OK doit être étiqueté OK, pas OK ou OK.
-   **N’utilisez pas de boutons OK pour les erreurs ou les avertissements.** Les problèmes ne sont jamais OK. Utilisez à la place la fermeture.

    **Incorrect :**

    ![capture d’écran du message avec le bouton OK ](images/win-dialog-box-image34.png)

    Dans cet exemple, la fermeture doit être utilisée à la place de OK.

-   **N’utilisez pas les boutons OK dans les boîtes de dialogue non modales.** Au lieu de cela, les boîtes de dialogue non modales doivent utiliser des boutons de validation spécifiques à la tâche (par exemple, Rechercher). Toutefois, certaines boîtes de dialogue non modales requièrent uniquement un bouton Fermer.

**Bouton Annuler**

-   **Le fait de cliquer sur annuler signifie abandonner toutes les modifications, annuler la tâche, fermer la fenêtre et rétablir l’état précédent de l’environnement, sans aucun effet secondaire.** Pour les boîtes de dialogue de choix imbriquées, le fait de cliquer sur Annuler dans la boîte de dialogue choix du propriétaire signifie que toutes les modifications apportées par les boîtes de dialogue de choix sont également abandonnées.
-   **Fournissez un bouton Annuler pour permettre aux utilisateurs d’abandonner explicitement les modifications.** Les boîtes de dialogue requièrent un point de sortie clair. Ne dépendez pas des utilisateurs qui recherchent le bouton Fermer dans la barre de titre.

    -   **Exception :** Ne fournissez pas de bouton Annuler pour les boîtes de dialogue sans paramètres. Les boutons OK et fermer ont le même effet que l’annulation dans ce cas.

    **Incorrect :**

    ![capture d’écran du message avec le bouton OK uniquement ](images/win-dialog-box-image35.png)

    Dans cet exemple, le fait d’avoir uniquement un bouton Fermer dans la barre de titre fait apparaître comme si les utilisateurs n’ont pas de choix.

-   **N’utilisez pas les boutons Annuler pour répondre aux questions.**

    **Incorrect :**

    ![capture d’écran du message avec OK pour Oui-aucune question ](images/win-dialog-box-image36.png)

    Dans cet exemple, OK et Cancel ne sont pas utilisés correctement pour répondre à une question oui ou non.

-   **N’affectez pas de clés d’accès pour annuler, car ESC est la touche d’accès.** Cela rend les autres clés d’accès plus faciles à assigner.
-   **N’utilisez pas les boutons Annuler dans les boîtes de dialogue non modales.** Au lieu de cela, utilisez plutôt Close.
-   **Ne désactivez pas le bouton Annuler.** Les utilisateurs doivent toujours être en mesure d’annuler les boîtes de dialogue.
    -   **Exception :** Vous pouvez désactiver le bouton Annuler dans une boîte de dialogue de progression s’il y a un point pendant lequel l’opération ne peut pas être annulée. Toutefois, une meilleure solution consiste à concevoir des opérations de ce type pour qu’elles soient toujours annulables.

**Boutons Fermer**

-   **Utilisez les boutons Fermer pour les boîtes de dialogue non modales, ainsi que les dialogues modaux qui ne peuvent pas être annulés.**
-   **En cliquant sur Fermer, vous fermez la fenêtre de boîte de dialogue, en laissant les effets secondaires existants.** N’utilisez pas Done, car il ne s’agit pas d’une construction impérative. Pour les boîtes de dialogue de choix imbriquées, le fait de cliquer sur Fermer dans la boîte de dialogue choix du propriétaire signifie que toutes les modifications apportées par les boîtes de dialogue de choix sont conservées.
-   **Placez un bouton Fermer explicite dans le corps de la boîte de dialogue.** Les boîtes de dialogue requièrent un point de sortie clair. Ne dépendez pas des utilisateurs qui recherchent le bouton Fermer dans la barre de titre.
-   **Assurez-vous que le bouton fermer de la barre de titre a le même effet que annuler ou fermer.**
-   **N’affectez pas de clés d’accès pour fermer, car ESC est la clé d’accès.** Cela rend les autres clés d’accès plus faciles à assigner.

**Appliquer des boutons**

-   **N’utilisez pas de boutons appliquer dans les boîtes de dialogue qui ne sont pas des feuilles de propriétés ou des panneaux de contrôle.** Le bouton appliquer signifie appliquer les modifications en attente, mais laissez la fenêtre ouverte. Cela permet aux utilisateurs d’évaluer les modifications avant de fermer la fenêtre. Toutefois, seules les feuilles de propriétés et les panneaux de contrôle ont ce besoin.

    **Incorrect :**

    ![capture d’écran de la boîte de dialogue avec le bouton appliquer ](images/win-dialog-box-image37.png)

    Dans cet exemple, une boîte de dialogue Choice a un bouton Apply.

**Boutons de validation pour les boîtes de dialogue indirectes**

**Remarque :** Les boîtes de dialogue indirectes sont affichées en dehors du contexte, soit en raison d’un résultat indirect d’une tâche, soit en raison d’un problème lié à un processus système ou en arrière-plan. Pour les boîtes de dialogue indirectes, le bouton Annuler est ambigu, car cela peut signifier l’annulation de la boîte de dialogue ou l’annulation de l’intégralité de la tâche.

-   **Si les utilisateurs ont besoin d’annuler la boîte de dialogue et la tâche, attribuez des boutons de validation pour les deux.** Étiquetez le bouton qui annule la boîte de dialogue avec une réponse négative à l’instruction principale. Étiquetez le bouton qui annule l’intégralité de la tâche avec annuler. L’utilisation de l’annulation permet à la boîte de dialogue d’être utilisée dans de nombreux contextes.

    **Correct :**

    ![capture d’écran de la boîte de dialogue avec enregistrer/ne pas enregistrer ](images/win-dialog-box-image38.png)

    dans cet exemple, cette boîte de dialogue est affichée en Windows Paint à la suite d’une commande New ou Exit lorsque le graphique n’a pas été enregistré. Ne pas enregistrer ferme la boîte de dialogue sans enregistrer, tandis que Cancel annule la commande New ou Exit.

    **Incorrect :**

    ![capture d’écran de la boîte de dialogue avec les boutons Oui/non ](images/win-dialog-box-image39.png)

    dans cet exemple, il n’existe aucun moyen d’annuler la tâche (en fermant Office barre de raccourcis) qui a conduit à afficher cette boîte de dialogue. Cette boîte de dialogue a besoin d’un bouton Annuler.

-   **Si les utilisateurs doivent simplement annuler la boîte de dialogue, mais pas la tâche, utilisez un bouton avec une réponse négative spécifique à l’instruction principale** et n’avez pas de bouton Annuler.

    ![capture d’écran de la boîte de dialogue avec exécuter/ne pas exécuter ](images/win-dialog-box-image24.png)

    dans cet exemple, cette boîte de dialogue s’affiche indirectement à la suite de la navigation vers une page Web qui installe un contrôle de ActiveX. L’utilisation de Cancel serait ambiguë ici. donc, n’utilisez pas.

Pour plus d’informations et d’exemples, consultez [boutons de commande](ctrl-command-buttons.md).

### <a name="command-links"></a>Liens de commande

-   **Présentez un ensemble de commandes de longue durée à l’aide de liens de commande, au lieu de boutons de commande ou d’une combinaison de cases d’option et d’un bouton OK.** Cela permet aux utilisateurs de répondre d’un simple clic. Toutefois, cette approche ne fonctionne que pour une seule question.
-   **Commencez par présenter les liens de commande les plus couramment utilisés.** L’ordre qui en résulte doit suivre à peu près la probabilité d’utilisation, mais également avoir un Flow logique.
    -   **Exception :** Les liens de commande qui aboutissent à tout doivent être placés en premier.
-   Si un lien de commande requiert une explication supplémentaire, **fournissez une explication supplémentaire.** Les explications supplémentaires décrivent la raison pour laquelle les utilisateurs peuvent souhaiter choisir la commande, ou ce qui se passe si la commande est sélectionnée.
-   **N’utilisez pas d’explications supplémentaires qui sont des reformulations de mot du lien de commande.** Utilisez une explication supplémentaire uniquement lorsque vous ne pouvez pas rendre un lien de commande explicite. Si vous fournissez une explication supplémentaire pour un lien de commande, cela ne signifie pas que vous devez les fournir pour toutes les commandes.

![capture d’écran de la boîte de dialogue avec des options de recherche de texte ](images/win-dialog-box-image40.png)

Dans cet exemple, l’explication supplémentaire décrit les implications de l’une des options.

-   **Utilisez des expressions qui commencent par un verbe, sans ponctuation finale.**
-   **Si une commande est fortement recommandée, envisagez d’ajouter « (recommandé) » à l’étiquette.** Veillez à ajouter à l’étiquette du lien, et non à l’explication supplémentaire.
-   **Si une commande est destinée uniquement aux utilisateurs expérimentés, envisagez d’ajouter « (avancé) » à l’étiquette.** Veillez à ajouter à l’étiquette du lien, et non à l’explication supplémentaire.
-   **Fournissez toujours un bouton Annuler explicite**. N’utilisez pas de lien de commande à cet effet.

**Incorrect :**

![capture d’écran de la boîte de dialogue avec lien ne pas quitter ](images/win-dialog-box-image41.png)

Dans cet exemple, la boîte de dialogue utilise un lien de commande au lieu d’un bouton Annuler.

Pour plus d’informations et d’exemples, consultez [liens de commande](ctrl-command-links.md).

### <a name="dont-show-this-ltitemgt-again"></a>Ne plus afficher cet &lt; élément &gt;

-   **Envisagez d’utiliser l' &lt; option ne plus afficher cet élément &gt; pour permettre aux utilisateurs de supprimer une boîte de dialogue périodique, uniquement s’il n’existe pas de meilleure solution.** Il est préférable de toujours afficher la boîte de dialogue si les utilisateurs en ont vraiment besoin, ou simplement l’éliminer si ce n’est pas le cas.
-   **Utilisez cette formulation spécifique &lt; pour remplacer &gt; l’élément par l’élément spécifique.** Par exemple, ne plus afficher ce rappel. Quand vous faites référence à une boîte de dialogue en général, utilisez ne plus afficher ce message.
-   **Indiquez clairement quand l’entrée utilisateur sera utilisée pour les futures valeurs par défaut** en ajoutant la phrase suivante sous l’option : vos sélections seront utilisées par défaut à l’avenir.
-   **Ne sélectionnez pas l’option par défaut. Si la boîte de dialogue ne doit être affichée qu’une seule fois, faites-le sans demander.** N’utilisez pas cette option comme excuse pour importuner les utilisateurs à s’assurer que le comportement par défaut n’est pas ennuyeux.

**Incorrect :**

![capture d’écran du message demandant une question inutile ](images/win-dialog-box-image42.png)

Dans cet exemple, le message ne doit être affiché qu’une seule fois. Vous n’avez pas besoin de vous demander.

-   **Rendez le paramètre persistant pour chaque utilisateur.**
-   **Si les utilisateurs sélectionnent l’option et cliquent sur Annuler, cette option n’est pas prise en compte.** Ce paramètre est une méta-option, donc il ne suit pas le comportement d’annulation standard qui ne laisse aucun effet secondaire. Notez que si les utilisateurs ne souhaitent pas voir la boîte de dialogue à l’avenir, ils veulent également l’annuler.
-   Si les utilisateurs peuvent avoir besoin de restaurer ces boîtes de dialogue, fournissez une commande **restaurer les messages** dans la boîte de dialogue Options du programme.

### <a name="ask-me-later"></a>Me redemander ultérieurement

-   Indiquez cette option pour ignorer une boîte de dialogue uniquement quand :
    -   **La boîte de dialogue est indirecte**, de sorte que les utilisateurs sont susceptibles de se concentrer sur une autre tâche.
    -   **Les utilisateurs doivent répondre, mais pas immédiatement**, afin qu’ils puissent continuer à travailler.
    -   **La question nécessite une réflexion ou un effort suffisants** pour que les utilisateurs puissent prendre de meilleures décisions si le temps est écoulé.
    -   **La boîte de dialogue ou l’option s’affichera automatiquement plus tard** (afin que les utilisateurs soient vraiment invités plus tard).
-   **Incorrect :**
-   ![capture d’écran du message avec l’option me demander plus tard ](images/win-dialog-box-image43.png)
-   Dans cet exemple, la question est suffisamment simple pour que l’ajout d’une option me demander ultérieurement ne complique que cela.
-   Dans le cas contraire, attendez-vous à ce que les utilisateurs répondent maintenant, mais autorisez-les à fermer la boîte de dialogue normalement avec l’annulation ou la fermeture. Lorsqu’elle est utilisée correctement, cette option doit être rare.

### <a name="morefewer"></a>Plus ou moins

-   **Utilisez plus ou moins de boutons de divulgation progressive pour afficher ou masquer les options avancées ou rarement utilisées, les commandes ou les détails qui ne sont généralement pas nécessaires aux utilisateurs.** Cela simplifie la boîte de dialogue pour une utilisation classique. Ne masquez pas les options, les commandes ou les informations les plus couramment utilisées, car les utilisateurs ne les trouvent peut-être pas.

![capture d’écran de la boîte de dialogue avec le bouton plus d’options ](images/win-dialog-box-image24.png)

Dans cet exemple, les options rarement utilisées sont masquées par défaut.

-   **N’utilisez pas plus ou moins de contrôles à moins qu’il y ait vraiment plus de détails à afficher.** Ne vous contentez pas de réafficher les mêmes informations dans un format différent.
-   **N’utilisez pas plus ou moins de contrôles pour afficher l’aide.** Utilisez les liens d’aide ou les notes de bas de page à la place.
-   **Avec les boîtes de dialogue de tâche, évitez de combiner plus ou moins de contrôles avec ne plus afficher cet &lt; élément &gt; .** Cette combinaison a une apparence maladroite.
-   Pour obtenir des instructions sur l’étiquetage, consultez [Divulgation progressive](ctrl-progressive-disclosure-controls.md).

### <a name="footnotes"></a>Notes de bas de page

-   **Utilisez les notes de bas de page pour les informations qui ne sont pas essentielles à l’objectif d’une boîte de dialogue, mais que les utilisateurs peuvent trouver utiles pour prendre des décisions.** La plupart des utilisateurs doivent être en mesure d’ignorer les notes de bas de page et de prendre des décisions éclairées dans leur réponse à la boîte de dialogue.

![capture d’écran de la boîte de dialogue avec clarification de la note ](images/win-dialog-box-image44.png)

Dans cet exemple, les informations de la note de bas de page sont supplémentaires, et non essentielles.

### <a name="disabling-or-removing-controls-vs-giving-error-messages"></a>Désactivation ou suppression des contrôles et attribution de messages d’erreur

-   Quand un contrôle ne s’applique pas dans le contexte actuel, envisagez les options suivantes :
    -   **Supprimez le contrôle lorsqu’il n’existe aucun moyen pour les utilisateurs de l’activer, ou que les utilisateurs ne s’attendent pas à ce qu’ils s’appliquent et que son état ne change pas fréquemment.** Cela simplifie la boîte de dialogue et les utilisateurs ne le manquent pas. Le fait d’avoir un contrôle s’affiche et disparaît fréquemment.
    -   **Désactivez le contrôle lorsque les utilisateurs s’attendent à ce qu’ils s’appliquent fréquemment ou que son état change fréquemment, et que les utilisateurs puissent facilement déduire la raison pour laquelle le contrôle est désactivé.** La désactivation d’un bouton valider est un exemple de déduction simple lorsqu’il existe une seule zone de texte vide qui nécessite une entrée. Vous pouvez utiliser des [bulles](ctrl-balloons.md) pour afficher des problèmes d’entrée d’utilisateur non critiques avec des zones de texte et des listes déroulantes modifiables. Toutefois, si le problème ne peut pas être expliqué avec une bulle ou implique plusieurs contrôles, la déduction n’est plus facile.
    -   **Sinon, laissez le contrôle activé, mais fournissez un message d’erreur lorsqu’il est utilisé de manière incorrecte.** Si vous désactivez dans ce cas, il est difficile pour les utilisateurs de comprendre pourquoi le contrôle est désactivé. Les utilisateurs sont obligés de déterminer le problème via l’expérimentation et la logique déduite. Il est préférable de fournir un message d’erreur utile pour expliquer le problème de manière explicite.
-   **Conseil :** Si vous ne savez pas si vous devez désactiver un contrôle ou envoyer un message d’erreur, commencez par composer le message d’erreur que vous pouvez fournir. Si le message d’erreur contient des informations utiles que les utilisateurs cibles ne peuvent pas déduire rapidement, laissez le contrôle activé et donnez l’erreur. Sinon, désactivez le contrôle.
-   **Si vous désactivez un contrôle, désactivez également tous les contrôles associés**, tels que son étiquette, ses explications supplémentaires ou ses boutons de commande. Toutefois, ne désactivez pas les [zones de groupe](ctrl-group-boxes.md), l’étiquette de groupe ou l’explication du groupe, le cas échéant.

![capture d’écran de la boîte de dialogue avec des contrôles estompés ](images/win-dialog-box-image45.png)

Dans cet exemple, les étiquettes de zone de texte désactivée sont également désactivées, mais l’étiquette de groupe et l’explication des groupes ne le sont pas.

### <a name="required-input"></a>Entrée requise

-   Pour indiquer que les utilisateurs doivent fournir des informations dans un contrôle, envisagez les options suivantes :
    -   **N’indiquez rien, mais gérez les entrées requises manquantes avec des messages d’erreur.** Cette approche réduit l’encombrement et fonctionne bien si la plupart des entrées sont facultatives ou si les utilisateurs ne sont pas susceptibles d’ignorer des contrôles, ce qui réduit le nombre de messages d’erreur.
    -   **Indiquez l’entrée requise en utilisant un astérisque au début de l’étiquette.** Décrivez l’astérisque en utilisant l’une des deux opérations suivantes :

        -   Note de bas de page en bas de la zone de contenu qui indique l' \* entrée requise.
        -   Info-bulle sur l’astérisque indiquant une entrée requise.

        Cette approche fonctionne bien si le nombre de contrôles requis n’est pas important, mais si la plupart des contrôles sont requis.

        ![capture d’écran des étiquettes de zone de texte avec des astérisques ](images/win-dialog-box-image46.png)

        Dans cet exemple, des astérisques sont utilisés pour indiquer les entrées requises.

    -   **Si tous les contrôles nécessitent une entrée, indiquez « toutes les entrées requises » à un emplacement approprié en haut de la zone de contenu.** Cette approche réduit l’encombrement pour ce cas spécifique.
    -   **Indiquer les entrées facultatives avec « (facultatif) » après l’étiquette.** Cette approche fonctionne bien si la plupart des entrées sont nécessaires, mais dans le cas contraire.

-   **Pour des besoins de cohérence, essayez d’utiliser la même méthode pour indiquer les entrées requises dans votre programme.** En particulier, indiquez une entrée obligatoire ou facultative si nécessaire, mais évitez de les utiliser dans le même programme.

### <a name="error-handling"></a>Gestion des erreurs

-   Évitez les erreurs en utilisant des contrôles qui sont limités à une entrée utilisateur valide. Vous pouvez également réduire le nombre d’erreurs en fournissant des valeurs par défaut raisonnables.
-   Validez l’entrée d’utilisateur dès que possible, puis affichez les erreurs aussi près que possible du point d’entrée.
-   **Utilisez la gestion des erreurs non modale (erreurs ou bulles sur place) pour les problèmes d’entrée d’utilisateur.**
    -   **Utilisez des bulles pour les problèmes d’entrée d’utilisateur non critiques détectés dans une zone de texte ou immédiatement après qu’une zone de texte perd le focus.** Les bulles ne nécessitent pas d’espace d’écran disponible ou la disposition dynamique requise pour afficher des messages sur place. Affichez une seule bulle à la fois. Étant donné que le problème n’est pas critique, aucune icône d’erreur n’est nécessaire. Les bulles disparaissent quand l’utilisateur clique dessus, lorsque le problème est résolu ou après un délai d’attente.

        ![capture d’écran du message « caractère incorrect » ](images/win-dialog-box-image47.png)

        Dans cet exemple, une bulle indique un problème d’entrée tout en restant dans le contrôle.

-   **Utilisez des erreurs sur place pour la détection des erreurs différées**, généralement des erreurs trouvées en cliquant sur un bouton de validation. (N’utilisez pas d’erreurs sur place pour les paramètres qui sont validés immédiatement.) Il peut y avoir plusieurs erreurs sur place à la fois. Utilisez du texte normal et une icône d’erreur de 16x16 pixels, en les plaçant directement en regard du problème, dans la mesure du possible. Les erreurs sur place ne sont pas supprimées, sauf si l’utilisateur est validé et qu’aucune autre erreur n’est détectée.

    ![capture d’écran de la boîte de dialogue avec deux messages d’erreur ](images/win-dialog-box-image48.png)

    Dans cet exemple, une erreur sur place est utilisée pour une erreur trouvée en cliquant sur le bouton valider.

-   **Utilisez la gestion des erreurs modale (boîtes de dialogue de tâches ou boîtes de message) pour tous les autres problèmes,** y compris les erreurs qui impliquent plusieurs contrôles ou les erreurs non contextuelles ou non contextuelles trouvées par un clic sur un bouton de validation.
-   **Lorsqu’un problème d’entrée est détecté et signalé, définissez le focus d’entrée sur le premier contrôle avec les données incorrectes.** Faites défiler le contrôle vers l’affichage si nécessaire.

Pour plus d’informations et d’exemples, consultez [messages d’erreur](mess-error.md) et [bulles](ctrl-balloons.md).

### <a name="help"></a>Aide

-   Lorsque vous fournissez une assistance utilisateur, envisagez les options suivantes (classées par ordre de préférence) :
    -   Donnez aux contrôles interactifs des étiquettes explicites. Les utilisateurs sont plus susceptibles de lire les étiquettes sur des contrôles interactifs que tout autre texte.
    -   Fournissez des explications en contexte à l’aide d' [étiquettes de texte statiques](text-ui.md).
    -   Fournissez un lien d’aide spécifique vers une rubrique d’aide pertinente.
-   **Localisez les liens d’aide en bas de la zone de contenu de la boîte de dialogue.** Si la boîte de dialogue contient une note de bas de page et que le lien d’aide est associé, placez le lien d’aide dans la note de bas de page.

    ![capture d’écran de la boîte de dialogue avec le lien d’aide ](images/win-dialog-box-image40.png)

    Dans cet exemple, le lien d’aide s’applique à la boîte de dialogue entière.

    -   **Exception :** Si une boîte de dialogue contient plusieurs groupes de paramètres distincts qui ont des rubriques d’aide distinctes (peut-être dans des zones de groupe), recherchez les liens d’aide en bas des groupes.

-   **N’utilisez pas de liens vers des rubriques d’aide générales ou vagues ou des boutons d’aide génériques.** Les utilisateurs ignorent souvent l’aide générique.

Pour plus d’informations et d’exemples, consultez [l’aide](winenv-help.md)de.

### <a name="default-values"></a>Valeurs par défaut

-   Incluez un bouton de validation par défaut dans chaque boîte de dialogue.
-   Pour les boîtes de dialogue de questions :
    -   **Sélectionnez le niveau de sécurité le plus sûr (pour éviter la perte de données ou l’accès au système), la réponse la plus sécurisée étant la valeur par défaut.** Si la sécurité et la sécurité ne sont pas des facteurs, sélectionnez la réponse la plus probable ou la plus pratique.
        -   **Exception :** N’effectuez pas de réponse destructrice par défaut à moins qu’il existe un moyen simple et évident d’annuler la commande.
-   Pour les boîtes de dialogue de choix :
    -   Pour les valeurs par défaut initiales, **Sélectionnez la plus sûre (pour empêcher la perte de données ou l’accès système) et les valeurs les plus sécurisées pour chaque contrôle.** Si la sécurité et la sécurité ne sont pas des facteurs, sélectionnez les options les plus probables ou les plus pratiques.
    -   Pour les valeurs par défaut suivantes, **resélectionnez les options sélectionnées précédemment si ces valeurs sont susceptibles d’être répétées, ce qui est sûr et sécurisé.** Dans le cas contraire, sélectionnez les valeurs par défaut initiales.

![capture d’écran de la boîte de dialogue Imprimer ](images/win-dialog-box-image49.png)

Dans cet exemple, il est très probable que les utilisateurs choisissent les mêmes paramètres d’impression qu’à la dernière fois. Toutefois, le nombre de copies souhaitées est susceptible de changer. ce paramètre n’est donc pas resélectionné.

## <a name="recommended-sizing-and-spacing"></a>Dimensionnement et espacement recommandés

-   **prendre en charge la résolution d’écran minimale Windows Vista de 800 x 600 pixels.** Les dispositions peuvent être optimisées pour les fenêtres redimensionnables à l’aide d’une résolution d’écran de 1024 x 768 pixels.
-   **Utilisez des fenêtres redimensionnables quand cela est possible pour éviter les barres de défilement et les données tronquées.** Windows avec du contenu dynamique et des listes qui tirent le meilleur parti des fenêtres redimensionnables.
-   **Les fenêtres à taille fixe doivent être entièrement visibles et dimensionnées pour s’ajuster à la zone de travail.**
-   **Les fenêtres redimensionnables peuvent être optimisées pour des résolutions plus élevées, mais en fonction des besoins au moment de l’affichage de la résolution réelle de l’écran.**
-   **Choisissez une taille de fenêtre par défaut adaptée à son contenu.** N’hésitez pas à utiliser des tailles de fenêtre initiales supérieures si vous pouvez utiliser l’espace de manière efficace.

## <a name="text"></a>Texte

### <a name="general"></a>Général

-   **Supprimez le texte redondant.** Recherchez du texte redondant dans les titres, des instructions principales, des instructions supplémentaires, des zones de contenu, des liens de commande et des boutons de validation. En règle générale, laissez le texte intégral dans les instructions et les contrôles interactifs, et supprimez toute redondance des autres emplacements.
-   **Utilisez une formulation positive.** Une formulation positive est plus facile à comprendre pour les utilisateurs.

**Correct :**

Voulez-vous activer le partage de fichiers et d’imprimantes ?

**Incorrect :**

Voulez-vous désactiver le partage de fichiers et d’imprimantes ?

Toutefois, la formulation doit correspondre à la commande associée, même si la commande est négativement formulées ; par exemple, utilisez Disable pour confirmer une commande Disable.

-   **Si nécessaire, utilisez le mot « fenêtre » pour faire référence à la boîte de dialogue elle-même.**
-   **Utilisez la deuxième personne (« vous/votre ») pour indiquer aux utilisateurs la marche à suivre** dans la zone instructions et contenu principales. Souvent, la deuxième personne est impliquée.

**Exemples :**

Choisir les images que vous souhaitez imprimer

Choisir un compte

-   **Utilisez la première personne (« I/me/My ») pour permettre aux utilisateurs d’indiquer au programme ce qu’il doit faire** dans les contrôles de la zone de contenu qui répondent à l’instruction principale.

**Exemple :** Imprimez les photos sur mon appareil photo.

### <a name="dialog-box-titles"></a>Titres des boîtes de dialogue

-   **Utilisez le titre pour identifier la commande, la fonctionnalité ou le programme d’où provient une boîte de dialogue.**
    -   Si le dialogue est initié par l’utilisateur, identifiez-le à l’aide du nom de la commande ou de la fonctionnalité. **Exceptions :**
        -   Si une boîte de dialogue est affichée par de nombreuses commandes différentes, envisagez d’utiliser le nom du programme à la place.
        -   Si ce titre est redondant avec l’instruction principale, utilisez le nom du programme à la place.
    -   S’il s’agit d’un programme ou d’un système initié (et donc hors contexte), identifiez-le à l’aide du nom du programme ou de la fonctionnalité pour fournir le contexte.
    -   N’utilisez pas le titre pour expliquer ce que vous devez faire dans la boîte de dialogue qui est l’objectif de l’instruction principale.
-   Utilisez le nom de commande exact pour les noms basés sur une commande, mais n’incluez pas les points de suspension, le cas échéant. Vous pouvez inclure le titre de menu de la commande si nécessaire pour composer un bon titre. Exemple : pour un objet... dans un menu Insertion, utilisez l’objet insérer un titre.
-   **Si une boîte de dialogue non modale s’affiche dans la barre des tâches, optimisez le titre pour l’afficher sur la barre des tâches** en plaçant d’abord les informations distinctives. Exemples : « 66% terminé » et « 3 rappels ».
-   **N’incluez pas les mots « boîte de dialogue » ou « progression » dans le titre.** Ceci est implicite, et sa conservation permet aux utilisateurs de les analyser plus facilement.
-   Utilisez la mise [en majuscules de style titre](glossary.md), sans ponctuation finale.

### <a name="main-instructions"></a>Instructions principales

-   **Utilisez l’instruction principale pour décrire de façon concise ce que vous devez faire dans la boîte de dialogue.** L’instruction doit être une instruction spécifique, une direction impérative ou une question. Les bonnes instructions communiquent l’objectif de l’utilisateur avec la boîte de dialogue plutôt que de se concentrer uniquement sur les mécanismes de manipulation.
-   **Omettez l’instruction principale lorsque la seule chose que vous pouvez prononcer est évidente.** Dans ce cas, le contenu de la boîte de dialogue est explicite. Par exemple, les boîtes de dialogue courantes fichier ouvert et enregistrement de fichier n’ont pas besoin d’une instruction principale, car leur contexte et leur conception rendent leur objectif évident.
-   **Omettez les étiquettes de contrôle qui restatent l’instruction principale.** Dans ce cas, l’instruction principale prend la clé d’accès.

**Acceptable:**

![capture d’écran de la zone de texte avec étiquette redondante ](images/win-dialog-box-image50.png)

Dans cet exemple, l’étiquette de la zone de texte n’est qu’une REstate de l’instruction principale.

**Conseillé**

![capture d’écran de la même zone de texte avec une étiquette ](images/win-dialog-box-image51.png)

Dans cet exemple, l’étiquette redondante est supprimée, de sorte que l’instruction principale prend la clé d’accès.

-   **N’utilisez qu’une seule phrase complète.** Réduisez l’instruction principale aux informations essentielles. Si vous devez en expliquer davantage, utilisez des instructions supplémentaires.
-   **Utilisez des verbes spécifiques chaque fois que cela est possible.** Les verbes spécifiques (exemples : connexion, enregistrement, installation) sont plus explicites pour les utilisateurs que les verbes génériques (exemples : configurer, gérer, définir).
-   Utilisez la mise [en majuscules de style phrase](glossary.md).
-   **N’incluez pas de périodes finales si l’instruction est une instruction.** Si l’instruction est une question, incluez un point d’interrogation final.
-   **Pour les boîtes de dialogue de progression, utilisez une expression gerund pour expliquer brièvement l’opération en cours,** en terminant par des points de suspension. Exemple : impression de vos images...
-   **Conseil :** Vous pouvez évaluer une instruction principale en imaginant ce que vous feriez pour un ami. En cas de réponse avec l’instruction principale, il ne s’agit pas d’une instruction naturelle, sans aide ou difficile à retravailler.

### <a name="supplemental-instructions"></a>Instructions supplémentaires

-   **Si nécessaire, utilisez une instruction supplémentaire facultative pour présenter des informations supplémentaires utiles pour comprendre ou utiliser la page.** Vous pouvez fournir des informations plus détaillées et définir la terminologie.
-   **Si la boîte de dialogue est lancée par le programme ou par le système (et donc hors contexte), utilisez l’instruction supplémentaire pour expliquer pourquoi la boîte de dialogue s’est affichée.** Pour ces boîtes de dialogue, le contexte n’est généralement pas évident.
-   **Ne répétez pas l’instruction principale avec un libellé légèrement différent.** Au lieu de cela, omettez l’instruction supplémentaire s’il n’y a pas d’autres à ajouter.
-   Utilisez des phrases complètes, des majuscules de style phrase et des signes de ponctuation de fin.

### <a name="command-links"></a>Liens de commande

-   **Choisissez un texte de lien concis qui communique clairement et différencie ce que fait le lien de commande.** Elle doit être explicite et correspondre à l’instruction principale. Les utilisateurs ne doivent pas avoir à déterminer ce que signifie le lien ou la manière dont il diffère des autres liens.
-   **Toujours démarrer les liens de commande avec un verbe.**
-   Utilisez les majuscules comme pour les phrases.
-   N’utilisez pas de ponctuation finale.
-   **Si nécessaire, fournissez une explication supplémentaire en utilisant des phrases complètes et en terminant la ponctuation.** Toutefois, ajoutez ces explications uniquement si nécessaire, mais n’ajoutez pas d’explications à tous les liens de commande juste parce qu’un lien de commande en a besoin.

Pour plus d’informations et d’exemples, consultez Instructions relatives aux [liens de commande](ctrl-command-links.md) .

### <a name="commit-buttons"></a>Boutons de validation

-   **Utilisez des étiquettes de bouton de validation spécifiques qui sont logiques et qui sont une réponse à l’instruction principale.** Idéalement, les utilisateurs ne doivent pas lire d’autres éléments pour comprendre l’étiquette. Les utilisateurs sont beaucoup plus susceptibles de lire des étiquettes de bouton de commande que du texte statique.
-   **Démarrez les étiquettes de bouton de validation avec un verbe. Les exceptions sont OK, oui et non.**
-   Utilisez les majuscules comme pour les phrases.
-   N’utilisez pas de ponctuation finale.
-   Attribuez une [clé d’accès](glossary.md)unique.
    -   **Exception :** N’affectez pas de touches d’accès aux boutons OK et annuler, car les touches entrée et Échap sont leurs clés d’accès. Cela rend les autres clés d’accès plus faciles à assigner.

## <a name="documentation"></a>Documentation

Quand vous faites référence à des boîtes de dialogue :

-   Dans programmation et autres documents techniques, reportez-vous aux boîtes de dialogue sous forme de boîtes de dialogue. Partout ailleurs, reportez-vous aux boîtes de dialogue en fonction de leur titre. Si la barre de titre est masquée, reportez-vous à la boîte de dialogue à l’aide de l’instruction principale.
-   Si vous devez faire référence à une boîte de dialogue en général, utilisez la fenêtre de la documentation de l’utilisateur. Vous pouvez faire référence à une boîte de dialogue de question simple ou à une confirmation en tant que message.
-   Utilisez le titre exact ou le texte d’instruction principal, y compris la mise en majuscules.
-   Dans la mesure du possible, mettez en forme le titre en gras. Sinon, placez le titre entre guillemets uniquement si nécessaire pour éviter toute confusion.

exemple : dans **Sécurité Windows**, cliquez sur **autres Options**.

