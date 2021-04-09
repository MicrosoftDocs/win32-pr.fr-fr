---
title: Assistants
description: Malgré ce merveilleux, le nom de saugrenu, les assistants ne sont pas véritablement une forme spéciale de l’interface utilisateur, et ils n’ont qu’une gamme particulière d’utilitaires.
ms.assetid: 122d6e65-92f0-4e8a-92f7-ecd7e90665c8
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 6455c38228606932e9144c744dd217d0a7fa67e8
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "103869357"
---
# <a name="wizards"></a>Assistants

> [!NOTE]
> Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Malgré ce merveilleux, le nom de saugrenu, les assistants ne sont pas véritablement une forme spéciale de l’interface utilisateur, et ils n’ont qu’une gamme particulière d’utilitaires.

Les assistants sont utilisés pour effectuer des tâches en plusieurs étapes.

![Capture d’écran montrant l’Assistant Ajout d’imprimante avec « quel type d’imprimante voulez-vous installer ? » prompt.](images/win-wizards-image1.png)

![Capture d’écran montrant l’Assistant Ajout d’imprimante lors de la recherche d’imprimantes disponibles.](images/win-wizards-image2.png)

![capture d’écran de l’Assistant Ajout d’imprimante ](images/win-wizards-image3.png)

Plusieurs étapes d’un Assistant sont présentées sous la forme d’une séquence de pages.

Les assistants incluent généralement les types de pages suivants :

-   Les pages de choix sont utilisées pour recueillir des informations et permettre aux utilisateurs d’effectuer des choix.
-   La page valider est utilisée pour effectuer une action qui ne peut pas être annulée en cliquant sur précédent ou annuler.
-   La page progression est utilisée pour afficher la progression d’une opération longue.

La conception de l’Assistant moderne est plus efficace, ce qui rend la page de progression facultative pour les opérations plus courtes et est souvent distribuée avec la [page d’accueil](glossary.md) traditionnelle et la [page de félicitations](glossary.md) au début et à la fin.

Toutes les pages de l’Assistant possèdent les composants suivants :

-   Une barre de titre pour identifier le nom de l’Assistant, avec un bouton précédent dans l’angle supérieur gauche, et un bouton fermer avec des boutons de réduction/agrandissement et de restauration facultatifs. Notez que la barre de titre comprend également une icône pour l’identifier dans la barre des tâches.
-   Instruction principale pour expliquer l’objectif de l’utilisateur avec la page.
-   Zone de contenu avec du texte facultatif et éventuellement d’autres contrôles.
-   Une zone de commande avec au moins un bouton valider pour valider la tâche ou passer à l’étape suivante.

Bien qu’un Assistant comporte plusieurs étapes, ces étapes doivent toutes être ajoutées à une seule tâche, du point de vue de l’utilisateur. Il s’agit du principe de conception fondamental de l’Assistant « un Assistant, une tâche ».

Ainsi, dans cet article, une tâche est la fonction de base d’un Assistant (par exemple, la tâche d’un Assistant installation consiste à installer un programme). Les sous-tâches sont des aspects de la tâche plus grande (par exemple, une sous-tâche d’un assistant d’installation peut consister à configurer le programme à installer). Enfin, chaque page de l’Assistant est considérée comme une étape dans une tâche ou une sous-tâche donnée (par exemple, deux ou trois étapes peuvent être impliquées dans la configuration du programme).

**Remarque :** Les instructions relatives à l' [installation](exper-setup.md), aux [boîtes de dialogue](win-dialog-box.md)et aux [barres de progression](progress-bars.md) sont présentées dans des articles distincts.

## <a name="is-this-the-right-user-interface"></a>S’agit-il de l’interface utilisateur appropriée ?

Un Assistant peut être utilisé pour n’importe quelle tâche nécessitant plusieurs étapes d’entrée. Toutefois, les assistants effectifs ont des exigences supplémentaires :

-   **L’Assistant effectue-t-il une seule tâche atomique ?** N’utilisez pas les interactions qui ne sont pas des tâches uniques (un programme entier ne doit jamais être un Assistant, sauf s’il effectue une seule tâche). N’utilisez pas les assistants pour combiner des tâches indépendantes ou des étapes en grande partie non liées.
-   **Le nombre de questions requises peut-il être réduit ? Existe-t-il des valeurs par défaut acceptables qui fonctionnent bien dans la plupart des cas ou qui peuvent être ajustées si nécessaire ultérieurement ? Par conséquent, le nombre de pages peut-il être réduit ?** Si c’est le cas, essayez de simplifier la tâche pour qu’elle puisse être présentée sur une seule page (par exemple, une boîte de dialogue) ou éliminer complètement la nécessité d’entrée (ce qui permet d’effectuer la tâche directement).
-   **Les questions requises doivent-elles être fournies de façon séquentielle ? Existe-t-il plusieurs questions probables, mais facultatives ?** Dans ce cas, envisagez une boîte de dialogue ou une boîte de dialogue à onglets.

    **Correct :**

    ![capture d’écran de la boîte de dialogue Options d’impression ](images/win-wizards-image4.png)

    La boîte de dialogue Options d’impression de Microsoft PowerPoint contient de nombreuses options d’entrée d’utilisateur. vous pouvez donc les présenter dans un Assistant. Toutefois, il n’est pas nécessaire de les fournir de manière séquentielle, donc une boîte de dialogue est un meilleur choix.

Les assistants sont une forme relativement lourde de l’interface utilisateur. Si une solution appropriée et allégée est disponible, utilisez-la !

## <a name="design-concepts"></a>Principes de conception

### <a name="overuse-of-wizards"></a>Utilisation abusive des assistants

Historiquement, les assistants diffèrent de l’interface utilisateur ordinaire en ce qu’ils ont été conçus pour aider les utilisateurs à effectuer des tâches particulièrement complexes (avec des étapes résidant dans des emplacements disparates) et disposent souvent d’une intelligence intégrée pour aider les utilisateurs à se dérouler correctement. Aujourd’hui, toute l’interface utilisateur doit être conçue pour rendre les tâches aussi simples que possible. il n’est donc pas nécessaire d’utiliser une interface utilisateur spéciale à cet effet.

