---
title: Création de descripteurs
description: Décrit et montre des exemples pour créer des vues de mémoire tampon d’index, de vertex et de constantes ; la ressource de nuanceur, la cible de rendu, l’accès non ordonné, la sortie de flux et les vues de stencil de profondeur ; et les échantillonneurs. Toutes les méthodes de création de descripteurs sont des threads libres.
ms.assetid: 0D360A7C-8A2F-49E1-A5CC-98C958B59D1C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aac9aab5dde0f5ca0864fcc1627ade984c6b6ccf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548533"
---
# <a name="creating-descriptors"></a>Création de descripteurs

Décrit et montre des exemples pour créer des vues de mémoire tampon d’index, de vertex et de constantes ; la ressource de nuanceur, la cible de rendu, l’accès non ordonné, la sortie de flux et les vues de stencil de profondeur ; et les échantillonneurs. Toutes les méthodes de création de descripteurs sont des threads libres.

-   [Vue de la mémoire tampon d’index](#index-buffer-view)
-   [Vue de mémoire tampon de vertex](#vertex-buffer-view)
-   [Affichage des ressources de nuanceur](#shader-resource-view)
-   [Vue de mémoire tampon constante](#constant-buffer-view)
-   [Échantillonneur](#sampler)
-   [Vue d’accès non ordonné](#unordered-access-view)
-   [Affichage de sortie de flux](#stream-output-view)
-   [Affichage de la cible de rendu](#render-target-view)
-   [Vue du stencil de profondeur](#depth-stencil-view)
-   [Rubriques connexes](#related-topics)

## <a name="index-buffer-view"></a>Vue de la mémoire tampon d’index

Pour créer une vue de mémoire tampon d’index, remplissez une structure de [**\_ vue de \_ tampon \_ d’index D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_index_buffer_view) :

``` syntax
typedef struct D3D12_INDEX_BUFFER_VIEW
{
    D3D12_GPU_VIRTUAL_ADDRESS BufferLocation;
    UINT SizeInBytes;
    DXGI_FORMAT Format;
}   D3D12_INDEX_BUFFER_VIEW;
```

Définissez l’emplacement (Call [**GetGPUVirtualAddress**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress)) et la taille de la mémoire tampon, en notant que l' \_ adresse virtuelle du GPU D3D12 \_ \_ est définie comme suit :

`typedef UINT64 D3D12_GPU_VIRTUAL_ADDRESS;`

Reportez-vous à l’énumération de [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) . En général, pour un tampon d’index, la définition suivante peut être utilisée :

`const DXGI_FORMAT StandardIndexFormat = DXGI_FORMAT_R32_UINT;`

Enfin, appelez [**ID3D12GraphicsCommandList :: IASetIndexBuffer**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer).

Par exemple,


```C++
// Initialize the index buffer view.
m_indexBufferView.BufferLocation = m_indexBuffer->GetGPUVirtualAddress();
m_indexBufferView.SizeInBytes = SampleAssets::IndexDataSize;
m_indexBufferView.Format = SampleAssets::StandardIndexFormat;
```



## <a name="vertex-buffer-view"></a>Vue de mémoire tampon de vertex

Pour créer une vue de mémoire tampon de vertex, remplissez une structure de [**\_ \_ \_ vue de mémoire tampon de vertex D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view) :

``` syntax
typedef struct D3D12_VERTEX_BUFFER_VIEW {
    D3D12_GPU_VIRTUAL_ADDRESS BufferLocation;  
    UINT SizeInBytes;  
    UINT StrideInBytes;  
} D3D12_VERTEX_BUFFER_VIEW;
```

Définissez l’emplacement (Call [**GetGPUVirtualAddress**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress)) et la taille de la mémoire tampon, en notant que l' \_ adresse virtuelle du GPU D3D12 \_ \_ est définie comme suit :

`typedef UINT64 D3D12_GPU_VIRTUAL_ADDRESS;`

Le Stride est généralement la taille d’une structure de données de vertex unique, par exemple `sizeof(Vertex);` , puis appelle [**ID3D12GraphicsCommandList :: IASetVertexBuffers**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers).

Par exemple,


```C++
// Initialize the vertex buffer view.
m_vertexBufferView.BufferLocation = m_vertexBuffer->GetGPUVirtualAddress();
m_vertexBufferView.SizeInBytes = SampleAssets::VertexDataSize;
m_vertexBufferView.StrideInBytes = SampleAssets::StandardVertexStride;
```



## <a name="shader-resource-view"></a>Affichage des ressources de nuanceur

Pour créer une vue de ressource de nuanceur, remplissez une structure de [**\_ vue de ressource de nuanceur D3D12 \_ \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc) :

``` syntax
typedef struct D3D12_SHADER_RESOURCE_VIEW_DESC  
    {  
    DXGI_FORMAT Format;  
    D3D12_SRV_DIMENSION ViewDimension;  
    UINT Shader4ComponentMapping;  
    union   
        {  
        D3D12_BUFFER_SRV Buffer;  
        D3D12_TEX1D_SRV Texture1D;  
        D3D12_TEX1D_ARRAY_SRV Texture1DArray;  
        D3D12_TEX2D_SRV Texture2D;  
        D3D12_TEX2D_ARRAY_SRV Texture2DArray;  
        D3D12_TEX2DMS_SRV Texture2DMS;  
        D3D12_TEX2DMS_ARRAY_SRV Texture2DMSArray;  
        D3D12_TEX3D_SRV Texture3D;  
        D3D12_TEXCUBE_SRV TextureCube;  
        D3D12_TEXCUBE_ARRAY_SRV TextureCubeArray;  
        }   ;  
    }   D3D12_SHADER_RESOURCE_VIEW_DESC; 
```

Le `ViewDimension` champ est défini sur zéro ou une valeur de l’énumération d' [**\_ \_ \_ indicateurs SRV de mémoire tampon D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_srv_flags) .

Les enums et les structures référencés par la [**\_ vue de ressource du nuanceur D3D12 \_ \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc) sont :

-   [**\_format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
-   [**\_Mémoire tampon D3D12 \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_srv)
-   [**D3D12 \_ TEX1D \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_srv)
-   [**\_SRV du \_ tableau D3D12 TEX1D \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_srv)
-   [**D3D12 \_ TEX2D \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_srv)
-   [**\_SRV du \_ tableau D3D12 TEX2D \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [**D3D12 \_ TEX2DMS \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_srv)
-   [**\_SRV du \_ tableau D3D12 TEX2DMS \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_srv)
-   [**D3D12 \_ TEX3D \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_srv)
-   [**D3D12 \_ TEXCUBE \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texcube_srv)
-   [**\_SRV du \_ tableau D3D12 TEXCUBE \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texcube_array_srv)

Notez que float `ResourceMinLODClamp` a été ajouté à SRVs pour Tex1D/2D/3D/cube. Dans D3D11, il s’agit d’une propriété d’une ressource, mais cela ne correspondait pas à la façon dont elle était implémentée dans le matériel. `StructureByteStride` a été ajouté à la mémoire tampon SRVs, où, dans D3D11, il s’agissait d’une propriété de la ressource. Si Stride est différent de zéro, cela indique une vue de mémoire tampon structurée, et le format doit être défini sur DXGI \_ format \_ Unknown.

Enfin, pour créer l’affichage des ressources de nuanceur, appelez [**ID3D12Device :: CreateShaderResourceView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview).

Par exemple,


```C++
// Describe and create an SRV.
D3D12_SHADER_RESOURCE_VIEW_DESC srvDesc = {};
srvDesc.ViewDimension = D3D12_SRV_DIMENSION_TEXTURE2D;
srvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
srvDesc.Format = tex.Format;
srvDesc.Texture2D.MipLevels = tex.MipLevels;
srvDesc.Texture2D.MostDetailedMip = 0;
srvDesc.Texture2D.ResourceMinLODClamp = 0.0f;
m_device->CreateShaderResourceView(m_textures[i].Get(), &srvDesc, cbvSrvHandle);
```



## <a name="constant-buffer-view"></a>Vue de mémoire tampon constante

Pour créer une vue de mémoire tampon constante, remplissez une structure de [**\_ vue de \_ mémoire tampon constante D3D12 \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_constant_buffer_view_desc) :

``` syntax
typedef struct D3D12_CONSTANT_BUFFER_VIEW_DESC {
  D3D12_GPU_VIRTUAL_ADDRESS BufferLocation;
  UINT   SizeInBytes;
} D3D12_CONSTANT_BUFFER_VIEW_DESC;
```

Appelez ensuite [**ID3D12Device :: CreateConstantBufferView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview).

Par exemple,


```C++
// Describe and create a constant buffer view.
D3D12_CONSTANT_BUFFER_VIEW_DESC cbvDesc = {};
cbvDesc.BufferLocation = m_constantBuffer->GetGPUVirtualAddress();
cbvDesc.SizeInBytes = (sizeof(ConstantBuffer) + 255) & ~255;    // CB size is required to be 256-byte aligned.
m_device->CreateConstantBufferView(&cbvDesc, m_cbvHeap->GetCPUDescriptorHandleForHeapStart());
```



## <a name="sampler"></a>Échantillonneur

Pour créer un exemple, remplissez une structure [**d' \_ échantillonneur \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_sampler_desc) :

``` syntax
typedef struct D3D12_SAMPLER_DESC
{
    D3D12_FILTER Filter;
    D3D12_TEXTURE_ADDRESS_MODE AddressU;
    D3D12_TEXTURE_ADDRESS_MODE AddressV;
    D3D12_TEXTURE_ADDRESS_MODE AddressW;
    FLOAT MipLODBias;
    UINT MaxAnisotropy;
    D3D12_COMPARISON_FUNC ComparisonFunc;
    FLOAT BorderColor[4]; // RGBA
    FLOAT MinLOD;
    FLOAT MaxLOD;
} D3D12_SAMPLER_DESC;
```

Pour remplir cette structure, reportez-vous aux énumérations suivantes :

-   [**\_Filtre D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter)
-   [**\_Type de filtre D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter_type)
-   [**\_Type de \_ réduction du filtre D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter_reduction_type)
-   [**MODE d’adresse de la \_ texture D3D12 \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode)
-   [**D3D12 de comparaison de la fonction \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func)

Enfin, appelez [**ID3D12Device :: CreateSampler**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createsampler).

Par exemple,


```C++
// Describe and create a sampler.
D3D12_SAMPLER_DESC samplerDesc = {};
samplerDesc.Filter = D3D12_FILTER_MIN_MAG_MIP_LINEAR;
samplerDesc.AddressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP;
samplerDesc.AddressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP;
samplerDesc.AddressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP;
samplerDesc.MinLOD = 0;
samplerDesc.MaxLOD = D3D12_FLOAT32_MAX;
samplerDesc.MipLODBias = 0.0f;
samplerDesc.MaxAnisotropy = 1;
samplerDesc.ComparisonFunc = D3D12_COMPARISON_FUNC_ALWAYS;
m_device->CreateSampler(&samplerDesc, m_samplerHeap->GetCPUDescriptorHandleForHeapStart());
```



## <a name="unordered-access-view"></a>Vue d’accès non ordonné

Pour créer une vue d’accès non triée, remplissez une structure de [**\_ vue d’accès non triée D3D12 \_ \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_unordered_access_view_desc) :

``` syntax
typedef struct D3D12_UNORDERED_ACCESS_VIEW_DESC
{
    DXGI_FORMAT Format;
    D3D12_UAV_DIMENSION ViewDimension;

    union
    {
        D3D12_BUFFER_UAV Buffer;
        D3D12_TEX1D_UAV Texture1D;
        D3D12_TEX1D_ARRAY_UAV Texture1DArray;
        D3D12_TEX2D_UAV Texture2D;
        D3D12_TEX2D_ARRAY_UAV Texture2DArray;
        D3D12_TEX3D_UAV Texture3D;
    };
} D3D12_UNORDERED_ACCESS_VIEW_DESC;
```

Le `ViewDimension` champ est défini sur zéro ou une valeur de la [**\_ mémoire tampon D3D12 \_ UAV \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags) Enum.

Reportez-vous aux structures et énumérations suivantes :

-   [**\_format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
-   [**\_Mémoire tampon D3D12 \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav)
-   [**D3D12 \_ TEX1D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_uav)
-   [**D3D12 \_ TEX1D \_ array \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_uav)
-   [**D3D12 \_ TEX2D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_uav)
-   [**D3D12 \_ TEX2D \_ array \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)
-   [**D3D12 \_ TEX3D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_uav)

`StructureByteStride` a été ajouté à la mémoire tampon UAVs, où, dans D3D11, il s’agissait d’une propriété de la ressource. Si Stride est différent de zéro, cela indique une vue de mémoire tampon structurée, et le format doit être défini sur DXGI \_ format \_ Unknown.

Enfin, appelez [**ID3D12Device :: CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview).

Par exemple,


```C++
// Create the unordered access views (UAVs) that store the results of the compute work.
CD3DX12_CPU_DESCRIPTOR_HANDLE processedCommandsHandle(m_cbvSrvUavHeap->GetCPUDescriptorHandleForHeapStart(), ProcessedCommandsOffset, m_cbvSrvUavDescriptorSize);
for (UINT frame = 0; frame < FrameCount; frame++)
{
    // Allocate a buffer large enough to hold all of the indirect commands
    // for a single frame as well as a UAV counter.
    commandBufferDesc = CD3DX12_RESOURCE_DESC::Buffer(CommandBufferSizePerFrame + sizeof(UINT), D3D12_RESOURCE_FLAG_ALLOW_UNORDERED_ACCESS);
    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &commandBufferDesc,
        D3D12_RESOURCE_STATE_COPY_DEST,
        nullptr,
        IID_PPV_ARGS(&m_processedCommandBuffers[frame])));

    D3D12_UNORDERED_ACCESS_VIEW_DESC uavDesc = {};
    uavDesc.Format = DXGI_FORMAT_UNKNOWN;
    uavDesc.ViewDimension = D3D12_UAV_DIMENSION_BUFFER;
    uavDesc.Buffer.FirstElement = 0;
    uavDesc.Buffer.NumElements = TriangleCount;
    uavDesc.Buffer.StructureByteStride = sizeof(IndirectCommand);
    uavDesc.Buffer.CounterOffsetInBytes = CommandBufferSizePerFrame;
    uavDesc.Buffer.Flags = D3D12_BUFFER_UAV_FLAG_NONE;

    m_device->CreateUnorderedAccessView(            
        m_processedCommandBuffers[frame].Get(),
        m_processedCommandBuffers[frame].Get(),
        &uavDesc,
        processedCommandsHandle);

    processedCommandsHandle.Offset(CbvSrvUavDescriptorCountPerFrame, m_cbvSrvUavDescriptorSize);
}

// Allocate a buffer that can be used to reset the UAV counters and initialize it to 0.
ThrowIfFailed(m_device->CreateCommittedResource(
    &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
    D3D12_HEAP_FLAG_NONE,
    &CD3DX12_RESOURCE_DESC::Buffer(sizeof(UINT)),
    D3D12_RESOURCE_STATE_GENERIC_READ,
    
    nullptr,
    IID_PPV_ARGS(&m_processedCommandBufferCounterReset)));

UINT8* pMappedCounterReset = nullptr;
CD3DX12_RANGE readRange(0, 0);        // We do not intend to read from this resource on the CPU.
ThrowIfFailed(m_processedCommandBufferCounterReset->Map(0, &readRange, reinterpret_cast<void**>(&pMappedCounterReset)));
ZeroMemory(pMappedCounterReset, sizeof(UINT));
m_processedCommandBufferCounterReset->Unmap(0, nullptr);
```



## <a name="stream-output-view"></a>Affichage de sortie de flux

Pour créer un affichage de sortie de flux, renseignez une structure [**\_ desc de \_ sortie \_ de flux D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) .

``` syntax
typedef struct D3D12_STREAM_OUTPUT_DESC  
    {  
    _Field_size_full_(NumEntries)  const D3D12_SO_DECLARATION_ENTRY *pSODeclaration;  
    UINT NumEntries;  
    _Field_size_full_(NumStrides)  const UINT *pBufferStrides;  
    UINT NumStrides;  
    UINT RasterizedStream;  
    }   D3D12_STREAM_OUTPUT_DESC;  
```

Appelez ensuite [**ID3D12GraphicsCommandList :: SOSetTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets).

## <a name="render-target-view"></a>Affichage de la cible de rendu

Pour créer une vue de cible de rendu, remplissez une structure de [**\_ vue de cible de rendu D3D12 \_ \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_target_view_desc) .

``` syntax
typedef struct D3D12_RENDER_TARGET_VIEW_DESC
{
    DXGI_FORMAT Format;
    D3D12_RTV_DIMENSION ViewDimension;

    union
    {
        D3D12_BUFFER_RTV Buffer;
        D3D12_TEX1D_RTV Texture1D;
        D3D12_TEX1D_ARRAY_RTV Texture1DArray;
        D3D12_TEX2D_RTV Texture2D;
        D3D12_TEX2D_ARRAY_RTV Texture2DArray;
        D3D12_TEX2DMS_RTV Texture2DMS;
        D3D12_TEX2DMS_ARRAY_RTV Texture2DMSArray;
        D3D12_TEX3D_RTV Texture3D;
    };
} D3D12_RENDER_TARGET_VIEW_DESC;
```

Le `ViewDimension` champ est défini sur zéro ou une valeur de l’énumération de la [**\_ \_ dimension D3D12 RTV**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_rtv_dimension) .

Reportez-vous aux structures et énumérations suivantes :

-   [**\_format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
-   [**D3D12 \_ - \_ RTV de tampon**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_rtv)
-   [**D3D12 \_ TEX1D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_rtv)
-   [**D3D12 \_ \_ tableau TEX1D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_rtv)
-   [**D3D12 \_ TEX2D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_rtv)
-   [**D3D12 \_ TEX2DMS \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_rtv)
-   [**D3D12 \_ \_ tableau TEX2D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [**D3D12 \_ \_ tableau TEX2DMS \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_rtv)
-   [**D3D12 \_ TEX3D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_rtv)

Enfin, appelez [**ID3D12Device :: CreateRenderTargetView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrendertargetview).

Par exemple,

```C++
// Create descriptor heaps.
{
    // Describe and create a render target view (RTV) descriptor heap.
    D3D12_DESCRIPTOR_HEAP_DESC rtvHeapDesc = {};
    rtvHeapDesc.NumDescriptors = FrameCount;
    rtvHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_RTV;
    rtvHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_NONE;
    ThrowIfFailed(m_device->CreateDescriptorHeap(&rtvHeapDesc, IID_PPV_ARGS(&m_rtvHeap)));

    m_rtvDescriptorSize = m_device->GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_RTV);
}

// Create frame resources.
{
    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart());

    // Create a RTV for each frame.
    for (UINT n = 0; n < FrameCount; n++)
    {
        ThrowIfFailed(m_swapChain->GetBuffer(n, IID_PPV_ARGS(&m_renderTargets[n])));
        m_device->CreateRenderTargetView(m_renderTargets[n].Get(), nullptr, rtvHandle);
        rtvHandle.Offset(1, m_rtvDescriptorSize);
    }
```



## <a name="depth-stencil-view"></a>Vue du stencil de profondeur

Pour créer une vue de stencil de profondeur, remplissez une structure de [**\_ vue de stencil de profondeur \_ \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_view_desc) :

``` syntax
typedef struct D3D12_DEPTH_STENCIL_VIEW_DESC  
    {  
    DXGI_FORMAT Format;  
    D3D12_DSV_DIMENSION ViewDimension;  
    D3D12_DSV_FLAGS Flags;  
    union   
        {  
        D3D12_TEX1D_DSV Texture1D;  
        D3D12_TEX1D_ARRAY_DSV Texture1DArray;  
        D3D12_TEX2D_DSV Texture2D;  
        D3D12_TEX2D_ARRAY_DSV Texture2DArray;  
        D3D12_TEX2DMS_DSV Texture2DMS;  
        D3D12_TEX2DMS_ARRAY_DSV Texture2DMSArray;  
        }   ;  
    }   D3D12_DEPTH_STENCIL_VIEW_DESC;  
```

Le `ViewDimension` champ est défini sur zéro ou une valeur de l’énumération de la [**\_ \_ dimension DSV D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_dsv_dimension) . Reportez-vous à l’énumération des [**\_ \_ indicateurs DSV D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_dsv_flags) pour les paramètres de l’indicateur.

Reportez-vous aux structures et énumérations suivantes :

-   [**\_format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
-   [**D3D12 \_ TEX1D \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_dsv)
-   [**\_DSV D3D12 TEX1D \_ array \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_dsv)
-   [**D3D12 \_ TEX2D \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_dsv)
-   [**\_DSV D3D12 TEX2D \_ array \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_dsv)
-   [**D3D12 \_ TEX2DMS \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_dsv)
-   [**\_DSV D3D12 TEX2DMS \_ array \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_dsv)

Enfin, appelez [**ID3D12Device :: CreateDepthStencilView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createdepthstencilview).

Par exemple,


```C++
// Create the depth stencil view.
{
    D3D12_DEPTH_STENCIL_VIEW_DESC depthStencilDesc = {};
    depthStencilDesc.Format = DXGI_FORMAT_D32_FLOAT;
    depthStencilDesc.ViewDimension = D3D12_DSV_DIMENSION_TEXTURE2D;
    depthStencilDesc.Flags = D3D12_DSV_FLAG_NONE;

    D3D12_CLEAR_VALUE depthOptimizedClearValue = {};
    depthOptimizedClearValue.Format = DXGI_FORMAT_D32_FLOAT;
    depthOptimizedClearValue.DepthStencil.Depth = 1.0f;
    depthOptimizedClearValue.DepthStencil.Stencil = 0;

    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &CD3DX12_RESOURCE_DESC::Tex2D(DXGI_FORMAT_D32_FLOAT, m_width, m_height, 1, 0, 1, 0, D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL),
        D3D12_RESOURCE_STATE_DEPTH_WRITE,
        &depthOptimizedClearValue,
        IID_PPV_ARGS(&m_depthStencil)
        ));

    m_device->CreateDepthStencilView(m_depthStencil.Get(), &depthStencilDesc, m_dsvHeap->GetCPUDescriptorHandleForHeapStart());
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Descripteurs](descriptors.md)
</dt> <dt>

[Tas de descripteurs](descriptor-heaps.md)
</dt> </dl>

 

 