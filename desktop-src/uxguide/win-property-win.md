---
title: Windows de propriété
description: La fenêtre Propriétés est le nom collectif des types suivants de feuille de propriétés d’interfaces utilisateur (IU) utilisés pour afficher et modifier les propriétés d’un objet ou d’une collection d’objets dans une boîte de dialogue. Inspecteur de propriété utilisé pour afficher et modifier les propriétés d’un objet ou d’une collection d’objets dans un volet. Options de la boîte de dialogue permettant d’afficher et de modifier les options d’une application.
ms.assetid: 18fc04da-9f84-4a44-9f3d-a9e29b121e7c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 73260459c1dc22ee488233f3c7edebe25203a811a430870fdd4e68e1c2e153ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594320"
---
# <a name="property-windows"></a>Windows de propriété

> [!NOTE]
> ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

La fenêtre Propriétés est le nom collectif pour les types d’interfaces utilisateur (IU) suivants :

-   Feuille de propriétés : permet d' **afficher et de modifier les propriétés d’un objet ou d’une collection d’objets dans une boîte de dialogue**.
-   Inspecteur de propriété : permet d' **afficher et de modifier les propriétés d’un objet ou d’une collection d’objets dans un volet**.
-   Options, boîte de dialogue : permet d' **afficher et de modifier les options d’une application**.

Une propriété pour un objet est l’un des éléments suivants :

-   Paramètre que les utilisateurs peuvent modifier (par exemple, le nom d’un fichier et l’attribut de lecture seule).
-   Attribut d’un objet que les utilisateurs ne peuvent pas modifier directement (par exemple, la date de création et de taille d’un fichier).

Contrairement aux boîtes de dialogue (autres que les boîtes de dialogue d’options) et aux assistants, les fenêtres de propriétés prennent généralement en charge plusieurs tâches au lieu d’une seule tâche.

Les fenêtres de propriétés sont généralement organisées en pages, accessibles via des onglets. Les fenêtres de propriétés sont souvent associées à des onglets (et vice versa), mais **les onglets ne sont pas essentiels pour les fenêtres de propriétés**.

![capture d’écran de la feuille de propriétés des propriétés du document ](images/win-property-win-image1.png)

Feuille de propriétés standard.

**Remarque :** Les instructions relatives à la [disposition](vis-layout.md) et aux [onglets](ctrl-tabs.md) sont présentées dans des articles distincts.

## <a name="is-this-the-right-user-interface"></a>S’agit-il de l’interface utilisateur appropriée ?

Pour vous décider, posez-vous les questions suivantes :

-   **La définition des propriétés oblige-t-elle les utilisateurs à effectuer une séquence d’étapes fixe et non triviale ?** Dans ce cas, utilisez plutôt un [Assistant](win-wizards.md) ou un [Workflow de tâche](glossary.md) .
-   **Le contenu est-il uniquement une option d’application ?** Dans ce cas, utilisez une boîte de dialogue Options.
-   **Le contenu est-il uniquement un attribut de l’application ?** Dans ce cas, utilisez une [zone à propos de](glossary.md).
-   **Le contenu est-il principalement constitué des propriétés d’un objet (ses paramètres ou ses attributs) ?** Si ce n’est pas le cas, utilisez une boîte de dialogue [boîte](win-dialog-box.md) ou à [onglets](glossary.md)standard.
-   Les utilisateurs **risquent-ils d’afficher ou de modifier les propriétés fréquemment ou sur une période prolongée ?** Dans ce cas, utilisez un inspecteur de propriété. Sinon, utilisez une feuille de propriétés.
-   Les utilisateurs **risquent-ils d’afficher ou de modifier les propriétés de plusieurs objets à la fois ?** Dans ce cas, utilisez un inspecteur de propriété. Sinon, utilisez une feuille de propriétés.

**Les feuilles de propriétés et les inspecteurs de propriétés ne sont pas exclusifs.** Vous pouvez afficher les propriétés les plus fréquemment sollicitées dans un inspecteur de propriété et le jeu complet dans la feuille de propriétés.

## <a name="design-concepts"></a>Principes de conception

**Les fenêtres de propriétés deviennent souvent un motif de dumping pour un assortiment impair de paramètres de technologie de bas niveau.** Trop souvent, ces propriétés sont organisées dans des onglets, mais au-delà de celles qui ne sont pas conçues pour des tâches ou des utilisateurs particuliers. Par conséquent, lorsque les utilisateurs sont confrontés à une tâche dans une fenêtre de propriétés, ils ne savent souvent pas quoi faire.

