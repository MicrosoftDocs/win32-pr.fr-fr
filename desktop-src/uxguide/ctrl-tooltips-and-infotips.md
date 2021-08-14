---
title: Info-bulles et info-bulles
description: Une info-bulle est une petite fenêtre contextuelle qui étiquette le contrôle sans étiquette désigné, par exemple les contrôles de barre d’outils sans étiquette ou les boutons de commande.
ms.assetid: 80979281-eefb-485a-b42f-7f9e05665357
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 4df7950529b2ac78c9d9bbf51c8996f17bcd985898a286f8d58e05db3b94d27e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118041135"
---
# <a name="tooltips-and-infotips"></a>Info-bulles et info-bulles

> [!NOTE]
> ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Une info-bulle est une petite fenêtre contextuelle qui étiquette le contrôle sans étiquette désigné, par exemple les contrôles de barre d’outils sans étiquette ou les boutons de commande.

![Capture d’écran montrant le bouton imprimer avec l’info-bulle « imprimer (Ctrl + P) » affiché.](images/ctrl-tooltips-and-infotips-image1.png)

Info-bulle standard pour un bouton de barre d’outils.

Étant donné que les info-bulles sont tellement utiles, il existe un contrôle associé appelé info-bulles, qui fournit un texte plus descriptif que celui possible avec les info-bulles.

une info-bulle est une petite fenêtre contextuelle qui décrit de façon concise l’objet désigné, par exemple les descriptions des contrôles toolbar, les icônes, les graphiques, les liens, les objets Windows Explorer, les éléments menu Démarrer et les boutons de la barre des tâches. Les info-bulles sont une forme de [contrôles de divulgation progressive](ctrl-progressive-disclosure-controls.md), ce qui évite d’avoir à toujours obtenir un texte descriptif à l’écran.

![capture d’écran du bouton partager avec une info-bulle ](images/ctrl-tooltips-and-infotips-image2.png)

Info-bulle classique.

Dans le cadre de cet article, les info-bulles et les info-bulles sont appelés conseils.

Astuces aider les utilisateurs à comprendre les objets inconnus ou inconnus qui ne sont pas décrits directement dans l’interface utilisateur (iu). Ils s’affichent automatiquement lorsque les utilisateurs pointent le pointeur sur un objet et sont supprimés lorsque les utilisateurs cliquent sur le contrôle ou déplacent la souris, ou lorsque le Conseil expire.

**Développeurs :** Il n’y a pas de contrôle info-bulle ; info-bulles sont implémentées avec le contrôle ToolTip. La distinction est l’utilisation, et non l’implémentation.

> [!Note]  
> Les instructions relatives aux [bulles](ctrl-balloons.md), aux [barres d’outils](cmd-toolbars.md)et à [l’aide](winenv-help.md) sont présentées dans des articles distincts.

 

## <a name="is-this-the-right-control"></a>Est-ce le contrôle approprié ?

Pour vous décider, posez-vous les questions suivantes :

-   **Les informations sont-elles affichées en fonction du pointage pointeur ?** Si ce n’est pas le cas, utilisez un autre contrôle. Affichez les conseils uniquement à la suite de l’intervention de l’utilisateur. En revanche, les [bulles](ctrl-balloons.md) peuvent s’afficher de manière autonome (comme c’est le cas avec les notifications), de sorte qu’elles possèdent une fin qui identifie leur source.
-   **Le contrôle a-t-il une étiquette avec un libellé ?** Si ce n’est pas le cas, utilisez une info-bulle pour l’indiquer. Notez que la plupart des contrôles doivent être étiquetés et, par conséquent, ne pas avoir d’info-bulles. Les contrôles ToolBar et les boutons de commande avec des étiquettes graphiques doivent avoir des info-bulles.
-   **Un objet bénéficie-t-il d’une description supplémentaire ou d’informations supplémentaires ?** Si c’est le cas, utilisez une info-bulle. Toutefois, le texte doit être supplémentaire, ce qui n’est pas essentiel pour les tâches principales. S’il est essentiel, mettez-le directement dans l’interface utilisateur de sorte que les utilisateurs le trouvent sans peine.
-   **Les informations supplémentaires sont-elles une erreur, un avertissement ou un État ?** Dans ce cas, utilisez un autre élément d’interface utilisateur, tel qu’une bulle, un [message d’erreur](mess-error.md)ou une [barre d’État](ctrl-status-bars.md). L’icône de la zone de notification info-bulles est une exception, car elle peut être utilisée pour afficher des informations d’État.
-   **Les utilisateurs doivent-ils interagir avec l’info-bulle ?** Si c’est le cas, utilisez un autre contrôle, tel qu’une info-bulle. Il est impossible d’interagir avec une info-bulle parce qu’elle disparaît lorsqu’on déplace la souris.
-   **Les utilisateurs doivent-ils imprimer les informations supplémentaires ?** Si c’est le cas, utilisez un autre contrôle, tel qu’un champ de commentaire statique. Toutefois, vous pouvez également utiliser info-bulles pour fournir un accès direct à ces informations.

    ![capture d’écran de la bulle de commentaire ](images/ctrl-tooltips-and-infotips-image3.png)

    dans cet exemple, un champ de commentaire statique dans Microsoft Word permet aux utilisateurs d’imprimer des commentaires.

