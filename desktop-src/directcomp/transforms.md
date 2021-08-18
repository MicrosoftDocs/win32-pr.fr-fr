---
title: Transformations (DirectComposition)
description: Cette rubrique traite de la prise en charge de Microsoft DirectComposition pour les transformations affines (linéaire) à deux dimensions (2D) et décrit les types de transformations pris en charge par DirectComposition.
ms.assetid: a0f41cc6-e848-4831-8063-609e17d9b4c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c8cc34975ab8304300a1523269808775107f4ce0554432da8c3c04a01f25881
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504812"
---
# <a name="transforms-directcomposition"></a>Transformations (DirectComposition)

> [!NOTE]
> pour les applications sur Windows 10, nous vous recommandons d’utiliser des api Windows. UI. Composition au lieu de DirectComposition. Pour plus d’informations, consultez [moderniser votre application de bureau à l’aide de la couche visuelle](/windows/uwp/composition/visual-layer-in-desktop-apps).

Cette rubrique traite de la prise en charge de Microsoft DirectComposition pour les transformations affines (linéaire) à deux dimensions (2D) et décrit les types de transformations pris en charge par DirectComposition.

DirectComposition prend également en charge les transformations de perspective 3D, mais étant donné qu’elles nécessitent la création d’une bitmap intermédiaire, DirectComposition les considère comme des effets plutôt que des transformations. Pour plus d’informations sur les effets de transformation de perspective 3D, consultez [Effects](effects.md).

Cette rubrique comporte les sections suivantes :

