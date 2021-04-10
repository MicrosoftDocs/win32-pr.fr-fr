---
title: Liens de commande
description: Avec les liens de commande, les utilisateurs sélectionnent une réponse unique à une instruction principale et, en procédant ainsi, passent à l’étape suivante dans une tâche.
ms.assetid: a77819b1-9a32-4468-94fb-3f73a469fb81
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 29031b4456950db6ceff30d75b354dece92c5897
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "103761288"
---
# <a name="command-links"></a>Liens de commande

> [!NOTE]
> Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Avec les liens de commande, les utilisateurs sélectionnent une réponse unique à une instruction principale et, en procédant ainsi, passent à l’étape suivante dans une tâche.

Les liens de commande ont une apparence propre et légère qui permet d’obtenir des étiquettes descriptives, et qui s’affichent avec une flèche standard ou une icône personnalisée, ainsi qu’une explication supplémentaire facultative.

![capture d’écran d’une boîte de dialogue de lien de commande classique ](images/ctrl-command-links-image1.png)

Ensemble classique de liens de commande.

Les liens de commande sont similaires aux [cases d’option](ctrl-radio-buttons.md) en ce qu’ils sont utilisés pour effectuer une sélection parmi un ensemble de choix associés s’excluant mutuellement. Comme les cases d’option, les liens de commande sont toujours présentés dans des ensembles, jamais individuellement. Dans l’apparence, les liens de commande ont une apparence légère similaire aux [liens](ctrl-links.md)standard, sans cadre ou autre offre [de clic fort](glossary.md). Les liens de commande sont également similaires aux [boutons de commande](ctrl-command-buttons.md), dans la mesure où ils peuvent être le « bouton de commande » par défaut et qu’une clé d’accès peut lui être attribuée. Comme pour les [boutons valider](glossary.md), cliquez dessus pour fermer la fenêtre (pour les boîtes de dialogue) ou passer à la page suivante (pour les assistants et les flux de pages).

> [!Note]  
> Les instructions relatives aux [liens](ctrl-links.md) et à la [mise en page](vis-layout.md) sont présentées dans des articles distincts.

 

## <a name="is-this-the-right-control"></a>Est-ce le contrôle approprié ?

Pour vous décider, posez-vous les questions suivantes :

-   **Les options sont-elles les réponses à l’instruction principale et associées à l’objectif principal de la fenêtre ou de la page ?** Les utilisateurs doivent-ils y répondre pour faire autre chose que simplement naviguer vers une autre page ? Si ce n’est pas le cas, utilisez un autre contrôle, comme des boutons de commande ou des liens. Les liens de commande ne sont pas appropriés pour les choix secondaires ou facultatifs, ni pour la navigation pure.

    ![capture d’écran d’un élément de panneau de configuration personnaliser ](images/ctrl-command-links-image2.png)

    Alors que l’élément du panneau de configuration de personnalisation semble utiliser des liens de commande, les options sont des liens standard, car cette [page de concentrateur](winenv-ctrl-panels.md) est destinée à une navigation pure.

-   **Le contrôle est-il utilisé pour choisir une réponse d’un ensemble de réponses s’excluant mutuellement ?** Si ce n’est pas le cas, utilisez un autre contrôle. Pour permettre aux utilisateurs de choisir des commandes individuelles, utilisez les boutons de commande ou les liens.
-   **Pour les boîtes de dialogue, le fait de cliquer sur le contrôle ferme-t-il la fenêtre ?** Si ce n’est pas le cas, utilisez un contrôle qui ne requiert pas la fermeture de la fenêtre, comme les cases d’option, les boutons de commande ou les liens.

    **Incorrect :**

    ![capture d’écran de la boîte de dialogue Paramètres de pare-feu avec onglet ](images/ctrl-command-links-image3.png)

    Les liens de commande ne peuvent pas être utilisés dans les fenêtres de propriétés ou les boîtes de dialogue à onglets car le fait de cliquer sur le contrôle ferme la fenêtre.

