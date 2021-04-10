---
title: Éléments graphiques
description: Les éléments graphiques affichent les relations, la hiérarchie et l’accentuation visuellement. Elles incluent les arrière-plans, les bannières, les verres, les agrégateurs, les séparateurs, les ombres et les poignées.
ms.assetid: f9e741e9-a72e-4bdb-bd95-8916c7cf344f
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: a452668bc1685143273df80fd144642a18019213
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "103953319"
---
# <a name="graphic-elements"></a>Éléments graphiques

> [!NOTE]
> Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Les *éléments graphiques* affichent les relations, la hiérarchie et l’accentuation visuellement. Elles incluent les arrière-plans, les bannières, les verres, les agrégateurs, les séparateurs, les ombres et les poignées.

![capture d’écran de l’Explorateur Windows avec l’ombre, etc. ](images/vis-graphic-image1.png)

Exemple avec plusieurs types d’éléments graphiques.

Les éléments graphiques ne sont généralement pas interactifs. Toutefois, les séparateurs sont interactifs pour le contenu redimensionnable et les descripteurs sont des graphiques qui affichent l’interactivité.

**Remarque :** Les instructions relatives aux [zones de groupe](ctrl-group-boxes.md), aux [animations](vis-animations.md), aux [icônes](vis-icons.md)et à la [personnalisation](exper-branding.md) sont présentées dans des articles distincts.

## <a name="is-this-the-right-user-interface"></a>S’agit-il de l’interface utilisateur appropriée ?

Tandis que les éléments graphiques sont un moyen visuel fort d’indiquer des relations, leur utilisation augmente l’encombrement visuel et réduit l’espace disponible sur une surface. Ils doivent être utilisés avec modération.

Une tendance à la conception dans Microsoft Windows est une apparence plus simple et plus claire en éliminant les graphiques et les lignes inutiles.

Pour déterminer si un élément graphique est nécessaire, posez-vous les questions suivantes :

-   **La présentation et la communication de la conception sont-elles aussi claires et efficaces sans l’élément ?** Si c’est le cas, supprimez-le.
-   **Pouvez-vous communiquer efficacement les relations à l’aide de la disposition seule ?** Dans ce cas, utilisez la [disposition](vis-layout.md) à la place. Vous pouvez placer des contrôles connexes les uns à côté des autres et placer un espace supplémentaire entre des contrôles non liés. Vous pouvez également utiliser la mise en retrait pour afficher les relations hiérarchiques.

![capture d’écran d’une disposition à quatre icônes ](images/vis-graphic-image2.png)

Dans cet exemple, la disposition seule est utilisée pour afficher les relations de contrôle.

-   **La communication est-elle efficace sans texte ?** Dans le cas contraire, utilisez une [zone de groupe](ctrl-group-boxes.md), un séparateur étiqueté ou une autre [étiquette](text-ui.md).

## <a name="usage-patterns"></a>Modèles d’usage

Les éléments graphiques ont plusieurs modèles d’utilisation :



