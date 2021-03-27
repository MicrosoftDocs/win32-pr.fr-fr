---
title: dcl_input_sv (SM4-ASM)
description: '\_SV entrée DCL \_ (SM4-ASM)'
ms.assetid: 59270148-e2eb-4525-a888-ad7e843d62a5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 650196dff224259f48d1471f3005f95ec0de9c8b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679190"
---
# <a name="dcl_input_sv-sm4---asm"></a><span data-ttu-id="b7473-103">\_SV entrée DCL \_ (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="b7473-103">dcl\_input\_sv (sm4 - asm)</span></span>

<span data-ttu-id="b7473-104">Déclare un registre d’entrée de nuanceur qui attend qu’une [valeur système](dx-graphics-hlsl-semantics.md) soit fournie à partir d’une étape précédente.</span><span class="sxs-lookup"><span data-stu-id="b7473-104">Declares a shader-input register that expects a [system-value](dx-graphics-hlsl-semantics.md) to be provided from a preceding stage.</span></span>



| <span data-ttu-id="b7473-105">\_entrée DCL \_ SV v *N \[ . Mask \]*, *systemValueName \[ , interpolationMode \]*</span><span class="sxs-lookup"><span data-stu-id="b7473-105">dcl\_input\_sv v *N\[.mask\]*, *systemValueName\[, interpolationMode\]*</span></span> |
|------------------------------------------------------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b7473-106">Élément</span><span class="sxs-lookup"><span data-stu-id="b7473-106">Item</span></span></th>
<th><span data-ttu-id="b7473-107">Description</span><span class="sxs-lookup"><span data-stu-id="b7473-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b7473-108"><span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N [. masque]</em></span><span class="sxs-lookup"><span data-stu-id="b7473-108"><span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N[.mask]</em></span></span><br/></td>
<td><span data-ttu-id="b7473-109">dans Registre de données de vertex.</span><span class="sxs-lookup"><span data-stu-id="b7473-109">[in] A vertex data register.</span></span> <br/>
<ul>
<li><span data-ttu-id="b7473-110"><em>N</em> est un entier qui identifie le numéro du Registre.</span><span class="sxs-lookup"><span data-stu-id="b7473-110"><em>N</em> is an integer that identifies the register number.</span></span></li>
<li><span data-ttu-id="b7473-111"><em>[. Mask]</em> est un masque de composant facultatif (. XYZW) qui spécifie les composants Register à utiliser.</span><span class="sxs-lookup"><span data-stu-id="b7473-111"><em>[.mask]</em> is an optional component mask (.xyzw) that specifies which of the register components to use.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7473-112"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span><em>systemValueName</em></span><span class="sxs-lookup"><span data-stu-id="b7473-112"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span><em>systemValueName</em></span></span><br/></td>
<td><span data-ttu-id="b7473-113">dans Nom de la valeur système qui est une chaîne (voir <a href="dx-graphics-hlsl-semantics.md">sémantique de valeur système</a>) sans &quot; &quot; préfixe SV_.</span><span class="sxs-lookup"><span data-stu-id="b7473-113">[in] The system-value name which is a string (see <a href="dx-graphics-hlsl-semantics.md">system-value semantics</a>) without the &quot;SV_&quot; prefix.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7473-114"><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolationMode</em></span><span class="sxs-lookup"><span data-stu-id="b7473-114"><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolationMode</em></span></span><br/></td>
<td><span data-ttu-id="b7473-115">[in] Facultatif.</span><span class="sxs-lookup"><span data-stu-id="b7473-115">[in] Optional.</span></span> <span data-ttu-id="b7473-116">Mode d’interpolation qui affecte la façon dont les valeurs sont calculées lors de la pixellisation. le mode est utilisé uniquement par un nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="b7473-116">The interpolation mode which affects how values are calculated during rasterization; the mode is only used by a pixel shader.</span></span> <span data-ttu-id="b7473-117">Ce peut être l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="b7473-117">It can be one of the following values:</span></span> <br/>
<ul>
<li><span data-ttu-id="b7473-118">constant : n’effectue pas d’interpolation entre les valeurs de registre.</span><span class="sxs-lookup"><span data-stu-id="b7473-118">constant - do not interpolate between register values.</span></span></li>
<li><span data-ttu-id="b7473-119">linéaire-interpolation linéaire entre les valeurs de registre.</span><span class="sxs-lookup"><span data-stu-id="b7473-119">linear - interpolate linearly between register values.</span></span></li>
<li><span data-ttu-id="b7473-120">linearCentroid-identique à Linear, mais au centre de gravité de l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="b7473-120">linearCentroid - same as linear but centroid clamped when multisampling.</span></span></li>
<li><span data-ttu-id="b7473-121">linearNoperspective : identique à linéaire, mais sans correction de perspective.</span><span class="sxs-lookup"><span data-stu-id="b7473-121">linearNoperspective - same as linear but with no perspective correction.</span></span></li>
<li><span data-ttu-id="b7473-122">linearNoperspectiveCentroid-identique à Linear, mais sans correction de perspective et de centre de gravité lors de l’échantillonnage multiple.</span><span class="sxs-lookup"><span data-stu-id="b7473-122">linearNoperspectiveCentroid - same as linear but with no perspective correction and centroid clamped when multisampling.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="b7473-123">Un masque de composant pour une déclaration de valeur système peut être n’importe quel sous-ensemble approprié de \[ XYZW \] ; les déclarations peuvent ne pas se chevaucher (chaque déclaration doit suivre la séquence XYZW).</span><span class="sxs-lookup"><span data-stu-id="b7473-123">A component mask for a system-value declaration can be any appropriate subset of \[xyzw\]; declarations may not overlap (each declaration must follow the sequence xyzw).</span></span> <span data-ttu-id="b7473-124">Lorsque vous déclarez des valeurs de système scalaires (distance de découpage et distance de Culling par exemple), vous pouvez déclarer plusieurs valeurs système dans un seul registre.</span><span class="sxs-lookup"><span data-stu-id="b7473-124">When declaring scalar system values (clip distance and cull distance for example), you can declare multiple system values in a single register.</span></span> <span data-ttu-id="b7473-125">Dans ce cas, assurez-vous que les autres modificateurs comme les modes d’interpolation correspondent.</span><span class="sxs-lookup"><span data-stu-id="b7473-125">If you do so, make sure other modifiers like the interpolation modes match.</span></span>

