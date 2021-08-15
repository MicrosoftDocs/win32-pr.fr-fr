---
title: Barres d'outils
description: Les barres d’outils sont un moyen de regrouper les commandes pour un accès efficace.
ms.assetid: 8f36307c-54fc-493d-a2ff-57db29e3508d
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 8015e1dec17ad524645b474b21d42af9269ffbc8d24279c56612620f0e4bb615
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118450035"
---
# <a name="toolbars"></a>Barres d'outils

> [!NOTE]
> ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Les barres d’outils sont un moyen de regrouper les commandes pour un accès efficace.

![capture d’écran de deux barres d’outils avec des éléments étiquetés ](images/cmd-toolbars-image1.png)

Certaines barres d’outils typiques.

**Utilisez les barres d’outils en plus ou à la place des barres de menus.** Les barres d’outils peuvent être plus efficaces que les barres de menus, car elles sont directes (toujours affichées au lieu d’être affichées au clic de la souris), immédiate (au lieu de demander une entrée supplémentaire) et contiennent les commandes les plus fréquemment utilisées (au lieu d’une liste complète). Contrairement aux barres de menus, les barres d’outils ne doivent pas nécessairement être complètes ou explicites, mais aussi rapides, pratiques et efficaces.

Certaines barres d’outils sont personnalisables, ce qui permet aux utilisateurs d’ajouter ou de supprimer des barres d’outils, de modifier leur taille et leur emplacement, et même de modifier leur contenu. Certains types de barres d’outils peuvent être désancrés, ce qui se traduit par une fenêtre de palette. Pour plus d’informations sur les variétés de barres d’outils, consultez [modèles d’utilisation](#usage-patterns) dans cet article.

> [!Note]  
> Les instructions relatives aux [menus](cmd-menus.md), aux [boutons de commande](ctrl-command-buttons.md)et aux [icônes](vis-icons.md) sont présentées dans des articles distincts.

 

## <a name="is-this-the-right-user-interface"></a>S’agit-il de l’interface utilisateur appropriée ?

Pour vous décider, posez-vous les questions suivantes :

-   **La fenêtre est-elle une fenêtre principale ?** Les barres d’outils fonctionnent bien pour les fenêtres principales, mais elles sont généralement insurmontables pour les fenêtres secondaires. Pour les fenêtres secondaires, utilisez à la place des [boutons de commande](ctrl-command-buttons.md), des [boutons de menu](ctrl-command-buttons.md)et [des liens](ctrl-command-links.md) .
-   **Existe-t-il un petit nombre de commandes fréquemment utilisées ?** Les barres d’outils ne peuvent pas gérer autant de commandes que les barres de menus. elles fonctionnent donc mieux pour accéder efficacement à un petit nombre de commandes fréquemment utilisées.
-   **La plupart des commandes sont-elles immédiates ?** Autrement dit, s’agit-il essentiellement de commandes qui ne nécessitent pas d’entrée supplémentaire ? Pour être efficace, les barres d’outils doivent avoir une apparence directe et immédiate. Si ce n’est pas le cas, les barres de menus sont mieux adaptées aux commandes qui nécessitent une entrée supplémentaire.
-   **La plupart des commandes peuvent-elles être présentées directement ?** Autrement dit, les utilisateurs interagissent avec eux à l’aide d’un simple clic. Bien que certaines commandes puissent être présentées à l’aide de boutons de menu, la présentation de la plupart des commandes de cette façon permet de défaire l’efficacité de la barre d’outils et de faire de la barre de menus un meilleur choix.
-   **Les commandes sont-elles bien représentées par des icônes ?** Les boutons de la barre d’outils sont généralement représentés par des icônes plutôt que par des étiquettes de texte (bien que certains boutons de la barre d’outils utilisent les deux), tandis que les commandes de menu sont représentées par Si les icônes de commande ne sont pas de qualité supérieure et ne sont pas explicites, une barre de menus peut être un meilleur choix.

Si votre programme comporte une barre d’outils sans barre de menus et que la plupart des commandes sont accessibles indirectement par le biais de boutons de menu et de [boutons partagés](ctrl-command-buttons.md), cette barre d’outils est essentiellement une barre de menus. Appliquez plutôt le modèle menus de la [barre d’outils](cmd-menus.md) dans les menus instructions.

## <a name="design-concepts"></a>Principes de conception

Une bonne barre de menus est un catalogue complet de toutes les commandes de niveau supérieur disponibles, tandis qu’une bonne barre d’outils offre un accès rapide et pratique aux commandes fréquemment utilisées. Une barre d’outils ne tente pas de former les utilisateurs à les rendre plus productifs. Une fois que les utilisateurs apprennent à accéder à une commande dans une barre d’outils, ils continuent rarement à accéder à la commande à partir de la barre de menus. Pour ces raisons, la barre de menus d’un programme et sa barre d’outils n’ont pas besoin de correspondre directement.

### <a name="toolbars-vs-menu-bars"></a>Barres d’outils et barres de menus

En règle générale, les barres d’outils sont différentes des barres de menus des manières suivantes :

-   **Argument.** Les barres d’outils présentent uniquement les commandes les plus fréquemment utilisées, tandis que les barres de menus cataloguent toutes les commandes de niveau supérieur disponibles au sein d’un programme.
-   **Immédiat.** Le fait de cliquer sur une commande de barre d’outils prend effet immédiatement, alors qu’une commande de menu peut nécessiter une entrée supplémentaire. Par exemple, une commande Imprimer dans une barre de menus affiche d’abord la boîte de dialogue Imprimer, tandis qu’un bouton imprimer de la barre d’outils imprime immédiatement une seule copie d’un document sur l’imprimante par défaut.

    ![capture d’écran du bouton d’impression de la barre d’outils sélectionné ](images/cmd-toolbars-image2.png)

    Dans cet exemple, en cliquant sur le bouton imprimer de la barre d’outils, vous imprimez immédiatement une seule copie d’un document sur l’imprimante par défaut.

-   **Direction.** Les commandes de barre d’outils sont appelées en un seul clic, tandis que les commandes de barre de menus requièrent la navigation dans le menu.
-   **Nombre et densité.** L’espace d’écran requis par une barre d’outils est proportionnel au nombre de ses commandes et cet espace est toujours utilisé, même si les commandes ne le sont pas. Par conséquent, les barres d’outils doivent utiliser efficacement leur espace. En revanche, les commandes de la barre de menus sont normalement masquées dans la vue et leur structure hiérarchique autorise un nombre quelconque de commandes.
-   **Taille et présentation.** Pour compresser de nombreuses commandes dans un petit espace, les barres d’outils utilisent généralement des commandes basées sur des icônes (avec des étiquettes basées sur des info-bulles), tandis que les barres de menus utilisent des commandes textuelles (avec des icônes facultatives). Alors que les boutons de barre d’outils peuvent avoir des étiquettes de texte standard, ils utilisent beaucoup plus d’espace.

    ![capture d’écran de la barre d’outils avec l’étiquette d’envoi/réception ](images/cmd-toolbars-image3.png)

    Les boutons de barre d’outils étiquetés prennent au moins trois fois plus d’espace que ceux sans étiquette.

-   **Explicite.** Les barres d’outils bien conçues ont besoin d’icônes qui sont généralement explicites, car les utilisateurs ne peuvent pas trouver efficacement des commandes simplement à l’aide d’info-bulles. Toutefois, les barres d’outils fonctionnent toujours bien si quelques commandes moins fréquemment utilisées ne sont pas explicites.

    ![capture d’écran de la barre d’outils avec des icônes familières ](images/cmd-toolbars-image4.png)

    Dans cet exemple, les icônes les plus fréquemment utilisées sont explicites.

-   **Reconnaître et distinguer.** Pour les commandes fréquemment utilisées, les utilisateurs se souviennent des attributs de bouton de barre d’outils tels que l’emplacement, la forme et la couleur. Avec les barres d’outils bien conçues, les utilisateurs peuvent trouver rapidement les commandes même si elles ne se souviennent pas du symbole d’icône exact. En revanche, les utilisateurs mémorisent les emplacements de commandes de barre de menus fréquemment utilisés, mais s’appuient sur les étiquettes de commande pour effectuer des sélections.

    ![capture d’écran de la boîte de dialogue Options de l’outil capture ](images/cmd-toolbars-image5.png)

    Pour les commandes de barre d’outils, les options emplacement distinctif, forme et couleur permettent de rendre les icônes identifiables et différenciables.

    ![capture d’écran de la barre de menus avec la commande de fichier sélectionnée ](images/cmd-toolbars-image6.png)

    Pour les commandes de la barre de menus, les utilisateurs dépendent en fin de leurs étiquettes.

### <a name="efficiency"></a>Efficacité

Étant donné leurs caractéristiques, les barres d’outils doivent être conçues principalement pour améliorer l’efficacité. Une barre d’outils inefficace n’est pas tout à fait pertinente.

**Si vous n’avez qu’une seule chose...**

Assurez-vous que vos barres d’outils sont conçues principalement pour des performances optimales. Les barres d’outils de focus sur les commandes fréquemment utilisées, immédiates, directes et rapidement reconnaissables.

### <a name="hiding-menu-bars"></a>Masquer les barres de menus

En règle générale, les barres d’outils fonctionnent correctement avec les barres de menus : les bonnes barres d’outils offrent une efficacité et de bonnes barres de menus fournissent une exhaustivité. **Le fait d’avoir à la fois des barres de menus et des barres d’outils permet de se concentrer sur ses points forts sans compromis.**

Étonnamment, ce modèle s’arrête avec des programmes simples. Pour les programmes avec seulement quelques commandes, il n’est pas judicieux d’avoir à la fois une barre de menus et une barre d’outils, car la barre de menus finit par être une version non efficace et redondante de la barre d’outils.

pour éliminer cette redondance, de nombreux programmes simples dans Windows Vista se concentrent sur la fourniture de commandes uniquement via la barre d’outils et le masquage de la barre de menus par défaut. ces programmes incluent Windows explorer, Windows Internet explorer, Lecteur Windows Media et Windows galerie de photos.

Il ne s’agit pas d’une modification minime. La suppression de la barre de menus modifie fondamentalement la nature des barres d’outils, car celles-ci doivent être complètes et peuvent être modifiées de la manière suivante :

-   **Argument.** La suppression de la barre de menus signifie que toutes les commandes qui ne sont pas directement disponibles à partir d’une fenêtre ou de ses menus contextuels doivent être accessibles à partir de la barre d’outils, quelle que soit leur fréquence d’utilisation.
-   **Immédiat.** La suppression de la barre de menus fait de la barre d’outils le seul point d’accès visible pour les commandes, ce qui nécessite que la barre d’outils ait les versions entièrement fonctionnelles. Par exemple, s’il n’y a pas de barre de menus, une commande imprimer sur une barre d’outils doit afficher la boîte de dialogue Imprimer au lieu de l’imprimer immédiatement. (Bien que l’utilisation d’un bouton partagé soit un excellent compromis dans ce cas. Consultez [menu standard et boutons de fractionnement](#standard-menu-and-split-buttons) pour le bouton standard imprimer le fractionnement.)

    ![capture d’écran des options de la barre d’outils et de la commande d’impression ](images/cmd-toolbars-image7.png)

    dans cet exemple, le bouton d’impression de la barre d’outils de Windows galerie Photo contient une commande imprimer qui affiche la boîte de dialogue imprimer.

-   **Direction.** Pour économiser de l’espace et éviter tout encombrement, les commandes moins fréquemment utilisées peuvent être déplacées vers des boutons de menu, ce qui les rend moins directs.

Les barres d’outils utilisées pour compléter une barre de menus sont conçues différemment des barres d’outils conçues pour être utilisées avec une barre de menus supprimée ou masquée. Et étant donné que vous ne pouvez pas supposer que les utilisateurs affichent une barre de menus masquée pour exécuter une seule commande, le masquage d’une barre de menus doit être traité de la même façon que la suppression complète de la conception. (Si vous masquez la barre de menus par défaut, ne partez pas du principe que les utilisateurs pensent afficher la barre de menus pour rechercher une commande, voire déterminer comment l’afficher.)

La conception d’une barre d’outils pour travailler sans barre de menus implique souvent des compromis. Mais pour des performances optimales, ne vous inquiétez pas trop. Si le masquage de la barre de menus aboutit à une barre d’outils inefficace, ne masquez pas la barre de menus !

### <a name="keyboard-accessibility"></a>Accessibilité du clavier

À partir du clavier, l’accès aux barres d’outils est très différent de celui des barres de menus. Les barres de menus reçoivent le focus d’entrée lorsque les utilisateurs appuient sur la touche Alt et perdent le focus d’entrée avec la touche ÉCHAP. Une fois qu’une barre de menus a le focus d’entrée, elle est désélectionnée indépendamment du reste de la fenêtre, en gérant toutes les touches de direction, le début, la fin et les touches de tabulation. En revanche, les barres d’outils reçoivent le focus d’entrée lorsque les utilisateurs appuient sur la touche TAB dans tout le contenu de la fenêtre. Étant donné que les barres d’outils sont en dernier dans l’ordre de tabulation, elles peuvent nécessiter un effort important pour les activer sur une page occupée (sauf si les utilisateurs savent utiliser Maj + Tab pour revenir en arrière).

L’accessibilité présente un dilemme ici : alors que les barres d’outils sont plus faciles pour les utilisateurs de la souris, elles sont moins accessibles aux utilisateurs du clavier. Ce n’est pas un problème si une barre de menus et une barre d’outils sont à la fois, mais si la barre de menus est supprimée ou masquée.

Pour des raisons d’accessibilité, il est préférable de conserver la barre de menus au lieu de la supprimer complètement en faveur d’une barre d’outils. Si vous devez choisir entre supprimer la barre de menus et la simplement masquer, préférez la masquer.

## <a name="usage-patterns"></a>Modèles d’usage

Les barres d’outils ont plusieurs modèles d’utilisation :



|     Usage                                                                                                                 |     Exemple                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Barres d’outils principales**<br/> barre d’outils conçue pour fonctionner sans barre de menus, masquée ou supprimée. <br/> | les barres d’outils principales doivent équilibrer la nécessité d’une efficacité optimale, afin qu’elles fonctionnent mieux pour les programmes simples. <br/> ![capture d’écran de la barre d’outils de l’Explorateur Windows ](images/cmd-toolbars-image8.png)<br/> barre d’outils principale de l’explorateur de Windows.<br/>                                                                        |
| **Barres d’outils supplémentaires**<br/> barre d’outils conçue pour fonctionner avec une barre de menus. <br/>                         | les barres d’outils supplémentaires peuvent se concentrer sur l’efficacité sans compromis. <br/> ![capture d’écran d’une barre de menus sur une barre d’outils ](images/cmd-toolbars-image9.png)<br/> une barre d’outils supplémentaire de Windows Movie Maker.<br/>                                                                                                                  |
| **Menus de la barre d’outils**<br/> barre de menus implémentée en tant que barre d’outils. <br/>                                        | les menus de la barre d’outils sont des barres d’outils constituées principalement de commandes dans les [boutons de menu](ctrl-command-buttons.md) et les boutons partagés, avec seulement quelques commandes directes, le cas échéant. <br/> ![capture d’écran de la barre de menus avec des icônes et des commandes ](images/cmd-toolbars-image10.png)<br/> menu de la barre d’outils de Windows galerie de photos.<br/> |
| **Barres d’outils personnalisables**<br/> barre d’outils qui peut être personnalisée par les utilisateurs. <br/>                          | les barres d’outils personnalisables permettent aux utilisateurs d’ajouter ou de supprimer des barres d’outils, de modifier leur taille et leur emplacement, et même de modifier leur contenu. <br/> ![capture d’écran d’une barre d’outils avec des dizaines d’icônes ](images/cmd-toolbars-image11.png)<br/> Barre d’outils personnalisable à partir de Microsoft Visual Studio.<br/>                                             |
| **Fenêtres de palette**<br/> boîte de dialogue non modale qui présente un tableau de commandes. <br/>                 | les fenêtres de palette sont des barres d’outils non ancrées. <br/> ![capture d’écran de la boîte de dialogue couleurs ](images/cmd-toolbars-image12.png)<br/> ![capture d’écran d’une boîte de dialogue de polices ](images/cmd-toolbars-image13.png)<br/> fenêtres de Palette à partir de Windows Paint.<br/>                                                                             |



 

Les barres d’outils ont les styles suivants :



|   Style                                                                                                                                     |  Exemple                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Icônes sans étiquette**<br/> une ou plusieurs lignes de petits boutons d’icône sans étiquette. <br/>                                           | Utilisez ce style si le nombre de boutons à étiqueter est trop important ou si le programme est fréquemment utilisé. avec ce style, les programmes avec des fonctionnalités complexes peuvent avoir plusieurs lignes et, par conséquent, il s’agit du seul style qui doit être personnalisable. avec ce style, certains boutons de commande peuvent être étiquetés s’ils sont fréquemment utilisés. <br/> ![capture d’écran de la barre d’outils avec petites icônes sans étiquette ](images/cmd-toolbars-image14.png)<br/> Barre d’outils d’icônes sans étiquette de WordPad.<br/> |
| **Grandes icônes sans étiquette**<br/> une seule ligne de boutons de grande icône sans étiquette. <br/>                                         | Utilisez ce style pour les utilitaires simples qui ont des icônes facilement identifiables et qui sont généralement exécutés dans des fenêtres de petite taille. <br/> ![capture d’écran de la barre d’outils avec grandes icônes sans étiquette ](images/cmd-toolbars-image15.png)<br/> ![capture d’écran de la barre d’outils avec de grandes icônes ](images/cmd-toolbars-image16.png)<br/> les barres d’outils grandes icônes sans étiquette de Windows Live Messenger et Windows outil capture.<br/>                                                                       |
| **Icônes étiquetées**<br/> une seule ligne de petites icônes étiquetées. <br/>                                                          | Utilisez ce style s’il y a peu de commandes ou si le programme n’est pas fréquemment utilisé. ce style a toujours une seule ligne. <br/> ![capture d’écran de la barre d’outils avec les icônes étiquetées ](images/cmd-toolbars-image8.png)<br/> barre d’outils d’icônes étiquetées à partir de Windows Explorer.<br/>                                                                                                                                                                                                               |
| **Barres d’outils partielles**<br/> ligne partielle de petites icônes permettant d’économiser de l’espace quand une barre d’outils complète n’est pas nécessaire. <br/>       | Utilisez ce style pour les fenêtres avec des boutons de navigation, une zone de recherche ou des onglets pour éliminer le poids inutile en haut de la fenêtre. <br/> ![capture d’écran de la barre de menus, barre d’outils et barre des favoris ](images/cmd-toolbars-image17.png)<br/> Les barres d’outils partielles peuvent être associées à des boutons de navigation, à une zone de recherche ou à des onglets.<br/>                                                                                                                                                  |
| **Grandes barres d’outils partielles**<br/> ligne partielle de grandes icônes utilisée pour économiser de l’espace quand une barre d’outils complète n’est pas nécessaire. <br/> | Utilisez ce style pour les utilitaires simples qui ont des boutons de navigation ou une zone de recherche pour éliminer le poids inutile en haut de la fenêtre. <br/> ![capture d’écran d’une grande barre d’outils partielle ](images/cmd-toolbars-image18.png)<br/> Barre d’outils partielle importante de Windows Defender.<br/>                                                                                                                                                                                         |



 

Enfin, les contrôles ToolBar ont plusieurs modèles d’utilisation :



|     Usage                                                                                                                 |     Exemple                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Boutons d’icône de commande**<br/> Lorsque vous cliquez sur un bouton de commande, une action immédiate est lancée. <br/>                                                                                                 | ![capture d’écran d’une barre d’outils d’icônes étiquetées ](images/cmd-toolbars-image19.png)<br/> exemples de boutons de commande d’icône de Windows télécopie et numérisation.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Boutons d’icône de mode**<br/> Cliquer sur un bouton mode active le mode sélectionné. <br/>                                                                                                            | ![capture d’écran d’une barre d’outils verticale ](images/cmd-toolbars-image20.png)<br/> exemples de boutons de mode de Windows Paint.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Boutons d’icône de propriété**<br/> l’état d’un bouton de propriété reflète l’état des objets actuellement sélectionnés, le cas échéant. Cliquer sur le bouton applique la modification aux objets sélectionnés. <br/> | ![capture d’écran des icônes de mise en forme et du texte sélectionné ](images/cmd-toolbars-image21.png)<br/> Exemples de boutons de propriété de Microsoft Word.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Boutons d’icônes étiquetés**<br/> un bouton de commande ou un bouton de propriété intitulé avec une icône et une étiquette de texte. <br/>                                                                               | Ces boutons sont utilisés pour les boutons de barre d’outils fréquemment utilisés dont l’icône n’est pas suffisamment explicite. ils sont également utilisés dans les barres d’outils qui contiennent autant de boutons que chaque bouton peut avoir une étiquette de texte. <br/> ![Capture d’écran qui affiche la barre d’outils avec des icônes étiquetées pour les boutons les plus fréquemment utilisés. ](images/cmd-toolbars-image22.png)<br/> Une barre d’outils avec ses boutons les plus fréquemment utilisés, étiquetés.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Boutons de menu**<br/> bouton de commande utilisé pour présenter un petit ensemble de commandes associées. <br/>                                                                                                | un triangle pointant vers le bas indique que lorsque vous cliquez sur le bouton, un menu s’affiche. <br/> ![capture d’écran de la barre d’outils et de la liste de commandes déroulante ](images/cmd-toolbars-image23.png)<br/> Bouton de menu avec un petit ensemble de commandes associées.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Boutons partagés**<br/> bouton de commande utilisé pour consolider les variations d’une commande, en particulier lorsque l’une des commandes est utilisée la plupart du temps. <br/>                                     | ![capture d’écran du bouton fractionner l’impression ](images/cmd-toolbars-image24.png)<br/> bouton partagé dans son état normal.<br/> comme un bouton de menu, un seul triangle pointant vers le bas indique que cliquer sur la partie la plus à droite du bouton affiche un menu. <br/> ![capture d’écran des commandes du bouton fractionner l’impression ](images/cmd-toolbars-image25.png)<br/> bouton partagé en baisse.<br/> dans cet exemple, un bouton partagé est utilisé pour regrouper toutes les commandes liées à l’impression. la commande d’impression immédiate est utilisée la plupart du temps, de sorte que les utilisateurs n’ont généralement pas besoin de voir les autres commandes. <br/> Contrairement à un bouton de menu, le fait de cliquer sur la partie gauche du bouton effectue l’action directement sur l’étiquette. les boutons fractionnés sont efficaces dans les situations où la commande suivante est susceptible d’être la même que la dernière commande. dans ce cas, l’étiquette est remplacée par la dernière commande, comme avec un sélecteur de couleurs :<br/> ![capture d’écran de l’icône de compartiment pour la peinture ](images/cmd-toolbars-image26.png)<br/> Dans cet exemple, l’étiquette est remplacée par la dernière commande.<br/> |
| **Listes déroulantes**<br/> liste déroulante (modifiable ou en lecture seule) utilisée pour afficher ou modifier une propriété. <br/>                                                                                   | ![capture d’écran de la liste déroulante des polices ](images/cmd-toolbars-image27.png)<br/> Dans cet exemple, les listes déroulantes sont utilisées pour afficher et définir des attributs de police.<br/> Une liste déroulante dans une barre d’outils reflète l’état de l’objet actuellement sélectionné, le cas échéant. La modification de la liste modifie l’état de l’objet sélectionné. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="guidelines"></a>Consignes

### <a name="presentation"></a>Présentation

-   **Choisissez un style de barre d’outils approprié en fonction du nombre de commandes et de leur utilisation.** Consultez le tableau style de barre d’outils précédent pour obtenir des conseils sur la façon de choisir. Évitez d’utiliser une configuration de barre d’outils qui prend trop d’espace dans la zone de travail du programme.
-   **Placez les barres d’outils juste au-dessus de la zone de contenu,** sous la barre de menus et la barre d’adresses, le cas échéant.
-   **Si de l’espace est au niveau Premium, économisez de l’espace en :**

    -   Omission des étiquettes des icônes connues et des commandes moins fréquemment utilisées.
    -   En utilisant uniquement une barre d’outils partielle au lieu de l’intégralité de la largeur de la fenêtre.
    -   Consolider les commandes associées avec un bouton de menu ou un bouton partagé.
    -   Utilisation d’un [Chevron de dépassement](glossary.md) pour révéler les commandes moins fréquemment utilisées.
    -   Affichage des commandes uniquement lorsqu’elles s’appliquent au contexte actuel.

    ![capture d’écran des icônes courantes de la barre d’outils non étiquetées ](images/cmd-toolbars-image28.png)

    le Windows barre d’outils Internet Explorer économise de l’espace en omettant les étiquettes des icônes connues, à l’aide d’une barre d’outils partielle et en utilisant un chevron de dépassement pour les commandes moins fréquemment utilisées.

-   **Pour le modèle de barre d’outils icônes non étiquetées, utilisez une configuration par défaut qui ne comporte pas plus de deux lignes de barres d’outils.** Si plus de deux lignes peuvent être utiles, rendez les barres d’outils personnalisables. Le démarrage de plus de deux lignes peut saturer les utilisateurs et prendre trop d’espace à partir de la zone de travail du programme.

    **Incorrect :**

    ![capture d’écran de la barre de menus et trois lignes de barres d’outils ](images/cmd-toolbars-image29.png)

    Une configuration par défaut avec plus de deux lignes de barres d’outils entraîne un trop grand encombrement visuel.

-   **Désactivez les boutons de barre d’outils individuels qui ne s’appliquent pas au contexte actuel** au lieu de les supprimer. Cela rend le contenu de la barre d’outils stable et plus facile à trouver.
-   **Désactiver les boutons de la barre d’outils individuels en cas de clic sur ceux-ci entraînerait une erreur.** Cela est nécessaire pour maintenir une sensation directe.
-   **Pour le modèle de barre d’outils icônes non étiquetées, supprimez les barres d’outils entières si elles ne s’appliquent pas au contexte actuel.** Affichez-les uniquement dans les modes applicables.

    ![capture d’écran de la barre d’outils de débogage ](images/cmd-toolbars-image30.png)

    Dans cet exemple, la barre d’outils de débogage s’affiche uniquement lorsque le programme est en cours d’exécution.

-   **Afficher les boutons de barre d’outils alignés à gauche.** L’icône d’aide, si elle est présente, est alignée à droite.

    ![capture d’écran de la barre d’outils, icône d’aide alignée à droite ](images/cmd-toolbars-image31.png)

    Tous les boutons de barre d’outils sont alignés à gauche, à l’exception de l’aide.

    **Exception :** Windows barres d’outils de style 7 aligner à gauche les commandes spécifiques au programme, mais aligner à droite les commandes standard et connues, telles que les Options, les affichages et l’aide.

-   **Ne modifiez pas dynamiquement les étiquettes de boutons de barre d’outils.** Cela est confus et inattendu. Toutefois, vous pouvez modifier l’icône pour refléter l’état actuel.

    ![capture d’écran de l’icône de compartiment pour la peinture ](images/cmd-toolbars-image26.png)

    Dans cet exemple, l’icône est modifiée pour indiquer la commande par défaut.

### <a name="controls-and-commands"></a>Contrôles et commandes

-   **Préférez les commandes les plus fréquemment utilisées.**
    -   **Pour les barres d’outils principales, fournissez des commandes complètes.** Les barres d’outils principales n’ont pas besoin d’être aussi complètes que les barres de menus, mais elles doivent fournir toutes les commandes qui ne sont pas facilement détectables ailleurs. Les barres d’outils principales n’ont pas besoin de commandes pour :
        -   Commandes qui sont directement sur l’interface utilisateur.
        -   Commandes généralement accessibles via les menus contextuels.
        -   Commandes standard et connues comme couper, copier et coller.
    -   **Pour les barres d’outils supplémentaires, fournissez les commandes qui sont les plus fréquemment utilisées.** Les commandes de la barre de menus sont un sur-ensemble des commandes de la barre d’outils. vous n’avez donc pas à fournir tout. Concentrez-vous sur l’accès aux commandes rapides et pratiques et ignorez le reste.
-   **Préférer les contrôles directs.** Utilisez les boutons de la barre d’outils dans l’ordre de préférence suivant :
    -   **Bouton d’icône.** Direct et occupe un espace minimal.
    -   **Bouton d’icône étiqueté.** Direct, mais prend plus d’espace.
    -   **Bouton partagé.** Directe pour la commande la plus courante, mais gère les variations de commande.
    -   **Bouton de menu.** Indirect, mais présente de nombreuses commandes.
-   **Préférer les commandes immédiates.** Pour les commandes qui peuvent être immédiats ou avoir une entrée supplémentaire pour plus de flexibilité :
    -   Pour les barres d’outils principales, utilisez les versions flexibles des commandes (telles que Print...).
    -   Pour les barres d’outils supplémentaires, utilisez les versions immédiates de la barre d’outils (par exemple, imprimer) et utilisez des versions flexibles dans la barre de menus (telle que imprimer...).
-   **Fournissez des étiquettes pour les commandes fréquemment utilisées, en** particulier si leurs icônes ne sont pas connues.

    **Acceptable:**

    ![capture d’écran de la barre d’outils sans icône nommée ](images/cmd-toolbars-image32.png)

    **Conseillé**

    ![capture d’écran de la barre d’outils avec certaines icônes étiquetées ](images/cmd-toolbars-image33.png)

    la barre d’outils Windows télécopie et analyse comporte peu de commandes, donc la meilleure version libelle les plus importantes.

-   Ne placez pas de commandes dans les menus de la barre d’outils qui se trouvent également directement dans la barre d’outils.

    **Incorrect :**

    ![capture d’écran de la commande imprimer sur la barre d’outils et le menu ](images/cmd-toolbars-image34.png)

    Dans cet exemple, Print est directement sur la barre d’outils. il n’est donc pas nécessaire de le faire dans le menu.

### <a name="organization-and-order"></a>Organisation et ordre

-   **Organisez les commandes dans une barre d’outils en groupes associés.**
-   **Commencez par placer les groupes les plus fréquemment utilisés. Dans un groupe, placez les commandes dans leur ordre logique.** Globalement, les commandes doivent avoir un flot logique pour faciliter leur recherche, tout en continuant d’afficher les commandes les plus fréquemment utilisées. Cela est plus efficace, en particulier en cas de dépassement de capacité.
-   **Utilisez les diviseurs de groupe uniquement si les commandes entre les groupes sont faiblement couplées.** Cela rend les regroupements évidents et les commandes plus faciles à trouver.

    ![Capture d’écran montrant une barre d’outils avec des icônes bien organisées utilisant des diviseurs de groupe.](images/cmd-toolbars-image35.png)

    ![capture d’écran de la barre d’outils avec des icônes bien organisées ](images/cmd-toolbars-image36.png)

    exemples de barres d’outils groupées à partir de Windows Mail.

-   **Évitez de placer des commandes destructrices à côté des commandes fréquemment utilisées.** Utilisez l’ordre ou le regroupement pour bénéficier de la séparation. En outre, envisagez de ne pas placer de commandes destructrices dans la barre d’outils, mais uniquement dans la barre de menus ou les menus contextuels.

    **Acceptable:**

    ![capture d’écran des boutons d’impression et de suppression adjacents ](images/cmd-toolbars-image37.png)

    **Conseillé**

    ![capture d’écran des boutons imprimer et supprimer séparés ](images/cmd-toolbars-image38.png)

    Dans un meilleur exemple, la commande Delete est physiquement séparée de Print.

-   **Utilisez le chevron de dépassement pour indiquer que toutes les commandes ne peuvent pas être affichées.** Toutefois, utilisez le dépassement de capacité uniquement si l’espace est insuffisant pour afficher toutes les commandes.

    **Incorrect :**

    ![capture d’écran du volet des favoris et des commandes masquées ](images/cmd-toolbars-image39.png)

    Le chevron de dépassement indique que toutes les commandes ne sont pas affichées, mais qu’il peut en être de plus avec une meilleure disposition.

-   **Assurez-vous que les commandes les plus fréquemment utilisées sont directement accessibles à partir de la barre d’outils (autrement dit, pas en débordement) dans de petites tailles de fenêtre.** Si nécessaire, réorganisez les commandes, déplacez les commandes moins fréquemment utilisées sur les boutons de menu ou les boutons partagés, ou même supprimez-les complètement de la barre d’outils. Si ce problème persiste, reconsidérez votre choix de style de barre d’outils.

### <a name="hiding-menu-bars"></a>Masquer les barres de menus

En règle générale, les barres d’outils fonctionnent bien avec les barres de menus, car elles permettent chacune de se concentrer sur leurs points forts sans compromis.

-   Masque la barre de menus par défaut si la barre de menus est redondante.
-   Masquez la barre de menus au lieu de la supprimer complètement, car les barres de menus sont plus accessibles aux utilisateurs du clavier.
-   Pour restaurer la barre de menus, fournissez une option de coche de barre de menus dans la catégorie de menu vue (pour les barres d’outils principales) ou outils (pour les barres d’outils secondaires). Pour plus d’informations, consultez [menu standard et boutons partagés](#standard-menu-and-split-buttons).
-   Affiche la barre de menus lorsque les utilisateurs appuient sur la touche Alt et définissent le focus d’entrée sur la première catégorie de menu.

### <a name="interaction"></a>Interaction

-   Au survol, affichez le [bouton offre](glossary.md) pour indiquer que l’icône est cliquable. Après le délai d’expiration des info-bulles, affichez l’info-bulle ou l’info-bulle.

    ![capture d’écran d’une info-bulle décrivant un bouton ](images/cmd-toolbars-image40.png)

    Cet exemple montre les différents États d’affichage.

-   Sur un simple clic gauche :
    -   Pour les boutons de commande, interagissez avec le contrôle comme d’habitude.
    -   Pour les boutons de mode, affichez le contrôle pour refléter le mode actuellement sélectionné. Si le mode affecte le comportement de l’interaction avec la souris, modifiez également le pointeur.

        ![capture d’écran d’un pointeur mis en forme comme un pot de peinture ](images/cmd-toolbars-image41.png)

        Dans cet exemple, le pointeur est modifié pour afficher le mode d’interaction avec la souris.

    -   Pour les boutons de propriété et les listes déroulantes, affichez le contrôle pour refléter l’état des objets actuellement sélectionnés, le cas échéant. Sur interaction, mettez à jour l’état du contrôle et appliquez la modification aux objets sélectionnés. Si rien n’est sélectionné, ne rien faire.

-   Dans le double-clic gauche, effectuez la même action qu’un simple clic gauche.
    -   **Exception :** Dans de rares occasions, une commande de barre d’outils peut être utilisée de manière plus efficace. Dans ce cas, utilisez le double-clic pour basculer le mode.

        ![capture d’écran de l’info-bulle montrant les fonctions du bouton ](images/cmd-toolbars-image42.png)

        Dans cet exemple, le double-clic sur la commande reproduire la mise en forme passe à un mode dans lequel tous les clics suivants appliquent le format. Les utilisateurs peuvent laisser le mode en un clic droit.

-   Cliquez avec le bouton droit sur :
    -   Pour les barres d’outils personnalisables, affichez le menu contextuel pour personnaliser la barre d’outils. Affichez le menu en cliquant avec le bouton droit sur souris enfoncé, et non pas sur la souris.
    -   Pour les autres barres d’outils, ne rien faire.

### <a name="icons"></a>Icônes

-   **Fournissez des icônes pour tous les contrôles ToolBar, à l’exception des listes déroulantes.**

    ![capture d’écran de la liste déroulante de taille de police ](images/cmd-toolbars-image43.png)

    Les listes déroulantes n’ont pas besoin d’icônes, contrairement à tous les autres contrôles ToolBar.

    **Exception :** Windows les barres d’outils de style 7 utilisent des icônes uniquement pour les commandes dont les icônes sont bien connues ; dans le cas contraire, ils utilisent des étiquettes de texte sans icônes. Cela améliore la clarté des étiquettes, mais nécessite plus d’espace.

-   **Assurez-vous que les icônes de barre d’outils sont clairement visibles par rapport à la couleur d’arrière-plan.** Évaluez toujours les icônes de barre d’outils en contexte et en mode de contraste élevé.
-   **Choisissez des conceptions d’icône qui communiquent clairement leur objectif, en particulier pour les commandes les plus fréquemment utilisées.** Les barres d’outils bien conçues ont besoin d’icônes explicites, car les utilisateurs ne peuvent pas trouver efficacement les commandes à l’aide de leurs info-bulles. Toutefois, les barres d’outils fonctionnent toujours bien si les icônes de quelques commandes moins fréquemment utilisées ne sont pas explicites.
-   **Choisissez des icônes qui peuvent être reconnaissables et pouvant être distinguées, en particulier pour les commandes les plus fréquemment utilisées.** Assurez-vous que les icônes ont des formes et des couleurs distinctives. Cela aide les utilisateurs à trouver rapidement les commandes, même s’ils ne se souviennent pas du symbole d’icône.
-   **Assurez-vous que les icônes de barre d’outils sont conformes aux règles d’icône de style Aero.**

Pour plus d’informations et d’exemples, consultez [icônes](vis-icons.md).

### <a name="standard-menu-and-split-buttons"></a>Menus standard et boutons partagés

Si vous utilisez des boutons de menu et des boutons partagés dans une barre d’outils, essayez d’utiliser les structures de menu standard suivantes et leurs commandes appropriées dans la mesure du possible. Contrairement aux barres de menus, les commandes de barre d’outils n’acceptent pas les clés d’accès.

**Barres d’outils principales**

Ces commandes reflètent les commandes qui se trouvent dans les barres de menus standard. elles doivent donc être utilisées uniquement pour les barres d’outils principales. Cette liste affiche les étiquettes de bouton (et type) avec leur ordre et leurs séparateurs, touches de raccourci et points de suspension. **Notez que la commande permettant d’afficher et de masquer la barre de menus se trouve dans le menu Affichage.**

<dl> Fichier <dl> NewCtrl + N  
Ouvrir... Ctrl + O  
Fermez <separator>  
SaveCtrl + S  
Enregistrer sous... <separator>  
Envoyer à <separator>  
Imprimer... Ctrl + P  
Aperçu avant impression  
Mise en page <separator>  
Exinitialisationt + F4 (raccourci généralement non fourni)
</dl> </dd> Edit(menu button) <dl> UndoCtrl + Z  
RedoCtrl + Y <separator>  
CutCtrl + X  
CopyCtrl + C  
PasteCtrl + V <separator>  
Sélectionner allCtrl + A <separator>  
DeleteDel (raccourci généralement non fourni)  
Renommer... <separator>  
Rechercher... Ctrl + F  
Find nextF3 (commande généralement non fournie)  
Remplacer... Ctrl + H  
Atteindre... CTRL + G
</dl> </dd> <dd>Imprimer (bouton partagé) <dl> Imprimer... Ctrl + P  
Aperçu avant impression <separator>  
Mise en page
</dl> </dd> Vue (bouton de menu) <dl> Barre de menus (vérifier si visible)  
Volet d’informations (vérifier si visible)  
Volet de visualisation (vérifier si visible)  
Barre d’État (vérifier si visible) <separator>  
Zoom  
Zoom inctrl + +  
Zoom arrière CTRL +- <separator>  
Taille du texte (le paramètre sélectionné contient une puce) <dl> Élevée  
Plus grand  
Moyen  
Plus petite  
Plus petit
</dl> </dd> <separator> ScreenF11 complet  
RefreshF5
</dl> </dd> Tools(menu button) <dl> ... <separator>  
Options
</dl>> </dd> Help(split button, use the Help icon) <dl> <program name> helpF1 <separator>  
Obtenir <program name>  
</dl> </dd> </dl>

**Barres d’outils supplémentaires**

Ces commandes complètent les barres de menus standard. Cette liste affiche les étiquettes de bouton (et type) avec leur ordre et leurs séparateurs, touches de raccourci et points de suspension. **Notez que la commande permettant d’afficher et de masquer la barre de menus se trouve dans le menu outils.**

Les noms de catégorie de barre d’outils supplémentaires diffèrent des noms de catégorie de menu standard, car ils doivent être plus englobants. Par exemple, la catégorie organiser est utilisée à la place de modifier, car elle contient des commandes qui ne sont pas liées à la modification. **Pour maintenir la cohérence entre les barres de menus et les barres d’outils, utilisez les noms de catégorie de menu standard si cela ne serait pas trompeur.**

**Incorrect :**

![capture d’écran des mêmes options pour différentes commandes ](images/cmd-toolbars-image44.png)

Dans cet exemple, la barre d’outils doit utiliser modifier au lieu de organiser la cohérence, car elle contient les commandes de menu Edition standard.

### <a name="palette-windows"></a>Fenêtres de palette

-   **Les fenêtres de palette utilisent des barres de titre plus courtes pour réduire l’espace à l’écran.** Placez un bouton Fermer dans la barre de titre.
-   **Définissez le texte de la barre de titre sur la commande qui affichait la fenêtre de la palette.**
-   **Utilisez la mise en majuscules de style phrase sans ponctuation finale.**
-   **Fournissez un menu contextuel pour les commandes de gestion de fenêtre.** Affiche ce menu contextuel quand les utilisateurs cliquent avec le bouton droit sur la barre de titre.

    ![capture d’écran de la boîte à outils avec menu contextuel ](images/cmd-toolbars-image45.png)

    Dans cet exemple, les utilisateurs peuvent cliquer avec le bouton droit sur la barre de titre pour afficher le menu contextuel.

-   **Lorsque cela est possible et utile, rendez les fenêtres de palette redimensionnables.** Indique que la fenêtre est redimensionnable, à l’aide de pointeurs de redimensionnement au-dessus du cadre de la fenêtre.
-   **Quand une fenêtre de palette est réaffichée, l’affiche en utilisant le même État que le dernier accès.** Lors de la fermeture, enregistrez la taille et l’emplacement de la fenêtre. Lors du réaffichage, restaurez la taille et l’emplacement des fenêtres enregistrées. Par ailleurs, envisagez de rendre ces attributs persistants entre les instances de programme par utilisateur.

### <a name="customization"></a>Personnalisation

-   **Fournir une personnalisation pour les barres d’outils comprenant deux lignes ou plus.** Seul le style d’icônes sans étiquette doit être personnalisé. Les barres d’outils simples avec peu de commandes n’ont pas besoin de personnalisation.
-   **Fournissez une bonne configuration par défaut.** Les utilisateurs ne doivent pas avoir à personnaliser leurs barres d’outils pour les scénarios courants. Ne vous inquiétez pas des utilisateurs qui personnalisent leur façon de procéder à une mauvaise configuration initiale. Supposons que la plupart des utilisateurs ne personnalisent pas leurs barres d’outils.
-   **Fournissez un menu contextuel avec les commandes suivantes :**
    -   Une liste de cases à cocher pour afficher les barres d’outils disponibles
    -   Verrouiller/déverrouiller les barres d’outils
    -   Personnaliser...
-   **Verrouiller les barres d’outils personnalisables par défaut**, pour éviter les modifications accidentelles.
-   **Pour la commande personnaliser, affichez une boîte de dialogue Options** qui vous permet de choisir les barres d’outils à afficher et les commandes sur chacune d’elles.

    ![capture d’écran de la boîte de dialogue Personnaliser et des options ](images/cmd-toolbars-image46.png)

    dans cet exemple, Visual Studio fournit une boîte de dialogue options pour personnaliser ses barres d’outils.

-   Fournissez une commande de réinitialisation pour revenir à la configuration de la barre d’outils d’origine dans la boîte de dialogue Personnaliser les options.
-   **Donnez la possibilité de personnaliser les barres d’outils à l’aide de la fonctionnalité glisser-déplacer des manières suivantes :**

    -   Définissez l’ordre et les positions de la barre d’outils.
    -   Définir des longueurs de barres d’outils, affichant toutes les barres d’outils trop petites pour afficher leur contenu avec un chevron de dépassement.
    -   S’ils sont pris en charge, détachez les barres d’outils pour les fenêtres de palette et vice versa.

    Quand la boîte de dialogue Personnaliser les options s’affiche :

    -   Définissez le contenu de la barre d’outils.
    -   Définit l’ordre du contenu de la barre d’outils.

    Cela permet aux utilisateurs d’apporter des modifications plus rapidement et plus efficacement.

-   **Enregistrez toutes les personnalisations de la barre d’outils,** en fonction de chaque utilisateur.

### <a name="using-ellipses"></a>Utilisation de ellipses

Alors que les commandes de la barre d’outils sont utilisées pour les actions immédiates, des informations supplémentaires sont parfois nécessaires pour effectuer cette action. Utilisez des points de suspension pour indiquer qu’une commande requiert plus d’informations avant de pouvoir prendre effet. Placez les points de suspension à la fin de l’info-bulle et de l’étiquette, le cas échéant.

![capture d’écran du texte info-bulle d’impression avec des points de suspension ](images/cmd-toolbars-image47.png)

Dans cet exemple, la page... commande affiche une boîte de dialogue Imprimer pour recueillir plus d’informations.

Toutefois, si une commande ne peut pas prendre effet immédiatement, aucun bouton de sélection n’est requis. Par exemple, les paramètres de partage n’ont pas de points de suspension, même s’ils ont besoin d’informations supplémentaires, car la commande ne peut pas être appliquée immédiatement.

![capture d’écran de la barre d’outils, de la commande et de l’info-bulle ](images/cmd-toolbars-image48.png)

la commande de Paramètres de partage n’a pas de points de suspension, car elle ne peut pas prendre effet immédiatement.

Étant donné que les barres d’outils s’affichent en permanence et que l’espace est limité, les **ellipses doivent être rarement utilisées**.

> [!Note]  
> Pour les menus affichés par une barre d’outils, appliquez les [indications relatives aux ellipses de menu](cmd-menus.md).

 

## <a name="recommended-sizing-and-spacing"></a>Dimensionnement et espacement recommandés

![capture d’écran des barres d’outils avec des informations d’espacement ](images/cmd-toolbars-image49.png)

Dimensionnement et espacement recommandés pour les barres d’outils standard.

## <a name="labels"></a>Étiquettes

### <a name="general"></a>Général

-   **Utilisez les majuscules comme pour les phrases.**
    -   **Exception :** Pour les applications héritées, vous pouvez utiliser la mise en majuscules de style titre si nécessaire pour éviter de mélanger les styles de mise en majuscules.

### <a name="unlabeled-icon-buttons"></a>Boutons d’icône sans étiquette

-   **Utilisez une info-bulle pour étiqueter la commande.** Pour le texte d’info-bulle, utilisez l’étiquette si le bouton a été étiqueté, mais incluez la touche de raccourci, le cas échéant.

    ![capture d’écran de la barre d’outils, de l’icône d’imprimante et de l’info-bulle ](images/cmd-toolbars-image50.png)

    Exemple d’info-bulle de bouton d’icône.

### <a name="labeled-icon-buttons"></a>Boutons d’icônes étiquetés

-   **Utilisez une étiquette concise.** Utilisez un seul mot si possible, quatre mots maximum.
-   **Placez l’étiquette à droite de l’icône.**
-   **Utilisez une info-bulle pour décrire la commande.** Étant donné que les boutons sont étiquetés, l’utilisation d’une info-bulle au lieu d’une info-bulle serait redondante.

    ![capture d’écran d’un bouton étiqueté avec une info-bulle ](images/cmd-toolbars-image51.png)

    Exemple d’une info-bulle de bouton d’icône étiquetée.

### <a name="drop-down-lists"></a>Listes déroulantes

-   **Si la liste a toujours une valeur, utilisez la valeur actuelle comme étiquette.**

    ![capture d’écran de la barre d’outils avec options de police ](images/cmd-toolbars-image52.png)

    Dans cet exemple, le nom de police actuellement sélectionné agit en tant qu’étiquette.

-   Si une liste déroulante modifiable n’a pas de valeur, utilisez une [invite](glossary.md).

    ![capture d’écran des carnets d’adresses de recherche d’étiquettes ](images/cmd-toolbars-image53.png)

    Dans cet exemple, une invite est utilisée pour l’étiquette de la liste déroulante.

### <a name="menu-buttons-and-split-buttons"></a>Boutons de menu et boutons partagés

-   **Préférer les noms de boutons de menu basés sur un verbe.** Toutefois, omettez le verbe s’il s’agit de créer, afficher, afficher ou gérer. Par exemple, les boutons de menu **Outils** et **page** n’ont pas de verbes.
-   **Utilisez un mot spécifique unique qui décrit clairement et avec précision le contenu du menu.** Alors que les noms n’ont pas besoin d’être tellement généraux qu’ils décrivent tous les éléments du menu, ils doivent être suffisamment prévisibles pour que les utilisateurs ne soient pas surpris par ce qu’ils recherchent dans le menu.
-   **Si ce n’est pas obligatoire, fournissez des descriptions d’info-bulle si elles sont utiles.**

### <a name="menu-items"></a>Éléments de menu

-   **Utilisez des noms d’élément de menu qui commencent par un verbe, un substantif ou une expression nominale.**
-   **Préférer les noms de menu basés sur un verbe.** Toutefois, omettez le verbe s’il s’agit de créer, afficher, afficher ou gérer. Par exemple, les commandes suivantes n’utilisent pas de verbes :
    -   À propos de
    -   Avancé
    -   Plein écran
    -   Nouveau
    -   Options
    -   Propriétés
-   **Utilisez des verbes spécifiques.** Évitez les verbes génériques sans aide, tels que change et Manage.
-   **Utilisez des noms singulières pour les commandes qui s’appliquent à un seul objet,** sinon utilisez des noms au pluriel.
-   **Pour les paires de commandes complémentaires, choisissez des noms clairement complémentaires.** Exemples : Add, Remove ; Afficher, masquer ; Insérer, supprimer.
-   **Choisissez des noms d’élément de menu en fonction des objectifs et des tâches de l’utilisateur, et non de la technologie.**
-   Utilisez les noms d’élément de menu suivants à des fins définies :
    -   **Options :** Pour afficher les options du programme.
    -   **Personnaliser :** Pour afficher les options de programme spécifiquement liées à la configuration de l’interface utilisateur mécanique.
    -   **Personnaliser :** Pour afficher un résumé des paramètres de [personnalisation](glossary.md) couramment utilisés.
    -   **Préférences :** N’utilisez pas. Utilisez à la place des options.
    -   **Propriétés :** Pour afficher la fenêtre des propriétés d’un objet.
    -   **Paramètres :** N’utilisez pas comme étiquette de menu. Utilisez à la place des options.
-   **Les éléments de menu qui affichent des sous-menus n’ont jamais de points de suspension sur leur étiquette.** La flèche de sous-menu indique qu’une autre sélection est requise.

## <a name="documentation"></a>Documentation

Lorsque vous faites référence à des barres d’outils :

-   S’il n’existe qu’une seule barre d’outils, reportez-vous à la barre d’outils.
-   S’il existe plusieurs barres d’outils, reportez-vous à leur nom, suivi de la barre d’outils Word. Reportez-vous à la barre d’outils principale qui est activée par défaut et contient des boutons pour les tâches de base, telles que l’ouverture et l’impression d’un fichier, comme barre d’outils standard.
-   La barre d’outils est un mot unique et non en majuscules. (Par contraste, la barre de menus est de deux mots.)
-   Reportez-vous aux boutons de barre d’outils par leurs étiquettes d’info-bulle. Utilisez le texte exact de l’étiquette, y compris sa mise en majuscules, mais n’incluez pas de points de suspension.
-   Reportez-vous aux boutons de menu de la barre d’outils par leurs étiquettes et le menu Word. Utilisez le texte exact de l’étiquette, y compris sa mise en majuscules.
-   Reportez-vous aux contrôles ToolBar en général sous forme de boutons de barre d’outils.
-   Pour décrire l’interaction avec l’utilisateur, cliquez sur les boutons de la barre d’outils et les listes déroulantes en lecture seule, puis entrez pour les listes déroulantes modifiables. N’utilisez pas Choose, SELECT ou Pick.
-   N’utilisez pas la mise en cascade, la liste déroulante ou la fenêtre contextuelle pour décrire les boutons de menu, sauf dans la documentation de programmation.
-   Reportez-vous aux éléments non disponibles comme indisponibles, non estompés, désactivés ou grisés. Utilisez Disabled dans la documentation de programmation.
-   Dans la mesure du possible, mettez en forme les étiquettes à l’aide du texte gras. Dans le cas contraire, placez les étiquettes entre guillemets uniquement si nécessaire pour éviter toute confusion.

Exemples :

-   Dans le menu **page** de la barre d’outils, cliquez sur **Envoyer la page par courrier électronique**.
-   Dans la zone **polices** de la barre d’outils, entrez « Segoe UI ».
-   Dans la barre d’outils **mise en forme** , pointez sur **Afficher**, puis cliquez sur **Commentaires**.

 