-   **Pour les assistants et les flux de page, clique sur avancer jusqu’à la page suivante sans engagement ?** N’utilisez pas de liens de commande pour valider une tâche ; Utilisez des boutons de validation à la place. Étant donné que les liens de commande ressemblent à des liens et que les utilisateurs associent des liens avec la navigation dans un workflow de page, les liens ne sont pas appropriés pour les [pages de validation](glossary.md) , car les utilisateurs doivent toujours pouvoir revenir en arrière.
-   **Pour les assistants et les flux de pages, les autres pages utilisent-elles des liens de commande ?** Si c’est le cas et que tous les autres facteurs sont égaux, préférez des liens de commande pour assurer la cohérence entre les pages.
-   **Le nombre de réponses est-il compris entre deux et cinq ?** Il ne doit jamais y avoir de lien de commande unique. Étant donné que les liens de commande sont des contrôles volumineux et que l’espace utilisé par l’écran est proportionnel au nombre d’options, conservez le nombre de réponses à au moins cinq. Pour six options ou plus, utilisez des cases d’option, des liens standard ou un [affichage de liste](ctrl-list-views.md)à sélection unique.

    ![capture d’écran de la boîte de dialogue avec la liste des commandes ](images/ctrl-command-links-image4.png)

    Dans cet exemple, la fonctionnalité d’exécution automatique de Microsoft Windows utilise un mode liste.

-   **Une combinaison de cases d’option et d’un bouton de validation est-elle un meilleur choix ?** Les cases d’option sont un meilleur choix lorsque l’une des conditions suivantes est vraie :
    -   **La plupart des utilisateurs doivent sélectionner une option forte par défaut.** Les utilisateurs sont moins susceptibles de modifier une case d’option par défaut qu’un lien de commande par défaut, en particulier dans un Assistant, où les utilisateurs sont habitués à cliquer sur suivant pour accepter les valeurs par défaut appropriées. En revanche, les liens de commande sont un meilleur choix si vous souhaitez inciter les utilisateurs à faire un choix explicite.
    -   **Les utilisateurs doivent interagir avec les choix (par exemple, pour afficher des informations supplémentaires) avant de prendre une décision.** Par exemple, la sélection d’une case d’option peut afficher une description de l’option de manière dynamique.

        ![capture d’écran de la boîte de dialogue avec des cases d’option ](images/ctrl-command-links-image5.png)

        Dans cet exemple, la sélection d’une case d’option affiche une description de l’option.

    -   **La page contient des options secondaires ou connexes.** Les liens de commande ont tendance à dominer la page, ce qui permet de négliger facilement tout le reste. En outre, une fois que vous avez cliqué sur un lien de commande, il est impossible de sélectionner les options secondaires.

        **Incorrect :**

        ![capture d’écran de la boîte de dialogue avec des contrôles mixtes ](images/ctrl-command-links-image6.png)

        Dans cet exemple, il existe deux façons de répondre à l’instruction principale. Un lien de commande n’a pas été utilisé pour la première réponse, car il serait difficile de sélectionner les options secondaires.

        **Correct :**

        ![capture d’écran de la boîte de dialogue avec les mêmes contrôles ](images/ctrl-command-links-image7.png)

        Dans cet exemple, les cases d’option rendent les réponses claires, tout en permettant aux utilisateurs de sélectionner des options secondaires.

