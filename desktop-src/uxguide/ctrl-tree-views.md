---
title: Arborescences
description: Avec une arborescence, les utilisateurs peuvent afficher et interagir avec une collection hiérarchique d’objets, en utilisant une sélection unique ou une sélection multiple.
ms.assetid: f0206485-e028-41d8-9be2-5d59f0a0b677
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: ade51b421350dc90bf72e2ff1a683bf1d352f7c1
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524493"
---
# <a name="tree-views"></a>Arborescences

> [!NOTE]
> Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Avec une arborescence, les utilisateurs peuvent afficher et interagir avec une collection hiérarchique d’objets, en utilisant une sélection unique ou une sélection multiple.

Dans une arborescence, les objets qui contiennent des données sont appelés nœuds terminaux et les objets qui contiennent d’autres objets sont appelés des nœuds conteneurs. Un nœud conteneur unique de premier niveau est appelé le nœud racine. Les utilisateurs peuvent développer et réduire les nœuds de conteneur en cliquant sur les boutons plus et moins Expander.

![capture d’écran de l’arborescence de l’Explorateur Windows ](images/ctrl-tree-views-image1.png)

Arborescence classique.

> [!Note]  
> Les instructions relatives à la [disposition](vis-layout.md) et aux [menus](cmd-menus.md) sont présentées dans des articles distincts.

 

## <a name="is-this-the-right-control"></a>Est-ce le contrôle approprié ?

**Le fait de disposer de données hiérarchiques ne signifie pas que vous devez utiliser une arborescence.** Très souvent, un [affichage de liste](ctrl-list-views.md) est un choix plus simple, mais plus puissant. Affichages de liste :

-   Prendre en charge plusieurs vues différentes.
-   Prendre en charge le tri des données par toutes les colonnes en mode Détails.
-   Prise en charge de l’Organisation des données en groupes, formant une hiérarchie à deux niveaux.

**Pour utiliser un mode liste, vous pouvez aplatir les informations hiérarchiques à l’aide des techniques suivantes :**

-   Supprimez le nœud racine, le cas échéant, car il n’est souvent pas nécessaire.
-   Utilisez les groupes de mode liste, les onglets, les [listes déroulantes](/windows/desktop/uxguide/ctrl-drop)ou [les en-têtes extensibles](glossary.md) pour remplacer les conteneurs de niveau supérieur.

    ![capture d’écran des groupes de vue de liste contenant des listes ](images/ctrl-tree-views-image2.png)

    Dans cet exemple, les groupes de vue de liste sont utilisés pour les conteneurs de niveau supérieur.

    ![capture d’écran des onglets utilisés pour les conteneurs de niveau supérieur ](images/ctrl-tree-views-image3.png)

    Dans cet exemple, les onglets sont utilisés pour les conteneurs de niveau supérieur

    ![capture d’écran de la liste déroulante utilisée en tant que conteneur ](images/ctrl-tree-views-image4.png)

    Dans cet exemple, une liste déroulante est utilisée pour les conteneurs de niveau supérieur.

-   Si un contrôle associé affiche le contenu du conteneur sélectionné, ce contrôle peut afficher des niveaux inférieurs de la hiérarchie.

    ![capture d’écran du volet table des matières ](images/ctrl-tree-views-image5.png)

    Dans cet exemple, les conteneurs de bas niveau sont affichés dans la fenêtre de document.

**Vous devez utiliser une arborescence si vous devez afficher une hiérarchie de plus de deux niveaux (à l’exclusion du nœud racine).**

Pour déterminer si une arborescence est le bon contrôle, posez-vous les questions suivantes :