|                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Illustrations graphiques**<br/> Utilisez pour communiquer une idée visuellement. <br/>                         | Les illustrations graphiques sont similaires aux icônes, à ceci près qu’elles peuvent avoir n’importe quelle taille et ne sont généralement pas interactives. <br/> ![graphique de l’historique d’utilisation de l’UC de capture d’écran ](images/vis-graphic-image3.png)<br/> Dans cet exemple, une illustration graphique est utilisée pour suggérer la nature d’une fonctionnalité.<br/>                                                                                                                                                                                                        |
| **Arrière-plans**<br/> Utilisez pour mettre en évidence ou retirer les différents types de contenu. <br/>           | Les arrière-plans peuvent être utilisés pour mettre en évidence du contenu important. <br/> ![capture d’écran du message de virus sur l’arrière-plan rouge ](images/vis-graphic-image4.png)<br/> dans cet exemple, un arrière-plan est utilisé pour mettre en évidence une tâche importante.<br/> les arrière-plans peuvent également servir à mettre en évidence du contenu secondaire. <br/> ![capture d’écran des éléments du panneau de configuration ](images/vis-graphic-image5.png)<br/> Dans cet exemple, les tâches secondaires sont déssoulignées en les localisant dans un volet de tâches.<br/>   |
| **Bande**<br/> utilisé pour indiquer un État important. <br/>                                         | Contrairement aux arrière-plans, les bannières mettent principalement en évidence une chaîne de texte unique. <br/> ![capture d’écran de la bannière avec les informations de paramètres ](images/vis-graphic-image6.png)<br/> Dans cet exemple, une bannière est utilisée pour indiquer que les paramètres de la page sont contrôlés par stratégie de groupe.<br/>                                                                                                                                                                                                       |
| **Glass**<br/> Utilisez stratégiquement pour réduire le poids visuel d’une fenêtre. <br/>                   | La transparence peut réduire le poids d’une surface en vous concentrant sur le contenu au lieu de la fenêtre elle-même. <br/> ![capture d’écran de l’oiseau dans la Galerie de photos Windows ](images/vis-graphic-image7.png)<br/> Dans cet exemple, la transparence porte l’attention de l’utilisateur sur le contenu au lieu des contrôles.<br/>                                                                                                                                                                                                 |
| **Agrégateurs**<br/> Utilisez pour créer une relation visuelle entre des contrôles étroitement liés. <br/> | ![capture d’écran des flèches de navigation arrière et avant ](images/vis-graphic-image8.png)<br/> dans cet exemple, l’arrière-plan d’un agrégateur est utilisé pour mettre en évidence la relation entre les boutons précédent et suivant dans l’Explorateur.<br/> ![capture d’écran des contrôles de la Galerie de photos Windows ](images/vis-graphic-image7.png)<br/> Dans cet exemple, une agrégation de limites est utilisée pour mettre en évidence la relation entre les contrôles et les faire ressembler à un contrôle unique au lieu de huit.<br/> |
| **Séparateurs**<br/> Utilisez pour séparer les contrôles faiblement liés ou non liés. <br/>                   | Les séparateurs peuvent être interactifs ou non interactifs. les séparateurs interactifs entre le contenu redimensionnable sont appelés séparateurs. <br/> ![capture d’écran du séparateur de séparateur pour le bouton nom ](images/vis-graphic-image9.png)<br/> dans cet exemple, un séparateur interactif est utilisé pour le contenu redimensionnable.<br/> ![capture d’écran du séparateur pour les informations du navigateur ](images/vis-graphic-image10.png)<br/> Dans cet exemple, le séparateur n’est pas interactif.<br/>                  |
| **Ombres**<br/> Utilisez pour faire ressortir le contenu visuellement par rapport à son arrière-plan. <br/>             | ![capture d’écran de quatre photos avec des ombres ](images/vis-graphic-image11.png)<br/> Dans cet exemple, les ombres font ressortir l’illustration de l’arrière-plan.<br/>                                                                                                                                                                                                                                                                                                                                   |
| **Poignées**<br/> Utilisez pour indiquer qu’un objet peut être déplacé ou redimensionné. <br/>                    | Les handles sont toujours interactifs et leur comportement est suggéré par le pointeur de la souris au pointage. <br/> ![capture d’écran d’un angle de fenêtre avec un pointeur de redimensionnement ](images/vis-graphic-image12.png)<br/> ![capture d’écran de la zone de sélection avec le pointeur de redimensionnement ](images/vis-graphic-image13.png)<br/> Dans ces exemples, les handles indiquent qu’un objet peut être redimensionné.<br/>                                                                                                                       |



 

## <a name="guidelines"></a>Consignes

### <a name="general"></a>Général

-   **Ne transmettent pas d’informations essentielles par le biais d’éléments graphiques uniquement.** Cela présente des problèmes d’accessibilité pour les utilisateurs présentant des handicaps ou des handicaps.

### <a name="graphic-designs"></a>Conceptions graphiques

-   **Les graphiques sont plus efficaces lorsqu’ils renforcent une seule idée simple.** Les graphiques complexes qui nécessitent une idée d’interpréter ne fonctionnent pas correctement. Les Hieroglyphics sont préférables pour les dessins de la cave.

    **Incorrect :**

    ![capture d’écran de l’avertissement à l’aide d’un graphique complexe ](images/vis-graphic-image14.png)

    Dans cet exemple, un graphique complexe de Windows XP tente d’expliquer de manière inefficacee une décision complexe d’approbation.

-   **N’utilisez pas de flèches, de chevrons, d’images de bouton ou d’autres intuitivité associés à des contrôles interactifs.** Cela invite les utilisateurs à interagir avec vos graphiques.
-   **Évitez les quantités de couleur rouge, jaune et vert pur dans vos conceptions.** Pour éviter toute confusion, réservez ces couleurs pour communiquer l’État. Si vous devez utiliser ces couleurs pour des éléments autres que l’État, utilisez des tons muets plutôt que des couleurs pures.
-   **Utilisez des conceptions culturellement neutres.** Ce qui peut avoir une signification particulière dans un pays, une région ou une culture peut ne pas avoir la même signification dans un autre.
-   **Évitez d’utiliser des personnes, des visages, des sexes ou des parties de corps, ainsi que des symboles religieux, politiques et nationaux.** Ces images peuvent ne pas être facilement traduites ou choquantes.
-   **Lorsque vous devez représenter des personnes ou des utilisateurs, présentez-les de façon générique.** Évitez les représentations réalistes.

### <a name="backgrounds-and-banners"></a>Arrière-plans et bannières