Pour vous assurer que vos fenêtres de propriétés sont utiles et utilisables, procédez comme suit :

-   Vérifiez que les propriétés sont nécessaires.
-   Présenter les propriétés en termes d’objectifs de l’utilisateur, et non de technologie.
-   Présenter les propriétés au niveau approprié.
-   Concevoir des pages pour des tâches spécifiques.
-   Concevez des pages pour des utilisateurs spécifiques, en particulier des utilisateurs limités (non-administrateurs).
-   Organisez les pages de propriétés efficacement.

**Si vous n’avez qu’une seule chose...**

Présenter les propriétés en termes d’objectifs de l’utilisateur, et non de technologie. Supposons que vous décrivez la propriété et pourquoi elle est utile pour un ami. Comment l’expliqueriez-vous ? Quelle langue utiliseriez-vous ? C’est le langage à utiliser dans vos pages de propriétés.

## <a name="usage-patterns"></a>Modèles d’usage

Les fenêtres de propriétés ont plusieurs modèles d’utilisation.

-   Feuilles de propriétés. Les propriétés d’un seul objet sont affichées dans une boîte de dialogue non modale.
-   Feuilles de propriétés à plusieurs objets. Les propriétés de plusieurs objets sont affichées dans une boîte de dialogue non modale.
-   Feuilles de propriétés de paramètres effectives. Les propriétés effectives d’un seul objet sont affichées dans une boîte de dialogue non modale.
-   Boîtes de dialogue Options. Les propriétés d’une application sont affichées dans une boîte de dialogue modale.
-   Inspecteurs de propriété. Les propriétés de la sélection actuelle (un seul objet ou groupe d’objets) s’affichent dans un volet de fenêtre sans mode ou dans une fenêtre non ancrée.

Tous les modèles de fenêtre de propriétés sauf les inspecteurs de propriété utilisent une validation différée, ce qui signifie que les modifications prennent effet uniquement lorsque les utilisateurs cliquent sur OK ou appliquer. Les inspecteurs de propriété utilisent une validation immédiate (les propriétés sont modifiées dès que les utilisateurs effectuent des modifications). il n’est donc pas nécessaire d’utiliser les boutons OK, annuler et appliquer.

## <a name="guidelines"></a>Consignes

### <a name="property-sheets"></a>Feuilles de propriétés

-   **Afficher une feuille de propriétés lorsque les utilisateurs :**
    -   Sélectionnez la commande propriétés pour un objet.
    -   Définissez le focus d’entrée sur un objet et appuyez sur Alt + Entrée.

**Feuilles de propriétés à plusieurs objets**

-   **Affichez les propriétés communes de tous les objets sélectionnés.** Lorsque les valeurs de propriété diffèrent, affichez les contrôles associés à ces valeurs à l’aide d’un État mixte. (Consultez les instructions de contrôle respectives pour l’utilisation des valeurs à États mixtes).
-   Si l’objet sélectionné est une collection de plusieurs objets discrets (par exemple, un dossier de fichiers), **Affichez les propriétés de l’objet groupé unique au lieu d’une feuille de propriétés à plusieurs objets pour les objets discrets.**

### <a name="options-dialog-boxes"></a>Boîtes de dialogue Options

-   **Ne séparez pas les options de la personnalisation.** Autrement dit, vous ne devez pas avoir à la fois une commande Options et une commande de personnalisation. Les utilisateurs sont souvent confondus par cette séparation. Au lieu de cela, accédez à la personnalisation par le biais d’options.

### <a name="property-pages"></a>pages de propriétés

-   **Suivez ces instructions pour l’ordre des pages :**
    -   Définissez la page général ou son équivalent sur la première page.
    -   Définissez la page avancé ou son équivalent sur la dernière page.
    -   Pour les pages restantes :
        -   Organisez-les dans des groupes de pages associées.
        -   Ordonnez les groupes en fonction de leur probabilité d’utilisation.
        -   Dans chaque groupe, ordonnez les pages en fonction de leurs relations ou de la probabilité qu’elles leur soient utilisées.
        -   Vous ne devriez pas avoir autant de pages qu’il est nécessaire de les afficher dans l’ordre alphabétique.
