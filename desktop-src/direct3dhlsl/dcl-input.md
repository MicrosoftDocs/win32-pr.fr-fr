---
title: dcl_input (SM4-ASM)
description: '\_entrée DCL (SM4-ASM)'
ms.assetid: 13456f2a-ee6c-42da-a9fe-670ab0fcbddf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 400a1d47b6e0f9d82ec662553c36629deb4b1f0b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990837"
---
# <a name="dcl_input-sm4---asm"></a><span data-ttu-id="f505c-103">\_entrée DCL (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="f505c-103">dcl\_input (sm4 - asm)</span></span>

<span data-ttu-id="f505c-104">Déclare un registre d’entrée de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="f505c-104">Declares a shader-input register.</span></span>



| <span data-ttu-id="f505c-105">\_entrée DCL v *N \[ . Mask \] \[ , interpolationMode \]*</span><span class="sxs-lookup"><span data-stu-id="f505c-105">dcl\_input v *N\[.mask\]\[, interpolationMode\]*</span></span> |
|-------------------------------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f505c-106">Élément</span><span class="sxs-lookup"><span data-stu-id="f505c-106">Item</span></span></th>
<th><span data-ttu-id="f505c-107">Description</span><span class="sxs-lookup"><span data-stu-id="f505c-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f505c-108"><span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N [. masque]</em></span><span class="sxs-lookup"><span data-stu-id="f505c-108"><span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N[.mask]</em></span></span><br/></td>
<td><span data-ttu-id="f505c-109">dans Registre de données de vertex.</span><span class="sxs-lookup"><span data-stu-id="f505c-109">[in] A vertex data register.</span></span> <br/>
<ul>
<li><span data-ttu-id="f505c-110"><em>N</em> est un entier qui identifie le numéro du Registre.</span><span class="sxs-lookup"><span data-stu-id="f505c-110"><em>N</em> is an integer that identifies the register number.</span></span></li>
<li><span data-ttu-id="f505c-111"><em>[. Mask]</em> est un masque de composant facultatif (. XYZW) qui spécifie les composants Register à utiliser.</span><span class="sxs-lookup"><span data-stu-id="f505c-111"><em>[.mask]</em> is an optional component mask (.xyzw) that specifies which of the register components to use.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f505c-112"><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolationMode</em></span><span class="sxs-lookup"><span data-stu-id="f505c-112"><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolationMode</em></span></span><br/></td>
<td><span data-ttu-id="f505c-113">[in] Facultatif.</span><span class="sxs-lookup"><span data-stu-id="f505c-113">[in] Optional.</span></span> <span data-ttu-id="f505c-114">Mode d’interpolation, qui est respecté uniquement sur les registres d’entrée de nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="f505c-114">The interpolation mode, which is only honored on pixel shader input registers.</span></span> <span data-ttu-id="f505c-115">Ce peut être l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="f505c-115">It can be one of the following values:</span></span> <br/>
<ul>
<li><span data-ttu-id="f505c-116">constant : n’effectue pas d’interpolation entre les valeurs de registre.</span><span class="sxs-lookup"><span data-stu-id="f505c-116">constant - do not interpolate between register values.</span></span></li>
<li><span data-ttu-id="f505c-117">linéaire-interpolation linéaire entre les valeurs de registre.</span><span class="sxs-lookup"><span data-stu-id="f505c-117">linear - interpolate linearly between register values.</span></span></li>
<li><span data-ttu-id="f505c-118">linearCentroid-identique à Linear, mais au centre de gravité de l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="f505c-118">linearCentroid - same as linear but centroid clamped when multisampling.</span></span></li>
<li><span data-ttu-id="f505c-119">linearNoperspective : identique à linéaire, mais sans correction de perspective.</span><span class="sxs-lookup"><span data-stu-id="f505c-119">linearNoperspective - same as linear but with no perspective correction.</span></span></li>
<li><span data-ttu-id="f505c-120">linearNoperspectiveCentroid-identique à Linear, centre de gravité de l’échantillonnage, sans correction de perspective.</span><span class="sxs-lookup"><span data-stu-id="f505c-120">linearNoperspectiveCentroid - same as linear, centroid clamped when multisampling, no perspective correction.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="interpolation-notes"></a><span data-ttu-id="f505c-121">Remarques sur l’interpolation</span><span class="sxs-lookup"><span data-stu-id="f505c-121">Interpolation Notes</span></span>

