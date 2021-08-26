---
title: Rubans
description: Les rubans sont la méthode moderne pour aider les utilisateurs à trouver, comprendre et utiliser les commandes de manière efficace et directe \ 8212 ; avec un nombre minimal de clics, avec moins de recours à la version d’évaluation et à l’erreur, sans avoir à faire référence à l’aide.
ms.assetid: 8a4699da-9840-4622-9e94-d6d5c4e7708c
ms.custom: contperf-fy21q1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: cf74a58ae2fd9dda735c419f4ffa42b38d06c18c
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884444"
---
# <a name="ribbons"></a>Rubans

> [!NOTE]
> ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Les rubans constituent le moyen le plus efficace pour aider les utilisateurs à trouver, comprendre et utiliser des commandes efficacement et directement avec un nombre minimal de clics, avec moins besoin de recourir à une version d’évaluation et à une erreur, et sans avoir à faire référence à l’aide.

Un ruban est une barre de commandes qui organise les fonctionnalités d’un programme en une série d’onglets en haut d’une fenêtre. L’utilisation d’un ruban augmente la détectabilité des fonctions et des fonctions, permet une apprentissage plus rapide du programme dans son ensemble et rend les utilisateurs plus en mesure de contrôler leur expérience avec le programme. Un ruban peut remplacer la barre de menus et les barres d’outils traditionnelles.

![capture d’écran d’un ruban ](images/cmd-ribbons-image1.png)

Ruban typique.

Les onglets du ruban sont composés de groupes, qui sont un ensemble étiqueté de commandes étroitement liées. Outre les onglets et les groupes, les rubans sont constitués des éléments suivants :

- Un bouton d’application, qui présente un menu de commandes qui impliquent d’effectuer des opérations dans ou avec un document ou un espace de travail, tel que des commandes associées aux fichiers.
- Une barre d’outils accès rapide, qui est une petite barre d’outils personnalisable qui affiche les commandes fréquemment utilisées.
- Les onglets principaux sont les onglets qui s’affichent toujours.
- Des onglets contextuels, qui s’affichent uniquement lorsqu’un type d’objet particulier est sélectionné. Les onglets qui s’affichent toujours sont appelés des onglets principaux.
- Un jeu d’onglets est une collection d’onglets contextuels pour un type d’objet unique. Étant donné que les objets peuvent avoir plusieurs types (par exemple, un en-tête dans une table qui a une image est de trois types), plusieurs jeux d’onglets contextuels peuvent être affichés à la fois.
- Les onglets modaux, qui sont des onglets principaux affichés avec un mode temporaire particulier, tels que l’aperçu avant impression.
- Les galeries, qui sont des listes de commandes ou d’options présentées graphiquement. Une galerie basée sur les résultats illustre l’effet des commandes ou des options à la place des commandes elles-mêmes. Une galerie dans le ruban s’affiche dans un ruban, par opposition à une fenêtre indépendante.
- Info-bulles améliorées, qui expliquent de façon concise les commandes qui leur sont associées et donnent les touches de raccourci. Ils peuvent également inclure des graphiques et des références à l’aide. Les info-bulles améliorées réduisent le besoin d’aide liée à la commande.
- Lanceurs de boîte de dialogue, qui sont des boutons en bas de certains groupes qui ouvrent des boîtes de dialogue contenant des fonctionnalités liées au groupe.

les rubans ont été introduits à l’origine avec Microsoft Office 2007. pour savoir pourquoi Office a besoin d’utiliser des rubans et que les nombreux problèmes liés à l’utilisation d’un ruban sont résolus, consultez [l’histoire du ruban](/archive/blogs/jensenh/the-story-of-the-ribbon).

> [!Note]  
> Les instructions relatives aux [menus](cmd-menus.md), [barres d’outils](cmd-toolbars.md), [boutons de commande](ctrl-command-buttons.md)et [icônes](vis-icons.md) sont présentées dans des articles distincts.

## <a name="is-this-the-right-user-interface"></a>S’agit-il de l’interface utilisateur appropriée ?

Pour décider d’utiliser un ruban, posez-vous les questions suivantes :

### <a name="program-type"></a>Type de programme

- **Quel est le type de programme que vous concevez ?** Le type de programme est un bon indicateur de l’adéquation d’un ruban. Les rubans fonctionnent bien pour la création et la création de documents, ainsi que pour les visionneuses de documents et les navigateurs. Les rubans peuvent fonctionner pour d’autres types de programmes, mais d’autres formes de présentation de commande peuvent être plus appropriées. En général, les programmes légers doivent avoir une présentation de commande légère.

### <a name="discoverability-and-learning-issues"></a>Problèmes de découverte et d’apprentissage

- **Les utilisateurs ont-ils des difficultés à trouver des commandes ? Les utilisateurs demandent-ils des fonctionnalités qui se trouvent déjà dans le programme ?** Si c’est le cas, l’utilisation d’un ruban rendra les commandes plus faciles à trouver en présentant des étiquettes et des regroupements de commandes associées. L’utilisation d’un ruban évolue également mieux que les barres de menus et les barres d’outils pour une croissance future.
- **Les utilisateurs ont-ils des difficultés à comprendre les commandes du programme ? Les utilisateurs ont souvent recours à des « essais et des erreurs » pour sélectionner la commande de droite ou déterminer le fonctionnement des commandes ?** Si c’est le cas, l’utilisation d’un ruban avec des commandes orientées résultats basées sur les galeries et les aperçus dynamiques rend les commandes plus faciles à comprendre.

### <a name="command-characteristics"></a>Caractéristiques de la commande

- **Les commandes sont-elles présentées à plusieurs emplacements ? Si votre programme existe déjà, les commandes sont-elles présentées dans des barres de menus, des barres d’outils, des volets des tâches et dans la zone de travail elle-même ?** Si c’est le cas, l’utilisation d’un ruban unifier les commandes dans un emplacement unique, ce qui les rend plus faciles à trouver.
- **Les commandes s’appliquent-elles à la totalité de la fenêtre ou uniquement à des volets spécifiques ?** Les rubans fonctionnent mieux pour les commandes qui s’appliquent à la totalité de la fenêtre ou à des objets spécifiques. Les commandes sur place fonctionnent mieux pour les volets de fenêtre individuels.
- **La plupart des commandes peuvent-elles être présentées directement ? Autrement dit, les utilisateurs peuvent-ils interagir avec eux à l’aide d’un simple clic ? Si vous accédez à des commandes couramment utilisées à partir de menus et de boîtes de dialogue, pouvez-vous les Refactoriser pour qu’ils soient directs ?** Bien que certaines commandes puissent être présentées à l’aide de menus et de boîtes de dialogue, la présentation de la plupart des commandes de cette façon ne permet pas de renforcer l’efficacité d’un ruban, ce qui peut faire de la barre de menus un meilleur choix.

### <a name="command-scale"></a>Mise à l’échelle des commandes

- **Existe-t-il un petit nombre de commandes ? Les commandes les plus fréquemment utilisées peuvent-elles être présentées facilement sur une simple barre d’outils simple ?** L’utilisation d’un ruban est utile si l’ajout d’onglets principaux et contextuels aboutit à un onglet de base simple qui peut être utilisé seul pour effectuer les tâches les plus courantes. Si ce n’est pas le cas, l’avantage de l’utilisation d’un ruban peut ne pas justifier son poids supplémentaire pour un petit nombre de commandes.
- **Existe-t-il un grand nombre de commandes ? L’utilisation d’un ruban nécessite-t-elle plus de sept onglets principaux ? Les utilisateurs devront-ils constamment modifier les onglets pour effectuer des tâches courantes ?** Si c’est le cas, l’utilisation des barres d’outils (qui ne nécessitent pas de modification des onglets) et des [fenêtres de palette](cmd-toolbars.md) (qui peuvent nécessiter la modification des onglets, mais il peut y avoir plusieurs ouvertures à la fois) peut être un choix plus efficace.
- **Les utilisateurs ont-ils tendance à utiliser un petit nombre de commandes la plupart du temps ?** Dans ce cas, ils peuvent utiliser efficacement un ruban en plaçant ces commandes sous l’onglet dossier de démarrage. La modification constante des onglets rend un ruban trop inefficace.
- **Le programme bénéficie-t-il de la taille maximale de la zone de contenu du programme ?** Dans ce cas, l’utilisation d’une barre de menus et d’une barre d’outils unique est plus efficace qu’un ruban. Toutefois, si votre programme requiert au moins trois lignes de barres d’outils ou utilise des volets de tâches, l’utilisation d’un ruban est plus efficace.
- **Les utilisateurs ont tendance à travailler dans une zone spécifique au sein d’une grande fenêtre dans le programme pendant de longues périodes de temps ?** Dans ce cas, ils tirent parti de la proximité des mini-barres d’outils, des fenêtres de palette et des commandes directes. Faire passer l’aller-retour de la zone de travail au ruban serait trop inefficace.
- **Pour plus d’efficacité et de flexibilité, les utilisateurs doivent-ils apporter des modifications significatives au contenu, à l’emplacement ou à la taille de présentation de la commande ?** Dans ce cas, les barres d’outils personnalisables et extensibles et les fenêtres de palette sont un meilleur choix. Notez que certains types de barres d’outils peuvent être désancrés pour devenir des fenêtres de palette, et les fenêtres de palette peuvent être déplacées, redimensionnées et personnalisées.

Enfin, envisagez cette question ultime : est-ce **que l’amélioration de la détectabilité, la facilité d’apprentissage, l’efficacité et la productivité méritent le coût de l’espace supplémentaire et la nécessité d’utiliser des onglets pour organiser les commandes ?** Si c’est le cas, l’utilisation d’un ruban est un excellent choix. Si vous n’êtes pas sûr, envisagez de tester l’utilisation d’une conception basée sur le ruban et de la comparer à la meilleure solution.

Les rubans sont une forme de présentation de commande nouvelle et attrayante, ainsi qu’un excellent moyen de moderniser un programme. Mais comme c’est le cas, ils ne sont pas le bon choix pour chaque programme.

**Incorrect :**

![capture d’écran d’un ruban avec une calculatrice ](images/cmd-ribbons-image2.png)

N’hésitez pas à effectuer cette opération.

## <a name="seven-most-important-things"></a>Sept choses les plus importantes

1. Choisissez une solution de commande adaptée à votre type de programme. L’utilisation d’un ruban doit rendre un programme plus simple, plus efficace et plus facile à utiliser, jamais opposé. Si l’utilisation d’un ruban n’est pas appropriée, envisagez plutôt d’utiliser des commandes riches.  
2. Ne sous-estimez pas le défi de créer un ruban efficace. Ne vous attendez pas à ce qu’il s’agit d’un port simple de vos barres de menus et barres d’outils existantes. Et ne vous préoccupez pas que l’utilisation d’un ruban rend automatiquement votre programme plus performant. La volonté de valider le temps et l’effort requis pour la redéfinition d’une commande est un facteur important pour décider d’utiliser un ruban.  
3. Rendez les commandes détectables. Choisissez une conception d’onglets qui a un mappage clair, évident et unique entre vos commandes et les onglets descriptifs où elles se trouvent. Les utilisateurs doivent être en mesure de déterminer rapidement et en toute confiance l’onglet qui contient la commande qu’ils recherchent et de choisir rarement l’onglet incorrect.  
4. Rendez les commandes explicites. Les utilisateurs doivent comprendre l’effet d’une commande à partir de l’étiquette, de l’icône, de l’info-bulle et de l’aperçu. Ils ne doivent pas avoir à expérimenter ou lire une rubrique d’aide pour voir comment fonctionne une commande.  
5. Rendre l’utilisation des commandes efficace :
    - Les utilisateurs passent la plupart de leur temps sous l’onglet de démarrage.
    - Les utilisateurs doivent rarement avoir à modifier les onglets pendant les tâches courantes.
    - Lorsque la fenêtre est agrandie et que les utilisateurs se trouvent dans l’onglet approprié, les commandes les plus fréquemment utilisées ont le plus d’importance visuelle et les utilisateurs peuvent les appeler en un seul clic. Les utilisateurs peuvent exécuter toutes les autres commandes de l’onglet avec au plus quatre clics.
    - Les utilisateurs ne doivent pas avoir à ouvrir des boîtes de dialogue pour fournir des commandes et modifier les attributs dans les tâches courantes.
