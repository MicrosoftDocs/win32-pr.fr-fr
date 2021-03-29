---
title: Texture, objet
description: Dans Direct3D 10, vous spécifiez les échantillonneurs et les textures indépendamment. l’échantillonnage de texture est implémenté à l’aide d’un objet de texture basée sur un modèle. Cet objet de texture basé sur un modèle a un format spécifique, retourne un type spécifique et implémente plusieurs méthodes.
ms.assetid: e8cb483a-d831-4942-b6fe-61dd5edb1813
keywords:
- Objet texture HLSL
topic_type:
- apiref
api_name:
- Texture Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b075ddc1f659923efd03d9fe9d21ee3238e656e9
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2021
ms.locfileid: "104211659"
---
# <a name="texture-object"></a><span data-ttu-id="b72f0-105">Texture, objet</span><span class="sxs-lookup"><span data-stu-id="b72f0-105">Texture Object</span></span>

<span data-ttu-id="b72f0-106">Dans Direct3D 10, vous spécifiez les échantillonneurs et les textures indépendamment. l’échantillonnage de texture est implémenté à l’aide d’un objet de texture basée sur un modèle.</span><span class="sxs-lookup"><span data-stu-id="b72f0-106">In Direct3D 10, you specify the samplers and textures independently; texture sampling is implemented by using a templated-texture object.</span></span> <span data-ttu-id="b72f0-107">Cet objet de texture basé sur un modèle a un format spécifique, retourne un type spécifique et implémente plusieurs méthodes.</span><span class="sxs-lookup"><span data-stu-id="b72f0-107">This templated-texture object has a specific format, returns a specific type, and implements several methods.</span></span>




|                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b72f0-108">Différences entre Direct3D9 et Direct3D10 : dans Direct3D 9, les échantillonneurs sont liés à des textures spécifiques ; dans Direct3D 10, les textures et les échantillonneurs sont des objets indépendants.</span><span class="sxs-lookup"><span data-stu-id="b72f0-108">Differences between Direct3D9 and Direct3D10: In Direct3D 9, samplers are bound to specific textures; in Direct3D 10, textures and samplers are independent objects.</span></span> <span data-ttu-id="b72f0-109">Chaque objet de texture basée sur un modèle implémente des méthodes d’échantillonnage de texture qui prennent à la fois la texture et l’échantillonneur comme paramètres d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b72f0-109">Each templated-texture object implements texture sampling methods that take both the texture and the sampler as input parameters.</span></span><br/> |



 

<span data-ttu-id="b72f0-110">Voici la syntaxe permettant de créer tous les objets texture (à l’exception des objets à échantillonnages).</span><span class="sxs-lookup"><span data-stu-id="b72f0-110">Here is the syntax for creating all texture objects (except multisampled objects).</span></span>



| <span data-ttu-id="b72f0-111">Nom du \[ < *type* > \] de la</span><span class="sxs-lookup"><span data-stu-id="b72f0-111">Object1 \[<*Type*>\] *Name*;</span></span> |
|------------------------------------|



 

<span data-ttu-id="b72f0-112">Les objets multiéchantillonnés (Texture2DMS et Texture2DMSArray) requièrent que la taille de la texture soit explicitement indiquée et exprimée sous la forme du nombre d’échantillons.</span><span class="sxs-lookup"><span data-stu-id="b72f0-112">Multisampled objects (Texture2DMS and Texture2DMSArray) require the texture size to be explicitly stated and expressed as the number of samples.</span></span>