<span data-ttu-id="f505c-122">Par défaut, les attributs de vertex sont interpolés à partir d’un centre de pixels lors de l’exécution de l’anticrénelage multiéchantillonne.</span><span class="sxs-lookup"><span data-stu-id="f505c-122">By default, vertex attributes are interpolated from a pixel center when performing multisample antialiasing.</span></span> <span data-ttu-id="f505c-123">Si un centre de pixels n’est pas couvert, un attribut est extrapolé à un centre de pixels avant l’interpolation.</span><span class="sxs-lookup"><span data-stu-id="f505c-123">If a pixel center is not covered, an attribute is extrapolated to a pixel center before interpolation.</span></span>

<span data-ttu-id="f505c-124">Pour un pixel qui n’est pas entièrement couvert ou un attribut qui ne couvre pas un centre de pixels, vous pouvez spécifier un échantillonnage de centre de gravité qui force l’échantillonnage à quelque endroit que ce soit dans la zone couverte du pixel.</span><span class="sxs-lookup"><span data-stu-id="f505c-124">For a pixel that is not fully covered or an attribute that does not cover a pixel center, you can specify centroid sampling which forces sampling to occur somewhere within the covered area of the pixel.</span></span> <span data-ttu-id="f505c-125">Étant donné qu’un exemple de masque (s’il est utilisé) est appliqué avant le calcul du centre de gravité, tout emplacement d’échantillonnage masqué par l’exemple de masque ne peut pas être choisi comme emplacement de centre de gravité.</span><span class="sxs-lookup"><span data-stu-id="f505c-125">Because a sample mask (if used) is applied before the centroid is computed, any sample location masked out by the sample mask cannot be chosen as a centroid location.</span></span>

<span data-ttu-id="f505c-126">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="f505c-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f505c-127">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="f505c-127">Vertex Shader</span></span> | <span data-ttu-id="f505c-128">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="f505c-128">Geometry Shader</span></span> | <span data-ttu-id="f505c-129">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="f505c-129">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="f505c-130">x</span><span class="sxs-lookup"><span data-stu-id="f505c-130">x</span></span>             | <span data-ttu-id="f505c-131">x</span><span class="sxs-lookup"><span data-stu-id="f505c-131">x</span></span>               | <span data-ttu-id="f505c-132">x</span><span class="sxs-lookup"><span data-stu-id="f505c-132">x</span></span>            |



 

<span data-ttu-id="f505c-133">Pour identifier l’entrée en tant que valeur système, utilisez l' [ \_ entrée DCL \_ (SM4-ASM)](dcl-input-sv.md).</span><span class="sxs-lookup"><span data-stu-id="f505c-133">To identify the input as a system value, use [dcl\_input\_sv (sm4 - asm)](dcl-input-sv.md).</span></span>

<span data-ttu-id="f505c-134">Cette instruction est incluse pour faciliter le débogage d’un nuanceur dans l’assembly. vous ne pouvez pas créer de nuanceur dans un langage assembleur à l’aide du nuanceur modèle 4.</span><span class="sxs-lookup"><span data-stu-id="f505c-134">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="f505c-135">Exemple</span><span class="sxs-lookup"><span data-stu-id="f505c-135">Example</span></span>

<span data-ttu-id="f505c-136">Voici quelques exemples.</span><span class="sxs-lookup"><span data-stu-id="f505c-136">Here are some examples.</span></span>


```
dcl_input v3.xyz

dcl_input v0.x, linearCentroid
```



## <a name="minimum-shader-model"></a><span data-ttu-id="f505c-137">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="f505c-137">Minimum Shader Model</span></span>

<span data-ttu-id="f505c-138">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="f505c-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f505c-139">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="f505c-139">Shader Model</span></span>                                              | <span data-ttu-id="f505c-140">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="f505c-140">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f505c-141">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="f505c-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f505c-142">Oui</span><span class="sxs-lookup"><span data-stu-id="f505c-142">yes</span></span>       |
| [<span data-ttu-id="f505c-143">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="f505c-143">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f505c-144">Oui</span><span class="sxs-lookup"><span data-stu-id="f505c-144">yes</span></span>       |
| [<span data-ttu-id="f505c-145">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="f505c-145">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f505c-146">Oui</span><span class="sxs-lookup"><span data-stu-id="f505c-146">yes</span></span>       |
| [<span data-ttu-id="f505c-147">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f505c-147">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f505c-148">non</span><span class="sxs-lookup"><span data-stu-id="f505c-148">no</span></span>        |
| [<span data-ttu-id="f505c-149">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f505c-149">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f505c-150">non</span><span class="sxs-lookup"><span data-stu-id="f505c-150">no</span></span>        |
| [<span data-ttu-id="f505c-151">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f505c-151">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f505c-152">non</span><span class="sxs-lookup"><span data-stu-id="f505c-152">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f505c-153">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f505c-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f505c-154">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f505c-154">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





