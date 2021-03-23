---
title: Téléchargement de différents types de ressources
description: Montre comment utiliser une mémoire tampon pour télécharger à la fois des données de mémoire tampon constantes et des données de mémoire tampon de vertex vers le GPU, et comment les sous-allouer et placer des données dans des mémoires tampons.
ms.assetid: 255B0482-21D6-4276-8009-3F3891879CA1
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd2edca2cd9f4d3becf5036056a89f91c50f2c24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103712"
---
# <a name="uploading-different-types-of-resources"></a><span data-ttu-id="9dae3-103">Téléchargement de différents types de ressources</span><span class="sxs-lookup"><span data-stu-id="9dae3-103">Uploading Different Types of Resources</span></span>

<span data-ttu-id="9dae3-104">Montre comment utiliser une mémoire tampon pour télécharger à la fois des données de mémoire tampon constantes et des données de mémoire tampon de vertex vers le GPU, et comment les sous-allouer et placer des données dans des mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="9dae3-104">Shows how to use one buffer to upload both constant buffer data and vertex buffer data to the GPU, and how to properly sub-allocate and place data within buffers.</span></span> <span data-ttu-id="9dae3-105">L’utilisation d’une seule mémoire tampon augmente la flexibilité de l’utilisation de la mémoire et fournit aux applications un contrôle plus étroit de l’utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="9dae3-105">The use of one single buffer increases memory usage flexibility and provides applications with tighter control of memory usage.</span></span> <span data-ttu-id="9dae3-106">Montre également les différences entre les modèles D3D11 et D3D12 pour le téléchargement de différents types de ressources.</span><span class="sxs-lookup"><span data-stu-id="9dae3-106">Also shows the differences between the D3D11 and D3D12 models for uploading different types of resources.</span></span>