-   **Rendez les pages cohérentes en associant toutes les propriétés de chaque page à un objectif unique et spécifique, basé sur les tâches.**
-   **Si l’espace le permet, Expliquez l’objectif de la fenêtre de propriétés en haut de la page s’il n’est pas évident pour vos utilisateurs cibles.** Si la page est utilisée pour effectuer une seule tâche, **formulez le texte comme une instruction claire sur la façon d’effectuer cette tâche**. Utilisez des phrases complètes, se terminant par un point.

    ![capture d’écran de la feuille de propriétés propriétés du pare-feu ](images/win-property-win-image2.png)

    dans cet exemple, l’objectif du pare-feu Microsoft Windows est expliqué en haut de la page général.

-   **Faites en sorte qu’un contenu similaire soit cohérent entre les pages en utilisant des noms et des emplacements de contrôle cohérents.** Par exemple, si plusieurs pages ont des zones de nom, essayez de les placer dans le même emplacement sur la page et d’utiliser des étiquettes cohérentes. Le contenu similaire ne doit pas rebondir d’une page à l’autre.
-   **Placez la même propriété sur la même page dans votre application.** Par exemple, ne placez pas de propriété expiration dans l’onglet général pour un type d’objet, et sous l’onglet avancé pour un autre type.
-   **Si les utilisateurs sont susceptibles de démarrer avec la dernière page affichée, rendez l’onglet de page persistant et sélectionnez-le par défaut.** Rendez les paramètres persistants en fonction de la fenêtre de propriétés, par utilisateur. Dans le cas contraire, sélectionnez la première page par défaut.
-   **Ne rendez pas les paramètres sur une page dépendants des paramètres d’autres pages.** Placez les paramètres dépendants sur une seule page à la place. La modification d’un paramètre sur une page ne doit jamais modifier automatiquement les paramètres d’autres pages.
    -   **Exception :** Si les paramètres dépendants se trouvent dans deux fenêtres de propriétés différentes, utilisez des étiquettes de texte statiques pour expliquer cette relation dans les deux emplacements.
-   **Ne faites pas défiler les pages de propriétés.** Les onglets et les barres de défilement sont utilisés pour augmenter la zone effective d’une fenêtre, mais un mécanisme doit suffire. Au lieu d’utiliser des barres de défilement, agrandissez les pages de propriétés et disposez les pages de manière efficace.

**Premières pages**

-   Pour les propriétés de l’objet, **Placez le nom de l’objet sur la première page.**
-   Si vous associez des [icônes](vis-icons.md) (facultatives) à vos objets, **Affichez l’icône appropriée dans le coin supérieur gauche** de la première page.

**Pages générales**

-   **Évitez les pages générales.** Vous n’êtes pas obligé de disposer d’une page générale. Utilisez une page générale uniquement si :
    -   Les propriétés s’appliquent à plusieurs tâches et sont significatives pour la plupart des utilisateurs. Ne placez pas de propriétés spécialisées ou avancées sur une page général, mais vous pouvez les rendre accessibles via un bouton de commande sur la page général.
    -   Les propriétés ne correspondent pas à une catégorie plus spécifique. Si c’est le cas, utilisez plutôt ce nom pour la page.

**Pages avancées**

-   **Évitez les pages avancées.** Utilisez une page avancée uniquement si :
    -   Les propriétés s’appliquent aux tâches rares et sont particulièrement explicites pour les utilisateurs expérimentés.
    -   Les propriétés ne correspondent pas à une catégorie plus spécifique. Si c’est le cas, utilisez plutôt ce nom pour la page.
-   **N’appelez pas les propriétés Advanced sur la base de mesures technologiques uniquement.** Par exemple, une option d’association d’imprimante peut être une fonction d’imprimante avancée, mais elle est significative pour tous les utilisateurs. elle ne doit donc pas être sur une page avancée.

### <a name="owned-property-windows"></a>Fenêtres de propriétés détenues

-   **N’affichez pas plus d’une fenêtre de propriété appartenant à partir d’une fenêtre de propriétés.** Afficher plus d’un rend la signification des boutons OK et annuler difficile à comprendre. Vous pouvez afficher d’autres types de boîtes de dialogue auxiliaires (telles que des sélecteurs d’objets) en fonction des besoins.

    **Incorrect :**

    ![capture d’écran de trois fenêtres de propriétés détenues ](images/win-property-win-image3.png)

    Dans cet exemple, la boîte de dialogue Options du propriétaire a trois niveaux de fenêtres de propriétés détenues. Par conséquent, les significations de OK et d’annulation sont confuses.

