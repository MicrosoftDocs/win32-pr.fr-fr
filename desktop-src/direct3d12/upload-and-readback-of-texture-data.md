---
title: Chargement de données de texture dans des mémoires tampons
description: Le chargement de données de texture 2D ou 3D est similaire au chargement de données 1D, à ceci près que les applications doivent être plus particulièrement attentifes à l’alignement des données liées au pas à pas.
ms.assetid: 22A25A94-A45C-482D-853A-FA6860EE7E4E
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aadbd1e71b3c9895b75c973397488472b57f8eb1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548600"
---
# <a name="uploading-texture-data-through-buffers"></a><span data-ttu-id="481e8-103">Chargement de données de texture dans des mémoires tampons</span><span class="sxs-lookup"><span data-stu-id="481e8-103">Uploading Texture Data Through Buffers</span></span>

<span data-ttu-id="481e8-104">Le chargement de données de texture 2D ou 3D est similaire au chargement de données 1D, à ceci près que les applications doivent être plus particulièrement attentifes à l’alignement des données liées au pas à pas.</span><span class="sxs-lookup"><span data-stu-id="481e8-104">Uploading 2D or 3D texture data is similar to uploading 1D data, except that applications need to pay closer attention to data alignment related to row pitch.</span></span> <span data-ttu-id="481e8-105">Les mémoires tampons peuvent être utilisées de façon orthogonale et simultanée à partir de plusieurs parties du pipeline graphique, et sont très flexibles.</span><span class="sxs-lookup"><span data-stu-id="481e8-105">Buffers can be used orthogonally and concurrently from multiple parts of the graphics pipeline, and are very flexible.</span></span>