-   **Le contexte est-il que les utilisateurs peuvent trouver les conseils ennuyeux ou gênants ?** Si c’est le cas, envisagez d’utiliser une autre solution, y compris ne rien faire du tout. Si vous utilisez des conseils dans de tels contextes, autorisez les utilisateurs à les désactiver.

Lorsqu’ils sont utilisés de manière appropriée, les conseils améliorent la communication avec l’utilisateur. **N’utilisez jamais des conseils comme substituts pour une bonne conception.** Si un graphique, un bouton ou un autre objet oblige les utilisateurs à continuer à vérifier un Conseil pour le comprendre, la conception est incorrecte. Corrigez plutôt la conception.

## <a name="design-concepts"></a>Principes de conception

Astuces sont un moyen puissant de simplifier une interface utilisateur. Ils fournissent les informations dont les utilisateurs ont besoin lorsqu’ils en ont besoin, avec un minimum d’effort de leur part. Astuces peut vous aider à utiliser l’espace à l’écran plus efficacement et à réduire l’encombrement de l’écran. Toutefois, les conseils mal conçus peuvent être gênants, gênants, inutiles, insurmontables ou en cours. Les concepts de conception suivants sont conçus pour illustrer la différence.

### <a name="discoverability"></a>Détectabilité

Astuces afficher automatiquement quand les utilisateurs pointent le pointeur sur un objet pendant une période donnée. Ce mécanisme de délai rend les astuces très pratiques, mais réduit également leur découverte.

au fil du temps, les utilisateurs apprennent que certains objets standard, tels que les boutons de la barre d’outils, les boutons graphiques, les éléments de menu Démarrer et les icônes de la zone de notification, possèdent des conseils, ce qui vous permet de prendre leur détectabilité pour les autorisations.

La découverte des conseils dans des emplacements non standard est plus longue pour les utilisateurs. Il n’y a pas d’indice visuel, tel qu’une zone réactive ou une modification de pointeur, qui indique qu’un objet a une info-bulle. Pire encore, certains utilisateurs déplacent leur souris autour d’un grand nombre, surtout lorsqu’ils apprennent à naviguer dans l’interface utilisateur. Les utilisateurs doivent savoir qu’un objet a une astuce, soit par le passé, soit par l’expérimentation.

Vous pouvez améliorer la détectabilité en utilisant des conseils de manière cohérente, ce qui favorise la prévisibilité. Si vous fournissez des conseils pour certains objets, vous devez les fournir pour tous les objets similaires pour lesquels les utilisateurs sont susceptibles de vouloir obtenir des informations supplémentaires. Parfois, il peut être difficile de le faire, car vous devez également vous assurer que les conseils sont utiles et pas évidents.

Si vous fournissez des astuces détectables et cohérentes et utiles pour être un problème, envisagez d’autres conceptions, telles que des étiquettes de contrôle explicites ou du texte supplémentaire sur place.

### <a name="appropriate-information"></a>Informations appropriées

Les informations appropriées pour les conseils ont les caractéristiques suivantes :

-   **Bref.** Les fenêtres contextuelles utilisées par les conseils sont parfaites pour des phrases courtes et des fragments de phrase, ainsi que du texte mis en forme. Les blocs de texte volumineux et non mis en forme sont difficiles à lire et insurmontables.
-   **Facilement.** Le texte info-bulle doit être informatif. Il ne devrait pas être évident ou simplement répéter ce qui est déjà à l’écran.
-   **Supplémentaires.** Étant donné que le texte info-bulle n’est pas toujours visible, il doit s’agir d’informations supplémentaires que les utilisateurs n’ont pas à lire. Les informations importantes doivent être communiquées à l’aide d’étiquettes de contrôle explicites ou de texte supplémentaire sur place.
-   **Statique.** Les utilisateurs ne sont pas censés passer d’une instance à l’autre, de sorte qu’il est peu probable qu’ils remarquent des modifications du contenu dynamique, telles que des informations d’État. Les astuces pour les icônes de la zone de notification sont une exception notable : les utilisateurs sont plus susceptibles de découvrir des modifications dans les informations sur les pourboires, car ces icônes communiquent principalement l’État.