-   Pour les fenêtres de propriétés qui utilisent un modèle de validation différée, assurez-vous que **les utilisateurs peuvent annuler les modifications apportées dans une fenêtre de propriété appartenant en cliquant sur Annuler dans la fenêtre propriétaire.**
-   Si une fenêtre de propriété possédée requiert une validation immédiate, **indiquez que les modifications ont été validées en renommant le bouton Annuler de la fenêtre propriétaire pour fermer.** Rétablir le bouton à nouveau si l’utilisateur clique sur appliquer.

    ![capture d’écran de la fenêtre de propriétés avec OK et fermer ](images/win-property-win-image4.png)

    Dans cet exemple, les modifications apportées aux dictionnaires personnalisés et aux paramètres de grammaire ne peuvent pas être annulées. Vous pouvez fournir des commentaires aux utilisateurs en remplaçant annuler par fermer.

**Autres fenêtres détenues**

-   Si une fenêtre appartenant est utilisée pour effectuer une tâche auxiliaire, **ne renommez pas le bouton Annuler.** Les instructions précédentes s’appliquent uniquement aux fenêtres de propriétés détenues, et non aux boîtes de dialogue utilisées pour effectuer des tâches auxiliaires.

    ![capture d’écran de la fenêtre propriétaire et nettoyage de disque ](images/win-property-win-image5.png)

    Dans cet exemple, le nettoyage de disque est une tâche auxiliaire, donc les recommandations précédentes ne s’appliquent pas. Par exemple, le bouton Annuler de la fenêtre propriétaire ne doit pas être remplacé par fermer.

-   Si la fenêtre qui vous appartient est utilisée pour effectuer une tâche auxiliaire, **ne fermez pas la fenêtre Propriétés du propriétaire lorsque vous cliquez sur le bouton de commande.** Cela a pour effet de désorienter et suppose que la seule raison pour laquelle l’utilisateur a affiché la fenêtre de propriétés était d’exécuter cette commande.

    **Incorrect :**

    ![capture d’écran de la boîte de dialogue Options ](images/win-property-win-image6.png)

    Dans cet exemple, si vous cliquez sur **protéger le document** , la boîte de dialogue Options s’ouvre de manière incorrecte.

### <a name="tabs"></a>Tabulations

-   **Utilisez des étiquettes d’onglet concises.** Utilisez un ou deux mots qui décrivent clairement le contenu de la page. Des étiquettes plus longues entraînent une utilisation inefficace de l’espace à l’écran, en particulier lorsque les étiquettes sont localisées.
-   **Utilisez des étiquettes d’onglet explicites et explicites.** évitez les étiquettes d’onglet génériques qui peuvent s’appliquer à n’importe quel onglet, tel que général, avancé ou Paramètres.
-   **Utilisez des tabulations horizontales si :**
    -   La fenêtre Propriétés a sept onglets ou moins (y compris les extensions tierces).
    -   **Tous les onglets s’ajustent sur une ligne, même lorsque l’interface utilisateur est localisée.**
    -   Vous utilisez des tabulations horizontales dans les autres fenêtres de propriétés de votre application.
-   **Utilisez des tabulations verticales si :**

    -   La fenêtre de propriétés comporte huit onglets ou plus (y compris les extensions tierces).
    -   **L’utilisation de tabulations horizontales nécessitera plusieurs lignes.**
    -   Vous utilisez des tabulations verticales sur les autres fenêtres de propriétés de votre application.

    ![capture d’écran de la fenêtre de propriétés avec tabulations verticales ](images/win-property-win-image7.png)

    Dans cet exemple, les onglets verticaux sont utilisés pour prendre en charge huit onglets ou plus.

-   **Pour conserver de l’espace pour les inspecteurs de propriété, envisagez d’utiliser une liste déroulante au lieu de tabulations**, en particulier si l’utilisateur a rarement modifié l’onglet actuel.
-   **Si un onglet ne s’applique pas au contexte actuel et que les utilisateurs ne l’attendent pas, supprimez l’onglet.** Cela simplifie l’interface utilisateur, et les utilisateurs ne le manquent pas.

    **Incorrect :**

    ![capture d’écran de l’onglet emplacements de fichiers estompés ](images/win-property-win-image8.png)

    dans cet exemple, l’onglet emplacements des fichiers est incorrectement désactivé quand Microsoft Word 2003 est utilisé comme éditeur de messagerie électronique. La page doit être supprimée, car les utilisateurs ne s’attendent pas à afficher ou à modifier les emplacements des fichiers dans ce contexte.