-   [<span data-ttu-id="481e8-106">Charger les données de texture via des tampons</span><span class="sxs-lookup"><span data-stu-id="481e8-106">Upload Texture Data via Buffers</span></span>](#upload-texture-data-via-buffers)
-   [<span data-ttu-id="481e8-107">Destination</span><span class="sxs-lookup"><span data-stu-id="481e8-107">Copying</span></span>](#copying)
-   [<span data-ttu-id="481e8-108">Mappage et annulation du mappage</span><span class="sxs-lookup"><span data-stu-id="481e8-108">Mapping and unmapping</span></span>](#mapping-and-unmapping)
-   [<span data-ttu-id="481e8-109">Alignement de la mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="481e8-109">Buffer alignment</span></span>](#buffer-alignment)
-   [<span data-ttu-id="481e8-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="481e8-110">Related topics</span></span>](#related-topics)

## <a name="upload-texture-data-via-buffers"></a><span data-ttu-id="481e8-111">Charger les données de texture via des tampons</span><span class="sxs-lookup"><span data-stu-id="481e8-111">Upload Texture Data via Buffers</span></span>

<span data-ttu-id="481e8-112">Les applications doivent charger des données via [**ID3D12GraphicsCommandList :: CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) ou [**ID3D12GraphicsCommandList :: CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion).</span><span class="sxs-lookup"><span data-stu-id="481e8-112">Applications must upload data via [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) or [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion).</span></span> <span data-ttu-id="481e8-113">Les données de texture sont plus susceptibles d’être plus volumineuses, accessibles à plusieurs reprises et tirent parti de la cohérence améliorée du cache des dispositions de mémoire non linéaires par rapport aux autres données de ressources.</span><span class="sxs-lookup"><span data-stu-id="481e8-113">Texture data is much more likely to be larger, accessed repeatedly, and benefit from the improved cache-coherency of non-linear memory layouts than other resource data.</span></span> <span data-ttu-id="481e8-114">Lorsque les mémoires tampons sont utilisées dans D3D12, les applications disposent d’un contrôle total sur l’emplacement et la disposition des données associées à la copie des données de ressources, à condition que les exigences d’alignement de la mémoire soient respectées.</span><span class="sxs-lookup"><span data-stu-id="481e8-114">When buffers are used in D3D12, applications have full control on data placement and arrangement associated with copying resource data around, as long as the memory alignment requirements are satisfied.</span></span>

<span data-ttu-id="481e8-115">L’exemple met en évidence l’emplacement où l’application aplatit simplement les données 2D en 1J avant de les placer dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="481e8-115">The sample highlights where the application simply flattens 2D data into 1D before placing it in the buffer.</span></span> <span data-ttu-id="481e8-116">Pour le scénario 2D mipmap, l’application peut aplatir chaque sous-ressource discrètement et rapidement utiliser un algorithme de sous-allocation 1D, ou utiliser une technique de sous-allocation 2D plus complexe pour réduire l’utilisation de la mémoire vidéo.</span><span class="sxs-lookup"><span data-stu-id="481e8-116">For the mipmap 2D scenario, the application can either flatten each sub-resource discretely and quickly use a 1D sub-allocation algorithm, or, use a more complicated 2D sub-allocation technique to minimize video memory utilization.</span></span> <span data-ttu-id="481e8-117">La première technique est censée être utilisée plus souvent, car elle est plus simple.</span><span class="sxs-lookup"><span data-stu-id="481e8-117">The first technique is expected to be used more often as it is simpler.</span></span> <span data-ttu-id="481e8-118">La deuxième technique peut être utile lors de l’empaquetage de données sur un disque ou sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="481e8-118">The second technique may be useful when packing data onto a disk or across a network.</span></span> <span data-ttu-id="481e8-119">Dans les deux cas, l’application doit toujours appeler les API de copie pour chaque sous-ressource.</span><span class="sxs-lookup"><span data-stu-id="481e8-119">In either case, the application must still call the copy APIs for each sub-resource.</span></span>

``` syntax
// Prepare a pBitmap in memory, with bitmapWidth, bitmapHeight, and pixel format of DXGI_FORMAT_B8G8R8A8_UNORM. 
//
// Sub-allocate from the buffer for texture data.
//

D3D12_SUBRESOURCE_FOOTPRINT pitchedDesc = { 0 };
pitchedDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
pitchedDesc.Width = bitmapWidth;
pitchedDesc.Height = bitmapHeight;
pitchedDesc.Depth = 1;
pitchedDesc.RowPitch = Align(bitmapWidth * sizeof(DWORD), D3D12_TEXTURE_DATA_PITCH_ALIGNMENT);

//
// Note that the helper function UpdateSubresource in D3DX12.h, and ID3D12Device::GetCopyableFootprints 
// can help applications fill out D3D12_SUBRESOURCE_FOOTPRINT and D3D12_PLACED_SUBRESOURCE_FOOTPRINT structures.
//
// Refer to the D3D12 Code example for the previous section "Uploading Different Types of Resources"
// for the code for SuballocateFromBuffer.
//

SuballocateFromBuffer(
    pitchedDesc.Height * pitchedDesc.RowPitch,
    D3D12_TEXTURE_DATA_PLACEMENT_ALIGNMENT
    );

D3D12_PLACED_SUBRESOURCE_FOOTPRINT placedTexture2D = { 0 };
placedTexture2D.Offset = m_pDataCur – m_pDataBegin;
placedTexture2D.Footprint = pitchedDesc;

//
// Copy texture data from DWORD* pBitmap->pixels to the buffer
//

for (UINT y = 0; y < bitmapHeight; y++)
{
  UINT8 *pScan = m_pDataBegin + placedTexture2D.Offset + y * pitchedDesc.RowPitch;
  memcpy( pScan, &(pBitmap->pixels[y * bitmapWidth]), sizeof(DWORD) * bitmapWidth );
}

//
// Create default texture2D resource.
//

D3D12_RESOURCE_DESC  textureDesc { ... };

CComPtr<ID3D12Resource> texture2D;
d3dDevice->CreateCommittedResource( 
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT), 
        D3D12_HEAP_FLAG_NONE, &textureDesc, 
        D3D12_RESOURCE_STATE_COPY_DEST, 
        nullptr, 
        IID_PPV_ARGS(&texture2D) );

//
// Copy heap data to texture2D.
//

commandList->CopyTextureRegion( 
        &CD3DX12_TEXTURE_COPY_LOCATION( texture2D, 0 ), 
        0, 0, 0, 
        &CD3DX12_TEXTURE_COPY_LOCATION( m_spUploadHeap, placedTexture2D ), 
        nullptr );
```

<span data-ttu-id="481e8-120">Notez l’utilisation des structures d’assistance [**CD3DX12 les \_ \_ Propriétés du tas**](cd3dx12-heap-properties.md) et l' [**\_ \_ \_ emplacement de copie de texture CD3DX12**](cd3dx12-texture-copy-location.md), ainsi que les méthodes [**CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) et [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion).</span><span class="sxs-lookup"><span data-stu-id="481e8-120">Note the use of the helper structures [**CD3DX12\_HEAP\_PROPERTIES**](cd3dx12-heap-properties.md) and [**CD3DX12\_TEXTURE\_COPY\_LOCATION**](cd3dx12-texture-copy-location.md), and the methods [**CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) and [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion).</span></span>

## <a name="copying"></a><span data-ttu-id="481e8-121">Copie</span><span class="sxs-lookup"><span data-stu-id="481e8-121">Copying</span></span>

<span data-ttu-id="481e8-122">Les méthodes D3D12 permettent aux applications de remplacer D3D11 [**UpdateSubresource**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource), [**CopySubresourceRegion**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copysubresourceregion)et les données initiales des ressources.</span><span class="sxs-lookup"><span data-stu-id="481e8-122">D3D12 methods enable applications to replace D3D11 [**UpdateSubresource**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource), [**CopySubresourceRegion**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copysubresourceregion), and resource initial data.</span></span> <span data-ttu-id="481e8-123">Une sous-ressource 3D unique de données de texture de ligne principale peut se trouver dans les ressources de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="481e8-123">A single 3D subresource worth of row-major texture data may be located in buffer resources.</span></span> <span data-ttu-id="481e8-124">[**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) peut copier les données de texture de la mémoire tampon vers une ressource de texture avec une disposition de texture inconnue, et vice versa.</span><span class="sxs-lookup"><span data-stu-id="481e8-124">[**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) can copy that texture data from the buffer to a texture resource with an unknown texture layout, and vice versa.</span></span> <span data-ttu-id="481e8-125">Les applications doivent préférer ce type de technique pour remplir les ressources GPU fréquemment sollicitées, en créant de grandes mémoires tampons dans un tas de chargement lors de la création des ressources GPU fréquemment utilisées dans un segment de mémoire par défaut qui n’a pas d’accès au processeur.</span><span class="sxs-lookup"><span data-stu-id="481e8-125">Applications should prefer this type of technique to populate frequently accessed GPU resources, by creating large buffers in an UPLOAD heap while creating the frequently accessed GPU resources in a DEFAULT heap that has no CPU access.</span></span> <span data-ttu-id="481e8-126">Une telle technique prend en charge efficacement les GPU discrètes et leur grande quantité de mémoire inaccessible par le processeur, sans les architectures UMA les plus courantes.</span><span class="sxs-lookup"><span data-stu-id="481e8-126">Such a technique efficiently supports discrete GPUs and their large amounts of CPU-inaccessible memory, without commonly impairing UMA architectures.</span></span>

<span data-ttu-id="481e8-127">Notez les deux constantes suivantes :</span><span class="sxs-lookup"><span data-stu-id="481e8-127">Note the following two constants:</span></span>

``` syntax
const UINT D3D12_TEXTURE_DATA_PITCH_ALIGNMENT = 256;
const UINT D3D12_TEXTURE_DATA_PLACEMENT_ALIGNMENT = 512;
```

-   [<span data-ttu-id="481e8-128">**Encombrement des sous- \_ ressources D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="481e8-128">**D3D12\_SUBRESOURCE\_FOOTPRINT**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)
-   [<span data-ttu-id="481e8-129">**Encombrement des sous- \_ ressources placé par D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="481e8-129">**D3D12\_PLACED\_SUBRESOURCE\_FOOTPRINT**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)
-   [<span data-ttu-id="481e8-130">**\_Emplacement de \_ copie de texture D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="481e8-130">**D3D12\_TEXTURE\_COPY\_LOCATION**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)
-   [<span data-ttu-id="481e8-131">**\_Type de \_ copie de texture D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="481e8-131">**D3D12\_TEXTURE\_COPY\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type)
-   [<span data-ttu-id="481e8-132">**ID3D12Device :: GetCopyableFootprints**</span><span class="sxs-lookup"><span data-stu-id="481e8-132">**ID3D12Device::GetCopyableFootprints**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)
-   [<span data-ttu-id="481e8-133">**ID3D12GraphicsCommandList::CopyResource**</span><span class="sxs-lookup"><span data-stu-id="481e8-133">**ID3D12GraphicsCommandList::CopyResource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [<span data-ttu-id="481e8-134">**ID3D12GraphicsCommandList::CopyTextureRegion**</span><span class="sxs-lookup"><span data-stu-id="481e8-134">**ID3D12GraphicsCommandList::CopyTextureRegion**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [<span data-ttu-id="481e8-135">**ID3D12GraphicsCommandList::CopyBufferRegion**</span><span class="sxs-lookup"><span data-stu-id="481e8-135">**ID3D12GraphicsCommandList::CopyBufferRegion**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [<span data-ttu-id="481e8-136">**ID3D12GraphicsCommandList::CopyTiles**</span><span class="sxs-lookup"><span data-stu-id="481e8-136">**ID3D12GraphicsCommandList::CopyTiles**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [<span data-ttu-id="481e8-137">**ID3D12CommandQueue::UpdateTileMappings**</span><span class="sxs-lookup"><span data-stu-id="481e8-137">**ID3D12CommandQueue::UpdateTileMappings**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings)

## <a name="mapping-and-unmapping"></a><span data-ttu-id="481e8-138">Mappage et annulation du mappage</span><span class="sxs-lookup"><span data-stu-id="481e8-138">Mapping and unmapping</span></span>

<span data-ttu-id="481e8-139">[**Les**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) mappages et les [**mappages**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) peuvent être appelés par plusieurs threads en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="481e8-139">[**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) and [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) can be called by multiple threads safely.</span></span> <span data-ttu-id="481e8-140">Le premier appel à **Map** alloue une plage d’adresses virtuelles de processeur pour la ressource.</span><span class="sxs-lookup"><span data-stu-id="481e8-140">The first call to **Map** allocates a CPU virtual address range for the resource.</span></span> <span data-ttu-id="481e8-141">Le dernier appel à la valeur de **mappage** libère la plage d’adresses virtuelles de l’UC.</span><span class="sxs-lookup"><span data-stu-id="481e8-141">The last call to **Unmap** deallocates the CPU virtual address range.</span></span> <span data-ttu-id="481e8-142">L’adresse virtuelle de l’UC est généralement retournée à l’application.</span><span class="sxs-lookup"><span data-stu-id="481e8-142">The CPU virtual address is commonly returned to the application.</span></span>

<span data-ttu-id="481e8-143">Chaque fois que des données sont transmises entre l’UC et le GPU via des ressources dans des segments de mémoire readback, [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) et [**DEMAPPAGE**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) doivent être utilisés pour prendre en charge tous les systèmes D3D12 est pris en charge sur.</span><span class="sxs-lookup"><span data-stu-id="481e8-143">Whenever data is passed between the CPU and GPU through resources in readback heaps, [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) and [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) must be used to support all systems D3D12 is supported on.</span></span> <span data-ttu-id="481e8-144">Conserver les plages aussi fortes que possible optimise l’efficacité sur les systèmes qui requièrent des plages (consultez la [**\_ page D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)).</span><span class="sxs-lookup"><span data-stu-id="481e8-144">Keeping the ranges as tight as possible maximizes efficiency on the systems that require ranges (refer to [**D3D12\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)).</span></span>

<span data-ttu-id="481e8-145">Les performances des outils de débogage bénéficient non seulement de l’utilisation précise des plages sur tous les appels de [**mappage de mappage**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)  /  [](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) , mais également des applications qui démappent les ressources lorsque les modifications de l’UC ne sont plus effectuées.</span><span class="sxs-lookup"><span data-stu-id="481e8-145">The performance of debugging tools benefit not only from the accurate usage of ranges on all [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) / [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) calls, but also from applications unmapping resources when CPU modifications will no longer be made.</span></span>

<span data-ttu-id="481e8-146">La méthode D3D11 de l’utilisation de [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (avec le paramètre de rejet défini) pour renommer des ressources n’est pas prise en charge dans D3D12.</span><span class="sxs-lookup"><span data-stu-id="481e8-146">The D3D11 method of using [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (with the DISCARD parameter set) to rename resources is not supported in D3D12.</span></span> <span data-ttu-id="481e8-147">Les applications doivent implémenter le changement de nom des ressources.</span><span class="sxs-lookup"><span data-stu-id="481e8-147">Applications must implement resource renaming themselves.</span></span> <span data-ttu-id="481e8-148">Tous les appels **Map** ne sont IMPLICITement pas des \_ remplacements et des threads multithread.</span><span class="sxs-lookup"><span data-stu-id="481e8-148">All **Map** calls are implicitly NO\_OVERWRITE and multi-threaded.</span></span> <span data-ttu-id="481e8-149">Il incombe à l’application de s’assurer que tout travail GPU approprié contenu dans les listes de commandes est terminé avant l’accès aux données avec le processeur.</span><span class="sxs-lookup"><span data-stu-id="481e8-149">It is the application’s responsibility to ensure that any relevant GPU work contained in command lists is finished before the accessing data with the CPU.</span></span> <span data-ttu-id="481e8-150">Les appels D3D12 à **Map** ne vident pas implicitement les mémoires tampons de commande et ne bloquent pas l’attente de la fin du travail du GPU.</span><span class="sxs-lookup"><span data-stu-id="481e8-150">D3D12 calls to **Map** do not implicitly flush any command buffers, nor do they block waiting for the GPU to finish work.</span></span> <span data-ttu-id="481e8-151">Par conséquent, le **mappage** et le [**mappage peuvent même**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) être optimisés dans certains scénarios.</span><span class="sxs-lookup"><span data-stu-id="481e8-151">As a result, **Map** and [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) may even be optimized out in some scenarios.</span></span>

## <a name="buffer-alignment"></a><span data-ttu-id="481e8-152">Alignement de la mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="481e8-152">Buffer alignment</span></span>

<span data-ttu-id="481e8-153">Restrictions d’alignement de mémoire tampon :</span><span class="sxs-lookup"><span data-stu-id="481e8-153">Buffer alignment restrictions:</span></span>

-   <span data-ttu-id="481e8-154">La copie linéaire des sous-ressources doit être alignée sur 512 octets (avec le pas de la ligne aligné sur les octets d’alignement du pas de \_ données de texture D3D12 \_ \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="481e8-154">Linear subresource copying must be aligned to 512 bytes (with the row pitch aligned to D3D12\_TEXTURE\_DATA\_PITCH\_ALIGNMENT bytes).</span></span>
-   <span data-ttu-id="481e8-155">Les lectures de données constantes doivent être un multiple de 256 octets à partir du début du tas (c’est-à-dire uniquement des adresses qui sont alignées sur 256 octets).</span><span class="sxs-lookup"><span data-stu-id="481e8-155">Constant data reads must be a multiple of 256 bytes from the beginning of the heap (i.e. only from addresses that are 256-byte aligned).</span></span>
-   <span data-ttu-id="481e8-156">Les lectures de données d’index doivent être un multiple de la taille de type de données d’index (c’est-à-dire uniquement à partir d’adresses qui sont naturellement alignées pour les données).</span><span class="sxs-lookup"><span data-stu-id="481e8-156">Index data reads must be a multiple of the index data type size (i.e. only from addresses that are naturally aligned for the data).</span></span>
-   <span data-ttu-id="481e8-157">[**ID3D12GraphicsCommandList ::D rawinstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) et [**ID3D12GraphicsCommandList ::D données rawindexedinstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced) doivent provenir de décalages multiples de 4 (c’est-à-dire uniquement à partir d’adresses qui sont alignées sur des DWORD).</span><span class="sxs-lookup"><span data-stu-id="481e8-157">[**ID3D12GraphicsCommandList::DrawInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) and [**ID3D12GraphicsCommandList::DrawIndexedInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced) data must be from offsets that are multiples of 4 (i.e. only from addresses that are DWORD aligned).</span></span>

## <a name="related-topics"></a><span data-ttu-id="481e8-158">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="481e8-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="481e8-159">Sous-allocation dans des mémoires tampons</span><span class="sxs-lookup"><span data-stu-id="481e8-159">Suballocation Within Buffers</span></span>](large-buffers.md)
</dt> </dl>

 

 