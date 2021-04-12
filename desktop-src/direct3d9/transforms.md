---
description: La partie de Direct3D qui pousse la géométrie via le pipeline de géométrie de fonction fixe est le moteur de transformation.
ms.assetid: ed52e32f-8fae-4e6f-b908-26e05ce940cc
title: Transformations (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f482ef12c88140c2eff4c61e634fd3297aeaf295
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392880"
---
# <a name="transforms-direct3d-9"></a><span data-ttu-id="0d21e-103">Transformations (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0d21e-103">Transforms (Direct3D 9)</span></span>

<span data-ttu-id="0d21e-104">La partie de Direct3D qui pousse la géométrie via le pipeline de géométrie de fonction fixe est le moteur de transformation.</span><span class="sxs-lookup"><span data-stu-id="0d21e-104">The part of Direct3D that pushes geometry through the fixed function geometry pipeline is the transform engine.</span></span> <span data-ttu-id="0d21e-105">Il localise le modèle et la visionneuse dans le monde entier, projette les sommets pour l’affichage à l’écran et découpe les sommets dans la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="0d21e-105">It locates the model and viewer in the world, projects vertices for display on the screen, and clips vertices to the viewport.</span></span> <span data-ttu-id="0d21e-106">Le moteur de transformation effectue également des calculs d’éclairage pour déterminer les composants diffus et spéculaire à chaque vertex.</span><span class="sxs-lookup"><span data-stu-id="0d21e-106">The transform engine also performs lighting computations to determine diffuse and specular components at each vertex.</span></span>

<span data-ttu-id="0d21e-107">Le pipeline Geometry prend des sommets comme entrée.</span><span class="sxs-lookup"><span data-stu-id="0d21e-107">The geometry pipeline takes vertices as input.</span></span> <span data-ttu-id="0d21e-108">Le moteur de transformation applique les transformations universelles, de vue et de projection aux sommets, découpe le résultat et transmet tout le contenu au rastériseur.</span><span class="sxs-lookup"><span data-stu-id="0d21e-108">The transform engine applies the world, view, and projection transforms to the vertices, clips the result, and passes everything to the rasterizer.</span></span>

<span data-ttu-id="0d21e-109">Au début du pipeline, les vertex d’un modèle sont déclarés par rapport à un système de coordonnées local.</span><span class="sxs-lookup"><span data-stu-id="0d21e-109">At the head of the pipeline, a model's vertices are declared relative to a local coordinate system.</span></span> <span data-ttu-id="0d21e-110">Il s’agit d’une origine locale et d’une orientation.</span><span class="sxs-lookup"><span data-stu-id="0d21e-110">This is a local origin and an orientation.</span></span> <span data-ttu-id="0d21e-111">Cette orientation des coordonnées est souvent appelée espace de modèle, et les coordonnées individuelles sont appelées coordonnées de modèle.</span><span class="sxs-lookup"><span data-stu-id="0d21e-111">This orientation of coordinates is often referred to as model space, and individual coordinates are called model coordinates.</span></span>

<span data-ttu-id="0d21e-112">La première étape du pipeline de géométrie transforme les vertex d’un modèle de leur système de coordonnées local en un système de coordonnées utilisé par tous les objets d’une scène.</span><span class="sxs-lookup"><span data-stu-id="0d21e-112">The first stage of the geometry pipeline transforms a model's vertices from their local coordinate system to a coordinate system that is used by all the objects in a scene.</span></span> <span data-ttu-id="0d21e-113">Le processus de réorientation des vertex est appelé la transformation universelle.</span><span class="sxs-lookup"><span data-stu-id="0d21e-113">The process of reorienting the vertices is called the world transform.</span></span> <span data-ttu-id="0d21e-114">Cette nouvelle orientation est communément appelée espace universel, et chaque vertex dans l’espace universel est déclaré à l’aide de coordonnées universelles.</span><span class="sxs-lookup"><span data-stu-id="0d21e-114">This new orientation is commonly referred to as world space, and each vertex in world space is declared using world coordinates.</span></span>

<span data-ttu-id="0d21e-115">À l’étape suivante, les vertex qui décrivent votre monde 3D sont orientés par rapport à une caméra.</span><span class="sxs-lookup"><span data-stu-id="0d21e-115">In the next stage, the vertices that describe your 3D world are oriented with respect to a camera.</span></span> <span data-ttu-id="0d21e-116">Autrement dit, votre application choisit un point de vue pour la scène, et les coordonnées de l’espace universel sont déplacées et pivotées autour de la vue de l’appareil photo, ce qui fait de l’espace universel dans l’espace de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="0d21e-116">That is, your application chooses a point-of-view for the scene, and world space coordinates are relocated and rotated around the camera's view, turning world space into camera space.</span></span> <span data-ttu-id="0d21e-117">Il s’agit de la transformation de la vue.</span><span class="sxs-lookup"><span data-stu-id="0d21e-117">This is the view transform.</span></span>

<span data-ttu-id="0d21e-118">L’étape suivante est la transformation de projection.</span><span class="sxs-lookup"><span data-stu-id="0d21e-118">The next stage is the projection transform.</span></span> <span data-ttu-id="0d21e-119">Dans cette partie du pipeline, les objets sont généralement mis à l’échelle en fonction de leur distance par rapport à la visionneuse afin de fournir l’illusion de profondeur à une scène. les objets proches sont rendus plus volumineux que les objets distants, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="0d21e-119">In this part of the pipeline, objects are usually scaled with relation to their distance from the viewer in order to give the illusion of depth to a scene; close objects are made to appear larger than distant objects, and so on.</span></span> <span data-ttu-id="0d21e-120">Par souci de simplicité, cette documentation fait référence à l’espace dans lequel les vertex existent après la transformation de projection en tant qu’espace de projection.</span><span class="sxs-lookup"><span data-stu-id="0d21e-120">For simplicity, this documentation refers to the space in which vertices exist after the projection transform as projection space.</span></span> <span data-ttu-id="0d21e-121">Certains livres graphiques peuvent faire référence à l’espace de projection comme un espace homogène après la perspective.</span><span class="sxs-lookup"><span data-stu-id="0d21e-121">Some graphics books might refer to projection space as post-perspective homogeneous space.</span></span> <span data-ttu-id="0d21e-122">Toutes les transformations de projection n’ajustent pas la taille des objets dans une scène.</span><span class="sxs-lookup"><span data-stu-id="0d21e-122">Not all projection transforms scale the size of objects in a scene.</span></span> <span data-ttu-id="0d21e-123">Une projection telle que celle-ci est parfois appelée projection affine ou orthogonale.</span><span class="sxs-lookup"><span data-stu-id="0d21e-123">A projection such as this is sometimes called an affine or orthogonal projection.</span></span>

<span data-ttu-id="0d21e-124">Dans la dernière partie du pipeline, tous les vertex qui ne seront pas visibles à l’écran sont supprimés, de sorte que le rastériseur ne prend pas le temps de calculer les couleurs et l’ombrage pour un élément qui ne sera jamais visible.</span><span class="sxs-lookup"><span data-stu-id="0d21e-124">In the final part of the pipeline, any vertices that will not be visible on the screen are removed, so that the rasterizer doesn't take the time to calculate the colors and shading for something that will never be seen.</span></span> <span data-ttu-id="0d21e-125">Ce processus est appelé découpage.</span><span class="sxs-lookup"><span data-stu-id="0d21e-125">This process is called clipping.</span></span> <span data-ttu-id="0d21e-126">Après le découpage, les sommets restants sont mis à l’échelle en fonction des paramètres de la fenêtre d’affichage et convertis en coordonnées d’écran.</span><span class="sxs-lookup"><span data-stu-id="0d21e-126">After clipping, the remaining vertices are scaled according to the viewport parameters and converted into screen coordinates.</span></span> <span data-ttu-id="0d21e-127">Les vertex résultants, visibles à l’écran lorsque la scène est pixellisée, existent dans l’espace à l’écran.</span><span class="sxs-lookup"><span data-stu-id="0d21e-127">The resulting vertices, seen on the screen when the scene is rasterized, exist in screen space.</span></span>

<span data-ttu-id="0d21e-128">Les transformations sont utilisées pour convertir la géométrie d’un objet d’un espace de coordonnées à un autre.</span><span class="sxs-lookup"><span data-stu-id="0d21e-128">Transforms are used to convert object geometry from one coordinate space to another.</span></span> <span data-ttu-id="0d21e-129">Direct3D utilise des matrices pour effectuer des transformations 3D.</span><span class="sxs-lookup"><span data-stu-id="0d21e-129">Direct3D uses matrices to perform 3D transforms.</span></span> <span data-ttu-id="0d21e-130">Cette section explique comment les matrices créent des transformations 3D, décrit certaines utilisations courantes des transformations et détaille la façon dont vous pouvez combiner des matrices pour produire une matrice unique qui englobe plusieurs transformations.</span><span class="sxs-lookup"><span data-stu-id="0d21e-130">This section explains how matrices create 3D transforms, describes some common uses for transforms, and details how you can combine matrices to produce a single matrix that encompasses multiple transforms.</span></span>

-   <span data-ttu-id="0d21e-131">[Transformation universelle (Direct3D 9)](world-transform.md) : conversion de l’espace de modèle en espace universel</span><span class="sxs-lookup"><span data-stu-id="0d21e-131">[World Transform (Direct3D 9)](world-transform.md) - convert from model space to world space</span></span>
-   <span data-ttu-id="0d21e-132">[Vue de la transformation (Direct3D 9)](view-transform.md) -conversion à partir de l’espace universel pour afficher l’espace</span><span class="sxs-lookup"><span data-stu-id="0d21e-132">[View Transform (Direct3D 9)](view-transform.md) - convert from world space to view space</span></span>
-   <span data-ttu-id="0d21e-133">[Transformation de projection (Direct3D 9)](projection-transform.md) -conversion de l’espace d’affichage à l’espace de projection</span><span class="sxs-lookup"><span data-stu-id="0d21e-133">[Projection Transform (Direct3D 9)](projection-transform.md) - convert from view space to projection space</span></span>

## <a name="matrix-transforms"></a><span data-ttu-id="0d21e-134">Transformations de matrice</span><span class="sxs-lookup"><span data-stu-id="0d21e-134">Matrix Transforms</span></span>

<span data-ttu-id="0d21e-135">Dans les applications qui fonctionnent avec des graphiques 3D, vous pouvez utiliser les transformations géométriques pour effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="0d21e-135">In applications that work with 3D graphics, you can use geometrical transforms to do the following:</span></span>

-   <span data-ttu-id="0d21e-136">Exprimer l’emplacement d’un objet par rapport à un autre objet.</span><span class="sxs-lookup"><span data-stu-id="0d21e-136">Express the location of an object relative to another object.</span></span>
-   <span data-ttu-id="0d21e-137">Faire pivoter et dimensionner les objets.</span><span class="sxs-lookup"><span data-stu-id="0d21e-137">Rotate and size objects.</span></span>
-   <span data-ttu-id="0d21e-138">Modifiez les positions, les directions et les perspectives d’affichage.</span><span class="sxs-lookup"><span data-stu-id="0d21e-138">Change viewing positions, directions, and perspectives.</span></span>

<span data-ttu-id="0d21e-139">Vous pouvez transformer n’importe quel point (x, y, z) en un autre point (x, y, z) à l’aide d’une matrice 4x4, comme illustré dans l’équation suivante.</span><span class="sxs-lookup"><span data-stu-id="0d21e-139">You can transform any point (x,y,z) into another point (x', y', z') by using a 4x4 matrix, as shown in the following equation.</span></span>

![équation de la transformation de tout point en un autre point](images/matmult.png)

<span data-ttu-id="0d21e-141">Effectuez les équations suivantes sur (x, y, z) et la matrice pour produire le point (x, y, z).</span><span class="sxs-lookup"><span data-stu-id="0d21e-141">Perform the following equations on (x, y, z) and the matrix to produce the point (x', y', z').</span></span>

![équations pour le nouveau point](images/matexpnd.png)

<span data-ttu-id="0d21e-143">Les transformations les plus courantes sont la traduction, la rotation et la mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="0d21e-143">The most common transforms are translation, rotation, and scaling.</span></span> <span data-ttu-id="0d21e-144">Vous pouvez combiner les matrices qui produisent ces effets dans une seule matrice pour calculer plusieurs transformations à la fois.</span><span class="sxs-lookup"><span data-stu-id="0d21e-144">You can combine the matrices that produce these effects into a single matrix to calculate several transforms at once.</span></span> <span data-ttu-id="0d21e-145">Par exemple, vous pouvez créer une matrice unique pour traduire et faire pivoter une série de points.</span><span class="sxs-lookup"><span data-stu-id="0d21e-145">For example, you can build a single matrix to translate and rotate a series of points.</span></span>

<span data-ttu-id="0d21e-146">Les matrices sont écrites dans l’ordre des colonnes de lignes.</span><span class="sxs-lookup"><span data-stu-id="0d21e-146">Matrices are written in row-column order.</span></span> <span data-ttu-id="0d21e-147">Une matrice qui ajuste uniformément les sommets le long de chaque axe, appelée mise à l’échelle uniforme, est représentée par la matrice suivante à l’aide de la notation mathématique.</span><span class="sxs-lookup"><span data-stu-id="0d21e-147">A matrix that evenly scales vertices along each axis, known as uniform scaling, is represented by the following matrix using mathematical notation.</span></span>

![équation d’une matrice pour la mise à l’échelle uniforme](images/matrix.png)

<span data-ttu-id="0d21e-149">En C++, Direct3D déclare des matrices sous la forme d’un tableau à deux dimensions, à l’aide de la structure [**D3DMATRIX**](d3dmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="0d21e-149">In C++, Direct3D declares matrices as a two-dimensional array, using the [**D3DMATRIX**](d3dmatrix.md) structure.</span></span> <span data-ttu-id="0d21e-150">L’exemple suivant montre comment initialiser une structure **D3DMATRIX** pour qu’elle agisse comme une matrice de mise à l’échelle uniforme.</span><span class="sxs-lookup"><span data-stu-id="0d21e-150">The following example shows how to initialize a **D3DMATRIX** structure to act as a uniform scaling matrix.</span></span>


```
// In this example, s is a variable of type float.

D3DMATRIX scale = {
    s,               0.0f,            0.0f,            0.0f,
    0.0f,            s,               0.0f,            0.0f,
    0.0f,            0.0f,            s,               0.0f,
    0.0f,            0.0f,            0.0f,            1.0f
};
```



## <a name="translate"></a><span data-ttu-id="0d21e-151">Translate</span><span class="sxs-lookup"><span data-stu-id="0d21e-151">Translate</span></span>

<span data-ttu-id="0d21e-152">L’équation suivante traduit le point (x, y, z) en un nouveau point (x, y, z).</span><span class="sxs-lookup"><span data-stu-id="0d21e-152">The following equation translates the point (x, y, z) to a new point (x', y', z').</span></span>

![équation d’une matrice de translation pour un nouveau point](images/transl8.png)

<span data-ttu-id="0d21e-154">Vous pouvez créer manuellement une matrice de traduction en C++.</span><span class="sxs-lookup"><span data-stu-id="0d21e-154">You can manually create a translation matrix in C++.</span></span> <span data-ttu-id="0d21e-155">L’exemple suivant montre le code source d’une fonction qui crée une matrice pour traduire des vertex.</span><span class="sxs-lookup"><span data-stu-id="0d21e-155">The following example shows the source code for a function that creates a matrix to translate vertices.</span></span>


```
D3DXMATRIX Translate(const float dx, const float dy, const float dz) {
    D3DXMATRIX ret;

    D3DXMatrixIdentity(&ret);
    ret(3, 0) = dx;
    ret(3, 1) = dy;
    ret(3, 2) = dz;
    return ret;
}    // End of Translate
```



<span data-ttu-id="0d21e-156">Pour plus de commodité, la bibliothèque de l’utilitaire D3DX fournit la fonction [**D3DXMatrixTranslation**](d3dxmatrixtranslation.md) .</span><span class="sxs-lookup"><span data-stu-id="0d21e-156">For convenience, the D3DX utility library supplies the [**D3DXMatrixTranslation**](d3dxmatrixtranslation.md) function.</span></span>

## <a name="scale"></a><span data-ttu-id="0d21e-157">Scale</span><span class="sxs-lookup"><span data-stu-id="0d21e-157">Scale</span></span>

<span data-ttu-id="0d21e-158">L’équation suivante met à l’échelle le point (x, y, z) en valeurs arbitraires dans les directions x, y et z vers un nouveau point (x, y, z).</span><span class="sxs-lookup"><span data-stu-id="0d21e-158">The following equation scales the point (x, y, z) by arbitrary values in the x-, y-, and z-directions to a new point (x', y', z').</span></span>

![équation d’une matrice de mise à l’échelle pour un nouveau point](images/matscale.png)

## <a name="rotate"></a><span data-ttu-id="0d21e-160">Faire pivoter</span><span class="sxs-lookup"><span data-stu-id="0d21e-160">Rotate</span></span>

<span data-ttu-id="0d21e-161">Les transformations décrites ici sont destinées aux systèmes de coordonnées de gauche et peuvent être différentes des matrices de transformation que vous avez vues ailleurs.</span><span class="sxs-lookup"><span data-stu-id="0d21e-161">The transforms described here are for left-handed coordinate systems, and so may be different from transform matrices that you have seen elsewhere.</span></span>

<span data-ttu-id="0d21e-162">L’équation suivante fait pivoter le point (x, y, z) autour de l’axe x, produisant un nouveau point (x, y, z).</span><span class="sxs-lookup"><span data-stu-id="0d21e-162">The following equation rotates the point (x, y, z) around the x-axis, producing a new point (x', y', z').</span></span>

![équation d’une matrice de rotation x pour un nouveau point](images/matxrot.png)

<span data-ttu-id="0d21e-164">L’équation suivante fait pivoter le point autour de l’axe y.</span><span class="sxs-lookup"><span data-stu-id="0d21e-164">The following equation rotates the point around the y-axis.</span></span>

![équation d’une matrice de rotation y pour un nouveau point](images/matyrot.png)

<span data-ttu-id="0d21e-166">L’équation suivante fait pivoter le point autour de l’axe z.</span><span class="sxs-lookup"><span data-stu-id="0d21e-166">The following equation rotates the point around the z-axis.</span></span>

![équation d’une matrice de rotation z pour un nouveau point](images/matzrot.png)

<span data-ttu-id="0d21e-168">Dans ces exemples de matrices, la lettre grecque thêta représente l’angle de rotation, en radians.</span><span class="sxs-lookup"><span data-stu-id="0d21e-168">In these example matrices, the Greek letter theta stands for the angle of rotation, in radians.</span></span> <span data-ttu-id="0d21e-169">Les angles sont mesurés dans le sens des aiguilles d’une montre sur l’axe de rotation vers l’origine.</span><span class="sxs-lookup"><span data-stu-id="0d21e-169">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

<span data-ttu-id="0d21e-170">Dans une application C++, utilisez les fonctions [**D3DXMatrixRotationX**](d3dxmatrixrotationx.md), [**D3DXMatrixRotationY**](d3dxmatrixrotationy.md)et [**D3DXMatrixRotationZ**](d3dxmatrixrotationz.md) fournies par la bibliothèque de l’utilitaire D3DX pour créer des matrices de rotation.</span><span class="sxs-lookup"><span data-stu-id="0d21e-170">In a C++ application, use the [**D3DXMatrixRotationX**](d3dxmatrixrotationx.md), [**D3DXMatrixRotationY**](d3dxmatrixrotationy.md), and [**D3DXMatrixRotationZ**](d3dxmatrixrotationz.md) functions supplied by the D3DX utility library to create rotation matrices.</span></span> <span data-ttu-id="0d21e-171">Voici le code de la fonction **D3DXMatrixRotationX** .</span><span class="sxs-lookup"><span data-stu-id="0d21e-171">The following is the code for the **D3DXMatrixRotationX** function.</span></span>


```
D3DXMATRIX* WINAPI D3DXMatrixRotationX
    ( D3DXMATRIX *pOut, float angle )
{
#if DBG
    if(!pOut)
        return NULL;
#endif

    float sin, cos;
    sincosf(angle, &sin, &cos);  // Determine sin and cos of angle

    pOut->_11 = 1.0f; pOut->_12 =  0.0f;   pOut->_13 = 0.0f; pOut->_14 = 0.0f;
    pOut->_21 = 0.0f; pOut->_22 =  cos;    pOut->_23 = sin;  pOut->_24 = 0.0f;
    pOut->_31 = 0.0f; pOut->_32 = -sin;    pOut->_33 = cos;  pOut->_34 = 0.0f;
    pOut->_41 = 0.0f; pOut->_42 =  0.0f;   pOut->_43 = 0.0f; pOut->_44 = 1.0f;

    return pOut;
}
```



## <a name="concatenating-matrices"></a><span data-ttu-id="0d21e-172">Concaténation de matrices</span><span class="sxs-lookup"><span data-stu-id="0d21e-172">Concatenating Matrices</span></span>

<span data-ttu-id="0d21e-173">L’un des avantages de l’utilisation des matrices est que vous pouvez combiner les effets de deux matrices ou plus en les multipliant.</span><span class="sxs-lookup"><span data-stu-id="0d21e-173">One advantage of using matrices is that you can combine the effects of two or more matrices by multiplying them.</span></span> <span data-ttu-id="0d21e-174">Cela signifie que, pour faire pivoter un modèle, puis le traduire à un emplacement donné, vous n’avez pas besoin d’appliquer deux matrices.</span><span class="sxs-lookup"><span data-stu-id="0d21e-174">This means that, to rotate a model and then translate it to some location, you don't need to apply two matrices.</span></span> <span data-ttu-id="0d21e-175">Au lieu de cela, vous multipliez les matrices de rotation et de translation pour produire une matrice composite qui contient tous les effets.</span><span class="sxs-lookup"><span data-stu-id="0d21e-175">Instead, you multiply the rotation and translation matrices to produce a composite matrix that contains all their effects.</span></span> <span data-ttu-id="0d21e-176">Ce processus, appelé concaténation de matrice, peut être écrit avec l’équation suivante.</span><span class="sxs-lookup"><span data-stu-id="0d21e-176">This process, called matrix concatenation, can be written with the following equation.</span></span>

![équation de la concaténation de matrice](images/matrxcat.png)

<span data-ttu-id="0d21e-178">Dans cette équation, C est la matrice composite en cours de création et M ₁ à mn sont les matrices individuelles.</span><span class="sxs-lookup"><span data-stu-id="0d21e-178">In this equation, C is the composite matrix being created, and M₁ through Mₙ are the individual matrices.</span></span> <span data-ttu-id="0d21e-179">Dans la plupart des cas, seules deux ou trois matrices sont concaténées, mais il n’existe aucune limite.</span><span class="sxs-lookup"><span data-stu-id="0d21e-179">In most cases, only two or three matrices are concatenated, but there is no limit.</span></span>

<span data-ttu-id="0d21e-180">Utilisez la fonction [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) pour effectuer une multiplication de matrice.</span><span class="sxs-lookup"><span data-stu-id="0d21e-180">Use the [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) function to perform matrix multiplication.</span></span>

<span data-ttu-id="0d21e-181">L’ordre dans lequel la multiplication de la matrice est effectuée est essentiel.</span><span class="sxs-lookup"><span data-stu-id="0d21e-181">The order in which the matrix multiplication is performed is crucial.</span></span> <span data-ttu-id="0d21e-182">La formule précédente reflète la règle de la concaténation de matrice de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="0d21e-182">The preceding formula reflects the left-to-right rule of matrix concatenation.</span></span> <span data-ttu-id="0d21e-183">Autrement dit, les effets visibles des matrices que vous utilisez pour créer une matrice composite se produisent dans l’ordre de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="0d21e-183">That is, the visible effects of the matrices that you use to create a composite matrix occur in left-to-right order.</span></span> <span data-ttu-id="0d21e-184">L’exemple suivant illustre une matrice universelle classique.</span><span class="sxs-lookup"><span data-stu-id="0d21e-184">A typical world matrix is shown in the following example.</span></span> <span data-ttu-id="0d21e-185">Imaginez que vous créez la matrice universelle pour un soubattante volante de stéréotype.</span><span class="sxs-lookup"><span data-stu-id="0d21e-185">Imagine that you are creating the world matrix for a stereotypical flying saucer.</span></span> <span data-ttu-id="0d21e-186">Vous souhaiterez probablement faire tourner le volant volant autour de son centre-l’axe y de l’espace de modèle, et le traduire à un autre emplacement de votre scène.</span><span class="sxs-lookup"><span data-stu-id="0d21e-186">You would probably want to spin the flying saucer around its center - the y-axis of model space - and translate it to some other location in your scene.</span></span> <span data-ttu-id="0d21e-187">Pour obtenir cet effet, vous créez d’abord une matrice de rotation, puis vous la multipliez par une matrice de traduction, comme illustré dans l’équation suivante.</span><span class="sxs-lookup"><span data-stu-id="0d21e-187">To accomplish this effect, you first create a rotation matrix, and then multiply it by a translation matrix, as shown in the following equation.</span></span>

![équation de spin basée sur une matrice de rotation et une matrice de traduction](images/wrldexpl.png)

<span data-ttu-id="0d21e-189">Dans cette formule, R<sub>y</sub> est une matrice de rotation autour de l’axe des y et T<sub>w</sub> est une translation à une position en coordonnées universelles.</span><span class="sxs-lookup"><span data-stu-id="0d21e-189">In this formula, R<sub>y</sub> is a matrix for rotation about the y-axis, and T<sub>w</sub> is a translation to some position in world coordinates.</span></span>

<span data-ttu-id="0d21e-190">L’ordre dans lequel vous multipliez les matrices est important car, contrairement à la multiplication de deux valeurs scalaires, la multiplication de matrices n’est pas commutative.</span><span class="sxs-lookup"><span data-stu-id="0d21e-190">The order in which you multiply the matrices is important because, unlike multiplying two scalar values, matrix multiplication is not commutative.</span></span> <span data-ttu-id="0d21e-191">La multiplication des matrices dans l’ordre opposé a pour effet visuel de traduire le volant volant en position d’espace universel, puis de le faire pivoter autour de l’origine du monde.</span><span class="sxs-lookup"><span data-stu-id="0d21e-191">Multiplying the matrices in the opposite order has the visual effect of translating the flying saucer to its world space position, and then rotating it around the world origin.</span></span>

<span data-ttu-id="0d21e-192">Quel que soit le type de matrice que vous créez, n’oubliez pas la règle de gauche à droite pour vous assurer que vous atteignez les effets attendus.</span><span class="sxs-lookup"><span data-stu-id="0d21e-192">No matter what type of matrix you are creating, remember the left-to-right rule to ensure that you achieve the expected effects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d21e-193">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0d21e-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d21e-194">Prise en main</span><span class="sxs-lookup"><span data-stu-id="0d21e-194">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 