-   **Pour mettre en évidence du contenu, utilisez du texte foncé sur un arrière-plan clair.** Le texte noir sur un arrière-plan gris clair ou jaune fonctionne bien.

    ![capture d’écran du texte du lien bleu sur l’arrière-plan jaune ](images/vis-graphic-image15.png)

    Dans cet exemple, le lien obtient l’attention de l’utilisateur, car il se trouve sur un arrière-plan jaune.

-   **Pour mettre en évidence le contenu, utilisez du texte clair sur un arrière-plan sombre.** Le texte blanc sur un arrière-plan gris foncé ou bleu est bien adapté.

    ![capture d’écran du lien d’aide blanc sur l’arrière-plan vert ](images/vis-graphic-image16.png)

    Dans cet exemple, le contenu de l’arrière-plan foncé est désactivé.

-   **Si un dégradé est utilisé, assurez-vous que la couleur du texte a un bon contraste sur tout le dégradé.**
-   **Utilisez toujours une icône de pixel de 16x16 pour attirer l’attention sur la bannière.** Les bannières sont trop faciles à négliger dans le cas contraire. Pour obtenir des instructions et des exemples supplémentaires, consultez [icônes standard](vis-std-icons.md).
-   **Utilisez les arrière-plans et les bannières avec précaution.** Bien que l’objectif de l’arrière-plan ou de la bannière soit de mettre le contenu en évidence, les résultats sont très souvent opposés à un phénomène connu sous le nom de « cécité de bannière ».

### <a name="glass"></a>Glass

-   **Envisagez d’utiliser la transparence de manière stratégique dans les petites régions qui touchent le cadre de la fenêtre sans texte.** Cela peut donner à un programme un aspect plus simple, plus clair et plus cohérent en faisant en sorte que la région apparaisse comme faisant partie du cadre.
-   **N’utilisez pas de verre dans les situations où un arrière-plan de fenêtre ordinaire serait plus attrayant ou plus facile à utiliser.**

### <a name="separators"></a>Séparateurs

-   **Utilisez des lignes verticales et horizontales pour les séparateurs.** Veillez à disposer d’un espace suffisant entre les séparateurs et le contenu qui est séparé.
-   Pour les séparateurs entre le contenu dimensionnable (séparateurs), affichez le pointeur de redimensionnement au pointage.

![Capture d’écran montrant un séparateur avec un pointeur de redimensionnement.](images/vis-graphic-image17.png)

![capture d’écran d’un séparateur avec un pointeur de redimensionnement ](images/vis-graphic-image18.png)

Dans ces exemples, les pointeurs de redimensionnement sont affichés au pointage.

### <a name="shadows"></a>Ombres

-   **Utilisez-le uniquement pour que le contenu ou les objets les plus significatifs de votre programme soient déplacés en fonction de l’arrière-plan.** Pensez à l’encombrement visuel dans d’autres circonstances.

### <a name="high-dpi-support"></a>Prise en charge des résolutions élevées

-   **Prend en charge les modes vidéo de 96 et de 120 points par pouce (dpi).** Détectez le mode PPP au démarrage et gérez les événements de changement PPP. Windows est optimisé pour 96 et 120 ppp et utilise 96 dpi par défaut.
-   **Préférez fournir des bitmaps distinctes restituées spécifiquement pour les PPP 96 et 120 sur la mise à l’échelle des graphiques.** Au moins, fournissez des versions 96 et 120 ppp pour les bitmaps les plus importantes et visibles, ainsi que pour centrer ou mettre à l’échelle les autres. De telles applications sont considérées comme « compatibles avec les résolutions élevées » et offrent une meilleure expérience visuelle globale que les programmes mis à l’échelle automatiquement par Windows.
    -   Développeurs : vous pouvez déclarer un programme prenant en charge la résolution haute résolution (et empêcher la mise à l’échelle automatique) la définition de l’indicateur de prise en charge DPI dans le manifeste du programme, ou en appelant l’API SetProcessDPIAware () lors de l’initialisation du programme. Vous pouvez utiliser des macros pour simplifier la sélection des graphiques appropriés. Pour les bitmaps Win32, vous pouvez utiliser SS \_ CENTERIMAGE pour centrer ou SS \_ REALSIZECONTROL pour mettre à l’échelle.
-   Vérifiez votre programme à la fois dans 96 et 120 ppp pour :
    -   Graphiques trop petits ou trop grands.
    -   Graphiques découpés, superposés ou non correctement ajustés.
    -   Graphiques mal étirés (« pixelisée »).
    -   Texte qui est coupé ou non ajusté dans les arrière-plans graphiques.

## <a name="text"></a>Texte

-   **Pour l’accessibilité et la localisation, n’utilisez pas de texte dans les graphiques.** N’effectuez d’exceptions que pour représenter le [marquage](exper-branding.md) et le texte comme un concept abstrait.

 