| <span data-ttu-id="b72f0-113">Object2 \[ < *type, Samples* > \] *Name*;</span><span class="sxs-lookup"><span data-stu-id="b72f0-113">Object2 \[<*Type, Samples*>\] *Name*;</span></span> |
|---------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="b72f0-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b72f0-114">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b72f0-115">Élément</span><span class="sxs-lookup"><span data-stu-id="b72f0-115">Item</span></span></th>
<th><span data-ttu-id="b72f0-116">Description</span><span class="sxs-lookup"><span data-stu-id="b72f0-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b72f0-117"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Dessin</em></span><span class="sxs-lookup"><span data-stu-id="b72f0-117"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="b72f0-118">Objet texture.</span><span class="sxs-lookup"><span data-stu-id="b72f0-118">A texture object.</span></span> <span data-ttu-id="b72f0-119">Il doit s’agir de l’un des types suivants.</span><span class="sxs-lookup"><span data-stu-id="b72f0-119">Must be one of the following types.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b72f0-120">Type de la</span><span class="sxs-lookup"><span data-stu-id="b72f0-120">Object1 Type</span></span></th>
<th><span data-ttu-id="b72f0-121">Description</span><span class="sxs-lookup"><span data-stu-id="b72f0-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b72f0-122">Buffer</span><span class="sxs-lookup"><span data-stu-id="b72f0-122">Buffer</span></span></td>
<td><span data-ttu-id="b72f0-123">Buffer</span><span class="sxs-lookup"><span data-stu-id="b72f0-123">Buffer</span></span> </td>
</tr>
<tr class="even">
<td><span data-ttu-id="b72f0-124">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b72f0-124">Texture1D</span></span></td>
<td><span data-ttu-id="b72f0-125">texture 1D</span><span class="sxs-lookup"><span data-stu-id="b72f0-125">1D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b72f0-126">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="b72f0-126">Texture1DArray</span></span></td>
<td><span data-ttu-id="b72f0-127">Tableau de textures 1D</span><span class="sxs-lookup"><span data-stu-id="b72f0-127">Array of 1D textures</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b72f0-128">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b72f0-128">Texture2D</span></span></td>
<td><span data-ttu-id="b72f0-129">texture 2D</span><span class="sxs-lookup"><span data-stu-id="b72f0-129">2D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b72f0-130">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="b72f0-130">Texture2DArray</span></span></td>
<td><span data-ttu-id="b72f0-131">Tableau de textures 2D</span><span class="sxs-lookup"><span data-stu-id="b72f0-131">Array of 2D textures</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b72f0-132">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b72f0-132">Texture3D</span></span></td>
<td><span data-ttu-id="b72f0-133">texture 3D</span><span class="sxs-lookup"><span data-stu-id="b72f0-133">3D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b72f0-134">TextureCube</span><span class="sxs-lookup"><span data-stu-id="b72f0-134">TextureCube</span></span></td>
<td><span data-ttu-id="b72f0-135">Texture de cube</span><span class="sxs-lookup"><span data-stu-id="b72f0-135">Cube texture</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b72f0-136">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="b72f0-136">TextureCubeArray</span></span>  </td>
<td><span data-ttu-id="b72f0-137">Tableau de textures de cube</span><span class="sxs-lookup"><span data-stu-id="b72f0-137">Array of cube textures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b72f0-138">Type object2</span><span class="sxs-lookup"><span data-stu-id="b72f0-138">Object2 Type</span></span></td>
<td><span data-ttu-id="b72f0-139">Description</span><span class="sxs-lookup"><span data-stu-id="b72f0-139">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b72f0-140">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="b72f0-140">Texture2DMS</span></span></td>
<td><span data-ttu-id="b72f0-141">texture multiéchantillonnée 2D</span><span class="sxs-lookup"><span data-stu-id="b72f0-141">2D multisampled texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b72f0-142">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="b72f0-142">Texture2DMSArray</span></span></td>
<td><span data-ttu-id="b72f0-143">Tableau de textures multiéchantillonnées 2D</span><span class="sxs-lookup"><span data-stu-id="b72f0-143">Array of 2D multisampled textures</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<ol>
<li><span data-ttu-id="b72f0-144">Le type de mémoire tampon prend en charge la plupart des méthodes d’objets texture, à l’exception de GetDimensions,.</span><span class="sxs-lookup"><span data-stu-id="b72f0-144">The Buffer type supports most texture object methods except GetDimensions.</span></span></li>
<li><span data-ttu-id="b72f0-145">TextureCubeArray est disponible dans le nuancier modèle 4,1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="b72f0-145">TextureCubeArray is available in shader model 4.1 or higher.</span></span></li>
<li><span data-ttu-id="b72f0-146">Le modèle de nuanceur 4,1 est disponible dans Direct3D 10,1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="b72f0-146">Shader model 4.1 is available in Direct3D 10.1 or higher.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b72f0-147"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Entrer</em></span><span class="sxs-lookup"><span data-stu-id="b72f0-147"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="b72f0-148">facultatif.</span><span class="sxs-lookup"><span data-stu-id="b72f0-148">Optional.</span></span> <span data-ttu-id="b72f0-149">Tout type HLSL <a href="dx-graphics-hlsl-scalar.md">scalaire</a> ou type <a href="dx-graphics-hlsl-vector.md"><strong>HLSL vectoriel</strong></a>, entouré par des crochets pointus.</span><span class="sxs-lookup"><span data-stu-id="b72f0-149">Any <a href="dx-graphics-hlsl-scalar.md">scalar HLSL type</a> or <a href="dx-graphics-hlsl-vector.md"><strong>vector HLSL type</strong></a>, surrounded by angle brackets.</span></span> <span data-ttu-id="b72f0-150">Le type par défaut est <strong>float4</strong>.</span><span class="sxs-lookup"><span data-stu-id="b72f0-150">The default type is <strong>float4</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b72f0-151"><span id="Name"></span><span id="name"></span><span id="NAME"></span><em>Nomme</em></span><span class="sxs-lookup"><span data-stu-id="b72f0-151"><span id="Name"></span><span id="name"></span><span id="NAME"></span><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="b72f0-152">Chaîne ASCII qui spécifie le nom de l’objet de texture.</span><span class="sxs-lookup"><span data-stu-id="b72f0-152">An ASCII string that specifies the texture object name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b72f0-153"><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span><em>Extraits</em></span><span class="sxs-lookup"><span data-stu-id="b72f0-153"><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span><em>Samples</em></span></span></p></td>
<td><p><span data-ttu-id="b72f0-154">Nombre d’échantillons (plages comprises entre 1 et 128).</span><span class="sxs-lookup"><span data-stu-id="b72f0-154">The number of samples (ranges between 1 and 128).</span></span></p></td>
</tr>
</tbody>
</table>



 

