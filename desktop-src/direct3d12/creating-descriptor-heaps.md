---
title: Création de tas de descripteurs
description: Pour créer et configurer un tas de descripteur, vous devez sélectionner un type de tas de descripteur, déterminer le nombre de descripteurs qu’il contient et définir des indicateurs qui indiquent s’il est visible par l’UC et/ou nuanceur visible.
ms.assetid: 58677023-692C-4BA4-90B7-D568F3DD3F73
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 218d21d462dd393360e9ebfcb07ab5b35524b9d8d8c01c8ab1ef28ef90166eb2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857989"
---
# <a name="creating-descriptor-heaps"></a>Création de tas de descripteurs

Pour créer et configurer un tas de descripteur, vous devez sélectionner un type de tas de descripteur, déterminer le nombre de descripteurs qu’il contient et définir des indicateurs qui indiquent s’il est visible par l’UC et/ou nuanceur visible.

-   [Types de tas de descripteur](#descriptor-heap-types)
-   [Propriétés du tas du descripteur](#descriptor-heap-properties)
-   [Handles de descripteur](#descriptor-handles)
-   [Méthodes du tas du descripteur](#descriptor-heap-methods)
-   [Wrapper de tas de descripteur minimal](#minimal-descriptor-heap-wrapper)
-   [Rubriques connexes](#related-topics)

## <a name="descriptor-heap-types"></a>Types de tas de descripteur

Le type de segment de mémoire est déterminé par un membre de l’énumération du [**\_ type de \_ tas \_ du descripteur D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type) :

``` syntax
typedef enum D3D12_DESCRIPTOR_HEAP_TYPE
{
    D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV,    // Constant buffer/Shader resource/Unordered access views
    D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER,        // Samplers
    D3D12_DESCRIPTOR_HEAP_TYPE_RTV,            // Render target view
    D3D12_DESCRIPTOR_HEAP_TYPE_DSV,            // Depth stencil view
    D3D12_DESCRIPTOR_HEAP_TYPE_NUM_TYPES       // Simply the number of descriptor heap types
} D3D12_DESCRIPTOR_HEAP_TYPE;
```

## <a name="descriptor-heap-properties"></a>Propriétés du tas du descripteur

Les propriétés du tas sont définies sur la structure [**\_ desc du \_ tas \_ du descripteur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) , qui fait référence à la fois au [**\_ \_ \_ type de tas**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type) du descripteur D3D12 et aux enums du [**\_ \_ tas \_ de descripteurs D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags) .

Le \_ nuanceur de l’indicateur de tas du descripteur d’indicateur D3D12 \_ \_ \_ \_ visible peut éventuellement être défini sur un tas de descripteur pour indiquer qu’il est lié à une liste de commandes pour référence par des nuanceurs. Les tas de descripteurs créés *sans* cet indicateur permettent aux applications d’organiser les descripteurs dans la mémoire du processeur avant de les copier dans un tas de descripteur visible du nuanceur, par commodité. Toutefois, il est également intéressant pour les applications de créer directement des descripteurs dans des tas de descripteurs visibles par le nuanceur, sans qu’il soit nécessaire d’effectuer un stage sur le processeur.

Cet indicateur s’applique uniquement aux échantillonneurs CBV, SRV, UAV et. Elle ne s’applique pas aux autres types de tas de descripteurs, car les nuanceurs ne référencent pas directement les autres types.

Par exemple, décrivez et créez un tas de descripteur d’échantillonnage.


```C++
// Describe and create a sampler descriptor heap.
D3D12_DESCRIPTOR_HEAP_DESC samplerHeapDesc = {};
samplerHeapDesc.NumDescriptors = 1;
samplerHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER;
samplerHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE;
ThrowIfFailed(m_device->CreateDescriptorHeap(&samplerHeapDesc, IID_PPV_ARGS(&m_samplerHeap)));
```



Décrire et créer une vue de mémoire tampon constante (CBV), un tas de vue de ressource de nuanceur (SRV) et un tas de descripteurs de vue d’accès non ordonné (UAV).


```C++
// Describe and create a shader resource view (SRV) and unordered
// access view (UAV) descriptor heap.
D3D12_DESCRIPTOR_HEAP_DESC srvUavHeapDesc = {};
srvUavHeapDesc.NumDescriptors = DescriptorCount;
srvUavHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV;
srvUavHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE;
ThrowIfFailed(m_device->CreateDescriptorHeap(&srvUavHeapDesc, IID_PPV_ARGS(&m_srvUavHeap)));

m_rtvDescriptorSize = m_device->GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_RTV);
m_srvUavDescriptorSize = m_device->GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV);
```



## <a name="descriptor-handles"></a>Handles de descripteur

Le [**\_ \_ \_ handle**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) du descripteur GPU D3D12 et les structures de [**\_ \_ \_ handle du**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) descripteur d’UC D3D12 identifient les descripteurs spécifiques dans un tas de descripteur. Un handle est un peu comme un pointeur, mais l’application ne doit pas le déréférencer manuellement. dans le cas contraire, le comportement n’est pas défini. L’utilisation des handles doit traverser l’API. Un handle lui-même peut être copié librement ou passé dans des API qui opèrent sur des descripteurs/use. Étant donné qu’il n’existe pas de comptage de référence, l’application doit s’assurer qu’elle n’utilise pas de handle après la suppression du tas de descripteur sous-jacent.

Les applications peuvent déterminer la taille incrémentielle des descripteurs pour un type de tas de descripteur donné, afin qu’ils puissent générer des handles à n’importe quel emplacement dans un tas de descripteur, en commençant par le handle de la base. Les applications ne doivent jamais coder en dur les tailles d’incrément de handle de descripteur et doivent toujours les interroger pour une instance d’appareil donnée ; dans le cas contraire, le comportement n’est pas défini. Les applications ne doivent pas non plus utiliser les tailles et les handles d’incrément pour effectuer leur propre examen ou manipulation des données du tas du descripteur, car les résultats de cette opération ne sont pas définis. Les handles ne peuvent pas être utilisés en tant que pointeurs, mais plutôt en tant que proxies pour les pointeurs afin d’éviter les déréférencements accidentels.

> [!Note]
>
> Il existe une structure d’assistance, \_ \_ handle de descripteur GPU CD3DX12 \_ , définie dans l’en-tête d3dx12. h, qui hérite de la structure de [**\_ \_ \_ handle du descripteur GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) et fournit l’initialisation et d’autres opérations utiles. De même, la \_ \_ structure d’assistance du handle du descripteur de processeur CD3DX12 \_ est définie pour la structure de [**\_ \_ \_ handle du descripteur de processeur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) .

 

Ces deux structures d’assistance sont utilisées lors du remplissage des listes de commandes.


```C++
// Fill the command list with all the render commands and dependent state.
void D3D12nBodyGravity::PopulateCommandList()
{
    // Command list allocators can only be reset when the associated
    // command lists have finished execution on the GPU; apps should use
    // fences to determine GPU execution progress.
    ThrowIfFailed(m_commandAllocators[m_frameIndex]->Reset());

    // However, when ExecuteCommandList() is called on a particular command
    // list, that command list can then be reset at any time and must be before
    // re-recording.
    ThrowIfFailed(m_commandList->Reset(m_commandAllocators[m_frameIndex].Get(), m_pipelineState.Get()));

    // Set necessary state.
    m_commandList->SetPipelineState(m_pipelineState.Get());
    m_commandList->SetGraphicsRootSignature(m_rootSignature.Get());

    m_commandList->SetGraphicsRootConstantBufferView(RootParameterCB, m_constantBufferGS->GetGPUVirtualAddress() + m_frameIndex * sizeof(ConstantBufferGS));

    ID3D12DescriptorHeap* ppHeaps[] = { m_srvUavHeap.Get() };
    m_commandList->SetDescriptorHeaps(_countof(ppHeaps), ppHeaps);

    m_commandList->IASetVertexBuffers(0, 1, &m_vertexBufferView);
    m_commandList->IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_POINTLIST);
    m_commandList->RSSetScissorRects(1, &m_scissorRect);

    // Indicate that the back buffer will be used as a render target.
    m_commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET));

    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    m_commandList->OMSetRenderTargets(1, &rtvHandle, FALSE, nullptr);

    // Record commands.
    const float clearColor[] = { 0.0f, 0.0f, 0.1f, 0.0f };
    m_commandList->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);

    // Render the particles.
    float viewportHeight = static_cast<float>(static_cast<UINT>(m_viewport.Height) / m_heightInstances);
    float viewportWidth = static_cast<float>(static_cast<UINT>(m_viewport.Width) / m_widthInstances);
    for (UINT n = 0; n < ThreadCount; n++)
    {
        const UINT srvIndex = n + (m_srvIndex[n] == 0 ? SrvParticlePosVelo0 : SrvParticlePosVelo1);

        D3D12_VIEWPORT viewport;
        viewport.TopLeftX = (n % m_widthInstances) * viewportWidth;
        viewport.TopLeftY = (n / m_widthInstances) * viewportHeight;
        viewport.Width = viewportWidth;
        viewport.Height = viewportHeight;
        viewport.MinDepth = D3D12_MIN_DEPTH;
        viewport.MaxDepth = D3D12_MAX_DEPTH;
        m_commandList->RSSetViewports(1, &viewport);

        CD3DX12_GPU_DESCRIPTOR_HANDLE srvHandle(m_srvUavHeap->GetGPUDescriptorHandleForHeapStart(), srvIndex, m_srvUavDescriptorSize);
        m_commandList->SetGraphicsRootDescriptorTable(RootParameterSRV, srvHandle);

        m_commandList->DrawInstanced(ParticleCount, 1, 0, 0);
    }

    m_commandList->RSSetViewports(1, &m_viewport);

    // Indicate that the back buffer will now be used to present.
    m_commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT));

    ThrowIfFailed(m_commandList->Close());
}
```



## <a name="descriptor-heap-methods"></a>Méthodes du tas du descripteur

Les tas de descripteurs ([**ID3D12DescriptorHeap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap)) héritent de [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable). Cela impose la responsabilité de la gestion de la résidence des tas de descripteurs sur les applications, tout comme les tas de ressources. Les méthodes de gestion des dépassements s’appliquent uniquement aux tas visibles du nuanceur, car les tas non visibles par le nuanceur ne sont pas visibles directement pour le GPU.

La méthode [**ID3D12Device :: GetDescriptorHandleIncrementSize**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize) permet aux applications de décaler manuellement des handles dans un tas (en produisant des handles dans n’importe quel emplacement dans un tas de descripteur). Le handle de l’emplacement de début du tas provient de [**ID3D12DescriptorHeap :: GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart) / [**ID3D12DescriptorHeap :: GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart). Le décalage s’effectue en ajoutant la taille d’incrément \* du nombre de descripteurs à décaler au début du tas du descripteur. Notez que la taille de l’incrément ne peut pas être considérée comme une taille d’octet puisque les applications ne doivent pas déréférencer des handles comme s’il s’agissait de mémoire : la mémoire pointée a une disposition non standardisée et peut varier même pour un appareil donné.

[**GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart) retourne un handle de processeur pour les tas de descripteurs visibles par l’UC. Elle retourne un handle NULL (et la couche de débogage signale une erreur) si le tas du descripteur n’est pas visible par l’UC.

[**GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart) retourne un handle GPU pour les tas de descripteurs visibles du nuanceur. Elle retourne un handle NULL (et la couche de débogage signale une erreur) si le tas du descripteur n’est pas visible par le nuanceur.

Par exemple, la création de vues de cible de rendu pour afficher du texte D2D à l’aide d’un appareil 11on12.


```C++
    // Create descriptor heaps.
    {
        // Describe and create a render target view (RTV) descriptor heap.
        D3D12_DESCRIPTOR_HEAP_DESC rtvHeapDesc = {};
        rtvHeapDesc.NumDescriptors = FrameCount;
        rtvHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_RTV;
        rtvHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_NONE;
        ThrowIfFailed(m_d3d12Device->CreateDescriptorHeap(&rtvHeapDesc, IID_PPV_ARGS(&m_rtvHeap)));

        m_rtvDescriptorSize = m_d3d12Device->GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_RTV);
    }

    // Create frame resources.
    {
        CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart());

        // Create a RTV, D2D render target, and a command allocator for each frame.
        for (UINT n = 0; n < FrameCount; n++)
        {
            ThrowIfFailed(m_swapChain->GetBuffer(n, IID_PPV_ARGS(&m_renderTargets[n])));
            m_d3d12Device->CreateRenderTargetView(m_renderTargets[n].Get(), nullptr, rtvHandle);

            // Create a wrapped 11On12 resource of this back buffer. Since we are 
            // rendering all D3D12 content first and then all D2D content, we specify 
            // the In resource state as RENDER_TARGET - because D3D12 will have last 
            // used it in this state - and the Out resource state as PRESENT. When 
            // ReleaseWrappedResources() is called on the 11On12 device, the resource 
            // will be transitioned to the PRESENT state.
            D3D11_RESOURCE_FLAGS d3d11Flags = { D3D11_BIND_RENDER_TARGET };
            ThrowIfFailed(m_d3d11On12Device->CreateWrappedResource(
                m_renderTargets[n].Get(),
                &d3d11Flags,
                D3D12_RESOURCE_STATE_RENDER_TARGET,
                D3D12_RESOURCE_STATE_PRESENT,
                IID_PPV_ARGS(&m_wrappedBackBuffers[n])
                ));

            // Create a render target for D2D to draw directly to this back buffer.
            ComPtr<IDXGISurface> surface;
            ThrowIfFailed(m_wrappedBackBuffers[n].As(&surface));
            ThrowIfFailed(m_d2dDeviceContext->CreateBitmapFromDxgiSurface(
                surface.Get(),
                &bitmapProperties,
                &m_d2dRenderTargets[n]
                ));

            rtvHandle.Offset(1, m_rtvDescriptorSize);

            ThrowIfFailed(m_d3d12Device->CreateCommandAllocator(D3D12_COMMAND_LIST_TYPE_DIRECT, IID_PPV_ARGS(&m_commandAllocators[n])));
        }
    
    }
```



## <a name="minimal-descriptor-heap-wrapper"></a>Wrapper de tas de descripteur minimal

Les développeurs d’applications souhaiteront probablement créer leur propre code d’assistance pour gérer les tas et les handles de descripteur. Un exemple de base est illustré ci-dessous. Des wrappers plus sophistiqués peuvent, par exemple, effectuer le suivi des types de descripteurs dans un segment de mémoire et stocker les arguments de création du descripteur.

``` syntax
class CDescriptorHeapWrapper
{
public:
    CDescriptorHeapWrapper() { memset(this, 0, sizeof(*this)); }

    HRESULT Create(
        ID3D12Device* pDevice, 
        D3D12_DESCRIPTOR_HEAP_TYPE Type, 
        UINT NumDescriptors, 
        bool bShaderVisible = false)
    {
        D3D12_DESCRIPTOR_HEAP_DESC Desc;
        Desc.Type = Type;
        Desc.NumDescriptors = NumDescriptors;
        Desc.Flags = (bShaderVisible ? D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE : D3D12_DESCRIPTOR_HEAP_FLAG_NONE);
       
        HRESULT hr = pDevice->CreateDescriptorHeap(&Desc, 
                               __uuidof(ID3D12DescriptorHeap), 
                               (void**)&pDH);
        if (FAILED(hr)) return hr;

        hCPUHeapStart = pDH->GetCPUDescriptorHandleForHeapStart();
        hGPUHeapStart = pDH->GetGPUDescriptorHandleForHeapStart();

        HandleIncrementSize = pDevice->GetDescriptorHandleIncrementSize(Desc.Type);
        return hr;
    }
    operator ID3D12DescriptorHeap*() { return pDH; }

    D3D12_CPU_DESCRIPTOR_HANDLE hCPU(UINT index)
    {
        return hCPUHeapStart.MakeOffsetted(index,HandleIncrementSize); 
    }
    D3D12_GPU_DESCRIPTOR_HANDLE hGPU(UINT index) 
    {
        assert(Desc.Flags&D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE); 
        return hGPUHeapStart.MakeOffsetted(index,HandleIncrementSize); 
    }
    D3D12_DESCRIPTOR_HEAP_DESC Desc;
    CComPtr<ID3D12DescriptorHeap> pDH;
    D3D12_CPU_DESCRIPTOR_HANDLE hCPUHeapStart;
    D3D12_GPU_DESCRIPTOR_HANDLE hGPUHeapStart;
    UINT HandleIncrementSize;
};
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Tas de descripteurs](descriptor-heaps.md)
</dt> </dl>

 

 