Pourtant, la conviction persiste que les assistants sont une interface utilisateur spéciale, principalement parce qu’ils sont appelés « assistants » (beaucoup plus créatifs que, par exemple, « boîtes de dialogue » et « fenêtres de propriétés »). Au lieu de cela, il est préférable de les considérer comme des tâches à plusieurs étapes et de ne pas attirer une attention particulière sur ce fait.

Avant de créer un Assistant, déterminez si les utilisateurs doivent vraiment être interrompus à partir du déroulement principal du programme. Il peut y avoir une solution contextuelle plus légère, inline, qui se sentira plus utile et efficace pour les utilisateurs. Par exemple, une fonctionnalité mal conçue dans un programme ne permet pas à un assistant de l’expliquer et de le simplifier. Cela garantit la reconception de la fonctionnalité elle-même. Un Assistant ne doit pas être utilisé en tant que bande-aide pour résoudre un problème plus basique avec le programme.

### <a name="wizards-do-have-appropriate-functions"></a>Les assistants disposent des fonctions appropriées

Les assistants sont l’une des clés permettant de simplifier l’expérience utilisateur. Elles vous permettent d’effectuer une opération complexe, telle que la configuration d’un programme, et de la décomposer en une série d’étapes simples. À chaque étape du processus, vous pouvez fournir une explication de ce qui est nécessaire et afficher les contrôles qui permettent à l’utilisateur d’effectuer des sélections et d’entrer du texte.

Certains types de tâches à plusieurs étapes se prêtent au formulaire de l’Assistant. Par exemple, dans Windows, plusieurs assistants impliquent des fonctions de connectivité (à Internet ou au réseau d’entreprise, ou à des périphériques périphériques tels que des imprimantes et des télécopieurs).

![capture d’écran de l’Assistant de connexion ](images/win-wizards-image5.png)

La connexion à un réseau est une tâche courante dans Windows appropriée pour un Assistant.

Ici, la fonction de l’Assistant consiste à effectuer une médiation entre un nom connu et stable (le système d’exploitation prêt à l’emploi) et un événement inconnu et variable (dispositifs de connectivité avec une société de téléphone ou un fournisseur de services Internet). La complexité des écosystèmes informatiques est suffisamment significative à présent qu’il est réellement utile d’utiliser des assistants pour réduire cette complexité.

Les autres types de tâches qui fonctionnent bien avec les assistants Windows incluent des fonctionnalités haut de gamme (telles que la reconnaissance vocale et de l’écriture manuscrite) et des expériences multimédias riches (telles que la configuration des options de création et de publication de films). Les assistants peuvent également être déployés pour des tâches en plusieurs étapes de base, telles que la résolution des problèmes. En résumé, si différents utilisateurs sont susceptibles de vouloir expérimenter votre programme de manière très différente, cela peut indiquer la nécessité d’un Assistant et sa capacité pour plusieurs points d’entrée utilisateur.

Pour votre programme, il est intéressant de consacrer un peu de temps à la conception pour déterminer la fonction que votre Assistant sert, et si cette fonction s’élève vraiment au niveau du déploiement d’un Assistant.

### <a name="wizard-length"></a>Longueur de l’Assistant

Les questions de conception apparaissent naturellement autour du nombre et de l’Organisation des pages et des options. Par exemple :

-   Existe-t-il un nombre optimal de pages pour un Assistant ? Ou au moins une plage souhaitée ?
-   Si l’Assistant doit être concis et rationalisé, les utilisateurs peuvent le terminer aussi rapidement que possible ?
-   Faut-il plus de pages qui nécessitent moins de choix ? Ou moins de pages avec plus de complexité ? Quelle conception est considérée comme plus utilisable ?
-   Pouvez-vous concevoir des expériences d’Assistant plus rapides en appliquant des conventions d’interface utilisateur telles que des pages à onglets ?

