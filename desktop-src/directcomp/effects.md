---
title: Effets (DirectComposition)
description: Cette rubrique présente les principes fondamentaux des effets Microsoft DirectComposition et décrit les types d’effets pris en charge par DirectComposition.
ms.assetid: 805B17D2-2F6B-4C25-8C6D-41FFA5DFC774
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9c5119367a35725a85efe20b8ba4d0f9f9887ff91b4d9618e2215bedfbfef67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117905048"
---
# <a name="effects-directcomposition"></a>Effets (DirectComposition)

> [!NOTE]
> pour les applications sur Windows 10, nous vous recommandons d’utiliser des api Windows. UI. Composition au lieu de DirectComposition. Pour plus d’informations, consultez [moderniser votre application de bureau à l’aide de la couche visuelle](/windows/uwp/composition/visual-layer-in-desktop-apps).

Cette rubrique présente les principes fondamentaux des effets Microsoft DirectComposition et décrit les types d’effets pris en charge par DirectComposition.

Cette rubrique contient les sections suivantes :

-   [Qu’est-ce qu’un effet DirectComposition ?](#what-is-a-directcomposition-effect)
-   [Opacity](#opacity)
-   [effets de transformation de perspective 3D](#3d-perspective-transform-effects)
    -   [Espace de coordonnées 3D DirectComposition](#the-directcomposition-3d-coordinate-space)
    -   [effet de transformation de rotation 3D](#3d-rotation-transform-effect)
    -   [effet de transformation de mise à l’échelle 3D](#3d-scaling-transform-effect)
    -   [effet de transformation de translation 3D](#3d-translation-transform-effect)
    -   [transformation de matrice 3D, effet](#3d-matrix-transform-effect)
    -   [Groupe d’effets de transformation 3D](#3d-transform-effect-group)
-   [Objets Effect](#effect-objects)
-   [Rubriques connexes](#related-topics)

## <a name="what-is-a-directcomposition-effect"></a>Qu’est-ce qu’un effet DirectComposition ?

Un *effet* DirectComposition est une opération bitmap qui est appliquée lors de la pixellisation d’un visuel pour modifier l’apparence du visuel d’une certaine façon.

DirectComposition crée un effet en acceptant une sous-arborescence visuelle et en la rendant dans une seule bitmap avant d’appliquer l’effet. Par exemple, pour créer un effet de transformation de perspective 3D, DirectComposition produit une image d’une sous-arborescence visuelle, puis texture l’image sur un plan 3D qui est transformé en fonction de la matrice résultante de l’effet de transformation 3D.

DirectComposition prend en charge les types d’effets suivants.



| Type d’effet                                                   | Description                                                                |
|---------------------------------------------------------------|----------------------------------------------------------------------------|
| [Opacity](#opacity)                                           | Définit l’opacité d’un visuel entier.                                      |
| [transformation de perspective 3D](#3d-perspective-transform-effects) | Applique un effet de transformation de perspective à trois dimensions (3D) à un visuel. |



 

> [!Note]  
> DirectComposition n’effectue pas de traitement spécial lors de l’application d’effets à du contenu stéréo 3D. Cela signifie que le contenu 3D peut apparaître disproportionné lorsqu’un effet est appliqué à celui-ci.

 

## <a name="opacity"></a>Opacity

L’effet d’opacité vous permet de définir le facteur d’opacité appliqué à un visuel entier lorsque l’élément visuel est rendu. Il diffère d’un masque Alpha en ce que le même facteur d’opacité est appliqué à tous les pixels du visuel. L’opacité est spécifiée sous la forme d’une valeur comprise entre 0 (complètement transparent) et 1 (entièrement opaque).

Le facteur d’opacité est appliqué du visuel parent aux éléments visuels enfants, mais les effets visibles des paramètres d’opacité imbriquée ne sont pas indiqués dans la valeur de la propriété des visuels enfants individuels. Par exemple, si un visuel racine a une opacité de 50% (0,5) et qu’un de ses enfants a une opacité de 20% (0,2), l’opacité nette pour cet enfant est rendue sous la forme de 10% (0,1), mais la valeur de la propriété opacité de l’enfant est toujours de 0,2.

## <a name="3d-perspective-transform-effects"></a>effets de transformation de perspective 3D

Cette section décrit l’espace de coordonnées utilisé par DirectComposition pour effectuer des effets de transformation de perspective 3D. Elle décrit également les types d’effets de transformation de perspective 3D pris en charge par DirectComposition.

-   [Espace de coordonnées 3D DirectComposition](#the-directcomposition-3d-coordinate-space)
-   [effet de transformation de rotation 3D](#3d-rotation-transform-effect)
-   [effet de transformation de mise à l’échelle 3D](#3d-scaling-transform-effect)
-   [effet de transformation de translation 3D](#3d-translation-transform-effect)
-   [transformation de matrice 3D, effet](#3d-matrix-transform-effect)
-   [Groupe d’effets de transformation 3D](#3d-transform-effect-group)

> [!Note]  
> Dans DirectComposition, l’application d’effets 3D à plusieurs niveaux dans l’arborescence d’éléments visuels ne fonctionne pas de la même manière qu’avec un moteur 3D complet tel que Microsoft Direct3D. Par exemple, imaginez un visuel parent qui a un seul visuel enfant. Si le visuel enfant pivote vers l’avant dans la direction z (autour de l’axe des y) de 90 degrés, le bord du côté visuel enfant est confronté à la visionneuse, ce qui signifie que le visuel n’est pas visible (car une image bitmap n’a pas de profondeur réelle). Si le visuel parent est ensuite pivoté vers l’arrière dans la direction z négative (autour de l’axe des y) de 90 degrés, le visuel enfant peut s’attendre à être entièrement visible (puisque les transformations sont inversées). Toutefois, dans DirectComposition, ce n’est pas le cas. Le visuel enfant n’est pas visible, car il a été « aplati » dans la bitmap parente.

 

### <a name="the-directcomposition-3d-coordinate-space"></a>Espace de coordonnées 3D DirectComposition

L’espace de coordonnées DirectComposition pour les effets de transformation 3D localise l’origine (0, 0, 0) dans le coin supérieur gauche de la surface de la bitmap, avec les valeurs positives de l’axe des x qui se poursuivent à droite, les valeurs positives de l’axe des y continuant vers le bas, et les valeurs positives de l’axe z qui continuent vers l’extérieur de l’origine Cette illustration montre l’espace de coordonnées 3D DirectComposition.

![espace de coordonnées 3D directcompostion](images/3d-coordinate-space.png)

### <a name="3d-rotation-transform-effect"></a>effet de transformation de rotation 3D

Un effet de transformation de rotation 3D fait pivoter un visuel dans trois dimensions selon l’angle spécifié à propos d’un vecteur d’axe de rotation \[ x, y, z \] situé sur le point central spécifié (x, y, z). L’angle est spécifié en degrés. Le vecteur de l’axe de rotation par défaut est \[ 0,-1 \] et le point central par défaut est (0, 0, 0).

Utilisez la méthode [**IDCompositionDevice :: CreateRotateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform3d) pour créer un objet de transformation de rotation 3D. La méthode récupère une interface [**IDCompositionRotateTransform3D**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform3d) que vous pouvez utiliser pour définir les propriétés de l’objet.

### <a name="3d-scaling-transform-effect"></a>effet de transformation de mise à l’échelle 3D

Un effet de transformation de mise à l’échelle 3D rend un visuel plus grand ou plus petit. Il met à l’échelle un visuel dans la \[ direction x, y, z \] autour du point central (x, y, z). Le point central par défaut est (0, 0, 0).

Utilisez la méthode [**IDCompositionDevice :: CreateScaleTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform3d) pour créer un objet de transformation de mise à l’échelle 3D. La méthode récupère une interface [**IDCompositionScaleTransform3D**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform3d) que vous pouvez utiliser pour définir les propriétés de l’objet.

### <a name="3d-translation-transform-effect"></a>effet de transformation de translation 3D

Un effet de transformation de translation 3D modifie la position d’un visuel dans la \[ direction x, y, z \] .

Utilisez la méthode [**IDCompositionDevice :: CreateTranslateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtranslatetransform3d) pour créer un objet de transformation de traduction 3D. La méthode récupère une interface [**IDCompositionTranslateTransform3D**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform3d) que vous pouvez utiliser pour définir les propriétés de l’objet.

### <a name="3d-matrix-transform-effect"></a>transformation de matrice 3D, effet

L’interface [**IDCompositionMatrixTransform3D**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform) vous permet de définir votre propre matrice de transformation 4 par 4 et de l’appliquer à un visuel. Cette interface est utile si vous devez appliquer un type d’effet de transformation de perspective 3D qui n’est pas disponible via les autres interfaces d’effet de transformation 3D DirectComposition. Vous définissez la matrice en remplissant une structure [**D3DMATRIX**](/windows/desktop/direct3d10/d3d10-d3dmatrix) et en la passant à la méthode [**IDCompositionMatrixTransform3D :: SetMatrix**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrix) . Vous pouvez également définir chaque élément de la matrice à l’aide de la méthode [**IDCompositionMatrixTransform3D :: SetMatrixElement**](/previous-versions/windows/desktop/legacy/hh437429(v=vs.85)) .

### <a name="3d-transform-effect-group"></a>Groupe d’effets de transformation 3D

[**IDCompositionDevice :: CreateTransform3DGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransform3dgroup) crée une collection d’effets de transformation 3D que vous pouvez appliquer à un visuel en tant que groupe. Le tableau peut inclure un nombre quelconque d’objets Transform et peut inclure des transformations de matrice, de rotation, de mise à l’échelle et de translation. La collection d’objets transformation 3D entraîne une transformation dont la valeur est la multiplication de matrice des matrices de transformation individuelles dans la collection.

L’ordre des transformations individuelles dans le groupe est important. Par exemple, si vous faites pivoter, puis mettez à l’échelle, puis Traduisez, vous obtenez un résultat différent de celui que vous convertissiez, puis faites pivoter, puis mettez à l’échelle. DirectComposition respecte l’ordre dans lequel vous spécifiez les transformations 3D dans un groupe transformer en 3D de la même façon que pour les transformations 2D. En outre, les transformations de perspective 3D entraînent l’aplatissement de l’arborescence d’éléments visuels après l’application de toutes les transformations 3D de l’objet visuel en cours. Cela permet de s’assurer que la scène semble aussi proche que possible de la 3D.

## <a name="effect-objects"></a>Objets Effect

Pour appliquer un effet à un visuel, vous devez d’abord créer et définir les propriétés d’un objet Effect qui représente le type d’effet que vous souhaitez produire sur le visuel. Ensuite, vous devez appliquer l’objet Effect à la propriété Effect du visuel.

Pour créer un objet Effect, utilisez l’une des méthodes d’interface [**IDCompositionDevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) suivantes pour créer un objet Effect pour le type d’effet de votre choix. Les méthodes suivantes créent des objets Effects :

-   [**CreateMatrixTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-creatematrixtransform3d)
-   [**CreateRotateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform3d)
-   [**CreateScaleTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform3d)
-   [**CreateTranslateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtranslatetransform3d)

Chacune des méthodes précédentes récupère une interface que vous pouvez utiliser pour définir les propriétés de l’objet Effect nouvellement créé. Utilisez les méthodes d’interface pour définir les propriétés en fonction des besoins afin de produire l’effet visuel souhaité.

La plupart des propriétés d’un objet Effect peuvent être animées. Pour animer une propriété particulière, créez un objet d’animation et appliquez-le à la propriété que vous souhaitez animer. Sinon, affectez à la propriété une valeur statique qui produit l’effet souhaité. Pour plus d’informations sur l’animation des propriétés, consultez [animation](animation.md).

Pour appliquer un objet Effect à Visual, appelez la méthode [**IDCompositionVisual :: SetEffect**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-seteffect) . Lorsque vous appliquez un effet à un visuel, l’effet est appliqué à l’ensemble de la sous-arborescence d’éléments visuels enracinée sur cet visuel. Ainsi, par exemple, si vous définissez l’opacité d’un visuel sur 50 pour cent, l’opacité de tous les éléments visuels enfants dans la sous-arborescence visuelle sera réduite de 50%. Vous pouvez appliquer le même objet Effects à un ou plusieurs visuels. Si vous modifiez les propriétés d’un objet Effect après l’avoir appliqué aux éléments visuels, tous les visuels sont recomposés pour refléter la modification.

À l’aide d’un objet de groupe d’effets, vous pouvez appliquer simultanément plusieurs effets à un visuel. Tout d’abord, appelez [**IDCompositionDevice :: CreateEffectGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createeffectgroup) pour créer l’objet de groupe d’effets, puis ajoutez des effets au groupe à l’aide de l’interface [**IDCompositionEffectGroup**](/windows/win32/api/dcomp/nn-dcomp-idcompositioneffectgroup) de l’objet.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 