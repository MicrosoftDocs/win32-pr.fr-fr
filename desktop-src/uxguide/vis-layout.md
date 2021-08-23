---
title: Layout
description: La disposition est le dimensionnement, l’espacement et le positionnement du contenu dans une fenêtre ou une page.
ms.assetid: 39cd896f-d3cc-4768-a20c-a7f598da7136
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 2bd705346f979a44cc2a8c7917f81b9e918ce5277893b5a377ab1ede4b945bb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119816901"
---
# <a name="layout"></a>Layout

> [!NOTE]
> ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

La disposition est le dimensionnement, l’espacement et le positionnement du contenu dans une fenêtre ou une page. Une disposition efficace est essentielle pour aider les utilisateurs à trouver rapidement ce qu’ils recherchent, et pour rendre l’apparence visuellement attrayante. Une mise en page efficace peut faire la différence entre les conceptions que les utilisateurs comprennent immédiatement et celles qui laissent les utilisateurs se sentir submergés.

**Remarque :** Les instructions relatives à la [gestion des fenêtres](win-window-mgt.md) sont présentées dans un article distinct. Le dimensionnement et l’espacement de contrôle spécifiques recommandés sont présentés dans leurs articles d’indications respectifs.

## <a name="design-concepts"></a>Principes de conception

### <a name="visual-hierarchy"></a>Hiérarchie visuelle

Une fenêtre ou une page a une hiérarchie visuelle claire quand son apparence indique la relation et la priorité de ses éléments. Sans hiérarchie visuelle, les utilisateurs devraient déterminer ces relations et priorités elles-mêmes.

La hiérarchie visuelle est obtenue par skillfully en associant les attributs suivants :

-   **Spécialisés.** La disposition indique l’emplacement des utilisateurs.
-   **Flow.** L’œil passe en douceur et naturellement par un chemin clair sur la surface, en recherchant des éléments d’interface utilisateur dans l’ordre approprié pour leur utilisation.
-   **Regroupement.** Les éléments d’interface utilisateur liés de manière logique ont une relation visuelle claire. Les éléments associés sont regroupés. les éléments non liés sont distincts.
-   **Privilégié.** Les éléments d’interface utilisateur sont mis en évidence en fonction de leur importance relative.
-   **Repère.** Les éléments d’interface utilisateur ont un positionnement coordonné. ils sont donc faciles à analyser et à s’afficher de manière ordonnée.

En outre, la disposition effective possède les attributs suivants :

-   **Indépendance des appareils.** La disposition s’affiche comme prévu, quelle que soit la police ou la taille de la police, les points par pouce (dpi), l’affichage ou l’adaptateur graphique.
-   **Facile à analyser.** Les utilisateurs peuvent trouver le contenu qu’ils recherchent d’un coup d’œil.
-   **Performance.** Les éléments d’interface utilisateur qui sont volumineux doivent être volumineux et les éléments de petite taille fonctionnent bien petit.
-   **Resizability.** Si utile, une fenêtre est redimensionnable et sa disposition de contenu est effective, quelle que soit la taille de la surface.
-   **Équilibrée.** Le contenu apparaît uniformément réparti sur l’aire.
-   **Simplicité visuelle.** Le sentiment qu’une disposition n’est pas plus compliquée qu’elle ne doit l’être. Les utilisateurs ne semblent pas submergés par l’apparence de la disposition.
-   **Cohérence.** Les fenêtres ou pages similaires utilisent une mise en page similaire, de sorte que les utilisateurs se sentent toujours orientés.

Si le dimensionnement, l’espacement et le placement sont des concepts simples, le défi avec la disposition est de parvenir à un mélange correct de ces attributs.

dans Windows, la disposition est communiquée à l’aide de métriques indépendantes des appareils, telles que les unités de boîte de dialogue (dlu) et les pixels relatifs.

### <a name="a-design-model-for-reading"></a>Modèle de conception pour la lecture

**Les utilisateurs choisissent ce qu’ils lisent à l’apparence et à l’organisation du contenu.** Pour créer une disposition efficace, vous devez comprendre ce que les utilisateurs ont tendance à lire et pourquoi.

Vous pouvez prendre des décisions en matière de disposition à l’aide de ce modèle de conception pour la lecture :

-   Les personnes lisent dans un ordre de gauche à droite et de haut en bas (dans les cultures occidentales).
-   Il existe deux modes de lecture : la lecture et l’analyse immersifs. L’objectif de la lecture immersive est la compréhension.

    ![figure de la flèche rouge dans le modèle de lecture en zigzag ](images/vis-layout-image1.png)

    Ce diagramme modélise la lecture immersive.

    En revanche, l’objectif de l’analyse est de trouver des éléments. Le chemin d’accès d’analyse global se présente comme suit :

    ![figure de la flèche rouge dans le modèle de lecture en diagonale ](images/vis-layout-image2.png)

    Ce diagramme modélise l’analyse.

    ![figure de la flèche rouge dans un modèle en bas et en arc ](images/vis-layout-image3.png)

    Si du texte s’exécute le long du bord gauche d’une page, les utilisateurs analysent d’abord le bord gauche.

-   Lors de l’utilisation de logiciels, les utilisateurs ne sont pas immergés dans l’interface utilisateur, mais dans leur travail. Par conséquent, les utilisateurs ne lisent généralement pas le texte de l’interface utilisateur qu’ils analysent. Ils lisent alors les bits de texte de façon complète uniquement lorsqu’ils pensent qu’ils en ont besoin.
-   Les utilisateurs ont tendance à ignorer les volets de navigation sur le côté gauche ou droit d’une page. Les utilisateurs reconnaissent qu’ils sont là, mais examinent les volets de navigation uniquement lorsqu’ils souhaitent naviguer.
-   Les utilisateurs ont tendance à ignorer les grands blocs de texte non mis en forme sans les lire du tout.

    ![figure de texte avec des flèches indiquant le texte à analyser ](images/vis-layout-image4.png)

    Les utilisateurs ont tendance à ignorer les grands blocs de texte et les volets de navigation lors de l’analyse.

-   Tous les éléments sont égaux, les utilisateurs regardent d’abord dans l’angle supérieur gauche d’une fenêtre, numérisent sur la page et terminent leur analyse dans le coin inférieur droit. Ils ont tendance à ignorer l’angle inférieur gauche.

    ![figure de la page et de l’angle supérieur gauche à la flèche inférieure droite ](images/vis-layout-image5.png)

    Comme tous les éléments sont égaux, les utilisateurs lisent ces nombres dans l’ordre suivant : 1, 2, 4 et 3.

-   Mais dans l’interface utilisateur interactive, les éléments d’interface utilisateur ne sont pas tous identiques. Les utilisateurs ont tendance à examiner les contrôles interactifs, en particulier les contrôles dans le coin supérieur gauche et le centre de la fenêtre et le texte visible en premier.

![figure de l’écran avec du texte net et flou ](images/vis-layout-image6.png)

Les utilisateurs se concentrent sur les principaux contrôles interactifs et sur l’instruction principale visible, et n’examinent les autres éléments que lorsqu’ils en ont besoin.

-   Les utilisateurs ont tendance à lire des étiquettes de contrôle interactives, en particulier celles qui semblent pertinentes pour accomplir la tâche en cours. En revanche, les utilisateurs ont tendance à lire le texte statique uniquement lorsqu’ils pensent qu’ils en ont besoin.
-   Les éléments qui apparaissent différemment attirent l’attention. Le texte en gras et le texte de grande taille sont extraits du texte normal. Les éléments d’interface utilisateur avec une couleur ou sur un arrière-plan coloré. Les éléments avec des icônes dépassent les éléments sans icônes.
-   Les utilisateurs ne font pas défiler sauf s’ils ont une raison de. Si le contenu [situé au-dessus du pli](glossary.md) ne fournit pas de raison de faire défiler, ce n’est pas le cas.
-   Une fois que les utilisateurs ont décidé de faire, ils arrêtent immédiatement l’analyse et le font.
-   Étant donné que les utilisateurs arrêtent l’analyse lorsqu’ils pensent qu’ils sont terminés, ils ont tendance à ignorer tout ce qui se trouve au-delà de ce qui semble être le point de terminaison.