-   **Les données sont-elles hiérarchiques ?** Si ce n’est pas le cas, utilisez un autre contrôle.
-   **La hiérarchie a-t-elle au moins trois niveaux (à l’exclusion de la racine) ?** Si ce n’est pas le cas, envisagez des alternatives telles que les groupes de mode liste, les onglets, les listes déroulantes ou les en-têtes extensibles.
-   **Les éléments ont-ils des données auxiliaires ?** Dans ce cas, envisagez d’utiliser une vue liste en mode Détails pour tirer pleinement parti des données auxiliaires.
-   **Les données de niveau inférieur sont-elles liées à des sous-tâches indépendantes ?** Dans ce cas, envisagez d’afficher les informations dans un contrôle associé ou dans une fenêtre distincte (affichée à l’aide de [boutons de commande](ctrl-command-buttons.md) ou de [liens](ctrl-command-links.md)).
-   **Les utilisateurs cibles sont-ils avancés ?** Les utilisateurs avancés sont plus compétents pour utiliser des arborescences. Si votre application est destinée aux utilisateurs débutants, évitez d’utiliser des arborescences.
-   **Les éléments ont-ils une catégorisation unique, naturelle et hiérarchique familière à la plupart des utilisateurs ?** Si c’est le cas, les données sont idéales pour une arborescence. Si vous avez besoin de plusieurs vues ou tris, utilisez plutôt un mode liste.
-   **Les utilisateurs doivent-ils voir les données de niveau inférieur dans certains scénarios, mais pas dans tous, ou bien tout le temps ?** Si c’est le cas, les données sont idéales pour une arborescence.

> [!Note]  
> Parfois, un contrôle ressemblant à une arborescence est implémenté à l’aide d’un mode liste. Dans ce cas, appliquez les instructions en fonction de l’utilisation, et non de l’implémentation.

 

## <a name="design-concepts"></a>Principes de conception

Les arborescences sont conçues pour organiser les données et faciliter leur recherche, mais il est difficile de rendre les données dans une arborescence facilement détectables. Tenez compte des principes suivants lorsque vous décidez des arborescences et de leur organisation.

### <a name="predictability-and-discoverability"></a>Prévisibilité et détectabilité

**Une arborescence est basée sur les relations entre les objets.** Les arborescences fonctionnent mieux lorsque les objets forment une relation claire, bien connue et mutuellement exclusive dans laquelle chaque objet est mappé à un conteneur unique et facile à déterminer.

**Un problème important est qu’un objet peut apparaître dans des nœuds différents.** Par exemple, où les utilisateurs devraient-ils trouver un périphérique matériel qui lit de la musique, possède-t-il un disque dur volumineux et utilise un port USB ? Peut-être dans l’un des différents nœuds de conteneur, tels que le multimédia, le stockage, l’USB et éventuellement dans les ressources matérielles. Une solution consiste à placer chaque objet sous le conteneur unique le plus approprié, indépendamment des circonstances. une autre approche consiste à placer chaque objet sous tous les conteneurs qui s’appliquent. La première favorise une hiérarchie simple, propre, et la dernière favorise la détectabilité, chacune présentant des avantages et des problèmes potentiels.

**Les utilisateurs ne comprennent peut-être pas complètement la disposition de l’arborescence, mais ils constituent un modèle mental des relations après l’interaction avec l’arbre pendant un certain temps.** Si ce modèle mental est incorrect, cela provoque une confusion. Supposons, par exemple, qu’un lecteur de musique se trouve dans les conteneurs multimédia, de stockage et USB. Cette organisation améliore la détectabilité. Si un utilisateur trouve pour la première fois l’appareil dans multimédia, il peut conclure que tous les appareils tels que les lecteurs musicaux apparaissent dans le conteneur multimédia. L’utilisateur s’attend à ce que des appareils similaires, tels que des appareils photo numériques, s’affichent dans le conteneur multimédia et deviendront confus si ce n’est pas le cas.

**La difficulté lors de la conception d’une arborescence consiste à équilibrer la détectabilité avec un modèle utilisateur prévisible qui minimise la confusion.**

### <a name="breadth-vs-depth"></a>Largeur et profondeur