6. Aidez les utilisateurs à choisir des commandes et des options en toute confiance et à réduire les besoins en matière d’évaluation et d’erreur. Utilisez des commandes orientées résultats chaque fois que cela est approprié, souvent sous la forme de galeries et d’aperçus instantanés.  
7. Assurez-vous que le ruban s’adapte bien aux plus grandes tailles de fenêtre.  

## <a name="design-concepts"></a>Principes de conception

### <a name="adapting-a-ribbon-in-an-existing-program"></a>Adaptation d’un ruban dans un programme existant

Si vous pouvez simplement Refactoriser une barre de menus et une conception de barre d’outils traditionnelles d’un programme existant dans un format de ruban, cela n’a pas pour effet d’éviter la plus grande partie de la valeur de l’utilisation d’un ruban. Les rubans ont la valeur la plus grande lorsqu’ils sont utilisés pour présenter des commandes immédiates orientées résultats, souvent sous la forme de galeries et d’aperçus instantanés. Les commandes orientées résultats rendent les commandes plus faciles à comprendre et aux utilisateurs beaucoup plus efficaces et productives. Au lieu de refactoriser vos commandes existantes, il est préférable de reconcevoir entièrement la manière dont les commandes sont exécutées dans votre programme.

Ne sous-estimez pas le défi de créer un ruban efficace. Et ne vous préoccupez pas que l’utilisation d’un ruban rend automatiquement votre programme plus performant. La création d’un ruban efficace prend beaucoup de temps et d’efforts. La volonté de valider le temps et l’effort requis pour une telle conception de commande est un facteur important pour décider d’utiliser un ruban.

### <a name="the-nature-of-ribbons"></a>La nature des rubans

Par rapport aux barres de menus et barres d’outils traditionnelles, les rubans présentent les caractéristiques suivantes :

- **Interface utilisateur unique pour toutes les commandes.** Les barres de menus sont complètes et faciles à apprendre, et les barres d’outils sont efficaces et directes, mais pourquoi ne pas utiliser un peu plus d’espace à l’écran pour créer une interface utilisateur de commandes unique qui accomplit toutes ces fonctionnalités ? Avec une seule interface utilisateur, les rubans ne nécessitent pas que les utilisateurs déchiffrent l’interface utilisateur qui a la commande qu’ils recherchent.
- **Visible et explicite.** Les commandes de la barre de menus sont explicites dans leurs étiquettes, mais elles ne sont pas visibles à partir de la plupart du temps. Pour enregistrer l’espace à l’écran, les boutons de la barre d’outils sont principalement représentés par des icônes plutôt que par des étiquettes (même si certains boutons de la barre d’outils les utilisent) et dépendent des info-bulles lorsque l’icône n’est pas explicite. Toutefois, les utilisateurs connaissent généralement les icônes uniquement pour les commandes les plus couramment utilisées.
- En présentant la plupart des commandes avec des icônes étiquetées, les commandes de ruban sont visibles et explicites, et vous utilisez des info-bulles uniquement pour fournir des informations supplémentaires. Il y a peu de choses à faire ailleurs (par exemple, l’aide) pour comprendre une commande.
- **Regroupement étiqueté.** Tandis que les catégories de menu sont étiquetées, les groupes d’un menu déroulant ne le sont pas et sont indiqués uniquement avec un séparateur sans étiquette. Les groupes dans les barres d’outils sont également indiqués avec des séparateurs sans étiquette.
- En organisant des commandes dans des groupes étiquetés, les rubans facilitent la recherche des commandes et la détermination de leur objectif.
- **Modal mais pas hiérarchique.** Les barres de menus sont mises à l’échelle en créant une hiérarchie de commandes. Les menus avec de nombreux éléments peuvent utiliser un ou plusieurs niveaux de sous-menus pour fournir davantage de commandes.
- Les commandes de ruban requièrent plus d’espace que les commandes de barre d’outils. elles utilisent donc des onglets pour mettre à l’échelle. Cette utilisation des onglets rend les rubans modaux, ce qui oblige les utilisateurs à modifier les modes parfois pour rechercher des commandes. Toutefois, dans un onglet, la plupart des commandes sont directes ou utilisent un bouton ou un bouton de menu partagé unique, et non une hiérarchie.
- **Directe et immédiate.** Une commande est directe si elle est appelée avec un simple clic (autrement dit, sans naviguer dans les menus) et immédiate si elle prend effet immédiatement (autrement dit, sans boîtes de dialogue pour collecter des entrées supplémentaires). Les commandes de la barre de menus sont toujours indirectes et rarement immédiats. À l’instar des barres d’outils, la plupart des commandes de ruban sont conçues pour être directes et immédiates, les commandes les plus fréquemment utilisées étant appelées en un seul clic et sans qu’il soit nécessaire de recourir à une boîte de dialogue pour recueillir des informations supplémentaires.
- **Férer.** Les barres de menus et les barres d’outils sont principalement conçues pour améliorer l’espace. Pour offrir leurs avantages, les rubans peuvent consommer plus d’espace vertical, à peu près l’équivalent d’une barre de menus et trois lignes de barres d’outils. Étant que peu de programmes comportent au moins trois lignes de barres d’outils, les rubans consomment généralement plus d’espace que les interfaces utilisateur traditionnelles pour les commandes.
- **A un bouton d’application et une barre d’outils accès rapide.** Un ruban est toujours présenté avec un bouton d’application et une barre d’outils accès rapide. Cela permet aux utilisateurs d’accéder aux commandes relatives aux fichiers et fréquemment utilisées sans modifier les onglets et favorise la cohérence entre les programmes.
- **Personnalisation minimale.** Bien que les barres de menus aient une présentation fixe, de nombreuses barres d’outils sont tout à fait personnalisables, ce qui permet aux utilisateurs de définir des emplacements, des tailles et des contenus. Un ruban lui-même n’est pas personnalisable, mais la barre d’outils accès rapide offre une personnalisation limitée.
- **Amélioration de l’accessibilité du clavier.** Les barres de menus offrent une excellente accessibilité du clavier, car l’utilisation de la touche Alt donne directement le focus d’entrée de la barre de menus. Toutefois, il n’existe aucun mécanisme de ce type pour les barres d’outils, car ils partagent la navigation au clavier avec le contenu de la fenêtre. Par conséquent, les utilisateurs doivent accéder à la barre d’outils à l’aide de la touche Tab (qui reçoit le dernier taquet de tabulation), puis naviguer jusqu’à une commande spécifique à l’aide des touches de direction.

En revanche, les rubans offrent une meilleure accessibilité du clavier par le biais des [touches accélératrices](glossary.md), généralement avec un processus en trois étapes :

- Appuyez sur ALT pour passer en mode KeyTip.
- Appuyez sur un caractère pour choisir un onglet, le bouton d’application ou une commande dans la barre d’outils accès rapide.
- Dans un onglet, appuyez sur une ou deux lettres pour choisir une commande.

    Cette approche est très visuelle. Il est également plus flexible, ce qui lui permet d’évoluer mieux et d’avoir davantage d’affectations de touches d’accès mnémoniques.

    Ne confondez pas les touches d’accès rapide avec les touches de raccourci. Bien que les touches d’accès rapide et les touches de raccourci fournissent un accès clavier à l’interface utilisateur, elles ont des objectifs et des instructions différents. Pour plus d’informations, consultez [clavier](inter-keyboard.md).

### <a name="the-nature-of-rich-commands"></a>La nature des commandes riches

Les commandes riches font référence à la présentation et à l’interaction des commandes utilisées par les rubans, sans nécessairement utiliser un conteneur de ruban. Les commandes riches présentent les caractéristiques suivantes :

- **L’étiquetage.** Toutes les commandes reçoivent des étiquettes explicites, avec des exceptions uniquement lorsque les icônes sont extrêmement connues et que l’espace est très bien connu.

    **Correct :**

    ![capture d’écran d’un ruban de mise en forme de caractères ](images/cmd-ribbons-image3.png)

    Ces commandes sont extrêmement bien connues afin qu’elles n’aient pas besoin d’étiquettes.

    **Incorrect :**

    ![capture d’écran d’un ruban avec des icônes rarement utilisées ](images/cmd-ribbons-image4.png)

    Ces icônes inintelligibles nécessitent des étiquettes pour les commandes riches.

