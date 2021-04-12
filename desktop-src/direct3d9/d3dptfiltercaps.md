---
description: Constantes de filtrage de texture.
ms.assetid: 4434e456-670e-46a9-ba78-affdc195fe1c
title: D3DPTFILTERCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c122b1260d568a43c69c336059e26a6ecfde2a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033772"
---
# <a name="d3dptfiltercaps"></a><span data-ttu-id="09f7f-103">D3DPTFILTERCAPS</span><span class="sxs-lookup"><span data-stu-id="09f7f-103">D3DPTFILTERCAPS</span></span>

<span data-ttu-id="09f7f-104">Constantes de filtrage de texture.</span><span class="sxs-lookup"><span data-stu-id="09f7f-104">Texture filtering constants.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="09f7f-105">#définition</span><span class="sxs-lookup"><span data-stu-id="09f7f-105">#define</span></span></td>
<td><span data-ttu-id="09f7f-106">Description</span><span class="sxs-lookup"><span data-stu-id="09f7f-106">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09f7f-107">D3DPTFILTERCAPS_CONVOLUTIONMONO</span><span class="sxs-lookup"><span data-stu-id="09f7f-107">D3DPTFILTERCAPS_CONVOLUTIONMONO</span></span></td>
<td><span data-ttu-id="09f7f-108">L’appareil prend en charge le filtrage de convolution monochrome.</span><span class="sxs-lookup"><span data-stu-id="09f7f-108">Device supports monochrome convolution filtering.</span></span> <span data-ttu-id="09f7f-109">Ce filtre est représenté par le membre D3DTEXF_CONVOLUTIONMONO du type énuméré <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="09f7f-109">This filter is represented by the D3DTEXF_CONVOLUTIONMONO member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="09f7f-110">Différences entre Direct3D 9 et Direct3D 9Ex :</span><span class="sxs-lookup"><span data-stu-id="09f7f-110">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="09f7f-111">Cet indicateur est disponible uniquement dans Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="09f7f-111">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09f7f-112">D3DPTFILTERCAPS_MAGFPOINT</span><span class="sxs-lookup"><span data-stu-id="09f7f-112">D3DPTFILTERCAPS_MAGFPOINT</span></span></td>
<td><span data-ttu-id="09f7f-113">L’appareil prend en charge le filtrage par point-échantillon par étape pour agrandir les textures.</span><span class="sxs-lookup"><span data-stu-id="09f7f-113">Device supports per-stage point-sample filtering for magnifying textures.</span></span> <span data-ttu-id="09f7f-114">Le filtre d’agrandissement de l’échantillon de point est représenté par le D3DTEXF_POINT membre du type énuméré <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="09f7f-114">The point-sample magnification filter is represented by the D3DTEXF_POINT member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09f7f-115">D3DPTFILTERCAPS_MAGFLINEAR</span><span class="sxs-lookup"><span data-stu-id="09f7f-115">D3DPTFILTERCAPS_MAGFLINEAR</span></span></td>
<td><span data-ttu-id="09f7f-116">L’appareil prend en charge le filtrage de l’interpolation bilinéaire par étape pour agrandir les des mipmaps.</span><span class="sxs-lookup"><span data-stu-id="09f7f-116">Device supports per-stage bilinear interpolation filtering for magnifying mipmaps.</span></span> <span data-ttu-id="09f7f-117">Le filtre d’interpolation bilinéaire mappage MIP est représenté par le membre D3DTEXF_LINEAR du type énuméré <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="09f7f-117">The bilinear interpolation mipmapping filter is represented by the D3DTEXF_LINEAR member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09f7f-118">D3DPTFILTERCAPS_MAGFANISOTROPIC</span><span class="sxs-lookup"><span data-stu-id="09f7f-118">D3DPTFILTERCAPS_MAGFANISOTROPIC</span></span></td>
<td><span data-ttu-id="09f7f-119">L’appareil prend en charge le filtrage anisotrope par étape pour agrandir les textures.</span><span class="sxs-lookup"><span data-stu-id="09f7f-119">Device supports per-stage anisotropic filtering for magnifying textures.</span></span> <span data-ttu-id="09f7f-120">Le filtre d’agrandissement anisotrope est représenté par le D3DTEXF_ANISOTROPIC membre du type énuméré <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="09f7f-120">The anisotropic magnification filter is represented by the D3DTEXF_ANISOTROPIC member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09f7f-121">D3DPTFILTERCAPS_MAGFPYRAMIDALQUAD</span><span class="sxs-lookup"><span data-stu-id="09f7f-121">D3DPTFILTERCAPS_MAGFPYRAMIDALQUAD</span></span></td>
<td><span data-ttu-id="09f7f-122">L’appareil prend en charge l’exemple de filtrage pyramidal par étape pour agrandir les textures.</span><span class="sxs-lookup"><span data-stu-id="09f7f-122">Device supports per-stage pyramidal sample filtering for magnifying textures.</span></span> <span data-ttu-id="09f7f-123">Le filtre d’agrandissement pyramidal est représenté par le D3DTEXF_PYRAMIDALQUAD membre du type énuméré <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="09f7f-123">The pyramidal magnifying filter is represented by the D3DTEXF_PYRAMIDALQUAD member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09f7f-124">D3DPTFILTERCAPS_MAGFGAUSSIANQUAD</span><span class="sxs-lookup"><span data-stu-id="09f7f-124">D3DPTFILTERCAPS_MAGFGAUSSIANQUAD</span></span></td>
<td><span data-ttu-id="09f7f-125">L’appareil prend en charge le filtrage gaussien Quad par étape pour agrandir les textures.</span><span class="sxs-lookup"><span data-stu-id="09f7f-125">Device supports per-stage Gaussian quad filtering for magnifying textures.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09f7f-126">D3DPTFILTERCAPS_MINFPOINT</span><span class="sxs-lookup"><span data-stu-id="09f7f-126">D3DPTFILTERCAPS_MINFPOINT</span></span></td>
<td><span data-ttu-id="09f7f-127">L’appareil prend en charge le filtrage par point-échantillon par étape pour les textures minimisation.</span><span class="sxs-lookup"><span data-stu-id="09f7f-127">Device supports per-stage point-sample filtering for minifying textures.</span></span> <span data-ttu-id="09f7f-128">Le filtre de réduction d’échantillon de point est représenté par le membre D3DTEXF_POINT du type énuméré <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="09f7f-128">The point-sample minification filter is represented by the D3DTEXF_POINT member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09f7f-129">D3DPTFILTERCAPS_MINFLINEAR</span><span class="sxs-lookup"><span data-stu-id="09f7f-129">D3DPTFILTERCAPS_MINFLINEAR</span></span></td>
<td><span data-ttu-id="09f7f-130">L’appareil prend en charge le filtrage linéaire par étape pour les textures minimisation.</span><span class="sxs-lookup"><span data-stu-id="09f7f-130">Device supports per-stage linear filtering for minifying textures.</span></span> <span data-ttu-id="09f7f-131">Le filtre de réduction linéaire est représenté par le D3DTEXF_LINEAR membre du type énuméré <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="09f7f-131">The linear minification filter is represented by the D3DTEXF_LINEAR member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09f7f-132">D3DPTFILTERCAPS_MINFANISOTROPIC</span><span class="sxs-lookup"><span data-stu-id="09f7f-132">D3DPTFILTERCAPS_MINFANISOTROPIC</span></span></td>
<td><span data-ttu-id="09f7f-133">L’appareil prend en charge le filtrage anisotrope par étape pour les textures minimisation.</span><span class="sxs-lookup"><span data-stu-id="09f7f-133">Device supports per-stage anisotropic filtering for minifying textures.</span></span> <span data-ttu-id="09f7f-134">Le filtre de minimisation anisotrope est représenté par le D3DTEXF_ANISOTROPIC membre du type énuméré <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="09f7f-134">The anisotropic minification filter is represented by the D3DTEXF_ANISOTROPIC member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09f7f-135">D3DPTFILTERCAPS_MINFPYRAMIDALQUAD</span><span class="sxs-lookup"><span data-stu-id="09f7f-135">D3DPTFILTERCAPS_MINFPYRAMIDALQUAD</span></span></td>
<td><span data-ttu-id="09f7f-136">L’appareil prend en charge le filtrage par étape de l’exemple pyramidal pour les textures minimisation.</span><span class="sxs-lookup"><span data-stu-id="09f7f-136">Device supports per-stage pyramidal sample filtering for minifying textures.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09f7f-137">D3DPTFILTERCAPS_MINFGAUSSIANQUAD</span><span class="sxs-lookup"><span data-stu-id="09f7f-137">D3DPTFILTERCAPS_MINFGAUSSIANQUAD</span></span></td>
<td><span data-ttu-id="09f7f-138">L’appareil prend en charge le filtrage gaussien Quad par étape pour les textures minimisation.</span><span class="sxs-lookup"><span data-stu-id="09f7f-138">Device supports per-stage Gaussian quad filtering for minifying textures.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09f7f-139">D3DPTFILTERCAPS_MIPFPOINT</span><span class="sxs-lookup"><span data-stu-id="09f7f-139">D3DPTFILTERCAPS_MIPFPOINT</span></span></td>
<td><span data-ttu-id="09f7f-140">L’appareil prend en charge le filtrage par point-échantillon par étape pour des mipmaps.</span><span class="sxs-lookup"><span data-stu-id="09f7f-140">Device supports per-stage point-sample filtering for mipmaps.</span></span> <span data-ttu-id="09f7f-141">Le filtre mappage MIP point-Sample est représenté par le membre D3DTEXF_POINT du type énuméré <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="09f7f-141">The point-sample mipmapping filter is represented by the D3DTEXF_POINT member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09f7f-142">D3DPTFILTERCAPS_MIPFLINEAR</span><span class="sxs-lookup"><span data-stu-id="09f7f-142">D3DPTFILTERCAPS_MIPFLINEAR</span></span></td>
<td><span data-ttu-id="09f7f-143">L’appareil prend en charge le filtrage de l’interpolation bilinéaire par étape pour des mipmaps.</span><span class="sxs-lookup"><span data-stu-id="09f7f-143">Device supports per-stage bilinear interpolation filtering for mipmaps.</span></span> <span data-ttu-id="09f7f-144">Le filtre d’interpolation bilinéaire mappage MIP est représenté par le membre D3DTEXF_LINEAR du type énuméré <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="09f7f-144">The bilinear interpolation mipmapping filter is represented by the D3DTEXF_LINEAR member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="09f7f-145">Ces constantes sont utilisées par les membres TextureFilterCaps, CubeTextureFilterCaps, VolumeTextureFilterCaps et VertexTextureFilterCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="09f7f-145">These constants are used by TextureFilterCaps, CubeTextureFilterCaps, VolumeTextureFilterCaps, and VertexTextureFilterCaps members of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="09f7f-146">Informations constantes</span><span class="sxs-lookup"><span data-stu-id="09f7f-146">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="09f7f-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="09f7f-147">Header</span></span>                   | <span data-ttu-id="09f7f-148">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="09f7f-148">d3d9caps.h</span></span> |
| <span data-ttu-id="09f7f-149">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="09f7f-149">Minimum operating system</span></span> | <span data-ttu-id="09f7f-150">Windows 98</span><span class="sxs-lookup"><span data-stu-id="09f7f-150">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="09f7f-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="09f7f-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09f7f-152">Constantes Direct3D</span><span class="sxs-lookup"><span data-stu-id="09f7f-152">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
