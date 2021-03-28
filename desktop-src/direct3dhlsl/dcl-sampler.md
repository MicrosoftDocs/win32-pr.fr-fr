---
title: dcl_sampler (SM4-ASM)
description: '\_exemple de DCL (SM4-ASM)'
ms.assetid: 285a47fa-2d47-4ba9-90b9-3f4c61d5dce1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 45b6da3bcdb027a00edeb4f009773533424efeb8
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104383060"
---
# <a name="dcl_sampler-sm4---asm"></a><span data-ttu-id="659c9-103">\_exemple de DCL (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="659c9-103">dcl\_sampler (sm4 - asm)</span></span>

<span data-ttu-id="659c9-104">Déclare un registre d’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="659c9-104">Declares a sampler register.</span></span>



| <span data-ttu-id="659c9-105">DCL \_ sampler SN, mode</span><span class="sxs-lookup"><span data-stu-id="659c9-105">dcl\_sampler sN, mode</span></span> |
|-----------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="659c9-106">Élément</span><span class="sxs-lookup"><span data-stu-id="659c9-106">Item</span></span></th>
<th><span data-ttu-id="659c9-107">Description</span><span class="sxs-lookup"><span data-stu-id="659c9-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="659c9-108"><span id="sN"></span><span id="sn"></span><span id="SN"></span>s<em>N</em></span><span class="sxs-lookup"><span data-stu-id="659c9-108"><span id="sN"></span><span id="sn"></span><span id="SN"></span>s<em>N</em></span></span><br/></td>
<td><span data-ttu-id="659c9-109">dans Un registre d’échantillonnage, où <em>N</em> est un entier qui désigne le numéro du Registre.</span><span class="sxs-lookup"><span data-stu-id="659c9-109">[in] A sampler register, where <em>N</em> is an integer that denotes the register number.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="659c9-110"><span id="mode"></span><span id="MODE"></span><em>mode</em></span><span class="sxs-lookup"><span data-stu-id="659c9-110"><span id="mode"></span><span id="MODE"></span><em>mode</em></span></span><br/></td>
<td><span data-ttu-id="659c9-111">dans Mode échantillonneur qui limite les États de l’échantillonneur (répertoriés dans les membres de <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_sampler_desc"><strong>D3D10_SAMPLER_DESC</strong></a>) qui sont honorés.</span><span class="sxs-lookup"><span data-stu-id="659c9-111">[in] A sampler mode, which constrains which sampler states (listed in the members of <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_sampler_desc"><strong>D3D10_SAMPLER_DESC</strong></a>) are honored.</span></span> <span data-ttu-id="659c9-112">Les modes et les États sont répertoriés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="659c9-112">The modes and states are listed in the following table.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="659c9-113">Mode</span><span class="sxs-lookup"><span data-stu-id="659c9-113">Mode</span></span></th>
<th><span data-ttu-id="659c9-114">États de l’échantillonneur honorés</span><span class="sxs-lookup"><span data-stu-id="659c9-114">Sampler States Honored</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="659c9-115">default</span><span class="sxs-lookup"><span data-stu-id="659c9-115">default</span></span></td>
<td><span data-ttu-id="659c9-116"><em>Filtre</em> (peut ne pas utiliser les valeurs _COMPARISON ou _TEXT), adsent <em>/V/W</em>, <em>MinLOD/MaxLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em>, <em>BorderColor [4]</em></span><span class="sxs-lookup"><span data-stu-id="659c9-116"><em>Filter</em> (may not use the _COMPARISON or _TEXT values), <em>AddressU/V/W</em>, <em>MinLOD/MaxLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em>, <em>BorderColor[4]</em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="659c9-117">comparaison</span><span class="sxs-lookup"><span data-stu-id="659c9-117">comparison</span></span></td>
<td><span data-ttu-id="659c9-118"><em>Filter</em>, <em>ComparisonFunction</em>, adverse <em>/V/W</em>, <em>MinLOD, MaxLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em>, <em>BorderColor [4]</em></span><span class="sxs-lookup"><span data-stu-id="659c9-118"><em>Filter</em>, <em>ComparisonFunction</em>, <em>AddressU/V/W</em>, <em>MinLOD,MaxLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em>, <em>BorderColor[4]</em></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="659c9-119">carbur</span><span class="sxs-lookup"><span data-stu-id="659c9-119">mono</span></span></td>
<td><span data-ttu-id="659c9-120"><em>Filter</em> (doit être l’une des valeurs _TEXT), <em>MonoFilterWidth</em>, <em>MonoFilterHeight</em> (ces deux États sont l’état global du périphérique), <em>MinLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em></span><span class="sxs-lookup"><span data-stu-id="659c9-120"><em>Filter</em> (must be one of the _TEXT values), <em>MonoFilterWidth</em>, <em>MonoFilterHeight</em> (these two states are global device state), <em>MinLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em></span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="659c9-121">Le mode limite les exemples d’instructions qui peuvent être utilisés. ce tableau répertorie les méthodes d’objet de texture prises en charge pour chaque mode.</span><span class="sxs-lookup"><span data-stu-id="659c9-121">The mode restricts the sample instructions that can be used; this table lists the texture-object methods that are supported for each mode.</span></span>