### <a name="appropriate-timeouts"></a>Délais d’expiration appropriés

L’affichage et la suppression automatiques appropriés des conseils sont essentiels pour l’objectif des utilisateurs qui maintiennent le contrôle de leur environnement d’interface utilisateur. Astuces avez trois valeurs de délai d’attente :

-   **D'.** L’heure à laquelle le pointeur doit rester immobile pour que l’info-bulle s’affiche. L’heure par défaut est de 0,5 secondes.
-   **Réafficher.** L’heure à laquelle le pointeur doit rester immobile au fur et à mesure que le pointeur se déplace d’une cible à l’autre. L’heure par défaut est de 0,1 secondes.
-   **Levée.** Heure après laquelle le Conseil est automatiquement supprimé. L’heure par défaut est de 5 secondes.

Si vous avez trop de valeurs initiale et de réaffichages trop courtes, vous obtiendrez une expérience gênante et perturbatrice, car elles seraient souvent affichées par inadvertance, tandis que des conseils ne peuvent pas répondre ou ne pas être détectés. L’heure de suppression par défaut fonctionne bien pour le texte d’info-bulle, tel qu’il est utilisé dans les info-bulles. Info-bulles a un texte plus long, donc il a besoin de plus de temps d’affichage.

### <a name="appropriate-placement"></a>Emplacement approprié

Astuces doit être placé près de l’objet en cours de survol, généralement à la fin ou à la tête du pointeur, si possible. Toutefois, ils ne doivent jamais être placés d’une manière qui interfère avec ce que l’utilisateur fait en masquant l’objet qui l’intéresse. Pour éviter ce problème, vous devrez peut-être déplacer le Conseil à l’extérieur du pointeur, mais à côté de l’objet. Ce n’est pas un problème tant que la relation entre l’objet et son Tip est claire. Assurez-vous que les utilisateurs ne déplacent pas le pointeur simplement pour faire disparaître les conseils de votre programme.

### <a name="accessibility"></a>Accessibilité

Astuces avoir un effet inhabituel sur l’accessibilité. Bien qu’ils soient normalement déclenchés en plaçant le pointeur sur un objet, les astuces sont gérées par les [lecteurs d’écran](inter-accessibility.md) pour les contrôles avec accès au clavier. Lorsqu’elles sont utilisées de manière appropriée pour obtenir des informations plus concises, utiles, statiques et supplémentaires, les conseils peuvent améliorer l’accessibilité globale. En fait, le modèle d’info-bulle du texte de remplacement est la meilleure façon de rendre les graphiques accessibles. Toutefois, en cas d’utilisation inappropriée, elles nuisent à l’accessibilité en rendant les informations importantes ou dynamiques plus difficiles à obtenir.

Fournir plusieurs méthodes pour accéder à un contrôle si ce contrôle requiert un Conseil qui n’a pas accès au clavier.

![capture d’écran du bouton d’impression avec info-bulle ](images/ctrl-tooltips-and-infotips-image4.png)

Dans cet exemple, les utilisateurs peuvent imprimer à l’aide du bouton de barre d’outils (qui n’est pas accessible par le clavier) ou du raccourci clavier de la commande d’impression.

**Si vous n’avez qu’une seule chose...**

Concevez des conseils détectables qui affichent des informations plus précises, utiles, statiques et supplémentaires à l’endroit approprié au moment opportun.

## <a name="usage-patterns"></a>Modèles d’usage

Astuces avoir plusieurs modèles d’utilisation :



