---
title: Transformations (DirectComposition)
description: Cette rubrique traite de la prise en charge de Microsoft DirectComposition pour les transformations affines (linéaire) à deux dimensions (2D) et décrit les types de transformations pris en charge par DirectComposition.
ms.assetid: a0f41cc6-e848-4831-8063-609e17d9b4c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 991e1205422864efdec82bbd4067b9c7662aaf29
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118654"
---
# <a name="transforms-directcomposition"></a><span data-ttu-id="d6c1b-103">Transformations (DirectComposition)</span><span class="sxs-lookup"><span data-stu-id="d6c1b-103">Transforms (DirectComposition)</span></span>

> [!NOTE]
> <span data-ttu-id="d6c1b-104">Pour les applications sur Windows 10, nous vous recommandons d’utiliser des API Windows. UI. composition au lieu de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="d6c1b-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="d6c1b-105">Pour plus d’informations, consultez [moderniser votre application de bureau à l’aide de la couche visuelle](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="d6c1b-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="d6c1b-106">Cette rubrique traite de la prise en charge de Microsoft DirectComposition pour les transformations affines (linéaire) à deux dimensions (2D) et décrit les types de transformations pris en charge par DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="d6c1b-106">This topic discusses Microsoft DirectComposition support for two-dimensional (2D) affine (linear) transforms, and describes the types of transforms that DirectComposition supports.</span></span>

<span data-ttu-id="d6c1b-107">DirectComposition prend également en charge les transformations de perspective 3D, mais étant donné qu’elles nécessitent la création d’une bitmap intermédiaire, DirectComposition les considère comme des effets plutôt que des transformations.</span><span class="sxs-lookup"><span data-stu-id="d6c1b-107">DirectComposition also supports 3D perspective transforms, but because they require the creation of an intermediate bitmap, DirectComposition considers them to be effects rather than transforms.</span></span> <span data-ttu-id="d6c1b-108">Pour plus d’informations sur les effets de transformation de perspective 3D, consultez [Effects](effects.md).</span><span class="sxs-lookup"><span data-stu-id="d6c1b-108">For information about 3D perspective transform effects, see [Effects](effects.md).</span></span>

<span data-ttu-id="d6c1b-109">Cette rubrique comporte les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="d6c1b-109">This topic includes the following sections:</span></span>

