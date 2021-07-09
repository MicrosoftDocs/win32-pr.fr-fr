---
title: Téléchargement de différents types de ressources
description: Montre comment utiliser une mémoire tampon pour télécharger à la fois des données de mémoire tampon constantes et des données de mémoire tampon de vertex vers le GPU, et comment les sous-allouer et placer des données dans des mémoires tampons.
ms.assetid: 255B0482-21D6-4276-8009-3F3891879CA1
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03d4755124bbadcdd255a6e99739b710845ab14
ms.sourcegitcommit: a30d0436a84986234df673c6def6694d5a8579f6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113563779"
---
# <a name="uploading-different-types-of-resources"></a><span data-ttu-id="590ce-103">Téléchargement de différents types de ressources</span><span class="sxs-lookup"><span data-stu-id="590ce-103">Uploading different types of resources</span></span>

<span data-ttu-id="590ce-104">Montre comment utiliser une mémoire tampon pour télécharger à la fois des données de mémoire tampon constantes et des données de mémoire tampon de vertex vers le GPU, et comment les sous-allouer et placer des données dans des mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="590ce-104">Shows how to use one buffer to upload both constant buffer data and vertex buffer data to the GPU, and how to properly sub-allocate and place data within buffers.</span></span> <span data-ttu-id="590ce-105">L’utilisation d’une seule mémoire tampon augmente la flexibilité de l’utilisation de la mémoire et fournit aux applications un contrôle plus étroit de l’utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="590ce-105">The use of a single buffer increases memory usage flexibility, and provides applications with tighter control over memory usage.</span></span> <span data-ttu-id="590ce-106">Montre également les différences entre les modèles Direct3D 11 et Direct3D 12 pour le téléchargement de différents types de ressources.</span><span class="sxs-lookup"><span data-stu-id="590ce-106">Also shows the differences between the Direct3D 11 and Direct3D 12 models for uploading different types of resources.</span></span>

## <a name="upload-different-types-of-resources"></a><span data-ttu-id="590ce-107">Télécharger différents types de ressources</span><span class="sxs-lookup"><span data-stu-id="590ce-107">Upload different types of resources</span></span>

<span data-ttu-id="590ce-108">Dans Direct3D 12, vous créez une mémoire tampon pour prendre en charge différents types de données de ressources pour le téléchargement, et vous copiez les données de ressources dans le même tampon d’une façon similaire pour différentes données de ressource.</span><span class="sxs-lookup"><span data-stu-id="590ce-108">In Direct3D 12, you create one buffer to accommodate different types of resource data for uploading, and you copy resource data to the same buffer in a similar way for different resource data.</span></span> <span data-ttu-id="590ce-109">Des vues individuelles sont ensuite créées pour lier ces données de ressource au pipeline Graphics dans le modèle de liaison de ressource Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="590ce-109">Individual views are then created to bind those resource data to the graphics pipeline in the Direct3D 12 resource binding model.</span></span>

<span data-ttu-id="590ce-110">Dans Direct3D 11, vous créez des mémoires tampons distinctes pour différents types de données de ressource (Notez les différentes `BindFlags` utilisées dans l’exemple de code Direct3D 11 ci-dessous), en liant explicitement chaque mémoire tampon de ressources au pipeline graphique, et en actualisant les données de ressources avec différentes méthodes en fonction de différents types de ressources.</span><span class="sxs-lookup"><span data-stu-id="590ce-110">In Direct3D 11, you create separate buffers for different types of resource data (note the different `BindFlags` used in the Direct3D 11 sample code below), explicitly binding each resource buffer to the graphics pipeline, and update the resource data with different methods based on different resource types.</span></span>

<span data-ttu-id="590ce-111">Dans Direct3D 12 et Direct3D 11, vous ne devez utiliser les ressources de téléchargement que lorsque l’UC écrira les données une seule fois et que le GPU les lira une seule fois.</span><span class="sxs-lookup"><span data-stu-id="590ce-111">In both Direct3D 12 and Direct3D 11, you should use upload resources only where the CPU will write the data once, and the GPU will read it once.</span></span>

<span data-ttu-id="590ce-112">Dans certains cas,</span><span class="sxs-lookup"><span data-stu-id="590ce-112">In some cases,</span></span>
* <span data-ttu-id="590ce-113">le GPU lit les données plusieurs fois, ou</span><span class="sxs-lookup"><span data-stu-id="590ce-113">the GPU will read the data multiple times, or</span></span>
* <span data-ttu-id="590ce-114">le GPU ne lit pas les données de manière linéaire, ou</span><span class="sxs-lookup"><span data-stu-id="590ce-114">the GPU won't read the data linearly, or</span></span>
* <span data-ttu-id="590ce-115">le rendu est déjà limité au GPU.</span><span class="sxs-lookup"><span data-stu-id="590ce-115">the rendering is significantly GPU-limited already.</span></span>