|    Usage                                                                                                                             |    Exemple                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Info-bulles**<br/> Affichez l’étiquette d’un contrôle ou d’un glyphe sans étiquette. <br/>                                         | Comme ces conseils servent d’étiquettes, leur texte suit les indications relatives aux étiquettes pour le contrôle sous-jacent. <br/> ![capture d’écran du bouton Exporter la liste avec l’info-bulle ](images/ctrl-tooltips-and-infotips-image5.png)<br/> dans cet exemple, l’info-bulle indique l’étiquette de la commande.<br/> ![capture d’écran du bouton fermer avec l’info-bulle ](images/ctrl-tooltips-and-infotips-image6.png)![capture d’écran du bouton de lecture avec l’info-bulle ](images/ctrl-tooltips-and-infotips-image7.png)<br/> dans ces exemples, les info-bulles étiquettent les boutons graphiques.<br/> ![capture d’écran de l’affichage du glyphe de menu avec info-bulle ](images/ctrl-tooltips-and-infotips-image8.png)<br/> Dans cet exemple, l’info-bulle étiquette un glyphe.<br/> |
| **Info-bulles**<br/> fournissez une description supplémentaire ou une explication d’un objet ou d’un contrôle. <br/>                  | Utilisez info-bulles pour décrire ou expliquer des objets et des contrôles tels que les contrôles ToolBar, les [icônes](vis-icons.md) (y compris les superpositions [d'](cmd-toolbars.md) icône), les [liens](ctrl-links.md), les [onglets](ctrl-tabs.md), les [contrôles de divulgation progressive](ctrl-progressive-disclosure-controls.md)et les contrôles personnalisés. <br/> ![capture d’écran du bouton courrier électronique avec une info-bulle ](images/ctrl-tooltips-and-infotips-image9.png)<br/> ![capture d’écran du bouton de gravure avec une info-bulle ](images/ctrl-tooltips-and-infotips-image10.png)<br/> Dans ces exemples, info-bulles fournit des informations supplémentaires sur les contrôles et les objets.<br/>                                                                                        |
| **Texte de remplacement info-bulles**<br/> Décrivez un graphique pour l’accessibilité. <br/>                                              | Ce modèle est principalement destiné aux utilisateurs qui ont une forme de troubles de la vision et peut utiliser un lecteur d’écran. <br/> ![capture d’écran du bouton Démarrer de Windows avec une info-bulle ](images/ctrl-tooltips-and-infotips-image11.png)<br/> dans cet exemple, l’info-bulle décrit le graphique menu Démarrer.<br/>                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Miniatures**<br/> affiche une petite image d’un élément. <br/>                                                         | Les miniatures offrent une représentation graphique facilement reconnaissable d’une fenêtre ou d’un document. <br/> ![capture d’écran de la miniature des catégories du panneau de configuration ](images/ctrl-tooltips-and-infotips-image12.png)<br/> dans cet exemple, la barre des tâches Windows fournit des conseils miniatures pour ses éléments.<br/> ![capture d’écran de la miniature de photo et de ses données ](images/ctrl-tooltips-and-infotips-image13.png)<br/> dans cet exemple, Windows galerie de photos fournit des conseils miniatures pour ses éléments.<br/>                                                                                                                                                                                                                      |
| **Info-bulles détails**<br/> Affichez des informations détaillées sur un objet. <br/>                                        | Les info-bulles sont un moyen efficace d’afficher des informations détaillées sur un objet ou de fournir des données. <br/> ![capture d’écran de l’info-bulle montrant le type de fichier ](images/ctrl-tooltips-and-infotips-image14.png)![capture d’écran du graphique avec l’info-bulle détaillant les valeurs ](images/ctrl-tooltips-and-infotips-image15.png)<br/> Dans ces exemples, info-bulles fournit des informations détaillées sur un objet ou des données.<br/>                                                                                                                                                                                                                                                                                                      |
| **Menu Démarrer info-bulles**<br/> Décrivez un élément dans le menu Démarrer. <br/>                                              | Le menu Démarrer comprend des noms de programme et des destinations Windows importantes, telles que des documents, des images et le panneau de configuration. ces conseils décrivent les éléments du menu Démarrer, en général en donnant une brève description du programme ou de la destination, ainsi que des tâches principales que les utilisateurs peuvent effectuer. ces descriptions sont également indexées par la zone de recherche du menu Démarrer, ce qui aide les utilisateurs à trouver les programmes dont ils ont besoin. <br/> ![capture d’écran de l’info-bulle du centre d’accueil ](images/ctrl-tooltips-and-infotips-image16.png)<br/> dans cet exemple, l’info-bulle décrit ce que les utilisateurs peuvent faire avec un programme dans la menu Démarrer.<br/>                                                                                    |
| **Panneau de configuration info-bulles**<br/> Décrivez une catégorie ou une tâche du panneau de configuration. <br/>                                    | Ces conseils fournissent des informations supplémentaires pour aider les utilisateurs à choisir la catégorie et l’élément appropriés du panneau de configuration. <br/> ![capture d’écran de la catégorie comptes d’utilisateur avec info-bulle ](images/ctrl-tooltips-and-infotips-image17.png)<br/> Dans cet exemple, l’info-bulle décrit la catégorie comptes d’utilisateur du panneau de configuration.<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| **Nom complet info-bulles**<br/> affiche le nom complet d’un élément lorsque le nom est tronqué ou n’est pas entièrement visible. <br/> | Ces conseils vous permettent d’afficher des éléments dans un espace plus compact, tout en réduisant le besoin de défilement horizontal. Cela est particulièrement important lorsque la longueur du contenu est inconnue, car elle est dynamique. Contrairement aux autres modèles, lorsqu’ils sont utilisés dans des listes et des arborescences, ces conseils s’affichent directement sur l’objet source. <br/> ![capture d’écran de l’info-bulle du titre de groupe de cases d’option ](images/ctrl-tooltips-and-infotips-image18.png)<br/> Dans cet exemple, une info-bulle est utilisée pour afficher le nom complet de l’élément au pointage.<br/>                                                                                                                                                                                     |
| **Info-bulles d’État**<br/> Affichez les informations d’État pour les icônes de la zone de notification. <br/>                              | Normalement, les conseils doivent être statiques, car les utilisateurs ne sont pas censés passer d’une instance à l’autre. les icônes de la **zone de notification font exception** au fait que ces icônes communiquent l’État et qu’aucun autre espace n’est disponible pour le texte d’État. <br/> ![capture d’écran de l’info-bulle « Messenger non connecté » ](images/ctrl-tooltips-and-infotips-image19.png)<br/> ![capture d’écran de l’info-bulle « Messenger connecté » ](images/ctrl-tooltips-and-infotips-image20.png)<br/> Dans ces exemples, info-bulles fournit des informations d’État pour les icônes de la zone de notification.<br/>                                                                                                                                  |



 

## <a name="guidelines"></a>Consignes

### <a name="timeouts"></a>Délais d’expiration

-   **Utilisez les délais d’attente initial et de réaffichage par défaut. Titre**
    -   Les miniatures qui ne sont pas redondantes et affichées sur le côté de leur objet associé peuvent être affichées immédiatement (sans aucun délai). Toutefois, utilisez le délai d’expiration initial par défaut pour les miniatures redondantes (par exemple, une grande info-bulle pour un petit objet graphique) ou des miniatures couvrant l’objet associé.
-   **Pour les info-bulles, utilisez le délai d’expiration de la suppression des pourboires par défaut de cinq secondes.**
-   **Pour info-bulles, désactivez le délai d’attente de suppression du Conseil. Développeurs :** étant donné que vous ne pouvez pas désactiver techniquement le délai de suppression, définissez sa valeur la plus élevée.
-   Pour l’accessibilité, si vous devez définir les valeurs de délai d’attente sur une valeur autre que la valeur maximale, faites-les multiples des \_ paramètres système SPI GETMOUSEHOVERTIME et SPI \_ GETMESSAGEDURATION au lieu d’utiliser des heures fixes. Cela permet d’ajuster les délais d’attente à la vitesse de l’utilisateur.

### <a name="placement"></a>Sélection élective

-   **Évitez de couvrir l’objet avec lequel l’utilisateur est sur le ou l’utilisateur d’interagir.** Placez toujours le Conseil sur le côté de l’objet, même si cela nécessite une séparation entre le pointeur et l’info-bulle. Une séparation n’est pas un problème tant que la relation entre l’objet et son info-bulle est claire.

    -   **Exception :** Info-bulles de nom complet utilisés dans les listes et les arborescences.

    **Incorrect :**

    ![capture d’écran de la zone de recherche masquant l’info-bulle ](images/ctrl-tooltips-and-infotips-image21.png)

    **Correct :**

    ![capture d’écran de l’info-bulle placée sous la zone de recherche ](images/ctrl-tooltips-and-infotips-image22.png)

    Dans l’exemple correct, l’info-bulle est placée à l’extérieur de la zone de recherche, même si cela nécessite de l’espace entre elle et le signe insertion.

    **Incorrect :**

    ![capture d’écran de l’info-bulle masquant le texte révisé ](images/ctrl-tooltips-and-infotips-image23.png)

    **Correct :**

    ![capture d’écran de l’info-bulle placée au-dessus du texte révisé ](images/ctrl-tooltips-and-infotips-image24.png)

    Dans l’exemple correct, le texte sous-jacent est beaucoup plus utile que le Conseil, c’est pourquoi l’info-bulle est bien placée.

-   **Pour les collections d’éléments, évitez de couvrir l’objet suivant que l’utilisateur est susceptible d’afficher ou d’interagir avec.** Pour les éléments disposés horizontalement, évitez de placer des conseils à droite ; pour les éléments organisés verticalement, évitez de placer des conseils ci-dessous.

    **Incorrect :**

    ![capture d’écran de l’info-bulle masquant la liste des éléments récents ](images/ctrl-tooltips-and-infotips-image25.png)

    **Correct :**

    ![capture d’écran de l’info-bulle en regard de la liste des éléments récents ](images/ctrl-tooltips-and-infotips-image26.png)

    Dans l’exemple incorrect, le Conseil couvre l’objet que l’utilisateur est le plus susceptible d’interagir avec Next.

-   **Pour les conseils potentiellement gênants (souvent de grande taille), assurez-vous que les informations sont utiles pour la plupart des utilisateurs.** Si ce n’est pas le cas, vous pouvez faire en sorte que les astuces distractions soient facultatives ou même les éliminer. Dans le cas contraire, la plupart des utilisateurs devront déplacer le pointeur à l’extérieur de l’objet cible pour se débarrasser du Conseil.

### <a name="tooltips"></a>Info-bulles

-   **Utilisez des info-bulles pour fournir des étiquettes pour les contrôles sans étiquette.** Les contrôles qui ont généralement des info-bulles sont des [boutons de barre d’outils](cmd-toolbars.md), des boutons graphiques et des [contrôles de divulgation progressive](ctrl-progressive-disclosure-controls.md). Les contrôles avec des invites sont considérés comme étiquetés, tels que les [zones de texte](ctrl-text-boxes.md) et les [zones de liste modifiable](/windows/desktop/uxguide/ctrl-drop). Tous les autres contrôles doivent avoir des étiquettes explicites.
-   Utilisez des fragments de phrase sans ponctuation finale.
-   Utilisez les majuscules comme pour les phrases.
    -   **Exception :** cette recommandation est une nouveauté pour Windows Vista. Pour les applications héritées, vous pouvez utiliser la mise en majuscules de style titre si nécessaire pour éviter de mélanger les styles de mise en majuscules.
-   Ajoutez des [points de suspension](ctrl-command-buttons.md) si l’étiquette est destinée à une commande qui a besoin d’informations supplémentaires.
-   Comme avec les étiquettes normales, les **info-bulles gardent** généralement cinq mots ou moins, mais préfèrent des étiquettes spécifiques sur des étiquettes vagues.

    **Acceptable:**

    ![capture d’écran de l’info-bulle d’impression ](images/ctrl-tooltips-and-infotips-image27.png)

    **Conseillé**

    ![capture d’écran de l’info-bulle « imprimer sur l’imprimante par défaut » ](images/ctrl-tooltips-and-infotips-image28.png)

    **Meilleures**

    ![capture d’écran de l’info-bulle « imprimer (document Writer) » ](images/ctrl-tooltips-and-infotips-image29.png)

    **Incorrect :**

    ![capture d’écran de l’info-bulle détaillée ](images/ctrl-tooltips-and-infotips-image30.png)

    Dans ces exemples, le meilleur exemple est à la fois concis et spécifique, tandis que l’exemple incorrect est inutilement détaillé.

-   **Les info-bulles peuvent également fournir des détails supplémentaires sur les boutons de la barre d’outils étiquetés si cela s’avère utile.** Ne vous contentez pas de répéter ou de repasser un mot de ce qui figure déjà dans l’étiquette.

    **Correct :**

    ![capture d’écran de l’info-bulle « Rechercher dans toutes les Outlook » ](images/ctrl-tooltips-and-infotips-image31.png)

    Dans cet exemple, l’info-bulle explique ce que fait la recherche.

    **Incorrect :**

    ![capture d’écran de l’étiquette du bouton répété d’info-bulle ](images/ctrl-tooltips-and-infotips-image32.png)

    Dans cet exemple, l’info-bulle répète simplement ce qui se trouve déjà dans l’étiquette.

-   **Vous n’avez pas besoin de fournir des info-bulles de contrôles étiquetés simplement pour des raisons de cohérence.**

    ![capture d’écran des boutons étiquetés et sans étiquette ](images/ctrl-tooltips-and-infotips-image33.png)

    Dans cet exemple, les boutons de barre d’outils sans étiquette comportent des info-bulles, mais pas les autres.

-   Le cas échéant, **rendez les info-bulles plus utiles en fournissant des raccourcis clavier et des valeurs par défaut.** Placez ces informations supplémentaires entre parenthèses. Cela permet d’obtenir des info-bulles utiles pour les contrôles étiquetés, même s’ils se répètent simplement sur l’étiquette. N’envisagez pas ce texte supplémentaire lors de l’évaluation de la concision d’une info-bulle.

    ![capture d’écran de l’info-bulle « imprimer (document Writer) » ](images/ctrl-tooltips-and-infotips-image29.png)

    Dans cet exemple, Word affiche les valeurs par défaut et les raccourcis clavier dans les info-bulles de la barre d’outils.

### <a name="infotips"></a>Info-bulles

-   **Pour les info-bulles dans des emplacements non standard, privilégiez la cohérence par rapport à l’utilité pour améliorer la détectabilité.** Donnez des conseils pour tous les objets pour lesquels les utilisateurs sont susceptibles de vouloir obtenir des informations supplémentaires, même si quelques info-bulles peuvent être évidents. Cela évite que les utilisateurs attendent une info-bulle qui ne se produira jamais.
    -   **Exception :** Si seuls quelques objets ont des info-bulles utiles, n’utilisez pas de info-bulles. Utilisez plutôt des étiquettes de contrôle explicites ou du texte supplémentaire sur place à la place.
-   Utilisez des phrases entières avec une ponctuation finale.
    -   **Exception :** Icône de zone de notification [info-bulles](winenv-notification.md) n’utilisez pas de ponctuation finale.
-   Utilisez les majuscules comme pour les phrases.
-   Utilisez des dizaines d’instants, et non un futur.
-   Utilisez des constructions grammaticales parallèles. Le parallélisme exige que les mots et expressions ayant la même fonction aient la même forme.
    -   **Exception :** Pour le modèle d’info-bulle de nom complet, le texte de l’info-bulle correspond exactement à la formulation, à la mise en majuscules et à la ponctuation du contrôle sous-jacent.
-   **Évitez les grands info-bulles.** Les grands info-bulles sont difficiles à lire et difficiles à positionner sans interférer avec l’objet sous-jacent.
-   **Mettez en forme info-bulles pour faciliter la lecture et l’analyse de leur contenu.** Les blocs volumineux de texte non mis en forme peuvent être difficiles à lire.

    **Incorrect :**

    ![capture d’écran de l’info-bulle longue, non structurée et d’exécution ](images/ctrl-tooltips-and-infotips-image34.png)

    **Correct :**

    ![capture d’écran de la même info-bulle avec une ligne par élément ](images/ctrl-tooltips-and-infotips-image35.png)

    Dans l’exemple approprié, le texte mis en forme est beaucoup plus facile à lire et à analyser.

-   Lors de la première utilisation dans une info-bulle, épelez les noms des acronymes, suivis de l’acronyme entre parenthèses. Exemple : « protocole DHCP (Dynamic Host Configuration Protocol) ».

### <a name="start-menu-infotips"></a>Menu Démarrer info-bulles

-   utilisez menu Démarrer info-bulles pour **décrire l’élément de façon concise et répertorier les principales tâches que les utilisateurs peuvent effectuer avec l’élément.**
-   **Soyez utile.** Concentrez-vous sur ce que les utilisateurs peuvent faire. Ne vous contentez pas de répéter le nom de l’élément ou même de l’utiliser dans la description.
-   **Être spécifiques.** Évitez les verbes génériques et les expressions Catch-All, comme et d’autres tâches. Si les informations sont importantes, répertoriez-les en particulier. dans le cas contraire, partez du principe que les utilisateurs comprennent que tous les éléments ne sont pas listés dans le info-bulles.
-   **Soyez concis.** Utilisez 25 mots ou moins. Plus de info-bulles découragent la lecture.
-   **Commencez avec un verbe impératif actuel,** tel que créer, modifier, afficher et envoyer. préférer des verbes spécifiques sur des verbes génériques tels que manage et open, qui s’appliquent vraiment à la plupart des menu Démarrer éléments. Accédez directement au point.

    **Incorrect :**

    ![capture d’écran de l’info-bulle : ouvre le dossier musique ](images/ctrl-tooltips-and-infotips-image36.png)

    **Conseillé**

    ![capture d’écran de l’info-bulle : stocker et lire la musique ](images/ctrl-tooltips-and-infotips-image37.png)

    Dans l’exemple incorrect, l’info-bulle commence par un verbe générique. Le meilleur exemple se termine jusqu’au point avec des verbes spécifiques, mais continue à utiliser la formulation « and Other » inutile à la fin du Conseil.

-   **N’utilisez pas la langue qui semble marketing.**

    **Incorrect :**

    ![capture d’écran de l’info-bulle « point de départ d’un arrêt » ](images/ctrl-tooltips-and-infotips-image38.png)

    Dans cet exemple, l’info-bulle ressemble à marketing.

-   étant donné que ces info-bulles sont indexés pour la zone de recherche menu Démarrer, **décrivez les tâches importantes de votre programme à l’aide des termes pour lesquels les utilisateurs sont le plus susceptibles d’effectuer des recherches. Envisagez d’utiliser des mots clés et des synonymes courants.**

    **Incorrect :**

    ![capture d’écran de l’info-bulle : créer des DVD ](images/ctrl-tooltips-and-infotips-image39.png)

    **Correct :**

    ![capture d’écran de l’info-bulle : créer (graver) des CD, des DVD ](images/ctrl-tooltips-and-infotips-image40.png)

    Dans l’exemple correct, l’info-bulle a des synonymes courants.

-   Utilisez les majuscules comme pour les phrases.
-   **Développeurs :** le texte de l’info-bulle menu Démarrer provient du champ de commentaire de l’élément.

### <a name="quick-launch-tooltips"></a>Info-bulles de lancement rapide

-   **Utilisez une info-bulle avec le format :** Launch (nom complet du programme)
-   N’utilisez pas de ponctuation finale.
-   N’utilisez pas de texte supplémentaire pour décrire le programme ou ce qu’il fait. Étant donné que les utilisateurs choisissent les programmes qui s’affichent dans la barre de lancement rapide, ils connaissent déjà leur rôle.

### <a name="control-panel-infotips"></a>Panneau de configuration info-bulles

-   Utilisez le panneau de configuration info-bulles pour décrire de façon **concise les tâches du panneau de configuration et le matériel et les logiciels configurés.**
-   **Les noms et les icônes des panneaux de configuration doivent avoir info-bulles.** Les tâches individuelles n’ont pas d’info-bulles.
-   **Soyez utile.** Concentrez-vous sur ce que les utilisateurs peuvent faire. Ne vous contentez pas de répéter le nom de l’élément du panneau de configuration ou même de l’utiliser dans la description.
-   **Être spécifiques.** Évitez les verbes génériques et les expressions Catch-All comme et autre matériel. Si les informations sont importantes, répertoriez-les en particulier. dans le cas contraire, partez du principe que les utilisateurs comprennent que tous les éléments ne sont pas listés dans le info-bulles.

    **Incorrect :**

    ![capture d’écran de l’info-bulle : configure votre souris ](images/ctrl-tooltips-and-infotips-image41.png)

    **Correct :**

    ![capture d’écran de l’info-bulle détaillée pour les paramètres de la souris ](images/ctrl-tooltips-and-infotips-image42.png)

    Dans l’exemple approprié, les types de matériel configurés sont répertoriés spécifiquement.

-   **Soyez concis.** Utilisez 25 mots ou moins. Plus de info-bulles découragent la lecture.
-   **Commencez avec un verbe impératif actuel.**

    **Correct :**

    Configurez les paramètres d’affichage et de connexion Internet.

    Ajustez les paramètres pour la vision, l’audition et la mobilité.

-   **Accédez directement au point.** N’utilisez pas de langue qui s’applique à un panneau de configuration, comme « utiliser pour afficher et configurer les paramètres de l’apparence et des fonctionnalités de votre... » ou « fournit des options pour vous... »
-   N’utilisez pas la langue qui semble marketing.

    **Incorrect :**

    Votre point de départ unique pour tous vos besoins en matière de configuration de disque.

-   Étant donné que ces info-bulles sont indexés pour la zone de recherche du panneau de configuration, **Décrivez les éléments à l’aide des termes pour lesquels les utilisateurs sont les plus susceptibles d’effectuer des recherches.** Envisagez d’utiliser des synonymes communs pour les tâches et les objets populaires.

    ![capture d’écran de l’info-bulle avec les tâches du contrôleur de jeu ](images/ctrl-tooltips-and-infotips-image43.png)

    Dans cet exemple, l’élément est décrit à l’aide de termes pour lesquels les utilisateurs sont le plus susceptibles d’effectuer des recherches.

-   Si un élément du panneau de configuration est susceptible d’être confondu avec d’autres personnes, expliquez comment il est différent dans l’info-bulle.

    **Incorrect :**

    ![capture d’écran de l’info-bulle absente de détails spécifiques ](images/ctrl-tooltips-and-infotips-image44.png)

    Dans cet exemple, les deux éléments du panneau de configuration configurent le son, mais l’info-bulle ne clarifie pas la différence.

    **Correct :**

    ![capture d’écran de l’info-bulle avec des détails spécifiques ](images/ctrl-tooltips-and-infotips-image45.png)

    Dans cet exemple, la différence entre les deux éléments est plus évidente en raison du Conseil.

### <a name="icons"></a>Icônes

contrairement aux versions précédentes de Windows, Windows Vista permet d’avoir des icônes.

-   Pour les info-bulles, n’utilisez pas d’icônes.
-   Pour info-bulles, utilisez les icônes uniquement si elles facilitent la reconnaissance ou la compréhension, ou fournissent un contexte. La plupart des info-bulles ne doivent pas avoir d’icônes.

    ![capture d’écran d’une info-bulle de volume avec icône de casque ](images/ctrl-tooltips-and-infotips-image46.png)

    Dans cet exemple, l’info-bulle a une icône pour aider à associer l’icône à sa signification.

-   L’icône doit utiliser le [style Aero](vis-icons.md) et présenter une apparence discrète.

Pour obtenir des instructions générales et des exemples, consultez [icônes](vis-icons.md).

## <a name="documentation"></a>Documentation

Lorsque vous faites référence à des conseils :

-   En programmation et dans d’autres documents techniques, reportez-vous au type de Conseil (info-bulle ou info-bulle). Partout ailleurs, il vous suffit d’appeler un Conseil.
-   Les variations suivantes sont incorrectes : info-bulle, info-bulle et info-bulle.
-   Pour décrire l’interaction de l’utilisateur, utilisez Hover.

