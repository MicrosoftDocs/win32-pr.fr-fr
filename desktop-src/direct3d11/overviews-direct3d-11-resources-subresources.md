---
title: Sous-ressources (graphiques Direct3D 11)
description: Cette rubrique décrit les sous-ressources de texture ou des parties d’une ressource.
ms.assetid: 57444cb5-6c8b-4dac-8d6b-ca2b45eafac9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a432dbfbcbf08c4359ea436a3e8fa025c801d12
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104032160"
---
# <a name="subresources-direct3d-11-graphics"></a><span data-ttu-id="d21e1-103">Sous-ressources (graphiques Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="d21e1-103">Subresources (Direct3D 11 Graphics)</span></span>

<span data-ttu-id="d21e1-104">Cette rubrique décrit les sous-ressources de texture ou des parties d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="d21e1-104">This topic describes texture subresources, or portions of a resource.</span></span>

<span data-ttu-id="d21e1-105">Direct3D peut faire référence à une ressource entière ou référencer des sous-ensembles d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="d21e1-105">Direct3D can reference an entire resource or it can reference subsets of a resource.</span></span> <span data-ttu-id="d21e1-106">Le terme sous-ressource fait référence à un sous-ensemble d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="d21e1-106">The term subresource refers to a subset of a resource.</span></span>

<span data-ttu-id="d21e1-107">Une mémoire tampon est définie en tant que sous-ressource unique.</span><span class="sxs-lookup"><span data-stu-id="d21e1-107">A buffer is defined as a single subresource.</span></span> <span data-ttu-id="d21e1-108">Les textures sont un peu plus compliquées, car il existe plusieurs types de textures (1D, 2D, etc.) qui prennent en charge des niveaux de mipmap et/ou des tableaux de texture.</span><span class="sxs-lookup"><span data-stu-id="d21e1-108">Textures are a little more complicated because there are several different texture types (1D, 2D, etc.) some of which support mipmap levels and/or texture arrays.</span></span> <span data-ttu-id="d21e1-109">En commençant par le cas le plus simple, une texture 1D est définie en tant que sous-ressource unique, comme le montre l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="d21e1-109">Beginning with the simplest case, a 1D texture is defined as a single subresource, as shown in the following illustration.</span></span>

![illustration d’une texture 1D](images/d3d10-1d-texture.png)

<span data-ttu-id="d21e1-111">Cela signifie que le tableau de texels qui composent une texture 1D est contenu dans une seule sous-ressource.</span><span class="sxs-lookup"><span data-stu-id="d21e1-111">This means that the array of texels that make up a 1D texture are contained in a single subresource.</span></span>

<span data-ttu-id="d21e1-112">Si vous développez une texture 1D avec trois niveaux de mipmap, elle peut être visualisée comme dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="d21e1-112">If you expand a 1D texture with three mipmap levels, it can be visualized like the following illustration.</span></span>

![illustration d’une texture 1D avec trois niveaux de mipmap](images/d3d10-resource-texture1d.png)

<span data-ttu-id="d21e1-114">Imaginez qu’il s’agit d’une texture unique composée de trois sous-ressources.</span><span class="sxs-lookup"><span data-stu-id="d21e1-114">Think of this as a single texture that is made up of three subresources.</span></span> <span data-ttu-id="d21e1-115">Une sous-ressource peut être indexée à l’aide du niveau de détail (LOD) pour une seule texture.</span><span class="sxs-lookup"><span data-stu-id="d21e1-115">A subresource can be indexed using the level-of-detail (LOD) for a single texture.</span></span> <span data-ttu-id="d21e1-116">Lors de l’utilisation d’un tableau de textures, l’accès à une sous-ressource particulière nécessite à la fois le LOD et la texture particulière.</span><span class="sxs-lookup"><span data-stu-id="d21e1-116">When using an array of textures, accessing a particular subresource requires both the LOD and the particular texture.</span></span> <span data-ttu-id="d21e1-117">L’API combine ces deux informations dans un seul index de sous-ressources de base zéro, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="d21e1-117">Alternately, the API combines these two pieces of information into a single zero-based subresource index, as shown in the following illustration.</span></span>

![illustration d’un index de sous-ressources de base zéro](images/d3d10-resource-texture1darray-sub-indexing.png)

## <a name="selecting-subresources"></a><span data-ttu-id="d21e1-119">Sélection de sous-ressources</span><span class="sxs-lookup"><span data-stu-id="d21e1-119">Selecting Subresources</span></span>