-   **Pour les boîtes de dialogue, un groupe de boutons de validation sera-t-il un meilleur choix ?** Les liens de commande fonctionnent mieux quand les options requièrent des réponses plus longues, plus explicatives et des explications supplémentaires, mais un groupe de boutons de validation constitue un meilleur choix s’il existe quelques options simples.

    **Incorrect :**

    ![capture d’écran de la boîte de dialogue avec enregistrer et ne pas enregistrer ](images/ctrl-command-links-image8.png)

    Dans cet exemple, l’utilisation de liens de commande pour les commandes simples rend la boîte de dialogue inutilement compliquée.

    **Correct :**

    ![Capture d’écran montrant une boîte de dialogue avec les boutons « enregistrer », « ne pas enregistrer » et « annuler ».](images/ctrl-command-links-image9.png)

    Dans cet exemple, l’utilisation de boutons de validation simples est directement vers le point.

    Toutefois, les liens de commande explicites sont toujours mieux choisis quand le texte est utilisé pour expliquer les boutons de validation.

    **Incorrect :**

    ![capture d’écran de la boîte de dialogue avec du texte inutile ](images/ctrl-command-links-image10.png)

    Dans cet exemple, le texte est utilisé pour expliquer les boutons de validation.

    **Correct :**

    ![capture d’écran des étiquettes qui n’ont pas besoin de texte supplémentaire ](images/ctrl-command-links-image11.png)

    Dans cet exemple, les liens de commande sont explicites.

> [!Note]  
> Les liens de commande nécessitent Windows Vista ou une version ultérieure, donc ils ne sont pas adaptés aux versions antérieures de Windows. Vous pouvez utiliser des liens standard comme substituts.

 

![capture d’écran des liens standard avec des icônes et du texte ](images/ctrl-command-links-image12.png)

Dans cet exemple, des liens standard avec une icône et une explication supplémentaire sont utilisés comme substituts des liens de commande dans Windows XP.

## <a name="design-concepts"></a>Principes de conception

La seule raison pour laquelle les liens de commande vous permettent d’utiliser des étiquettes plus descriptives et des explications supplémentaires facultatives ne signifient pas. Prenons l’exemple suivant :

**Incorrect :**

![capture d’écran de la boîte de dialogue avec trop de texte ](images/ctrl-command-links-image13.png)

Cette boîte de dialogue est sérieusement en cours de communication.

Cette boîte de dialogue prend une question simple et la complique inutilement avec le texte de lien de commande. Les utilisateurs ne veulent pas lire tout ce texte pour des questions simples.

Nous pouvons simplifier cette boîte de dialogue en appliquant trois règles de lien de commande :

-   **N’utilisez pas une explication supplémentaire qui est un retraitement de mot du lien de commande.** Utilisez une explication supplémentaire uniquement lorsque vous ne pouvez pas rendre un lien de commande explicite. Si vous fournissez une explication supplémentaire pour un lien de commande, cela ne signifie pas que vous devez les fournir pour toutes les commandes.
-   **Sélectionnez le niveau de sécurité le plus sûr (pour éviter la perte de données ou l’accès au système) et la réponse la plus sécurisée est la valeur par défaut.** Si la sécurité et la sécurité ne sont pas des facteurs, sélectionnez la réponse la plus probable ou la plus pratique.
-   **Fournissez un bouton Annuler explicite.** N’utilisez pas de lien de commande à cet effet.

En appliquant ces instructions, nous pouvons éliminer les explications supplémentaires inutiles, faire de la réponse la plus pratique la réponse par défaut et fournir un bouton Annuler explicite.

**Conseillé**

![capture d’écran de la boîte de dialogue avec des commandes et des étiquettes ](images/ctrl-command-links-image14.png)

Version améliorée avec des liens de commande plus simples.

Bien qu’il soit vrai que cette version n’explique pas explicitement que l’enregistrement n’est pas considéré comme une perte, peu d’utilisateurs modifient leur décision en fonction de ces informations, ce qui en fait un bon compromis.

Cette boîte de dialogue peut être améliorée en analysant si les liens de commande sont même le bon contrôle à utiliser dans ce cas. Les boutons de validation sont en fait un meilleur choix, car des réponses plus explicatives plus longues ne sont pas nécessaires.

**Meilleures**