Les études de convivialité ont montré que **les utilisateurs sont plus performants dans la recherche d’objets dans une arborescence qui est large que dans une arborescence. par** conséquent, lors de la conception d’une arborescence, vous devez préférer élargir la profondeur. Dans l’idéal, une arborescence ne doit pas comporter plus de quatre niveaux (sans compter le nœud racine) et les objets les plus fréquemment utilisés doivent apparaître dans les deux premiers niveaux.

### <a name="other-principles"></a>Autres principes

-   Quand les utilisateurs trouvent ce qu’ils recherchent, ils cessent de regarder. Ils ne cherchent pas à déterminer où un objet peut être trouvé parce qu’ils n’ont pas besoin de. Ces utilisateurs peuvent supposer que le premier chemin qu’ils trouvent est le seul chemin.
-   Les utilisateurs éprouvent des difficultés à trouver des objets dans des arborescences volumineuses et complexes. Les utilisateurs n’effectuent pas de recherche manuelle exhaustive pour trouver des objets dans ces arbres. ils s’arrêtent une fois qu’ils pensent qu’ils ont fait un effort raisonnable. Par conséquent, les arborescences volumineuses et complexes doivent être complétées par d’autres méthodes d’accès, telles que la recherche de mot, un index ou un filtrage.
-   Certains programmes permettent aux utilisateurs de créer leurs propres arborescences. Bien que ces arborescences auto-conçues puissent être alignées avec le modèle mental d’un utilisateur, elles sont souvent créées de manière irrégulière et mal gérée. Par exemple, si un système de fichiers, un programme de messagerie électronique et une liste de favoris stockent généralement des types d’informations similaires, les utilisateurs se déplacent rarement de la même façon.

**Si vous n’avez qu’une seule chose...**

Évaluez soigneusement les avantages et les inconvénients de l’utilisation des arborescences. Une organisation hiérarchique des données ne signifie pas que vous devez utiliser une arborescence.

## <a name="usage-patterns"></a>Modèles d’usage

Les arborescences présentent plusieurs modèles d’utilisation :