-   **Si un onglet ne s’applique pas au contexte actuel et que les utilisateurs peuvent s’attendre à ce que :**

    -   **Affichez l’onglet.**
    -   **Désactivez les contrôles sur la page.**
    -   **Incluez du texte expliquant pourquoi les contrôles sont désactivés.**

    Ne désactivez pas l’onglet car cela n’est pas explicite et interdit l’exploration. En outre, les utilisateurs qui recherchent une propriété spécifique sont obligés d’examiner tous les autres onglets.

    ![capture d’écran des contrôles d’affichage grisés ](images/win-property-win-image9.png)

    Dans cet exemple à partir de Word 2003, aucune des options d’affichage ne s’applique en mode lecture. Toutefois, les utilisateurs peuvent s’attendre à ce qu’ils s’appliquent en fonction de l’étiquette d’onglet, de sorte que la page s’affiche, mais les options sont désactivées.

-   **N’affectez pas d’effets à la modification des onglets.** La modification de l’onglet actuel ne doit jamais avoir d’effets secondaires, appliquer des paramètres ou générer un message d’erreur.
-   **N’imbriquez pas d’onglets ou combinez des onglets horizontaux avec des tabulations verticales.** Au lieu de cela, réduisez le nombre d’onglets, utilisez uniquement des tabulations verticales ou utilisez un autre contrôle comme une liste déroulante.
-   **N’utilisez pas d’onglets si une fenêtre de propriétés n’a qu’un seul onglet et n’est pas extensible.** Utilisez une boîte de dialogue standard avec OK, annuler et un bouton appliquer facultatif à la place. Les fenêtres de propriétés extensibles (qui peuvent être étendues par des tiers) doivent toujours utiliser des onglets.
-   **Ne placez pas d’icônes sur les onglets.** Les icônes ajoutent généralement un encombrement visuel inutile, consomment de l’espace à l’écran et n’améliorent souvent pas la compréhension des utilisateurs. Ajoutez uniquement des icônes qui facilitent la compréhension, telles que les symboles standard.

    **Incorrect :**

    ![capture d’écran des étiquettes d’onglet avec des icônes ](images/win-property-win-image10.png)

    Dans cet exemple, les graphiques ajoutent un désordre visuel inutile et n’améliorent pas la compréhension des utilisateurs.

-   **N’utilisez pas de logos de produit pour les graphiques d’onglets.** Les onglets ne sont pas destinés à la personnalisation.
-   **Ne pas faire défiler les onglets horizontaux.** Le défilement horizontal n’est pas facilement détectable. Toutefois, vous pouvez faire défiler verticalement les onglets.

    **Incorrect :**

    ![capture d’écran de l’étiquette de tabulation horizontale tronquée ](images/win-property-win-image11.png)

    Dans cet exemple, les onglets horizontaux défilent.

### <a name="command-buttons"></a>Boutons de commande

-   **Placez les boutons de commande qui s’appliquent à toutes les pages de propriétés en bas de la fenêtre de propriétés.** Alignez les boutons à droite et utilisez cet ordre (de gauche à droite) : OK, annuler et appliquer.
-   **Placez les boutons de commande qui s’appliquent uniquement aux pages de propriétés individuelles directement dans la page de propriétés.**

### <a name="commit-buttons"></a>Boutons de validation

**Boutons OK**

-   **Pour les fenêtres de propriétés de propriétaire, le bouton OK signifie appliquer les modifications en attente (effectuées depuis l’ouverture de la fenêtre ou la dernière application) et fermer la fenêtre.**
-   **Pour les fenêtres de propriétés détenues, le bouton OK signifie conserver les modifications, fermer la fenêtre et appliquer les modifications lorsque les modifications de la fenêtre propriétaire sont appliquées.**
-   **Ne renommez pas le bouton OK.** Contrairement à d’autres boîtes de dialogue, les fenêtres de propriétés ne sont pas utilisées pour effectuer une tâche spécifique. S’il est judicieux de renommer le bouton OK (pour imprimer, par exemple), la fenêtre n’est pas une fenêtre de propriétés.
-   **N’attribuez pas de clé d’accès.**

**Bouton Annuler**

-   **Le bouton Annuler signifie ignorer toutes les modifications en attente (effectuées depuis l’ouverture de la fenêtre ou la dernière application) et fermer la fenêtre.**
-   **Si toutes les modifications en attente ne peuvent pas être abandonnées, renommez le bouton Annuler pour fermer.** Le fait de cliquer sur Annuler doit abandonner toutes les modifications en attente.
-   **Si la fenêtre de propriété appartenant requiert une validation immédiate, renommez le bouton Annuler de la fenêtre propriétaire pour indiquer que les modifications ont été validées.**
-   **N’attribuez pas de clé d’accès.**

