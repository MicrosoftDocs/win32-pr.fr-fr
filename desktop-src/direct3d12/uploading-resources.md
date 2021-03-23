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
# <a name="uploading-different-types-of-resources"></a>Téléchargement de différents types de ressources

Montre comment utiliser une mémoire tampon pour télécharger à la fois des données de mémoire tampon constantes et des données de mémoire tampon de vertex vers le GPU, et comment les sous-allouer et placer des données dans des mémoires tampons. L’utilisation d’une seule mémoire tampon augmente la flexibilité de l’utilisation de la mémoire et fournit aux applications un contrôle plus étroit de l’utilisation de la mémoire. Montre également les différences entre les modèles D3D11 et D3D12 pour le téléchargement de différents types de ressources.

-   [Télécharger différents types de ressources](#upload-different-types-of-resources)
    -   [Exemple de code : D3D11](#code-example-d3d11)
    -   [Exemple de code : D3D12](#code-example-d3d12)
-   [Constantes](#constants)
-   [Ressources](#uploading-different-types-of-resources)
-   [Réflexion de la taille des ressources](#resource-size-reflection)
-   [Alignement de la mémoire tampon](#buffer-alignment)
-   [Rubriques connexes](#related-topics)

## <a name="upload-different-types-of-resources"></a>Télécharger différents types de ressources

Dans D3D12, les applications créent une mémoire tampon pour prendre en charge différents types de données de ressources pour le téléchargement, et copient les données de ressources dans le même tampon d’une façon similaire pour différentes données de ressource. Des vues individuelles sont ensuite créées pour lier ces données de ressource au pipeline Graphics dans le nouveau modèle de liaison de ressources.

Dans D3D11, les applications créent des mémoires tampons distinctes pour différents types de données de ressource (Notez les différentes `BindFlags` utilisées dans l’exemple de code d3d11 ci-dessous), en liant explicitement chaque mémoire tampon de ressources au pipeline graphique, et mettent à jour les données de ressources avec différentes méthodes en fonction de différents types de ressources.

Dans D3D12 et D3D11, les applications doivent uniquement utiliser des ressources de téléchargement où l’UC écrira les données une seule fois et le GPU les lira une fois. Si le GPU lit les données plusieurs fois, le GPU ne lit pas les données de manière linéaire, ou le rendu est déjà limité au GPU. La meilleure option consiste à utiliser [**ID3D12GraphicsCommandList :: CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) ou [**ID3D12GraphicsCommandList :: CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) pour copier les données de mémoire tampon de chargement dans une ressource par défaut. Une ressource par défaut peut résider dans la mémoire vidéo physique sur des GPU discrètes.

### <a name="code-example-d3d11"></a>Exemple de code : D3D11

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

### <a name="code-example-d3d12"></a>Exemple de code : D3D12

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

Notez l’utilisation des structures d’assistance [**CD3DX12 les \_ \_ Propriétés du tas**](cd3dx12-heap-properties.md) et la description de la [**\_ ressource \_ CD3DX12**](cd3dx12-resource-desc.md).

## <a name="constants"></a>Constantes

Pour définir des constantes, des vertex et des index dans un segment de mémoire de chargement ou readback, utilisez les API suivantes :

-   [**ID3D12Device::CreateConstantBufferView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
-   [**ID3D12GraphicsCommandList::IASetVertexBuffers**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)
-   [**ID3D12GraphicsCommandList::IASetIndexBuffer**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer)

## <a name="resources"></a>Ressources

Les ressources sont le concept D3D qui soustrait l’utilisation de la mémoire physique GPU. Les ressources requièrent un espace d’adressage virtuel GPU pour accéder à la mémoire physique. La création de ressources est libre de threads.

Il existe trois types de ressources en ce qui concerne la création d’adresses virtuelles et la flexibilité dans D3D12 :

-   Ressources validées

    Les ressources validées sont l’idée la plus courante des ressources D3D sur les générations. La création d’une telle ressource alloue de la plage d’adresses virtuelles, un tas implicite suffisamment grand pour s’ajuster à la ressource entière et valide la plage d’adresses virtuelles dans la mémoire physique encapsulée par le tas. Les propriétés de tas implicites doivent être passées pour correspondre à la parité fonctionnelle avec les versions D3D précédentes. Reportez-vous à [**ID3D12Device :: CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).

-   Ressources réservées

    Les ressources réservées sont équivalentes aux ressources en mosaïque D3D11. Lors de leur création, seule une plage d’adresses virtuelles est allouée et n’est pas mappée à un segment de mémoire. L’application mappera ces ressources aux tas ultérieurement. Les fonctionnalités de ces ressources sont actuellement inchangées par rapport à D3D11, car elles peuvent être mappées à un segment de mémoire avec une granularité de mosaïque de 64 Ko avec [**UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings). Reportez-vous à [ **ID3D12Device :: CreateReservedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource)

-   Ressources placées

    Nouveauté de D3D12, les applications peuvent créer des tas distincts des ressources. Par la suite, l’application peut localiser plusieurs ressources dans un seul segment de mémoire. Cela peut être effectué sans créer de ressources en mosaïque ou réservées, ce qui permet d’activer les fonctionnalités de tous les types de ressources qui peuvent être créés directement par les applications. Plusieurs ressources peuvent se chevaucher, et l’application doit utiliser `TiledResourceBarrier` pour réutiliser la mémoire physique correctement. Reportez-vous à [ **ID3D12Device :: CreatePlacedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource)

## <a name="resource-size-reflection"></a>Réflexion de la taille des ressources

Les applications doivent utiliser la réflexion de la taille des ressources pour comprendre la quantité de textures de la pièce avec des dispositions de texture inconnues qui requièrent dans les tas. Les mémoires tampons sont également prises en charge, mais principalement par commodité.

Les applications doivent être conscientes des différences d’alignement majeures, afin d’aider à regrouper les ressources de façon plus dense.

Par exemple, un tableau à un seul élément avec une mémoire tampon d’un octet retourne une taille de 64 Ko et un alignement de 64 Ko, car les mémoires tampons ne peuvent actuellement être alignées que de 64 Ko.

En outre, un tableau à trois éléments avec deux textures alignées de 64 Ko à texture unique et une texture alignée de 4 Mo à Texel unique signale des tailles différentes en fonction de l’ordre du tableau. Si les textures alignées de 4 Mo sont en milieu, la taille obtenue est 12 Mo. Dans le cas contraire, la taille obtenue est de 8 Mo. L’alignement retourné est toujours de 4 Mo, le super-ensemble de tous les alignements dans le tableau de ressources.

Référencez les API suivantes :

-   [**\_Informations d' \_ allocation de ressources D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
-   [**GetResourceAllocationInfo**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)

## <a name="buffer-alignment"></a>Alignement de la mémoire tampon

Les restrictions d’alignement de mémoire tampon n’ont pas changé par rapport à D3D11, notamment :

-   4 Mo pour les textures à échantillons multiples.
-   64 Ko pour les textures et les mémoires tampons d’échantillon simple.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sous-allocation dans des mémoires tampons](large-buffers.md)
</dt> </dl>

 

 