| Usage                           |    Exemple                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Arborescences avec des nœuds de conteneur uniquement**<br/> les utilisateurs peuvent afficher et interagir avec un conteneur à la fois. <br/>                        | En règle générale, ces vues d’arborescence ont un contrôle associé qui affiche le contenu du conteneur sélectionné, afin que les utilisateurs puissent interagir avec un seul conteneur à la fois. <br/> ![capture d’écran du volet conteneur et du volet contenu ](images/ctrl-tree-views-image6.png)<br/> Dans cet exemple, l’arborescence contient uniquement des nœuds conteneurs. Le contenu du nœud sélectionné s’affiche dans le contrôle d’affichage de liste associé.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Arborescences avec des nœuds conteneurs et terminaux**<br/> les utilisateurs peuvent afficher et interagir avec des conteneurs et des feuilles.<br/>                       | En règle générale, ces vues d’arborescence ont un contrôle associé qui affiche le contenu du conteneur ou feuille sélectionné. le fait de permettre aux utilisateurs d’interagir avec les feuilles de route est souvent nécessaire pour prendre en charge la sélection multiple. <br/> ![capture d’écran du volet d’arborescence et du volet de contenu ](images/ctrl-tree-views-image7.png)<br/> dans cet exemple, l’arborescence contient à la fois des nœuds conteneur et feuille. étant donné que la sélection multiple est prise en charge, le contenu des éléments ouverts est affiché à l’aide d' [onglets](ctrl-tabs.md) dans le contrôle associé.<br/> l’arborescence peut également avoir une liste organisée, où les conteneurs sont des en-têtes et les feuilles sont des options. <br/> ![capture d’écran de l’arborescence avec les en-têtes et les options ](images/ctrl-tree-views-image8.png)<br/> Dans cet exemple, l’arborescence laisse les options et les conteneurs sont des catégories d’options.<br/> |
| **Affichages de l’arborescence de cases à cocher**<br/> les utilisateurs peuvent sélectionner n’importe quel nombre d’éléments, y compris aucun.<br/>                                             | Les cases à cocher indiquent clairement que plusieurs sélections sont possibles. Utilisez ce modèle d’arborescence lorsque la sélection multiple est essentielle ou couramment utilisée. <br/> ![capture d’écran de l’arborescence avec des cases à cocher ](images/ctrl-tree-views-image9.png)<br/> Dans cet exemple, une arborescence de cases à cocher permet de sélectionner les fonctionnalités à activer ou à désactiver.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Générateurs d’arborescence**<br/> les utilisateurs peuvent créer une arborescence en ajoutant un conteneur ou une feuille à la fois et en définissant éventuellement la commande.<br/> | De nombreuses arborescences peuvent être créées ou modifiées par les utilisateurs. certaines arborescences sont créées en utilisant des menus contextuels et des opérations de glisser-déplacer (comme les dossiers dans l’Explorateur Windows), tandis que d’autres arborescences sont créées à l’aide d’une boîte de dialogue spécialisée (telle que la liste des favoris dans Windows Internet Explorer). <br/> ![capture d’écran de la boîte de dialogue favoris ](images/ctrl-tree-views-image10.png)<br/> Dans cet exemple à partir d’Internet Explorer, les utilisateurs peuvent créer leur propre liste de favoris à l’aide d’une boîte de dialogue.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| **Arborescences avec des méthodes d’accès alternatives**<br/> les utilisateurs peuvent trouver des objets de manière différente de l’utilisation d’une arborescence hiérarchique.<br/>        | Comme mentionné précédemment, les utilisateurs ont des difficultés à trouver des objets dans des arborescences volumineuses et complexes, de sorte que ces arbres doivent être complétés par d’autres méthodes d’accès, telles qu’une recherche de mots, un index ou un filtrage. <br/> ![capture d’écran des onglets sommaire, index et favoris ](images/ctrl-tree-views-image11.png)<br/> dans cet exemple, les utilisateurs peuvent également accéder aux informations à l’aide d’une table des matières, d’un index et de favoris. pour certains utilisateurs, les onglets index et recherche peuvent être plus utiles que l’onglet Sommaire.<br/> ![capture d’écran du menu Démarrer et de la zone de recherche de Windows ](images/ctrl-tree-views-image12.png)<br/> Dans cet exemple, le menu Démarrer de Windows permet également aux utilisateurs d’accéder aux programmes, fichiers et pages Web en tapant une partie du nom dans la zone de recherche.<br/>                                                                                                             |



 

## <a name="guidelines"></a>Consignes

### <a name="presentation"></a>Présentation

-   **Dans un conteneur, triez les éléments dans un ordre logique.** Triez les noms dans l’ordre alphabétique, les nombres dans l’ordre numérique et les dates dans l’ordre chronologique.
-   **Utilisez l’attribut toujours afficher la sélection** afin que les utilisateurs puissent facilement déterminer l’élément sélectionné, même si le contrôle n’a pas le focus d’entrée.
-   **Si l’arborescence agit comme une table des matières, utilisez l’attribut de développement unique pour simplifier la gestion de l’arborescence.** De cette façon, seule la partie pertinente de l’arborescence est développée.
-   **Évitez de présenter des arborescences vides.** Si un utilisateur crée une arborescence, initialisez l’arborescence avec des instructions ou des exemples d’éléments dont les utilisateurs peuvent avoir besoin.

    ![capture d’écran de la liste des favoris d’Internet Explorer ](images/ctrl-tree-views-image13.png)

    Dans cet exemple, la liste est initialement présentée avec des exemples.

