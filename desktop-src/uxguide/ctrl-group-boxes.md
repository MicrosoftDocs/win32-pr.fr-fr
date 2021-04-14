---
title: Zones de groupe
description: Une zone de groupe est un cadre rectangulaire étiqueté qui entoure un ensemble de contrôles connexes. Une zone de groupe est un moyen d’afficher les relations visuellement. Hormis le fait que vous fournissez éventuellement une clé d’accès pour un groupe de contrôles, elle ne fournit aucune fonctionnalité.
ms.assetid: 5b5ffb36-3ed1-44cd-af87-5cddf46c56a6
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 67f930383f2d4412d30027971c6cab2bd3edcccd
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104564786"
---
# <a name="group-boxes"></a>Zones de groupe

> [!NOTE]
> Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Une zone de groupe est un cadre rectangulaire étiqueté qui entoure un ensemble de contrôles connexes. Une zone de groupe est un moyen d’afficher les relations visuellement. Hormis le fait que vous fournissez éventuellement une clé d’accès pour un groupe de contrôles, elle ne fournit aucune fonctionnalité.

![capture d’écran de la zone de groupe contenant les cases à cocher ](images/ctrl-group-boxes-image1.png)

Zone de groupe classique.

> [!Note]  
> Les instructions relatives à la [disposition](vis-layout.md) sont présentées dans un article distinct.

 

## <a name="is-this-the-right-control"></a>Est-ce le contrôle approprié ?

Tandis que les zones de groupe sont un moyen visuel fort d’indiquer les relations, leur utilisation augmente l’encombrement visuel et réduit considérablement l’espace disponible sur une surface. Elles sont visuellement lourdes et doivent être utilisées avec modération, uniquement lorsqu’il n’y a pas de meilleure solution.

Une tendance à la conception dans Windows est une apparence plus simple et plus claire en éliminant les lignes inutiles.

Pour déterminer si une zone de groupe est nécessaire, posez-vous les questions suivantes :

-   **Existe-t-il plusieurs contrôles dans le groupe ?** Si ce n’est pas le cas, utilisez une étiquette de texte brut à la place. Une exception rare est l’utilisation d’une zone de groupe avec un contrôle unique pour maintenir la cohérence avec d’autres zones de groupe sur la même surface.

**Incorrect :** ![ capture d’écran de la zone de groupe contenant une zone de texte ](images/ctrl-group-boxes-image2.png)

Dans cet exemple, la zone de groupe n’a qu’un seul contrôle.

-   **Les contrôles sont-ils liés ? L’indication de la relation est-elle plus claire ?** Si ce n’est pas le cas, présentez les contrôles séparément en dehors d’une zone de groupe.
-   **Tous les contrôles sont-ils à l’intérieur du groupe ?** Dans ce cas, indiquez la relation sur la plus grande surface, telle que la boîte de dialogue ou la page parente.

**Incorrect :** ![ capture d’écran de la zone de groupe contenant tous les contrôles ](images/ctrl-group-boxes-image3.png)

Dans cet exemple, tous les contrôles (à part des boutons de validation) de la boîte de dialogue se trouvent dans la zone de groupe.

-   **Pouvez-vous communiquer efficacement les relations à l’aide de la disposition seule ?** Dans ce cas, utilisez la [disposition](vis-layout.md) à la place. Vous pouvez placer des contrôles connexes les uns à côté des autres et placer un espace supplémentaire entre des contrôles non liés. Vous pouvez également utiliser les en-têtes et la mise en retrait pour afficher les relations hiérarchiques.

![figure de quatre icônes avec quatre groupes de tâches ](images/ctrl-group-boxes-image4.png)

Dans cet exemple, la disposition seule est utilisée pour afficher les relations de contrôle.

-   **Pouvez-vous communiquer efficacement les relations à l’aide d’un séparateur ?** Si c’est le cas, utilisez un séparateur à la place. Un séparateur est une ligne horizontale qui unifie les contrôles situés au-dessous. Les séparateurs offrent une apparence plus simple et plus claire. Toutefois, contrairement aux zones de groupe, elles fonctionnent mieux quand elles s’étendent à la largeur totale de la surface.
    -   **Développeurs :** Vous pouvez implémenter un séparateur avec un rectangle gravé avec une hauteur d’un.

![Capture d’écran montrant les contrôles de courrier électronique, séparés par des séparateurs de rectangles gravés.](images/ctrl-group-boxes-image5.png)