![capture d’écran de la boîte de dialogue avec des boutons de validation ](images/ctrl-command-links-image15.png)

La version correcte utilise des boutons valider pour se trouver directement au point.

Les liens de commande présentent de nombreux avantages, mais lorsqu’ils sont utilisés au contraire, ils entraînent un dépassement de la communication. Pour les boîtes de dialogue, envisagez d’utiliser d’abord les boutons de validation et utilisez des liens de commande uniquement si les boutons de validation n’ont pas le même travail.

**Lorsqu’ils sont utilisés de manière appropriée, les liens de commande doivent simplifier et clarifier votre interface utilisateur.** Si les résultats sont opposés, effectuez un pas à pas détaillé, passez en revue les alternatives et concentrez-vous sur ce dont vous avez vraiment besoin pour communiquer.

**Si vous n’avez qu’une seule chose...** N’utilisez pas de liens de commande pour la surcommunication. Les liens de commande doivent simplifier et clarifier la communication, et ne pas compliquer la communication.

## <a name="usage-patterns"></a>Modèles d’usage

Les liens de commande ont plusieurs modèles d’utilisation :



|                                                                                                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Réponses de page** Les liens de commande sont utilisés pour répondre à l’instruction principale et passer à la page suivante.    | avec ce modèle, les liens de commande remplacent le bouton suivant, mais il existe toujours un bouton Annuler.<br/>Les réponses de page n’impliquent pas l’engagement. étant donné que les liens de commande ressemblent à des liens et que les utilisateurs associent des liens avec navigation dans un workflow de page, les liens ne sont pas appropriés pour les pages de validation les utilisateurs doivent toujours pouvoir revenir en arrière. <br/> ![Capture d’écran montrant une boîte de dialogue « se connecter à Internet » avec des liens de commande « sans fil », « Broadband (PPPoE) » et « Dial-up ».](images/ctrl-command-links-image16.png)<br/>Dans cet exemple, des liens de commande sont utilisés pour fournir des réponses descriptives à l’instruction principale. Alors que les cases d’option peuvent être utilisées ici, les liens de commande permettent aux utilisateurs de répondre d’un simple clic.<br/> |
| **Réponses aux boîtes de dialogue** Des liens de commande sont utilisés pour répondre à l’instruction principale et fermer la boîte de dialogue.  | avec ce modèle, les liens de commande remplacent les boutons de validation (tels que OK), mais il existe toujours un bouton Annuler.<br/>Contrairement aux flux de pages, il n’existe aucun moyen d’annuler une réponse basée sur une boîte de dialogue une fois qu’elle a été effectuée. par conséquent, les liens de commande de la boîte de dialogue impliquent un engagement. <br/> ![capture d’écran de la boîte de dialogue avec des liens de commande ](images/ctrl-command-links-image17.png)<br/>Dans cet exemple, des liens de commande sont utilisés pour fournir des réponses descriptives à l’instruction principale. Alors que les cases d’option peuvent être utilisées ici, les liens de commande permettent aux utilisateurs de choisir un seul clic.<br/>                                                   |
| **Réponses détaillées** Une page ou une réponse de boîte de dialogue qui contient des informations détaillées.                          | Il peut arriver que les utilisateurs aient besoin d’informations plus détaillées pour choisir leur réponse. <br/> ![capture d’écran de la boîte de dialogue Copier un fichier et des miniatures ](images/ctrl-command-links-image18.png)<br/> Dans cet exemple, des liens de commande détaillés sont utilisés afin que les utilisateurs puissent prendre des décisions avisées. Les miniatures et les détails de fichier aident les utilisateurs à décider.<br/>                                                                                                                                                                                                                                                                                                         |



 

## <a name="guidelines"></a>Consignes

### <a name="interaction"></a>Interaction

-   **Afficher un pointeur occupé si le résultat d’un clic sur un lien de commande n’est pas instantané.** Sans commentaires, les utilisateurs peuvent supposer que le clic n’a pas eu lieu et cliquer à nouveau sur.