<span data-ttu-id="590ce-116">Dans ce cas, la meilleure option consiste à utiliser [**ID3D12GraphicsCommandList :: CopyTextureRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) ou [**ID3D12GraphicsCommandList :: CopyBufferRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) pour copier les données de mémoire tampon de chargement dans une ressource par défaut.</span><span class="sxs-lookup"><span data-stu-id="590ce-116">In those cases, the better option might be to use [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) or [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) to copy the upload buffer data to a default resource.</span></span>

<span data-ttu-id="590ce-117">Une ressource par défaut peut résider dans la mémoire vidéo physique sur des GPU discrètes.</span><span class="sxs-lookup"><span data-stu-id="590ce-117">A default resource can reside in physical video memory on discrete GPUs.</span></span>

### <a name="code-example-direct3d-11"></a><span data-ttu-id="590ce-118">Exemple de code : Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="590ce-118">Code Example: Direct3D 11</span></span>

```cpp
// Direct3D 11: Separate buffers for each resource type.

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

### <a name="code-example-direct3d-12"></a><span data-ttu-id="590ce-119">Exemple de code : Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="590ce-119">Code Example: Direct3D 12</span></span>

```cpp
// Direct3D 12: One buffer to accommodate different types of resources

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

<span data-ttu-id="590ce-120">Notez l’utilisation des structures d’assistance [**CD3DX12_HEAP_PROPERTIES**](cd3dx12-heap-properties.md) et [**CD3DX12_RESOURCE_DESC**](cd3dx12-resource-desc.md).</span><span class="sxs-lookup"><span data-stu-id="590ce-120">Note the use of the helper structures [**CD3DX12_HEAP_PROPERTIES**](cd3dx12-heap-properties.md) and [**CD3DX12_RESOURCE_DESC**](cd3dx12-resource-desc.md).</span></span>

## <a name="constants"></a><span data-ttu-id="590ce-121">Constantes</span><span class="sxs-lookup"><span data-stu-id="590ce-121">Constants</span></span>

<span data-ttu-id="590ce-122">Pour définir des constantes, des sommets et des index au sein d’un segment de mémoire de chargement ou de readback, utilisez les API suivantes.</span><span class="sxs-lookup"><span data-stu-id="590ce-122">To set constants, vertices, and indexes within an upload or readback heap, use the following APIs.</span></span>