-   [<span data-ttu-id="d6c1b-110">Qu’est-ce qu’une transformation 2D DirectComposition ?</span><span class="sxs-lookup"><span data-stu-id="d6c1b-110">What is a DirectComposition 2D transform?</span></span>](#what-is-a-directcomposition-2d-transform)
-   [<span data-ttu-id="d6c1b-111">Espace de coordonnées 2D DirectComposition</span><span class="sxs-lookup"><span data-stu-id="d6c1b-111">The DirectComposition 2D coordinate space</span></span>](#the-directcomposition-2d-coordinate-space)
-   [<span data-ttu-id="d6c1b-112">Prise en charge des transformations 2D affines</span><span class="sxs-lookup"><span data-stu-id="d6c1b-112">Support for affine 2D transforms</span></span>](#support-for-affine-2d-transforms)
-   [<span data-ttu-id="d6c1b-113">Transformations 2D de la matrice</span><span class="sxs-lookup"><span data-stu-id="d6c1b-113">Matrix 2D transforms</span></span>](#matrix-2d-transforms)
-   [<span data-ttu-id="d6c1b-114">Groupes de transformations</span><span class="sxs-lookup"><span data-stu-id="d6c1b-114">Transform Groups</span></span>](#transform-groups)
-   [<span data-ttu-id="d6c1b-115">Transformer l’animation</span><span class="sxs-lookup"><span data-stu-id="d6c1b-115">Transform animation</span></span>](#transform-animation)
-   [<span data-ttu-id="d6c1b-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d6c1b-116">Related topics</span></span>](#related-topics)

## <a name="what-is-a-directcomposition-2d-transform"></a><span data-ttu-id="d6c1b-117">Qu’est-ce qu’une transformation 2D DirectComposition ?</span><span class="sxs-lookup"><span data-stu-id="d6c1b-117">What is a DirectComposition 2D transform?</span></span>

<span data-ttu-id="d6c1b-118">Une transformation 2D vous permet de modifier la position, la taille ou la nature d’un visuel dans deux dimensions en le déplaçant vers un autre emplacement (translation), en le rendant plus grand ou plus petit (mise à l’échelle), en le transformant (rotation) ou en distorsion de sa forme (inclinaison).</span><span class="sxs-lookup"><span data-stu-id="d6c1b-118">A 2D transform enables you to alter the position, size, or nature of a visual in two dimensions by moving the visual to another location (translation), making it larger or smaller (scaling), turning it (rotation), or distorting its shape (skewing).</span></span>

<span data-ttu-id="d6c1b-119">Une transformation 2D est obtenue en mappant les points d’un visuel d’une position à l’autre dans le même espace de coordonnées, ou d’un espace de coordonnées à un autre.</span><span class="sxs-lookup"><span data-stu-id="d6c1b-119">A 2D transform is achieved by mapping the points of a visual from one position to another within the same coordinate space, or from one coordinate space to another.</span></span> <span data-ttu-id="d6c1b-120">Ce mappage est décrit par une table de valeurs appelée matrice de transformation, définie sous la forme d’une collection de trois lignes avec trois colonnes de valeurs à virgule flottante, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d6c1b-120">This mapping is described by a table of values called a transformation matrix, defined as a collection of three rows with three columns of floating-point values as shown in the following table.</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="d6c1b-121">M11Default : 1,0</span><span class="sxs-lookup"><span data-stu-id="d6c1b-121">M11Default: 1.0</span></span><br/>
        <span data-ttu-id="d6c1b-122">M21Default : 0,0</span><span class="sxs-lookup"><span data-stu-id="d6c1b-122">M21Default: 0.0</span></span><br/>
        <span data-ttu-id="d6c1b-123">M31OffsetX : 0,0</span><span class="sxs-lookup"><span data-stu-id="d6c1b-123">M31OffsetX: 0.0</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="d6c1b-124">M12Default : 0,0</span><span class="sxs-lookup"><span data-stu-id="d6c1b-124">M12Default: 0.0</span></span><br/>
        <span data-ttu-id="d6c1b-125">M22Default : 1,0</span><span class="sxs-lookup"><span data-stu-id="d6c1b-125">M22Default: 1.0</span></span><br/>
        <span data-ttu-id="d6c1b-126">M32OffsetY : 0,0</span><span class="sxs-lookup"><span data-stu-id="d6c1b-126">M32OffsetY: 0.0</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="d6c1b-127">0.0</span><span class="sxs-lookup"><span data-stu-id="d6c1b-127">0.0</span></span><br/>
        <span data-ttu-id="d6c1b-128">0.0</span><span class="sxs-lookup"><span data-stu-id="d6c1b-128">0.0</span></span><br/>
        <span data-ttu-id="d6c1b-129">1,0</span><span class="sxs-lookup"><span data-stu-id="d6c1b-129">1.0</span></span>
    :::column-end:::
:::row-end:::

<span data-ttu-id="d6c1b-130">La matrice de transformation pour les transformations 2D affines est une matrice 3 par 2 qui omet la troisième colonne de la matrice de transformation précédente.</span><span class="sxs-lookup"><span data-stu-id="d6c1b-130">The transformation matrix for affine 2D transforms is a 3-by-2 matrix that omits the third column from the previous transformation matrix.</span></span> <span data-ttu-id="d6c1b-131">Le tableau suivant montre la disposition de cette matrice.</span><span class="sxs-lookup"><span data-stu-id="d6c1b-131">The following table shows the layout of this matrix.</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="d6c1b-132">M11Default : 1,0</span><span class="sxs-lookup"><span data-stu-id="d6c1b-132">M11Default: 1.0</span></span><br/>
        <span data-ttu-id="d6c1b-133">M21Default : 0,0</span><span class="sxs-lookup"><span data-stu-id="d6c1b-133">M21Default: 0.0</span></span><br/>
        <span data-ttu-id="d6c1b-134">M31OffsetX : 0,0</span><span class="sxs-lookup"><span data-stu-id="d6c1b-134">M31OffsetX: 0.0</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="d6c1b-135">M12Default : 0,0</span><span class="sxs-lookup"><span data-stu-id="d6c1b-135">M12Default: 0.0</span></span><br/>
        <span data-ttu-id="d6c1b-136">M22Default : 1,0</span><span class="sxs-lookup"><span data-stu-id="d6c1b-136">M22Default: 1.0</span></span><br/>
        <span data-ttu-id="d6c1b-137">M32OffsetY : 0,0</span><span class="sxs-lookup"><span data-stu-id="d6c1b-137">M32OffsetY: 0.0</span></span>
    :::column-end:::
:::row-end:::

> [!Note]  
> <span data-ttu-id="d6c1b-138">DirectComposition n’effectue pas de traitement spécial lors de l’application de transformations 2D au contenu stéréo.</span><span class="sxs-lookup"><span data-stu-id="d6c1b-138">DirectComposition does no special processing when applying 2D transforms to stereo content.</span></span> <span data-ttu-id="d6c1b-139">Cela signifie que le contenu 3D peut apparaître disproportionné lorsqu’une transformation 2D est appliquée.</span><span class="sxs-lookup"><span data-stu-id="d6c1b-139">This means the 3D content might appear distorted when a 2D transform is applied to it.</span></span>

 

## <a name="the-directcomposition-2d-coordinate-space"></a><span data-ttu-id="d6c1b-140">Espace de coordonnées 2D DirectComposition</span><span class="sxs-lookup"><span data-stu-id="d6c1b-140">The DirectComposition 2D coordinate space</span></span>

<span data-ttu-id="d6c1b-141">DirectComposition utilise un espace de coordonnées 2D de gauche. autrement dit, les valeurs positives de l’axe des x augmentent vers la droite et les valeurs positives de l’axe des y augmentent vers le bas.</span><span class="sxs-lookup"><span data-stu-id="d6c1b-141">DirectComposition uses a left-handed 2D coordinate space; that is, positive x-axis values increase to the right and positive y-axis values increase downward.</span></span> <span data-ttu-id="d6c1b-142">Les éléments visuels sont positionnés par rapport à l’origine, qui est le point d’intersection de l’axe x et de l’axe y (0,0), comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="d6c1b-142">Visuals are positioned relative to the origin, which is the point where the x-axis and y-axis intersect (0, 0), as shown in the following illustration.</span></span>

![axe x et axe y d’un espace de coordonnées droitier](images/coordinatespace.png)

<span data-ttu-id="d6c1b-144">En manipulant des valeurs dans une matrice de transformation 3 par 2, vous pouvez faire pivoter, mettre à l’échelle, incliner et traduire un objet en deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="d6c1b-144">By manipulating values in a 3-by-2 transformation matrix, you can rotate, scale, skew, and translate an object in two dimensions.</span></span> <span data-ttu-id="d6c1b-145">Par exemple, si vous définissez OffsetX sur 100 et OffsetY sur 200, vous déplacez l’objet vers la droite de 100 pixels et de 200 pixels.</span><span class="sxs-lookup"><span data-stu-id="d6c1b-145">For example, if you set OffsetX to 100 and OffsetY to 200, you move the object to the right 100 pixels and down 200 pixels.</span></span>

## <a name="support-for-affine-2d-transforms"></a><span data-ttu-id="d6c1b-146">Prise en charge des transformations 2D affines</span><span class="sxs-lookup"><span data-stu-id="d6c1b-146">Support for affine 2D transforms</span></span>

<span data-ttu-id="d6c1b-147">Le tableau suivant décrit les types de transformations 2D affines pris en charge par DirectComposition et répertorie les interfaces que vous pouvez utiliser pour effectuer les différents types de transformations.</span><span class="sxs-lookup"><span data-stu-id="d6c1b-147">The following table describes the types of affine 2D transforms supported by DirectComposition, and lists the interfaces that you can use to perform the various types of transformations.</span></span>



| <span data-ttu-id="d6c1b-148">Transformation/interface</span><span class="sxs-lookup"><span data-stu-id="d6c1b-148">Transform/interface</span></span>                                                                               | <span data-ttu-id="d6c1b-149">Description</span><span class="sxs-lookup"><span data-stu-id="d6c1b-149">Description</span></span>                                                                                              | <span data-ttu-id="d6c1b-150">Illustration</span><span class="sxs-lookup"><span data-stu-id="d6c1b-150">Illustration</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6c1b-151">Faire pivoter le saut de ligne [**Idcompositionrotatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform)2D \[\]</span><span class="sxs-lookup"><span data-stu-id="d6c1b-151">Rotate 2D [**idcompositionrotatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform)\[newline\]</span></span>          | <span data-ttu-id="d6c1b-152">faire pivoter un visuel selon l’angle spécifié par-dessus le point central spécifié.</span><span class="sxs-lookup"><span data-stu-id="d6c1b-152">rotate a visual by the specified angle about the specified center point.</span></span>                                 | ![illustration d’un carré pivoté de 45 degrés dans le sens des aiguilles d’une montre autour du centre du carré d’origine](images/rotate.png)               |
| <span data-ttu-id="d6c1b-154">Mettre à l’échelle le saut de ligne [**Idcompositionscaletransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)2D \[\]</span><span class="sxs-lookup"><span data-stu-id="d6c1b-154">Scale 2D [**idcompositionscaletransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)\[newline\]</span></span>             | <span data-ttu-id="d6c1b-155">mettre à l’échelle un visuel par le facteur spécifié à propos du point central spécifié.</span><span class="sxs-lookup"><span data-stu-id="d6c1b-155">scale a visual by the specified factor about the specified center point.</span></span>                                 | ![illustration d’une mise à l’échelle carrée de 130%](images/scale.png)                                                                  |
| <span data-ttu-id="d6c1b-157">Incliner le saut de ligne [**Idcompositionskewtransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)2D \[\]</span><span class="sxs-lookup"><span data-stu-id="d6c1b-157">Skew 2D [**idcompositionskewtransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)\[newline\]</span></span>                | <span data-ttu-id="d6c1b-158">incliner un visuel selon l’angle spécifié le long de l’axe x et de l’axe y, et autour du point central spécifié.</span><span class="sxs-lookup"><span data-stu-id="d6c1b-158">skew a visual by the specified angle along the x-axis and y-axis, and around the specified center point.</span></span> | ![illustration d’un carré incliné de 30 degrés dans le sens inverse des aiguilles d’une montre à partir de l’axe y](images/skew.png)                                   |
| <span data-ttu-id="d6c1b-160">Traduire le[](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform) \[ saut de ligne idcompositiontranslatetransform 2D\]</span><span class="sxs-lookup"><span data-stu-id="d6c1b-160">Translate 2D [**idcompositiontranslatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform)\[newline\]</span></span> | <span data-ttu-id="d6c1b-161">modifier la position d’un visuel dans la direction de l’axe x et de l’axe y.</span><span class="sxs-lookup"><span data-stu-id="d6c1b-161">change the position of a visual in the direction of the x-axis and y-axis.</span></span>                               | ![illustration d’un carré déplacé de 20 unités le long de l’axe x positif et de 10 unités le long de l’axe y positif](images/translate.png) |



 

## <a name="matrix-2d-transforms"></a><span data-ttu-id="d6c1b-163">Transformations 2D de la matrice</span><span class="sxs-lookup"><span data-stu-id="d6c1b-163">Matrix 2D transforms</span></span>

<span data-ttu-id="d6c1b-164">L’interface [**IDCompositionMatrixTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform) vous permet de définir votre propre matrice de transformation 2D affine 3-by-2 et de l’appliquer à un visuel.</span><span class="sxs-lookup"><span data-stu-id="d6c1b-164">The [**IDCompositionMatrixTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform) interface enables you to define your own 3-by-2 affine 2D transform matrix and apply it to a visual.</span></span> <span data-ttu-id="d6c1b-165">Cette interface est utile si vous devez appliquer un type de transformation 2D affine qui n’est pas disponible via les autres interfaces de transformation DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="d6c1b-165">This interface is useful if you need to apply a type of affine 2D transform that is not available through the other DirectComposition transform interfaces.</span></span> <span data-ttu-id="d6c1b-166">Vous définissez la matrice en remplissant une [**structure \_ \_ matrice \_ F de matrice D2D**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) et en la passant à la méthode [**IDCompositionMatrixTransform :: SetMatrix**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrix) .</span><span class="sxs-lookup"><span data-stu-id="d6c1b-166">You define the matrix by filling a [**D2D\_MATRIX\_3X2\_F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) structure and passing it to the [**IDCompositionMatrixTransform::SetMatrix**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrix) method.</span></span>

## <a name="transform-groups"></a><span data-ttu-id="d6c1b-167">Groupes de transformations</span><span class="sxs-lookup"><span data-stu-id="d6c1b-167">Transform Groups</span></span>

<span data-ttu-id="d6c1b-168">Vous pouvez utiliser des groupes de transformation pour combiner plusieurs transformations en une seule.</span><span class="sxs-lookup"><span data-stu-id="d6c1b-168">You can use transform groups to combine multiple transforms into one.</span></span> <span data-ttu-id="d6c1b-169">Un groupe de transformations définit une collection d’objets de transformation dont les matrices sont multipliées dans l’ordre dans lequel ils sont spécifiés dans la collection.</span><span class="sxs-lookup"><span data-stu-id="d6c1b-169">A transform group defines a collection of transform objects whose matrices are multiplied together in the order in which they are specified in the collection.</span></span> <span data-ttu-id="d6c1b-170">La matrice de transformation qui en résulte est ensuite appliquée à l’éléments visuels.</span><span class="sxs-lookup"><span data-stu-id="d6c1b-170">The resulting transform matrix is then applied to the visual.</span></span> <span data-ttu-id="d6c1b-171">Un groupe de transformations produit le même résultat que l’application de chaque transformation séparément.</span><span class="sxs-lookup"><span data-stu-id="d6c1b-171">A transform group produces the same result as applying each transform separately.</span></span>

<span data-ttu-id="d6c1b-172">Gardez à l’esprit que l’ordre des objets de transformation dans un groupe de transformations est important.</span><span class="sxs-lookup"><span data-stu-id="d6c1b-172">Keep in mind that the order of the transform objects in a transform group is important.</span></span> <span data-ttu-id="d6c1b-173">Par exemple, si un visuel est d’abord pivoté, puis mis à l’échelle, puis traduit, le résultat est différent si le visuel est traduit pour la première fois, puis pivoté, puis mis à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="d6c1b-173">For example, if a visual is first rotated, then scaled, and then translated, the result is different than if the visual is first translated, then rotated, and then scaled.</span></span> <span data-ttu-id="d6c1b-174">DirectComposition applique toujours les transformations à un visuel dans l’ordre dans lequel elles sont spécifiées dans la collection.</span><span class="sxs-lookup"><span data-stu-id="d6c1b-174">DirectComposition always applies the transforms to a visual in the order in which they are specified in the collection.</span></span>

<span data-ttu-id="d6c1b-175">Pour créer un groupe de transformations, commencez par créer les objets de transformation que vous souhaitez inclure dans le groupe, puis transmettez un tableau de pointeurs d’objet de transformation à la méthode [**IDCompositionDevice :: CreateTransformGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) .</span><span class="sxs-lookup"><span data-stu-id="d6c1b-175">To create a transform group, first create the transform objects that you want to include in the group, and then pass an array of transform object pointers to the [**IDCompositionDevice::CreateTransformGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) method.</span></span> <span data-ttu-id="d6c1b-176">Après avoir créé un groupe de transformations, vous ne pouvez pas ajouter ou supprimer des objets de transformation.</span><span class="sxs-lookup"><span data-stu-id="d6c1b-176">After you create a transform group, you cannot add or remove any transform objects.</span></span> <span data-ttu-id="d6c1b-177">Toutefois, vous pouvez modifier les propriétés des objets de transformation individuels dans la collection, et les modifications sont reflétées dans la matrice de transformation résultante.</span><span class="sxs-lookup"><span data-stu-id="d6c1b-177">However, you can modify the properties of the individual transform objects in the collection, and the changes will be reflected in the resulting transform matrix.</span></span>

## <a name="transform-animation"></a><span data-ttu-id="d6c1b-178">Transformer l’animation</span><span class="sxs-lookup"><span data-stu-id="d6c1b-178">Transform animation</span></span>

<span data-ttu-id="d6c1b-179">Les propriétés d’une transformation peuvent être animées.</span><span class="sxs-lookup"><span data-stu-id="d6c1b-179">The properties of a transform can be animated.</span></span> <span data-ttu-id="d6c1b-180">Quand une propriété est animée, DirectComposition modifie la valeur de la propriété au fil du temps, plutôt qu’en une seule fois.</span><span class="sxs-lookup"><span data-stu-id="d6c1b-180">When a property is animated, DirectComposition changes the value of the property over time, rather than all at once.</span></span> <span data-ttu-id="d6c1b-181">Cela s’avère particulièrement utile lors de la création de transitions.</span><span class="sxs-lookup"><span data-stu-id="d6c1b-181">This is particularly useful when creating transitions.</span></span> <span data-ttu-id="d6c1b-182">Pour plus d’informations, consultez [animation](animation.md).</span><span class="sxs-lookup"><span data-stu-id="d6c1b-182">For more information, see [Animation](animation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6c1b-183">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d6c1b-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6c1b-184">Concepts DirectComposition</span><span class="sxs-lookup"><span data-stu-id="d6c1b-184">DirectComposition Concepts</span></span>](directcomposition-concepts.md)
</dt> </dl>

 

 