<span data-ttu-id="d21e1-120">Certaines API accèdent à une ressource entière (par exemple, la méthode [**ID3D11DeviceContext :: CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) ), d’autres accèdent à une partie d’une ressource (par exemple, la méthode [**ID3D11DeviceContext :: UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) ou la méthode [**ID3D11DeviceContext :: CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) ).</span><span class="sxs-lookup"><span data-stu-id="d21e1-120">Some APIs access an entire resource (for example the [**ID3D11DeviceContext::CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) method), others access a portion of a resource (for example the [**ID3D11DeviceContext::UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) method or the [**ID3D11DeviceContext::CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) method).</span></span> <span data-ttu-id="d21e1-121">Les méthodes qui accèdent à une partie d’une ressource utilisent généralement une description de la vue (telle que la structure [**\_ \_ \_ DSV d3d11 TEX2D Array**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_dsv) ) pour spécifier les sous-ressources auxquelles accéder.</span><span class="sxs-lookup"><span data-stu-id="d21e1-121">The methods that access a portion of a resource generally use a view description (such as the [**D3D11\_TEX2D\_ARRAY\_DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_dsv) structure) to specify the subresources to access.</span></span>

<span data-ttu-id="d21e1-122">Les illustrations des sections suivantes montrent les termes utilisés par une description de la vue lors de l’accès à un tableau de textures.</span><span class="sxs-lookup"><span data-stu-id="d21e1-122">The illustrations in the following sections show the terms used by a view description when accessing an array of textures.</span></span>

### <a name="array-slice"></a><span data-ttu-id="d21e1-123">Tranche de tableau</span><span class="sxs-lookup"><span data-stu-id="d21e1-123">Array Slice</span></span>

<span data-ttu-id="d21e1-124">À partir d’un tableau de textures, chaque texture avec des mipmaps, une *tranche de tableau* (représentée par le rectangle blanc) comprend une texture et toutes ses sous-ressources, comme le montre l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="d21e1-124">Given an array of textures, each texture with mipmaps, an *array slice* (represented by the white rectangle) includes one texture and all of its subresources, as shown in the following illustration.</span></span>

![illustration d’une tranche de tableau](images/d3d10-resource-array-slice.png)

### <a name="mip-slice"></a><span data-ttu-id="d21e1-126">Tranche MIP</span><span class="sxs-lookup"><span data-stu-id="d21e1-126">Mip Slice</span></span>

<span data-ttu-id="d21e1-127">Une *tranche MIP* (représentée par le rectangle blanc) comprend un niveau de mipmap pour chaque texture d’un tableau, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="d21e1-127">A *mip slice* (represented by the white rectangle) includes one mipmap level for every texture in an array, as shown in the following illustration.</span></span>

![illustration d’une tranche MIP](images/d3d10-resource-mip-slice.png)

### <a name="selecting-a-single-subresource"></a><span data-ttu-id="d21e1-129">Sélection d’une seule sous-ressource</span><span class="sxs-lookup"><span data-stu-id="d21e1-129">Selecting a Single Subresource</span></span>

<span data-ttu-id="d21e1-130">Vous pouvez utiliser ces deux types de tranches pour choisir une seule sous-ressource, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="d21e1-130">You can use these two types of slices to choose a single subresource, as shown in the following illustration.</span></span>

![illustration du choix d’une sous-ressource à l’aide d’un segment de tableau et d’une tranche MIP](images/d3d10-resource-subresources-1.png)

### <a name="selecting-multiple-subresources"></a><span data-ttu-id="d21e1-132">Sélection de plusieurs sous-ressources</span><span class="sxs-lookup"><span data-stu-id="d21e1-132">Selecting Multiple Subresources</span></span>

<span data-ttu-id="d21e1-133">Vous pouvez aussi utiliser ces deux types de tranches avec le nombre de niveaux de mipmap et/ou le nombre de textures, pour choisir plusieurs sous-ressources, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="d21e1-133">Or you can use these two types of slices with the number of mipmap levels and/or number of textures, to choose multiple subresources, as shown in the following illustration.</span></span>

![illustration du choix de plusieurs sous-ressources](images/d3d10-resource-subresources-2.png)

> [!Note]  
> <span data-ttu-id="d21e1-135">Une [**vue de cible de rendu**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_render_target_view_desc) ne peut utiliser qu’une seule sous-ressource ou une seule tranche MIP et ne peut pas inclure de sous-ressources de plus d’une tranche MIP.</span><span class="sxs-lookup"><span data-stu-id="d21e1-135">A [**render-target view**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_render_target_view_desc) can only use a single subresource or mip slice and cannot include subresources from more than one mip slice.</span></span> <span data-ttu-id="d21e1-136">Autrement dit, chaque texture dans une vue de cible de rendu doit avoir la même taille.</span><span class="sxs-lookup"><span data-stu-id="d21e1-136">That is, every texture in a render-target view must be the same size.</span></span> <span data-ttu-id="d21e1-137">Un [**affichage des ressources de nuanceur**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) peut sélectionner n’importe quelle région rectangulaire de sous-ressources, comme illustré dans la figure.</span><span class="sxs-lookup"><span data-stu-id="d21e1-137">A [**shader-resource view**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) can select any rectangular region of subresources, as shown in the figure.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d21e1-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d21e1-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d21e1-139">Ressources</span><span class="sxs-lookup"><span data-stu-id="d21e1-139">Resources</span></span>](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 