**Appliquer des boutons**

-   **Pour les feuilles de propriétés de propriétaire, le bouton appliquer signifie appliquer les modifications en attente (effectuées depuis l’ouverture de la fenêtre ou la dernière application), mais laissez la fenêtre ouverte.** Cela permet aux utilisateurs d’évaluer les modifications avant de fermer la feuille de propriétés.
-   **Pour les feuilles de propriétés détenues, n’utilisez pas.** L’utilisation d’un bouton appliquer sur une feuille de propriétés possédée rend la signification des boutons de validation sur la feuille de propriétés de propriétaire difficile à comprendre.
-   **Ne fournissez un bouton appliquer que si la feuille de propriétés contient des paramètres (au moins un) avec des effets que les utilisateurs peuvent évaluer de manière explicite.** En règle générale, les boutons appliquer sont utilisés lorsque les paramètres apportent des modifications visibles. Les utilisateurs doivent pouvoir appliquer une modification, évaluer la modification et apporter d’autres modifications en fonction de cette évaluation. Si ce n’est pas le cas, supprimez le bouton appliquer au lieu de le désactiver.

    **Incorrect :**

    ![capture d’écran des propriétés système avec le bouton appliquer ](images/win-property-win-image12.png)

    Dans cet exemple, aucune des propriétés système n’a d’effet visuel, donc le bouton appliquer n’a pas de valeur et doit être supprimé.

-   **Placez tous les paramètres que les utilisateurs peuvent vouloir appliquer sur les pages propriétaires.** N’utilisez pas de boutons appliquer sur les feuilles de propriétés détenues, car cela peut prêter à confusion.
-   **Utilisez les boutons appliquer uniquement avec les feuilles de propriétés, et non avec les boîtes de dialogue Options.**
-   **Activez le bouton appliquer uniquement lorsqu’il existe des modifications en attente**. Sinon, désactivez-la.
-   **Assignez « A » comme clé d’accès.**

**Boutons Fermer**

-   **Si toutes les modifications en attente ne peuvent pas être abandonnées, renommez le bouton Annuler pour fermer.** Le fait de cliquer sur Annuler doit abandonner toutes les modifications en attente.
-   **Ne confirmez pas si les utilisateurs ignorent leurs modifications.**
    -   **Exception :** Si la fenêtre des propriétés contient des paramètres qui nécessitent un effort important pour définir et que l’utilisateur a apporté des modifications, vous pouvez afficher une [confirmation](mess-confirm.md) si l’utilisateur clique sur le bouton Fermer dans la barre de titre. La raison en est que certains utilisateurs supposent par erreur que le bouton fermer de la barre de titre a le même effet que le bouton OK.
-   **À l’exception du message de confirmation, vérifiez que le bouton fermer de la barre de titre a le même effet que annuler ou fermer.**

### <a name="page-contents"></a>Contenu de la page

-   **Vérifiez que les propriétés sont nécessaires.** N’encombrez pas vos pages avec des propriétés inutiles simplement pour éviter de prendre des décisions de conception matérielle.
-   **Présenter les propriétés en termes d’objectifs de l’utilisateur, et non de technologie.** La seule raison pour laquelle une propriété configure une technologie spécifique ne signifie pas que vous devez présenter la propriété en ce qui concerne cette technologie.
    -   Si vous devez présenter des paramètres en termes de technologie (peut-être parce que vos utilisateurs reconnaissent le nom de la technologie), incluez une brève description de la façon dont l’utilisateur bénéficie de ce paramètre.
-   **Présenter les propriétés au niveau approprié.** Vous n’avez pas besoin de présenter des paramètres individuels de bas niveau sur une page de propriétés. par conséquent, présentez les propriétés à un niveau approprié pour vos utilisateurs.
-   **Concevoir des pages de propriétés pour des tâches spécifiques.** Déterminez les tâches que les utilisateurs effectueront et assurez-vous qu’il existe un chemin d’accès clair pour effectuer ces tâches.
-   **Organisez les pages de propriétés efficacement** en réduisant le nombre d’onglets, en déterminant ce qui va sur une page en fonction du regroupement logique et de la cohérence, et en simplifiant la présentation de la page.

<!-- -->