-   [<span data-ttu-id="590ce-123">**ID3D12Device::CreateConstantBufferView**</span><span class="sxs-lookup"><span data-stu-id="590ce-123">**ID3D12Device::CreateConstantBufferView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
-   [<span data-ttu-id="590ce-124">**ID3D12GraphicsCommandList::IASetVertexBuffers**</span><span class="sxs-lookup"><span data-stu-id="590ce-124">**ID3D12GraphicsCommandList::IASetVertexBuffers**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)
-   [<span data-ttu-id="590ce-125">**ID3D12GraphicsCommandList::IASetIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="590ce-125">**ID3D12GraphicsCommandList::IASetIndexBuffer**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer)

## <a name="resources"></a><span data-ttu-id="590ce-126">Ressources</span><span class="sxs-lookup"><span data-stu-id="590ce-126">Resources</span></span>

<span data-ttu-id="590ce-127">Les ressources sont le concept Direct3D qui soustrait l’utilisation de la mémoire physique GPU.</span><span class="sxs-lookup"><span data-stu-id="590ce-127">Resources are the Direct3D concept that abstracts the usage of GPU physical memory.</span></span> <span data-ttu-id="590ce-128">Les ressources requièrent un espace d’adressage virtuel GPU pour accéder à la mémoire physique.</span><span class="sxs-lookup"><span data-stu-id="590ce-128">Resources require GPU virtual address space to access physical memory.</span></span> <span data-ttu-id="590ce-129">La création de ressources est libre de threads.</span><span class="sxs-lookup"><span data-stu-id="590ce-129">Resource creation is free-threaded.</span></span>

<span data-ttu-id="590ce-130">Il existe trois types de ressources en ce qui concerne la création d’adresses virtuelles et la flexibilité dans Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="590ce-130">There are three types of resources with respect to virtual address creation and flexibility in Direct3D 12.</span></span>

### <a name="committed-resources"></a><span data-ttu-id="590ce-131">Ressources validées</span><span class="sxs-lookup"><span data-stu-id="590ce-131">Committed resources</span></span>

<span data-ttu-id="590ce-132">Les ressources validées sont l’idée la plus courante des ressources Direct3D sur les générations.</span><span class="sxs-lookup"><span data-stu-id="590ce-132">Committed resources are the most common idea of Direct3D resources over the generations.</span></span> <span data-ttu-id="590ce-133">La création d’une telle ressource alloue de la plage d’adresses virtuelles, un tas implicite suffisamment grand pour s’ajuster à la ressource entière et valide la plage d’adresses virtuelles dans la mémoire physique encapsulée par le tas.</span><span class="sxs-lookup"><span data-stu-id="590ce-133">Creating such a resource allocates virtual address range, an implicit heap large enough to fit the whole resource, and commits the virtual address range to the physical memory encapsulated by the heap.</span></span> <span data-ttu-id="590ce-134">Les propriétés de tas implicites doivent être passées pour correspondre à la parité fonctionnelle avec les versions Direct3D précédentes.</span><span class="sxs-lookup"><span data-stu-id="590ce-134">The implicit heap properties must be passed to match functional parity with previous Direct3D versions.</span></span> <span data-ttu-id="590ce-135">Reportez-vous à [**ID3D12Device :: CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span><span class="sxs-lookup"><span data-stu-id="590ce-135">Refer to [**ID3D12Device::CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span></span>

### <a name="reserved-resources"></a><span data-ttu-id="590ce-136">Ressources réservées</span><span class="sxs-lookup"><span data-stu-id="590ce-136">Reserved resources</span></span>

<span data-ttu-id="590ce-137">Les ressources réservées sont équivalentes aux ressources en mosaïque Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="590ce-137">Reserved resources are equivalent to Direct3D 11 tiled resources.</span></span> <span data-ttu-id="590ce-138">Lors de leur création, seule une plage d’adresses virtuelles est allouée et n’est mappée à aucun segment.</span><span class="sxs-lookup"><span data-stu-id="590ce-138">On their creation, only a virtual address range is allocated, and not mapped to any heap.</span></span> <span data-ttu-id="590ce-139">L’application mappera ces ressources aux tas ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="590ce-139">The application will map such resources to heaps later.</span></span> <span data-ttu-id="590ce-140">Les capacités de ces ressources sont actuellement inchangées par rapport à Direct3D 11, car elles peuvent être mappées à un segment de mémoire avec une granularité de mosaïque de 64 Ko avec [**UpdateTileMappings**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings).</span><span class="sxs-lookup"><span data-stu-id="590ce-140">The capabilities of such resources are currently unchanged from Direct3D 11, as they can be mapped to a heap at a 64KB tile granularity with [**UpdateTileMappings**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings).</span></span> <span data-ttu-id="590ce-141">Reportez-vous à [**ID3D12Device :: CreateReservedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createreservedresource).</span><span class="sxs-lookup"><span data-stu-id="590ce-141">Refer to [**ID3D12Device::CreateReservedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createreservedresource).</span></span>

### <a name="placed-resources"></a><span data-ttu-id="590ce-142">Ressources placées</span><span class="sxs-lookup"><span data-stu-id="590ce-142">Placed resources</span></span>

<span data-ttu-id="590ce-143">Nouveauté de Direct3D 12, vous pouvez créer des tas distincts des ressources.</span><span class="sxs-lookup"><span data-stu-id="590ce-143">New for Direct3D 12, you can create heaps separate from resources.</span></span> <span data-ttu-id="590ce-144">Par la suite, vous pouvez rechercher plusieurs ressources dans un seul segment de mémoire.</span><span class="sxs-lookup"><span data-stu-id="590ce-144">Afterward, you can locate multiple resources within a single heap.</span></span> <span data-ttu-id="590ce-145">Vous pouvez le faire sans créer de ressources en mosaïque ou réservées, ce qui permet d’activer les fonctionnalités pour tous les types de ressources qui peuvent être créés directement par votre application.</span><span class="sxs-lookup"><span data-stu-id="590ce-145">You can do that without creating tiled or reserved resources, enabling the capabilities for all resource types able to be created directly by your application.</span></span> <span data-ttu-id="590ce-146">Plusieurs ressources peuvent se chevaucher et vous devez utiliser [**ID3D12GraphicsCommandList :: ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) pour réutiliser la mémoire physique correctement.</span><span class="sxs-lookup"><span data-stu-id="590ce-146">Multiple resources might overlap, and you must use the [**ID3D12GraphicsCommandList::ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) to re-use physical memory correctly.</span></span> <span data-ttu-id="590ce-147">Reportez-vous à [**ID3D12Device :: CreatePlacedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource).</span><span class="sxs-lookup"><span data-stu-id="590ce-147">Refer to [**ID3D12Device::CreatePlacedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource).</span></span>

## <a name="resource-size-reflection"></a><span data-ttu-id="590ce-148">Réflexion de la taille des ressources</span><span class="sxs-lookup"><span data-stu-id="590ce-148">Resource size reflection</span></span>

<span data-ttu-id="590ce-149">Vous devez utiliser la réflexion de la taille des ressources pour comprendre la quantité d’espace dont les textures de texture inconnues ont besoin dans les tas.</span><span class="sxs-lookup"><span data-stu-id="590ce-149">You must use resource size reflection to understand how much space textures with unknown texture layouts require in heaps.</span></span> <span data-ttu-id="590ce-150">Les mémoires tampons sont également prises en charge, mais principalement par commodité.</span><span class="sxs-lookup"><span data-stu-id="590ce-150">Buffers are also supported, but mostly as a convenience.</span></span>

<span data-ttu-id="590ce-151">Vous devez être conscient des différences d’alignement majeures, afin d’aider à regrouper les ressources de façon plus dense.</span><span class="sxs-lookup"><span data-stu-id="590ce-151">You should be aware of major alignment discrepancies, to help pack resources more densely.</span></span>

<span data-ttu-id="590ce-152">Par exemple, un tableau à un seul élément avec une mémoire tampon d’un octet retourne une *taille* de 64 Ko et un *alignement* de 64 Ko, car les mémoires tampons ne peuvent être alignées que de 64 Ko.</span><span class="sxs-lookup"><span data-stu-id="590ce-152">For example, a single-element array with a one-byte-buffer returns a *Size* of 64KB, and an *Alignment* of 64KB, because buffers can be only 64KB-aligned.</span></span>

<span data-ttu-id="590ce-153">En outre, un tableau à trois éléments avec deux textures alignées de 64 Ko à texture unique et une texture alignée de 4 Mo à Texel unique signale des tailles différentes en fonction de l’ordre du tableau.</span><span class="sxs-lookup"><span data-stu-id="590ce-153">Also, a three element array with two single-texel 64KB aligned textures and a single-texel 4MB aligned texture reports differing sizes based on the order of the array.</span></span> <span data-ttu-id="590ce-154">Si les textures alignées de 4 Mo sont en milieu, la *taille* résultante est 12 Mo.</span><span class="sxs-lookup"><span data-stu-id="590ce-154">If the 4MB aligned textures is in the middle, then the resulting *Size* is 12MB.</span></span> <span data-ttu-id="590ce-155">Dans le cas contraire, la taille obtenue est de 8 Mo.</span><span class="sxs-lookup"><span data-stu-id="590ce-155">Otherwise, the resulting Size is 8MB.</span></span> <span data-ttu-id="590ce-156">L’alignement retourné serait toujours 4Mo, le sur-ensemble de tous les alignements dans le tableau de ressources.</span><span class="sxs-lookup"><span data-stu-id="590ce-156">The Alignment returned would always be 4MB, the superset of all alignments in the resource array.</span></span>

<span data-ttu-id="590ce-157">Référencez les API suivantes.</span><span class="sxs-lookup"><span data-stu-id="590ce-157">Reference the following APIs.</span></span>

- [<span data-ttu-id="590ce-158">**\_Informations d' \_ allocation de ressources D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="590ce-158">**D3D12\_RESOURCE\_ALLOCATION\_INFO**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
- [<span data-ttu-id="590ce-159">**GetResourceAllocationInfo**</span><span class="sxs-lookup"><span data-stu-id="590ce-159">**GetResourceAllocationInfo**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)

## <a name="buffer-alignment"></a><span data-ttu-id="590ce-160">Alignement de la mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="590ce-160">Buffer alignment</span></span>

<span data-ttu-id="590ce-161">Les restrictions d’alignement de mémoire tampon n’ont pas changé par rapport à Direct3D 11, notamment :</span><span class="sxs-lookup"><span data-stu-id="590ce-161">Buffer alignment restrictions have not changed from Direct3D 11, notably:</span></span>

- <span data-ttu-id="590ce-162">4 Mo pour les textures à échantillons multiples.</span><span class="sxs-lookup"><span data-stu-id="590ce-162">4 MB for multi-sample textures.</span></span>
- <span data-ttu-id="590ce-163">64 Ko pour les textures et les mémoires tampons d’échantillon simple.</span><span class="sxs-lookup"><span data-stu-id="590ce-163">64 KB for single-sample textures and buffers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="590ce-164">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="590ce-164">Related topics</span></span>

* [<span data-ttu-id="590ce-165">Sous-allocation dans des mémoires tampons</span><span class="sxs-lookup"><span data-stu-id="590ce-165">Suballocation within buffers</span></span>](large-buffers.md)
