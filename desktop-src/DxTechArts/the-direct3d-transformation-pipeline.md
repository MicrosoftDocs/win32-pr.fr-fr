---
title: Pipeline de transformation Direct3D
description: Cet article fournit une explication technique pour les développeurs d’applications Direct3D sur la manière de définir les paramètres du pipeline de transformation Direct3D en manipulant directement les matrices Direct3D.
ms.assetid: 48ae49f0-1162-c292-4bd4-34da5aadd2df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2b97a87293a840ccd9641b1418c2005cf73a855
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "103869325"
---
# <a name="the-direct3d-transformation-pipeline"></a><span data-ttu-id="b9054-103">Pipeline de transformation Direct3D</span><span class="sxs-lookup"><span data-stu-id="b9054-103">The Direct3D Transformation Pipeline</span></span>

<span data-ttu-id="b9054-104">Cet article fournit une explication technique pour les développeurs d’applications Direct3D sur la manière de définir les paramètres du pipeline de transformation Direct3D en manipulant directement les matrices Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b9054-104">This article provides a technical explanation for Direct3D application developers on how to set the parameters of the Direct3D Transformation Pipeline by the direct manipulation of Direct3D matrices.</span></span>

-   [<span data-ttu-id="b9054-105">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="b9054-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="b9054-106">Pipeline de transformation</span><span class="sxs-lookup"><span data-stu-id="b9054-106">The Transformation Pipeline</span></span>](#the-transformation-pipeline)
-   [<span data-ttu-id="b9054-107">Conseils d’utilisation</span><span class="sxs-lookup"><span data-stu-id="b9054-107">Usage Tips</span></span>](#usage-tips)

## <a name="overview"></a><span data-ttu-id="b9054-108">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="b9054-108">Overview</span></span>

<span data-ttu-id="b9054-109">Direct3D utilise trois transformations pour modifier vos coordonnées de modèle 3D en coordonnées de pixels (espace à l’écran).</span><span class="sxs-lookup"><span data-stu-id="b9054-109">Direct3D uses three transformations to change your 3D model coordinates into pixel coordinates (screen space).</span></span> <span data-ttu-id="b9054-110">Ces transformations sont la transformation universelle, la transformation de vue et la transformation de projection.</span><span class="sxs-lookup"><span data-stu-id="b9054-110">These transformations are world transform, view transform, and projection transform.</span></span>

<span data-ttu-id="b9054-111">La transformation universelle contrôle la manière dont les coordonnées du modèle sont transformées en coordonnées universelles.</span><span class="sxs-lookup"><span data-stu-id="b9054-111">World transform controls how model coordinates are transformed into world coordinates.</span></span> <span data-ttu-id="b9054-112">La transformation universelle peut inclure des translations, des rotations et des mises à l’échelle, mais elle ne s’applique pas aux lumières.</span><span class="sxs-lookup"><span data-stu-id="b9054-112">World transform can include translations, rotations, and scalings, but it does not apply to lights.</span></span> <span data-ttu-id="b9054-113">Pour plus d’informations sur l’utilisation des transformations universelles, consultez [transformation universelle](/windows/desktop/direct3d9/world-transform).</span><span class="sxs-lookup"><span data-stu-id="b9054-113">For more information on working with world transforms, see [World Transform](/windows/desktop/direct3d9/world-transform).</span></span>

<span data-ttu-id="b9054-114">La transformation de vue contrôle la transition des coordonnées universelles en « espace de caméra », en déterminant la position de la caméra dans le monde.</span><span class="sxs-lookup"><span data-stu-id="b9054-114">View transform controls the transition from world coordinates into "camera space," determining camera position in the world.</span></span> <span data-ttu-id="b9054-115">Pour obtenir un exemple d’utilisation des transformations de vue, consultez [View Transform](/windows/desktop/direct3d9/view-transform).</span><span class="sxs-lookup"><span data-stu-id="b9054-115">For an example of working with view transforms, see [View Transform](/windows/desktop/direct3d9/view-transform).</span></span>

<span data-ttu-id="b9054-116">Transformation de projection change la géométrie de l’espace de l’appareil photo en «espace et applique la distorsion de perspective.</span><span class="sxs-lookup"><span data-stu-id="b9054-116">Projection transform changes the geometry from camera space into "clip space" and applies perspective distortion.</span></span> <span data-ttu-id="b9054-117">Le terme « espace du clip » fait référence à la façon dont la géométrie est découpée au volume de la vue pendant cette transformation.</span><span class="sxs-lookup"><span data-stu-id="b9054-117">The term "clip space" refers to how the geometry is clipped to the view volume during this transform.</span></span> <span data-ttu-id="b9054-118">Pour obtenir un exemple d’utilisation des transformations de projection, consultez [projection Transform](/windows/desktop/direct3d9/projection-transform).</span><span class="sxs-lookup"><span data-stu-id="b9054-118">For an example of working with projection transforms, see [Projection Transform](/windows/desktop/direct3d9/projection-transform).</span></span>

<span data-ttu-id="b9054-119">Enfin, la géométrie de l’espace de l’élément est transformée en coordonnées en pixels (espace à l’écran).</span><span class="sxs-lookup"><span data-stu-id="b9054-119">Finally, the geometry in clip space is transformed into pixel coordinates (screen space).</span></span> <span data-ttu-id="b9054-120">Cette transformation est contrôlée par les paramètres de la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="b9054-120">This transformation is controlled by the viewport settings.</span></span>

<span data-ttu-id="b9054-121">Les vertex de découpage et de transformation doivent avoir lieu dans un espace homogène (simplement placé, espace dans lequel le système de coordonnées comprend un quatrième élément), mais le résultat final pour la plupart des applications doit être des coordonnées tridimensionnelles (3D) non homogènes définies dans l’espace d’écran.</span><span class="sxs-lookup"><span data-stu-id="b9054-121">Clipping and transforming vertices must take place in homogenous space (simply put, space in which the coordinate system includes a fourth element), but the final result for most applications needs to be non-homogenous three-dimensional (3D) coordinates defined in "screen space."</span></span> <span data-ttu-id="b9054-122">Cela signifie que les vertex d’entrée et le volume de découpage doivent être traduits dans un espace homogène pour exécuter le découpage, puis retraduits en espace non homogène pour être affichés.</span><span class="sxs-lookup"><span data-stu-id="b9054-122">This means that both the input vertices and the clipping volume must be translated into homogenous space to perform the clipping and then translated back into non-homogenous space to be displayed.</span></span>

<span data-ttu-id="b9054-123">Les trois transformations Direct3D (monde, vue et transformation de projection) sont définies par les matrices Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b9054-123">The three Direct3D transformations-world, view, and projection transform-are defined by Direct3D matrices.</span></span> <span data-ttu-id="b9054-124">Une matrice Direct3D est une matrice de 4x4 homogène définie par une structure [**D3DMATRIX**](/windows/desktop/direct3d9/d3dmatrix) .</span><span class="sxs-lookup"><span data-stu-id="b9054-124">A Direct3D matrix is a 4x4 homogenous matrix defined by a [**D3DMATRIX**](/windows/desktop/direct3d9/d3dmatrix) structure.</span></span> <span data-ttu-id="b9054-125">Bien que les matrices Direct3D ne sont pas des objets standard, elles ne sont pas représentées par une interface COM. vous pouvez les créer et les définir comme n’importe quel autre objet Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b9054-125">Although Direct3D matrices are not standard objects-they are not represented by a COM interface-you can create and set them just as you would any other Direct3D object.</span></span> <span data-ttu-id="b9054-126">Pour plus d’informations sur les matrices Direct3D, consultez [transformations](/windows/desktop/direct3d9/transforms).</span><span class="sxs-lookup"><span data-stu-id="b9054-126">For more information on Direct3D matrices, see [Transforms](/windows/desktop/direct3d9/transforms).</span></span>

## <a name="the-transformation-pipeline"></a><span data-ttu-id="b9054-127">Pipeline de transformation</span><span class="sxs-lookup"><span data-stu-id="b9054-127">The Transformation Pipeline</span></span>

<span data-ttu-id="b9054-128">Si un vertex dans la coordonnée du modèle est donné par PM = (XM, YM, ZM, 1), les transformations présentées dans la figure suivante sont appliquées aux coordonnées de calcul de l’écran PS = (XS, distinctes, ZS, WS).</span><span class="sxs-lookup"><span data-stu-id="b9054-128">If a vertex in the model coordinate is given by Pm = (Xm, Ym, Zm, 1), then the transformations shown in the following figure are applied to compute screen coordinates Ps = (Xs, Ys, Zs, Ws).</span></span>

![transformation de l’espace de modèle en espace d’écran](images/d3dxfrm61.gif)

<span data-ttu-id="b9054-130">Voici les descriptions des étapes présentées dans la figure précédente :</span><span class="sxs-lookup"><span data-stu-id="b9054-130">Here are descriptions of the stages that are shown in the preceding figure:</span></span>

1.  <span data-ttu-id="b9054-131">Le Mworld de la matrice universelle transforme les vertex de l’espace du modèle en espace universel.</span><span class="sxs-lookup"><span data-stu-id="b9054-131">World matrix Mworld transforms vertices from the model space to the world space.</span></span> <span data-ttu-id="b9054-132">Cette matrice est définie par :</span><span class="sxs-lookup"><span data-stu-id="b9054-132">This matrix is set by:</span></span>

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_WORLD, matrix address) 
    ```

    <span data-ttu-id="b9054-133">L’implémentation Direct3D suppose que la dernière colonne de cette matrice est (0, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="b9054-133">Direct3D implementation assumes that the last column of this matrix is (0, 0, 0, 1).</span></span> <span data-ttu-id="b9054-134">Aucune erreur n’est retournée si l’utilisateur spécifie une matrice avec une dernière colonne différente, mais l’éclairage et le brouillard sont incorrects.</span><span class="sxs-lookup"><span data-stu-id="b9054-134">No error is returned if the user specifies a matrix with a different last column, but the lighting and fog will be incorrect.</span></span>

2.  <span data-ttu-id="b9054-135">Afficher la matrice mView transforme les sommets de l’espace universel vers l’espace de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="b9054-135">View matrix Mview transforms vertices from the world space to the camera space.</span></span> <span data-ttu-id="b9054-136">Cette matrice est définie par :</span><span class="sxs-lookup"><span data-stu-id="b9054-136">This matrix is set by:</span></span>

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_VIEW, matrix address) 
    ```

    <span data-ttu-id="b9054-137">L’implémentation Direct3D suppose que la dernière colonne de cette matrice est (0, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="b9054-137">Direct3D implementation assumes that the last column of this matrix is (0, 0, 0, 1).</span></span> <span data-ttu-id="b9054-138">Aucune erreur n’est retournée si l’utilisateur spécifie une matrice avec une dernière colonne différente, mais l’éclairage et le brouillard sont incorrects.</span><span class="sxs-lookup"><span data-stu-id="b9054-138">No error is returned if the user specifies a matrix with different last column, but the lighting and fog will be incorrect.</span></span>

3.  <span data-ttu-id="b9054-139">La matrice de projection mproj transforme les vertex de l’espace de l’appareil photo à l’espace de projection.</span><span class="sxs-lookup"><span data-stu-id="b9054-139">Projection matrix Mproj transforms vertices from the camera space to the projection space.</span></span> <span data-ttu-id="b9054-140">Cette matrice est définie par :</span><span class="sxs-lookup"><span data-stu-id="b9054-140">This matrix is set by:</span></span>

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_PROJECTION, matrix address) 
    ```

    <span data-ttu-id="b9054-141">La dernière colonne de la matrice de projection doit être (0, 0, 1, 0) ou (0, 0, a, 0) pour des effets de brouillard et d’éclairage corrects ; (0, 0, 1, 0) le formulaire est préféré.</span><span class="sxs-lookup"><span data-stu-id="b9054-141">The last column of the projection matrix should be (0, 0, 1, 0), or (0, 0, a, 0) for correct fog and lighting effects; (0, 0, 1, 0) form is preferred.</span></span>

    <span data-ttu-id="b9054-142">Le volume de détourage de tous les points XP = (XP, YP, ZP, WP) dans l’espace de projection est défini comme suit :</span><span class="sxs-lookup"><span data-stu-id="b9054-142">Clipping volume for all points Xp = (Xp, Yp, Zp, Wp) in the projection space is defined as:</span></span>

    ``` syntax
        -Wp < Xp <= Wp 
        -Wp < Yp <= Wp 
        0 < Zp <= Wp 
    ```

    <span data-ttu-id="b9054-143">Tous les points qui ne répondent pas à ces équations sont découpés.</span><span class="sxs-lookup"><span data-stu-id="b9054-143">All points that do not satisfy these equations will be clipped.</span></span>

    <span data-ttu-id="b9054-144">Si un volume de vue est défini comme suit :</span><span class="sxs-lookup"><span data-stu-id="b9054-144">If a view volume is defined as:</span></span>

    -   <span data-ttu-id="b9054-145">SW-largeur de la fenêtre d’écran dans l’espace de l’appareil photo dans le plan de découpage</span><span class="sxs-lookup"><span data-stu-id="b9054-145">Sw-screen window width in camera space in near clipping plane</span></span>
    -   <span data-ttu-id="b9054-146">SH-hauteur de la fenêtre d’écran dans l’espace de l’appareil photo dans le plan de découpage</span><span class="sxs-lookup"><span data-stu-id="b9054-146">Sh-screen window height in camera space in near clipping plane</span></span>
    -   <span data-ttu-id="b9054-147">Zn-distance au plan de découpage proche le long des axes Z dans l’espace de caméra</span><span class="sxs-lookup"><span data-stu-id="b9054-147">Zn-distance to the near clipping plane along Z axes in camera space</span></span>
    -   <span data-ttu-id="b9054-148">ZF-distance au plan de découpage lointain le long des axes Z dans l’espace de caméra</span><span class="sxs-lookup"><span data-stu-id="b9054-148">Zf-distance to the far clipping plane along Z axes in camera space</span></span>

    <span data-ttu-id="b9054-149">Ensuite, une matrice de projection de perspective peut être écrite comme suit :</span><span class="sxs-lookup"><span data-stu-id="b9054-149">then a perspective projection matrix could be written as follows:</span></span>

    ![Affiche une matrice de projection de perspective.](images/d3dxfrm62.gif)

    <span data-ttu-id="b9054-151">où mij est membre de mproj.</span><span class="sxs-lookup"><span data-stu-id="b9054-151">where Mij are members of Mproj.</span></span>

    <span data-ttu-id="b9054-152">Pour la projection orthogonale, nous avons :</span><span class="sxs-lookup"><span data-stu-id="b9054-152">For the orthogonal projection we have:</span></span>

    ![projection orthogonale](images/d3dxfrm63.gif)

    <span data-ttu-id="b9054-154">Direct3D suppose que la matrice de projection de la perspective se présente sous la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="b9054-154">Direct3D assumes that the perspective projection matrix has the form:</span></span>

    ![matrice de projection de perspective](images/d3dxfrm64.gif)

    <span data-ttu-id="b9054-156">Si la matrice de projection de la perspective n’a pas cette forme, il y aura des artefacts.</span><span class="sxs-lookup"><span data-stu-id="b9054-156">If the perspective projection matrix does not have this form, there will be some artifacts.</span></span> <span data-ttu-id="b9054-157">Par exemple, le brouillard de table ne fonctionnera pas.</span><span class="sxs-lookup"><span data-stu-id="b9054-157">For example, table fog will not work.</span></span>

4.  <span data-ttu-id="b9054-158">Direct3D permet à l’utilisateur de modifier le volume du clip comme suit :</span><span class="sxs-lookup"><span data-stu-id="b9054-158">Direct3D allows the user to change the clip volume as follows:</span></span>

    ![modifier le volume du clip](images/d3dxfrm65.gif)

    <span data-ttu-id="b9054-160">Elle peut être réécrite comme suit :</span><span class="sxs-lookup"><span data-stu-id="b9054-160">This can be rewritten as:</span></span>

    ![modifier le volume du clip réécrit](images/d3dxfrm66.gif)

    <span data-ttu-id="b9054-162">où :</span><span class="sxs-lookup"><span data-stu-id="b9054-162">where:</span></span>

    ``` syntax
        Cx, Cy - dvClipX, dvClipY from D3DVIEWPORT9  
        Cw, Ch - dvClipWidth, dvClipHeight from D3DVIEWPORT9  
        Zmin, Zmax - dvMinZ, dvMaxZ from D3DVIEWPORT9  
    ```

    <span data-ttu-id="b9054-163">Cette transformation peut fournir une précision accrue et est équivalente à la mise à l’échelle et au décalage du volume de découpage.</span><span class="sxs-lookup"><span data-stu-id="b9054-163">This transformation can provide increased precision and is equivalent to scaling and shifting the clipping volume.</span></span>

    <span data-ttu-id="b9054-164">La matrice Mclip correspondante est la suivante :</span><span class="sxs-lookup"><span data-stu-id="b9054-164">The corresponding Mclip matrix is:</span></span>

    ![matrice mclip](images/d3dxfrm67.gif)

    <span data-ttu-id="b9054-166">Un vertex est transformé par :</span><span class="sxs-lookup"><span data-stu-id="b9054-166">A vertex is transformed by:</span></span>

    ``` syntax
        dvClipWidth = 2   
        dvClipHeight = 2   
        dvClipX = -1   
        dvClipY = 1   
        dvMinZ = 0   
        dvMaxZ = 1   
    ```

    <span data-ttu-id="b9054-167">Si vous ne souhaitez pas mettre à l’échelle le volume du clip, vous pouvez définir les paramètres de la fenêtre d’affichage sur les valeurs par défaut :</span><span class="sxs-lookup"><span data-stu-id="b9054-167">If you do not want to scale the clip volume, you can set viewport parameters to default values:</span></span>

    ``` syntax
        (Xc, Yc, Zc, Wc) = (Xp, Yp, Zp, Wp) * Mclip   
    ```

5.  <span data-ttu-id="b9054-168">L’étape de découpage est facultative si l’utilisateur spécifie l' \_ indicateur D3DDP DONOTCLIP dans un appel DrawPrimitive.</span><span class="sxs-lookup"><span data-stu-id="b9054-168">The clipping stage is optional if the user specifies the D3DDP\_DONOTCLIP flag in a DrawPrimitive call.</span></span> <span data-ttu-id="b9054-169">Dans ce cas, toutes les matrices (y compris MVS) peuvent être combinées.</span><span class="sxs-lookup"><span data-stu-id="b9054-169">In this case, all matrices (including Mvs) can be combined.</span></span>
6.  <span data-ttu-id="b9054-170">La matrice de mise à l’échelle de la fenêtre MVS met à l’échelle les coordonnées à l’intérieur de la fenêtre d’affichage et retourne l’axe Y du haut vers le haut :</span><span class="sxs-lookup"><span data-stu-id="b9054-170">The viewport scale matrix Mvs scales coordinates to be within the viewport window and flips the Y axis from up to down:</span></span>

    ![matrice de mise à l’échelle Viewport MVS](images/d3dxfrm68.gif)

    <span data-ttu-id="b9054-172">où :</span><span class="sxs-lookup"><span data-stu-id="b9054-172">where:</span></span>

    ``` syntax
        dwX, dwY - viewport offsets in pixels from D3DVIEWPORT9 
        dwWidth, dwHeight - viewport width and height in pixels from D3DVIEWPORT9    
    ```

7.  <span data-ttu-id="b9054-173">Enfin, les coordonnées d’écran sont calculées et transmises au rastériseur :</span><span class="sxs-lookup"><span data-stu-id="b9054-173">Finally, screen coordinates are computed and passed to the rasterizer:</span></span>

    ![coordonnées d’écran calculées et transmises au rastériseur](images/d3dxfrm69.gif)

## <a name="usage-tips"></a><span data-ttu-id="b9054-175">Conseils d’utilisation</span><span class="sxs-lookup"><span data-stu-id="b9054-175">Usage Tips</span></span>

<span data-ttu-id="b9054-176">Voici quelques conseils pour utiliser le pipeline de transformation Direct3D :</span><span class="sxs-lookup"><span data-stu-id="b9054-176">Here are some tips for how to use the Direct3D Transformation Pipeline:</span></span>

-   <span data-ttu-id="b9054-177">La dernière colonne des matrices de monde et de vue doit être (0, 0, 0, 1), sinon l’éclairage sera incorrect.</span><span class="sxs-lookup"><span data-stu-id="b9054-177">The last column of the world and view matrices should be (0, 0, 0, 1), or the lighting will be incorrect.</span></span>
-   <span data-ttu-id="b9054-178">Définissez les paramètres de la fenêtre d’affichage pour générer une matrice de Mclip d’identité, sauf si vous comprenez exactement ce qui est nécessaire pour.</span><span class="sxs-lookup"><span data-stu-id="b9054-178">Set the viewport parameters to build an identity Mclip matrix, unless you understand exactly what it is needed for.</span></span>

    ``` syntax
        dvClipWidth = 2 
        dvClipHeight = 2
        dvClipX = -1
        dvClipY = 1
        dvMinZ = 0 
        dvMaxZ = 1
    ```

 

 