-   **Si une option est fortement recommandée, ajoutez « (recommandé) » à l’étiquette.**
-   **Fournissez un bouton de commande restaurer les paramètres par défaut pour une page de propriétés ou la totalité de la fenêtre de propriétés dans les cas suivants :**

    -   Vos utilisateurs sont susceptibles de considérer les paramètres complexes et difficiles à comprendre.
    -   Le fait d’avoir des paramètres incorrects peut entraîner des ruptures de fonctionnalité, mais les valeurs par défaut peuvent être restaurées.
    -   Il est plus facile pour les utilisateurs de redémarrer lorsque l’objet est mal configuré.

    ![capture d’écran de l’onglet avec le bouton restaurer les paramètres par défaut ](images/win-property-win-image13.png)

    dans cet exemple, les paramètres du pare-feu Windows sont complexes et peuvent entraîner des ruptures de fonctionnalité. En cas de problème, il est souvent plus facile pour les utilisateurs de recommencer en cliquant sur restaurer les valeurs par défaut.

-   Confirmez la commande restaurer les valeurs par défaut si son effet n’est pas évident ou si les paramètres sont complexes. Indiquez la confirmation en utilisant des [ellipses](ctrl-command-buttons.md).
-   **Le cas échéant, affichez un aperçu des résultats d’un paramètre.**

    ![capture d’écran des exemples de pointeur de propriétés de souris ](images/win-property-win-image14.png)

    Dans cet exemple, la page affiche un aperçu des schémas de pointeur. En cliquant sur appliquer, vous affichez également un aperçu, et l’aperçu de la page est plus efficace pour les utilisateurs.

    ![capture d’écran de l’aperçu des résultats des paramètres de police ](images/win-property-win-image15.png)

    Dans cet exemple, la zone d’aperçu affiche les résultats des paramètres de police. Cet exemple montre que vous pouvez afficher un aperçu des paramètres qui ne sont pas graphiques.

### <a name="help"></a>Aide

-   Lorsque vous fournissez une assistance utilisateur, **envisagez d’utiliser les options suivantes** (classées dans l’ordre de préférence) :
    -   Donnez aux contrôles interactifs des étiquettes explicites. Les utilisateurs sont plus susceptibles de lire les étiquettes sur des contrôles interactifs que tout autre texte.
    -   Fournissez des explications en contexte à l’aide d’étiquettes de texte statiques.
    -   Fournissez un [lien](ctrl-links.md) spécifique vers une rubrique d’aide pertinente.
-   **Localisez les liens d’aide en bas de chaque page.** Si une page contient plusieurs groupes de paramètres distincts qui ont une rubrique d’aide (peut-être dans des zones de groupe), recherchez le lien d’aide en bas du groupe.
-   **N’utilisez pas de liens vers des rubriques d’aide générales ou vagues ou des boutons d’aide génériques.** Les utilisateurs ignorent souvent l’aide générique.

Pour plus d’informations et d’exemples, consultez [l’aide](winenv-help.md)de.

### <a name="standard-users-and-protected-administrators"></a>Utilisateurs standard et administrateurs protégés

**De nombreux paramètres requièrent des privilèges d’administrateur pour changer.** si un processus requiert des privilèges d’administrateur, Windows et versions ultérieures requièrent des [utilisateurs Standard](glossary.md) et des [administrateurs protégés](glossary.md) pour élever leurs privilèges de manière explicite. Cela permet d’empêcher le code malveillant de s’exécuter avec des privilèges d’administrateur.

Pour plus d’informations et d’exemples, consultez [contrôle de compte d’utilisateur](winenv-uac.md).

### <a name="default-values"></a>Valeurs par défaut

-   **Les paramètres dans une fenêtre de propriétés doivent refléter l’état actuel de l’application, de l’objet ou de la collection d’objets.** Sinon, cela serait trompeur et peut entraîner des résultats indésirables. Par exemple, si les paramètres reflètent les recommandations mais pas l’état actuel, les utilisateurs peuvent cliquer sur Annuler au lieu d’apporter des modifications, en pensant qu’aucune modification n’est nécessaire.
-   **Choisissez le plus sûr (pour éviter la perte de données ou l’accès au système) et l’état initial le plus sécurisé.** Supposons que la plupart des utilisateurs ne modifieront pas les paramètres.
-   **Si la sécurité et la sécurité ne sont pas des facteurs, choisissez l’état initial le plus probable ou le plus pratique.**

## <a name="text"></a>Texte

### <a name="commands"></a>Commandes

