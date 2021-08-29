---
title: Découpage (DirectComposition)
description: Cette rubrique décrit la prise en charge de Microsoft DirectComposition pour les éléments visuels de découpage.
ms.assetid: B6E0D8F5-B6B9-40CC-B079-850AC8F2D538
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 446dda9cc95341dcce041dbfbfd32a9d0368e74b2a67aabe1a8b1c4856165ea4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043395"
---
# <a name="clipping-directcomposition"></a>Découpage (DirectComposition)

> [!NOTE]
> pour les applications sur Windows 10, nous vous recommandons d’utiliser des api Windows. UI. Composition au lieu de DirectComposition. Pour plus d’informations, consultez [moderniser votre application de bureau à l’aide de la couche visuelle](/windows/uwp/composition/visual-layer-in-desktop-apps).

Le découpage permet d’afficher uniquement une partie d’une arborescence visuelle ou visuelle en limitant le rendu de l’arborescence ou du visuel à une zone rectangulaire particulière. Cette rubrique décrit la prise en charge de Microsoft DirectComposition pour les éléments visuels de découpage. Il comprend les sections suivantes :

-   [Rectangle de découpage](#clip-rectangle)
-   [Clip, objet](#clip-object)
-   [Rectangle de découpage animé](#animated-clip-rectangle)
-   [Rubriques connexes](#related-topics)

## <a name="clip-rectangle"></a>Rectangle de découpage

Un objet visuel a une propriété de clip qui définit une zone rectangulaire, ou un *rectangle de découpage*, dans le contenu de la bitmap du visuel. Lorsque l’élément visuel est rendu à l’écran, seule la partie du contenu de la bitmap qui se trouve à l’intérieur du rectangle de découpage est dessinée à l’écran, tandis que le contenu qui s’étend hors du rectangle de découpage est coupé (non dessiné). Par défaut, la propriété Clip comprend tout le contenu de la bitmap.

La propriété de découpage d’un élément visuel s’applique à tous les éléments visuels enfants et descendants. En d’autres termes, tout contenu enfant ou descendant qui se trouve en dehors des limites du rectangle de découpage du parent est également coupé.

DirectComposition applique la propriété Clip avant d’appliquer les propriétés de transformation OffsetX, OffsetY et 2D, mais après l’application des propriétés Effect et 3D Transform. Cela signifie que les transformations 2D, les offsets et les décalages, affectent à la fois le contenu visuel et le rectangle de découpage. Alors que les transformations et les effets 3D ne s’appliquent pas au rectangle de découpage.

Par exemple, lors de l’application d’un décalage ou d’une transformation 2D, le rectangle de découpage est affecté par la matrice de transformation. Par conséquent, l’ajout d’un décalage et d’une rotation 2D (45 degrés) avec un rectangle de découpage arrondi se traduira par ce qui suit :

![Diagramme montrant l’effet d’une transformation 2D sur un rectangle de découpage.](images/clipping2dtransform.png)

Lors de l’application d’une transformation 3D « au sein » du rectangle de découpage, le rectangle de découpage n’est pas affecté par la matrice de transformation. Même lors de l’application d’une rotation autour de l’axe Z (de la même façon que l’exemple précédent), le diagramme suivant est le résultat :

![Diagramme montrant qu’une transformation 3D n’affecte pas l’élément Rectangle (rotation visuelle dans le clip).](images/clipping3dtransform.png)

Notez que le visuel pivoté dans le clip, car la matrice 3D n’est pas appliquée au clip lui-même.

Si la propriété Clip est définie sur un rectangle vide, l’élément visuel est entièrement coupé ; autrement dit, le visuel est inclus dans l’arborescence d’éléments visuels, mais il n’affiche rien. Si vous ne souhaitez pas inclure un visuel particulier dans une composition, supprimez l’élément visuel de l’arborescence d’éléments visuels au lieu de définir un rectangle de découpage vide. La suppression des résultats visuels améliore les performances.

Vous définissez la propriété clip d’un élément visuel à l’aide de la méthode [**IDCompositionVisual :: SetClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_)) . Cette méthode comprend des surcharges qui vous permettent de définir la valeur de la propriété clip sur un rectangle statique ou un objet clip. Utilisez un rectangle statique si vous n’avez pas besoin de modifier les dimensions du rectangle de découpage pendant la durée de vie de l’élément visuel. Si vous avez besoin de modifier les dimensions ou d’animer le rectangle de découpage, utilisez un objet clip.

## <a name="clip-object"></a>Clip, objet

Un objet clip est un objet COM (Component Object Model) qui représente un rectangle de découpage. Vous créez un objet clip à l’aide de la méthode [**IDCompositionDevice :: CreateRectangleClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrectangleclip) , puis vous utilisez l’interface [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) de l’objet pour définir les propriétés de l’objet. Un objet clip nouvellement créé a les valeurs minimales possibles pour les propriétés Left et Top, ainsi que les valeurs maximales possibles pour les propriétés Right et Bottom, ce qui en fait un objet de non-op. En d’autres termes, l’objet représente un rectangle de découpage qui inclut la totalité du contenu de la bitmap d’un visuel.

Un objet clip comprend un ensemble de propriétés qui vous permettent de spécifier des angles arrondis pour l’objet clip. Les propriétés vous permettent de définir le rayon x et le rayon y de chaque angle de l’objet de découpage.

## <a name="animated-clip-rectangle"></a>Rectangle de découpage animé

Vous pouvez animer un rectangle de découpage en appliquant des objets d’animation aux propriétés gauche, haut, droite et inférieure d’un objet clip. Utilisez la méthode surchargée [**IDCompositionVisual :: SetClip (IDCompositionClip)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) pour appliquer le rectangle de découpage animé à la propriété clip d’un élément visuel.

Pour plus d’informations sur les objets d’animation, consultez [animation](animation.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts DirectComposition](directcomposition-concepts.md)
</dt> <dt>

[Comment découper un objet Rectangle](how-to--set-the-clip-rectangle-for-a-visual.md)
</dt> </dl>

 

 