-   **Ne rendez pas les nœuds conteneurs réductibles si les utilisateurs n’ont aucune raison de les réduire.** Cela ajoute une complexité inutile.
-   **Si les performances de chargement sont un problème, Affichez uniquement les conteneurs de premier et de deuxième niveau de l’arborescence par défaut.** Vous pouvez ensuite charger des données supplémentaires à la demande lorsqu’un utilisateur développe des branches dans l’arborescence.
-   **Si les utilisateurs développent ou réduisent un conteneur, rendez-le persistant afin qu’il entre en vigueur lors de la prochaine affichage de l’arborescence**, à moins que les utilisateurs ne soient susceptibles de commencer à utiliser l’État par défaut. La persistance doit être effectuée en fonction de l’arborescence, par utilisateur.
-   **Si des conteneurs de haut niveau ont un contenu similaire, envisagez d’utiliser des indices visuels pour les différencier.**

    **Incorrect :**

    ![capture d’écran des éléments Outlook avec différentes icônes ](images/ctrl-tree-views-image14.png)

    Dans cet exemple, les dossiers boîte aux lettres et Archive ont un contenu similaire. Une fois les arborescences développées, il est très difficile pour les utilisateurs de savoir où ils se trouvent dans l’arborescence, ce qui se traduit par une confusion. L’utilisation d’icônes légèrement différentes dans les différentes sections peut résoudre ce problème.

-   **Reprenons la connexion des lignes.** Bien que ces lignes indiquent clairement les relations entre les nœuds de conteneur et les nœuds terminaux, elles ajoutent un encombrement visuel sans contribuer de manière significative à la compréhension. Plus précisément, ils ne peuvent pas être utiles lorsque les nœuds sont proches les uns des autres, pas plus qu’ils n’aident quand les nœuds sont tellement éloignés que le défilement est nécessaire.

    **Correct :**

    ![capture d’écran de l’arborescence avec lignes de connexion ](images/ctrl-tree-views-image15.png)

    **Conseillé**

    ![capture d’écran de l’arborescence sans lignes de connexion ](images/ctrl-tree-views-image16.png)

    Les lignes qui se connectent peu pour faciliter la compréhension.

### <a name="interaction"></a>Interaction

-   **Envisagez de fournir un comportement de double-clic.** Un double-clic doit avoir le même effet que la sélection d’un élément et l’exécution de sa commande par défaut.
-   **Effectuez un double-clic sur le comportement redondant.** Il doit toujours y avoir un bouton de commande ou une commande de menu contextuel qui a le même effet.
-   Si un élément nécessite une explication supplémentaire, **fournissez l’explication dans une info-bulle**.

    ![capture d’écran des favoris avec une info-bulle pour un élément ](images/ctrl-tree-views-image17.png)

    Dans cet exemple, une info-bulle fournit des informations supplémentaires.

-   **Fournissez des menus contextuels des commandes appropriées.** Ces commandes incluent couper, copier, coller, supprimer ou supprimer, renommer et propriétés.
-   **Lors de la désactivation d’une arborescence, désactivez également les étiquettes et les boutons de commande associés.**

### <a name="tree-organization"></a>Organisation de l’arborescence

-   **Utilisez une structure hiérarchique naturelle familière à la plupart des utilisateurs.**
-   **Si vous ne pouvez pas utiliser une telle structure, essayez d’équilibrer la détectabilité avec un modèle utilisateur prévisible qui minimise la confusion.**
-   **Pour améliorer en toute sécurité la détectabilité, placez un élément dans plusieurs conteneurs lorsque :**
    -   L’élément n’est pas lié à d’autres éléments similaires (par conséquent, les utilisateurs ne sont pas confondus par des associations incorrectes).
    -   Il n’y a que quelques éléments situés de manière redondante (l’arborescence n’est donc pas encombrée).
-   **Utilisez la structure hiérarchique la plus simple qui fonctionne bien.** Pour cela, procédez de la façon suivante :
    -   Placez les objets les plus fréquemment utilisés dans les deux premiers niveaux de l’arborescence (sans compter le nœud racine) et placez les objets les moins fréquemment sollicités plus loin dans la hiérarchie.
    -   Éliminez les conteneurs non nécessaires ou combinez des conteneurs de niveau intermédiaire redondants.
