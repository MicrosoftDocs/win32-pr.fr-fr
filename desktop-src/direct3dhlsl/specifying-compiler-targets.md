---
title: Spécification de cibles de compilateur
description: Ici, nous répertorions les cibles pour les différents profils pris en charge par D3DCompile \ Functions et le compilateur HLSL.
ms.assetid: 594E1C14-C1D4-4207-91A1-28892CE6D821
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d68fc6c5a202ad537b02a20846d36526533240f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382735"
---
# <a name="specifying-compiler-targets"></a><span data-ttu-id="3dcf7-103">Spécification de cibles de compilateur</span><span class="sxs-lookup"><span data-stu-id="3dcf7-103">Specifying Compiler Targets</span></span>

<span data-ttu-id="3dcf7-104">Vous devez spécifier la cible de nuanceur (jeu de fonctionnalités de nuanceur) à compiler lorsque vous appelez la fonction [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile), [**D3DCompile2**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2)ou [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) .</span><span class="sxs-lookup"><span data-stu-id="3dcf7-104">You need to specify the shader target — set of shader features — to compile against when you call the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile), [**D3DCompile2**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2), or [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) function.</span></span> <span data-ttu-id="3dcf7-105">Ici, nous répertorions les cibles pour les différents profils que les fonctions **D3DCompile \*** et le compilateur HLSL prennent en charge.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-105">Here we list the targets for various profiles that the **D3DCompile\*** functions and the HLSL compiler support.</span></span>

