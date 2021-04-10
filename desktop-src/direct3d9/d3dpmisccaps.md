---
description: Indicateurs des fonctionnalités primitives du pilote divers.
ms.assetid: 7912c682-c179-453b-8a34-e87958217500
title: D3DPMISCCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76af50a1e7f78f6441af9e985f55e42ee2298b46
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201076"
---
# <a name="d3dpmisccaps"></a><span data-ttu-id="2c8db-103">D3DPMISCCAPS</span><span class="sxs-lookup"><span data-stu-id="2c8db-103">D3DPMISCCAPS</span></span>

<span data-ttu-id="2c8db-104">Indicateurs des fonctionnalités primitives du pilote divers.</span><span class="sxs-lookup"><span data-stu-id="2c8db-104">Miscellaneous driver primitive capability flags.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2c8db-105">#définition</span><span class="sxs-lookup"><span data-stu-id="2c8db-105">#define</span></span></td>
<td><span data-ttu-id="2c8db-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c8db-106">Value</span></span></td>
<td><span data-ttu-id="2c8db-107">Description</span><span class="sxs-lookup"><span data-stu-id="2c8db-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c8db-108">D3DPMISCCAPS_MASKZ</span><span class="sxs-lookup"><span data-stu-id="2c8db-108">D3DPMISCCAPS_MASKZ</span></span></td>
<td><span data-ttu-id="2c8db-109">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="2c8db-109">0x00000002L</span></span></td>
<td><span data-ttu-id="2c8db-110">L’appareil peut activer et désactiver la modification de la mémoire tampon de profondeur sur les opérations de pixels.</span><span class="sxs-lookup"><span data-stu-id="2c8db-110">Device can enable and disable modification of the depth buffer on pixel operations.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c8db-111">D3DPMISCCAPS_CULLNONE</span><span class="sxs-lookup"><span data-stu-id="2c8db-111">D3DPMISCCAPS_CULLNONE</span></span></td>
<td><span data-ttu-id="2c8db-112">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="2c8db-112">0x00000010L</span></span></td>
<td><span data-ttu-id="2c8db-113">Le pilote n’effectue pas l’élimination des triangles.</span><span class="sxs-lookup"><span data-stu-id="2c8db-113">The driver does not perform triangle culling.</span></span> <span data-ttu-id="2c8db-114">Cela correspond au membre D3DCULL_NONE du type énuméré <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="2c8db-114">This corresponds to the D3DCULL_NONE member of the <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c8db-115">D3DPMISCCAPS_CULLCW</span><span class="sxs-lookup"><span data-stu-id="2c8db-115">D3DPMISCCAPS_CULLCW</span></span></td>
<td><span data-ttu-id="2c8db-116">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="2c8db-116">0x00000020L</span></span></td>
<td><span data-ttu-id="2c8db-117">Le pilote prend en charge le sens des aiguilles d’une montre à travers l’État D3DRS_CULLMODE.</span><span class="sxs-lookup"><span data-stu-id="2c8db-117">The driver supports clockwise triangle culling through the D3DRS_CULLMODE state.</span></span> <span data-ttu-id="2c8db-118">(Cela s’applique uniquement aux primitives de triangle.) Cet indicateur correspond au D3DCULL_CW membre du type énuméré <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="2c8db-118">(This applies only to triangle primitives.) This flag corresponds to the D3DCULL_CW member of the <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c8db-119">D3DPMISCCAPS_CULLCCW</span><span class="sxs-lookup"><span data-stu-id="2c8db-119">D3DPMISCCAPS_CULLCCW</span></span></td>
<td><span data-ttu-id="2c8db-120">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="2c8db-120">0x00000040L</span></span></td>
<td><span data-ttu-id="2c8db-121">Le pilote prend en charge l’élimination dans le sens inverse dans l’État D3DRS_CULLMODE.</span><span class="sxs-lookup"><span data-stu-id="2c8db-121">The driver supports counterclockwise culling through the D3DRS_CULLMODE state.</span></span> <span data-ttu-id="2c8db-122">(Cela s’applique uniquement aux primitives de triangle.) Cet indicateur correspond au D3DCULL_CCW membre du type énuméré <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="2c8db-122">(This applies only to triangle primitives.) This flag corresponds to the D3DCULL_CCW member of the <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c8db-123">D3DPMISCCAPS_COLORWRITEENABLE</span><span class="sxs-lookup"><span data-stu-id="2c8db-123">D3DPMISCCAPS_COLORWRITEENABLE</span></span></td>
<td><span data-ttu-id="2c8db-124">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="2c8db-124">0x00000100L</span></span></td>
<td><span data-ttu-id="2c8db-125">L’appareil prend en charge les écritures par canal pour la mémoire tampon de couleur de rendu-cible par le biais de l’État D3DRS_COLORWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="2c8db-125">Device supports per-channel writes for the render-target color buffer through the D3DRS_COLORWRITEENABLE state.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c8db-126">D3DPMISCCAPS_CLIPPLANESCALEDPOINTS</span><span class="sxs-lookup"><span data-stu-id="2c8db-126">D3DPMISCCAPS_CLIPPLANESCALEDPOINTS</span></span></td>
<td><span data-ttu-id="2c8db-127">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="2c8db-127">0x00000200L</span></span></td>
<td><span data-ttu-id="2c8db-128">L’appareil découpe correctement les points de la taille mis à l’échelle de plus de 1,0 en plans de découpage définis par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2c8db-128">Device correctly clips scaled points of size greater than 1.0 to user-defined clipping planes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c8db-129">D3DPMISCCAPS_CLIPTLVERTS</span><span class="sxs-lookup"><span data-stu-id="2c8db-129">D3DPMISCCAPS_CLIPTLVERTS</span></span></td>
<td><span data-ttu-id="2c8db-130">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="2c8db-130">0x00000200L</span></span></td>
<td><span data-ttu-id="2c8db-131">Éléments d’appareil primitives de vertex transformés.</span><span class="sxs-lookup"><span data-stu-id="2c8db-131">Device clips post-transformed vertex primitives.</span></span> <span data-ttu-id="2c8db-132">Spécifiez D3DUSAGE_DONOTCLIP lorsque le pipeline ne doit pas effectuer de découpage.</span><span class="sxs-lookup"><span data-stu-id="2c8db-132">Specify D3DUSAGE_DONOTCLIP when the pipeline should not do any clipping.</span></span> <span data-ttu-id="2c8db-133">Dans ce cas, il peut être nécessaire d’effectuer des découpages logiciels supplémentaires au moment du dessin, ce qui nécessite que la mémoire tampon du vertex soit dans la mémoire système.</span><span class="sxs-lookup"><span data-stu-id="2c8db-133">For this case, additional software clipping may need to be performed at draw time, requiring the vertex buffer to be in system memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c8db-134">D3DPMISCCAPS_TSSARGTEMP</span><span class="sxs-lookup"><span data-stu-id="2c8db-134">D3DPMISCCAPS_TSSARGTEMP</span></span></td>
<td><span data-ttu-id="2c8db-135">0x00000400L</span><span class="sxs-lookup"><span data-stu-id="2c8db-135">0x00000400L</span></span></td>
<td><span data-ttu-id="2c8db-136">L’appareil prend en charge <a href="d3dta.md">D3DTA</a> pour le registre temporaire.</span><span class="sxs-lookup"><span data-stu-id="2c8db-136">Device supports <a href="d3dta.md">D3DTA</a> for temporary register.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c8db-137">D3DPMISCCAPS_BLENDOP</span><span class="sxs-lookup"><span data-stu-id="2c8db-137">D3DPMISCCAPS_BLENDOP</span></span></td>
<td><span data-ttu-id="2c8db-138">0x00000800L</span><span class="sxs-lookup"><span data-stu-id="2c8db-138">0x00000800L</span></span></td>
<td><span data-ttu-id="2c8db-139">L’appareil prend en charge les opérations de fusion alpha autres que D3DBLENDOP_ADD.</span><span class="sxs-lookup"><span data-stu-id="2c8db-139">Device supports alpha-blending operations other than D3DBLENDOP_ADD.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c8db-140">D3DPMISCCAPS_NULLREFERENCE</span><span class="sxs-lookup"><span data-stu-id="2c8db-140">D3DPMISCCAPS_NULLREFERENCE</span></span></td>
<td><span data-ttu-id="2c8db-141">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="2c8db-141">0x00000100L</span></span></td>
<td><span data-ttu-id="2c8db-142">Appareil de référence qui n’est pas rendu.</span><span class="sxs-lookup"><span data-stu-id="2c8db-142">A reference device that does not render.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c8db-143">D3DPMISCCAPS_INDEPENDENTWRITEMASKS</span><span class="sxs-lookup"><span data-stu-id="2c8db-143">D3DPMISCCAPS_INDEPENDENTWRITEMASKS</span></span></td>
<td><span data-ttu-id="2c8db-144">0x00004000L</span><span class="sxs-lookup"><span data-stu-id="2c8db-144">0x00004000L</span></span></td>
<td><span data-ttu-id="2c8db-145">L’appareil prend en charge des masques d’écriture indépendants pour plusieurs textures d’élément ou plusieurs cibles de rendu.</span><span class="sxs-lookup"><span data-stu-id="2c8db-145">Device supports independent write masks for multiple element textures or multiple render targets.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c8db-146">D3DPMISCCAPS_PERSTAGECONSTANT</span><span class="sxs-lookup"><span data-stu-id="2c8db-146">D3DPMISCCAPS_PERSTAGECONSTANT</span></span></td>
<td><span data-ttu-id="2c8db-147">0x00008000L</span><span class="sxs-lookup"><span data-stu-id="2c8db-147">0x00008000L</span></span></td>
<td><span data-ttu-id="2c8db-148">L’appareil prend en charge les constantes par étape.</span><span class="sxs-lookup"><span data-stu-id="2c8db-148">Device supports per-stage constants.</span></span> <span data-ttu-id="2c8db-149">Consultez D3DTSS_CONSTANT dans <a href="/windows/desktop/direct3d9/d3dtexturestagestatetype"><strong>D3DTEXTURESTAGESTATETYPE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2c8db-149">See D3DTSS_CONSTANT in <a href="/windows/desktop/direct3d9/d3dtexturestagestatetype"><strong>D3DTEXTURESTAGESTATETYPE</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c8db-150">D3DPMISCCAPS_POSTBLENDSRGBCONVERT</span><span class="sxs-lookup"><span data-stu-id="2c8db-150">D3DPMISCCAPS_POSTBLENDSRGBCONVERT</span></span></td>
<td><span data-ttu-id="2c8db-151">0x00200000L</span><span class="sxs-lookup"><span data-stu-id="2c8db-151">0x00200000L</span></span></td>
<td><span data-ttu-id="2c8db-152">L’appareil prend en charge la conversion en sRVB après la fusion.</span><span class="sxs-lookup"><span data-stu-id="2c8db-152">Device supports conversion to sRGB after blending.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2c8db-153">Différences entre Direct3D 9 et Direct3D 9Ex :</span><span class="sxs-lookup"><span data-stu-id="2c8db-153">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="2c8db-154">Cet indicateur est disponible uniquement dans Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="2c8db-154">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c8db-155">D3DPMISCCAPS_FOGANDSPECULARALPHA</span><span class="sxs-lookup"><span data-stu-id="2c8db-155">D3DPMISCCAPS_FOGANDSPECULARALPHA</span></span></td>
<td><span data-ttu-id="2c8db-156">0x00010000L</span><span class="sxs-lookup"><span data-stu-id="2c8db-156">0x00010000L</span></span></td>
<td><span data-ttu-id="2c8db-157">L’appareil prend en charge le brouillard distinct et l’alpha spéculaire.</span><span class="sxs-lookup"><span data-stu-id="2c8db-157">Device supports separate fog and specular alpha.</span></span> <span data-ttu-id="2c8db-158">De nombreux appareils utilisent le canal alpha spéculaire pour stocker le facteur de brouillard.</span><span class="sxs-lookup"><span data-stu-id="2c8db-158">Many devices use the specular alpha channel to store the fog factor.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c8db-159">D3DPMISCCAPS_SEPARATEALPHABLEND</span><span class="sxs-lookup"><span data-stu-id="2c8db-159">D3DPMISCCAPS_SEPARATEALPHABLEND</span></span></td>
<td><span data-ttu-id="2c8db-160">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="2c8db-160">0x00020000L</span></span></td>
<td><span data-ttu-id="2c8db-161">L’appareil prend en charge des paramètres de fusion distincts pour le canal alpha.</span><span class="sxs-lookup"><span data-stu-id="2c8db-161">Device supports separate blend settings for the alpha channel.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c8db-162">D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS</span><span class="sxs-lookup"><span data-stu-id="2c8db-162">D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS</span></span></td>
<td><span data-ttu-id="2c8db-163">0x00040000L</span><span class="sxs-lookup"><span data-stu-id="2c8db-163">0x00040000L</span></span></td>
<td><span data-ttu-id="2c8db-164">L’appareil prend en charge des profondeurs différentes pour plusieurs cibles de rendu.</span><span class="sxs-lookup"><span data-stu-id="2c8db-164">Device supports different bit depths for multiple render targets.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c8db-165">D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING</span><span class="sxs-lookup"><span data-stu-id="2c8db-165">D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING</span></span></td>
<td><span data-ttu-id="2c8db-166">0x00080000L</span><span class="sxs-lookup"><span data-stu-id="2c8db-166">0x00080000L</span></span></td>
<td><span data-ttu-id="2c8db-167">L’appareil prend en charge les opérations de nuanceur de pixel après plusieurs cibles de rendu.</span><span class="sxs-lookup"><span data-stu-id="2c8db-167">Device supports post-pixel shader operations for multiple render targets.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c8db-168">D3DPMISCCAPS_FOGVERTEXCLAMPED</span><span class="sxs-lookup"><span data-stu-id="2c8db-168">D3DPMISCCAPS_FOGVERTEXCLAMPED</span></span></td>
<td><span data-ttu-id="2c8db-169">0x00100000L</span><span class="sxs-lookup"><span data-stu-id="2c8db-169">0x00100000L</span></span></td>
<td><span data-ttu-id="2c8db-170">Pinces de l’appareil : facteur de mélange de brouillard par vertex.</span><span class="sxs-lookup"><span data-stu-id="2c8db-170">Device clamps fog blend factor per vertex.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2c8db-171">Ces constantes sont utilisées par le membre PrimitiveMiscCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="2c8db-171">These constants are used by the PrimitiveMiscCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="2c8db-172">Informations constantes</span><span class="sxs-lookup"><span data-stu-id="2c8db-172">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="2c8db-173">En-tête</span><span class="sxs-lookup"><span data-stu-id="2c8db-173">Header</span></span>                   | <span data-ttu-id="2c8db-174">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="2c8db-174">d3d9caps.h</span></span> |
| <span data-ttu-id="2c8db-175">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="2c8db-175">Minimum operating system</span></span> | <span data-ttu-id="2c8db-176">Windows 98</span><span class="sxs-lookup"><span data-stu-id="2c8db-176">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="2c8db-177">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2c8db-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c8db-178">Constantes Direct3D</span><span class="sxs-lookup"><span data-stu-id="2c8db-178">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