<span data-ttu-id="b7473-126">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="b7473-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b7473-127">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="b7473-127">Vertex Shader</span></span> | <span data-ttu-id="b7473-128">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="b7473-128">Geometry Shader</span></span> | <span data-ttu-id="b7473-129">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="b7473-129">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="b7473-130">x</span><span class="sxs-lookup"><span data-stu-id="b7473-130">x</span></span>             | <span data-ttu-id="b7473-131">x</span><span class="sxs-lookup"><span data-stu-id="b7473-131">x</span></span>               | <span data-ttu-id="b7473-132">x</span><span class="sxs-lookup"><span data-stu-id="b7473-132">x</span></span>            |



 

<span data-ttu-id="b7473-133">Cette instruction est incluse pour faciliter le débogage d’un nuanceur dans l’assembly. vous ne pouvez pas créer de nuanceur dans un langage assembleur à l’aide du nuanceur modèle 4.</span><span class="sxs-lookup"><span data-stu-id="b7473-133">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="b7473-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="b7473-134">Example</span></span>

<span data-ttu-id="b7473-135">Voici quelques exemples :</span><span class="sxs-lookup"><span data-stu-id="b7473-135">Here are some examples:</span></span>


```
// valid
dcl_input v0.y, linear
dcl_input_sv v0.w, clipDistance
dcl_input_sv v0.z, cullDistance
```




```
// invalid declarations
dcl_input v0.y, linear
dcl_input_sv v0.x, clipDistance  // the y component was previously declared, this declaration must use 
                                 // either the z or w component

dcl_input v0.y, linearNoPerspective                  // the interpolation mode is linear-no-perspective
dcl_input_sv v0.z, renderTargetArrayIndex, constant  // the interpolation modes is constant
                                                     // the interpolation modes must match
```



## <a name="minimum-shader-model"></a><span data-ttu-id="b7473-136">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="b7473-136">Minimum Shader Model</span></span>

<span data-ttu-id="b7473-137">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="b7473-137">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b7473-138">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="b7473-138">Shader Model</span></span>                                              | <span data-ttu-id="b7473-139">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="b7473-139">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b7473-140">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="b7473-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b7473-141">Oui</span><span class="sxs-lookup"><span data-stu-id="b7473-141">yes</span></span>       |
| [<span data-ttu-id="b7473-142">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="b7473-142">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b7473-143">Oui</span><span class="sxs-lookup"><span data-stu-id="b7473-143">yes</span></span>       |
| [<span data-ttu-id="b7473-144">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="b7473-144">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b7473-145">Oui</span><span class="sxs-lookup"><span data-stu-id="b7473-145">yes</span></span>       |
| [<span data-ttu-id="b7473-146">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b7473-146">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b7473-147">non</span><span class="sxs-lookup"><span data-stu-id="b7473-147">no</span></span>        |
| [<span data-ttu-id="b7473-148">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b7473-148">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b7473-149">non</span><span class="sxs-lookup"><span data-stu-id="b7473-149">no</span></span>        |
| [<span data-ttu-id="b7473-150">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b7473-150">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b7473-151">non</span><span class="sxs-lookup"><span data-stu-id="b7473-151">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b7473-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b7473-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7473-153">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b7473-153">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