-   Pour afficher les options du programme, utilisez « options ».
-   Pour afficher la fenêtre des propriétés d’un objet, utilisez « Properties ».
-   Pour afficher un résumé des paramètres de personnalisation de programme couramment utilisés, utilisez «[personnaliser](glossary.md)».
-   n’utilisez pas « Paramètres » ou « preferences ».
-   N’utilisez pas de [ellipses](ctrl-command-buttons.md) pour ces commandes.

### <a name="property-sheet-titles"></a>Titres de la feuille de propriétés

-   Pour un objet unique, utilisez « \[ Propriétés du nom de l’objet \] ».
    -   Si l’objet n’a pas de nom, utilisez le nom de type de l’objet. (Par exemple, les propriétés du compte d’utilisateur.)
-   Pour plusieurs objets, utilisez « \[ nom du premier objet \] ,... Propriétés».
    -   Si les objets n’ont pas de noms, utilisez le nom de type des objets. (Par exemple, propriétés des comptes d’utilisateur.)
    -   Si les objets ont des types différents, utilisez « propriétés de sélection ».
-   Utilisez la mise [en majuscules du style titre](glossary.md).
-   N’utilisez pas de ponctuation finale.
-   N’utilisez pas de traits d’Union, tels que « \[ nom de l’objet \] -Propriétés ».

### <a name="property-inspector-titles"></a>Titres de l’inspecteur de propriétés

-   Utilisez « Properties ».
-   Utilisez la mise en majuscules du style titre.
-   N’utilisez pas de ponctuation finale.

### <a name="options-dialog-box-titles"></a>Titres de la boîte de dialogue Options

-   Utilisez « options ».
-   Utilisez la mise en majuscules du style titre.
-   N’utilisez pas de ponctuation finale.

### <a name="property-page-tab-names"></a>Noms des onglets de page de propriétés

-   **Utilisez des étiquettes d’onglet concises.** Utilisez un ou deux mots qui décrivent clairement le contenu de la page. L’utilisation de noms d’onglets plus longs entraîne une utilisation inefficace de l’espace à l’écran, en particulier lorsque les noms des onglets sont localisés.
-   **Utilisez des étiquettes d’onglet explicites et explicites.** évitez les étiquettes d’onglet génériques qui peuvent s’appliquer à n’importe quel onglet, tel que général, avancé ou Paramètres.
-   Écrivez l’étiquette en tant qu’expression à un ou deux mots et n’utilisez pas de ponctuation finale.
-   Utilisez la mise [en majuscules de style phrase](glossary.md).
-   N’attribuez pas une [clé d’accès](glossary.md)unique.

### <a name="property-page-text"></a>Texte de la page de propriétés

-   Évitez les grands blocs de texte.
-   Fournissez suffisamment d’espace pour que le texte s’étende à 30% s’il est localisé.
-   N’utilisez pas formulées de texte comme commande dans les fenêtres de propriétés. Étant donné que les utilisateurs peuvent souhaiter simplement afficher des paramètres, vous ne souhaitez pas les inviter à modifier les paramètres.
-   Utilisez des majuscules et des signes de ponctuation de style phrase.

## <a name="documentation"></a>Documentation

Lorsque vous faites référence à des fenêtres de propriétés :

-   Dans programmation et autres documents techniques, reportez-vous aux boîtes de dialogue feuilles de propriétés et options en tant que feuilles de propriétés. Partout ailleurs, utilisez la boîte de dialogue, en particulier dans la documentation de l’utilisateur.
-   Utilisez le texte exact du titre, y compris sa mise en majuscules.
-   Pour décrire l’interaction de l’utilisateur, utilisez ouvrir et fermer.
-   Dans la mesure du possible, mettez en forme le titre en gras. Sinon, placez le titre entre guillemets uniquement si nécessaire pour éviter toute confusion.

Lorsque vous faites référence à des pages de propriétés :

-   Dans programmation et autres documents techniques, reportez-vous aux pages de propriétés en tant que pages de propriétés. Partout ailleurs, utilisez la touche Tab, en particulier dans la documentation de l’utilisateur.
-   Utilisez le texte exact du titre, y compris sa mise en majuscules.
-   Pour décrire l’interaction de l’utilisateur, utilisez Cliquer pour faire référence à un clic sur un onglet.
-   Dans la mesure du possible, mettez en forme le nom à l’aide du texte gras. Sinon, placez le nom entre guillemets uniquement si nécessaire pour éviter toute confusion.

 

 