![capture d’écran des options du clavier ](images/vis-layout-image7.png)

Les utilisateurs arrêtent l’analyse lorsqu’ils pensent qu’ils sont terminés.

Bien entendu, il y aura des exceptions à ce modèle général. Les appareils de suivi oculaire indiquent que le comportement réel des utilisateurs est tout à fait erratique. L’objectif de ce modèle est de vous aider à prendre des décisions et des compromis efficaces, et non à modéliser correctement le comportement de l’utilisateur. Mais comme vous avez lu cette liste, j’espère que vous avez déjà reconnu un grand nombre de vos propres modèles de lecture.

### <a name="designing-for-scanning"></a>Conception pour l’analyse

**Les utilisateurs ne lisent pas, et vous devez donc concevoir des surfaces d’interface utilisateur pour l’analyse.** Ne partez pas du principe que les utilisateurs lisent le texte tel qu’il est écrit de gauche à droite, de haut en bas, mais qu’ils regardent les éléments d’interface utilisateur qui attirent leur attention.

Pour la conception pour l’analyse :

-   Supposons que les utilisateurs commencent par analyser rapidement la fenêtre entière, puis à lire les éléments d’interface utilisateur dans l’ordre suivant :
    -   Contrôles interactifs au centre
    -   Boutons de validation
    -   Contrôles interactifs trouvés ailleurs
    -   Instruction principale
    -   Explications supplémentaires
    -   Texte présenté avec une icône d’avertissement
    -   Titre de la fenêtre
    -   Autre texte statique dans le corps principal
    -   Notes de bas de page
-   Placez les éléments d’interface utilisateur qui lancent une tâche dans l’angle supérieur gauche ou supérieur au centre.
-   Placez les éléments d’interface utilisateur qui terminent une tâche dans le coin inférieur droit.
-   Dans la mesure du possible, placez du texte crucial sur les contrôles interactifs à la place du texte statique.
-   Évitez de placer des informations cruciales dans le coin inférieur gauche ou en bas d’un contrôle ou d’une page longue défilement.
-   Ne présentez pas de grands blocs de texte. Éliminez le texte inutile. Utilisez le style de présentation de la [pyramide inversée](text-ui.md) .
-   Si vous voulez attirer l’attention des utilisateurs, assurez-vous que cette attention est justifiée.

Dans la mesure du possible, travaillez avec ce modèle au lieu de le combattre. Toutefois, il se peut que vous ayez besoin de mettre en évidence ou de mettre en évidence des éléments d’interface utilisateur spécifiques.

Pour mettre en évidence les éléments d’interface utilisateur principaux :

-   Placez les éléments d’interface utilisateur principaux dans le [chemin d’analyse](glossary.md).
-   Placez une interface utilisateur pour lancer une tâche dans le coin supérieur gauche ou supérieur au centre.
-   Placez les boutons de validation dans le coin inférieur droit.
-   Placez l’interface utilisateur principale restante au centre.
-   Utilisez des contrôles qui attirent votre attention, tels que des boutons de commande, des liens de commande et des icônes.
-   Utilisez le texte visible, y compris le texte de grande taille et le texte en gras.
-   Placez le texte que les utilisateurs doivent lire dans des contrôles interactifs, ou avec des icônes, ou sur des [bannières](vis-graphic.md).
-   Utilisez du texte foncé sur un arrière-plan clair.
-   Entourez les éléments d’un espace généreux.
-   N’exigez aucune interaction, telle que le pointage ou le pointage, pour voir l’élément que vous insistez.

    ![capture d’écran des options d’activation de Windows ](images/vis-layout-image8.png)

    Cet exemple montre de nombreuses façons de mettre en évidence des éléments d’interface utilisateur principaux.

Pour mettre en évidence les éléments d’interface utilisateur secondaires :

-   Placez les éléments d’interface utilisateur secondaires en dehors du chemin d’analyse.
-   Il n’est généralement pas nécessaire de voir les utilisateurs dans le coin inférieur gauche ou le bas de la fenêtre.
-   Utilisez des contrôles qui n’attirent pas l’attention, tels que des liens de tâches à la place de boutons de commande.
-   Utilisez du texte normal ou gris.
-   Utilisez du texte clair sur un arrière-plan sombre. Le texte blanc sur un arrière-plan gris foncé ou bleu est bien adapté.
-   Entourez les éléments avec un espace minimal.
-   Envisagez d’utiliser la [Divulgation progressive](ctrl-progressive-disclosure-controls.md) pour masquer les éléments d’interface utilisateur secondaires.

    ![capture d’écran des éléments d’interface volumineux et de petite taille ](images/vis-layout-image9.png)

    Cet exemple montre de nombreuses façons de mettre en évidence des éléments d’interface utilisateur secondaires.

### <a name="using-screen-space-effectively"></a>Utilisation efficace de l’espace à l’écran

L’utilisation efficace de l’espace à l’écran vous oblige à équilibrer plusieurs facteurs : utilisez trop d’espace et une fenêtre semble lourde et gaspiller, et même difficile à utiliser en fonction de la [Loi de Fitts](inter-mouse.md).

**Incorrect :**

![capture d’écran montrant trop d’espace blanc ](images/vis-layout-image10.png)

Dans cet exemple, la fenêtre est trop volumineuse pour son contenu.

D’un autre côté, utilisez trop peu d’espace et une fenêtre semble exigu, peu confortable et intimidante, et difficile à utiliser si elle nécessite un défilement et d’autres manipulations à utiliser.

**Incorrect :**

![capture d’écran avec un trop grand nombre de contrôles ](images/vis-layout-image11.png)

Dans cet exemple, la fenêtre est trop petite pour son contenu.

Bien que l’interface utilisateur critique doive tenir dans la [résolution effective](glossary.md)minimale prise en charge, ne supposez pas que l’utilisation de l’espace à l’écran signifie que Windows doit être aussi petit que possible. **Une disposition efficace a un respect de l’espace ouvert et ne tente pas de récolter tout dans le plus petit espace possible.** Les affichages modernes ont un espace d’écran significatif et il est judicieux d’utiliser cet espace efficacement lorsque vous le pouvez. Par conséquent, Err sur le côté de utilise trop d’espace d’écran plutôt que trop petit. Cela rend votre Windows plus claire et plus facile à aborder.

Vous savez qu’une disposition utilise efficacement l’espace à l’écran dans les cas suivants :

-   Windows, les volets de fenêtre et les contrôles n’ont pas besoin d’être redimensionnés pour être utilisables. Si la première chose que les utilisateurs effectuent est le redimensionnement d’une fenêtre, d’un volet ou d’un contrôle, sa taille est incorrecte.
-   Les données ne sont pas tronquées. La plupart des données dans les vues de liste et les arborescences n’ont pas de ellipses, et les données d’autres contrôles ne sont pas découpées, sauf si la longueur des données est anormalement élevée. Les données qui doivent être lues pour effectuer une tâche ne doivent pas être tronquées.
-   Les fenêtres et les contrôles sont dimensionnés de manière appropriée pour éliminer les défilements inutiles. Il y a peu de barres de défilement horizontales et aucune barre de défilement verticale inutile.
-   Les contrôles utilisent principalement leurs tailles standard. Efforcez-vous de réduire le nombre de tailles de contrôle, par exemple, en n’utilisant qu’une ou deux largeurs de bouton de commande sur une surface.
-   L’aire de l’interface utilisateur est équilibrée. Il n’y a pas de grandes zones d’écran inutilisées.

Choisissez des tailles de fenêtre qui sont juste assez grandes pour atteindre leur objectif. (Et si la fenêtre est redimensionnable, cet objectif s’applique à sa taille par défaut.) **Une combinaison de données tronquées ou de barres de défilement et d’un espace d’écran disponible est un signe clair de mise en page inefficace.**