### <a name="presentation"></a>Présentation

-   **Toujours présenter des liens de commande dans un ensemble de deux ou plus.** Logiquement, il n’y a aucune raison de poser une question qui n’a qu’une seule réponse.

    **Incorrect :**

    ![capture d’écran de la boîte de dialogue avec un lien de commande ](images/ctrl-command-links-image19.png)

    Dans cet exemple, la boîte de dialogue apparaît pour offrir un choix à l’utilisateur, mais il n’existe qu’une instruction. Il doit s’agir d’une boîte de dialogue d’information à la place.

-   **Commencez par présenter les liens de commande les plus couramment utilisés.** L’ordre qui en résulte doit suivre à peu près la probabilité d’utilisation, mais également avoir un Flow logique.
    -   **Exception :** Les liens de commande qui aboutissent à tout doivent être placés en premier.
-   **Fournissez un bouton Annuler explicite.** N’utilisez pas de lien de commande à cet effet. Bien souvent, les utilisateurs se rendent compte qu’ils ne souhaitent pas exécuter une tâche. L’utilisation d’un lien de commande pour annuler obligerait les utilisateurs à lire tous les liens de commande avec soin pour déterminer celui qui signifie annuler. Le fait d’avoir un bouton Annuler explicite permet aux utilisateurs d’annuler une tâche de manière efficace.

    **Incorrect :**

    ![capture d’écran de la boîte de dialogue avec le lien « ne pas quitter » ](images/ctrl-command-links-image20.png)

    Dans cet exemple, le lien de commande ne pas quitter doit être un bouton Annuler.

-   **Si le fait de fournir un bouton Annuler explicite laisse un lien de commande unique, fournissez un lien de commande pour annuler et un bouton Annuler.** Ce faisant, il est clair que les utilisateurs ont le choix. Phrase ce lien de commande explique en quoi il diffère de la première réponse, au lieu de simplement « annuler » ou une variante.

    ![capture d’écran de deux liens et d’un bouton Annuler ](images/ctrl-command-links-image21.png)

    Dans cet exemple, le deuxième lien de commande indique que l’utilisateur a un choix, mais il n’est pas annulé. Toutefois, il est formulées en termes de différence par rapport au premier lien de commande.

-   **Utilisez close au lieu de Cancel si vous ne pouvez pas ramener l’environnement à son état précédent, sans effet secondaire.**
-   **N’affiche pas les liens de commande désactivés.** Si un lien de commande ne s’applique pas au contexte actuel, supprimez-le à la place. Si la suppression de tous les liens de commande qui ne s’appliquent pas laisse un lien de commande unique, éliminez la fenêtre ou la page, ou affichez une [confirmation](mess-confirm.md) si un consentement explicite de l’utilisateur est nécessaire.

### <a name="icons"></a>Icônes

-   **Tous les liens de commande nécessitent une icône.** Les icônes aident les utilisateurs à distinguer les liens de commande des liens classiques et du texte de l’interface utilisateur.
-   **Utilisez l’icône de flèche uniquement pour les liens de commande.** Les liens habituels ne doivent pas utiliser l’icône en forme de flèche, sauf s’ils sont utilisés comme substituts des liens de commande dans Windows XP.
-   **Utilisez l’icône de bouclier de sécurité pour indiquer qu’une réponse requiert une élévation immédiate.** Pour obtenir des instructions supplémentaires sur l’utilisation de l’icône de bouclier de sécurité, consultez le [contrôle de compte d’utilisateur](winenv-uac.md).
-   **Utilisez des icônes personnalisées uniquement si elles aident les utilisateurs à identifier visuellement et différencier les options.** N’utilisez pas d’icônes personnalisées si elles ne sont pas immédiatement reconnaissables ou significatives.

    **Incorrect :**

    ![capture d’écran de deux liens de commande avec des icônes personnalisées ](images/ctrl-command-links-image22.png)

    Dans cet exemple, les icônes personnalisées ne sont pas immédiatement reconnaissables.

