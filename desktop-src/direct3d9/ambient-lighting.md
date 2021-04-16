---
description: L’éclairage ambiant offre une lumière constante pour une scène.
ms.assetid: 327095a7-f4e0-48c2-9e4d-bec8493fe37e
title: Éclairage ambiant (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e991981a9c1d7d24714e7014d08cefeaa94fe20f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523839"
---
# <a name="ambient-lighting-direct3d-9"></a><span data-ttu-id="7c93b-103">Éclairage ambiant (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7c93b-103">Ambient Lighting (Direct3D 9)</span></span>

<span data-ttu-id="7c93b-104">L’éclairage ambiant offre une lumière constante pour une scène.</span><span class="sxs-lookup"><span data-stu-id="7c93b-104">Ambient lighting provides constant lighting for a scene.</span></span> <span data-ttu-id="7c93b-105">Il prend en compte tous les sommets d’objets, car il ne dépend pas d’autres facteurs d’éclairage tels que les normales aux sommets, la direction de la lumière, la position de la lumière, la plage ou l’atténuation.</span><span class="sxs-lookup"><span data-stu-id="7c93b-105">It lights all object vertices the same because it is not dependent on any other lighting factors such as vertex normals, light direction, light position, range, or attenuation.</span></span> <span data-ttu-id="7c93b-106">Il s’agit du type d’éclairage le plus rapide, mais il produit des résultats moins réalistes.</span><span class="sxs-lookup"><span data-stu-id="7c93b-106">It is the fastest type of lighting but it produces the least realistic results.</span></span> <span data-ttu-id="7c93b-107">Direct3D contient une seule propriété de lumière ambiante globale que vous pouvez utiliser sans créer de lumière.</span><span class="sxs-lookup"><span data-stu-id="7c93b-107">Direct3D contains a single global ambient light property that you can use without creating any light.</span></span> <span data-ttu-id="7c93b-108">Vous pouvez également définir n’importe quel objet Light pour fournir un éclairage ambiant.</span><span class="sxs-lookup"><span data-stu-id="7c93b-108">Alternatively, you can set any light object to provide ambient lighting.</span></span> <span data-ttu-id="7c93b-109">L’éclairage ambiant d’une scène est décrit par l’équation suivante.</span><span class="sxs-lookup"><span data-stu-id="7c93b-109">The ambient lighting for a scene is described by the following equation.</span></span>

<span data-ttu-id="7c93b-110">Éclairage ambiant = C ₐ \* \[ g ₐ + Sum (atten<sub>i</sub> \* point<sub>i</sub> \* L<sub>ai</sub>)\]</span><span class="sxs-lookup"><span data-stu-id="7c93b-110">Ambient Lighting = Cₐ\*\[Gₐ + sum(Atten<sub>i</sub>\*Spot<sub>i</sub>\*L<sub>ai</sub>)\]</span></span>

<span data-ttu-id="7c93b-111">Où :</span><span class="sxs-lookup"><span data-stu-id="7c93b-111">Where:</span></span>



| <span data-ttu-id="7c93b-112">Paramètre</span><span class="sxs-lookup"><span data-stu-id="7c93b-112">Parameter</span></span>         | <span data-ttu-id="7c93b-113">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="7c93b-113">Default value</span></span> | <span data-ttu-id="7c93b-114">Type</span><span class="sxs-lookup"><span data-stu-id="7c93b-114">Type</span></span>          | <span data-ttu-id="7c93b-115">Description</span><span class="sxs-lookup"><span data-stu-id="7c93b-115">Description</span></span>                                                                                                                    |
|-------------------|---------------|---------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c93b-116">C ₐ</span><span class="sxs-lookup"><span data-stu-id="7c93b-116">Cₐ</span></span>                | <span data-ttu-id="7c93b-117">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="7c93b-117">(0,0,0,0)</span></span>     | <span data-ttu-id="7c93b-118">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="7c93b-118">D3DCOLORVALUE</span></span> | <span data-ttu-id="7c93b-119">Couleur ambiante du matériau</span><span class="sxs-lookup"><span data-stu-id="7c93b-119">Material ambient color</span></span>                                                                                                         |
| <span data-ttu-id="7c93b-120">ₐ g</span><span class="sxs-lookup"><span data-stu-id="7c93b-120">Gₐ</span></span>                | <span data-ttu-id="7c93b-121">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="7c93b-121">(0,0,0,0)</span></span>     | <span data-ttu-id="7c93b-122">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="7c93b-122">D3DCOLORVALUE</span></span> | <span data-ttu-id="7c93b-123">Couleur ambiante globale</span><span class="sxs-lookup"><span data-stu-id="7c93b-123">Global ambient color</span></span>                                                                                                           |
| <span data-ttu-id="7c93b-124">Atten<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="7c93b-124">Atten<sub>i</sub></span></span> | <span data-ttu-id="7c93b-125">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="7c93b-125">(0,0,0,0)</span></span>     | <span data-ttu-id="7c93b-126">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="7c93b-126">D3DCOLORVALUE</span></span> | <span data-ttu-id="7c93b-127">Atténuation de la lumière de la énièmeté.</span><span class="sxs-lookup"><span data-stu-id="7c93b-127">Light attenuation of the ith light.</span></span> <span data-ttu-id="7c93b-128">Consultez [facteur d’atténuation et de focalisation (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="7c93b-128">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span> |
| <span data-ttu-id="7c93b-129">Point<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="7c93b-129">Spot<sub>i</sub></span></span>  | <span data-ttu-id="7c93b-130">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="7c93b-130">(0,0,0,0)</span></span>     | <span data-ttu-id="7c93b-131">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="7c93b-131">D3DVECTOR</span></span>     | <span data-ttu-id="7c93b-132">Facteur Gong de la énième lumière.</span><span class="sxs-lookup"><span data-stu-id="7c93b-132">Spotlight factor of the ith light.</span></span> <span data-ttu-id="7c93b-133">Consultez [facteur d’atténuation et de focalisation (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="7c93b-133">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span>  |
| <span data-ttu-id="7c93b-134">Sum</span><span class="sxs-lookup"><span data-stu-id="7c93b-134">sum</span></span>               | <span data-ttu-id="7c93b-135">N/A</span><span class="sxs-lookup"><span data-stu-id="7c93b-135">N/A</span></span>           | <span data-ttu-id="7c93b-136">N/A</span><span class="sxs-lookup"><span data-stu-id="7c93b-136">N/A</span></span>           | <span data-ttu-id="7c93b-137">Somme de la lumière ambiante</span><span class="sxs-lookup"><span data-stu-id="7c93b-137">Sum of the ambient light</span></span>                                                                                                       |
| <span data-ttu-id="7c93b-138">L<sub>ai</sub></span><span class="sxs-lookup"><span data-stu-id="7c93b-138">L<sub>ai</sub></span></span>    | <span data-ttu-id="7c93b-139">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="7c93b-139">(0,0,0,0)</span></span>     | <span data-ttu-id="7c93b-140">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="7c93b-140">D3DVECTOR</span></span>     | <span data-ttu-id="7c93b-141">Couleur ambiante claire de la énième lumière</span><span class="sxs-lookup"><span data-stu-id="7c93b-141">Light ambient color of the ith light</span></span>                                                                                           |



 

<span data-ttu-id="7c93b-142">La valeur de C ₐ est :</span><span class="sxs-lookup"><span data-stu-id="7c93b-142">The value for Cₐ is either:</span></span>

-   <span data-ttu-id="7c93b-143">Sommet color1, si AMBIENTMATERIALSOURCE = D3DMCS \_ color1, et la première couleur de vertex est fournie dans la déclaration de vertex.</span><span class="sxs-lookup"><span data-stu-id="7c93b-143">vertex color1, if AMBIENTMATERIALSOURCE = D3DMCS\_COLOR1, and the first vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="7c93b-144">le sommet color2, si AMBIENTMATERIALSOURCE = D3DMCS \_ color2, et la deuxième couleur du vertex sont fournies dans une déclaration de vertex.</span><span class="sxs-lookup"><span data-stu-id="7c93b-144">vertex color2, if AMBIENTMATERIALSOURCE = D3DMCS\_COLOR2, and the second vertex color is supplied in vertex declaration.</span></span>
-   <span data-ttu-id="7c93b-145">couleur ambiante du matériau.</span><span class="sxs-lookup"><span data-stu-id="7c93b-145">material ambient color.</span></span>

> [!Note]  
> <span data-ttu-id="7c93b-146">Si l’une des options AMBIENTMATERIALSOURCE est utilisée et que la couleur du vertex n’est pas fournie, la couleur ambiante du matériau est utilisée.</span><span class="sxs-lookup"><span data-stu-id="7c93b-146">If either AMBIENTMATERIALSOURCE option is used, and the vertex color is not provided, then the material ambient color is used.</span></span>

 

<span data-ttu-id="7c93b-147">Pour utiliser la couleur ambiante du matériau, utilisez SetMaterial comme indiqué dans l’exemple de code ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="7c93b-147">To use the material ambient color, use SetMaterial as shown in the example code below.</span></span>

<span data-ttu-id="7c93b-148">G ₐ est la couleur ambiante globale.</span><span class="sxs-lookup"><span data-stu-id="7c93b-148">Gₐ is the global ambient color.</span></span> <span data-ttu-id="7c93b-149">Il est défini à l’aide de SetRenderState (D3DRS \_ ambiant).</span><span class="sxs-lookup"><span data-stu-id="7c93b-149">It is set using SetRenderState(D3DRS\_AMBIENT).</span></span> <span data-ttu-id="7c93b-150">Une scène Direct3D contient une couleur ambiante globale.</span><span class="sxs-lookup"><span data-stu-id="7c93b-150">There is one global ambient color in a Direct3D scene.</span></span> <span data-ttu-id="7c93b-151">Ce paramètre n’est pas associé à un objet Light Direct3D.</span><span class="sxs-lookup"><span data-stu-id="7c93b-151">This parameter is not associated with a Direct3D light object.</span></span>

<span data-ttu-id="7c93b-152">L<sub>ai</sub> est la couleur ambiante de l’énième lumière dans la scène.</span><span class="sxs-lookup"><span data-stu-id="7c93b-152">L<sub>ai</sub> is the ambient color of the ith light in the scene.</span></span> <span data-ttu-id="7c93b-153">Chaque lumière Direct3D a un ensemble de propriétés, dont l’une est la couleur ambiante.</span><span class="sxs-lookup"><span data-stu-id="7c93b-153">Each Direct3D light has a set of properties, one of which is the ambient color.</span></span> <span data-ttu-id="7c93b-154">Le terme somme (L<sub>ai</sub>) est la somme de toutes les couleurs ambiantes de la scène.</span><span class="sxs-lookup"><span data-stu-id="7c93b-154">The term, sum(L<sub>ai</sub>) is a sum of all the ambient colors in the scene.</span></span>

## <a name="example"></a><span data-ttu-id="7c93b-155">Exemple</span><span class="sxs-lookup"><span data-stu-id="7c93b-155">Example</span></span>

<span data-ttu-id="7c93b-156">Dans cet exemple, l’objet est coloré à l’aide de la lumière ambiante de scène et d’une couleur ambiante de matériau.</span><span class="sxs-lookup"><span data-stu-id="7c93b-156">In this example, the object is colored using the scene ambient light and a material ambient color.</span></span>


```
#define GRAY_COLOR  0x00bfbfbf

// create material
D3DMATERIAL9 mtrl;
ZeroMemory(&mtrl, sizeof(mtrl));
mtrl.Ambient.r = 0.75f;
mtrl.Ambient.g = 0.0f;
mtrl.Ambient.b = 0.0f;
mtrl.Ambient.a = 0.0f;
m_pd3dDevice->SetMaterial(&mtrl);
m_pd3dDevice->SetRenderState(D3DRS_AMBIENT, GRAY_COLOR);
```



<span data-ttu-id="7c93b-157">D’après l’équation, la couleur résultante pour les vertex d’objet est une combinaison de la couleur de l’élément et de la couleur claire.</span><span class="sxs-lookup"><span data-stu-id="7c93b-157">According to the equation, the resulting color for the object vertices is a combination of the material color and the light color.</span></span>

<span data-ttu-id="7c93b-158">Les deux illustrations suivantes affichent la couleur de matériau, grise, et la couleur claire, qui est brillante rouge.</span><span class="sxs-lookup"><span data-stu-id="7c93b-158">The following two illustrations show the material color, which is gray, and the light color, which is bright red.</span></span>

![illustration d’une sphère grise](images/amb1.jpg)![illustration d’une sphère rouge](images/lightred.jpg)

<span data-ttu-id="7c93b-161">La scène qui en résulte est présentée dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="7c93b-161">The resulting scene is shown in the following illustration.</span></span> <span data-ttu-id="7c93b-162">Le seul objet de la scène est une sphère.</span><span class="sxs-lookup"><span data-stu-id="7c93b-162">The only object in the scene is a sphere.</span></span> <span data-ttu-id="7c93b-163">La lumière ambiante illumine tous les vertex d’objets avec la même couleur.</span><span class="sxs-lookup"><span data-stu-id="7c93b-163">Ambient light lights all object vertices with the same color.</span></span> <span data-ttu-id="7c93b-164">Elle n’est pas dépendante de la normale du vertex ou de la direction de la lumière.</span><span class="sxs-lookup"><span data-stu-id="7c93b-164">It is not dependent on the vertex normal or the light direction.</span></span> <span data-ttu-id="7c93b-165">Par conséquent, la sphère ressemble à un cercle 2D, car il n’y a aucune différence dans l’ombrage autour de la surface de l’objet.</span><span class="sxs-lookup"><span data-stu-id="7c93b-165">As a result, the sphere looks like a 2D circle because there is no difference in shading around the surface of the object.</span></span>

![illustration d’une sphère avec éclairage ambiant](images/lighta.jpg)

<span data-ttu-id="7c93b-167">Pour donner une apparence plus réaliste aux objets, appliquez une lumière diffuse ou spéculaire en plus de l’éclairage ambiant.</span><span class="sxs-lookup"><span data-stu-id="7c93b-167">To give objects a more realistic look, apply diffuse or specular lighting in addition to ambient lighting.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c93b-168">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7c93b-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c93b-169">Mathématiques d’éclairage</span><span class="sxs-lookup"><span data-stu-id="7c93b-169">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