### <a name="control-sizing"></a>Dimensionnement du contrôle

En général, la première étape de l’utilisation de l’espace à l’écran consiste à déterminer la taille appropriée pour les différents éléments de l’interface utilisateur. Reportez-vous au [tableau de dimensionnement de contrôle](#recommended-sizing-and-spacing) , ainsi qu’au dimensionnement recommandé dans les Articles de la directive de contrôle spécifique.

La Loi de Fitts indique que la plus petite cible est, plus il faut de temps pour l’acquérir avec la souris. en outre, pour les ordinateurs qui utilisent technologie Windows Tablet and Touch, la « souris » peut être en fait un stylet ou le doigt de l’utilisateur. vous devez donc prendre en compte d’autres périphériques d’entrée lorsque vous déterminez les tailles des petits contrôles. **Une taille de contrôle de pixels relatifs de 16x16 est une bonne taille minimale pour tout périphérique d’entrée.** En revanche, les boutons standard de contrôle spin des pixels relatifs 15x9 sont trop petits pour être utilisés efficacement par les stylets.

### <a name="spacing"></a>Espacement

Le fait de fournir un espace important (mais pas excessif) rend la disposition plus confortable et plus facile à analyser. L’espace effectif n’est pas inutilisé. il joue un rôle important dans l’amélioration de la capacité des utilisateurs à effectuer des analyses, et ajoute également à l’attrait visuel de votre conception. Pour obtenir des instructions, reportez-vous à la [table Spacing](#recommended-sizing-and-spacing).

pour les ordinateurs qui utilisent technologie Windows Tablet and Touch, la « souris » peut être en fait un stylet ou le doigt de l’utilisateur. Le ciblage est plus difficile lorsque vous utilisez un stylet ou un doigt comme périphérique de pointage, ce qui a pour conséquence que les utilisateurs appuient à l’extérieur de la cible prévue. Lorsque les contrôles interactifs sont placés très proches les uns des autres, mais ne se touchent pas réellement, les utilisateurs peuvent cliquer sur l’espace inactif entre les contrôles. Étant donné que le fait de cliquer sur l’espace inactif n’a pas de résultat ou de rétroaction visuelle, les utilisateurs sont souvent incertains mal. Si les petits contrôles sont trop espacés, l’utilisateur doit appuyer avec précision pour éviter de cliquer sur l’objet incorrect. **Pour résoudre ces problèmes, les régions cibles des contrôles interactifs doivent être en contact ou avoir au moins 3 dlu (5 pixels relatifs) d’espace entre eux.**

Vous savez qu’une disposition présente un espace correct lorsque :

-   En général, la surface de l’interface utilisateur semble confortable et ne semble pas exigu.
-   L’espace s’affiche uniformément et est équilibré.
-   Les éléments associés sont proches les uns des autres et les éléments non liés sont relativement éloignés.
-   Il n’y a pas d’espace mort entre les contrôles qui sont censés être réunis, tels que les boutons de barre d’outils.

### <a name="resizable-windows"></a>Fenêtres redimensionnables

Les fenêtres redimensionnables sont également un facteur d’utilisation efficace de l’espace à l’écran. Certaines fenêtres se composent d’un contenu fixe et ne peuvent pas être redimensionnées, mais Windows avec du contenu redimensionnable doit être redimensionnable. Bien entendu, la raison pour laquelle les utilisateurs redimensionnent une fenêtre est d’utiliser l’espace d’écran supplémentaire, afin que le contenu soit développé en conséquence en donnant plus d’espace aux éléments de l’interface utilisateur qui en ont besoin. Windows avec du contenu dynamique, des documents, des images, des listes et des arborescences tirent le meilleur parti des fenêtres redimensionnables.

![capture d’écran de l’obtention de la barre de défilement du contrôle redimensionné ](images/vis-layout-image12.png)

Dans cet exemple, le redimensionnement de la fenêtre redimensionne le contrôle List View.

Cela dit, Windows peut être étiré trop grand. Par exemple, de nombreuses pages du panneau de configuration deviennent peu maniables lorsque le contenu est plus grand que 600 pixels relatifs. Dans ce cas, il est préférable de ne pas redimensionner la zone de contenu au-delà de cette largeur maximale ou de modifier l’origine du contenu lorsque la fenêtre est redimensionnée plus grand. Au lieu de cela, conservez une largeur maximale et une origine fixe supérieure gauche.

Le texte devient difficile à lire à mesure que la longueur de la ligne augmente. Pour les documents texte, envisagez une longueur de ligne maximale de 80 caractères pour faciliter la lecture du texte. (Les caractères incluent des lettres, des signes de ponctuation et des espaces.)

**Incorrect :**

![capture d’écran de la boîte de message larges avec du texte long ](images/vis-layout-image13.png)

Dans cet exemple, la longueur de texte long rend la lecture difficile.

Enfin, les fenêtres redimensionnables doivent également utiliser efficacement l’espace à l’écran lorsqu’elles sont plus petites, en rendant le contenu redimensionnable plus petit et en supprimant l’espace des éléments de l’interface utilisateur qui peuvent fonctionner efficacement sans lui. À un moment donné, la fenêtre ou ses éléments d’interface utilisateur deviennent trop petits pour être utilisables. par conséquent, ils doivent être affectés à une taille minimale ou certains éléments doivent être complètement supprimés.

![capture d’écran de la fenêtre avec ruban de grande taille, intrusif ](images/vis-layout-image14.png)

![capture d’écran de la fenêtre sans ruban ](images/vis-layout-image15.png)

Dans cet exemple, le volet a une taille minimale.

Certains programmes tirent parti de l’utilisation d’une présentation totalement différente pour rendre le contenu utilisable à des tailles plus petites.

![capture d’écran des boutons du lecteur multimédia centré ](images/vis-layout-image16.png)

dans cet exemple, Lecteur Windows Media modifie son format lorsque la fenêtre devient trop petite pour le format standard.

### <a name="focus"></a>Priorité

Une disposition a le focus lorsqu’il y a un emplacement évident à rechercher en premier. Le focus est important pour montrer aux utilisateurs où commencer l’analyse de votre fenêtre ou de votre page. Sans le focus, l’œil de l’utilisateur s’inerrer. Le point focal doit être un élément important que les utilisateurs doivent trouver et comprendre rapidement, et doivent avoir la plus grande importance visuelle. L’angle supérieur gauche est le point focal naturel pour la plupart des fenêtres.

Il ne doit y avoir qu’un seul point focal. Tout comme dans la vie réelle, l’œil ne peut se concentrer que sur une seule chose à la fois, les utilisateurs ne peuvent pas se concentrer simultanément sur plusieurs emplacements.

Pour qu’un élément d’interface utilisateur soit le point focal, vous pouvez lui donner un accent sur les points suivants :

-   En la plaçant dans la partie supérieure gauche ou centrale supérieure de l’aire.
-   Utilisation de contrôles interactifs qui sont importants et facilement compréhensibles.
-   Utilisation d’un texte visible, tel qu’une instruction principale.
-   Attribution de la sélection par défaut aux contrôles et du focus d’entrée initial.
-   Placement des contrôles dans un arrière-plan de couleur différent.

envisagez de Windows la recherche. le point focal de la recherche de Windows doit être la zone de recherche, car il s’agit du point de départ de la tâche. Toutefois, il se trouve dans le coin supérieur droit pour être cohérent avec le positionnement de la zone de recherche standard. La zone de recherche a le focus d’entrée, mais étant donné son emplacement dans le chemin d’analyse, cette indication seule n’est pas suffisante.

Pour résoudre ce problème, il y a une instruction visible dans la partie supérieure centrale de la fenêtre pour diriger les utilisateurs vers l’emplacement approprié.

**Acceptable:**

![capture d’écran de la boîte de dialogue Rechercher avec du texte utile ](images/vis-layout-image17.png)

Dans cet exemple, une instruction visible dans la partie supérieure centrale de la fenêtre dirige les utilisateurs vers la zone de recherche.

Sans les instructions, la fenêtre n’aurait pas de point focal évident.

**Incorrect :**

![capture d’écran de la boîte de dialogue Rechercher sans texte ](images/vis-layout-image18.png)

Cet exemple n’a pas de point focal évident. Les utilisateurs ne savent pas où chercher.

Si vous donnez un élément visuel à l’élément d’interface utilisateur, assurez-vous que cette attention est justifiée. dans le précédent exemple de recherche de Windows incorrect, le bouton tout en surbrillance se trouve dans le coin supérieur gauche et est l’accentant le plus visuel, mais ce n’est pas le point focal prévu. Les utilisateurs peuvent être amenés à regarder ce bouton en tentant de déterminer la marche à suivre.

**Incorrect :**

![capture d’écran du bouton tout en surbrillance ](images/vis-layout-image19.png)

Sans l’instruction visible comme point focal, le bouton tout en surbrillance est un point focal non intentionnel.

### <a name="flow"></a>Flux

Une disposition est fluide lorsque les utilisateurs sont dirigés correctement et naturellement par un chemin d’accès clair via sa surface, recherchant des éléments d’interface utilisateur dans l’ordre approprié à leur utilisation. Une fois que les utilisateurs identifient le point focal, ils doivent déterminer comment effectuer la tâche. Le placement des éléments d’interface utilisateur communique leur relation et doit refléter les étapes pour effectuer la tâche. En général, cela signifie que les étapes de la tâche doivent circuler naturellement dans un ordre de gauche à droite et de haut en bas (dans les cultures occidentales).

Vous savez qu’une disposition a un bon sens dans les cas suivants :

-   Le placement des éléments de l’interface utilisateur reflète les étapes dont les utilisateurs ont besoin pour effectuer la tâche.
-   Les éléments d’interface utilisateur qui lancent une tâche se trouvent dans l’angle supérieur gauche ou supérieur au centre.
-   Les éléments d’interface utilisateur qui terminent une tâche se trouvent dans le coin inférieur droit.
-   Les éléments d’interface associés sont réunis. les éléments non liés sont séparés.
-   Les étapes requises se trouvent dans le processus principal.
-   Les étapes facultatives sont en dehors du processus principal, éventuellement en raison de l’utilisation d’un arrière-plan ou d’une divulgation progressive appropriée.
-   Les éléments fréquemment utilisés apparaissent avant les éléments rarement utilisés dans le chemin d’analyse.
-   Les utilisateurs savent toujours quoi faire ensuite. Il n’y a pas de sauts ou de sauts inattendus dans le workflow de tâche.

**Incorrect :**

![capture d’écran de la disposition de boîte de dialogue déroutante ](images/vis-layout-image20.png)

Dans cet exemple, les utilisateurs ne savent pas quoi faire ensuite. Il y a des sauts et des sauts inattendus dans le workflow de tâche.

**Correct :**

![capture d’écran d’une boîte de dialogue bien planifiée ](images/vis-layout-image21.png)

Dans cet exemple, la présentation des éléments de l’interface utilisateur reflète les étapes nécessaires à l’exécution de la tâche.

### <a name="grouping"></a>Regroupement

Une disposition a un regroupement quand des éléments d’interface logiques liés à l’interface utilisateur ont une relation visuelle claire. Les groupes sont importants, car il est plus facile pour les utilisateurs de comprendre et de se concentrer sur un groupe d’éléments associés que sur les éléments individuellement. Les groupes rendent une disposition plus simple et plus facile à analyser.

Vous pouvez afficher le regroupement des manières suivantes (en augmentation du poids) :

-   **Dispose.** Vous pouvez regrouper les contrôles associés les uns à côté des autres et placer un espace supplémentaire entre les contrôles non liés.

    ![figure de quatre icônes avec quatre groupes de tâches ](images/vis-layout-image22.png)

    Dans cet exemple, la disposition seule est utilisée pour afficher les relations de contrôle.

-   **Séparateurs.** Un séparateur est une ligne horizontale ou verticale qui unifie un groupe de contrôles. Les séparateurs offrent une apparence plus simple et plus claire. Toutefois, contrairement aux zones de groupe, elles fonctionnent mieux quand elles s’étendent à l’ensemble de la surface.

    ![capture d’écran de trois icônes et de trois séparateurs ](images/vis-layout-image23.png)

    Dans cet exemple, les séparateurs étiquetés sont utilisés pour afficher les relations de contrôle.

-   **Agrégateurs.** Un agrégateur est un graphique qui crée une relation visuelle entre des contrôles étroitement liés.

    ![capture d’écran des contrôles à l’intérieur d’une ligne elliptique ](images/vis-layout-image24.png)

    Dans cet exemple, une agrégation de limites est utilisée pour mettre en évidence la relation entre les contrôles et les faire ressembler à un contrôle unique au lieu de huit.

-   **Zones de groupe.** Une zone de groupe est un cadre rectangulaire étiqueté qui entoure un ensemble de contrôles connexes.

    ![capture d’écran de cases à cocher dans une bordure rectangulaire ](images/vis-layout-image25.png)

    Dans cet exemple, une zone de groupe entoure et étiquette un ensemble de contrôles connexes.

-   **Fond.** Vous pouvez utiliser les arrière-plans pour mettre en évidence ou retirer les différents types de contenu.

    ![capture d’écran du côté gauche du panneau de configuration ](images/vis-layout-image26.png)

    Dans cet exemple, le volet de tâches du panneau de configuration est utilisé pour regrouper les tâches associées et les éléments du panneau de configuration.

    Pour éviter tout encombrement visuel, le meilleur choix est le regroupement de poids le plus clair qui effectue le travail. Pour plus d’informations, consultez [zones de groupe](ctrl-group-boxes.md), [onglets](ctrl-tabs.md), [séparateurs et arrière-plans](vis-graphic.md).

Quel que soit le style de regroupement, vous pouvez utiliser la mise en retrait pour afficher la relation des contrôles au sein d’un groupe. Les contrôles qui sont des homologues doivent être alignés à gauche, et les contrôles dépendants sont mis en retrait à 12 unités de plus ou 18 pixels relatifs.

![capture d’écran de trois niveaux de contrôles mis en retrait ](images/vis-layout-image27.png)

Les contrôles dépendants sont mis en retrait à 12 ou 18 pixels relatifs, ce qui correspond à la distance entre les cases à cocher et les cases d’option de leurs étiquettes.

Vous savez qu’une disposition a un bon regroupement lorsque :

-   La fenêtre ou les pages ont au plus 7 groupes.
-   L’objectif de chaque groupe est évident.
-   La relation entre les contrôles dans chaque groupe est évidente, en particulier pour les dépendances de contrôle.
-   Le regroupement simplifie le contenu au lieu de le rendre plus complexe.

### <a name="alignment"></a>Alignment

L’alignement est le positionnement coordonné des éléments d’interface utilisateur. L’alignement est important car il rend le contenu plus facile à analyser et affecte la perception visuelle de l’utilisateur.

Il y a plusieurs objectifs à prendre en compte lors de la détermination de l’alignement :

-   **Faciliter l’analyse horizontale.** Les utilisateurs peuvent lire horizontalement et rechercher les éléments associés les uns à côté des autres, sans aucun écart difficile.
-   **Faciliter l’analyse verticale.** Les utilisateurs peuvent analyser les colonnes d’éléments associés et trouver immédiatement ce qu’ils recherchent, avec un mouvement d’œil horizontal minimal.
-   **Complexité visuelle minimale.** Les utilisateurs perçoivent qu’une disposition est visuellement complexe si elle contient des lignes de grille d’alignement verticale inutiles.

### <a name="horizontal-alignment"></a>Alignement horizontal

**Alignement à gauche**

En raison de l’ordre de lecture de gauche à droite, l’alignement à gauche fonctionne bien pour la plupart du contenu. L’alignement à gauche permet d’analyser facilement les données en colonnes verticalement.

**Alignement à droite**

L’alignement à droite est le meilleur choix pour les données numériques, en particulier les [colonnes de données numériques](ctrl-text-boxes.md). L’alignement à droite fonctionne également bien pour les [boutons de validation](glossary.md) , ainsi que pour les contrôles alignés sur le bord de la fenêtre de droite.

![capture d’écran du bouton fléché vers le bas de la recherche avancée ](images/vis-layout-image28.png)

Dans cet exemple, le contrôle de la divulgation progressive de la recherche avancée est aligné à droite, car il est placé sur le bord de la fenêtre de droite.

**Alignement centré**

L’alignement au centre est réservé aux situations où l’alignement à gauche ou à droite est inapproprié ou non équilibré.

![capture d’écran des contrôles du lecteur multimédia centré ](images/vis-layout-image29.png)

Dans cet exemple, le contrôle Media Player est centré pour obtenir une apparence équilibrée.

Ne pas centrer le contenu de la fenêtre juste pour remplir l’espace.

**Incorrect :**

![capture d’écran d’une fenêtre avec trop d’espace blanc ](images/vis-layout-image30.png)

Dans cet exemple, le contenu n’est pas centré correctement dans une fenêtre redimensionnable pour remplir l’espace.

### <a name="vertical-alignment"></a>Alignement vertical

**Élément vers le haut**

En raison de l’ordre de lecture de haut en bas, l’alignement en haut fonctionne bien pour la plupart des contenus. L’alignement en haut facilite l’analyse horizontale des éléments d’interface utilisateur.

**Lignes de base de texte**

Quand vous alignez verticalement des contrôles avec du texte, alignez les lignes de base de texte pour obtenir un flot de lecture horizontal lisse.

**Correct :**

![capture d’écran de l’alignement du bouton et du texte de l’étiquette ](images/vis-layout-image31.png)

**Incorrect :**

![capture d’écran du texte du bouton et de l’étiquette non aligné ](images/vis-layout-image32.png)

Dans l’exemple correct, le contrôle et son étiquette sont alignés verticalement par leurs lignes de base de texte.

Vous savez qu’une disposition a un bon alignement dans les cas suivants :

-   Il est facile d’analyser à la fois horizontalement et verticalement.
-   Il a une apparence visuelle simple.

### <a name="label-alignment"></a>Alignement des étiquettes

Les règles d’alignement générales s’appliquent aux étiquettes de contrôle, mais il s’agit d’un problème courant pour une attention particulière. L’alignement des étiquettes a les objectifs suivants :

-   Facilitez l’analyse verticale pour trouver le bon contrôle.
-   Faciliter l’analyse horizontale pour associer des étiquettes à leurs contrôles.
-   Facilité de localisation, gestion des étiquettes dont la longueur varie entre les langues.
-   Fonctionne bien avec une combinaison de différentes longueurs d’étiquettes.
-   Permet d’utiliser efficacement l’espace disponible tout en évitant le texte tronqué.

L’objectif global est de réduire le nombre de mouvements oculaires requis pour trouver ce que les utilisateurs cherchent probablement, mais la nature des contrôles et les utilisateurs recherchés dépendent du contexte.

Il existe quatre styles d’emplacement et d’alignement d’étiquette communs, chacun avec ses avantages :

-   Étiquettes alignées à gauche au-dessus des contrôles
-   Étiquettes alignées à gauche à gauche des contrôles
-   Étiquettes alignées à gauche à gauche des contrôles, contrôles en drapeau à gauche
-   Étiquettes alignées à droite à gauche des contrôles

**Étiquettes alignées à gauche au-dessus des contrôles**

Ce style est le plus facile à localiser, car la disposition ne dépend pas de la longueur des étiquettes, mais elle prend l’espace le plus vertical.

![liste avec deux colonnes d’étiquettes au-dessus des contrôles ](images/vis-layout-image33.png)

Ce style prend l’espace le plus vertical, mais il est plus facile à localiser. Il s’agit d’un meilleur choix pour étiqueter principalement des contrôles interactifs.

Idéal pour :

-   Les contrôles étiquetés sont interactifs (pas seulement du texte).
-   L’interface utilisateur sera localisée. Ce style offre souvent de la place pour doubler ou même tripler la longueur de l’étiquette.
-   L’interface utilisateur utilise une technologie de disposition fixe (telle que Win32).
-   Il y a dix ou moins de contrôles. Avec davantage de contrôles, les étiquettes sont difficiles à analyser.
-   Il y a suffisamment d’espace vertical pour accueillir les étiquettes.
-   La disposition doit être de forme libre, pas seulement des colonnes.

**Étiquettes alignées à gauche à gauche des contrôles**

Ce style est le plus facile à analyser verticalement et il fonctionne également bien lorsque les étiquettes diffèrent beaucoup, mais il est plus difficile d’associer l’étiquette à son contrôle. Ce style peut utiliser des étiquettes à plusieurs lignes si nécessaire.

![liste avec quatre colonnes d’étiquettes à gauche des contrôles ](images/vis-layout-image34.png)

Ce style fonctionne bien. Toutefois, il y a deux colonnes, mais visuellement, il semble qu’il y ait quatre fois que les données semblent plus complexes.

Idéal pour :

-   Les utilisateurs sont susceptibles d’effectuer une analyse verticale pour trouver des étiquettes spécifiques.
-   Les utilisateurs ne peuvent pas lire les étiquettes et les contrôles d’une manière allant de gauche à droite et de haut en bas.
-   Il y a suffisamment d’espace horizontal pour accueillir les étiquettes.
-   Les étiquettes varient considérablement en longueur.
-   Il existe de nombreux contrôles, tels que les formulaires.
-   Il y a peu de colonnes. Visuellement, les étiquettes et les contrôles apparaissent sous la forme de deux colonnes individuelles.

**Étiquettes alignées à gauche à gauche des contrôles, contrôles en drapeau à gauche**

Ce style facilite l’analyse verticale des étiquettes, les étiquettes et les contrôles, et l’efficacité de l’espacement. mais il est plus difficile d’analyser les contrôles verticalement. Les contrôles sont alignés à droite pour tirer pleinement parti de l’espace disponible.

![liste de deux colonnes d’étiquettes avec des contrôles irréguliers ](images/vis-layout-image35.png)

Ce style est compact et facile à lire, mais il est difficile d’analyser les contrôles verticalement.

Idéal pour :

-   L’interface utilisateur utilise une technologie de présentation variable (par exemple, Windows Presentation Foundation).
-   Les utilisateurs sont susceptibles d’effectuer une analyse verticale pour trouver des étiquettes spécifiques.
-   Les utilisateurs sont susceptibles de lire les étiquettes et les contrôles de gauche à droite et de haut en bas.
-   Les utilisateurs ne sont pas susceptibles d’analyser les contrôles verticalement.
-   Le texte du contrôle varie en fonction de la longueur et sera probablement tronqué si un autre style était utilisé.
-   Les contrôles sont en lecture seule, tels que les zones de texte en lecture seule. Pour les autres contrôles, cet alignement sera mal écrit. Toutefois, les contrôles peuvent devenir modifiables au clic.
-   Il y a plusieurs colonnes, mais peu de contrôles dans une colonne.

**Étiquettes alignées à droite à gauche des contrôles**

Ce style est le plus facile à lire horizontalement pour associer les étiquettes à leurs contrôles, mais il est difficile d’analyser les étiquettes verticalement et ne fonctionne pas correctement lorsque les labelsList avec des étiquettes et des contrôles en retrait diffèrent beaucoup.

![liste avec étiquettes et contrôles mis en retrait ](images/vis-layout-image36.png)

Ce style permet une analyse verticale facile des contrôles, mais rend difficile l’analyse verticale des étiquettes.

Idéal pour :

-   Les utilisateurs sont susceptibles de lire les étiquettes et les contrôles de gauche à droite et de haut en bas.
-   Les utilisateurs ne sont pas susceptibles d’effectuer une analyse verticale pour trouver des étiquettes spécifiques, probablement parce que :
    -   Il y a peu de contrôles.
    -   Les étiquettes sont bien connues.
    -   Les contrôles sont principalement explicites et sont rarement vides (éventuellement avec des valeurs par défaut pour empêcher les contrôles vides).
-   Il y a suffisamment d’espace horizontal pour accueillir les étiquettes.
-   La longueur des étiquettes n’est pas très variable.
-   Il y a beaucoup de colonnes. Visuellement, les étiquettes et les contrôles apparaissent sous la forme d’une colonne unique.

Toutefois, avant d’adopter l’un de ces styles, tenez compte de deux facteurs supplémentaires :

-   Préférez un style que vous pouvez utiliser de manière cohérente dans votre programme.
-   Les étiquettes alignées à gauche au-dessus des contrôles à gauche des contrôles sont les styles les plus courants, donc ils doivent être prioritaires.

### <a name="balance"></a>Balance

Une fenêtre ou une page s’équilibre quand son contenu apparaît uniformément réparti sur sa surface. Si la surface a la même pondération que celle qu’elle a visuellement, une disposition équilibrée n’est pas une astuce sur un côté.

Le problème d’équilibre le plus courant consiste à avoir trop de contenu sur le côté gauche d’une fenêtre ou d’une page. Vous pouvez créer un équilibre des manières suivantes :

-   En utilisant des marges plus grandes sur le côté gauche que sur la droite.
-   Placement des éléments de l’interface utilisateur utilisés pour effectuer une tâche à droite.
-   Placement des éléments d’interface utilisateur utilisés tout au long de la tâche au centre.
-   Allongement des contrôles redimensionnables ou à plusieurs lignes.
-   Utilisation stratégique de l’alignement du centre.

![capture d’écran de l’imprimante à gauche et texte à droite ](images/vis-layout-image37.png)

Cette mise en page de l’Assistant bien équilibrée affiche une marge de gauche supérieure à droite pour améliorer l’équilibre.

Si ces techniques n’atteignent pas le solde, envisagez de réduire la largeur de la fenêtre ou de la page pour mieux correspondre à son contenu.

Pour les surfaces redimensionnables, ne Centrez pas le contenu juste pour obtenir un équilibre. Au lieu de cela, conservez une origine fixe supérieure gauche, définissez une surface d’exposition maximale et équilibrez le contenu dans l’espace utilisé.

### <a name="grids"></a>Grilles

Une grille est un système d’alignement sous-jacent invisible. Les grilles peuvent être symétriques, mais les grilles asymétriques fonctionnent tout aussi bien. Lorsqu’elles sont utilisées par une seule fenêtre ou page, les grilles permettent d’organiser le contenu dans une surface. Lorsqu’elles sont réutilisées, les grilles créent une disposition cohérente entre les surfaces.

Le nombre de lignes de la grille affecte la perception de la complexité visuelle. Une disposition avec moins de lignes de grille s’affiche plus simple qu’une disposition avec davantage de lignes de la grille.

**Visuellement complexe :**

![capture d’écran de la boîte de dialogue encombrée ](images/vis-layout-image38.png)

**Visuellement simple :**

![capture d’écran de la boîte de dialogue organisée ](images/vis-layout-image39.png)

Les quadrillages inutiles créent une complexité visuelle.

Vous savez qu’une disposition utilise des grilles de manière efficace dans les cas suivants :

-   Windows ou des pages avec un contenu ou une fonction similaire ont une disposition similaire.
-   Les éléments de conception répétés apparaissent dans des emplacements similaires sur les fenêtres et les pages.
-   Il n’y a pas de quadrillage d’alignement vertical et horizontal inutile.

### <a name="visual-simplicity"></a>Simplicité visuelle

La simplicité visuelle est le sentiment qu’une disposition n’est pas plus compliquée qu’elle ne doit l’être.

Vous savez qu’une disposition présente une simplicité visuelle quand elle :

-   Élimine les couches inutiles de chrome de fenêtre.
-   Présente le contenu en utilisant au plus sept groupes facilement identifiables.
-   Utilise le regroupement léger, tel que la disposition et les séparateurs au lieu des zones de groupe.
-   Utilise des contrôles légers, tels que des liens au lieu de boutons de commande pour les commandes secondaires, et des listes déroulantes au lieu de listes pour les choix.
-   Réduit le nombre de lignes de grille d’alignement vertical et horizontal.
-   Réduit le nombre de tailles de contrôle, par exemple, à l’aide d’une ou deux largeurs de bouton de commande sur une surface.
-   Utilise la divulgation progressive pour masquer les éléments d’interface utilisateur jusqu’à ce qu’ils soient nécessaires.
-   Utilise suffisamment d’espace pour que la fenêtre ou la page ne semble pas exigu.
-   Dimensionne les fenêtres et les contrôles de manière appropriée afin d’éliminer les défilements inutiles.
-   Utilise une police unique avec un petit nombre de tailles et de couleurs de texte.

En règle générale, si un élément de disposition peut être éliminé sans nuire à l’efficacité de l’interface utilisateur, il est probable qu’il soit.

## <a name="guidelines"></a>Consignes

### <a name="screen-resolution-and-dpi"></a>Résolution d’écran et PPP

-   **prendre en charge la résolution minimale Windows de 800 x 600 pixels.** Pour les interfaces utilisateur critiques qui doivent fonctionner en mode sans échec, prennent en charge une résolution efficace de 640 x 480 pixels. Veillez à tenir compte de l’espace utilisé par la barre des tâches en réservant 48 [pixels relatifs](glossary.md) verticaux pour les fenêtres affichées avec la barre des tâches.
-   **Optimisez les dispositions de fenêtres redimensionnables pour une résolution efficace de 1024 x 768 pixels.** Redimensionnez automatiquement ces fenêtres pour réduire la résolution de l’écran d’une manière qui reste fonctionnelle.
-   **Veillez à tester votre Windows en mode 96 points par pouce (dpi) (à 800x600 pixels), 120 ppp (à 1024 x 768 pixels) et 144 dpi (en 1200x900 pixels).** Vérifiez les problèmes de disposition, tels que le découpage des contrôles, du texte et des fenêtres, et l’étirement des icônes et des bitmaps.
-   **Pour les programmes qui utilisent des scénarios tactiles et mobiles, optimisez pour 120 ppp.** Les écrans haute résolution sont actuellement répandus sur les PC tactiles et les ordinateurs portables.

### <a name="window-size"></a>Taille de la fenêtre

-   **Choisissez une taille de fenêtre par défaut adaptée à son contenu.** N’hésitez pas à utiliser des tailles de fenêtre initiales supérieures si vous pouvez utiliser l’espace de manière efficace.
-   **Utilisez une hauteur équilibrée pour les proportions de largeur.** Les proportions entre 3:5 et 5:3 sont préférées, bien que les proportions de 1:3 puissent être utilisées pour les boîtes de dialogue de message (telles que les erreurs et les avertissements).
-   **Utilisez des fenêtres redimensionnables quand cela est possible pour éviter les barres de défilement et les données tronquées.** Windows avec du contenu dynamique, des documents, des images, des listes et des arborescences tirent le meilleur parti des fenêtres redimensionnables.
-   **Pour les documents texte, envisagez une longueur de ligne maximale de 80 caractères** pour faciliter la lecture du texte. (Les caractères incluent des lettres, des signes de ponctuation et des espaces.)
-   Fenêtres à taille fixe :
    -   **Les fenêtres à taille fixe doivent être entièrement visibles et dimensionnées pour s’ajuster à la zone de travail.**
-   Fenêtres redimensionnables :
    -   **Les fenêtres redimensionnables peuvent être optimisées pour des résolutions plus élevées, mais en fonction des besoins au moment de l’affichage de la résolution réelle de l’écran.**
    -   **Les tailles de fenêtre progressivement plus volumineuses doivent afficher progressivement plus d’informations.** Assurez-vous qu’au moins une partie ou un contrôle de fenêtre a un contenu redimensionnable.
    -   **Conserver l’origine supérieure gauche du contenu fixe, car la fenêtre est redimensionnée.** Ne déplacez pas l’origine pour équilibrer le contenu au fur et à mesure que la taille de la fenêtre change.
    -   **Définissez une taille de contenu maximale si le contenu peut être trop étendu trop grand.** Si le contenu devient encombrant, ne redimensionnez pas la zone de contenu au-delà de sa largeur maximale ou modifiez l’origine du contenu, car la fenêtre est redimensionnée en fonction de sa taille. Au lieu de cela, conservez une largeur maximale et une origine fixe supérieure gauche.
    -   **Définissez une taille de fenêtre minimale s’il y a une taille au-dessous de laquelle le contenu n’est plus utilisable.** Pour les contrôles redimensionnables, définissez la taille minimale des éléments redimensionnables sur leur plus petite taille fonctionnelle, telle que la largeur minimale des colonnes fonctionnelles dans les affichages de liste. Les éléments facultatifs de l’interface utilisateur doivent être complètement supprimés.
    -   **Envisagez de modifier la présentation afin que le contenu soit utilisable à des tailles plus petites.**

        ![capture d’écran des contrôles du lecteur multimédia ](images/vis-layout-image16.png)

        dans cet exemple, Lecteur Windows Media modifie son format lorsque la fenêtre devient trop petite pour le format standard.

### <a name="control-size"></a>Taille du contrôle

-   **Rendez tous les contrôles interactifs au moins de 16x16 pixels relatifs.** cela fonctionne bien pour tous les périphériques d’entrée, y compris technologie Windows Tablet and Touch.
-   **Dimensionnez les contrôles pour éviter les données tronquées.** Ne tronquez pas les données qui doivent être lues pour effectuer une tâche. Taille des colonnes d’affichage de liste pour éviter les données tronquées.
-   **Dimensionnez les contrôles pour éliminer les défilements inutiles.** Augmentez légèrement les contrôles si vous supprimez une barre de défilement. Il doit y avoir peu de barres de défilement verticales et pas de barres de défilement horizontales inutiles.

    ![capture d’écran de la liste dimensionnée pour éviter une barre de défilement ](images/vis-layout-image40.png)

    Dans cet exemple, la liste déroulante est dimensionnée pour éliminer la barre de défilement.

-   **Réduisez le nombre de tailles de contrôle sur une surface.** Préférez l’utilisation des [tailles de contrôle recommandées standard](#recommended-sizing-and-spacing) et, si nécessaire, utilisez des contrôles plus grands ou plus petits de taille constante. Essayez d’utiliser une seule largeur pour les zones de liste et les arborescences, et pas plus de trois largeurs pour les boutons de commande et les listes déroulantes. Toutefois, les largeurs de zone de texte et de zone de liste déroulante doivent suggérer la longueur de leur entrée la plus longue ou attendue.

    ![capture d’écran de la boîte de dialogue avec des listes et des boutons ](images/vis-layout-image41.png)

    Dans cet exemple, une zone de liste et une taille de bouton de commande sont utilisées de manière cohérente.

-   **Pour les contrôles dimensionnés en fonction de leur texte, incluez 30 pour cent supplémentaires (jusqu’à 200 pour cent pour du texte plus petit) pour tout texte qui sera localisé.** Cette règle suppose que la disposition est conçue à l’aide de texte en anglais. Notez également que cette règle fait référence au texte localisé, et non aux nombres.
-   **Étendez les contrôles de texte statique, les cases à cocher et les cases d’option à la largeur maximale qui sera adaptée à la disposition.** Cela évite la troncation du texte de longueur variable et de la localisation.

    **Incorrect :**

    ![capture d’écran du contrôle de progression et du texte partiel ](images/vis-layout-image42.png)

    Dans cet exemple, le texte du contrôle est inutilement tronqué.

### <a name="control-spacing"></a>Espacement des contrôles

-   **Si les contrôles ne sont pas en contact, vous devez disposer d’au moins 3 unités de commande (5 pixels relatifs) d’espace entre eux.** Dans le cas contraire, les utilisateurs peuvent cliquer sur l’espace inactif entre les contrôles. Étant donné que le fait de cliquer sur l’espace inactif n’a pas de résultat ou de rétroaction visuelle, les utilisateurs sont souvent incertains mal.

### <a name="placement"></a>Sélection élective

-   **Réorganisez les éléments d’interface utilisateur dans une surface pour qu’ils circulent naturellement dans un ordre de gauche à droite et de haut en bas (dans les cultures occidentales).** Le placement des éléments d’interface utilisateur communique leur relation et doit refléter les étapes pour effectuer la tâche.
-   **Placez les éléments d’interface utilisateur qui lancent une tâche dans l’angle supérieur gauche ou supérieur au centre.** Donnez à l’élément d’interface utilisateur que les utilisateurs doivent d’abord examiner la plus grande importance visuelle.
-   **Placez les éléments d’interface utilisateur qui terminent une tâche dans le coin inférieur droit.**
-   **Placez ensemble les éléments d’interface utilisateur associés et séparez les éléments non liés.**
-   **Placez les étapes requises dans le processus principal.**
-   **Placez des étapes facultatives en dehors du processus principal,** éventuellement en raison de l’utilisation d’un arrière-plan ou d’une divulgation progressive appropriée.
-   **Placez les éléments fréquemment utilisés avant les éléments rarement utilisés** dans le chemin d’analyse.

### <a name="focus"></a>Priorité

-   **Choisissez un seul élément d’interface utilisateur que les utilisateurs doivent consulter en premier pour être le point focal.** Le point focal doit être un élément important que les utilisateurs doivent trouver et comprendre rapidement.
-   **Placez le point focal dans le coin supérieur gauche ou le centre supérieur.**
-   **Donnez au point focal la plus grande importance visuelle,** par exemple le texte visible, la sélection par défaut ou le focus d’entrée initial.

### <a name="alignment"></a>Alignment

-   Normalement, utilisez l’alignement à gauche.
-   Utilisez l’alignement à droite pour les données numériques, en particulier les colonnes de données numériques.
-   Utilisez l’alignement à droite pour les boutons de validation, ainsi que les contrôles alignés sur le bord de la fenêtre de droite.
-   Utilisez l’alignement centré lorsque l’alignement à gauche ou à droite est inapproprié ou s’il est déséquilibré.
-   Quand vous alignez verticalement des contrôles avec du texte, alignez les lignes de base de texte pour obtenir un flot de lecture horizontal lisse.
-   Pour l’alignement des étiquettes, reportez-vous à la section [alignement des étiquettes](#label-alignment) dans concepts de conception.

### <a name="accessibility"></a>Accessibilité

-   **N’utilisez pas la disposition comme seul moyen de transmettre des informations importantes sur une interface utilisateur.** Les utilisateurs qui ont des troubles de la vision peuvent ne pas être en mesure d’interpréter cette présentation. Par exemple, assurez-vous que les étiquettes de contrôle communiquent leur relation à d’autres éléments.
-   **N’incorporez pas de contrôles subordonnés dans les étiquettes de contrôle pour créer une phrase ou une expression.** Ces associations sont basées uniquement sur la disposition et ne sont pas gérées correctement par la navigation au clavier ou les technologies d’assistance d’accessibilité. En outre, cette technique n’est pas localisable, car la structure de phrase varie en fonction de la langue.

    **Incorrect :**

    ![capture d’écran d’une zone de texte au milieu d’une phrase ](images/vis-layout-image43.png)

    Dans cet exemple, la zone de texte est placée incorrectement dans l’étiquette de la case à cocher.

    **Correct :**

    ![capture d’écran d’une zone de texte à la fin d’une phrase ](images/vis-layout-image44.png)

    Ici, la zone de texte est placée après l’étiquette de la case à cocher.

-   **Rendre le regroupement accessible.** Les groupes définis par les volets de fenêtre, les zones de groupe, les séparateurs, les étiquettes de texte et les agrégateurs sont gérés automatiquement par les aides à l’accessibilité. Toutefois, les groupes définis uniquement par le placement et les arrière-plans ne le sont pas et doivent être définis par programmation pour l’accessibilité.

Pour plus d’instructions, consultez [accessibilité](inter-accessibility.md).

## <a name="recommended-sizing-and-spacing"></a>Dimensionnement et espacement recommandés

**Dimensionnement du contrôle**

Le tableau suivant répertorie les tailles recommandées (largeur x hauteur, ou hauteur si un seul nombre) pour les éléments d’interface utilisateur courants (pour 9 PT. Segoe UI à 96 ppp). Les largeurs basées sur l’élément le plus long en anglais ajoutent 30 pour cent pour la localisation (jusqu’à 200 pour cent pour du texte plus bref) pour tout texte (mais pas les nombres) qui sera localisé.



| Exemple | Control | Unités du dialogue | Pixels relatifs |
|-------------------------------------------------------------------------------------------------|----------------------------|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| ![capture d’écran des cases à cocher et de leurs étiquettes ](images/vis-layout-image45.png)<br/>       | Cases à cocher<br/>     | 10<br/>                                                                                     | 17<br/>                                                                                              |
| ![capture d’écran de la zone de liste déroulante ](images/vis-layout-image46.png)<br/>                          | Zones de liste modifiable<br/>     | largeur de l’élément le plus long + 30% x 14<br/>                                                       | largeur de l’élément le plus long + 30% x 23<br/>                                                                |
| ![capture d’écran d’un bouton de commande ](images/vis-layout-image47.png)<br/>                   | Boutons de commande<br/> | 50 x 14<br/>                                                                                | 75 x 23<br/>                                                                                         |
| ![capture d’écran de l’un des deux liens de commande sélectionnés ](images/vis-layout-image48.png)<br/>  | Liens de commande<br/>   | 25 (une ligne) ou 35 (deux lignes)<br/>                                                        | 41 (une ligne) ou 58 (deux lignes)<br/>                                                                 |
| ![capture d’écran d’une liste déroulante ](images/vis-layout-image49.png)<br/>                   | Listes déroulantes<br/> | largeur des données valides les plus longues + 30% x 14<br/>                                                 | largeur de l’élément le plus long + 30% x 23<br/>                                                                |
| ![capture d’écran d’une zone de liste ](images/vis-layout-image50.png)<br/>                         | Zones de liste<br/>      | largeur de l’élément le plus long + 30% x un nombre entier d’éléments (3 éléments au minimum)<br/>            |                                                                                                            |
| ![capture d’écran d’une liste de fichiers image ](images/vis-layout-image51.png)<br/>            | Affichages de liste<br/>      | largeur des colonnes évitant les données tronquées x un nombre entier d’éléments<br/>                 |                                                                                                            |
| ![capture d’écran d’une barre de progression ](images/vis-layout-image52.png)<br/>                     | Barres de progression<br/>   | 107 ou 237 x 8<br/>                                                                         | 160 ou 355 x 15<br/>                                                                                 |
| ![capture d’écran des cases d’option ](images/vis-layout-image53.png)<br/>                      | Cases d’option<br/>   | 10<br/>                                                                                     | 17<br/>                                                                                              |
| ![capture d’écran du contrôle Slider ](images/vis-layout-image54.png)<br/>                     | Curseurs<br/>         | 15<br/>                                                                                     | 24<br/>                                                                                              |
| ![capture d’écran du texte : « sélectionner le fuseau horaire » ](images/vis-layout-image55.png)<br/>           | Texte (statique)<br/>   | 8<br/>                                                                                      | 13<br/>                                                                                              |
| ![capture d’écran d’une zone de texte vide ](images/vis-layout-image56.png)<br/>                     | Zones de texte<br/>      | largeur de l’entrée la plus longue ou attendue + 30% x 14 (une ligne) + 10 pour chaque ligne supplémentaire<br/> | largeur des données valides les plus longues + 30% x 23 pixels relatifs (une ligne) + 16 pour chaque ligne supplémentaire<br/> |
| ![capture d’écran de dossiers imbriqués dans l’Explorateur Windows ](images/vis-layout-image57.png)<br/> | Arborescences<br/>      | largeur de l’élément le plus long + 30% x un nombre entier d’éléments (5 éléments au minimum)<br/>            |                                                                                                            |



 

**Espacement**

Le tableau suivant répertorie l’espacement recommandé entre les éléments d’interface utilisateur communs (pour 9 PT. Segoe UI à 96 ppp).



|   &nbsp; | Élément | Unités du dialogue | Pixels relatifs |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| ![Image représentant l’espacement des marges de la boîte de dialogue ](images/vis_layout_image58.jpeg)<br/>        | Marges de la boîte de dialogue<br/>                                                                         | 7 sur tous les côtés<br/>                                                                 | 11 sur tous les côtés<br/>                                                                |
| ![Image représentant l’espacement entre les étiquettes et les contrôles ](images/vis_layout_image59.jpeg)<br/>  | Entre les étiquettes de texte et leurs contrôles associés (par exemple, les zones de texte et les zones de liste)<br/> | 3<br/>                                                                              | 5<br/>                                                                              |
| ![Image présentant l’espacement entre les contrôles connexes ](images/vis_layout_image60.jpeg)<br/>     | Entre les contrôles connexes<br/>                                                                   | 4<br/>                                                                              | 7<br/>                                                                              |
| ![Image représentant l’espacement entre les contrôles non liés ](images/vis_layout_image61.jpeg)<br/>   | Entre des contrôles non liés<br/>                                                                 | 7<br/>                                                                              | 11<br/>                                                                             |
| ![Image représentant l’espacement du premier contrôle dans un groupe ](images/vis_layout_image62.jpeg)<br/>  | Premier contrôle dans une zone de groupe<br/>                                                               | 11 en haut de la zone de groupe ; Aligner verticalement sur le titre de la zone de groupe<br/> | 16 en haut de la zone de groupe ; Aligner verticalement sur le titre de la zone de groupe<br/> |
| ![Aa511279. between (en-US, MSDN. 10) .jpg](images/vis_layout_image60.jpeg)<br/>         | Entre les contrôles dans une zone de groupe<br/>                                                            | 4<br/>                                                                              | 7<br/>                                                                              |
| ![Image représentant l’espacement entre les boutons ](images/vis_layout_image63.jpeg)<br/>              | Entre les boutons disposés horizontalement ou verticalement<br/>                                        | 4<br/>                                                                              | 7<br/>                                                                              |
| ![Image représentant l’espacement du dernier contrôle dans un groupe ](images/vis_layout_image64.jpeg)<br/>   | Dernier contrôle dans une zone de groupe<br/>                                                                | 7 au-dessus du bas de la zone de groupe<br/>                                            | 11 au-dessus du bas de la zone de groupe<br/>                                           |
| ![Image représentant l’espacement du bord gauche de la zone de groupe ](images/vis_layout_image65.jpeg)<br/>  | À partir du bord gauche d’une zone de groupe<br/>                                                          | 6<br/>                                                                              | 9<br/>                                                                              |
| ![Image représentant l’espacement de l’étiquette de texte à côté du contrôle ](images/vis_layout_image66.jpeg)<br/> | Étiquette de texte à côté d’un contrôle<br/>                                                                | 3 en haut du contrôle<br/>                                             | 5 en haut du contrôle<br/>                                             |
| ![Image représentant l’espacement entre les paragraphes du texte ](images/vis_layout_image67.jpeg)<br/>   | Entre des paragraphes de texte<br/>                                                                 | 7<br/>                                                                              | 11<br/>                                                                             |
|                                                                                                   | Espace le plus petit entre les contrôles interactifs<br/>                                                | 3 ou aucun espace<br/>                                                                  | 5 ou aucun espace<br/>                                                                  |
|                                                                                                   | Espace le plus petit entre un contrôle non interactif et tout autre contrôle<br/>                     | 2<br/>                                                                              | 3<br/>                                                                              |



 

 