-   **Préférez une profondeur supérieure.** Dans l’idéal, une arborescence ne doit pas comporter plus de quatre niveaux et les objets les plus fréquemment utilisés doivent apparaître dans les deux premiers niveaux.
-   **Déterminez si vous avez vraiment besoin d’un nœud racine.** Fournissez un nœud racine si les utilisateurs ont besoin de pouvoir exécuter des commandes sur l’ensemble de l’arborescence (éventuellement à l’aide d’un menu contextuel sur le nœud racine). Dans le cas contraire, l’arborescence est plus simple et plus facile à utiliser sans elle.
-   **Si l’arborescence possède des méthodes d’accès alternatives, telles qu’une recherche de mots ou un index, optimisez l’arborescence pour la navigation en vous concentrant sur le contenu le plus utile.** Avec les autres méthodes d’accès, le contenu de l’arborescence n’a pas besoin d’être complet. La simplification de l’arborescence permet aux utilisateurs de trouver plus facilement le contenu le plus utile.

### <a name="check-box-tree-views"></a>Affichages de l’arborescence de cases à cocher

-   **Affichez le nombre d’éléments sélectionnés sous la liste**, en particulier si les utilisateurs sont susceptibles de sélectionner plusieurs éléments. Ce feedback aide les utilisateurs à confirmer que leur sélection est correcte.

    ![capture d’écran du nombre d’éléments sélectionnés ](images/ctrl-tree-views-image18.png)

    Dans cet exemple, le nombre d’éléments sélectionnés est affiché sous l’arborescence. Il est clair que deux éléments ne sont pas sélectionnés.

-   S’il y a peut-être un grand nombre d’éléments et que vous sélectionnez ou désactivez tous ces éléments, vous pouvez ajouter des boutons de commande Sélectionner tout et effacer tout.
-   **Utilisez les cases à cocher à état mixte pour indiquer la sélection partielle des éléments d’un conteneur.**

    **Correct :**

    ![capture d’écran de la fenêtre avec des cases à cocher à l’État mixte ](images/ctrl-tree-views-image19.png)

    Dans cet exemple, les cases à cocher à l’État mixte sont utilisées pour indiquer une sélection partielle.

## <a name="recommended-sizing-and-spacing"></a>Dimensionnement et espacement recommandés

![capture d’écran de l’espacement et du dimensionnement de l’arborescence ](images/ctrl-tree-views-image20.png)

Dimensionnement et espacement recommandés pour les contrôles d’arborescence.

-   **Choisissez une largeur d’arborescence qui évite le besoin de défilement horizontal** pour la plupart des éléments lorsque l’arborescence est entièrement développée.
-   **Incluez 30 pour cent supplémentaires pour prendre en charge la localisation.**
-   **Choisissez une hauteur d’arborescence qui élimine le défilement vertical inutile.** Envisagez une vue d’arborescence légèrement plus longue (ou encore plus si l’espace disponible est suffisant) si cela réduit la nécessité d’une barre de défilement verticale.

    **Incorrect :**

    ![capture d’écran du contrôle d’arborescence courte et étroite ](images/ctrl-tree-views-image21.png)

    Dans cet exemple, le fait de rendre l’arborescence légèrement plus larges et plus longue entraînerait l’élimination des barres de défilement dans la plupart des cas. Dans cette arborescence particulière, un seul conteneur peut être ouvert à la fois.

-   **Si les utilisateurs tirent parti de la taille de l’arborescence, rendez l’arborescence et sa fenêtre parente redimensionnable.** Cela permet aux utilisateurs d’ajuster la taille de l’arborescence en fonction des besoins.

## <a name="labels"></a>Étiquettes

### <a name="control-labels"></a>Étiquettes de contrôle