Dans cet exemple, les séparateurs étiquetés sont utilisés pour afficher les relations de contrôle.

![capture d’écran des contrôles séparés par des séparateurs ](images/ctrl-group-boxes-image6.png)

Dans cet exemple, les séparateurs sans étiquette sont utilisés pour afficher les relations de contrôle.

-   **Pouvez-vous communiquer efficacement les relations sans texte ?** Si c’est le cas, envisagez d’utiliser des éléments graphiques tels que les [arrière-plans](vis-graphic.md) ou les agrégateurs.

## <a name="guidelines"></a>Consignes

-   **N’imbriquez pas les zones de groupe.** Utilisez disposition pour afficher les relations dans une zone de groupe.

**Incorrect :** ![ capture d’écran d’une zone de groupe dans une zone de groupe ](images/ctrl-group-boxes-image7.png)

Dans cet exemple, les zones de groupe imbriquées entraînent un encombrement visuel inutile.

**Correct :** ![ capture d’écran des mêmes contrôles dans une zone de groupe ](images/ctrl-group-boxes-image8.png)

Dans cet exemple, la même relation de contrôle est affichée à l’aide de layout à la place.

-   Ne placez pas de contrôles dans les étiquettes de zone de groupe.
    -   **Exception :** Vous pouvez utiliser une case à cocher comme étiquette de zone de groupe si tous les contrôles à l’intérieur de la zone sont activés et désactivés par la case à cocher.

**Incorrect :** ![ capture d’écran de la liste déroulante sur une étiquette de zone de groupe ](images/ctrl-group-boxes-image9.png)

Dans cet exemple, une liste déroulante est placée incorrectement dans une zone de groupe. Cet exemple doit utiliser des [onglets](https://msdn.microsoft.com/library/windows/desktop/aa511493.aspx) à la place.

-   **Ne désactivez pas les zones de groupe.** Pour indiquer qu’un groupe de contrôles n’est pas actuellement appliqué, désactivez tous les contrôles dans la zone de groupe, mais pas la zone de groupe elle-même. Cette approche est plus accessible et peut être prise en charge de manière cohérente par toutes les infrastructures d’interface utilisateur.

## <a name="labels"></a>Étiquettes

-   Étiquetez toutes les zones de groupe.
-   N’attribuez pas de clé d’accès à l’étiquette. Cela n’est pas nécessaire et rend les autres clés d’accès plus difficiles à assigner. Au lieu de cela, affectez des clés d’accès aux contrôles dans la zone de groupe.
    -   **Exception :** Si une surface possède de nombreux contrôles, il se peut qu’il n’y ait pas suffisamment de clés d’accès disponibles. Dans ce cas, réduisez le nombre de touches d’accès en les assignant à des zones de groupe au lieu des contrôles dans les zones de groupe.
-   Utilisez la mise [en majuscules de style phrase](glossary.md).
-   Écrivez l’étiquette à l’aide d’un nom ou d’une expression nominale, pas en tant que phrase, et n’utilisez pas de ponctuation finale, y compris les signes deux-points.
-   Utilisez une formulation parallèle pour les étiquettes de zone de groupe dans la même surface.
-   Conserver les étiquettes de zone de groupe concises. N’utilisez pas le texte d’instructions comme étiquette. Vous pouvez toutefois obtenir un texte d’instructions dans la zone de groupe.
-   Ne répétez pas l’étiquette de la zone de groupe dans les étiquettes de contrôle dans la zone. Par exemple, si la zone de groupe est étiquetée alignement, étiquetez les cases d’option gauche, droite, etc., pas alignement à gauche ou alignement à droite.
-   Ne faites pas référence aux zones de groupe dans le texte de l’interface utilisateur.

## <a name="documentation"></a>Documentation

Lorsque vous faites référence à des zones de groupe :

-   Reportez-vous aux zones de groupe uniquement dans le programmeur et toute autre documentation technique. Pour la zone de groupe, utilisez deux minuscules.
-   Partout ailleurs, il n’est pas nécessaire d’inclure le nom de la zone de groupe dans une procédure, sauf si une boîte de dialogue contient plusieurs options portant le même nom. Dans ce cas, utilisez sous avec le nom de la zone de groupe.
-   Dans la mesure du possible, mettez en forme l’étiquette à l’aide de texte en gras. Sinon, placez l’étiquette entre guillemets uniquement si nécessaire pour éviter toute confusion.

Exemple : sous **effets**, sélectionnez **masqué**.

 

 