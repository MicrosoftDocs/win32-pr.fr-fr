---
title: Sous-ressources (Direct3D 12 Graphics)
description: Décrit comment une ressource est divisée en sous-ressources et comment référencer une seule, plusieurs ou plusieurs sous-ressources.
ms.assetid: C4F92F8A-DBF0-412B-8707-CC4C1BF2D88F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8fa8ea0d48fea7ee8e192d9dcf1fe5e3d22423
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104548552"
---
# <a name="subresources-direct3d-12-graphics"></a><span data-ttu-id="839d5-103">Sous-ressources (Direct3D 12 Graphics)</span><span class="sxs-lookup"><span data-stu-id="839d5-103">Subresources (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="839d5-104">Décrit comment une ressource est divisée en sous-ressources et comment référencer une seule, plusieurs ou plusieurs sous-ressources.</span><span class="sxs-lookup"><span data-stu-id="839d5-104">Describes how a resource is divided into subresources, and how to reference a single, multiple or slice of subresources.</span></span>

-   [<span data-ttu-id="839d5-105">Exemples de sous-ressources</span><span class="sxs-lookup"><span data-stu-id="839d5-105">Example subresources</span></span>](#example-subresources)
    -   [<span data-ttu-id="839d5-106">Indexation des sous-ressources</span><span class="sxs-lookup"><span data-stu-id="839d5-106">Subresource indexing</span></span>](#subresource-indexing)
    -   [<span data-ttu-id="839d5-107">Tranche MIP</span><span class="sxs-lookup"><span data-stu-id="839d5-107">Mip slice</span></span>](#mip-slice)
    -   [<span data-ttu-id="839d5-108">Tranche de tableau</span><span class="sxs-lookup"><span data-stu-id="839d5-108">Array slice</span></span>](#array-slice)
    -   [<span data-ttu-id="839d5-109">Tranche plan</span><span class="sxs-lookup"><span data-stu-id="839d5-109">Plane slice</span></span>](#plane-slice)
    -   [<span data-ttu-id="839d5-110">Sous-ressources multiples</span><span class="sxs-lookup"><span data-stu-id="839d5-110">Multiple subresources</span></span>](#multiple-subresources)
-   [<span data-ttu-id="839d5-111">API de sous-ressource</span><span class="sxs-lookup"><span data-stu-id="839d5-111">Subresource APIs</span></span>](#subresource-apis)
-   [<span data-ttu-id="839d5-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="839d5-112">Related topics</span></span>](#related-topics)

## <a name="example-subresources"></a><span data-ttu-id="839d5-113">Exemples de sous-ressources</span><span class="sxs-lookup"><span data-stu-id="839d5-113">Example subresources</span></span>

<span data-ttu-id="839d5-114">Si une ressource contient une mémoire tampon, elle contient simplement une sous-ressource avec un index de 0.</span><span class="sxs-lookup"><span data-stu-id="839d5-114">If a resource contains a buffer, then it simply contains one subresource with an index of 0.</span></span> <span data-ttu-id="839d5-115">Si la ressource contient une texture (ou un tableau de textures), le référencement des sous-ressources est plus complexe.</span><span class="sxs-lookup"><span data-stu-id="839d5-115">If the resource contains a texture (or texture array), then referencing the subresources is more complex.</span></span>

<span data-ttu-id="839d5-116">Certaines API accèdent à une ressource entière (telle que la méthode [**ID3D12GraphicsCommandList :: CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource) ), d’autres accèdent à une partie d’une ressource (par exemple, la méthode [**ID3D12Resource :: ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) ).</span><span class="sxs-lookup"><span data-stu-id="839d5-116">Some APIs access an entire resource (such as the [**ID3D12GraphicsCommandList::CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource) method), others access a portion of a resource (for example the [**ID3D12Resource::ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) method).</span></span> <span data-ttu-id="839d5-117">Les méthodes qui accèdent à une partie d’une ressource utilisent généralement une description de la vue (telle que la structure [**\_ SRV du \_ tableau \_ D3D12 TEX2D**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv) ) pour spécifier les sous-ressources auxquelles accéder.</span><span class="sxs-lookup"><span data-stu-id="839d5-117">The methods that access a portion of a resource generally use a view description (such as the [**D3D12\_TEX2D\_ARRAY\_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv) structure) to specify the subresources to access.</span></span> <span data-ttu-id="839d5-118">Reportez-vous à la section API des sous- [ressources](#subresource-apis) pour obtenir une liste complète.</span><span class="sxs-lookup"><span data-stu-id="839d5-118">Refer to the [Subresource APIs](#subresource-apis) section for a complete list.</span></span>

### <a name="subresource-indexing"></a><span data-ttu-id="839d5-119">Indexation des sous-ressources</span><span class="sxs-lookup"><span data-stu-id="839d5-119">Subresource indexing</span></span>

<span data-ttu-id="839d5-120">Pour indexer une sous-ressource particulière, les niveaux MIP sont indexés en premier lorsque chaque entrée de tableau est indexée.</span><span class="sxs-lookup"><span data-stu-id="839d5-120">To index a particular subresource, the mip levels are indexed first as each array entry is indexed.</span></span>

![indexation des sous-ressources](images/subresource-index.png)

### <a name="mip-slice"></a><span data-ttu-id="839d5-122">Tranche MIP</span><span class="sxs-lookup"><span data-stu-id="839d5-122">Mip slice</span></span>

<span data-ttu-id="839d5-123">Une tranche MIP comprend un niveau de mipmap pour chaque texture d’un tableau, comme illustré dans l’image suivante.</span><span class="sxs-lookup"><span data-stu-id="839d5-123">A mip slice includes one mipmap level for every texture in an array, as shown in the following image.</span></span>

![tranches MIP de sous-ressources](images/subresource-mip-slice.png)

### <a name="array-slice"></a><span data-ttu-id="839d5-125">Tranche de tableau</span><span class="sxs-lookup"><span data-stu-id="839d5-125">Array slice</span></span>

<span data-ttu-id="839d5-126">À partir d’un tableau de textures, chaque texture avec des mipmaps, une tranche de tableau comprend une texture et tous ses niveaux MIP, comme illustré dans l’image suivante.</span><span class="sxs-lookup"><span data-stu-id="839d5-126">Given an array of textures, each texture with mipmaps, an array slice includes one texture and all of its mip levels, as shown in the following image.</span></span>

![tranches de groupe de sous-ressources](images/subresource-array-slices.png)

### <a name="plane-slice"></a><span data-ttu-id="839d5-128">Tranche plan</span><span class="sxs-lookup"><span data-stu-id="839d5-128">Plane slice</span></span>

<span data-ttu-id="839d5-129">En général, les formats planaires ne sont pas utilisés pour stocker les données RVBA, mais dans les cas où il s’agit (par exemple, des données RGB 24bpp), un plan peut représenter l’image rouge, l’image verte et l’image bleue.</span><span class="sxs-lookup"><span data-stu-id="839d5-129">Typically planar formats are not used to store RGBA data, but in the cases where it is (perhaps 24bpp RGB data), one plane could represent the red image, one the green, and one the blue image.</span></span> <span data-ttu-id="839d5-130">Toutefois, un plan n’est pas nécessairement une couleur, deux couleurs ou plus peuvent être combinées dans un plan.</span><span class="sxs-lookup"><span data-stu-id="839d5-130">One plane though is not necessarily one color, two or more colors could be combined into one plane.</span></span> <span data-ttu-id="839d5-131">Plus généralement, les données planaires sont utilisées pour les données de Depth-Stencil et YCbCr sous-échantillonnées.</span><span class="sxs-lookup"><span data-stu-id="839d5-131">More typically planar data is used for sub-sampled YCbCr and Depth-Stencil data.</span></span> <span data-ttu-id="839d5-132">Depth-Stencil est le seul format qui prend entièrement en charge les des mipmaps, les tableaux et les plans multiples (souvent le plan 0 pour la profondeur et le plan 1 du stencil).</span><span class="sxs-lookup"><span data-stu-id="839d5-132">Depth-Stencil is the only format that fully supports mipmaps, arrays, and multiple planes (often plane 0 for Depth and plane 1 for Stencil).</span></span>

<span data-ttu-id="839d5-133">L’indexation des sous-ressources pour un tableau de deux images Depth-Stencil, chacune avec trois niveaux MIP, est illustrée ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="839d5-133">The subresource indexing for an array of two Depth-Stencil images, each with three mip levels, is shown below.</span></span>

![indexation du stencil de profondeur](images/depth-stencil-indexing.png)

<span data-ttu-id="839d5-135">Le sous-échantillon YCbCr prend en charge les tableaux et contient des plans, mais ne prend pas en charge des mipmaps.</span><span class="sxs-lookup"><span data-stu-id="839d5-135">Sub-sampled YCbCr supports arrays and has planes, but does not support mipmaps.</span></span> <span data-ttu-id="839d5-136">Les images YCbCr ont deux plans, l’un pour la luminance (Y), dont l’oeil humain est le plus sensible, et l’autre pour la chrominance (à la fois CB et CR, entrelacé) qui est moins sensible à l’oeil humain.</span><span class="sxs-lookup"><span data-stu-id="839d5-136">YCbCr images have two planes, one for the luminance (Y) that the human eye is most sensitive to, and one for the chrominance (both Cb, and Cr, interleaved) which the human eye is less sensitive to.</span></span> <span data-ttu-id="839d5-137">Ce format permet la compression des valeurs de chrominance afin de compresser une image sans affecter la luminance, et est un format de compression vidéo courant pour cette raison, bien qu’elle soit utilisée pour compresser des images fixes.</span><span class="sxs-lookup"><span data-stu-id="839d5-137">This format enables compression of the chrominance values in order to compress an image without affecting the luminance, and is a common video compression format for that reason, although it is used to compress still images.</span></span> <span data-ttu-id="839d5-138">L’image ci-dessous montre le format NV12, en notant que la chrominance a été compressée à un quart de la résolution de la luminance, ce qui signifie que la largeur de chaque plan est identique et que le plan de chrominance correspond à la moitié de la hauteur du plan de luminance.</span><span class="sxs-lookup"><span data-stu-id="839d5-138">The image below shows the NV12 format, noting the chrominance has been compressed to one quarter of the resolution of the luminance, meaning the width of each plane is identical, and the chrominance plane is half the height of the luminance plane.</span></span> <span data-ttu-id="839d5-139">Les plans sont indexés en tant que sous-ressources de manière identique à l’exemple de Depth-Stencil ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="839d5-139">The planes would be indexed as subresources in an identical way to the Depth-Stencil example above.</span></span>

![format nv12](images/ycbcr.png)

<span data-ttu-id="839d5-141">Les formats planaires existaient dans Direct3D 11, mais les plans individuels n’ont pas pu être traités individuellement, par exemple pour les opérations de copie ou de mappage.</span><span class="sxs-lookup"><span data-stu-id="839d5-141">Planar formats existed in Direct3D 11, but individual planes could not be addressed individually, say for copy or mapping operations.</span></span> <span data-ttu-id="839d5-142">Cela a été modifié dans Direct3D 12 afin que chaque plan ait reçu son propre ID de sous-ressource.</span><span class="sxs-lookup"><span data-stu-id="839d5-142">This was changed in Direct3D 12 so that each plane received its own subresource ID.</span></span> <span data-ttu-id="839d5-143">Comparez les deux méthodes suivantes pour calculer l’ID de sous-ressource.</span><span class="sxs-lookup"><span data-stu-id="839d5-143">Compare the following two methods for calculating the subresource ID.</span></span>

<span data-ttu-id="839d5-144">Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="839d5-144">Direct3D 11</span></span>

``` syntax
inline UINT D3D11CalcSubresource( UINT MipSlice, UINT ArraySlice, UINT MipLevels )
{
    return MipSlice + (ArraySlice * MipLevels); 
}
```

<span data-ttu-id="839d5-145">Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="839d5-145">Direct3D 12</span></span>

``` syntax
inline UINT D3D12CalcSubresource( UINT MipSlice, UINT ArraySlice, UINT PlaneSlice, UINT MipLevels, UINT ArraySize )
{ 
    return MipSlice + (ArraySlice * MipLevels) + (PlaneSlice * MipLevels * ArraySize); 
}
```

<span data-ttu-id="839d5-146">La plupart du matériel suppose que la mémoire pour le plan N est toujours allouée immédiatement après le plan N-1.</span><span class="sxs-lookup"><span data-stu-id="839d5-146">Most hardware assumes that the memory for plane N is always immediately allocated after plane N-1.</span></span>

<span data-ttu-id="839d5-147">Une alternative à l’utilisation de sous-ressources est qu’une application peut allouer une ressource complètement distincte par plan.</span><span class="sxs-lookup"><span data-stu-id="839d5-147">An alternative to using subresources is that an app could allocate a completely separate resource per plane.</span></span> <span data-ttu-id="839d5-148">Dans ce cas, l’application comprend les données planes et utilise plusieurs ressources pour les représenter.</span><span class="sxs-lookup"><span data-stu-id="839d5-148">In this case, the application understands the data is planar and uses multiple resources to represent it.</span></span>

### <a name="multiple-subresources"></a><span data-ttu-id="839d5-149">Sous-ressources multiples</span><span class="sxs-lookup"><span data-stu-id="839d5-149">Multiple subresources</span></span>

<span data-ttu-id="839d5-150">Un affichage des ressources de nuanceur peut sélectionner n’importe quelle zone rectangulaire de sous-ressources, à l’aide de l’une des tranches décrites ci-dessus et de l’utilisation judicieuse des champs dans les structures de vue (par exemple, [**D3D12 \_ TEX2D \_ array \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)), comme indiqué dans l’image.</span><span class="sxs-lookup"><span data-stu-id="839d5-150">A shader-resource view can select any rectangular region of subresources, using one of the slices described above and judicious use of fields in the view structures (such as [**D3D12\_TEX2D\_ARRAY\_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)), as shown in the image.</span></span>

![sélection de plusieurs sous-ressources](images/subresource-multiple.png)

<span data-ttu-id="839d5-152">Une vue de cible de rendu ne peut utiliser qu’une seule sous-ressource ou une seule tranche MIP et ne peut pas inclure de sous-ressources de plus d’une tranche MIP.</span><span class="sxs-lookup"><span data-stu-id="839d5-152">A render-target view can only use a single subresource or mip slice and cannot include subresources from more than one mip slice.</span></span> <span data-ttu-id="839d5-153">Autrement dit, chaque texture dans une vue de cible de rendu doit avoir la même taille.</span><span class="sxs-lookup"><span data-stu-id="839d5-153">That is, every texture in a render-target view must be the same size.</span></span> <span data-ttu-id="839d5-154">Un affichage des ressources de nuanceur peut sélectionner n’importe quelle zone rectangulaire de sous-ressources, comme illustré dans l’image.</span><span class="sxs-lookup"><span data-stu-id="839d5-154">A shader-resource view can select any rectangular region of subresources, as shown in the image.</span></span>

## <a name="subresource-apis"></a><span data-ttu-id="839d5-155">API de sous-ressource</span><span class="sxs-lookup"><span data-stu-id="839d5-155">Subresource APIs</span></span>

<span data-ttu-id="839d5-156">Les API suivantes référencent et utilisent des sous-ressources :</span><span class="sxs-lookup"><span data-stu-id="839d5-156">The following APIs reference and work with subresources:</span></span>

<span data-ttu-id="839d5-157">Énumérations :</span><span class="sxs-lookup"><span data-stu-id="839d5-157">Enumerations:</span></span>

-   [<span data-ttu-id="839d5-158">**\_Type de \_ copie de texture D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="839d5-158">**D3D12\_TEXTURE\_COPY\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type)

<span data-ttu-id="839d5-159">Les structures suivantes contiennent des index *PlaneSlice* , la plupart contiennent des index *MipSlice* .</span><span class="sxs-lookup"><span data-stu-id="839d5-159">The following structures contain *PlaneSlice* indexes, most contain *MipSlice* indexes.</span></span>

-   [<span data-ttu-id="839d5-160">**D3D12 \_ TEX2D \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="839d5-160">**D3D12\_TEX2D\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_rtv)
-   [<span data-ttu-id="839d5-161">**D3D12 \_ \_ tableau TEX2D \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="839d5-161">**D3D12\_TEX2D\_ARRAY\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [<span data-ttu-id="839d5-162">**D3D12 \_ TEX2D \_ SRV**</span><span class="sxs-lookup"><span data-stu-id="839d5-162">**D3D12\_TEX2D\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_srv)
-   [<span data-ttu-id="839d5-163">**\_SRV du \_ tableau D3D12 TEX2D \_**</span><span class="sxs-lookup"><span data-stu-id="839d5-163">**D3D12\_TEX2D\_ARRAY\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [<span data-ttu-id="839d5-164">**D3D12 \_ TEX2D \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="839d5-164">**D3D12\_TEX2D\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_uav)
-   [<span data-ttu-id="839d5-165">**D3D12 \_ TEX2D \_ array \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="839d5-165">**D3D12\_TEX2D\_ARRAY\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)

<span data-ttu-id="839d5-166">Les structures suivantes contiennent des index *ArraySlice* , la plupart contiennent des index *MipSlice* .</span><span class="sxs-lookup"><span data-stu-id="839d5-166">The following structures contain *ArraySlice* indexes, most contain *MipSlice* indexes.</span></span>

-   [<span data-ttu-id="839d5-167">**\_DSV D3D12 TEX1D \_ array \_**</span><span class="sxs-lookup"><span data-stu-id="839d5-167">**D3D12\_TEX1D\_ARRAY\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_dsv)
-   [<span data-ttu-id="839d5-168">**\_DSV D3D12 TEX2D \_ array \_**</span><span class="sxs-lookup"><span data-stu-id="839d5-168">**D3D12\_TEX2D\_ARRAY\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_dsv)
-   [<span data-ttu-id="839d5-169">**\_DSV D3D12 TEX2DMS \_ array \_**</span><span class="sxs-lookup"><span data-stu-id="839d5-169">**D3D12\_TEX2DMS\_ARRAY\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_dsv)
-   [<span data-ttu-id="839d5-170">**D3D12 \_ \_ tableau TEX1D \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="839d5-170">**D3D12\_TEX1D\_ARRAY\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_rtv)
-   [<span data-ttu-id="839d5-171">**D3D12 \_ \_ tableau TEX2D \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="839d5-171">**D3D12\_TEX2D\_ARRAY\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [<span data-ttu-id="839d5-172">**D3D12 \_ \_ tableau TEX2DMS \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="839d5-172">**D3D12\_TEX2DMS\_ARRAY\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_rtv)
-   [<span data-ttu-id="839d5-173">**\_SRV du \_ tableau D3D12 TEX1D \_**</span><span class="sxs-lookup"><span data-stu-id="839d5-173">**D3D12\_TEX1D\_ARRAY\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_srv)
-   [<span data-ttu-id="839d5-174">**\_SRV du \_ tableau D3D12 TEX2D \_**</span><span class="sxs-lookup"><span data-stu-id="839d5-174">**D3D12\_TEX2D\_ARRAY\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [<span data-ttu-id="839d5-175">**\_SRV du \_ tableau D3D12 TEX2DMS \_**</span><span class="sxs-lookup"><span data-stu-id="839d5-175">**D3D12\_TEX2DMS\_ARRAY\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_srv)
-   [<span data-ttu-id="839d5-176">**D3D12 \_ TEX1D \_ array \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="839d5-176">**D3D12\_TEX1D\_ARRAY\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_uav)
-   [<span data-ttu-id="839d5-177">**D3D12 \_ TEX2D \_ array \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="839d5-177">**D3D12\_TEX2D\_ARRAY\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)

<span data-ttu-id="839d5-178">Les structures suivantes contiennent des index *MipSlice* , mais ni des index *ArraySlice* , ni des index *PlaneSlice* .</span><span class="sxs-lookup"><span data-stu-id="839d5-178">The following structures contain *MipSlice* indexes, but neither *ArraySlice* nor *PlaneSlice* indexes.</span></span>

-   [<span data-ttu-id="839d5-179">**D3D12 \_ TEX1D \_ DSV**</span><span class="sxs-lookup"><span data-stu-id="839d5-179">**D3D12\_TEX1D\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_dsv)
-   [<span data-ttu-id="839d5-180">**D3D12 \_ TEX2D \_ DSV**</span><span class="sxs-lookup"><span data-stu-id="839d5-180">**D3D12\_TEX2D\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_dsv)
-   [<span data-ttu-id="839d5-181">**D3D12 \_ TEX1D \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="839d5-181">**D3D12\_TEX1D\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_rtv)
-   [<span data-ttu-id="839d5-182">**D3D12 \_ TEX3D \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="839d5-182">**D3D12\_TEX3D\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_rtv)
-   [<span data-ttu-id="839d5-183">**D3D12 \_ TEX1D \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="839d5-183">**D3D12\_TEX1D\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_uav)
-   [<span data-ttu-id="839d5-184">**D3D12 \_ TEX3D \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="839d5-184">**D3D12\_TEX3D\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_uav)

<span data-ttu-id="839d5-185">Les structures suivantes référencent également des sous-ressources :</span><span class="sxs-lookup"><span data-stu-id="839d5-185">The following structures also reference subresources:</span></span>

-   <span data-ttu-id="839d5-186">[**D3D12 \_ IGNORER la \_ région**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region) : structure utilisée pour la préparation de l’abandon d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="839d5-186">[**D3D12\_DISCARD\_REGION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region) : a structure used in preparation for discarding a resource.</span></span>
-   <span data-ttu-id="839d5-187">[**D3D12 \_ \_ \_ Encombrement**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) des sous-ressources placé : ajoute un décalage dans une ressource à l’encombrement de base.</span><span class="sxs-lookup"><span data-stu-id="839d5-187">[**D3D12\_PLACED\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) : adds an offset into a resource to the basic footprint.</span></span>
-   <span data-ttu-id="839d5-188">[**D3D12 \_ \_ \_ Barrière de transition de ressource**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) : décrit la transition des sous-ressources entre différentes utilisations (ressource de nuanceur, cible de rendu, etc.).</span><span class="sxs-lookup"><span data-stu-id="839d5-188">[**D3D12\_RESOURCE\_TRANSITION\_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) : describes the transition of subresources between different usages (shader resource, render target, etc.).</span></span>
-   <span data-ttu-id="839d5-189">[**D3D12 \_ \_Données**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) des sous-ressources : les données des sous-ressources incluent les données elles-mêmes, ainsi que la largeur des lignes et des secteurs.</span><span class="sxs-lookup"><span data-stu-id="839d5-189">[**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) : subresource data includes the data itself, and the row and slice pitch.</span></span>
-   <span data-ttu-id="839d5-190">[**D3D12 \_ \_Encombrement**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) des sous-ressources : un encombrement comprend le format, la largeur, la hauteur, la profondeur et l’espacement des lignes de la sous-ressource.</span><span class="sxs-lookup"><span data-stu-id="839d5-190">[**D3D12\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) : a footprint includes the format, width, height, depth and row-pitch of the subresource.</span></span>
-   <span data-ttu-id="839d5-191">[**D3D12 \_ \_Informations sur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_info) les sous-ressources : contient le décalage, la largeur des lignes et le pas de profondeur de la sous-ressource.</span><span class="sxs-lookup"><span data-stu-id="839d5-191">[**D3D12\_SUBRESOURCE\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_info) : contains the offset, row pitch and depth pitch of the subresource.</span></span>
-   <span data-ttu-id="839d5-192">[**D3D12 \_ \_Mosaïque**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) de sous-ressources : décrit un volume de sous-ressources en mosaïque (reportez-vous à [ressources en mosaïque de volume](volume-tiled-resources.md)).</span><span class="sxs-lookup"><span data-stu-id="839d5-192">[**D3D12\_SUBRESOURCE\_TILING**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) : describes a tiled subresource volume (refer to [Volume Tiled Resources](volume-tiled-resources.md)).</span></span>
-   <span data-ttu-id="839d5-193">[**D3D12 \_ \_ \_ Emplacement de copie de texture**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) : décrit une partie d’une texture à des fins de copie.</span><span class="sxs-lookup"><span data-stu-id="839d5-193">[**D3D12\_TEXTURE\_COPY\_LOCATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) : describes a portion of a texture for the purpose of copying.</span></span>
-   <span data-ttu-id="839d5-194">[**D3D12 \_ \_ \_ Coordonnée des ressources en mosaïque**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : décrit les coordonnées d’une ressource en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="839d5-194">[**D3D12\_TILED\_RESOURCE\_COORDINATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : describes the coordinates of a tiled resource.</span></span>

<span data-ttu-id="839d5-195">Méthodes :</span><span class="sxs-lookup"><span data-stu-id="839d5-195">Methods:</span></span>

-   <span data-ttu-id="839d5-196">[**ID3D12Device :: GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints) : obtient des informations sur une ressource pour permettre l’établissement d’une copie.</span><span class="sxs-lookup"><span data-stu-id="839d5-196">[**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints) : gets information on a resource, to enable a copy to be made.</span></span>
-   <span data-ttu-id="839d5-197">[**ID3D12Device :: GetResourceTiling**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : obtient des informations sur la façon dont une ressource en mosaïque est divisée en mosaïques.</span><span class="sxs-lookup"><span data-stu-id="839d5-197">[**ID3D12Device::GetResourceTiling**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : gets info about how a tiled resource is broken into tiles.</span></span>
-   <span data-ttu-id="839d5-198">[**ID3D12GraphicsCommandList :: ResolveSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource) : copie une sous-ressource échantillonnée sur plusieurs sous-ressources échantillonnées.</span><span class="sxs-lookup"><span data-stu-id="839d5-198">[**ID3D12GraphicsCommandList::ResolveSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource) : copies a multi-sampled subresource into a non-multi-sampled subresource.</span></span>
-   <span data-ttu-id="839d5-199">[**ID3D12Resource :: Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) : retourne un pointeur vers les données spécifiées dans la ressource et refuse l’accès au GPU à la sous-ressource.</span><span class="sxs-lookup"><span data-stu-id="839d5-199">[**ID3D12Resource::Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) : returns a pointer to the specified data in the resource, and denies the GPU access to the subresource.</span></span>
-   <span data-ttu-id="839d5-200">[**ID3D12Resource :: ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) : copie les données d’une sous-ressource, ou une zone rectangulaire d’une sous-ressource.</span><span class="sxs-lookup"><span data-stu-id="839d5-200">[**ID3D12Resource::ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) : copies data from a subresource, or a rectangular region of a subresource.</span></span>
-   <span data-ttu-id="839d5-201">[**ID3D12Resource :: DEMAPPAGE**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) : annule la correspondance de la plage de mémoire spécifiée et invalide le pointeur vers la ressource.</span><span class="sxs-lookup"><span data-stu-id="839d5-201">[**ID3D12Resource::Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) : unmaps the specified range of memory and invalidates the pointer to the resource.</span></span> <span data-ttu-id="839d5-202">Rétablit l’accès GPU à la sous-ressource.</span><span class="sxs-lookup"><span data-stu-id="839d5-202">Reinstates GPU access to the subresource.</span></span>
-   <span data-ttu-id="839d5-203">[**ID3D12Resource :: WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) : copie des données vers une sous-ressource, ou une zone rectangulaire d’une sous-ressource.</span><span class="sxs-lookup"><span data-stu-id="839d5-203">[**ID3D12Resource::WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) : copies data to a subresource, or a rectangular region of a subresource.</span></span>

<span data-ttu-id="839d5-204">Les textures doivent être dans l’État commun de l’état de la [**\_ ressource \_ \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) pour que l’accès au processeur via [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) et [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) soit légal, mais ce n’est pas le cas des tampons.</span><span class="sxs-lookup"><span data-stu-id="839d5-204">Textures must be in the [**D3D12\_RESOURCE\_STATE\_COMMON**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) state for CPU access through [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) and [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) to be legal; but buffers do not.</span></span> <span data-ttu-id="839d5-205">L’accès de l’UC à une ressource est généralement effectué par le biais de [**mappages de mappage**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) / [](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap).</span><span class="sxs-lookup"><span data-stu-id="839d5-205">CPU access to a resource is typically done through [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)/[**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap).</span></span>

## <a name="related-topics"></a><span data-ttu-id="839d5-206">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="839d5-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="839d5-207">Liaison de ressource</span><span class="sxs-lookup"><span data-stu-id="839d5-207">Resource Binding</span></span>](resource-binding.md)
</dt> </dl>

 

 