-   Toutes les arborescences ont besoin d’étiquettes. Écrivez l’étiquette en tant que mot ou expression, pas en tant que phrase, en terminant par un signe deux-points et en utilisant du [texte statique](glossary.md).
-   Attribuez une clé d’accès unique. Pour connaître les instructions d’affectation, consultez [clavier](inter-keyboard.md).
-   Utilisez les majuscules comme pour les phrases.
-   Placez l’étiquette au-dessus du contrôle, puis alignez l’étiquette sur le bord gauche du contrôle.
-   Pour les vues d’arborescence à sélection multiple, écrivez l’étiquette pour qu’il soit clair que plusieurs sélections sont possibles. Les étiquettes de vue d’arborescence de case à cocher peuvent être moins explicites.

    **Incorrect :**

    ![capture d’écran de l’arborescence avec l’étiquette composants ](images/ctrl-tree-views-image22.png)

    Dans cet exemple, l’étiquette ne fournit aucune information sur la sélection multiple.

    **Conseillé**

    ![capture d’écran de l’arborescence avec l’étiquette « une ou plusieurs » ](images/ctrl-tree-views-image23.png)

    Dans cet exemple, l’étiquette indique clairement que plusieurs sélections sont possibles.

    **Meilleures**

    ![capture d’écran de l’arborescence avec des cases à cocher ](images/ctrl-tree-views-image24.png)

    Dans cet exemple, les cases à cocher indiquent clairement que plusieurs sélections sont possibles, de sorte que l’étiquette n’a pas besoin d’être explicite.

### <a name="data-text"></a>Texte de données

-   Utilisez les majuscules comme pour les phrases.

### <a name="instructional-text"></a>Texte d’instructions

-   Si vous devez ajouter du texte d’instructions sur une arborescence, ajoutez-la au-dessus de l’étiquette. Utilisez des phrases complètes avec la ponctuation finale.
-   Utilisez les majuscules comme pour les phrases.
-   Les explications supplémentaires qui sont utiles, mais pas nécessaires, doivent être courtes. Placez ces informations entre parenthèses entre l’étiquette et le signe deux-points, après l’instruction principale si elle est utilisée à la place d’une étiquette ou sous le contrôle.

    ![capture d’écran de l’explication sous l’arborescence ](images/ctrl-tree-views-image8.png)

    Dans cet exemple, l’explication supplémentaire est sous le contrôle.

## <a name="documentation"></a>Documentation

Lorsque vous faites référence aux arborescences :

-   Utilisez le texte exact de l’étiquette, y compris sa mise en majuscules, mais n’incluez pas le trait de soulignement ou le signe deux-points. Incluez la liste de mots ou la liste hiérarchique si le contexte doit faire une distinction à partir de listes standard.
-   Pour les éléments d’arborescence, utilisez le texte exact de l’élément, y compris sa mise en majuscules.
-   Reportez-vous aux arborescences sous forme d’arborescences uniquement dans la programmation et dans d’autres documents techniques. Partout ailleurs, utilisez liste ou liste hiérarchique car le terme arborescence est confus pour la plupart des utilisateurs.
-   Pour décrire l’interaction avec l’utilisateur, utilisez SELECT pour les données, et développez et réduisez pour les boutons plus et moins.
-   Lorsque cela est possible, mettez en forme l’étiquette et les éléments d’arborescence à l’aide de texte en gras. Sinon, placez l’étiquette et les éléments entre guillemets uniquement si nécessaire pour éviter toute confusion.

Exemple : dans la liste **contenu** , sélectionnez **conception de l’interface utilisateur**.

Lorsque vous faites référence à des cases à cocher dans une arborescence :

-   Utilisez le texte d’étiquette exact, y compris sa mise en majuscules, et incluez la case à cocher mots. N’incluez pas le trait de soulignement de clé d’accès.
-   Pour décrire l’interaction de l’utilisateur, utilisez sélectionner et effacer.
-   Dans la mesure du possible, mettez en forme l’étiquette à l’aide de texte en gras. Sinon, placez l’étiquette entre guillemets uniquement si nécessaire pour éviter toute confusion.

Exemple : dans la liste **éléments à sauvegarder** , activez la case à cocher **Mes documents** .

