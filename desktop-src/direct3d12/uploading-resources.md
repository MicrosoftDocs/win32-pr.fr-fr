---
title: Téléchargement de différents types de ressources
description: Montre comment utiliser une mémoire tampon pour télécharger à la fois des données de mémoire tampon constantes et des données de mémoire tampon de vertex vers le GPU, et comment les sous-allouer et placer des données dans des mémoires tampons.
ms.assetid: 255B0482-21D6-4276-8009-3F3891879CA1
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03d4755124bbadcdd255a6e99739b710845ab14
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012852"
---
# <a name="uploading-different-types-of-resources"></a>Téléchargement de différents types de ressources

Montre comment utiliser une mémoire tampon pour télécharger à la fois des données de mémoire tampon constantes et des données de mémoire tampon de vertex vers le GPU, et comment les sous-allouer et placer des données dans des mémoires tampons. L’utilisation d’une seule mémoire tampon augmente la flexibilité de l’utilisation de la mémoire et fournit aux applications un contrôle plus étroit de l’utilisation de la mémoire. Montre également les différences entre les modèles Direct3D 11 et Direct3D 12 pour le téléchargement de différents types de ressources.

## <a name="upload-different-types-of-resources"></a>Télécharger différents types de ressources

Dans Direct3D 12, vous créez une mémoire tampon pour prendre en charge différents types de données de ressources pour le téléchargement, et vous copiez les données de ressources dans le même tampon d’une façon similaire pour différentes données de ressource. Des vues individuelles sont ensuite créées pour lier ces données de ressource au pipeline Graphics dans le modèle de liaison de ressource Direct3D 12.

Dans Direct3D 11, vous créez des mémoires tampons distinctes pour différents types de données de ressource (Notez les différentes `BindFlags` utilisées dans l’exemple de code Direct3D 11 ci-dessous), en liant explicitement chaque mémoire tampon de ressources au pipeline graphique, et en actualisant les données de ressources avec différentes méthodes en fonction de différents types de ressources.

Dans Direct3D 12 et Direct3D 11, vous ne devez utiliser les ressources de téléchargement que lorsque l’UC écrira les données une seule fois et que le GPU les lira une seule fois.

Dans certains cas,
* le GPU lit les données plusieurs fois, ou
* le GPU ne lit pas les données de manière linéaire, ou
* le rendu est déjà limité au GPU.

Dans ce cas, la meilleure option consiste à utiliser [**ID3D12GraphicsCommandList :: CopyTextureRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) ou [**ID3D12GraphicsCommandList :: CopyBufferRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) pour copier les données de mémoire tampon de chargement dans une ressource par défaut.

Une ressource par défaut peut résider dans la mémoire vidéo physique sur des GPU discrètes.

### <a name="code-example-direct3d-11"></a>Exemple de code : Direct3D 11

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

### <a name="code-example-direct3d-12"></a>Exemple de code : Direct3D 12

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

Notez l’utilisation des structures d’assistance [**CD3DX12_HEAP_PROPERTIES**](cd3dx12-heap-properties.md) et [**CD3DX12_RESOURCE_DESC**](cd3dx12-resource-desc.md).

## <a name="constants"></a>Constantes

Pour définir des constantes, des sommets et des index au sein d’un segment de mémoire de chargement ou de readback, utilisez les API suivantes.

-   [**ID3D12Device::CreateConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
-   [**ID3D12GraphicsCommandList::IASetVertexBuffers**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)
-   [**ID3D12GraphicsCommandList::IASetIndexBuffer**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer)

## <a name="resources"></a>Ressources

Les ressources sont le concept Direct3D qui soustrait l’utilisation de la mémoire physique GPU. Les ressources requièrent un espace d’adressage virtuel GPU pour accéder à la mémoire physique. La création de ressources est libre de threads.

Il existe trois types de ressources en ce qui concerne la création d’adresses virtuelles et la flexibilité dans Direct3D 12.

### <a name="committed-resources"></a>Ressources validées

Les ressources validées sont l’idée la plus courante des ressources Direct3D sur les générations. La création d’une telle ressource alloue de la plage d’adresses virtuelles, un tas implicite suffisamment grand pour s’ajuster à la ressource entière et valide la plage d’adresses virtuelles dans la mémoire physique encapsulée par le tas. Les propriétés de tas implicites doivent être passées pour correspondre à la parité fonctionnelle avec les versions Direct3D précédentes. Reportez-vous à [**ID3D12Device :: CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).

### <a name="reserved-resources"></a>Ressources réservées

Les ressources réservées sont équivalentes aux ressources en mosaïque Direct3D 11. Lors de leur création, seule une plage d’adresses virtuelles est allouée et n’est mappée à aucun segment. L’application mappera ces ressources aux tas ultérieurement. Les capacités de ces ressources sont actuellement inchangées par rapport à Direct3D 11, car elles peuvent être mappées à un segment de mémoire avec une granularité de mosaïque de 64 Ko avec [**UpdateTileMappings**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings). Reportez-vous à [**ID3D12Device :: CreateReservedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createreservedresource).

### <a name="placed-resources"></a>Ressources placées

Nouveauté de Direct3D 12, vous pouvez créer des tas distincts des ressources. Par la suite, vous pouvez rechercher plusieurs ressources dans un seul segment de mémoire. Vous pouvez le faire sans créer de ressources en mosaïque ou réservées, ce qui permet d’activer les fonctionnalités pour tous les types de ressources qui peuvent être créés directement par votre application. Plusieurs ressources peuvent se chevaucher et vous devez utiliser [**ID3D12GraphicsCommandList :: ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) pour réutiliser la mémoire physique correctement. Reportez-vous à [**ID3D12Device :: CreatePlacedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource).

## <a name="resource-size-reflection"></a>Réflexion de la taille des ressources

Vous devez utiliser la réflexion de la taille des ressources pour comprendre la quantité d’espace dont les textures de texture inconnues ont besoin dans les tas. Les mémoires tampons sont également prises en charge, mais principalement par commodité.

Vous devez être conscient des différences d’alignement majeures, afin d’aider à regrouper les ressources de façon plus dense.

Par exemple, un tableau à un seul élément avec une mémoire tampon d’un octet retourne une *taille* de 64 Ko et un *alignement* de 64 Ko, car les mémoires tampons ne peuvent être alignées que de 64 Ko.

En outre, un tableau à trois éléments avec deux textures alignées de 64 Ko à texture unique et une texture alignée de 4 Mo à Texel unique signale des tailles différentes en fonction de l’ordre du tableau. Si les textures alignées de 4 Mo sont en milieu, la *taille* résultante est 12 Mo. Dans le cas contraire, la taille obtenue est de 8 Mo. L’alignement retourné serait toujours 4Mo, le sur-ensemble de tous les alignements dans le tableau de ressources.

Référencez les API suivantes.

- [**\_Informations d' \_ allocation de ressources D3D12 \_**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
- [**GetResourceAllocationInfo**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)

## <a name="buffer-alignment"></a>Alignement de la mémoire tampon

Les restrictions d’alignement de mémoire tampon n’ont pas changé par rapport à Direct3D 11, notamment :

- 4 Mo pour les textures à échantillons multiples.
- 64 Ko pour les textures et les mémoires tampons d’échantillon simple.

## <a name="related-topics"></a>Rubriques connexes

* [Sous-allocation dans des mémoires tampons](large-buffers.md)