-   [<span data-ttu-id="9dae3-107">Télécharger différents types de ressources</span><span class="sxs-lookup"><span data-stu-id="9dae3-107">Upload Different Types of Resources</span></span>](#upload-different-types-of-resources)
    -   [<span data-ttu-id="9dae3-108">Exemple de code : D3D11</span><span class="sxs-lookup"><span data-stu-id="9dae3-108">Code Example: D3D11</span></span>](#code-example-d3d11)
    -   [<span data-ttu-id="9dae3-109">Exemple de code : D3D12</span><span class="sxs-lookup"><span data-stu-id="9dae3-109">Code Example: D3D12</span></span>](#code-example-d3d12)
-   [<span data-ttu-id="9dae3-110">Constantes</span><span class="sxs-lookup"><span data-stu-id="9dae3-110">Constants</span></span>](#constants)
-   [<span data-ttu-id="9dae3-111">Ressources</span><span class="sxs-lookup"><span data-stu-id="9dae3-111">Resources</span></span>](#uploading-different-types-of-resources)
-   [<span data-ttu-id="9dae3-112">Réflexion de la taille des ressources</span><span class="sxs-lookup"><span data-stu-id="9dae3-112">Resource size reflection</span></span>](#resource-size-reflection)
-   [<span data-ttu-id="9dae3-113">Alignement de la mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="9dae3-113">Buffer alignment</span></span>](#buffer-alignment)
-   [<span data-ttu-id="9dae3-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9dae3-114">Related topics</span></span>](#related-topics)

## <a name="upload-different-types-of-resources"></a><span data-ttu-id="9dae3-115">Télécharger différents types de ressources</span><span class="sxs-lookup"><span data-stu-id="9dae3-115">Upload Different Types of Resources</span></span>

<span data-ttu-id="9dae3-116">Dans D3D12, les applications créent une mémoire tampon pour prendre en charge différents types de données de ressources pour le téléchargement, et copient les données de ressources dans le même tampon d’une façon similaire pour différentes données de ressource.</span><span class="sxs-lookup"><span data-stu-id="9dae3-116">In D3D12, applications create one buffer to accommodate different types of resource data for uploading, and copy resource data to the same buffer in a similar way for different resource data.</span></span> <span data-ttu-id="9dae3-117">Des vues individuelles sont ensuite créées pour lier ces données de ressource au pipeline Graphics dans le nouveau modèle de liaison de ressources.</span><span class="sxs-lookup"><span data-stu-id="9dae3-117">Individual views are then created to bind those resource data to the graphics pipeline in the new resource binding model.</span></span>

<span data-ttu-id="9dae3-118">Dans D3D11, les applications créent des mémoires tampons distinctes pour différents types de données de ressource (Notez les différentes `BindFlags` utilisées dans l’exemple de code d3d11 ci-dessous), en liant explicitement chaque mémoire tampon de ressources au pipeline graphique, et mettent à jour les données de ressources avec différentes méthodes en fonction de différents types de ressources.</span><span class="sxs-lookup"><span data-stu-id="9dae3-118">In D3D11, applications create separate buffers for different types of resource data (note the different `BindFlags` used in the D3D11 sample code below), explicitly binding each resource buffer to the graphics pipeline, and update the resource data with different methods based on different resource types.</span></span>

<span data-ttu-id="9dae3-119">Dans D3D12 et D3D11, les applications doivent uniquement utiliser des ressources de téléchargement où l’UC écrira les données une seule fois et le GPU les lira une fois.</span><span class="sxs-lookup"><span data-stu-id="9dae3-119">In both D3D12 and D3D11, applications should only use upload resources where the CPU will write the data once and the GPU will read it once.</span></span> <span data-ttu-id="9dae3-120">Si le GPU lit les données plusieurs fois, le GPU ne lit pas les données de manière linéaire, ou le rendu est déjà limité au GPU.</span><span class="sxs-lookup"><span data-stu-id="9dae3-120">If the GPU will read the data multiple times, the GPU will not read the data linearly, or the rendering is significantly GPU-limited already.</span></span> <span data-ttu-id="9dae3-121">La meilleure option consiste à utiliser [**ID3D12GraphicsCommandList :: CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) ou [**ID3D12GraphicsCommandList :: CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) pour copier les données de mémoire tampon de chargement dans une ressource par défaut.</span><span class="sxs-lookup"><span data-stu-id="9dae3-121">The better option may be to use [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) or [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) to copy the upload buffer data to a default resource.</span></span> <span data-ttu-id="9dae3-122">Une ressource par défaut peut résider dans la mémoire vidéo physique sur des GPU discrètes.</span><span class="sxs-lookup"><span data-stu-id="9dae3-122">A default resource can reside in physical video memory on discrete GPUs.</span></span>

### <a name="code-example-d3d11"></a><span data-ttu-id="9dae3-123">Exemple de code : D3D11</span><span class="sxs-lookup"><span data-stu-id="9dae3-123">Code Example: D3D11</span></span>

``` syntax
// D3D11: Separate buffers for each resource type.

void main()
{
    // ...

    // Create a constant buffer.
    float constantBufferData[] = ...;

    D3D11_BUFFER_DESC constantBufferDesc = {0};  
    constantBufferDesc.ByteWidth = sizeof(constantBufferData);  
    constantBufferDesc.Usage = D3D11_USAGE_DYNAMIC;  
    constantBufferDesc.BindFlags = D3D11_BIND_CONSTANT_BUFFER;  
    constantBufferDesc.CPUAccessFlags = D3D11_CPU_ACCESS_WRITE;  

    ComPtr<ID3D11Buffer> constantBuffer;
    d3dDevice->CreateBuffer(  
        &constantBufferDesc,  
        NULL,
        &constantBuffer  
        );

    // Create a vertex buffer.
    float vertexBufferData[] = ...;

    D3D11_BUFFER_DESC vertexBufferDesc = { 0 };
    vertexBufferDesc.ByteWidth = sizeof(vertexBufferData);
    vertexBufferDesc.Usage = D3D11_USAGE_DYNAMIC;
    vertexBufferDesc.BindFlags = D3D11_BIND_VERTEX_BUFFER;

    ComPtr<ID3D11Buffer> vertexBuffer;
    d3dDevice->CreateBuffer(
        &vertexBufferDesc,
        NULL,
        &vertexBuffer
        );

    // ...
}

void DrawFrame()
{
    // ...

    // Bind buffers to the graphics pipeline.
    d3dDeviceContext->VSSetConstantBuffers(0, 1, constantBuffer.Get());
    d3dDeviceContext->IASetVertexBuffers(0, 1, vertexBuffer.Get(), ...);

    // Update the constant buffer.
    D3D11_MAPPED_SUBRESOURCE mappedResource;  
    d3dDeviceContext->Map(
        constantBuffer.Get(),
        0, 
        D3D11_MAP_WRITE_DISCARD,
        0,
        &mappedResource
        );
    memcpy(mappedResource.pData, constantBufferData,
        sizeof(contatnBufferData));
    d3dDeviceContext->Unmap(constantBuffer.Get(), 0);  

    // Update the vertex buffer.
    d3dDeviceContext->UpdateSubresource(
        vertexBuffer.Get(),
        0,
        NULL,
        vertexBufferData,
        sizeof(vertexBufferData),
        0
    );

    // ...
}
```

### <a name="code-example-d3d12"></a><span data-ttu-id="9dae3-124">Exemple de code : D3D12</span><span class="sxs-lookup"><span data-stu-id="9dae3-124">Code Example: D3D12</span></span>

``` syntax
// D3D12: One buffer to accommodate different types of resources

ComPtr<ID3D12Resource> m_spUploadBuffer;
UINT8* m_pDataBegin = nullptr;    // starting position of upload buffer
UINT8* m_pDataCur = nullptr;      // current position of upload buffer
UINT8* m_pDataEnd = nullptr;      // ending position of upload buffer

void main()
{
    //
    // Initialize an upload buffer
    //

    InitializeUploadBuffer(64 * 1024);

    // ...
}

void DrawFrame()
{
    // ...

    // Set vertices data to the upload buffer.

    float vertices[] = ...;
    UINT verticesOffset = 0;
    ThrowIfFailed(
        SetDataToUploadBuffer(
            vertices, sizeof(float), sizeof(vertices) / sizeof(float),
            sizeof(float), 
            verticesOffset
            ));

    // Set constant data to the upload buffer.

    float constants[] = ...;
    UINT constantsOffset = 0;
    ThrowIfFailed(
        SetDataToUploadBuffer(
            constants, sizeof(float), sizeof(constants) / sizeof(float), 
            D3D12_CONSTANT_BUFFER_DATA_PLACEMENT_ALIGNMENT, 
            constantsOffset
            ));

    // Create vertex buffer views for the new binding model.

    D3D12_VERTEX_BUFFER_VIEW vertexBufferViewDesc = {
        m_spUploadBuffer->GetGPUVirtualAddress() + verticesOffset,
        sizeof(vertices), // size
        sizeof(float) * 4,  // stride
    };

    commandList->IASetVertexBuffers( 
        0,
        1,
        &vertexBufferViewDesc,
        ));

    // Create constant buffer views for the new binding model.

    D3D12_CONSTANT_BUFFER_VIEW_DESC constantBufferViewDesc = {
        m_spUploadBuffer->GetGPUVirtualAddress() + constantsOffset,
        sizeof(constants) // size
         };

    d3dDevice->CreateConstantBufferView(
        &constantBufferViewDesc,
        ...
        ));

    // Continue command list building and execution ...
}

//
// Create an upload buffer and keep it always mapped.
//

HRESULT InitializeUploadBuffer(SIZE_T uSize)
{
    HRESULT hr = d3dDevice->CreateCommittedResource(
         &CD3DX12_HEAP_PROPERTIES( D3D12_HEAP_TYPE_UPLOAD ),    
               D3D12_HEAP_FLAG_NONE, 
               &CD3DX12_RESOURCE_DESC::Buffer( uSize ), 
               D3D12_RESOURCE_STATE_GENERIC_READ, nullptr,  
               IID_PPV_ARGS( &m_spUploadBuffer ) );

    if (SUCCEEDED(hr))
    {
        void* pData;
        //
        // No CPU reads will be done from the resource.
        //
        CD3DX12_RANGE readRange(0, 0);
        m_spUploadBuffer->Map( 0, &readRange, &pData ); 
        m_pDataCur = m_pDataBegin = reinterpret_cast< UINT8* >( pData );
        m_pDataEnd = m_pDataBegin + uSize;
    }
    return hr;
}

//
// Sub-allocate from the buffer, with offset aligned.
//

HRESULT SuballocateFromBuffer(SIZE_T uSize, UINT uAlign)
{
    m_pDataCur = reinterpret_cast< UINT8* >(
        Align(reinterpret_cast< SIZE_T >(m_pDataCur), uAlign)
        );

    return (m_pDataCur + uSize > m_pDataEnd) ? E_INVALIDARG : S_OK;
}

//
// Place and copy data to the upload buffer.
//

HRESULT SetDataToUploadBuffer(
    const void* pData, 
    UINT bytesPerData, 
    UINT dataCount, 
    UINT alignment, 
    UINT& byteOffset
    )
{
    SIZE_T byteSize = bytesPerData * dataCount;
    HRESULT hr = SuballocateFromBuffer(byteSize, alignment);
    if (SUCCEEDED(hr))
    {
        byteOffset = UINT(m_pDataCur - m_pDataBegin);
        memcpy(m_pDataCur, pData, byteSize); 
        m_pDataCur += byteSize;
    }
    return hr;
}

//
// Align uLocation to the next multiple of uAlign.
//

UINT Align(UINT uLocation, UINT uAlign)
{
    if ( (0 == uAlign) || (uAlign & (uAlign-1)) )
    {
        ThrowException("non-pow2 alignment");
    }

    return ( (uLocation + (uAlign-1)) & ~(uAlign-1) );
}
```

<span data-ttu-id="9dae3-125">Notez l’utilisation des structures d’assistance [**CD3DX12 les \_ \_ Propriétés du tas**](cd3dx12-heap-properties.md) et la description de la [**\_ ressource \_ CD3DX12**](cd3dx12-resource-desc.md).</span><span class="sxs-lookup"><span data-stu-id="9dae3-125">Note the use of the helper structures [**CD3DX12\_HEAP\_PROPERTIES**](cd3dx12-heap-properties.md) and [**CD3DX12\_RESOURCE\_DESC**](cd3dx12-resource-desc.md).</span></span>

## <a name="constants"></a><span data-ttu-id="9dae3-126">Constantes</span><span class="sxs-lookup"><span data-stu-id="9dae3-126">Constants</span></span>

<span data-ttu-id="9dae3-127">Pour définir des constantes, des vertex et des index dans un segment de mémoire de chargement ou readback, utilisez les API suivantes :</span><span class="sxs-lookup"><span data-stu-id="9dae3-127">To set constants, vertices and indexes within an Upload or Readback heap, use the following APIs:</span></span>

-   [<span data-ttu-id="9dae3-128">**ID3D12Device::CreateConstantBufferView**</span><span class="sxs-lookup"><span data-stu-id="9dae3-128">**ID3D12Device::CreateConstantBufferView**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
-   [<span data-ttu-id="9dae3-129">**ID3D12GraphicsCommandList::IASetVertexBuffers**</span><span class="sxs-lookup"><span data-stu-id="9dae3-129">**ID3D12GraphicsCommandList::IASetVertexBuffers**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)
-   [<span data-ttu-id="9dae3-130">**ID3D12GraphicsCommandList::IASetIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="9dae3-130">**ID3D12GraphicsCommandList::IASetIndexBuffer**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer)

## <a name="resources"></a><span data-ttu-id="9dae3-131">Ressources</span><span class="sxs-lookup"><span data-stu-id="9dae3-131">Resources</span></span>

<span data-ttu-id="9dae3-132">Les ressources sont le concept D3D qui soustrait l’utilisation de la mémoire physique GPU.</span><span class="sxs-lookup"><span data-stu-id="9dae3-132">Resources are the D3D concept which abstracts the usage of GPU physical memory.</span></span> <span data-ttu-id="9dae3-133">Les ressources requièrent un espace d’adressage virtuel GPU pour accéder à la mémoire physique.</span><span class="sxs-lookup"><span data-stu-id="9dae3-133">Resources require GPU virtual address space to access physical memory.</span></span> <span data-ttu-id="9dae3-134">La création de ressources est libre de threads.</span><span class="sxs-lookup"><span data-stu-id="9dae3-134">Resource creation is free-threaded.</span></span>

<span data-ttu-id="9dae3-135">Il existe trois types de ressources en ce qui concerne la création d’adresses virtuelles et la flexibilité dans D3D12 :</span><span class="sxs-lookup"><span data-stu-id="9dae3-135">There are three types of resources with respect to virtual address creation and flexibility in D3D12:</span></span>

-   <span data-ttu-id="9dae3-136">Ressources validées</span><span class="sxs-lookup"><span data-stu-id="9dae3-136">Committed resources</span></span>

    <span data-ttu-id="9dae3-137">Les ressources validées sont l’idée la plus courante des ressources D3D sur les générations.</span><span class="sxs-lookup"><span data-stu-id="9dae3-137">Committed resources are the most common idea of D3D resources over the generations.</span></span> <span data-ttu-id="9dae3-138">La création d’une telle ressource alloue de la plage d’adresses virtuelles, un tas implicite suffisamment grand pour s’ajuster à la ressource entière et valide la plage d’adresses virtuelles dans la mémoire physique encapsulée par le tas.</span><span class="sxs-lookup"><span data-stu-id="9dae3-138">Creating such a resource allocates virtual address range, an implicit heap large enough to fit the whole resource, and commits the virtual address range to the physical memory encapsulated by the heap.</span></span> <span data-ttu-id="9dae3-139">Les propriétés de tas implicites doivent être passées pour correspondre à la parité fonctionnelle avec les versions D3D précédentes.</span><span class="sxs-lookup"><span data-stu-id="9dae3-139">The implicit heap properties must be passed to match functional parity with previous D3D versions.</span></span> <span data-ttu-id="9dae3-140">Reportez-vous à [**ID3D12Device :: CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span><span class="sxs-lookup"><span data-stu-id="9dae3-140">Refer to [**ID3D12Device::CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span></span>

-   <span data-ttu-id="9dae3-141">Ressources réservées</span><span class="sxs-lookup"><span data-stu-id="9dae3-141">Reserved resources</span></span>

    <span data-ttu-id="9dae3-142">Les ressources réservées sont équivalentes aux ressources en mosaïque D3D11.</span><span class="sxs-lookup"><span data-stu-id="9dae3-142">Reserved resources are equivalent to D3D11 tiled resources.</span></span> <span data-ttu-id="9dae3-143">Lors de leur création, seule une plage d’adresses virtuelles est allouée et n’est pas mappée à un segment de mémoire.</span><span class="sxs-lookup"><span data-stu-id="9dae3-143">On their creation, only a virtual address range is allocated and not mapped to any heap.</span></span> <span data-ttu-id="9dae3-144">L’application mappera ces ressources aux tas ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="9dae3-144">The application will map such resources to heaps later.</span></span> <span data-ttu-id="9dae3-145">Les fonctionnalités de ces ressources sont actuellement inchangées par rapport à D3D11, car elles peuvent être mappées à un segment de mémoire avec une granularité de mosaïque de 64 Ko avec [**UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings).</span><span class="sxs-lookup"><span data-stu-id="9dae3-145">The capabilities of such resources are currently unchanged over D3D11, as they can be mapped to a heap at a 64KB tile granularity with [**UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings).</span></span> <span data-ttu-id="9dae3-146">Reportez-vous à [ **ID3D12Device :: CreateReservedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource)</span><span class="sxs-lookup"><span data-stu-id="9dae3-146">Refer to [**ID3D12Device::CreateReservedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource)</span></span>

-   <span data-ttu-id="9dae3-147">Ressources placées</span><span class="sxs-lookup"><span data-stu-id="9dae3-147">Placed resources</span></span>

    <span data-ttu-id="9dae3-148">Nouveauté de D3D12, les applications peuvent créer des tas distincts des ressources.</span><span class="sxs-lookup"><span data-stu-id="9dae3-148">New for D3D12, applications may create heaps separate from resources.</span></span> <span data-ttu-id="9dae3-149">Par la suite, l’application peut localiser plusieurs ressources dans un seul segment de mémoire.</span><span class="sxs-lookup"><span data-stu-id="9dae3-149">Afterward, the application may locate multiple resources within a single heap.</span></span> <span data-ttu-id="9dae3-150">Cela peut être effectué sans créer de ressources en mosaïque ou réservées, ce qui permet d’activer les fonctionnalités de tous les types de ressources qui peuvent être créés directement par les applications.</span><span class="sxs-lookup"><span data-stu-id="9dae3-150">This can be done without creating tiled or reserved resources, enabling the capabilities for all resource types able to be created directly by applications.</span></span> <span data-ttu-id="9dae3-151">Plusieurs ressources peuvent se chevaucher, et l’application doit utiliser `TiledResourceBarrier` pour réutiliser la mémoire physique correctement.</span><span class="sxs-lookup"><span data-stu-id="9dae3-151">Multiple resources may overlap, and the application must use the `TiledResourceBarrier` to re-use physical memory correctly.</span></span> <span data-ttu-id="9dae3-152">Reportez-vous à [ **ID3D12Device :: CreatePlacedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource)</span><span class="sxs-lookup"><span data-stu-id="9dae3-152">Refer to [**ID3D12Device::CreatePlacedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource)</span></span>

## <a name="resource-size-reflection"></a><span data-ttu-id="9dae3-153">Réflexion de la taille des ressources</span><span class="sxs-lookup"><span data-stu-id="9dae3-153">Resource size reflection</span></span>

<span data-ttu-id="9dae3-154">Les applications doivent utiliser la réflexion de la taille des ressources pour comprendre la quantité de textures de la pièce avec des dispositions de texture inconnues qui requièrent dans les tas.</span><span class="sxs-lookup"><span data-stu-id="9dae3-154">Applications must use resource size reflection to understand how much room textures with unknown texture layouts require in heaps.</span></span> <span data-ttu-id="9dae3-155">Les mémoires tampons sont également prises en charge, mais principalement par commodité.</span><span class="sxs-lookup"><span data-stu-id="9dae3-155">Buffers are also supported, but mostly as a convenience.</span></span>

<span data-ttu-id="9dae3-156">Les applications doivent être conscientes des différences d’alignement majeures, afin d’aider à regrouper les ressources de façon plus dense.</span><span class="sxs-lookup"><span data-stu-id="9dae3-156">Applications should be aware of major alignment discrepancies, to help pack resources more densely.</span></span>

<span data-ttu-id="9dae3-157">Par exemple, un tableau à un seul élément avec une mémoire tampon d’un octet retourne une taille de 64 Ko et un alignement de 64 Ko, car les mémoires tampons ne peuvent actuellement être alignées que de 64 Ko.</span><span class="sxs-lookup"><span data-stu-id="9dae3-157">For example, a single-element array with a one-byte-buffer returns a Size of 64KB and an Alignment of 64KB, as buffers currently can only be 64KB aligned.</span></span>

<span data-ttu-id="9dae3-158">En outre, un tableau à trois éléments avec deux textures alignées de 64 Ko à texture unique et une texture alignée de 4 Mo à Texel unique signale des tailles différentes en fonction de l’ordre du tableau.</span><span class="sxs-lookup"><span data-stu-id="9dae3-158">Also, a three element array with two single-texel 64KB aligned textures and a single-texel 4MB aligned texture reports differing sizes based on the order of the array.</span></span> <span data-ttu-id="9dae3-159">Si les textures alignées de 4 Mo sont en milieu, la taille obtenue est 12 Mo.</span><span class="sxs-lookup"><span data-stu-id="9dae3-159">If the 4MB aligned textures is in the middle, the resulting Size is 12MB.</span></span> <span data-ttu-id="9dae3-160">Dans le cas contraire, la taille obtenue est de 8 Mo.</span><span class="sxs-lookup"><span data-stu-id="9dae3-160">Otherwise, the resulting Size is 8MB.</span></span> <span data-ttu-id="9dae3-161">L’alignement retourné est toujours de 4 Mo, le super-ensemble de tous les alignements dans le tableau de ressources.</span><span class="sxs-lookup"><span data-stu-id="9dae3-161">The Alignment returned would always be 4MB, the super-set of all alignments in the resource array.</span></span>

<span data-ttu-id="9dae3-162">Référencez les API suivantes :</span><span class="sxs-lookup"><span data-stu-id="9dae3-162">Reference the following APIs:</span></span>

-   [<span data-ttu-id="9dae3-163">**\_Informations d' \_ allocation de ressources D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="9dae3-163">**D3D12\_RESOURCE\_ALLOCATION\_INFO**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
-   [<span data-ttu-id="9dae3-164">**GetResourceAllocationInfo**</span><span class="sxs-lookup"><span data-stu-id="9dae3-164">**GetResourceAllocationInfo**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)

## <a name="buffer-alignment"></a><span data-ttu-id="9dae3-165">Alignement de la mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="9dae3-165">Buffer alignment</span></span>

<span data-ttu-id="9dae3-166">Les restrictions d’alignement de mémoire tampon n’ont pas changé par rapport à D3D11, notamment :</span><span class="sxs-lookup"><span data-stu-id="9dae3-166">Buffer alignment restrictions have not changed from D3D11, notably:</span></span>

-   <span data-ttu-id="9dae3-167">4 Mo pour les textures à échantillons multiples.</span><span class="sxs-lookup"><span data-stu-id="9dae3-167">4 MB for multi-sample textures.</span></span>
-   <span data-ttu-id="9dae3-168">64 Ko pour les textures et les mémoires tampons d’échantillon simple.</span><span class="sxs-lookup"><span data-stu-id="9dae3-168">64 KB for single-sample textures and buffers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9dae3-169">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9dae3-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9dae3-170">Sous-allocation dans des mémoires tampons</span><span class="sxs-lookup"><span data-stu-id="9dae3-170">Suballocation Within Buffers</span></span>](large-buffers.md)
</dt> </dl>

 

 