-   **Pour les icônes personnalisées, utilisez des icônes de pixels 16x16 ou 32x32.** Utilisez les plus grandes icônes s’il y a suffisamment d’espace et qu’elles bénéficient visuellement de la plus grande taille. Si vous avez besoin de superpositions de bouclier de sécurité, utilisez des icônes de pixels 32x32 ou 48.

    ![capture d’écran de trois liens de commande avec des icônes ](images/ctrl-command-links-image23.png)

    Cet exemple utilise des icônes personnalisées 32 x 32 pixels.

    ![capture d’écran de deux liens de commande avec des icônes plus grandes ](images/ctrl-command-links-image24.png)

    Cet exemple utilise des icônes personnalisées de pixels 48, avec une superposition de bouclier de sécurité.

-   **Évitez de mélanger des icônes personnalisées avec l’icône de flèche standard dans une fenêtre ou une page.** Si vous utilisez une icône personnalisée sur une surface, essayez d’utiliser toutes les icônes personnalisées. Toutefois, préférez l’icône de flèche standard sur les icônes personnalisées sans signification.

### <a name="default-values"></a>Valeurs par défaut

-   **Sélectionnez le niveau de sécurité le plus sûr (pour éviter la perte de données ou l’accès au système) et la réponse la plus sécurisée est la valeur par défaut.** Si la sécurité et la sécurité ne sont pas des facteurs, sélectionnez la réponse la plus probable ou la plus pratique.
-   Dans la mesure du **possible, définissez la première réponse comme option par défaut** , car les utilisateurs s’attendent souvent à ce que, sauf si cette commande n’est pas logique.
-   **Pour les boîtes de dialogue, ne faites pas d’action destructrice le lien de commande par défaut** , sauf si vous avez un moyen simple d’annuler l’action.

## <a name="recommended-sizing-and-spacing"></a>Dimensionnement et espacement recommandés

![capture d’écran du dimensionnement et de l’espacement des liens de commande ](images/ctrl-command-links-image25.png)

## <a name="labels"></a>Étiquettes

> [!Note]  
> Étant donné que les liens de commande sont des réponses à une instruction principale, vous devez concevoir une [bonne instruction principale](text-ui.md) avant de déterminer ses réponses.

 

**Étiquettes des liens de commande**

-   **Choisissez une étiquette concise qui communique clairement et différencie ce que fait le lien de commande.** Elle doit être explicite et correspondre à l’instruction principale. Concentrez les étiquettes sur les différences entre les réponses. Les utilisateurs ne doivent pas avoir à déterminer ce que signifie le lien de commande ou la manière dont il diffère des autres liens de commande.

    **Incorrect :**

    ![capture d’écran d’un lien de commande redondant ](images/ctrl-command-links-image26.png)

    Dans cet exemple, quelle est la différence entre les deuxième et troisième réponses ? N’est-ce pas heureux qu’il y ait un bouton Annuler ?

-   **Commande Focus les étiquettes de lien pour aider les utilisateurs à prendre la bonne décision.** Omettez les détails qui n’affectent pas le choix. Les étiquettes n’ont pas besoin d’être une spécification complète de ce qui se passe.
-   **Démarrer des liens de commande avec un verbe.** N’utilisez pas de clic, toutefois, car l’étiquette doit communiquer ce que fait le lien de commande, et non son fonctionnement.
    -   **Exception :** Si tous les liens de commande commencent par le même verbe ou la même expression, éliminez le verbe ou l’expression redondant.