-   [<span data-ttu-id="3dcf7-106">Niveaux de fonctionnalité Direct3D 11,0 et 11,1</span><span class="sxs-lookup"><span data-stu-id="3dcf7-106">Direct3D 11.0 and 11.1 feature levels</span></span>](#direct3d-110-and-111-feature-levels)
-   [<span data-ttu-id="3dcf7-107">Niveau de fonctionnalité Direct3D 10,1</span><span class="sxs-lookup"><span data-stu-id="3dcf7-107">Direct3D 10.1 feature level</span></span>](#direct3d-101-feature-level)
-   [<span data-ttu-id="3dcf7-108">Niveau de fonctionnalité Direct3D 10,0</span><span class="sxs-lookup"><span data-stu-id="3dcf7-108">Direct3D 10.0 feature level</span></span>](#direct3d-100-feature-level)
-   [<span data-ttu-id="3dcf7-109">Niveaux de fonctionnalité Direct3D 9,1, 9,2 et 9,3</span><span class="sxs-lookup"><span data-stu-id="3dcf7-109">Direct3D 9.1, 9.2, and 9.3 feature levels</span></span>](#direct3d-91-92-and-93-feature-levels)
-   [<span data-ttu-id="3dcf7-110">Modèle de nuanceur Direct3D 9 hérité 3,0</span><span class="sxs-lookup"><span data-stu-id="3dcf7-110">Legacy Direct3D 9 Shader Model 3.0</span></span>](#legacy-direct3d-9-shader-model-30)
-   [<span data-ttu-id="3dcf7-111">Modèle de nuanceur Direct3D 9 hérité 2,0</span><span class="sxs-lookup"><span data-stu-id="3dcf7-111">Legacy Direct3D 9 Shader Model 2.0</span></span>](#legacy-direct3d-9-shader-model-20)
-   [<span data-ttu-id="3dcf7-112">Modèle de nuanceur Direct3D 9 hérité 1. x</span><span class="sxs-lookup"><span data-stu-id="3dcf7-112">Legacy Direct3D 9 Shader Model 1.x</span></span>](#legacy-direct3d-9-shader-model-1x)
-   [<span data-ttu-id="3dcf7-113">Effets hérités</span><span class="sxs-lookup"><span data-stu-id="3dcf7-113">Legacy Effects</span></span>](#legacy-effects)
-   [<span data-ttu-id="3dcf7-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="3dcf7-114">Notes</span></span>](#notes)
-   [<span data-ttu-id="3dcf7-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3dcf7-115">Related topics</span></span>](#related-topics)

## <a name="direct3d-110-and-111-feature-levels"></a><span data-ttu-id="3dcf7-116">Niveaux de fonctionnalité Direct3D 11,0 et 11,1</span><span class="sxs-lookup"><span data-stu-id="3dcf7-116">Direct3D 11.0 and 11.1 feature levels</span></span>

<span data-ttu-id="3dcf7-117">Voici les cibles de nuanceur que les niveaux de [fonctionnalité](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) Direct3D 11,0 et 11,1 prennent en charge.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-117">Here are the shader targets that Direct3D 11.0 and 11.1 [feature levels](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) support.</span></span>



| <span data-ttu-id="3dcf7-118">Cible</span><span class="sxs-lookup"><span data-stu-id="3dcf7-118">Target</span></span>   | <span data-ttu-id="3dcf7-119">Description</span><span class="sxs-lookup"><span data-stu-id="3dcf7-119">Description</span></span>                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dcf7-120">CS \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3dcf7-120">cs\_5\_0</span></span> | <span data-ttu-id="3dcf7-121">DirectCompute 5,0 ([nuanceur de calcul](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))</span><span class="sxs-lookup"><span data-stu-id="3dcf7-121">DirectCompute 5.0 ([compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))</span></span>                              |
| <span data-ttu-id="3dcf7-122">DS \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3dcf7-122">ds\_5\_0</span></span> | [<span data-ttu-id="3dcf7-123">Nuanceur de domaine</span><span class="sxs-lookup"><span data-stu-id="3dcf7-123">Domain shader</span></span>](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)             |
| <span data-ttu-id="3dcf7-124">GS \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3dcf7-124">gs\_5\_0</span></span> | <span data-ttu-id="3dcf7-125">[Nuanceur Geometry](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3dcf7-125">[Geometry shader](/previous-versions//bb205146(v=vs.85))</span></span> |
| <span data-ttu-id="3dcf7-126">HS \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3dcf7-126">hs\_5\_0</span></span> | [<span data-ttu-id="3dcf7-127">Nuanceur de coque</span><span class="sxs-lookup"><span data-stu-id="3dcf7-127">Hull shader</span></span>](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)                   |
| <span data-ttu-id="3dcf7-128">PS \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3dcf7-128">ps\_5\_0</span></span> | <span data-ttu-id="3dcf7-129">[Nuanceur de pixels](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3dcf7-129">[Pixel shader](/previous-versions//bb205146(v=vs.85))</span></span>          |
| <span data-ttu-id="3dcf7-130">vs \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3dcf7-130">vs\_5\_0</span></span> | <span data-ttu-id="3dcf7-131">[Nuanceur de sommets](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3dcf7-131">[Vertex shader](/previous-versions//bb205146(v=vs.85))</span></span>       |



 

## <a name="direct3d-101-feature-level"></a><span data-ttu-id="3dcf7-132">Niveau de fonctionnalité Direct3D 10,1</span><span class="sxs-lookup"><span data-stu-id="3dcf7-132">Direct3D 10.1 feature level</span></span>

<span data-ttu-id="3dcf7-133">Voici les cibles de nuanceur que le [niveau de fonctionnalité](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) Direct3D 10,1 prend en charge.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-133">Here are the shader targets that the Direct3D 10.1 [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) supports.</span></span>



| <span data-ttu-id="3dcf7-134">Cible</span><span class="sxs-lookup"><span data-stu-id="3dcf7-134">Target</span></span>   | <span data-ttu-id="3dcf7-135">Description</span><span class="sxs-lookup"><span data-stu-id="3dcf7-135">Description</span></span>                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dcf7-136">CS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="3dcf7-136">cs\_4\_1</span></span> | <span data-ttu-id="3dcf7-137">DirectCompute 4,1 ([nuanceur de calcul](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)) ¹</span><span class="sxs-lookup"><span data-stu-id="3dcf7-137">DirectCompute 4.1 ([compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))¹</span></span>                             |
| <span data-ttu-id="3dcf7-138">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="3dcf7-138">gs\_4\_1</span></span> | <span data-ttu-id="3dcf7-139">[Nuanceur Geometry](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3dcf7-139">[Geometry shader](/previous-versions//bb205146(v=vs.85))</span></span> |
| <span data-ttu-id="3dcf7-140">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="3dcf7-140">ps\_4\_1</span></span> | <span data-ttu-id="3dcf7-141">[Nuanceur de pixels](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3dcf7-141">[Pixel shader](/previous-versions//bb205146(v=vs.85))</span></span>          |
| <span data-ttu-id="3dcf7-142">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="3dcf7-142">vs\_4\_1</span></span> | <span data-ttu-id="3dcf7-143">[Nuanceur de sommets](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3dcf7-143">[Vertex shader](/previous-versions//bb205146(v=vs.85))</span></span>       |



 

## <a name="direct3d-100-feature-level"></a><span data-ttu-id="3dcf7-144">Niveau de fonctionnalité Direct3D 10,0</span><span class="sxs-lookup"><span data-stu-id="3dcf7-144">Direct3D 10.0 feature level</span></span>

<span data-ttu-id="3dcf7-145">Voici les cibles de nuanceur que le [niveau de fonctionnalité](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) Direct3D 10,0 prend en charge.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-145">Here are the shader targets that the Direct3D 10.0 [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) supports.</span></span>



| <span data-ttu-id="3dcf7-146">Cible</span><span class="sxs-lookup"><span data-stu-id="3dcf7-146">Target</span></span>   | <span data-ttu-id="3dcf7-147">Description</span><span class="sxs-lookup"><span data-stu-id="3dcf7-147">Description</span></span>                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dcf7-148">CS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3dcf7-148">cs\_4\_0</span></span> | <span data-ttu-id="3dcf7-149">DirectCompute 4,0 ([nuanceur de calcul](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)) ¹</span><span class="sxs-lookup"><span data-stu-id="3dcf7-149">DirectCompute 4.0 ([compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))¹</span></span>                             |
| <span data-ttu-id="3dcf7-150">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3dcf7-150">gs\_4\_0</span></span> | <span data-ttu-id="3dcf7-151">[Nuanceur Geometry](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3dcf7-151">[Geometry shader](/previous-versions//bb205146(v=vs.85))</span></span> |
| <span data-ttu-id="3dcf7-152">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3dcf7-152">ps\_4\_0</span></span> | <span data-ttu-id="3dcf7-153">[Nuanceur de pixels](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3dcf7-153">[Pixel shader](/previous-versions//bb205146(v=vs.85))</span></span>          |
| <span data-ttu-id="3dcf7-154">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3dcf7-154">vs\_4\_0</span></span> | <span data-ttu-id="3dcf7-155">[Nuanceur de sommets](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3dcf7-155">[Vertex shader](/previous-versions//bb205146(v=vs.85))</span></span>       |



 

## <a name="direct3d-91-92-and-93-feature-levels"></a><span data-ttu-id="3dcf7-156">Niveaux de fonctionnalité Direct3D 9,1, 9,2 et 9,3</span><span class="sxs-lookup"><span data-stu-id="3dcf7-156">Direct3D 9.1, 9.2, and 9.3 feature levels</span></span>

<span data-ttu-id="3dcf7-157">Voici les cibles de nuanceur que les [niveaux de fonctionnalité](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) Direct3D 9,1, 9,2 et 9,3 prennent en charge.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-157">Here are the shader targets that Direct3D 9.1, 9.2 and 9.3 [feature levels](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) support.</span></span>

> [!Note]  
> <span data-ttu-id="3dcf7-158">Lorsque vous utilisez les \* \_ \_ \_ \_ \_ profils de nuanceur HLSL de 4 niveaux 9 x, vous utilisez implicitement les profils [Shader Model 2. x](dx-graphics-hlsl-sm2.md) pour prendre en charge le matériel compatible Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-158">When you use the \*\_4\_0\_level\_9\_x HLSL shader profiles, you implicitly use of the [Shader Model 2.x](dx-graphics-hlsl-sm2.md) profiles to support Direct3D 9 capable hardware.</span></span> <span data-ttu-id="3dcf7-159">Les profils Shader Model 2. x prennent en charge un comportement de contrôle de Flow plus limité que le [modèle de nuanceur 4. x](dx-graphics-hlsl-sm4.md) et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-159">Shader Model 2.x profiles support more limited flow control behavior than the [Shader Model 4.x](dx-graphics-hlsl-sm4.md) and later profiles.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3dcf7-160">Cible</span><span class="sxs-lookup"><span data-stu-id="3dcf7-160">Target</span></span></th>
<th><span data-ttu-id="3dcf7-161">Description</span><span class="sxs-lookup"><span data-stu-id="3dcf7-161">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3dcf7-162">ps_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="3dcf7-162">ps_4_0_level_9_1</span></span></td>
<td><span data-ttu-id="3dcf7-163">[Nuanceur de pixels](/previous-versions//bb205146(v=vs.85)) pour 9,1 et 9,2 (limites similaires à ps_2_0)</span><span class="sxs-lookup"><span data-stu-id="3dcf7-163">[Pixel shader](/previous-versions//bb205146(v=vs.85)) for 9.1 and 9.2 (similar limits to ps_2_0)</span></span>
<ul>
<li><span data-ttu-id="3dcf7-164">64 instructions de texture arithmétique et 32</span><span class="sxs-lookup"><span data-stu-id="3dcf7-164">64 arithmetic and 32 texture instructions</span></span></li>
<li><span data-ttu-id="3dcf7-165">12 registres temporaires</span><span class="sxs-lookup"><span data-stu-id="3dcf7-165">12 temporary registers</span></span></li>
<li><span data-ttu-id="3dcf7-166">4 niveaux de lectures dépendantes</span><span class="sxs-lookup"><span data-stu-id="3dcf7-166">4 levels of dependent reads</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3dcf7-167">ps_4_0_level_9_3</span><span class="sxs-lookup"><span data-stu-id="3dcf7-167">ps_4_0_level_9_3</span></span></td>
<td><span data-ttu-id="3dcf7-168"><a href="/previous-versions//bb205146(v=vs.85)">Nuanceur de pixels</a> pour 9,3 (limites similaires à ps_2_x ² avec des fonctionnalités de nuanceur supplémentaires)</span><span class="sxs-lookup"><span data-stu-id="3dcf7-168"><a href="/previous-versions//bb205146(v=vs.85)">Pixel shader</a> for 9.3 (similar limits to ps_2_x² with additional shader features)</span></span>
<ul>
<li><span data-ttu-id="3dcf7-169">instructions 512</span><span class="sxs-lookup"><span data-stu-id="3dcf7-169">512 instructions</span></span></li>
<li><span data-ttu-id="3dcf7-170">32 registres temporaires</span><span class="sxs-lookup"><span data-stu-id="3dcf7-170">32 temporary registers</span></span></li>
<li><span data-ttu-id="3dcf7-171">Contrôle de Flow statique (profondeur maximale de 4)</span><span class="sxs-lookup"><span data-stu-id="3dcf7-171">Static flow control (max depth of 4)</span></span></li>
<li><span data-ttu-id="3dcf7-172">Contrôle de workflow dynamique (profondeur maximale de 24)</span><span class="sxs-lookup"><span data-stu-id="3dcf7-172">Dynamic flow control (max depth of 24)</span></span></li>
<li><span data-ttu-id="3dcf7-173">D3DPS20CAPS_ARBITRARYSWIZZLE</span><span class="sxs-lookup"><span data-stu-id="3dcf7-173">D3DPS20CAPS_ARBITRARYSWIZZLE</span></span></li>
<li><span data-ttu-id="3dcf7-174">D3DPS20CAPS_GRADIENTINSTRUCTIONS</span><span class="sxs-lookup"><span data-stu-id="3dcf7-174">D3DPS20CAPS_GRADIENTINSTRUCTIONS</span></span></li>
<li><span data-ttu-id="3dcf7-175">D3DPS20CAPS_PREDICATION</span><span class="sxs-lookup"><span data-stu-id="3dcf7-175">D3DPS20CAPS_PREDICATION</span></span></li>
<li><span data-ttu-id="3dcf7-176">D3DPS20CAPS_NODEPENDENTREADLIMIT</span><span class="sxs-lookup"><span data-stu-id="3dcf7-176">D3DPS20CAPS_NODEPENDENTREADLIMIT</span></span></li>
<li><span data-ttu-id="3dcf7-177">D3DPS20CAPS_NOTEXINSTRUCTIONLIMIT</span><span class="sxs-lookup"><span data-stu-id="3dcf7-177">D3DPS20CAPS_NOTEXINSTRUCTIONLIMIT</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3dcf7-178">vs_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="3dcf7-178">vs_4_0_level_9_1</span></span></td>
<td><span data-ttu-id="3dcf7-179"><a href="/previous-versions//bb205146(v=vs.85)">Vertex shader</a> pour 9,1 et 9,2 (semblable à vs_2_0)</span><span class="sxs-lookup"><span data-stu-id="3dcf7-179"><a href="/previous-versions//bb205146(v=vs.85)">Vertex shader</a> for 9.1 and 9.2 (similar to vs_2_0)</span></span>
<ul>
<li><span data-ttu-id="3dcf7-180">instructions 256</span><span class="sxs-lookup"><span data-stu-id="3dcf7-180">256 instructions</span></span></li>
<li><span data-ttu-id="3dcf7-181">12 registres temporaires</span><span class="sxs-lookup"><span data-stu-id="3dcf7-181">12 temporary registers</span></span></li>
<li><span data-ttu-id="3dcf7-182">Contrôle de Flow statique (profondeur maximale de 1)</span><span class="sxs-lookup"><span data-stu-id="3dcf7-182">Static flow control (max depth of 1)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3dcf7-183">vs_4_0_level_9_3</span><span class="sxs-lookup"><span data-stu-id="3dcf7-183">vs_4_0_level_9_3</span></span></td>
<td><span data-ttu-id="3dcf7-184"><a href="/previous-versions//bb205146(v=vs.85)">Vertex shader</a> pour 9,3 (semblable à vs_2_a ² avec des fonctionnalités de nuanceur supplémentaires et l’instanciation)</span><span class="sxs-lookup"><span data-stu-id="3dcf7-184"><a href="/previous-versions//bb205146(v=vs.85)">Vertex shader</a> for 9.3 (similar to vs_2_a² with additional shader features and instancing)</span></span>
<ul>
<li><span data-ttu-id="3dcf7-185">instructions 256</span><span class="sxs-lookup"><span data-stu-id="3dcf7-185">256 instructions</span></span></li>
<li><span data-ttu-id="3dcf7-186">32 registres temporaires</span><span class="sxs-lookup"><span data-stu-id="3dcf7-186">32 temporary registers</span></span></li>
<li><span data-ttu-id="3dcf7-187">Contrôle de Flow statique (profondeur maximale de 4)</span><span class="sxs-lookup"><span data-stu-id="3dcf7-187">Static flow control (max depth of 4)</span></span></li>
<li><span data-ttu-id="3dcf7-188">D3DVS20CAPS_PREDICATION</span><span class="sxs-lookup"><span data-stu-id="3dcf7-188">D3DVS20CAPS_PREDICATION</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="legacy-direct3d-9-shader-model-30"></a><span data-ttu-id="3dcf7-189">Modèle de nuanceur Direct3D 9 hérité 3,0</span><span class="sxs-lookup"><span data-stu-id="3dcf7-189">Legacy Direct3D 9 Shader Model 3.0</span></span>

<span data-ttu-id="3dcf7-190">Voici les cibles de nuanceur pour le modèle de nuanceur Direct3D 9 hérité 3,0 ³.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-190">Here are the shader targets for legacy Direct3D 9 shader model 3.0³.</span></span>



| <span data-ttu-id="3dcf7-191">Cible</span><span class="sxs-lookup"><span data-stu-id="3dcf7-191">Target</span></span>    | <span data-ttu-id="3dcf7-192">Description</span><span class="sxs-lookup"><span data-stu-id="3dcf7-192">Description</span></span>                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dcf7-193">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3dcf7-193">ps\_3\_0</span></span>  | <span data-ttu-id="3dcf7-194">[Nuanceur de pixels](/previous-versions//bb205146(v=vs.85)) 3,0</span><span class="sxs-lookup"><span data-stu-id="3dcf7-194">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 3.0</span></span>               |
| <span data-ttu-id="3dcf7-195">\_logiciel PS 3 \_</span><span class="sxs-lookup"><span data-stu-id="3dcf7-195">ps\_3\_sw</span></span> | <span data-ttu-id="3dcf7-196">[Nuanceur de pixels](/previous-versions//bb205146(v=vs.85)) 3,0 (logiciel)</span><span class="sxs-lookup"><span data-stu-id="3dcf7-196">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 3.0 (software)</span></span>    |
| <span data-ttu-id="3dcf7-197">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3dcf7-197">vs\_3\_0</span></span>  | <span data-ttu-id="3dcf7-198">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 3,0</span><span class="sxs-lookup"><span data-stu-id="3dcf7-198">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 3.0</span></span>            |
| <span data-ttu-id="3dcf7-199">vs \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3dcf7-199">vs\_3\_sw</span></span> | <span data-ttu-id="3dcf7-200">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 3,0 (logiciel)</span><span class="sxs-lookup"><span data-stu-id="3dcf7-200">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 3.0 (software)</span></span> |



 

## <a name="legacy-direct3d-9-shader-model-20"></a><span data-ttu-id="3dcf7-201">Modèle de nuanceur Direct3D 9 hérité 2,0</span><span class="sxs-lookup"><span data-stu-id="3dcf7-201">Legacy Direct3D 9 Shader Model 2.0</span></span>

<span data-ttu-id="3dcf7-202">Voici les cibles de nuanceur pour le modèle de nuanceur Direct3D 9 hérité 2,0 ³.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-202">Here are the shader targets for legacy Direct3D 9 shader model 2.0³.</span></span>



| <span data-ttu-id="3dcf7-203">Cible</span><span class="sxs-lookup"><span data-stu-id="3dcf7-203">Target</span></span>    | <span data-ttu-id="3dcf7-204">Description</span><span class="sxs-lookup"><span data-stu-id="3dcf7-204">Description</span></span>                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dcf7-205">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3dcf7-205">ps\_2\_0</span></span>  | <span data-ttu-id="3dcf7-206">[Nuanceur de pixels](/previous-versions//bb205146(v=vs.85)) 2,0</span><span class="sxs-lookup"><span data-stu-id="3dcf7-206">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 2.0</span></span>             |
| <span data-ttu-id="3dcf7-207">PS \_ 2 \_ a</span><span class="sxs-lookup"><span data-stu-id="3dcf7-207">ps\_2\_a</span></span>  | <span data-ttu-id="3dcf7-208">[Nuanceur de pixels](/previous-versions//bb205146(v=vs.85)) 2A</span><span class="sxs-lookup"><span data-stu-id="3dcf7-208">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 2a</span></span>              |
| <span data-ttu-id="3dcf7-209">PS \_ 2 \_ b</span><span class="sxs-lookup"><span data-stu-id="3dcf7-209">ps\_2\_b</span></span>  | <span data-ttu-id="3dcf7-210">[Nuanceur de pixels](/previous-versions//bb205146(v=vs.85)) 2b</span><span class="sxs-lookup"><span data-stu-id="3dcf7-210">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 2b</span></span>              |
| <span data-ttu-id="3dcf7-211">\_logiciel PS 2 \_</span><span class="sxs-lookup"><span data-stu-id="3dcf7-211">ps\_2\_sw</span></span> | <span data-ttu-id="3dcf7-212">Logiciel [nuanceur de pixels](/previous-versions//bb205146(v=vs.85)) 2,0</span><span class="sxs-lookup"><span data-stu-id="3dcf7-212">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 2.0 software</span></span>    |
| <span data-ttu-id="3dcf7-213">vs \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3dcf7-213">vs\_2\_0</span></span>  | <span data-ttu-id="3dcf7-214">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 2,0</span><span class="sxs-lookup"><span data-stu-id="3dcf7-214">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 2.0</span></span>          |
| <span data-ttu-id="3dcf7-215">vs \_ 2 \_ a</span><span class="sxs-lookup"><span data-stu-id="3dcf7-215">vs\_2\_a</span></span>  | <span data-ttu-id="3dcf7-216">[Nuanceur de sommet](/previous-versions//bb205146(v=vs.85)) 2A</span><span class="sxs-lookup"><span data-stu-id="3dcf7-216">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 2a</span></span>           |
| <span data-ttu-id="3dcf7-217">vs \_ 2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3dcf7-217">vs\_2\_sw</span></span> | <span data-ttu-id="3dcf7-218">Logiciel [vertex shader](/previous-versions//bb205146(v=vs.85)) 2,0</span><span class="sxs-lookup"><span data-stu-id="3dcf7-218">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 2.0 software</span></span> |



 

## <a name="legacy-direct3d-9-shader-model-1x"></a><span data-ttu-id="3dcf7-219">Modèle de nuanceur Direct3D 9 hérité 1. x</span><span class="sxs-lookup"><span data-stu-id="3dcf7-219">Legacy Direct3D 9 Shader Model 1.x</span></span>

<span data-ttu-id="3dcf7-220">Voici les cibles de nuanceur pour le modèle de nuanceur Direct3D 9 hérité 1. x ⁴.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-220">Here are the shader targets for legacy Direct3D 9 shader model 1.x⁴.</span></span>



| <span data-ttu-id="3dcf7-221">Cible</span><span class="sxs-lookup"><span data-stu-id="3dcf7-221">Target</span></span>   | <span data-ttu-id="3dcf7-222">Description</span><span class="sxs-lookup"><span data-stu-id="3dcf7-222">Description</span></span>                                                                                                                                                                       |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dcf7-223">TX \_ 1 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3dcf7-223">tx\_1\_0</span></span> | <span data-ttu-id="3dcf7-224">Profil de nuanceur de texture qui utilise les fonctions D3DX9 ⁵ héritées [**D3DXCreateTextureShader**](/windows/desktop/direct3d9/d3dxcreatetextureshader) et [**D3DXFillTextureTX**](/windows/desktop/direct3d9/d3dxfilltexturetx)</span><span class="sxs-lookup"><span data-stu-id="3dcf7-224">Texture shader profile that legacy D3DX9⁵ functions [**D3DXCreateTextureShader**](/windows/desktop/direct3d9/d3dxcreatetextureshader) and [**D3DXFillTextureTX**](/windows/desktop/direct3d9/d3dxfilltexturetx) use</span></span> |
| <span data-ttu-id="3dcf7-225">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="3dcf7-225">vs\_1\_1</span></span> | <span data-ttu-id="3dcf7-226">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 1,1</span><span class="sxs-lookup"><span data-stu-id="3dcf7-226">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 1.1</span></span>                                                            |



 

## <a name="legacy-effects"></a><span data-ttu-id="3dcf7-227">Effets hérités</span><span class="sxs-lookup"><span data-stu-id="3dcf7-227">Legacy Effects</span></span>

<span data-ttu-id="3dcf7-228">Voici les objectifs des effets hérités.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-228">Here are the effect targets for legacy effects.</span></span>



| <span data-ttu-id="3dcf7-229">Cible</span><span class="sxs-lookup"><span data-stu-id="3dcf7-229">Target</span></span>   | <span data-ttu-id="3dcf7-230">Description</span><span class="sxs-lookup"><span data-stu-id="3dcf7-230">Description</span></span>                               |
|----------|-------------------------------------------|
| <span data-ttu-id="3dcf7-231">FX \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3dcf7-231">fx\_2\_0</span></span> | <span data-ttu-id="3dcf7-232">Effets (FX) pour Direct3D 9 dans D3DX9 ⁵</span><span class="sxs-lookup"><span data-stu-id="3dcf7-232">Effects (FX) for Direct3D 9 in D3DX9⁵</span></span>     |
| <span data-ttu-id="3dcf7-233">FX \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3dcf7-233">fx\_4\_0</span></span> | <span data-ttu-id="3dcf7-234">Effets (FX) pour Direct3D 10,0 dans D3DX10 ⁵</span><span class="sxs-lookup"><span data-stu-id="3dcf7-234">Effects (FX) for Direct3D 10.0 in D3DX10⁵</span></span> |
| <span data-ttu-id="3dcf7-235">FX \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="3dcf7-235">fx\_4\_1</span></span> | <span data-ttu-id="3dcf7-236">Effets (FX) pour Direct3D 10,1 dans D3DX10 ⁵</span><span class="sxs-lookup"><span data-stu-id="3dcf7-236">Effects (FX) for Direct3D 10.1 in D3DX10⁵</span></span> |
| <span data-ttu-id="3dcf7-237">FX \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3dcf7-237">fx\_5\_0</span></span> | <span data-ttu-id="3dcf7-238">Effets (FX) pour Direct3D 11 ⁵</span><span class="sxs-lookup"><span data-stu-id="3dcf7-238">Effects (FX) for Direct3D 11⁵</span></span>             |



 

## <a name="notes"></a><span data-ttu-id="3dcf7-239">Notes</span><span class="sxs-lookup"><span data-stu-id="3dcf7-239">Notes</span></span>

<span data-ttu-id="3dcf7-240">Voici quelques remarques à propos desquelles les sections précédentes font référence :</span><span class="sxs-lookup"><span data-stu-id="3dcf7-240">Here are some notes that the preceding sections refer to:</span></span>

1.  <span data-ttu-id="3dcf7-241">les appareils de [niveau de fonctionnalité](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10,0 et 10,1 peuvent éventuellement prendre en charge DirectCompute.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-241">[feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10.0 and 10.1 devices can optionally support DirectCompute.</span></span> <span data-ttu-id="3dcf7-242">Pour vérifier la prise en charge, utilisez [**ID3D11Device :: CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) avec [**d3d11 \_ Feature \_ D3D10 \_ X \_ Hardware \_ options**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature).</span><span class="sxs-lookup"><span data-stu-id="3dcf7-242">To verify support, use [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) with [**D3D11\_FEATURE\_D3D10\_X\_HARDWARE\_OPTIONS**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature).</span></span>
2.  <span data-ttu-id="3dcf7-243">le [niveau de fonctionnalité](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9,3 requiert en fait un matériel conforme aux exigences du modèle de [nuanceur Direct3D 9 hérité 3,0](#legacy-direct3d-9-shader-model-30), mais ce niveau de fonctionnalité n’utilise pas les \_ cibles vs 3 \_ 0 ou PS \_ 3 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-243">[feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9.3 effectively requires hardware that complies with the requirements for [legacy Direct3D 9 shader model 3.0](#legacy-direct3d-9-shader-model-30), but this feature level does not make use of vs\_3\_0 or ps\_3\_0 targets.</span></span>
3.  <span data-ttu-id="3dcf7-244">Utilisez uniquement les modèles de nuanceur Direct3D 9 hérités avec l’API Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-244">Only use legacy Direct3D 9 shader models with the Direct3D 9 API.</span></span> <span data-ttu-id="3dcf7-245">Utilisez plutôt les profils 9. x avec les API Direct3D 10. x et 11. x.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-245">Instead, use the 9.x profiles with the Direct3D 10.x and 11.x API.</span></span>
4.  <span data-ttu-id="3dcf7-246">Les fonctions de **D3DCompile \*** de nuanceur HLSL actuelles ne prennent pas en charge les nuanceurs de pixels hérités 1. x.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-246">The current HLSL shader **D3DCompile\*** functions don't support legacy 1.x pixel shaders.</span></span> <span data-ttu-id="3dcf7-247">La dernière version du langage HLSL pour la prise en charge de ces cibles était D3DX9 dans la version d’octobre 2006 du kit de développement logiciel (SDK) DirectX.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-247">The last version of HLSL to support these targets was D3DX9 in the October 2006 release of the DirectX SDK.</span></span>
5.  <span data-ttu-id="3dcf7-248">Toutes les versions de D3DX et du SDK DirectX sont déconseillées.</span><span class="sxs-lookup"><span data-stu-id="3dcf7-248">All versions of D3DX and the DirectX SDK are deprecated.</span></span> <span data-ttu-id="3dcf7-249">Pour plus d’informations, consultez [où est le kit de développement logiciel (SDK) DirectX ?](/windows/desktop/directx-sdk--august-2009-).</span><span class="sxs-lookup"><span data-stu-id="3dcf7-249">For more info, see [Where is the DirectX SDK?](/windows/desktop/directx-sdk--august-2009-).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3dcf7-250">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3dcf7-250">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3dcf7-251">Guide de programmation pour HLSL</span><span class="sxs-lookup"><span data-stu-id="3dcf7-251">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 