## <a name="example-1"></a><span data-ttu-id="b72f0-155">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="b72f0-155">Example 1</span></span>

<span data-ttu-id="b72f0-156">Voici un exemple de déclaration d’un objet texture.</span><span class="sxs-lookup"><span data-stu-id="b72f0-156">Here is an example of declaring a texture object.</span></span>


```
Texture2D <float4> MyTex;

Texture2DMS <float4, 128> MyMSTex;
```



## <a name="texture-object-methods"></a><span data-ttu-id="b72f0-157">Méthodes de l’objet texture</span><span class="sxs-lookup"><span data-stu-id="b72f0-157">Texture Object Methods</span></span>

<span data-ttu-id="b72f0-158">Chaque objet texture implémente certaines méthodes ; Voici le tableau qui répertorie toutes les méthodes.</span><span class="sxs-lookup"><span data-stu-id="b72f0-158">Each texture object implements certain methods; here's the table that lists all of the methods.</span></span> <span data-ttu-id="b72f0-159">Consultez la page de référence pour chaque méthode pour voir les objets qui peuvent utiliser cette méthode.</span><span class="sxs-lookup"><span data-stu-id="b72f0-159">See the reference page for each method to see what objects can use that method.</span></span>



| <span data-ttu-id="b72f0-160">Texture, méthode</span><span class="sxs-lookup"><span data-stu-id="b72f0-160">Texture Method</span></span>                                                                     | <span data-ttu-id="b72f0-161">Description</span><span class="sxs-lookup"><span data-stu-id="b72f0-161">Description</span></span>                                                                                                       | <span data-ttu-id="b72f0-162">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b72f0-162">vs\_4\_0</span></span> | <span data-ttu-id="b72f0-163">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="b72f0-163">vs\_4\_1</span></span>  | <span data-ttu-id="b72f0-164">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b72f0-164">ps\_4\_0</span></span> | <span data-ttu-id="b72f0-165">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="b72f0-165">ps\_4\_1</span></span>  | <span data-ttu-id="b72f0-166">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b72f0-166">gs\_4\_0</span></span> | <span data-ttu-id="b72f0-167">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="b72f0-167">gs\_4\_1</span></span>  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|----------|-----------|----------|-----------|----------|-----------|
| [<span data-ttu-id="b72f0-168">CalculateLevelOfDetail</span><span class="sxs-lookup"><span data-stu-id="b72f0-168">CalculateLevelOfDetail</span></span>](dx-graphics-hlsl-to-calculate-lod.md)                    | <span data-ttu-id="b72f0-169">Calculer le LOD, retourner un résultat ancré.</span><span class="sxs-lookup"><span data-stu-id="b72f0-169">Calculate the LOD, return a clamped result.</span></span>                                                                       |          |           |          | <span data-ttu-id="b72f0-170">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-170">x</span></span>         |          |           |
| [<span data-ttu-id="b72f0-171">CalculateLevelOfDetailUnclamped</span><span class="sxs-lookup"><span data-stu-id="b72f0-171">CalculateLevelOfDetailUnclamped</span></span>](dx-graphics-hlsl-to-calculate-lod-unclamped.md) | <span data-ttu-id="b72f0-172">Calcule le LOD, retourne un résultat non ancré.</span><span class="sxs-lookup"><span data-stu-id="b72f0-172">Calculate the LOD, return an unclamped result.</span></span>                                                                    |          |           |          | <span data-ttu-id="b72f0-173">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-173">x</span></span>         |          |           |
| [<span data-ttu-id="b72f0-174">Gather</span><span class="sxs-lookup"><span data-stu-id="b72f0-174">Gather</span></span>](dx-graphics-hlsl-to-gather.md)                                           | <span data-ttu-id="b72f0-175">Obtient les quatre échantillons (composant rouge uniquement) qui seraient utilisés pour l’interpolation bilinéaire lors de l’échantillonnage d’une texture.</span><span class="sxs-lookup"><span data-stu-id="b72f0-175">Gets the four samples (red component only) that would be used for bilinear interpolation when sampling a texture.</span></span> |          | <span data-ttu-id="b72f0-176">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-176">x</span></span>         |          | <span data-ttu-id="b72f0-177">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-177">x</span></span>         |          | <span data-ttu-id="b72f0-178">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-178">x</span></span>         |
| [<span data-ttu-id="b72f0-179">GetDimensions</span><span class="sxs-lookup"><span data-stu-id="b72f0-179">GetDimensions</span></span>](dx-graphics-hlsl-to-getdimensions.md)                             | <span data-ttu-id="b72f0-180">Obtient la dimension de texture pour un niveau mipmap spécifié.</span><span class="sxs-lookup"><span data-stu-id="b72f0-180">Get the texture dimension for a specified mipmap level.</span></span>                                                           | <span data-ttu-id="b72f0-181">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-181">x</span></span>        | <span data-ttu-id="b72f0-182">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-182">x</span></span>         | <span data-ttu-id="b72f0-183">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-183">x</span></span>        | <span data-ttu-id="b72f0-184">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-184">x</span></span>         | <span data-ttu-id="b72f0-185">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-185">x</span></span>        | <span data-ttu-id="b72f0-186">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-186">x</span></span>         |
| [<span data-ttu-id="b72f0-187">GetDimensions, (MultiSample)</span><span class="sxs-lookup"><span data-stu-id="b72f0-187">GetDimensions (MultiSample)</span></span>](dx-graphics-hlsl-to-getdimensions.md)               | <span data-ttu-id="b72f0-188">Obtient la dimension de texture pour un niveau mipmap spécifié.</span><span class="sxs-lookup"><span data-stu-id="b72f0-188">Get the texture dimension for a specified mipmap level.</span></span>                                                           |          | <span data-ttu-id="b72f0-189">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-189">x</span></span>         |          | <span data-ttu-id="b72f0-190">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-190">x</span></span>         |          | <span data-ttu-id="b72f0-191">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-191">x</span></span>         |
| [<span data-ttu-id="b72f0-192">GetSamplePosition</span><span class="sxs-lookup"><span data-stu-id="b72f0-192">GetSamplePosition</span></span>](dx-graphics-hlsl-to-get-sample-position.md)                   | <span data-ttu-id="b72f0-193">Obtient la position de l’échantillon spécifié.</span><span class="sxs-lookup"><span data-stu-id="b72f0-193">Get the position of the specified sample.</span></span>                                                                         |          | <span data-ttu-id="b72f0-194">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-194">x</span></span>         |          | <span data-ttu-id="b72f0-195">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-195">x</span></span>         |          | <span data-ttu-id="b72f0-196">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-196">x</span></span>         |
| [<span data-ttu-id="b72f0-197">Load</span><span class="sxs-lookup"><span data-stu-id="b72f0-197">Load</span></span>](dx-graphics-hlsl-to-load.md)                                               | <span data-ttu-id="b72f0-198">Charger des données sans aucun filtrage ni échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="b72f0-198">Load data without any filtering or sampling.</span></span>                                                                      | <span data-ttu-id="b72f0-199">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-199">x</span></span>        | <span data-ttu-id="b72f0-200">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-200">x</span></span>         | <span data-ttu-id="b72f0-201">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-201">x</span></span>        | <span data-ttu-id="b72f0-202">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-202">x</span></span>         | <span data-ttu-id="b72f0-203">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-203">x</span></span>        | <span data-ttu-id="b72f0-204">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-204">x</span></span>         |
| [<span data-ttu-id="b72f0-205">Charger (multiéchantillonner)</span><span class="sxs-lookup"><span data-stu-id="b72f0-205">Load (Multisample)</span></span>](dx-graphics-hlsl-to-load.md)                                 | <span data-ttu-id="b72f0-206">Charger des données sans aucun filtrage ni échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="b72f0-206">Load data without any filtering or sampling.</span></span>                                                                      |          | <span data-ttu-id="b72f0-207">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-207">x</span></span>         | <span data-ttu-id="b72f0-208">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-208">x</span></span>        | <span data-ttu-id="b72f0-209">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-209">x</span></span>         |          | <span data-ttu-id="b72f0-210">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-210">x</span></span>         |
| [<span data-ttu-id="b72f0-211">Exemple</span><span class="sxs-lookup"><span data-stu-id="b72f0-211">Sample</span></span>](dx-graphics-hlsl-to-sample.md)                                           | <span data-ttu-id="b72f0-212">Échantillonner une texture.</span><span class="sxs-lookup"><span data-stu-id="b72f0-212">Sample a texture.</span></span>                                                                                                 |          |           | <span data-ttu-id="b72f0-213">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-213">x</span></span>        | <span data-ttu-id="b72f0-214">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-214">x</span></span>         |          |           |
| [<span data-ttu-id="b72f0-215">SampleBias</span><span class="sxs-lookup"><span data-stu-id="b72f0-215">SampleBias</span></span>](dx-graphics-hlsl-to-samplebias.md)                                   | <span data-ttu-id="b72f0-216">Échantillonner une texture après avoir appliqué la valeur de biais au niveau de mipmap.</span><span class="sxs-lookup"><span data-stu-id="b72f0-216">Sample a texture, after applying the bias value to the mipmap level.</span></span>                                              |          |           | <span data-ttu-id="b72f0-217">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-217">x</span></span>        | <span data-ttu-id="b72f0-218">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-218">x</span></span>         |          |           |
| [<span data-ttu-id="b72f0-219">SampleCmp</span><span class="sxs-lookup"><span data-stu-id="b72f0-219">SampleCmp</span></span>](dx-graphics-hlsl-to-samplecmp.md)                                     | <span data-ttu-id="b72f0-220">Échantillonner une texture, en utilisant une valeur de comparaison pour rejeter des exemples.</span><span class="sxs-lookup"><span data-stu-id="b72f0-220">Sample a texture, using a comparison value to reject samples.</span></span>                                                     |          |           | <span data-ttu-id="b72f0-221">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-221">x</span></span>        | <span data-ttu-id="b72f0-222">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-222">x</span></span>         |          |           |
| [<span data-ttu-id="b72f0-223">SampleCmpLevelZero</span><span class="sxs-lookup"><span data-stu-id="b72f0-223">SampleCmpLevelZero</span></span>](dx-graphics-hlsl-to-samplecmplevelzero.md)                   | <span data-ttu-id="b72f0-224">Échantillonner une texture (mipmap niveau 0 uniquement), en utilisant une valeur de comparaison pour rejeter les exemples.</span><span class="sxs-lookup"><span data-stu-id="b72f0-224">Sample a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span>                               | <span data-ttu-id="b72f0-225">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-225">x</span></span>        | <span data-ttu-id="b72f0-226">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-226">x</span></span>         | <span data-ttu-id="b72f0-227">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-227">x</span></span>        | <span data-ttu-id="b72f0-228">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-228">x</span></span>         | <span data-ttu-id="b72f0-229">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-229">x</span></span>        | <span data-ttu-id="b72f0-230">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-230">x</span></span>         |
| [<span data-ttu-id="b72f0-231">SampleGrad</span><span class="sxs-lookup"><span data-stu-id="b72f0-231">SampleGrad</span></span>](dx-graphics-hlsl-to-samplegrad.md)                                   | <span data-ttu-id="b72f0-232">Échantillonner une texture à l’aide d’un dégradé pour influencer la façon dont l’emplacement de l’échantillon est calculé.</span><span class="sxs-lookup"><span data-stu-id="b72f0-232">Sample a texture using a gradient to influence the way the sample location is calculated.</span></span>                         | <span data-ttu-id="b72f0-233">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-233">x</span></span>        | <span data-ttu-id="b72f0-234">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-234">x</span></span>         | <span data-ttu-id="b72f0-235">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-235">x</span></span>        | <span data-ttu-id="b72f0-236">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-236">x</span></span>         | <span data-ttu-id="b72f0-237">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-237">x</span></span>        | <span data-ttu-id="b72f0-238">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-238">x</span></span>         |
| [<span data-ttu-id="b72f0-239">SampleLevel</span><span class="sxs-lookup"><span data-stu-id="b72f0-239">SampleLevel</span></span>](dx-graphics-hlsl-to-samplelevel.md)                                 | <span data-ttu-id="b72f0-240">Échantillonner une texture sur le niveau de mipmap spécifié.</span><span class="sxs-lookup"><span data-stu-id="b72f0-240">Sample a texture on the specified mipmap level.</span></span>                                                                   | <span data-ttu-id="b72f0-241">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-241">x</span></span>        | <span data-ttu-id="b72f0-242">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-242">x</span></span>         | <span data-ttu-id="b72f0-243">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-243">x</span></span>        | <span data-ttu-id="b72f0-244">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-244">x</span></span>         | <span data-ttu-id="b72f0-245">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-245">x</span></span>        | <span data-ttu-id="b72f0-246">x</span><span class="sxs-lookup"><span data-stu-id="b72f0-246">x</span></span>         |



 