| <span data-ttu-id="659c9-122">Un échantillonneur fonctionnant dans ce mode</span><span class="sxs-lookup"><span data-stu-id="659c9-122">A Sampler Operating in this Mode</span></span> | <span data-ttu-id="659c9-123">Peut utiliser ces méthodes Texture-Object</span><span class="sxs-lookup"><span data-stu-id="659c9-123">Can Use these Texture-Object Methods</span></span>                                                                                                           |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="659c9-124">default</span><span class="sxs-lookup"><span data-stu-id="659c9-124">default</span></span>                          | <span data-ttu-id="659c9-125">[Exemple](dx-graphics-hlsl-to-sample.md), [SampleLevel](dx-graphics-hlsl-to-samplelevel.md), [SampleGrad](dx-graphics-hlsl-to-samplegrad.md)</span><span class="sxs-lookup"><span data-stu-id="659c9-125">[Sample](dx-graphics-hlsl-to-sample.md), [SampleLevel](dx-graphics-hlsl-to-samplelevel.md), [SampleGrad](dx-graphics-hlsl-to-samplegrad.md)</span></span> |
| <span data-ttu-id="659c9-126">comparaison</span><span class="sxs-lookup"><span data-stu-id="659c9-126">comparison</span></span>                       | <span data-ttu-id="659c9-127">[SampleCmp](dx-graphics-hlsl-to-samplecmp.md), [SampleCmpLevelZero](dx-graphics-hlsl-to-samplecmplevelzero.md)</span><span class="sxs-lookup"><span data-stu-id="659c9-127">[SampleCmp](dx-graphics-hlsl-to-samplecmp.md), [SampleCmpLevelZero](dx-graphics-hlsl-to-samplecmplevelzero.md)</span></span>                               |
| <span data-ttu-id="659c9-128">carbur</span><span class="sxs-lookup"><span data-stu-id="659c9-128">mono</span></span>                             | [<span data-ttu-id="659c9-129">SampleLevel</span><span class="sxs-lookup"><span data-stu-id="659c9-129">SampleLevel</span></span>](dx-graphics-hlsl-to-samplelevel.md)                                                                                             |



 

<span data-ttu-id="659c9-130">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="659c9-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="659c9-131">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="659c9-131">Vertex Shader</span></span> | <span data-ttu-id="659c9-132">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="659c9-132">Geometry Shader</span></span> | <span data-ttu-id="659c9-133">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="659c9-133">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="659c9-134">x</span><span class="sxs-lookup"><span data-stu-id="659c9-134">x</span></span>             | <span data-ttu-id="659c9-135">x</span><span class="sxs-lookup"><span data-stu-id="659c9-135">x</span></span>               | <span data-ttu-id="659c9-136">x\*</span><span class="sxs-lookup"><span data-stu-id="659c9-136">x\*</span></span>          |



 

<span data-ttu-id="659c9-137">\* -L’utilisation d’un échantillonneur en mode mono est prise en charge uniquement dans un nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="659c9-137">\* - Using a sampler in mono mode is supported only in a pixel shader.</span></span>

<span data-ttu-id="659c9-138">Cette instruction est incluse pour faciliter le débogage d’un nuanceur dans l’assembly. vous ne pouvez pas créer de nuanceur dans un langage assembleur à l’aide du nuanceur modèle 4.</span><span class="sxs-lookup"><span data-stu-id="659c9-138">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="659c9-139">Exemple</span><span class="sxs-lookup"><span data-stu-id="659c9-139">Example</span></span>

<span data-ttu-id="659c9-140">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="659c9-140">Here is an example.</span></span>


```
dcl_sampler s3, default
```



## <a name="minimum-shader-model"></a><span data-ttu-id="659c9-141">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="659c9-141">Minimum Shader Model</span></span>

<span data-ttu-id="659c9-142">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="659c9-142">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="659c9-143">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="659c9-143">Shader Model</span></span>                                              | <span data-ttu-id="659c9-144">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="659c9-144">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="659c9-145">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="659c9-145">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="659c9-146">Oui</span><span class="sxs-lookup"><span data-stu-id="659c9-146">yes</span></span>       |
| [<span data-ttu-id="659c9-147">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="659c9-147">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="659c9-148">Oui</span><span class="sxs-lookup"><span data-stu-id="659c9-148">yes</span></span>       |
| [<span data-ttu-id="659c9-149">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="659c9-149">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="659c9-150">Oui</span><span class="sxs-lookup"><span data-stu-id="659c9-150">yes</span></span>       |
| [<span data-ttu-id="659c9-151">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="659c9-151">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="659c9-152">non</span><span class="sxs-lookup"><span data-stu-id="659c9-152">no</span></span>        |
| [<span data-ttu-id="659c9-153">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="659c9-153">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="659c9-154">non</span><span class="sxs-lookup"><span data-stu-id="659c9-154">no</span></span>        |
| [<span data-ttu-id="659c9-155">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="659c9-155">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="659c9-156">non</span><span class="sxs-lookup"><span data-stu-id="659c9-156">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="659c9-157">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="659c9-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="659c9-158">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="659c9-158">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