-   [Qu’est-ce qu’une transformation 2D DirectComposition ?](#what-is-a-directcomposition-2d-transform)
-   [Espace de coordonnées 2D DirectComposition](#the-directcomposition-2d-coordinate-space)
-   [Prise en charge des transformations 2D affines](#support-for-affine-2d-transforms)
-   [Transformations 2D de la matrice](#matrix-2d-transforms)
-   [Groupes de transformations](#transform-groups)
-   [Transformer l’animation](#transform-animation)
-   [Rubriques connexes](#related-topics)

## <a name="what-is-a-directcomposition-2d-transform"></a>Qu’est-ce qu’une transformation 2D DirectComposition ?

Une transformation 2D vous permet de modifier la position, la taille ou la nature d’un visuel dans deux dimensions en le déplaçant vers un autre emplacement (translation), en le rendant plus grand ou plus petit (mise à l’échelle), en le transformant (rotation) ou en distorsion de sa forme (inclinaison).

Une transformation 2D est obtenue en mappant les points d’un visuel d’une position à l’autre dans le même espace de coordonnées, ou d’un espace de coordonnées à un autre. Ce mappage est décrit par une table de valeurs appelée matrice de transformation, définie sous la forme d’une collection de trois lignes avec trois colonnes de valeurs à virgule flottante, comme indiqué dans le tableau suivant.

:::row:::
    :::column:::
        M11Default : 1,0<br/>
        M21Default : 0,0<br/>
        M31OffsetX : 0,0
    :::column-end:::
    :::column:::
        M12Default : 0,0<br/>
        M22Default : 1,0<br/>
        M32OffsetY : 0,0
    :::column-end:::
    :::column:::
        0.0<br/>
        0.0<br/>
        1.0
    :::column-end:::
:::row-end:::

La matrice de transformation pour les transformations 2D affines est une matrice 3 par 2 qui omet la troisième colonne de la matrice de transformation précédente. Le tableau suivant montre la disposition de cette matrice.

:::row:::
    :::column:::
        M11Default : 1,0<br/>
        M21Default : 0,0<br/>
        M31OffsetX : 0,0
    :::column-end:::
    :::column:::
        M12Default : 0,0<br/>
        M22Default : 1,0<br/>
        M32OffsetY : 0,0
    :::column-end:::
:::row-end:::

> [!Note]  
> DirectComposition n’effectue pas de traitement spécial lors de l’application de transformations 2D au contenu stéréo. Cela signifie que le contenu 3D peut apparaître disproportionné lorsqu’une transformation 2D est appliquée.

 

## <a name="the-directcomposition-2d-coordinate-space"></a>Espace de coordonnées 2D DirectComposition

DirectComposition utilise un espace de coordonnées 2D de gauche. autrement dit, les valeurs positives de l’axe des x augmentent vers la droite et les valeurs positives de l’axe des y augmentent vers le bas. Les éléments visuels sont positionnés par rapport à l’origine, qui est le point d’intersection de l’axe x et de l’axe y (0,0), comme indiqué dans l’illustration suivante.

![axe x et axe y d’un espace de coordonnées droitier](images/coordinatespace.png)

En manipulant des valeurs dans une matrice de transformation 3 par 2, vous pouvez faire pivoter, mettre à l’échelle, incliner et traduire un objet en deux dimensions. Par exemple, si vous définissez OffsetX sur 100 et OffsetY sur 200, vous déplacez l’objet vers la droite de 100 pixels et de 200 pixels.

## <a name="support-for-affine-2d-transforms"></a>Prise en charge des transformations 2D affines

Le tableau suivant décrit les types de transformations 2D affines pris en charge par DirectComposition et répertorie les interfaces que vous pouvez utiliser pour effectuer les différents types de transformations.



| Transformation/interface                                                                               | Description                                                                                              | Illustration                                                                                                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Faire pivoter le saut de ligne [**Idcompositionrotatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform)2D \[\]          | faire pivoter un visuel selon l’angle spécifié par-dessus le point central spécifié.                                 | ![illustration d’un carré pivoté de 45 degrés dans le sens des aiguilles d’une montre autour du centre du carré d’origine](images/rotate.png)               |
| Mettre à l’échelle le saut de ligne [**Idcompositionscaletransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)2D \[\]             | mettre à l’échelle un visuel par le facteur spécifié à propos du point central spécifié.                                 | ![illustration d’une mise à l’échelle carrée de 130%](images/scale.png)                                                                  |
| Incliner le saut de ligne [**Idcompositionskewtransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)2D \[\]                | incliner un visuel selon l’angle spécifié le long de l’axe x et de l’axe y, et autour du point central spécifié. | ![illustration d’un carré incliné de 30 degrés dans le sens inverse des aiguilles d’une montre à partir de l’axe y](images/skew.png)                                   |
| Traduire le[](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform) \[ saut de ligne idcompositiontranslatetransform 2D\] | modifier la position d’un visuel dans la direction de l’axe x et de l’axe y.                               | ![illustration d’un carré déplacé de 20 unités le long de l’axe x positif et de 10 unités le long de l’axe y positif](images/translate.png) |



 

## <a name="matrix-2d-transforms"></a>Transformations 2D de la matrice

L’interface [**IDCompositionMatrixTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform) vous permet de définir votre propre matrice de transformation 2D affine 3-by-2 et de l’appliquer à un visuel. Cette interface est utile si vous devez appliquer un type de transformation 2D affine qui n’est pas disponible via les autres interfaces de transformation DirectComposition. Vous définissez la matrice en remplissant une [**structure \_ \_ matrice \_ F de matrice D2D**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) et en la passant à la méthode [**IDCompositionMatrixTransform :: SetMatrix**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrix) .

## <a name="transform-groups"></a>Groupes de transformations

Vous pouvez utiliser des groupes de transformation pour combiner plusieurs transformations en une seule. Un groupe de transformations définit une collection d’objets de transformation dont les matrices sont multipliées dans l’ordre dans lequel ils sont spécifiés dans la collection. La matrice de transformation qui en résulte est ensuite appliquée à l’éléments visuels. Un groupe de transformations produit le même résultat que l’application de chaque transformation séparément.

Gardez à l’esprit que l’ordre des objets de transformation dans un groupe de transformations est important. Par exemple, si un visuel est d’abord pivoté, puis mis à l’échelle, puis traduit, le résultat est différent si le visuel est traduit pour la première fois, puis pivoté, puis mis à l’échelle. DirectComposition applique toujours les transformations à un visuel dans l’ordre dans lequel elles sont spécifiées dans la collection.

Pour créer un groupe de transformations, commencez par créer les objets de transformation que vous souhaitez inclure dans le groupe, puis transmettez un tableau de pointeurs d’objet de transformation à la méthode [**IDCompositionDevice :: CreateTransformGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) . Après avoir créé un groupe de transformations, vous ne pouvez pas ajouter ou supprimer des objets de transformation. Toutefois, vous pouvez modifier les propriétés des objets de transformation individuels dans la collection, et les modifications sont reflétées dans la matrice de transformation résultante.

## <a name="transform-animation"></a>Transformer l’animation

Les propriétés d’une transformation peuvent être animées. Quand une propriété est animée, DirectComposition modifie la valeur de la propriété au fil du temps, plutôt qu’en une seule fois. Cela s’avère particulièrement utile lors de la création de transitions. Pour plus d’informations, consultez [animation](animation.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 