-   En général, **Utilisez une formulation positive** (ce qui vous permet d’effectuer une opération). Une formulation négative (permettant de ne pas faire un choix) est acceptable si elle rend les étiquettes plus faciles à comprendre.
-   **Utilisez une formulation parallèle et des étiquettes à une seule ligne.** Les étiquettes longues découragent la lecture et ne devraient pas être nécessaires. En outre, il est plus facile de faire référence à des étiquettes de taille modérée dans la documentation.
-   **Utilisez les majuscules comme pour les phrases.**
-   **N’utilisez pas de ponctuation de fin, sauf si l’étiquette est une question.**
-   **Attribuez une clé d’accès unique.** Pour obtenir des instructions, consultez [clavier](inter-keyboard.md).
-   **N’utilisez pas de ellipses.** Les ellipses signifient que des informations supplémentaires peuvent être nécessaires pour exécuter l’action. Les liens de commande utilisés correctement n’ont pas besoin de ellipses, car ils ont un effet immédiat.
-   **Si une réponse est fortement recommandée, ajoutez « (recommandé) » à l’étiquette.** Veillez à ajouter à l’étiquette, et non à l’explication supplémentaire.
-   **Si une réponse est destinée uniquement aux utilisateurs expérimentés, envisagez d’ajouter « (avancé) » à l’étiquette.** Veillez à ajouter à l’étiquette, et non à l’explication supplémentaire.

**Conseil :** Vous pouvez évaluer des liens de commande en imaginant qu’un ami a indiqué l’instruction principale et que vous avez répondu avec les liens de commande. En cas de réponse avec les liens de commande ne serait pas naturel ou difficile, modifiez les liens de commande et éventuellement l’instruction principale.

**Explications supplémentaires**

-   Si un lien de commande requiert une explication supplémentaire, **fournissez une explication supplémentaire**. Les explications supplémentaires décrivent la raison pour laquelle les utilisateurs peuvent souhaiter choisir une réponse ou ce qui se passe si une réponse est choisie.

    ![capture d’écran du texte décrivant les résultats de l’option ](images/ctrl-command-links-image27.png)

    Dans cet exemple, l’explication supplémentaire décrit les implications de l’option.

-   **N’utilisez pas une explication supplémentaire qui correspond à la reformulation de mot du lien de commande.** Utilisez une explication supplémentaire uniquement lorsque vous ne pouvez pas rendre un lien de commande explicite. Fournir une explication supplémentaire pour un lien de commande ne signifie pas que vous devez les fournir pour tous.
-   **Concentrez-vous sur les explications supplémentaires pour aider les utilisateurs à prendre la bonne décision.** Omettez les détails qui n’affectent pas le choix. Les explications supplémentaires n’ont pas besoin d’être une spécification complète de ce qui se passe.
-   **Utilisez une formulation parallèle et au plus trois lignes de texte.** Des explications supplémentaires découragent la lecture et ne devraient pas être nécessaires.
-   **Utilisez des phrases complètes et terminez la ponctuation.**

**Étiquettes de groupe de liens de commande**

-   **N’utilisez pas d’étiquettes de groupe.** Les instructions principales jouent le rôle d’étiquette de groupe pour les liens de commande.

## <a name="documentation"></a>Documentation

Lorsque vous faites référence à des liens de commande :

-   Utilisez le texte d’étiquette exact, y compris sa mise en majuscules, mais n’incluez pas le trait de soulignement de clé d’accès.
-   Si l’étiquette comprend un nom d’objet, omettez le nom de l’objet ou utilisez le texte de l’espace réservé.
-   Pour décrire l’interaction de l’utilisateur, utilisez le clic.
-   Dans la mesure du possible, mettez en forme l’étiquette à l’aide de texte en gras. Sinon, placez l’étiquette entre guillemets uniquement si nécessaire pour éviter toute confusion.

**Exemples :** Pour copier l’image, cliquez sur **copier et remplacer**.

Cliquez sur **Réinitialiser la carte réseau**. (Pour un lien de commande intitulé « réinitialiser le nom de l' *adaptateur* de carte réseau ».)

 