Microsoft a utilisé pour signaler que des assistants de trois pages ou moins sont conçus comme des assistants simples, et que ceux de quatre pages ou plus utilisent une conception avancée de l’Assistant (consultez les instructions de l' [expérience utilisateur Windows](/previous-versions/ms997609(v=msdn.10)) de 1999). Toutefois, les normes de conception de l’Assistant actuelles disparaissent de ce qui était l’une des principales différences entre les formulaires simples et avancés (l’utilisation des pages de bienvenue et de félicitations). par conséquent, ces catégories ne sont pas adéquates et le nombre de pages déterminant le choix de conception semble arbitraire.

Votre assistant doit être aussi long ou bref que la tâche l’exige ; Il n’existe aucune instruction fixe pour sa longueur. Un assistant d’une seule page doit être présenté sous la forme d’une boîte de dialogue, donc deux pages sont probablement la forme la plus condensée possible pour un Assistant.

**Correct :**

![capture d’écran de la boîte de dialogue créer un disque ](images/win-wizards-image6.png)

Cette tâche a tellement peu d’options qui la présentent comme un Assistant serait inutile. Une boîte de dialogue est le formulaire approprié pour cette interface utilisateur.

À l’autre extrémité du spectre, si vous avez un assistant qui comprend plusieurs points de décision et branches, et que les utilisateurs peuvent souvent perdre la trace de leur chemin de navigation, vous avez dépassé une limite pratique et vous devez réduire la longueur de l’Assistant. Vous pouvez également décomposer l’Assistant en plusieurs tâches distinctes.

Lorsque vous déterminez la longueur la plus appropriée pour votre Assistant, portez une attention particulière à vos utilisateurs cibles. Les programmes destinés aux utilisateurs finaux, tels que les particuliers et les employés de bureau, ont tendance à utiliser des assistants pour masquer la complexité. les assistants sont aussi courts que possible, avec une conception de page propre et simple, et des valeurs par défaut présélectionnées pour le plus grand nombre d’options possible. En revanche, les assistants serveur ou les programmes destinés aux professionnels de l’informatique ont tendance à être plus longs et plus complexes. Ce groupe d’utilisateurs cibles a une tolérance beaucoup plus élevée pour prendre des décisions de configuration et peut en fait devenir suspect si une trop grande complexité est masquée.

Si un Assistant par nature simplifie une tâche complexe, il doit le faire relativement au minimum pour un public techniquement sophistiqué, et relativement agressivement pour une base d’utilisateurs débutant.

**Correct :**

![capture d’écran de l’Assistant affichage des langues ](images/win-wizards-image7.png)

Cette page de l’Assistant est bien conçue pour les utilisateurs finaux, car elle réduit un sujet potentiellement complexe à un choix binaire simple et logique : installer ou désinstaller.

**Correct :**

![Capture d’écran montrant la page sélection des fonctionnalités de l’Assistant Installation de « SQL Server ».](images/win-wizards-image8.png)

Dans l’Assistant Installation de Microsoft SQL Server 2008, la conception des pages est plus chargée et les nombreux choix nécessitent plus de réflexion, mais le public cible est un administrateur de base de données qui s’attend à un contrôle étroit de la sélection des fonctionnalités.

Enfin, soyez attentif à la fréquence à laquelle la tâche particulière peut être exécutée. Une tâche rare peut déployer un Assistant plus long, tandis que les tâches fréquentes doivent absolument favoriser la concision.

### <a name="branching"></a>Création de branche

Pour les assistants plus longs, vous devrez peut-être créer des branches du flux de tâches dans lesquelles la séquence de pages peut varier en fonction de l’entrée utilisateur fournie « en amont ». La création de branche est par nature délocalisée pour les utilisateurs. vous devez donc concevoir l’expérience utilisateur pour transmettre la stabilité. Nous vous recommandons de ne pas avoir plus de deux points de décision qui créeront des branches dans l’intégralité de l’Assistant et pas plus d’une branche imbriquée dans une même branche.

Pour obtenir des instructions sur la création d’une expérience utilisateur stable dans un Assistant Création de branche [, consultez la](#branching) section « Instructions » de cet article.

### <a name="providing-a-navigation-guide"></a>Fournir un guide de navigation

Les guides de navigation peuvent être utiles quand il y a de nombreuses étapes dans la tâche, et que les utilisateurs peuvent perdre leur place dans la séquence, ou qu’ils veulent simplement connaître le temps nécessaire à l’exécution.

Les guides de navigation apparaissent souvent sous la forme d’une liste de pages ou de sections de l’Assistant, en regardant un peu comme une table des matières, dans une colonne ou un volet sur le côté gauche de chaque page. Bien que la liste soit persistante dans l’Assistant (la même liste de pages s’affiche sur chaque page), il existe un moyen visuel d’indiquer où l’utilisateur se trouve actuellement dans la séquence (par exemple, en utilisant le gras pour distinguer la page ou la section active).

Les guides de navigation peuvent être séquentiels ou non séquentiels. Le type séquentiel présente les pages précédentes avec les futures pages connues. Vous pouvez présenter l’avenir en termes de étapes au lieu de pages si les étapes sont connues et si les pages sont dépendantes. Vous pouvez ensuite remplir les pages dynamiquement lorsqu’elles sont connues. Étant donné que la séquence de navigation est fixe, le repère de navigation n’est pas interactif.

Les guides de navigation non séquentiels sont interactifs, ce qui permet aux utilisateurs de revisiter les pages précédemment affichées directement. Ils peuvent également ignorer la séquence de navigation pour les pages qui sont conçues pour être facultatives. Les pages facultatives doivent avoir des valeurs par défaut qui sont acceptables dans la plupart des cas. Avec ce type de guide :

-   Les pages affichées précédemment peuvent toujours être affichées directement.
-   Les pages ultérieures peuvent ne pas être affichées si elles ont des conditions préalables.
-   Les pages qui peuvent être visitées doivent être clairement distinguées de celles qui ne le peuvent pas (par exemple en utilisant des liens actifs ou désactivés), ainsi que des pages obligatoires ou facultatives.

Les utilisateurs peuvent être déconcertés quant à la signification du bouton précédent dans ce scénario. Le fait de cliquer sur précédent vous amène à la page ou à la section précédente dans le Guide de navigation, ou à la dernière page ou section affichée ? Étant donné que les assistants Windows placent à présent le bouton précédent dans l’angle supérieur gauche des pages de l’Assistant, plutôt que dans le coin inférieur droit avec les autres boutons de validation, les utilisateurs considèrent les fonctionnalités en arrière comme sur le Web. Par conséquent, la meilleure solution consiste à donner à votre bouton précédent le sens de navigation Web (cliquez sur précédent pour accéder à la dernière page ou section affichée) et utilisez le Guide de navigation de l’Assistant pour la navigation séquentielle.

### <a name="page-integrity"></a>Intégrité de la page

La conception de l’Assistant implique non seulement des décisions concernant l’ensemble du déroulement des tâches, comme la gestion de la navigation et de l’expérience de création de branche, mais également celles qui concernent les pages individuelles qui composent l’Assistant. **Le principe le plus important pour la conception de bonnes pages de l’Assistant est celui de l’intégrité : le contenu d’une page doit appartenir.**

Les pages de l’Assistant sont beaucoup plus utilisables si chacune d’entre elles se bloque de façon conceptuelle et ne traite qu’un seul aspect de la tâche globale. L' [instruction principale](glossary.md) est le principal moyen d’y parvenir. Identifiez clairement l’objectif ou l’objectif de la page pour les utilisateurs. Les [instructions supplémentaires](glossary.md)et tous les contrôles de la page se rapportent directement à l’instruction principale. Bien que les pages de l’Assistant doivent présenter aux utilisateurs des options pour lesquelles une réflexion est nécessaire, cet effort ne semble pas fonctionner, car il est étroitement axé sur l’intégrité de la page elle-même.

Malheureusement, les concepteurs d’Assistant informent souvent les utilisateurs d’un clic rapide sur le bouton suivant comme preuve de la convivialité, de la simplicité et de l’intégrité de leurs pages. La dernière expérience de l’Assistant n’est pas suivante, suivant, suivant, suivant, terminer. Bien qu’une telle expérience suggère que les valeurs par défaut ont été bien choisies, elle suggère également que l’Assistant n’était pas vraiment nécessaire, car tous les choix sont facultatifs.

En termes d’éléments visuels et de texte, réduisez ces éléments à l’étape « Bare Essentials ». Résistez à l’envie de regrouper plusieurs sous-tâches sur une seule page (l’Assistant burritos) ou de recourir à des onglets pour présenter des exigences d’entrée complexes. Une seule page doit couvrir une seule sous-tâche de la tâche globale de l’Assistant.

**Incorrect :**

![capture d’écran de l’Assistant Installation de SQL Server ](images/win-wizards-image9.png)

Avec trois onglets d’une entrée utilisateur relativement dense, cette page de l’Assistant tente d’accomplir trop de choses.

Dans la plupart des cas, conservez la taille de chaque page dans l’Assistant pour encourager une apparence cohérente. Bien que les assistants Windows autorisent les pages redimensionnables afin que la taille d’une page corresponde à la quantité de contenu, seules quelques-unes utilisent cette option.

Enfin, mettez à jour les éléments structurels de chaque page de l’Assistant par le biais de la séquence. Par exemple, ne déplacez pas le bouton précédent de l’angle supérieur gauche vers le haut dans la zone boutons de validation pour une ou deux pages. Ce niveau de cohérence de la disposition aide les utilisateurs à se sentir stables dans l’Assistant. Considérez ceci comme une ligne de base pour l’intégrité visuelle d’une page.

### <a name="finding-the-right-level-of-communication"></a>Recherche du niveau de communication approprié

Les utilisateurs disposent d’une faible tolérance pour la lecture de grands blocs de texte à l’écran, et même moins dans la surface de l’interface utilisateur dont l’objectif est de se déplacer rapidement au sein d’une tâche.

Les assistants ont tendance à communiquer. Ils occupent beaucoup d’espace sur l’écran, ce qui semble inciter un lecteur à occuper de l’espace. C’est comme une variante de la Loi de Parkinson : le texte de l’interface utilisateur se développe pour occuper l’espace disponible.

L’un de ces excès est la redondance. En raison des modèles utilisés dans le cadre de la conception de l’Assistant, la même langue peut apparaître à plusieurs emplacements sur une page, par exemple dans la barre de titre, les en-têtes, le corps du texte, les étiquettes de contrôle, etc.

Il est utile d’embaucher un éditeur professionnel pour nettoyer le texte de votre Assistant ruthlessly. Éliminez les questions et les options inutiles sur les pages individuelles et éliminez les pages entières de l’Assistant dans son ensemble (par exemple, les pages de bienvenue et de félicitations). Accédez directement au point de la page à l’aide d’une instruction principale concise, en utilisant le langage que votre public cible utilise pour décrire la tâche, et non le jargon de la technologie ou de la fonctionnalité que vous ou votre équipe utilisez en interne. Cette approche centrée sur l’utilisateur est essentielle pour améliorer la communication des assistants de votre programme.

Prêtez une attention toute particulière à la tonalité de votre Assistant : parfois, les impressions les plus durables de votre programme sont le résultat de ce que vous dites, mais comment faire ! Dans les assistants, les utilisateurs sont à l’aise avec un ton convivial et conversationnel, avec une utilisation libérale de la seconde personne pronom (« vous ») lorsque le programme demande une entrée. Pour plus d’instructions, consultez [style et Tone](text-style-tone.md).

Le fait de réduire le nombre de mots sur la page de l’Assistant est généralement possible, mais veillez à ne pas aller trop loin. Si la tâche est importante et qu’elle garantit un Assistant, les utilisateurs apprécient d’avoir suffisamment d’informations pour faire des choix judicieux. L’exemple suivant montre comment le texte de l’Assistant peut être condensé sans sacrifier la signification.

**Avant :**

![capture d’écran de l’Assistant ClearType, ébauche ](images/win-wizards-image10.png)

**Après :**

![capture d’écran de l’Assistant ClearType, modifiée ](images/win-wizards-image11.png)

La version modifiée de cette page d’Assistant fournit une instruction principale orientée tâches, supprime le paragraphe explicatif inutile sous l’instruction principale et révise l’étiquette de case à cocher pour clarifier l’objectif de la case à cocher.

**Si vous ne faites que trois choses...**

1. Mappez la tâche que vous essayez d’accomplir avec l’interface utilisateur appropriée pour effectuer la tâche. ne vous contentez pas d’utiliser par défaut un Assistant quand vous pensez avoir besoin de collecter un grand nombre d’entrées d’utilisateurs.

2. Réfléchissez bien à la longueur et à la structure de votre Assistant. préférez des assistants courts et non ramifiés pour que l’expérience reste aussi simple que possible, afin que les utilisateurs puissent revenir à leur tâche principale ou à l’intérêt de votre programme.

3. Garantir l’intégrité de chaque page de votre Assistant : le contenu d’une page doit clairement appartenir.

## <a name="guidelines"></a>Consignes

### <a name="general"></a>Général

-   **Envisagez d’abord les alternatives légères, telles que les boîtes de dialogue, les volets de tâches ou les pages uniques.** Vous n’avez pas besoin d’utiliser les assistants. vous pouvez fournir des informations et de l’aide utiles dans toutes les interfaces utilisateur.
-   **Utilisez les assistants pour les tâches en plusieurs étapes.** Utilisez les boîtes de dialogue à plusieurs pages pour les tâches à une seule étape avec des commentaires. Pour plus d’instructions, consultez [boîtes de dialogue](win-dialog-box.md).

    **Correct :**

    ![capture d’écran de la boîte de dialogue Diagnostics ](images/win-wizards-image12.png)

    ![capture d’écran des commentaires de la boîte de dialogue Diagnostics ](images/win-wizards-image13.png)

    Dans cet exemple, les diagnostics réseau Windows sont constitués de pages de progression et de résultats. Étant donné que la tâche n’est qu’une seule étape, elle ne nécessite pas les boutons de navigation dont les utilisateurs ont besoin dans un Assistant. Elle est en fait présentée sous la forme d’une boîte de dialogue à plusieurs pages.

### <a name="window-size"></a>Taille de la fenêtre

-   **Choisissez une taille de fenêtre qui peut afficher toutes les pages de l’Assistant sans défilement de page vertical ou horizontal.** Alors que les contrôles de la page peuvent nécessiter un défilement, les pages de l’Assistant ne le doivent pas.
-   **Augmentez la taille des fenêtres pour effectuer leurs tâches de façon confortable.** La mise en page ne doit pas être exigu ou obliger les utilisateurs à faire défiler ou redimensionner excessivement.
-   **Mais ne rendez pas Windows trop grand.** Les fenêtres plus grandes rendent la tâche plus complexe et nécessitent un déplacement supplémentaire pour l’interaction.
-   **Utilisez des fenêtres redimensionnables pour un assistant qui peuvent tirer parti de davantage d’espace à l’écran, mais n’en ont pas besoin.** Affectez une taille minimale appropriée. Les fenêtres redimensionnables sont utiles lorsque les pages requièrent l’interaction avec du contenu redimensionnable, par exemple des vues de liste volumineuses.

    **Correct :**

    ![capture d’écran du programme d’installation de Visual Studio, liste partielle ](images/win-wizards-image14.png)

    **Conseillé**

    ![capture d’écran du programme d’installation de Visual Studio, liste complète ](images/win-wizards-image15.png)

    Dans cet exemple, le redimensionnement de la fenêtre aide les utilisateurs à voir la liste complète.

-   **Envisagez d’utiliser des assistants dimensionnés de façon dynamique dont la taille de page change en fonction des besoins de son contenu.** Cela permet à un assistant de prendre en charge les mises en page avec un large éventail de contenu.
-   **Privilégiez le dimensionnement statique sur dynamique si les utilisateurs peuvent percevoir les modifications comme un manque de stabilité dans leur expérience de l’Assistant.** La stabilité visuelle est souvent l’hébergement du contenu. La plupart des assistants doivent adopter des tailles de fenêtre statiques standard, avec un dimensionnement dynamique réservé pour des cas spéciaux.

### <a name="wizard-length"></a>Longueur de l’Assistant

-   **Rendez votre Assistant aussi concis et rationalisé que possible.** Débarrassez-vous des options et des questions inutiles et utilisez les valeurs par défaut intelligentes pour réduire le nombre de pages requises pour l’entrée utilisateur.
    -   **Exception :** Les professionnels de l’informatique et les autres utilisateurs techniques ont une tolérance plus élevée pour les assistants plus longs et les exigences d’entrée détaillées.
-   **Faites de votre assistant un minimum de deux pages.** Un assistant à une seule page doit être repensé à la place comme une boîte de dialogue.
-   **Ne réduisez pas le nombre de pages de l’Assistant simplement en renforçant la complexité de chaque page.** Par exemple, une page d’assistant qui comprend trois onglets nécessitant une entrée utilisateur doit être repensée comme trois pages distinctes.
-   **N’augmentez pas le nombre de pages de l’Assistant en rendant chaque page aussi simple que les utilisateurs mindlessly cliquer sur suivant dans l’intégralité de la séquence.** Il s’agit d’un défaut de conception d’Assistant courant. Si une page de l’Assistant ne requiert pas au moins un degré de pensée, il n’est probablement pas nécessaire qu’elle soit dans l’Assistant.

### <a name="branching"></a>Création de branche

-   **Préférer la conception de l’Assistant sans branchement au branchement.** Les assistants qui ne sont pas des branches ont tendance à être plus simples, plus courts et faciles à parcourir. Grâce aux assistants de création de branche, il est plus difficile pour les utilisateurs de déterminer le nombre d’étapes dans la tâche, et où elles se trouvent dans la séquence.
-   **Si vous devez créer une branche, aidez les utilisateurs à se familiariser avec l’une des techniques suivantes :**
    -   **Énumérer les pages.** Une technique courante consiste à indiquer l’emplacement de l’utilisateur dans la séquence sur chaque page, par exemple avec l’expression step X de Y. Vérifiez que le point de terminaison (Y) est stable. En cas de modification de la valeur, la confiance des utilisateurs est compromise.
    -   **Incluez la notion de sous-étapes** (par exemple, étape 2A sur 6).
    -   **Effectuez des étapes indépendantes des pages, où chaque étape peut impliquer plusieurs pages.** Par exemple, un service de voyage peut utiliser l’organisation de l’Assistant en fonction de conventions de commerce électronique bien établies pour le secteur.

        **Correct :**

        ![capture d’écran de l’organisation Assistant en fonction de l’étape ](images/win-wizards-image16.png)

        Les étiquettes logiques peuvent fournir une orientation adéquate pour les utilisateurs d’un Assistant Création de branche.

    -   **Traitez les étapes facultatives comme persistantes dans la séquence d’énumération.** Par exemple, si une branche ignore quelques étapes facultatives, ignorez les étapes dans les commentaires, plutôt que pour la renumérotation. Ainsi, si un utilisateur fait un choix sur la page 2, ce qui a pour effet de rendre les pages 3 et 4 facultatives, affichez les étapes 1, 2, 5 et 6 sur 6. Ne renumérotez pas les étapes 5 et 6.
    -   **Si l’Assistant utilise une seule branche et que la branche se produit au début de la tâche, démarrez la séquence à ce stade, puis utilisez simplement l’approche sans branchement.** Autrement dit, en commençant au point de la branche, progressez dans l’ordre jusqu’à la fin de la branche.

-   **Si vous devez créer une branche, limitez le nombre de branches à un ou deux au sein d’un même Assistant.** N’incluez jamais plus d’une branche dans une branche (une branche « imbriquée »).

### <a name="commit-buttons"></a>Boutons de validation

-   **Lorsque les utilisateurs s’engagent sur une tâche, utilisez un bouton de validation qui est une réponse spécifique à l’instruction principale** (par exemple, imprimer, connecter ou démarrer). N’utilisez pas d’étiquettes génériques comme Next (qui n’implique pas engagement) ou terminer (qui n’est pas spécifique) pour la validation d’une tâche. Les étiquettes sur ces boutons de validation doivent être logiques. Démarrez toujours les étiquettes de bouton de validation avec un verbe. **Exceptions :**
    -   Utilisez terminer lorsque les réponses spécifiques sont toujours génériques, telles que enregistrer, sélectionner, choisir ou récupérer.
    -   Utilisez terminer pour modifier un paramètre spécifique ou une collection de paramètres.
-   **Un seul Assistant peut avoir plusieurs points de validation, mais un point unique est préféré.**
-   **Si nécessaire, vous pouvez renommer ou masquer les boutons de validation sur une page.** Cette flexibilité est l’un des avantages de la nouvelle conception de l’Assistant dans Windows qui n’était pas disponible dans les assistants plus anciens. Notez que le masquage d’un bouton de validation est différent de sa désactivation.
-   **Évitez de désactiver un bouton de validation positif.** Sinon, les utilisateurs doivent déduire la raison pour laquelle les boutons de validation sont désactivés. Il est préférable de laisser les boutons de validation activés et de fournir un message d’erreur utile à chaque fois qu’un problème survient. La désactivation du bouton est acceptable uniquement si la raison de cette action est évidente et non ambiguë.
-   **Ne confondez pas les boutons de navigation (suivant et précédent) avec les boutons de validation.** Ensuite, vous pouvez progresser dans l’Assistant sans engagement ; L’arrière-plan doit toujours être disponible sur la page suivante, et si vous cliquez sur précédent, vous devez annuler l’effet du dernier bouton suivant. Si ce n’est pas possible, les utilisateurs effectuent un engagement et sont indiqués par une étiquette spécifique sur le bouton valider. Pour plus d’instructions sur les boutons suivant et précédent, consultez [navigation](#providing-a-navigation-guide).

### <a name="cancel-buttons"></a>Bouton Annuler

-   **Ne demandez pas aux utilisateurs de confirmer s’ils veulent vraiment annuler.** Cela peut s’avérer ennuyeux. **Exceptions :**
    -   L’action a des conséquences significatives et, si elle est incorrecte, n’est pas facilement réparable.
    -   L’action peut entraîner une perte significative du temps ou de l’effort de l’utilisateur.
    -   L’action est clairement incohérente avec d’autres actions.
-   **Autoriser les utilisateurs à redémarrer les assistants au cas où ils auront été annulés par erreur.**
-   **Ne désactivez pas le bouton Annuler. Exceptions**
    -   Si l’annulation est néfaste, ce qui peut être le cas lors de l’exécution d’une tâche dans des assistants autonomes.
    -   Si l’annulation est impossible, ce qui peut être le cas lorsque l’Assistant n’a pas le contrôle sur toutes les étapes.

### <a name="close-buttons"></a>Boutons Fermer

-   **Utilisez la touche Fermer pour Follow-Up et les pages de saisie semi-automatique.** N’utilisez pas annuler, car la fermeture de la fenêtre n’abandonne pas les modifications ou les actions effectuées à ce stade. N’utilisez pas Done, car il ne s’agit pas d’un verbe impératif.
-   **Une fois la tâche exécutée, l’annulation doit être fermée (pour les assistants autonomes).** L’effet de la fermeture est simplement de fermer la fenêtre.

### <a name="other-controls"></a>Autres contrôles

-   **Utilisez des liens de commande uniquement pour les choix, pas pour les engagements.** Les boutons de validation spécifiques indiquent un engagement bien supérieur à celui des liens de commande dans un Assistant.
-   **Quand vous utilisez des liens de commande, masquez le bouton suivant, mais laissez le bouton Annuler.**

### <a name="using-pages-vs-dialog-boxes-or-inline-ui"></a>Utilisation des pages (par rapport aux boîtes de dialogue ou à l’interface utilisateur Inline)

-   **En général, préférez les pages aux boîtes de dialogue.** Les utilisateurs attendent des assistants qu’ils soient basés sur une page.
-   **Utilisez les boîtes de dialogue pour vous aider à compléter des pages,** par exemple avec des sélecteurs d’objets et des navigateurs.
-   **Utilisez les boîtes de dialogue pour envoyer des messages d’erreur qui s’appliquent à la page entière et qui résultent d’un clic sur un bouton de validation.**
-   **Utilisez la présentation en ligne pour les comportements dynamiques simples,** tels que la divulgation progressive et l’interface utilisateur contextuelle.
-   **Utilisez la présentation en ligne pour les messages d’erreur qui s’appliquent à des contrôles spécifiques.**

### <a name="wizard-pages"></a>Pages de l’assistant

-   **Concentrez-vous sur la prise de décision efficace.** Réduisez le nombre de pages pour vous concentrer sur Essentials. Consolidez les pages associées et prenez les pages facultatives du circuit principal. Le fait de faire en sorte que les utilisateurs cliquent sur suivant dans votre Assistant peut paraître une bonne expérience dans un premier temps, mais si les utilisateurs n’ont jamais besoin de modifier les paramètres par défaut, les pages sont probablement inutiles.
-   **Concevez chaque page de façon à obtenir une cohérence visuelle et un objectif unique.** Pour plus d’informations, consultez [intégrité des pages](#page-integrity).
-   **N’utilisez pas les pages d’accueil. rendez la première page fonctionnelle chaque fois que possible.** Utilisez une page Prise en main facultative uniquement lorsque :

    -   L’Assistant a des conditions préalables nécessaires pour terminer correctement l’Assistant.
    -   Les utilisateurs ne comprennent peut-être pas l’objectif de l’Assistant en fonction de sa première page de choix, et il n’y a pas d’espace pour obtenir une explication supplémentaire.
    -   L’instruction principale pour Prise en main pages est « avant de commencer : ».

    **Incorrect :**

    ![capture d’écran de la page de bienvenue du programme d’installation de MapPoint ](images/win-wizards-image17.png)

-   Les assistants modernes choisissent les premières pages fonctionnelles. Ici, il n’y a rien à faire, mais cliquez sur suivant. Pourquoi les utilisateurs sont-ils forcés de payer cette taxe sur leur temps précieux ?
-   **Sur les pages dans lesquelles les utilisateurs sont invités à faire des choix, optimisez les cas les plus probables.** Ces types de pages doivent présenter des choix réels, pas seulement des instructions.
    -   Si vous n’utilisez pas de page Prise en main, Expliquez l’objectif de l’Assistant en haut de la première page de choix.
-   **Utilisez les pages de validation pour clarifier la tâche lorsque les utilisateurs effectuent la validation.** En règle générale, la page de validation est la dernière page de choix et le bouton suivant est à nouveau labellisé pour indiquer la tâche en cours de validation.
    -   N’utilisez pas les pages de résumé qui résument simplement les sélections précédentes de l’utilisateur, à moins que la tâche ne soit risquée (impliquant la sécurité ou la perte de temps ou de l’argent) ou qu’il y a de bonnes chances que les utilisateurs aient besoin d’examiner leurs sélections.
-   **Utilisez les pages de progression pour afficher l’état d’une opération de longue durée.** Une fois l’opération terminée, la page progression doit passer automatiquement à l’étape suivante. Elle doit rester sur la page de progression uniquement en cas de problème que l’utilisateur doit voir. Le fait de cliquer à nouveau sur une page de progression ne doit pas avoir d’effet secondaire.
    -   **Utilisez une barre de progression unique et arrêtée.** Suivez les [instructions relatives à la barre de progression déterminées](progress-bars.md), notamment :
        -   Indiquez clairement la fin de l’opération. Ne laissez pas une barre de progression aller à 100%, sauf si l’opération est terminée.
        -   Ne pas redémarrer la progression. Une barre de progression perd sa valeur si elle redémarre (peut-être parce qu’une étape de l’opération se termine), car les utilisateurs n’ont aucun moyen de savoir à quel moment l’opération se termine. Au lieu de cela, vous devez faire en sorte que toutes les étapes de l’opération partagent une partie de la progression et que la barre de progression passe à l’achèvement une fois.
    -   **Fournissez une description concise de l’étape actuelle au-dessus de la barre de progression.** Pour les opérations rapides, un tel texte est inutile. la barre de progression seule est suffisante. Pour les opérations nécessitant une minute ou plus, le texte peut être utile.
        -   Utilisez des fragments de phrase, qui commencent généralement par un verbe, et se terminent par des points de suspension. Exemples : copie de fichiers..., installation des composants requis...
        -   Placez le texte au-dessus de la barre, et non ci-dessous.
        -   **Incorrect :**
        -   ![capture d’écran de la barre de progression avec le texte ci-dessous ](images/win-wizards-image18.png)
        -   Dans cet exemple, le texte explicatif doit apparaître au-dessus de la barre de progression.
        -   Évitez d’encombrer la page de progression avec des détails inutiles. Cette page n’est pas destinée au support technique. elle est destinée aux utilisateurs.
        -   **Incorrect :**
        -   ![capture d’écran de la barre de progression avec trop de détails ](images/win-wizards-image19.png)
        -   Dans cet exemple, les détails techniques, tels que les GUID, ne sont pas compréhensibles pour les utilisateurs.
-   **N’utilisez pas les pages de félicitations qui ne font rien, mais qui terminent l’Assistant.** Si les résultats de l’Assistant sont clairement évidents pour les utilisateurs, fermez simplement l’Assistant sur le bouton validation finale.
    -   Utilisez Follow-Up pages lorsqu’il existe des tâches associées que les utilisateurs sont susceptibles d’effectuer en tant que suivi. Évitez les tâches de suivi familières, telles que « envoyer un message électronique ».
    -   Utilisez les pages de saisie semi-automatique uniquement lorsque les résultats ne sont pas visibles et qu’il n’existe pas de meilleure façon de fournir des commentaires pour l’achèvement des tâches.
    -   Les assistants qui contiennent des pages de progression doivent utiliser une page de fin ou une page de Follow-Up pour indiquer l’achèvement des tâches. Pour les tâches de longue durée, fermez l’Assistant sur la page valider et utilisez les notifications pour envoyer vos commentaires.
-   **Utilisez les pages de résumé uniquement si l’entrée est complexe et que les utilisateurs doivent passer en revue, si la tâche implique un risque significatif (par exemple, une transition financière) ou si l’Assistant effectue une action basée sur une entrée utilisateur qui n’est pas évidente (pour créer une relation de confiance par transparence).** Souvent, les pages de résumé ne répondent pas à cette barre de gravité et peuvent être omises.
-   **Utilisez les pages d’erreur si l’Assistant ne peut pas être exécuté en raison d’un problème à partir duquel la récupération n’est pas possible.** Sur cette page, expliquez ce que le problème est en clair, sans comprendre les utilisateurs du jargon technique. Fournissez également des étapes pratiques que les utilisateurs peuvent entreprendre pour résoudre le problème. Pour plus d’instructions, consultez [messages d’erreur](mess-error.md).
    -   **Exception :** Si l’Assistant se termine avec un problème mineur à partir duquel la récupération est possible, présentez le problème en tant que tâche supplémentaire au lieu d’une erreur. Utilisez un langage positif, orienté réussite et encourageant, et non des termes tels que l’erreur, l’échec ou le problème. N’utilisez pas d’icône d’erreur.

### <a name="navigation"></a>Navigation

-   **Utilisez Next uniquement lorsque vous avancez jusqu’à la page suivante sans engagement.** L’avancement jusqu’à la page suivante est considéré comme un engagement quand son effet ne peut pas être annulé en cliquant sur précédent ou annuler.
-   **Utilisez l’arrière-plan uniquement pour corriger les erreurs.** Hormis les erreurs de correction, les utilisateurs ne doivent pas cliquer sur précédent pour progresser dans une tâche.
-   **Conserver les sélections de l’utilisateur via la navigation.** Par exemple, si l’utilisateur apporte des modifications, clique sur précédent, puis sur suivant, ces modifications doivent être conservées. Les utilisateurs ne sont pas censés devoir réentrer les modifications, sauf s’ils ont explicitement choisi de les effacer.
-   **Ne désactivez pas le bouton précédent, sauf si la répétition des étapes est néfaste.**
-   **Permettre aux utilisateurs de parcourir ou de réviser les choix dans les scénarios de navigation suivants :**
    -   L’utilisateur donne une entrée, clique sur le bouton valider, clique sur précédent pour passer en revue les modifications précédentes, ne change rien, puis clique à nouveau sur le bouton valider. Normalement, cela doit être possible et la deuxième validation doit simplement passer à la page suivante (car la tâche a déjà été effectuée).
    -   L’utilisateur donne une entrée, clique sur le bouton valider, clique sur précédent pour passer en revue les modifications précédentes, modifie une valeur, puis clique à nouveau sur le bouton valider. Normalement, cela doit être possible et la deuxième validation doit rétablir la tâche avec l’entrée modifiée (en remplaçant ou en annulant l’effet de la première).

### <a name="help"></a>Aide

-   **Concevez les pages de l’Assistant pour fournir suffisamment d’informations afin que la référence à la documentation dans l’aide du programme soit inutile.** Un Assistant fait déjà passer les utilisateurs de leur interaction directe souhaitée avec le programme. demander aux utilisateurs de rechercher de l’aide externe les supprime encore de cet État. L’aide doit être l’exception, et non la règle.
-   **Si vous devez fournir un point d’accès pour l’aide, utilisez un lien dans la partie inférieure gauche de la zone de contenu de la page (au-dessus de la zone de commande).** Ce lien doit être bref et généralement formulées sous la forme d’une question à laquelle les utilisateurs sont susceptibles de répondre.
-   **Correct :**
-   ![capture d’écran de la page de l’Assistant avec le lien d’aide ](images/win-wizards-image5.png)
-   Ce lien vers l’aide est approprié, car les informations de base en arrière-plan de ce type encombrent trop la page de l’Assistant.

## <a name="text"></a>Texte

### <a name="general"></a>Général

-   Utilisez votre et votre pour faire référence à l’utilisateur et à l’ordinateur, au document, aux paramètres, etc. de l’utilisateur. N’utilisez pas la première personne (I, My) pour faire référence à l’ordinateur ou à l’Assistant. Toutefois, il est acceptable d’utiliser la première personne dans les options que l’utilisateur sélectionne. Exemple : case à cocher **mon utilisation uniquement** .
-   Chaque page de l’Assistant doit avoir une [instruction principale](glossary.md).

### <a name="titles"></a>Titres

-   Placez le nom de l’Assistant dans la barre de titre. Utilisez la mise [en majuscules du style titre](glossary.md).
-   Les titres ne doivent pas inclure de signes de ponctuation, sauf pour ceux comportant des points d’interrogation.
-   N’incluez pas l’Assistant Word dans les titres de l’Assistant. Par exemple, utilisez l’Assistant Connexion à un réseau au lieu de l’Assistant Configuration du réseau.

### <a name="buttons"></a>Boutons

-   N’incluez pas de texte sur le bouton précédent. Utilisez le glyphe de flèche à la place, sans étiquette.
-   Ajoutez du texte sur le bouton suivant. N’utilisez pas de glyphes (tels que > ou >>) en plus du mot suivant.
-   Utilisez des étiquettes de bouton de validation spécifiques qui sont logiques et qui sont une réponse à l’instruction principale. Idéalement, les utilisateurs ne doivent pas lire d’autres éléments pour comprendre l’étiquette. Les utilisateurs sont beaucoup plus susceptibles de lire des étiquettes de bouton de commande que du texte statique.
-   Si possible, n’utilisez pas le mot terminer pour l’étiquette du bouton valider, car il existe généralement un bouton de validation mieux adapté :
    -   Si le fait de cliquer sur le bouton est validé sur la tâche (donc la tâche n’a pas déjà été effectuée), utilisez une étiquette spécifique qui commence par un verbe qui est une réponse à l’instruction principale (exemples : Print, Connect, Start).
    -   Si la tâche a déjà été effectuée dans l’Assistant, utilisez à la place la fermeture.

        **Exceptions :**

        -   Vous pouvez utiliser terminer lorsque l’étiquette spécifique est toujours générique, par exemple enregistrer, sélectionner, choisir ou récupérer.
        -   Vous pouvez utiliser terminer lorsque la tâche implique la modification d’un paramètre ou d’une collection de paramètres.

-   Démarrez les étiquettes de bouton de validation avec un verbe. Les exceptions sont OK, oui et non.
-   Utilisez la mise [en majuscules de style phrase](glossary.md).
-   N’utilisez pas de ponctuation finale.

## <a name="documentation"></a>Documentation

-   Bien que la plupart des assistants Windows ne contiennent plus le mot Assistant dans le titre, il est acceptable de faire référence aux assistants en tant qu’assistants dans la documentation. Cette référence doit être en minuscules.
-   **Correct :**
-   Si vous configurez un réseau pour la première fois, vous pouvez obtenir de l’aide à l’aide de l’Assistant **connexion à un réseau** .
-   Certains assistants hérités de versions antérieures de Windows peuvent inclure l’Assistant dans le titre. Lorsque vous faites référence à l’un de ces assistants, il est acceptable d’utiliser l' \[ \] Assistant x pour éviter de dire l’Assistant \[ x \] .
-   Reportez-vous à un écran individuel dans un Assistant sous la forme d’une page.

 

 