### <a name="return-type"></a><span data-ttu-id="b72f0-247">Type de retour</span><span class="sxs-lookup"><span data-stu-id="b72f0-247">Return Type</span></span>

<span data-ttu-id="b72f0-248">Le type de retour d’une méthode d’objet de texture est float4, sauf indication contraire, à l’exception des objets de texture d’anticrénelage à échantillonnages qui nécessitent toujours le type et le nombre d’échantillons spécifiés.</span><span class="sxs-lookup"><span data-stu-id="b72f0-248">The return type of a texture object method is float4 unless specified otherwise, with the exception of the multisampled anti-aliased texture objects that always need the type and sample count specified.</span></span> <span data-ttu-id="b72f0-249">Le type de retour est le même que le type de ressource de texture ([**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span><span class="sxs-lookup"><span data-stu-id="b72f0-249">The return type is the same as the texture resource type ([**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span></span> <span data-ttu-id="b72f0-250">En d’autres termes, il peut s’agir de l’un des types suivants.</span><span class="sxs-lookup"><span data-stu-id="b72f0-250">In other words, it can be any of the following types.</span></span>



| <span data-ttu-id="b72f0-251">Type</span><span class="sxs-lookup"><span data-stu-id="b72f0-251">Type</span></span>                       | <span data-ttu-id="b72f0-252">Description</span><span class="sxs-lookup"><span data-stu-id="b72f0-252">Description</span></span>                                                                                                                                                             |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b72f0-253">float</span><span class="sxs-lookup"><span data-stu-id="b72f0-253">float</span></span>                      | <span data-ttu-id="b72f0-254">32 bits float (voir [règles à virgule flottante](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) pour les différences par rapport à IEEE float)</span><span class="sxs-lookup"><span data-stu-id="b72f0-254">32-bit float (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span>                            |
| <span data-ttu-id="b72f0-255">int</span><span class="sxs-lookup"><span data-stu-id="b72f0-255">int</span></span>                        | <span data-ttu-id="b72f0-256">Entier 32 bits signé</span><span class="sxs-lookup"><span data-stu-id="b72f0-256">32-bit signed integer</span></span>                                                                                                                                                   |
| <span data-ttu-id="b72f0-257">nombre entier non signé</span><span class="sxs-lookup"><span data-stu-id="b72f0-257">unsigned int</span></span>               | <span data-ttu-id="b72f0-258">Entier non signé 32 bits</span><span class="sxs-lookup"><span data-stu-id="b72f0-258">32-bit unsigned integer</span></span>                                                                                                                                                 |
| <span data-ttu-id="b72f0-259">ronfler</span><span class="sxs-lookup"><span data-stu-id="b72f0-259">snorm</span></span>                      | <span data-ttu-id="b72f0-260">32-bit float dans la plage comprise entre-1 et 1 (voir les [règles à virgule flottante](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) pour les différences par rapport à IEEE float)</span><span class="sxs-lookup"><span data-stu-id="b72f0-260">32-bit float in range -1 to 1 inclusive (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span> |
| <span data-ttu-id="b72f0-261">unorm</span><span class="sxs-lookup"><span data-stu-id="b72f0-261">unorm</span></span>                      | <span data-ttu-id="b72f0-262">virgule flottante 32 bits dans la plage de 0 à 1 inclusive (voir les [règles à virgule flottante](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) pour les différences par rapport à IEEE float)</span><span class="sxs-lookup"><span data-stu-id="b72f0-262">32-bit float in range 0 to 1 inclusive (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span>  |
| <span data-ttu-id="b72f0-263">tout type ou struct de texture</span><span class="sxs-lookup"><span data-stu-id="b72f0-263">any texture type or struct</span></span> | <span data-ttu-id="b72f0-264">Le nombre de composants retournés doit être compris entre 1 et 3 inclus.</span><span class="sxs-lookup"><span data-stu-id="b72f0-264">The number of components returned must be between 1 and 3 inclusive.</span></span>                                                                                                    |



 

<span data-ttu-id="b72f0-265">En outre, le type de retour peut être n’importe quel type de texture, y compris une structure, mais il doit être inférieur à 4 composants tels qu’un type float1 qui retourne un composant.</span><span class="sxs-lookup"><span data-stu-id="b72f0-265">In addition, the return type can be any texture type including a structure but, it must be less than 4 components such as a float1 type which returns one component.</span></span>

## <a name="default-values-for-missing-components-in-a-texture"></a><span data-ttu-id="b72f0-266">Valeurs par défaut pour les composants manquants dans une texture</span><span class="sxs-lookup"><span data-stu-id="b72f0-266">Default Values for Missing Components in a Texture</span></span>

<span data-ttu-id="b72f0-267">La valeur par défaut pour les composants manquants dans un type de ressource de texture est égale à zéro pour tout composant, à l’exception du composant alpha (A); la valeur par défaut pour le A manquant est un.</span><span class="sxs-lookup"><span data-stu-id="b72f0-267">The default value for missing components in a texture resource type is zero for any component except the alpha component (A); the default value for the missing A is one.</span></span> <span data-ttu-id="b72f0-268">La façon dont celle-ci apparaît dans le nuanceur dépend du type de ressource de texture.</span><span class="sxs-lookup"><span data-stu-id="b72f0-268">The way that this one appears to the shader depends on the texture resource type.</span></span> <span data-ttu-id="b72f0-269">Il prend la forme du premier composant typé qui est réellement présent dans le type de ressource de texture (à partir de la gauche dans l’ordre RVBA).</span><span class="sxs-lookup"><span data-stu-id="b72f0-269">It takes the form of the first typed component that is actually present in the texture resource type (starting from the left in RGBA order).</span></span> <span data-ttu-id="b72f0-270">Si ce formulaire est UNORM ou FLOAT, la valeur par défaut pour le A manquant est 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="b72f0-270">If this form is UNORM or FLOAT, the default value for the missing A is 1.0f.</span></span> <span data-ttu-id="b72f0-271">Si le formulaire est Saint ou UINT, la valeur par défaut pour le A manquant est 0x1.</span><span class="sxs-lookup"><span data-stu-id="b72f0-271">If the form is SINT or UINT, the default value for the missing A is 0x1.</span></span>

<span data-ttu-id="b72f0-272">Par exemple, lorsqu’un nuanceur lit [**le \_ format \_ dxgi \_ R24 \_ UNORM \_ x8**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) , les valeurs par défaut pour G et B sont égales à zéro et la valeur par défaut est 1,0 f ; lorsqu’un nuanceur lit le type de ressource de texture [**dxgi \_ format \_ R16G16 \_ uint**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) , la valeur par défaut de B est zéro et la valeur par défaut pour est 0x00000001 ; quand un nuanceur lit le [**\_ format dxgi \_ R16 \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) de ressource de la texture Saint, les valeurs par défaut pour G et B sont égales à zéro et la valeur par défaut de est 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="b72f0-272">For example, when a shader reads the [**DXGI\_FORMAT\_R24\_UNORM\_X8\_TYPELESS**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default values for G and B are zero and the default value for A is 1.0f; when a shader reads the [**DXGI\_FORMAT\_R16G16\_UINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default value for B is zero and the default value for A is 0x00000001; when a shader reads the [**DXGI\_FORMAT\_R16\_SINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default values for G and B are zero and the default value for A is 0x00000001.</span></span>

## <a name="example-2"></a><span data-ttu-id="b72f0-273">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="b72f0-273">Example 2</span></span>

<span data-ttu-id="b72f0-274">Voici un exemple d’échantillonnage de texture à l’aide d’une méthode de texture.</span><span class="sxs-lookup"><span data-stu-id="b72f0-274">Here is an example of texture sampling using a texture method.</span></span>


```
sampler MySamp;
Texture2D <float4> MyTex;
 
float4 main( float2 TexCoords[2] : TEXCOORD ) : SV_Target
{
    return MyTex.Sample( MySamp, TexCoords[0] ));
}
```



## <a name="minimum-shader-model"></a><span data-ttu-id="b72f0-275">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="b72f0-275">Minimum Shader Model</span></span>

<span data-ttu-id="b72f0-276">Cet objet est pris en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="b72f0-276">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="b72f0-277">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="b72f0-277">Shader Model</span></span>                                                        | <span data-ttu-id="b72f0-278">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="b72f0-278">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="b72f0-279">[Nuancier modèle 4](dx-graphics-hlsl-sm4.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="b72f0-279">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="b72f0-280">Oui</span><span class="sxs-lookup"><span data-stu-id="b72f0-280">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b72f0-281">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b72f0-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b72f0-282">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="b72f0-282">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