- **Libre.** Au lieu de dimensionnement uniforme, les commandes sont dimensionnées en fonction de leur fréquence d’utilisation et d’importance. En plus de faciliter la recherche et le clic sur les commandes les plus fréquemment utilisées, vous pouvez également les rendre plus [touchable](https://msdn.microsoft.com/library/windows/desktop/cc872774.aspx).

    ![capture d’écran d’un grand et de trois petits boutons ](images/cmd-ribbons-image5.png)

    Dans cet exemple, le bouton le plus fréquemment utilisé est plus grand que les autres.

- **Dimensionnement dynamique.** Les contrôles de commandes riches sont redimensionnés pour tirer pleinement parti de l’espace disponible, par opposition à l’utilisation d’une taille fixe et à la troncation ou à l’utilisation du dépassement de capacité lorsque la taille est trop petite.

    ![capture d’écran d’un ruban étendu avec des boutons de taille égale ](images/cmd-ribbons-image6.png)![capture d’écran d’un petit ruban avec des boutons mixtes ](images/cmd-ribbons-image7.png)

    Dans cet exemple, les boutons de commande se redimensionnent pour fonctionner correctement dans l’espace disponible.

- **Boutons partagés.** Les boutons partagés sont un bon moyen de consolider un ensemble de variations d’une commande en cas de besoin, tout en conservant l’adressage direct pour la commande la plus fréquemment utilisée.

    ![capture d’écran de la commande Enregistrer sous et de ses options ](images/cmd-ribbons-image8.png)

    Dans cet exemple, la commande Enregistrer sous utilise un bouton partagé, où le bouton principal effectue la variation la plus courante et la partie de menu révèle un menu avec des variantes de la commande.

- **Menus déroulants et galeries enrichis.** Les menus déroulants, les listes déroulantes et les galeries prennent l’espace dont ils ont besoin pour communiquer et différencier l’effet des choix, souvent en utilisant des graphiques et des descriptions de texte. Les catégories sont utilisées pour organiser de grands ensembles d’options.

    ![capture d’écran des options de menu déroulant avec des icônes ](images/cmd-ribbons-image9.png)

    Dans ces exemples, le fait de cliquer sur un bouton de menu affiche une liste de choix qui montrent leur effet.

- **Aperçus dynamiques.** Chaque fois que l’utilisateur pointe sur une option de mise en forme, le programme montre à quoi ressemblera les résultats avec cette mise en forme à l’aide du contenu réel.

    ![capture d’écran des résultats des choix de mise en forme ](images/cmd-ribbons-image10.png)

    Les aperçus dynamiques affichent les résultats de l’application d’une option de mise en forme au pointage.

- **Info-bulles améliorées.** Ces instructions expliquent de façon concise les commandes qui leur sont associées et donnent les touches de raccourci. Elles peuvent également inclure des graphiques et des références à l’aide (bien qu’elles éliminent en grande partie la nécessité d’une aide liée à la commande).

    ![capture d’écran d’une grande info-bulle avec du texte et un graphique ](images/cmd-ribbons-image11.png)

    Les info-bulles améliorées expliquent de façon concise les commandes qui leur sont associées.

Alors que les rubans peuvent ne pas convenir à tous les programmes, tous les programmes peuvent potentiellement tirer parti de commandes riches.

### <a name="ribbons-always-have-an-application-button-and-quick-access-toolbar"></a>Les rubans disposent toujours d’un bouton d’application et d’une barre d’outils accès rapide

Le bouton d’application et la barre d’outils accès rapide fournissent des commandes utiles dans n’importe quel contexte, ce qui réduit la nécessité de modifier les onglets. Bien que ces trois composants soient logiquement indépendants, un ruban doit toujours avoir un bouton d’application et une barre d’outils accès rapide. Étant donné que les commandes peuvent être placées dans le ruban ou le bouton application, vous vous demandez peut-être où placer les commandes. Le choix n’est pas arbitraire.

Le bouton application est utilisé pour présenter un menu de commandes qui impliquent d’effectuer des opérations sur ou avec un fichier, telles que des commandes qui se trouvent traditionnellement dans le menu fichier pour créer, ouvrir et enregistrer des fichiers, imprimer et envoyer et publier des documents.

En revanche, le ruban lui-même est destiné aux commandes qui affectent le contenu de la fenêtre. Les exemples incluent des commandes utilisées pour lire, modifier ou utiliser le contenu, ou modifier la vue.

Si vous utilisez un ruban, vous devez également utiliser un bouton d’application même si votre programme n’implique pas de documents ou de fichiers. Dans ce cas, utilisez le menu de l’application pour présenter les commandes d’impression, les options de programme et la sortie du programme. Bien que le bouton d’application ne soit pas nécessaire pour ces programmes, son utilisation garantit la cohérence entre les programmes. Les utilisateurs n’ont pas à effectuer de recherche pour enregistrer et annuler des commandes ou des options de programme, car ils sont toujours au même endroit.

La barre d’outils accès rapide est requise même si le ruban n’utilise qu’un seul onglet. Là encore, de tels programmes n’ont pas besoin d’une barre d’outils d’accès rapide (étant donné que toutes les commandes sont déjà présentes sur l’onglet unique), une barre d’outils d’accès rapide personnalisable offre une cohérence entre les programmes. Par exemple, si les utilisateurs ont l’habitude de cliquer sur la commande Imprimer, ils doivent pouvoir le faire dans n’importe quel programme qui utilise un ruban.

### <a name="organization-and-discoverability"></a>Organisation et détectabilité

En fournissant des onglets et des groupes, les rubans vous permettent d’organiser vos commandes pour faciliter la découverte. Le défi est que si l’organisation est mal conçue, elle risque de nuire à la détectabilité à la place. Il doit y avoir un mappage clair, évident et unique entre vos commandes et les onglets et groupes descriptifs à l’endroit où ils résident.

Les utilisateurs se formeront d’un modèle mental du ruban après l’avoir utilisé pendant un certain temps. Si ce modèle mental n’a pas de sens pour les utilisateurs, est inefficace ou est incorrect, il entraîne des confusions et des frustrations. **L’objectif le plus important de la conception d’un ruban est de faciliter la recherche rapide et en toute confiance des commandes. Si vous n’effectuez pas cette opération, la conception de votre ruban échouera.** Pour atteindre cet objectif, la conception, le test utilisateur et l’itération doivent être soigneusement effectués. Ne partez pas du principe qu’il sera facile.

Voici quelques pièges courants à éviter :

- **Évitez les noms d’onglets et de groupes génériques.** Un bon nom de groupe ou d’onglet doit décrire précisément son contenu spécifique, de préférence à l’aide d’un langage basé sur les tâches et les objectifs. Évitez les noms d’onglets et de groupes génériques, ainsi que les noms basés sur la technologie. Par exemple, presque toutes les commandes d’un programme de création et de création de documents peuvent appartenir à des onglets intitulés modifier, format, outils, options, avancé, et bien plus encore. Reposez-vous sur des étiquettes spécifiques et descriptives, et non sur la mémorisation.
- **Évitez les noms de groupes et d’onglets trop spécifiques.** Alors que nous voulons que les noms de groupes et de groupes soient spécifiques, ils ne doivent pas être si spécifiques que les utilisateurs sont surpris par leur contenu. Les utilisateurs recherchent souvent des éléments à l’aide du processus d’élimination, donc les empêchent de surRechercher vos onglets ou groupes, car le nom est trompeur.
- **Évitez les chemins d’accès multiples à la même commande, en particulier si le chemin d’accès est inattendu ou si la commande nécessite de nombreux clics pour appeler.** Il peut sembler plus pratique de trouver une commande via plusieurs chemins d’accès. Mais gardez à l’esprit que lorsque les utilisateurs trouvent ce qu’ils cherchent, ils cessent de regarder. Il est trop facile pour les utilisateurs de supposer que le premier chemin qu’ils trouvent est le seul chemin d’accès, ce qui constitue un sérieux problème si ce chemin d’accès est inefficace ou inattendu. En outre, le fait d’avoir des commandes dupliquées complique la recherche d’autres commandes pour les utilisateurs.

![capture d’écran de la commande chemin indirect vers bordures ](images/cmd-ribbons-image12.png)

Dans cet exemple, vous pouvez modifier les bordures de paragraphe à l’aide de la commande bordures de page, même s’il existe un chemin d’accès direct sur l’onglet dossier de démarrage. Si les utilisateurs recherchant des bordures de paragraphe devaient tombés dans ce chemin d’accès inattendu, ils peuvent facilement supposer qu’il s’agit du seul chemin d’accès.

- **Évitez le placement de commande arbitraire.** Supposons que vous pensez avoir un bon onglet et une bonne conception de groupe, mais que vous découvrez que plusieurs commandes ne rentrent pas dans. Il est probable que la conception de vos onglets et groupes ne soit pas aussi bonne que possible, et vous devez continuer à l’affiner. Ne résolvez pas ce problème en plaçant ces commandes là où elles n’appartiennent pas. Si vous le faites, les utilisateurs devront probablement inspecter chaque onglet pour les trouver, puis oublier rapidement leur emplacement.
- **Évitez le positionnement basé sur le marketing.** Supposons que vous disposez d’une nouvelle version de votre programme et que votre équipe marketing souhaite vraiment promouvoir ses nouvelles fonctionnalités. Il peut être tentant de les placer sous l’onglet de démarrage, mais cela est une erreur coûteuse si cela nuit à la détectabilité globale. Tenez compte des futures versions de votre produit et de la frustration de l’entreprise qui évolue en permanence.

### <a name="tabs"></a>Tabulations

La première étape consiste à passer en revue les [onglets du ruban standard](#standard-ribbon-tabs). Si les commandes de votre programme sont mappées naturellement sur les onglets standard, basez votre organisation avec onglet sur ces normes. En revanche, si les commandes de votre programme ne sont pas mappées naturellement, n’essayez pas de le forcer. Déterminez une structure plus naturelle et veillez à effectuer un grand nombre de tests utilisateur pour vous assurer que vous avez le droit.

Pour les onglets non standard, tenez compte des points suivants :

- **Chaque nom d’onglet doit décrire son contenu.** Choisissez des noms explicites spécifiques, mais pas trop spécifiques. Les utilisateurs ne doivent jamais être surpris par leur contenu.
- **Chaque nom d’onglet doit refléter son objectif.** Prenez en compte l’objectif ou la tâche associé aux commandes.
- **Chaque nom d’onglet doit être clairement distinct de tous les autres noms d’onglets.**

L’onglet dossier de démarrage est une exception à ces considérations. Si vous n’avez pas besoin d’un onglet de démarrage, la plupart des programmes le doivent. L’onglet dossier de démarrage est le premier onglet et contient les commandes les plus fréquemment utilisées. Si vous avez fréquemment utilisé des commandes qui ne rentrent pas dans les autres onglets, l’onglet dossier de démarrage est le bon endroit.

Si vous ne pouvez pas déterminer un nom d’onglet descriptif significatif, cela est probablement dû au fait que l’onglet n’est pas bien conçu. Si votre organisation de ruban ne fonctionne pas, réexaminez votre conception d’onglets.

### <a name="groups"></a>Groupes

La Division de commandes en groupes structure les commandes en jeux associés. L’étiquette de groupe explique l’objectif commun de ses commandes.

Il existe plusieurs facteurs à prendre en compte lors de la détermination de groupes et de leur présentation :

- **Regroupement standard.** Bien qu’il existe des différences significatives dans les commandes entre les programmes, il existe des [groupes standard](#standard-ribbon-groups) qui sont communs à plusieurs programmes. L’affichage de ces commandes avec les mêmes noms et emplacements similaires améliore considérablement la détectabilité.

| Correct                                                                                      | Incorrect.                                                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| ![capture d’écran du zoom séparé du groupe de modification ](images/cmd-ribbons-image13.png)<br/>Le groupe de commandes de modification inclut toutes les commandes de modification, mais n’inclut pas la commande zoom.         | ![capture d’écran du zoom inclus dans le groupe d’édition ](images/cmd-ribbons-image14.png)<br/>La commande de zoom n’est pas une commande d’édition, mais se trouve dans le groupe d’édition. |

- **Granularité.** Une structure est bonne, mais une structure trop importante rend les commandes plus difficiles à trouver. Si les noms de groupes sont génériques, vous n’avez peut-être pas suffisamment de granularité. S’il existe des groupes avec une seule ou deux commandes chacune, vous avez probablement trop d’espace (bien que la présence d’une galerie dans le ruban sans aucune autre commande dans un groupe soit acceptable).

| Correct                                                                                                 | Incorrect.                                                                                                  |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| ![capture d’écran du zoom séparé du groupe de modification ](images/cmd-ribbons-image13.png)<br/> La modification du groupe de commandes comprend toutes les commandes de modification| ![capture d’écran de la modification du groupe divisé en deux groupes ](images/cmd-ribbons-image15.png)<br/>Le groupe de commandes d’édition a été fractionné en sections trop précises. Évitez les groupes avec une ou deux commandes uniquement.|

- **Noms.** Les noms de groupes corrects expliquent le rôle de leurs commandes. Si vos noms de groupe ne sont pas, reconsidérez le nom ou le regroupement. Si vous ne pouvez pas déterminer un nom significatif et descriptif, cela est probablement dû au fait que le groupe n’est pas bien conçu.

| Correct                                                                                                 | Incorrect.                                                                                                  |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| ![capture d’écran des commandes divisées en quatre groupes ](images/cmd-ribbons-image17.png) <br/> Utilisez des noms de groupes qui sont suffisamment spécifiques pour décrire les commandes contenues dans le groupe. | ![capture d’écran d’un groupe de formats avec plusieurs commandes ](images/cmd-ribbons-image16.png) <br/> Ce nom de groupe est trop vague pour être utile. Une meilleure approche consisterait à réorganiser ces commandes en groupes plus spécifiques. |

- **Ordre.** Les personnes lues dans un ordre de gauche à droite (dans les cultures occidentales), vous pouvez penser que les groupes à l’extrême gauche sont les plus perceptibles. Toutefois, le nom de l’onglet en surbrillance et le contenu de la fenêtre tendent à jouer le rôle de [points de contact](vis-layout.md), de sorte que les groupes au centre de l’onglet reçoivent généralement plus d’attention que le groupe le plus à gauche. Placez les groupes les plus couramment utilisés dans les emplacements les plus importants et assurez-vous qu’il existe un Flow logique pour les groupes à travers l’onglet.

![capture d’écran du groupe du presse-papiers à l’extrême gauche ](images/cmd-ribbons-image18.png)

Dans cet exemple, les groupes de polices et de paragraphes sont plus perceptibles que le groupe du presse-papiers, car ils sont les premiers visibles lors du déplacement à partir du document.

![capture d’écran du groupe de suivi sur l’onglet révision ](images/cmd-ribbons-image19.png)

Dans cet exemple, le groupe de suivi reçoit la plus grande attention, en partie parce que l’onglet révision en surbrillance agit comme un point focal.

- **Uniformité.** Il peut être difficile de reconnaître les commandes lorsque la présentation de la commande a la même apparence. L’utilisation d’icônes avec différentes formes et couleurs, des groupes avec des formats différents et des commandes de différentes tailles permet aux utilisateurs de reconnaître plus facilement les groupes de commandes. Les commandes doivent avoir une taille uniforme uniquement lorsque le ruban est réduit à sa taille inférieure.

| Correct | Incorrect. |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| ![capture d’écran du groupe avec des icônes de taille différente ](images/cmd-ribbons-image20.png)<br/>Utilisez une variété de tailles d’icône pour améliorer la reconnaissance| ![capture d’écran du groupe avec des icônes de même taille ](images/cmd-ribbons-image21.png)<br/>Ces commandes semblent trop similaires, car elles sont toutes de la même taille. |

### <a name="previews"></a>Versions préliminaires

Vous pouvez utiliser différents types d’aperçus pour afficher les résultats d’une commande. En utilisant des préversions utiles, vous pouvez améliorer l’efficacité de votre programme et réduire la nécessité d’une approche d’essai et d’évaluation. Les aperçus en direct vous invitent à expérimenter et à encourager la créativité.

Voici quelques-uns des différents types d’aperçus que vous pouvez utiliser :

- **Des icônes et des graphiques statiques réalistes.** Images statiques qui donnent une indication réaliste de l’effet d’une commande. Ils peuvent être utilisés dans des galeries, des menus déroulants et des info-bulles améliorées.

![capture d’écran de la liste déroulante des polices ](images/cmd-ribbons-image22.png)

Dans cet exemple, la liste déroulante police affiche chaque nom de police à l’aide de la police elle-même.

![capture d’écran de la Galerie de miniatures de filigrane ](images/cmd-ribbons-image23.png)

Dans cet exemple, des miniatures réalistes sont utilisées pour afficher les différents filigranes.

- **Graphiques et icônes dynamiques.** Les icônes et les graphiques modifiés pour refléter l’état actuel. Ces icônes sont particulièrement utiles pour les galeries, ainsi que des boutons partagés qui modifient leur effet par défaut pour qu’ils soient identiques à la dernière action.

![capture d’écran de la Galerie de styles de paragraphes ](images/cmd-ribbons-image24.png)

dans cet exemple, Microsoft Word modifie la galerie de styles pour refléter les styles actuels.

![capture d’écran des boutons de commande de mise en forme du texte ](images/cmd-ribbons-image25.png)

Dans cet exemple, Word modifie les commandes couleur de mise en surbrillance du texte et couleur de police pour indiquer leur effet actuel.

- **Aperçus dynamiques.** Lorsque les utilisateurs pointent sur une option de mise en forme, l’aperçu instantané affiche ce à quoi ressemblent les résultats avec cette mise en forme. Les aperçus dynamiques aident les utilisateurs à effectuer des sélections plus efficacement et en toute confiance en fonction du contexte réel de l’utilisateur.

![capture d’écran du sélecteur de couleurs de commande de couleur de page ](images/cmd-ribbons-image26.png)

Dans cet exemple, la commande couleur de page effectue un aperçu instantané en indiquant l’effet des options de couleur au pointage.

Les versions préliminaires dynamiques sont une fonctionnalité puissante qui peut véritablement améliorer la productivité de vos utilisateurs, mais même des préversions statiques simples peuvent être une grande aide.

### <a name="scaling-the-ribbon"></a>Mise à l’échelle du ruban

La mise à l’échelle d’une barre d’outils est simple : si une fenêtre est trop étroite pour afficher une barre d’outils, la barre d’outils affiche ce qui tient et rend tout le reste accessible via un bouton de dépassement de capacité. L’objectif des commandes enrichies est de tirer pleinement parti de l’espace disponible. par conséquent, la mise à l’échelle d’un ruban nécessite davantage de travail de conception. Il n’y a pas de taille de ruban par défaut. vous ne devez donc pas concevoir un ruban avec une largeur particulière à l’esprit. Vous devez concevoir des dispositions avec un large éventail de largeurs et constater que l’un d’eux peut être le plus important de vos utilisateurs. La mise à l’échelle est une partie fondamentale de la conception du ruban, pas de la dernière étape. Lors de la conception d’un onglet, spécifiez les différentes dispositions pour chaque groupe (jusqu’à trois) ainsi que les combinaisons qui peuvent être utilisées ensemble. Le ruban affiche la combinaison valide la plus grande qui correspond à la taille de fenêtre actuelle.

![capture d’écran des commandes de format dans les barres d’outils du menu de dépassement de capacité ](images/cmd-ribbons-image27.png) à l’aide d’un bouton de dépassement.

![capture d’écran des rubans avec différentes largeurs ](images/cmd-ribbons-image28.png) il n’y a pas de taille de ruban par défaut. La plus petite taille est une icône de groupe contextuel unique.

## <a name="guidelines"></a>Consignes

### <a name="general"></a>Général

- **Ne combinez pas les rubans avec les barres de menus et les barres d’outils dans une fenêtre.** Les rubans doivent être utilisés à la place des barres de menus et des barres d’outils. Toutefois, un ruban peut être combiné avec des fenêtres de palette et des éléments de navigation, tels que des boutons précédent et suivant et une barre d’adresses.
- **Toujours combiner un ruban avec un bouton d’application et une barre d’outils accès rapide.**
- **Sélectionnez l’onglet le plus à gauche (généralement Accueil) au démarrage d’un programme.** Ne rendez pas le dernier onglet sélectionné persistant entre les instances de programme.
- **Affiche le ruban dans son état normal (non réduit) lorsqu’un programme est démarré pour la première fois.** Les utilisateurs laissent souvent les paramètres par défaut inchangés. ainsi, si vous réduisez le ruban au démarrage du programme, toutes les commandes seront moins efficaces. En outre, l’indication du ruban initialement réduit peut être désorientée.
- **Rendre l’état du ruban persistant entre les instances de programme.** Par exemple, si un utilisateur réduit le ruban, il doit être affiché réduit lors de la prochaine exécution du programme. Mais encore une fois, ne pas rendre le dernier onglet sélectionné persistant de cette façon.

### <a name="using-tabs"></a>Utilisation des onglets

En règle générale, si vous avez moins d’onglets, il est préférable de supprimer les onglets qui ne permettent pas d’atteindre ces objectifs.

- **Dans la mesure du possible, utilisez les onglets standard.** L’utilisation des onglets standard améliore considérablement la détectabilité, en particulier entre les programmes. Consultez les [onglets du ruban standard](#standard-ribbon-tabs) plus loin dans cet article.
- **Étiquetez le premier onglet, le cas échéant.** L’onglet dossier de démarrage doit contenir les commandes les plus fréquemment utilisées. Si vous avez fréquemment utilisé des commandes qui ne rentrent pas dans les autres onglets, l’onglet dossier de démarrage est le bon endroit.
- Ajoutez un nouvel onglet si :
  - **Ses commandes sont étroitement liées à des tâches spécifiques et peuvent être décrites avec précision par l’étiquette de l’onglet.** L’ajout de l’onglet doit aider à rendre ses commandes faciles à trouver, ce qui n’est pas plus difficile.
  - **Ses commandes sont essentiellement sans rapport avec les tâches d’autres onglets.** L’ajout de l’onglet ne doit pas nécessiter un basculement de l’onglet lors des tâches couramment exécutées.
  - **L’onglet dispose de suffisamment de commandes pour justifier l’existence d’un emplacement supplémentaire.** N’avez pas d’onglets avec quelques commandes uniquement. **Exception :** Envisagez d’ajouter un onglet avec quelques commandes s’ils sont étroitement liés à une tâche spécifique et que l’ajout de l’onglet simplifie grandement un onglet de démarrage trop complexe.
- **Pour les autres onglets, placez d’abord les onglets les plus fréquemment utilisés, tout en conservant un ordre logique sur les onglets.**
- **Optimisez la conception des onglets afin que les utilisateurs recherchent les commandes rapidement et en toute confiance.** Toutes les autres considérations sont secondaires.
- **Ne fournissez pas d’onglet aide.** Au lieu de cela, fournissez de l’aide à l’aide de l’aide et des info-bulles améliorées.
- **Utilisez un maximum de sept onglets principaux.** S’il y en a plus de sept, il devient difficile de déterminer l’onglet qui contient une commande. Bien que sept onglets principaux soient acceptables pour les applications avec de nombreuses commandes, la plupart des programmes doivent viser quatre onglets au maximum.

### <a name="contextual-tabs"></a>Onglets contextuels

- **Utilisez un onglet contextuel pour afficher une collection de commandes qui sont pertinentes uniquement lorsque les utilisateurs sélectionnent un type d’objet particulier.** S’il n’y a que quelques commandes fréquemment utilisées, il peut être plus pratique et plus stable d’utiliser un onglet normal, et de désactiver simplement les commandes lorsqu’elles ne s’appliquent pas.
- ![capture d’écran des commandes Couper et copier grisées ](images/cmd-ribbons-image29.png)<br>Il est préférable de désactiver les commandes courantes, telles que couper et copier, plutôt que d’utiliser un onglet contextuel.
- **Inclut uniquement les commandes qui sont spécifiques à un type d’objet particulier.** Ne placez pas de commandes uniquement sur un onglet contextuel si les utilisateurs peuvent en avoir besoin sans sélectionner d’abord un objet.
- **Incluez les commandes fréquemment utilisées lors de l’utilisation d’un type d’objet particulier.** Placez les commandes contextuelles générales fréquemment utilisées dans les menus contextuels et les mini-barres d’outils pour éviter le basculement par tabulation pendant les tâches couramment exécutées. Vous pouvez également envisager de placer les commandes générales de manière redondante sur un onglet contextuel si vous n’effectuez pas le changement fréquent de tabulation. Mais n’abuser pas cela, n’essayez pas d’inclure chaque commande dont un utilisateur peut avoir besoin lors de l’utilisation de l’objet.
- ![capture d’écran de la commande bordures dans l’onglet conception ](images/cmd-ribbons-image30.png)<br/>Dans cet exemple, la commande bordures est incluse dans l’onglet conception pour éviter le basculement d’onglet fréquent pendant les tâches couramment exécutées.
- **Choisissez une couleur d’onglet contextuelle différente des onglets contextuels actuellement affichés.** Le même jeu d’onglets peut apparaître ultérieurement à l’aide d’une couleur différente pour y parvenir, mais essayer d’utiliser des assignations de couleurs cohérentes entre les appels chaque fois que cela est possible.
- La **sélection d’un onglet contextuel** facilite la détectabilité, améliore la perception de la stabilité et réduit le besoin de basculer entre les onglets. Sélectionnez un onglet contextuel automatiquement lorsque :
  - **L’utilisateur insère un objet.** Dans ce cas, sélectionnez le premier onglet contextuel dans le jeu.
  - **L’utilisateur double-clique sur un objet.** Dans ce cas, sélectionnez le premier onglet contextuel dans le jeu.
  - **L’utilisateur a sélectionné un onglet contextuel, a cliqué sur l’objet, puis a cliqué immédiatement sur un objet du même type.** Dans ce cas, revenez à l’onglet contextuel sélectionné précédemment.
- **Lorsque vous supprimez un onglet contextuel qui est l’onglet actif, définissez l’onglet dossier de démarrage ou le premier onglet actif.** Cela semble le plus stable.

### <a name="modal-tabs"></a>Onglets modaux

- **Utilisez un onglet modal pour afficher une collection de commandes qui s’appliquent à un mode temporaire particulier, et aucun des onglets principaux ne s’applique.** Si certains des onglets principaux s’appliquent, utilisez plutôt un onglet contextuel et désactivez les commandes qui ne s’appliquent pas. Étant donné que les onglets modaux sont très restrictifs, ils ne doivent être utilisés que lorsqu’il n’existe aucune meilleure solution.
- ![capture d’écran de l’onglet Aperçu avant impression ](images/cmd-ribbons-image31.png)<br/>L’aperçu avant impression est un onglet modal couramment utilisé.
- **Pour fermer un onglet modal, placez la &lt; commande en mode de fermeture &gt; comme dernière commande sous l’onglet.** Utilisez l’icône Fermer pour faciliter la recherche de la commande. Donnez le mode dans la commande pour éviter toute confusion concernant ce qui est fermé.
- ![capture d’écran du bouton Fermer l’aperçu avant impression ](images/cmd-ribbons-image32.png)<br/>Dans cet exemple, l’étiquetage explicite de la commande close avec le mode supprime tout doute sur ce qui est fermé.
- **Pour fermer un onglet modal, redéfinissez également le bouton Fermer dans la barre de titre de la fenêtre pour fermer le mode au lieu du programme.** Les tests utilisateur ont montré que de nombreux utilisateurs s’attendent à ce comportement.

### <a name="standard-ribbon-tabs"></a>Onglets du ruban standard

Dans la mesure du possible, mappez les commandes de votre programme à ces onglets standard, en fonction de leur ordre d’apparition standard.

#### <a name="regular-tabs"></a>Onglets normaux

- **Associé.** Contient les commandes les plus fréquemment utilisées. S’il est utilisé, il s’agit toujours du premier onglet.
- **Insérer.** Contient des commandes pour insérer du contenu et des objets dans un document. S’il est utilisé, il s’agit toujours du deuxième onglet.
- **Mise en page.** Contient des commandes qui affectent la mise en page, notamment les thèmes, la mise en page, l’arrière-plan, la mise en retrait, l’espacement et le positionnement. (Notez que les groupes de mise en retrait et d’espacement peuvent figurer à la place dans l’onglet dossier de démarrage, s’il y a suffisamment de place.) S’il est utilisé, il est toujours le troisième onglet.
- **Révise.** Contient des commandes permettant d’ajouter des commentaires, de suivre les modifications et de comparer les versions.
- **Affichage.** contient des commandes qui affectent la vue de document, notamment le mode d’affichage, les options afficher/masquer, le zoom, la gestion des fenêtres et les macros, qui se trouvent traditionnellement dans la catégorie de menu Windows. S’il est utilisé, il s’agit du dernier onglet normal, sauf si l’onglet Développeur est affiché.
- **Revel.** Contient les commandes utilisées uniquement par les développeurs. S’il est utilisé, il est masqué par défaut et le dernier onglet normal lorsqu’il est affiché.

La plupart des programmes n’ont pas besoin des onglets révision et développeur.

#### <a name="standard-contextual-tabs"></a>Onglets contextuels standard

- **Format.** Contient des commandes relatives à la modification du format du type d’objet sélectionné. S’applique généralement à une partie d’un objet.
- **Nomination.** Contient des commandes, souvent dans des galeries, pour appliquer des styles au type d’objet sélectionné. S’applique généralement à l’objet entier.
- **Dispose.** Contient des commandes pour modifier la structure d’un objet complexe, tel qu’un tableau ou un graphique.

Si vous avez des commandes contextuelles liées au format, à la conception et à la mise en page, mais pas suffisantes pour plusieurs onglets, il vous suffit de fournir un onglet format.

### <a name="standard-groups"></a>Groupes standard

- **Dans la mesure du possible, utilisez des groupes standard.** Le fait d’avoir des commandes communes avec les mêmes noms et des emplacements similaires améliore considérablement la détectabilité. Consultez les [groupes de ruban standard](#standard-ribbon-groups) plus loin dans cet article.
- **Ajoutez un nouveau groupe** si :
  - **Ses commandes sont étroitement liées et peuvent être décrites avec précision par l’étiquette de groupe.** L’ajout du groupe doit aider à rendre ses commandes faciles à trouver, ce qui n’est pas plus difficile.
  - **Ses commandes ont une relation plus faible avec les commandes dans d’autres groupes.** Alors que toutes les commandes d’un onglet doivent être étroitement liées, certaines relations de commande sont plus fortes que d’autres.
  - **Le groupe a suffisamment de commandes pour justifier l’existence d’un emplacement supplémentaire.** Recherchez les commandes 3-5 pour la plupart des groupes. Évitez d’avoir des groupes avec seulement 1-2 commandes, bien qu’il soit acceptable d’avoir une galerie dans le ruban sans aucune autre commande dans un groupe. Avoir de nombreux groupes avec une seule commande suggère une structure trop importante ou une absence de cohésion de commande.
- **Ne pas surOrganiser** en ajoutant des groupes là où ils ne sont pas nécessaires.
- **Envisagez de fractionner un groupe** dans les cas suivants :
  - ![capture d’écran du groupe de commandes désorganisé ](images/cmd-ribbons-image35.png)<br/>Le groupe a de nombreuses commandes de tailles et de besoins de l’organisation.
  - ![capture d’écran de deux noms de groupes de paragraphes longs ](images/cmd-ribbons-image33.png)<br>Le groupe possède des commandes qui tirent beaucoup parti de l’utilisation d’étiquettes supplémentaires.
- **Placez les groupes les plus couramment utilisés dans les emplacements les plus importants et assurez-vous qu’il existe un ordre logique pour les groupes à travers l’onglet.**
- **Optimisez la conception de groupe afin que les utilisateurs recherchent les commandes rapidement et en toute confiance.** Toutes les autres considérations sont secondaires.
- **Ne mettez pas à l’échelle des groupes contenant un seul bouton vers une icône de groupe contextuelle.** En cas de mise à l’échelle verticale, laissez-les sous la forme d’un seul bouton.
- **Utilisez un maximum de sept groupes.** S’il y a plus de sept groupes, il devient plus difficile de déterminer quel groupe a une commande.

### <a name="standard-ribbon-groups"></a>Groupes de ruban standard

Dans la mesure du possible, mappez les commandes de votre programme à ces groupes standard, qui sont fournis dans leurs onglets associés dans leur ordre d’apparition standard.

#### <a name="main-tab"></a>Onglet principal

- Presse-papiers
- Police
- Paragraph
- Modification

#### <a name="insert-tab"></a>Onglet Insérer

- Tables
- Illustrations

#### <a name="page-layout-tab"></a>Onglet mise en page

- Thèmes
- Mise en page
- Réorganiser

#### <a name="review-tab"></a>Onglet révision

- Vérification linguistique
- Commentaires

#### <a name="view-tab"></a>Onglet Affichage

- Vues de document
- Afficher/Masquer
- Zoom
- Fenêtre

### <a name="commands"></a>Commandes

- ![capture d’écran de la commande numéros de ligne sur le ruban ](images/cmd-ribbons-image36.png)<br/>**Tirez parti de la détectabilité et de l’extensibilité des rubans en exposant toutes les commandes couramment utilisées.** Le cas échéant, déplacez les commandes fréquemment utilisées à partir des boîtes de dialogue vers le ruban, en particulier celles qui sont connues pour être difficiles à trouver. Dans l’idéal, les utilisateurs doivent être en mesure d’effectuer des tâches courantes sans utiliser de boîtes de dialogue.

- **N’utilisez pas l’extensibilité des rubans pour justifier l’ajout d’une complexité inutile.** Continuez à exercer la contrainte n’ajoutez pas de commandes à un ruban juste parce que vous pouvez. Gardez l’expérience de commande globale simple. Voici les méthodes permettant de simplifier la présentation :
  - ![capture d’écran de la mini barre d’outils et du menu contextuel ](images/cmd-ribbons-image37.png)</br>**Utilisez les menus contextuels et les mini-barres d’outils pour les commandes contextuelles sur place.**
  - **Déplacez (ou conservez) rarement les commandes utilisées dans les boîtes de dialogue.** Utilisez les lanceurs de boîte de dialogue pour accéder à ces commandes. Vous pouvez toujours utiliser les boîtes de dialogue avec des rubans ! Essayez simplement de réduire la nécessité de les utiliser lors de tâches courantes.
  - **Éliminez les fonctionnalités redondantes, rarement utilisées.**

#### <a name="presentation"></a>Présentation

- **Présentez chaque commande sur un seul onglet. Évitez les chemins d’accès multiples à la même commande, en particulier si la commande requiert de nombreux clics à appeler.** Il peut sembler plus pratique de trouver une commande via plusieurs chemins d’accès. Mais gardez à l’esprit que lorsque les utilisateurs trouvent ce qu’ils cherchent, ils cessent de regarder. Il est très facile pour les utilisateurs de supposer que le premier chemin qu’ils trouvent est le seul chemin d’accès, ce qui constitue un sérieux problème si ce chemin d’accès est inefficace. **Exception :** Les onglets contextuels peuvent dupliquer quelques commandes à partir des onglets page d’hébergement et insérer si cela empêche la modification des onglets pour les tâches contextuelles courantes.
- **Dans un groupe, placez les commandes dans leur ordre logique, tout en donnant la préférence aux commandes les plus fréquemment utilisées.** Globalement, les commandes doivent avoir un flot logique pour faciliter leur recherche, tout en continuant d’afficher les commandes les plus fréquemment utilisées. En règle générale, les commandes avec des icônes de pixels 32x32 apparaissent avant les commandes avec des icônes de 16x16 pixels pour faciliter l’analyse entre les groupes.
- **Évitez de placer des commandes destructrices à côté des commandes fréquemment utilisées.** Une commande est considérée comme destructrice si son effet est répandu et qu’elle ne peut pas être facilement annulée, ou bien l’effet n’est pas immédiatement visible.
- **Utilisez des séparateurs pour indiquer des commandes étroitement liées, telles qu’un ensemble d’options s’excluant mutuellement.**
- ![capture d’écran des groupes de polices et de paragraphes ](images/cmd-ribbons-image3.png)<br/> **Envisagez d’utiliser des groupes de styles de barres d’outils pour les ensembles de commandes fortement connues et connues qui n’ont pas besoin d’étiquettes.** Cela vous permet de présenter de nombreuses commandes dans un espace compact sans affecter la détectabilité et la facilité d’apprentissage. Pour être si bien connu, ces commandes sont fréquemment utilisées, reconnues instantanément et ont tendance à se trouver dans l’onglet de démarrage.

- **Utilisez des icônes de pixels de 32x32 pour les commandes étiquetées les plus fréquemment utilisées et importantes.** Lors de la mise à l’échelle d’un groupe, rendez ces commandes le dernier à convertir en icônes de pixels 16x16.
- **Évitez le placement de commande arbitraire.** Réfléchissez bien à la conception de votre onglet et de votre groupe pour vous assurer que les utilisateurs ne perdent pas de temps à inspecter chaque onglet pour trouver la commande souhaitée.
- **Évitez le positionnement basé sur le marketing.** Les objectifs de marketing autour de la promotion de nouvelles fonctionnalités ont tendance à changer au fil du temps. Tenez compte des futures versions de votre produit et de la frustration de l’entreprise qui évolue en permanence.

#### <a name="interaction"></a>Interaction

- **Désactivez les commandes qui ne s’appliquent pas au contexte actuel, ou qui aboutiront directement à une erreur.** Si utile, utilisez l' [info-bulle améliorée](glossary.md) pour expliquer la raison pour laquelle la commande est désactivée. Ne masquez pas ces commandes, car cela peut entraîner la modification de la disposition du ruban, rendant l’instabilité de la présentation du ruban.
- **Ne mettez pas à jour les étiquettes de commande dynamiquement.** Là encore, cela peut entraîner la modification de la disposition des onglets, ce qui entraîne une apparence instable. Au lieu de cela, concevez des commandes pour qu’elles fonctionnent avec des étiquettes constantes.

    | Correct                                                                                       | Incorrect.                                                                 |
    |-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
    | ![capture d’écran de la note d’insertion et de la suppression ](images/cmd-ribbons-image38.png)<br/> Désactiver les commandes lorsqu’elles ne sont pas disponibles | ![capture d’écran de la note d’insertion, aucune note de suppression ](images/cmd-ribbons-image39.png)<br/>Ne pas masquer les commandes, même lorsqu’elles ne sont pas disponibles |

- **Préférer les contrôles directs.** Une commande est directe si elle est appelée avec un simple clic (autrement dit, sans naviguer dans les menus). Toutefois, à l’exception des galeries dans le ruban, les contrôles directs ne prennent pas en charge l’aperçu instantané, donc la nécessité de l’aperçu en direct est également un facteur.
- **Utilisez l’aperçu instantané** pour indiquer l’effet des options lorsqu’une commande fait partie d’un ensemble d’options de mise en forme associé, et l’aperçu instantané est important et pratique, en particulier si les utilisateurs sont susceptibles de choisir l’option incorrecte dans le cas contraire.
  - Si la commande est fréquemment utilisée, utilisez une galerie dans le ruban pour en indiquer la direction.
  - Si la commande est rarement utilisée, utilisez une galerie déroulante.
- **Exposez des commandes directes** à l’aide des contrôles suivants dans l’ordre de préférence suivant
  - **Boutons de commande, cases à cocher, cases d’option et galeries sur place.** Ils sont toujours directs.
  - **Boutons partagés.** Direct pour la commande la plus courante, mais indirect pour les variantes de commande.
  - **Boutons de menu.** Elles sont indirectes, mais présentent de nombreuses commandes faciles à trouver.
  - **Zones de texte (avec des contrôles spin).** L’entrée de texte nécessite généralement plus de travail que les autres types de contrôle.
- ![capture d’écran du ruban avec uniquement des boutons de menu ](images/cmd-ribbons-image42.png)</br>Si votre ruban se compose essentiellement de boutons de menu lorsqu’il est affiché en pleine taille, vous pouvez également utiliser une barre de menus.
- **Préférer les commandes immédiates.** ![capture d’écran du bouton fractionner l’impression et de son sous-menu ](images/cmd-ribbons-image43.png)<br/>Une commande est immédiate si elle prend effet immédiatement (autrement dit, sans boîtes de dialogue pour collecter des entrées supplémentaires). Si une commande peut nécessiter une entrée, envisagez d’utiliser un bouton partagé, avec la commande immédiate dans la partie de bouton et les commandes qui requièrent une entrée dans le sous-menu.

### <a name="galleries"></a>Galeries

**Utilisez une [Galerie](glossary.md)** si :

- **Il existe un ensemble bien défini de choix parmi ceux que les utilisateurs choisissent généralement.** Il peut y avoir un nombre illimité de variations, mais les sélections probables doivent être bien contenues. Si les choix ne sont pas étroitement liés, envisagez d’utiliser des galeries distinctes.
- **Les choix sont mieux exprimés visuellement, tels que les fonctionnalités de mise en forme.** L’utilisation de miniatures facilite l’exploration, la compréhension et la création de choix. Alors que les choix peuvent être étiquetés, la sélection est effectuée visuellement et les étiquettes de texte ne doivent pas être nécessaires pour comprendre les choix.
- **Les choix montrent le résultat obtenu immédiatement en un seul clic.** Il ne doit y avoir aucune boîte de dialogue de suivi pour clarifier l’intention de l’utilisateur ou un ensemble d’étapes pour obtenir le résultat indiqué. Si les utilisateurs peuvent souhaiter ajuster le choix, laissez-les le faire par la suite.

**Utilisez une galerie dans le ruban dans les** cas suivants :

- **Les choix sont fréquemment utilisés.** Les choix nécessitent de l’espace et méritent l’espace potentiellement pris par d’autres commandes.
- **Pour une utilisation standard, il n’est pas nécessaire de regrouper ou de filtrer les choix présentés.**
- **Les choix peuvent s’afficher efficacement dans la hauteur d’un ruban (48 pixels).**

#### <a name="thumbnails-in-galleries"></a>Miniatures dans les galeries

**Choisissez la plus petite taille de miniature de la Galerie standard** qui effectue le travail.

- Pour les galeries dans le ruban, utilisez des miniatures de 16x16, 48 ou 64x48 pixels.
- Pour les galeries déroulantes, utilisez des miniatures de 16x16, 32x32, 48, 64x48, 72x96, 96x72, 96x96 ou 128 x 128 pixels.
- Tous les éléments de la Galerie doivent avoir la même taille de miniature.

Pour les galeries dans le ruban :

- **Afficher un minimum de trois choix ; en savoir plus s’il y a de la place.** S’il n’y a pas suffisamment d’espace pour afficher au moins trois choix dans la taille de fenêtre classique, utilisez plutôt une galerie déroulante.
- **Développez galeries dans le ruban pour tirer parti de l’espace disponible.** Utilisez l’espace supplémentaire pour afficher plus d’éléments et les rendre plus faciles à choisir en un seul clic.

Pour les galeries déroulantes :

- **Affichez la galerie à partir d’une zone de liste déroulante, d’une liste déroulante, d’un bouton partagé ou d’un bouton de menu.**
- **Si l’utilisateur clique sur la fenêtre principale pour faire disparaître la Galerie déroulante, il vous suffit de faire disparaître la Galerie sans sélectionner ni modifier le contenu de la fenêtre principale.**
- **Si une galerie a de nombreux choix et que certains choix sont rarement utilisés, simplifiez la Galerie par défaut en vous concentrant sur les choix couramment utilisés.** Pour les commandes restantes, fournissez une commande appropriée en bas de la liste déroulante Galerie.
  - Si la commande affiche une liste d’autres variantes, nommez-la « autres `singular feature name` options... »
  - Si la commande affiche une boîte de dialogue qui permet aux utilisateurs de créer leurs propres options personnalisées, nommez-la « personnalisé `feature name` ... ».
- **Organiser les choix en groupes, si cela permet d’améliorer l’efficacité de la navigation.**
- ![capture d’écran de la Galerie et des filtres de symboles ](images/cmd-ribbons-image44.png)<br/>**Si une galerie comporte de nombreux éléments, envisagez d’ajouter un filtre pour aider les utilisateurs à trouver des choix plus efficacement.** Pour éviter toute confusion, affichez initialement la Galerie non filtrée. Toutefois, la plupart des galeries ne doivent pas nécessiter de filtre, car elles ne devraient pas avoir autant de choix et l’utilisation de groupes devrait suffire.

### <a name="command-previews"></a>Aperçus de commande

- **Utilisez des aperçus pour montrer l’effet d’une commande sans que les utilisateurs aient à l’exécuter en premier.** En utilisant des préversions utiles, vous pouvez améliorer l’efficacité et la facilité d’apprentissage de votre programme, et réduire la nécessité d’une évaluation et d’une erreur. Pour connaître les différents types d’aperçus de commande, consultez la section [aperçus](#previews) dans les concepts de conception de cet article.
- **Pour les aperçus instantanés, assurez-vous que la préversion peut être appliquée et l’état actuel restauré dans les 500 millisecondes.** Cela nécessite la possibilité d’appliquer des modifications de mise en forme rapidement et de façon interruptible. Les utilisateurs doivent être en mesure d’évaluer les différentes options rapidement pour que les aperçus en direct bénéficient de tous leurs avantages.
- **Évitez d’utiliser du texte dans les aperçus.** Dans le cas contraire, les images d’aperçu devront être localisées.

### <a name="icons"></a>Icônes

- ![capture d’écran de la liste déroulante et des cases à cocher ](images/cmd-ribbons-image45.png)<br/>**Fournissez des icônes pour tous les contrôles de ruban, à l’exception des listes déroulantes, des cases à cocher et des cases d’option.** La plupart des commandes requièrent des icônes de pixels 32 x 32 et 16 x 16 (seules les icônes de 16 x 16 pixels sont utilisées par la barre d’outils accès rapide). Les galeries utilisent généralement des icônes de pixels 16x16, 48 ou 64x48.
- **Fournissez des icônes uniques.** N’utilisez pas la même icône pour différentes commandes.
- **Vérifiez que les icônes du ruban sont clairement visibles par rapport à la couleur d’arrière-plan du ruban.** Évaluez toujours les icônes du ruban en mode de contraste élevé.
- **Choisissez des conceptions d’icône qui communiquent clairement leur effet, en** particulier pour les commandes les plus fréquemment utilisées. Les rubans bien conçus présentent des icônes explicites pour aider les utilisateurs à trouver et à comprendre efficacement les commandes.
- **Choisissez des icônes qui peuvent être reconnaissables et pouvant être distinguées, en** particulier pour les commandes les plus fréquemment utilisées. Assurez-vous que les icônes ont des formes et des couleurs distinctives. Cela aide les utilisateurs à trouver rapidement les commandes, même s’ils ne se souviennent pas du symbole d’icône.

    | Correct                                                                                                 | Incorrect.                                                                               |
    |--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
    | ![capture d’écran de l’injecteur d’yeux bleus et du crayon jaune ](images/cmd-ribbons-image46.png)<br/>Utilisez la forme et la couleur pour rendre les icônes faciles à distinguer. | ![capture d’écran de la pipette bleue et du crayon bleu ](images/cmd-ribbons-image47.png)<br/> Les icônes de même couleur sont difficiles à distinguer|

- ![capture d’écran de la commande comments dans le conteneur Popup ](images/cmd-ribbons-image48.png)<br/>**Envisagez de créer des icônes de groupe contextuel en plaçant l’icône de 16 x 16 pixels de la commande la plus visible dans le groupe à l’intérieur d’un conteneur visuel de 32 x 32 pixels.** Vous n’êtes pas obligé de créer des icônes différentes pour les groupes contextuels.
- ![capture d’écran des boutons de commande de mise en forme du texte ](images/cmd-ribbons-image25.png)<br/>**Si utile, modifiez l’icône pour refléter l’état actuel.** Cela s’avère particulièrement utile pour les boutons partagés dont l’effet par défaut peut changer.
- **Vérifiez que les icônes du ruban sont conformes aux règles d’icône de style Aero.** Toutefois, les icônes de ruban sont affichées directement au lieu d’être affichées en perspective.

| Correct                                                                                                 | Incorrect.                                                                               |
    |--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
    | ![capture d’écran des icônes de commande à deux dimensions ](images/cmd-ribbons-image49.png)<br/> Utilisez des icônes à deux dimensions.|![capture d’écran des icônes de commande en trois dimensions ](images/cmd-ribbons-image50.png)<br/> N’utilisez pas d’icônes en trois dimensions. |
 
### <a name="enhanced-tooltips"></a>Info-bulles améliorées

- **Toutes les commandes de ruban doivent avoir des info-bulles améliorées** pour fournir le nom de la commande, la touche de raccourci, la description et des informations supplémentaires facultatives. Évitez les info-bulles qui restatent simplement l’étiquette.

    **Incorrect :**

    ![capture d’écran de l’info-bulle qui répète le nom de la commande ](images/cmd-ribbons-image51.png)

    Dans cet exemple, l’info-bulle REstate simplement l’étiquette de la commande.

- **Lorsque cela est possible, décrivez complètement la commande à l’aide d’une description concise.** Lien pour obtenir de l’aide uniquement si une explication supplémentaire est vraiment nécessaire.

    **Incorrect :**

    ![capture d’écran de l’info-bulle pour la commande Strikethrough ](images/cmd-ribbons-image52.png)

    Dans cet exemple, la commande n’a pas besoin d’aide.

- **Si utile, illustrez l’effet de la commande à l’aide d’un aperçu.**

    ![capture d’écran de l’info-bulle et du graphique pour l’insertion d’un graphique ](images/cmd-ribbons-image53.png)

    Dans cet exemple, l’image d’info-bulle illustre l’effet de la commande.

Pour obtenir des instructions sur l’étiquetage, consultez [étiquettes d’info-bulle améliorées](#enhanced-tooltips).

### <a name="access-keys-and-keytips"></a>Touches d’accès et touches accélératrices

Les touches accélératrices sont le mécanisme utilisé pour afficher les touches d’accès pour les commandes affichées directement sur un ruban.

Les clés d’accès pour les commandes de menu déroulant sont indiquées par un caractère souligné. Ils diffèrent des clés d’accès de menu des manières suivantes :

- Deux touches d’accès aux caractères peuvent être utilisées. Par exemple, vous pouvez utiliser le mode FP pour accéder à la commande reproduire la mise en forme.
- Les affectations de touches d’accès s’affichent à l’aide de conseils plutôt que de soulignements, de sorte que la largeur des caractères et les descendants ne sont pas un facteur déterminant pour créer des affectations.

- **Affectez des clés d’accès à tous les onglets et commandes du ruban.** La seule exception possible concerne les commandes provenant de compléments hérités.
- **Pour le bouton de l’application et la barre d’outils accès rapide :**
  - Affectez la valeur F au bouton de l’application. Cette attribution est utilisée en raison de la similarité du bouton de l’application au menu fichier traditionnel.
  - ![capture d’écran des info-bulles de commandes sur un ruban ](images/cmd-ribbons-image54.png)<br/>Pour la barre d’outils accès rapide et les listes de fichiers récemment utilisées, assignez des touches d’accès numérique.
- ![capture d’écran montrant les touches accélératrices pour les onglets ](images/cmd-ribbons-image55.png)<br/>**Pour les onglets :**
  - Affectez H à la page d’hébergement.
  - En commençant par les onglets les plus fréquemment utilisés, attribuez la première lettre de l’étiquette.
  - Pour tous les onglets qui ne peuvent pas être assignés à la première lettre, choisissez une consonne distinctive ou une voyelle dans l’étiquette.
  - Pour les programmes qui ont été utilisés pour prendre en charge les barres de menus, efforcez-vous de maintenir la compatibilité des clés d’accès dans la meilleure mesure possible. Évitez d’attribuer différentes significations aux clés d’accès à partir de catégories de menu héritées. Par exemple, si la version de barre de menus héritée d’un programme avait un menu Edition, efforcez-vous d’utiliser une clé d’accès E à l’onglet équivalent. S’il n’y a pas d’onglet équivalent, n’attribuez pas de clé d’accès E à un onglet pour éviter toute confusion.
- ![capture d’écran montrant les touches accélératrices pour un ruban ](images/cmd-ribbons-image56.png)<br/>**Pour les commandes, les menus et les sous-menus du ruban :**
  - Assigner des combinaisons de touches d’accès uniques dans un onglet. Vous pouvez réutiliser les combinaisons de touches d’accès dans différents onglets.
  - Dans la mesure du possible, affectez les clés d’accès standard pour les commandes couramment utilisées. Consultez la [table des clés d’accès standard](inter-keyboard.md).
  - Pour les autres commandes :
    - Pour les commandes les plus fréquemment utilisées, choisissez lettres au début du premier ou du deuxième mot de l’étiquette, de préférence la première lettre.
    - Pour les commandes moins fréquemment utilisées, choisissez des lettres qui sont une consonne distinctive ou une voyelle dans l’étiquette, telle que « x » dans « quitter ».
    - Pour les commandes et les lanceurs de boîte de dialogue les moins fréquemment utilisés, utilisez deux lettres si nécessaire.
    - Pour les menus et les sous-menus, utilisez une seule lettre pour réduire le nombre de séquences de touches requises pour la commande complète.
    - N’utilisez pas de clés d’accès commençant par J, Y ou Z, car elles sont utilisées pour les onglets contextuels, les touches accélératrices non affectées et les groupes contextuels.
- ![capture d’écran des info-bulles pour les groupes contextuels ](images/cmd-ribbons-image58.png)<br/>**Pour les groupes contextuels :**
  - Utilisez une clé d’accès à deux lettres qui commence par Z.
  - À partir des groupes les plus fréquemment utilisés, affectez la deuxième lettre de clé d’accès à la première lettre de l’étiquette.
  - Pour tous les autres groupes, choisissez une consonne distinctive ou une voyelle dans l’étiquette.

Pour obtenir des instructions sur les touches de raccourci, consultez [clavier](inter-keyboard.md).

### <a name="application-buttons"></a>Boutons de l’application

- **Utilisez un bouton d’application pour présenter un menu de commandes qui impliquent d’effectuer une opération sur ou avec un fichier.** Les exemples incluent des commandes qui se trouvent traditionnellement dans le menu fichier pour créer, ouvrir et enregistrer des fichiers, imprimer et envoyer et publier des documents.
- **Fournissez toujours un bouton d’application lors de l’utilisation d’un ruban.** Si le programme n’utilise pas de fichiers, utilisez le bouton application pour accéder aux options du programme et à la commande quitter. Les boutons d’application affichent toujours un menu de commande qui ne sont jamais décoratifs.
- **Utilisez les commandes de menu d’application standard suivantes, le cas échéant :**
  - Nouveau  
  - Ouvrir  
  - Enregistrer  
  - Enregistrer sous...
  - Imprimer...
  - Impression rapide  
  - Aperçu avant impression  
  - Fermer  
  - Options  
  - Quitter  
  
- **Réservez des commandes qui appartiennent au menu application uniquement pour ce menu.** Ne les placez pas de façon redondante dans l’un des onglets.
- Pour chaque élément de menu, fournissez :
  - **Étiquette avec le nom de la commande.**
  - **Icône de 32 x 32 pixels.**
  - **Brève description.** Assurez-vous que la description peut être affichée à l’aide de deux lignes de texte au maximum.
- ![capture d’écran de la touche de raccourci de la documentation de l’info-bulle ](images/cmd-ribbons-image59.png)<br/>**Utilisez des info-bulles pour documenter les touches de raccourci.** Contrairement aux menus normaux, les menus de l’application ne documentent pas les touches de raccourci à l’aide d’étiquettes.

### <a name="quick-access-toolbars"></a>Barres d’outils accès rapide

- **Utilisez la barre d’outils accès rapide pour fournir un accès aux commandes fréquemment utilisées.** Les commandes peuvent provenir du bouton d’application ou du ruban.
- **Fournissez toujours une barre d’outils accès rapide lors de l’utilisation d’un ruban.** Procédez ainsi même si le ruban comporte un seul onglet. Cela garantit la cohérence entre les programmes.
- **Préremplissez la barre d’outils accès rapide avec les commandes fréquemment utilisées dans le menu de l’application.** Fournissez Save et Undo si votre programme les prend en charge, et ouvrez et imprimez-les s’ils sont pris en charge et fréquemment utilisés.
- **Pour le menu personnaliser la barre d’outils accès rapide, fournissez jusqu’à 12 des commandes immédiates les plus fréquemment utilisées.** Les commandes immédiates ne nécessitent pas d’entrée supplémentaire avant d’être prises en compte. elles conviennent donc parfaitement à la barre d’outils accès rapide. Bien qu’il peut s’agir de toutes les commandes immédiates, préférez les commandes qui ne sont pas sous l’onglet de démarrage, car les utilisateurs sont plus susceptibles de les choisir.
- **Pour le menu personnaliser la barre d’outils accès rapide, s’il existe une paire de commandes associées, fournissez les deux, quelle que soit la fréquence.** Les paires courantes sont ouvrir/fermer, sauvegarder/transférer et annuler/rétablir.
- **Pour la boîte de dialogue Personnaliser la barre d’outils accès rapide, fournissez un moyen d’ajouter une commande.** Fournissez un filtre de commandes populaires qui affiche les commandes les plus fréquemment utilisées, puis sélectionnez ce filtre par défaut.

### <a name="dialog-box-launchers"></a>Lanceurs de boîte de dialogue

- ![capture d’écran de la boîte de dialogue police et du groupe police ](images/cmd-ribbons-image60.png)<br/>**Fournissez un groupe avec un lanceur de boîte de dialogue s’il existe une boîte de dialogue associée avec des commandes et des paramètres rarement utilisés.** La boîte de dialogue doit contenir toutes les commandes dans le groupe, ainsi que d’autres non un ensemble de commandes complètement différent ou les mêmes commandes que le groupe.
- **N’utilisez pas de lanceur de boîte de dialogue pour exécuter des commandes directement.** Un lanceur de boîte de dialogue doit afficher une boîte de dialogue.
- **N’utilisez pas de lanceur de boîte de dialogue pour accéder aux commandes et aux paramètres fréquemment utilisés.** Comparées aux commandes directement sur le ruban, les commandes et les paramètres de la boîte de dialogue sont relativement indétectables.
- **Faites correspondre le nom de la boîte de dialogue avec le nom du groupe.** Il n’est pas nécessaire qu’il s’agit d’une correspondance exacte, mais les noms doivent être suffisamment semblables pour que les utilisateurs ne soient pas surpris par les résultats.

    **Incorrect :**

    ![capture d’écran de la boîte de dialogue de rappel ](images/cmd-ribbons-image61.png)

    Bien qu’un rappel soit une option de rappel, l’utilisation du lanceur de boîte de dialogue pour définir le son du rappel est inattendue.

- **Affichez uniquement les commandes et les paramètres liés au groupe.** Si la boîte de dialogue affiche d’autres choses, les utilisateurs peuvent conclure que ce chemin d’accès à ces autres commandes et paramètres est le seul chemin d’accès.

    **Incorrect :**

    ![capture d’écran de la boîte de dialogue police ](images/cmd-ribbons-image62.png)

    Dans cet exemple, la boîte de dialogue police affiche les paramètres d’espacement des caractères qui ne sont pas liés à l’onglet associé.

## <a name="labels"></a>Étiquettes

### <a name="tab-labels"></a>Étiquettes d’onglet

- **Étiquetez tous les onglets.**
- Dans la mesure **du possible, utilisez les onglets du ruban standard**.
- **Préférer des étiquettes de mots uniques et concises.** Alors que les étiquettes à plusieurs mots sont acceptables, elles prennent plus d’espace et sont plus difficiles à localiser.
- **Choisissez des noms d’onglet explicites qui décrivent clairement et précisément leur contenu.** Les noms doivent être spécifiques, mais ne sont pas trop spécifiques. Les noms des onglets doivent être suffisamment prévisibles pour que les utilisateurs ne soient pas surpris par leur contenu. Notez que l’onglet de démarrage est nommé de façon générique, car il est utilisé pour les commandes les plus fréquemment utilisées.
- **N’utilisez pas** de noms de groupes tels que « de base » et « avancé ». Ils demandent aux utilisateurs de déterminer si la commande qu’ils recherchent est de base ou avancée.
- **Choisissez des noms de tabulation qui reflètent leur objectif.** Examinez les objectifs ou les tâches associés à l’onglet.
- **Choisissez des noms de tabulation qui sont clairement distincts de tous les autres noms d’onglets.**
- **Utilisez des noms ou des verbes pour les onglets.** Comme les noms d’onglets ne nécessitent pas de formulation parallèle, choisissez la meilleure étiquette, qu’il s’agisse d’un nom ou d’un verbe.
- **N’utilisez pas les gérondifs** (les noms se terminent par « -ING »). Utilisez le verbe à partir duquel le gerund est dérivé à la place. (par exemple, utilisez « dessin » au lieu de « dessin ».)
- **Évitez les noms d’onglets ayant les mêmes lettres initiales, en particulier les onglets adjacents.** Lorsque le ruban est mis à l’échelle, ces noms d’onglets ont le même texte tronqué.
- **Préférer les noms singuliers.** Toutefois, vous pouvez utiliser un nom de pural si le nom singulier est maladroit.
- **Utilisez la mise en majuscules du style titre.**
- **N’utilisez pas de ponctuation finale.**

### <a name="contextual-tab-and-tab-set-labels"></a>Onglets contextuels et étiquettes de jeu d’onglets

- **Terminer les étiquettes de jeu d’onglets contextuelles avec « outils ».** Cela permet d’identifier l’objectif des onglets contextuels.
- Utilisez la mise en majuscules du style titre.
- N’utilisez pas de ponctuation finale.

### <a name="group-labels"></a>Étiquettes de groupe

- **Étiquetez tous les groupes** , sauf si le groupe a une seule commande et que les étiquettes de groupe et de commande seraient identiques.

- **Utilisez le ruban standard groupsWhenever pratique.**
- **Préférer des étiquettes de mots uniques et concises.** Alors que les étiquettes à plusieurs mots sont acceptables, elles prennent plus d’espace et sont plus difficiles à localiser.
- **Choisissez des noms de groupes significatifs qui décrivent clairement et précisément leur contenu.** Les noms doivent être spécifiques, et non génériques.
- **Choisissez des noms de groupes qui reflètent leur objectif.** Tenez compte des objectifs ou des tâches associés aux commandes du groupe.
- **Évitez d’utiliser les gérondifs** (les noms se terminent par « -ING »). Vous pouvez utiliser les gérondifs, toutefois, si l’utilisation du verbe à partir duquel le gerund est dérivé peut prêter à confusion. Par exemple, utilisez « modification » et « vérification » au lieu de « modifier » et « preuve ».
- **N’utilisez pas de noms de groupes qui sont identiques aux noms d’onglets.** L’utilisation du nom de l’onglet sur lequel se trouve le groupe ne fournit aucune information et l’utilisation du nom d’un autre onglet est confuse.
- **Préférer les noms singuliers.** Toutefois, vous pouvez utiliser un nom de pural si le nom singulier est maladroit. 
- **Utilisez les majuscules comme pour les phrases.**
- **N’utilisez pas de ponctuation finale.**

### <a name="command-labels"></a>Étiquettes de commande

- **Étiquetez toutes les commandes.** L’utilisation d’étiquettes de texte explicites permet aux utilisateurs de rechercher et de comprendre les commandes. **Exception :** Une commande peut être sans étiquette si son icône est extrêmement connue et que l’espace est à un niveau Premium. Les commandes sans étiquette sont très probablement sous l’onglet dossier de démarrage. Dans ce cas, affectez sa propriété Name à une étiquette de texte appropriée. Cela permet aux produits de technologie d’assistance tels que les lecteurs d’écran de fournir aux utilisateurs des informations alternatives sur le graphique.
- **Pour les boutons de commande, utilisez une étiquette concise et explicite.** Utilisez un seul mot si possible ; quatre mots maximum.
- **Pour les listes déroulantes, si la liste a toujours une valeur, utilisez la valeur actuelle comme étiquette.**
- ![capture d’écran de l’invite de recherche de carnets d’adresses ](images/cmd-ribbons-image67.png)<br/>Si une [liste déroulante modifiable](/windows/desktop/uxguide/ctrl-drop) n’a pas de valeur, utilisez une [invite](glossary.md).
- **Les listes déroulantes qui ne sont pas explicites ou qui sont rarement utilisées nécessitent une étiquette explicite.** Placez le signe deux-points à la fin de l’étiquette.
- ![capture d’écran de automatiquement après : \[ secondes \] ](images/cmd-ribbons-image69.png)<br. >**pour les zones de texte, utilisez une étiquette explicite.** Placez le signe deux-points à la fin de l’étiquette.
- **Utilisez les majuscules comme pour les phrases.** cela est plus approprié pour le [ton](text-style-tone.md)Windows.
- **Démarrez l’étiquette avec un verbe impératif.** sauf s’il est identique au nom de l’onglet ou du groupe ou à un verbe courant comme Show, Create, INSERT ou format.
- **N’utilisez pas de ponctuation finale.**
- **Pour économiser de l’espace, ne placez pas de ellipses sur les étiquettes de commande du ruban.** Toutefois, les ellipses sont utilisées par les commandes dans le bouton de l’application et les menus déroulants.

### <a name="enhanced-tooltip-labels"></a>Étiquettes d’info-bulle améliorées

- **Utilisez le titre pour fournir le nom de la commande et sa touche de raccourci, le cas échéant.**
- **Pour le titre, n’utilisez pas de ponctuation finale.**
- **Démarrez la description avec un verbe.** Utilisez la description pour aider les utilisateurs à déterminer si une fonctionnalité spécifique est celle qu’ils recherchent. La description doit être formulées pour terminer la phrase « il s’agit de la fonctionnalité à utiliser si vous le souhaitez... ».
- **Conservez la description concise.** Accédez directement au point. Un long texte découragera la lecture.
-   ![capture d’écran du bouton Coller Split et de deux info-bulles ](images/cmd-ribbons-image70.png)<br/>**Pour les boutons partagés, utilisez une info-bulle différente pour expliquer le menu du bouton partagé.**
- **Utilisez une description supplémentaire facultative pour expliquer comment utiliser le contrôle.** Ce texte peut inclure des informations sur l’état du contrôle (notamment la raison pour laquelle il est désactivé) si le contrôle lui-même n’indique pas d’État. Laissez ce texte concis et utilisez une rubrique d’aide pour obtenir des explications plus détaillées.
- ![capture d’écran de l’info-bulle avec un graphique et ](images/cmd-ribbons-image71.png)**du texte pour obtenir une description et une description supplémentaire, utilisez des phrases complètes avec une ponctuation finale.**
- Utilisez les majuscules comme pour les phrases.

### <a name="application-button-labels"></a>Étiquettes de bouton d’application

- [capture d’écran de l’option d’impression rapide sélectionnée ](images/cmd-ribbons-image72.png)<br/>**Utilisez « Quick » pour indiquer une version immédiate d’une commande.**

- **Utilisez des points de suspension pour indiquer qu’une commande requiert plus d’informations.**
- **Utilisez les majuscules comme pour les phrases.**

## <a name="documentation"></a>Documentation

Quand vous faites référence à des rubans :

- Reportez-vous au ruban et à ses composants en tant que ruban, onglets, groupes et contrôles. Ces termes ne sont pas écrits en majuscules.
- Reportez-vous au bouton rond comme bouton d’application et au menu qu’il contient comme menu d’application.
- Reportez-vous à la barre d’outils pour accéder à la barre d’outils accès rapide.
- Reportez-vous aux onglets en fonction de leurs étiquettes et de l’onglet mot. Utilisez le texte exact de l’étiquette, y compris sa mise en majuscules.
- Reportez-vous aux commandes par leurs étiquettes. Reportez-vous aux commandes sans étiquette par leurs noms d’info-bulle. Utilisez le texte exact de l’étiquette, y compris sa mise en majuscules, mais n’incluez pas les points de suspension. N’incluez pas le bouton ou la commande Word.
- Pour décrire l’interaction de l’utilisateur, cliquez sur pour les onglets et les contrôles. Utilisez entrée pour les listes déroulantes modifiables. N’utilisez pas Choose, SELECT ou Pick.
- Reportez-vous aux éléments non disponibles comme indisponibles, non estompés, désactivés ou grisés. Dans documentation de programmation, utilisez désactivé.
- Dans la mesure du possible, mettez en forme les étiquettes à l’aide du texte gras. Dans le cas contraire, placez les étiquettes entre guillemets uniquement si nécessaire pour éviter toute confusion.

Exemples :

- Dans l’onglet dossier de **démarrage** , cliquez sur **Collage spécial**.
- Dans l’onglet dossier de **démarrage** , dans la zone **police** , entrez « Segoe UI ».
- Sous l’onglet **révision** , cliquez sur **afficher les balises**, puis sur **réviseurs**.
- Sous l’onglet **format** , dans **Outils d’image**, cliquez sur **compresser les images**.
