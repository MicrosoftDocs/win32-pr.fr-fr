---
title: Création et enregistrement de listes de commandes et de bundles
description: Cette rubrique décrit l’enregistrement des listes de commandes et des offres groupées dans les applications Direct3D 12. Les listes de commandes et les offres groupées permettent aux applications d’enregistrer des appels de dessin ou de modification d’État pour une exécution ultérieure sur l’unité de traitement graphique (GPU).
ms.assetid: 0074B796-33A4-4AA1-A4E7-48A2A63F25B7
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5ef2b54138cf3a08b85e3e8cc31f97cbe66abf6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548571"
---
# <a name="creating-and-recording-command-lists-and-bundles"></a>Création et enregistrement de listes de commandes et de bundles

Cette rubrique décrit l’enregistrement des listes de commandes et des offres groupées dans les applications Direct3D 12. Les listes de commandes et les offres groupées permettent aux applications d’enregistrer des appels de dessin ou de modification d’État pour une exécution ultérieure sur l’unité de traitement graphique (GPU).

Au-delà des listes de commandes, l’API exploite les fonctionnalités présentes dans le matériel GPU en ajoutant un second niveau de listes de commandes, appelées « *bottes*». L’objectif des offres groupées est de permettre aux applications de regrouper un petit nombre de commandes API pour une exécution ultérieure. Au moment de la création du bundle, le pilote effectue autant de prétraitement que possible pour une exécution ultérieure. Les offres groupées sont conçues pour être utilisées et réutilisées plusieurs fois. En revanche, les listes de commandes ne sont généralement exécutées qu’une seule fois. Toutefois, une liste de commandes *peut* être exécutée plusieurs fois (tant que l’application s’assure que les exécutions précédentes sont terminées avant d’envoyer de nouvelles exécutions).

Toutefois, en règle générale, la génération d’appels d’API dans des offres groupées, les appels d’API et les offres groupées dans des listes de commandes, et les listes de commandes dans un frame unique, est illustrée dans le diagramme suivant, notant la réutilisation de **Bundle 1** dans la **liste de commandes 1** et la **liste de commandes 2**.

![génération de commandes, de regroupements et de listes de commandes dans des frames](images/gpu-workitems.png)

Il existe différentes restrictions pour créer et exécuter des offres groupées et des listes de commandes directes, et ces différences sont indiquées dans cette rubrique.

## <a name="creating-command-lists"></a>Création de listes de commandes

Les listes de commandes directes et les offres groupées sont créées en appelant [**ID3D12Device :: CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) ou [**ID3D12Device4 :: CreateCommandList1**](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-createcommandlist1).

Utilisez [**ID3D12Device4 :: CreateCommandList1**](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-createcommandlist1) pour créer une liste de commandes fermée, au lieu de créer une nouvelle liste et de la fermer immédiatement. Cela évite l’inefficacité de la création d’une liste avec un allocateur et un PSO, mais pas leur utilisation.

[**ID3D12Device :: CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) accepte les paramètres suivants comme entrée :

### <a name="d3d12_command_list_type"></a>\_Type de \_ liste de commandes D3D12 \_

L’énumération de [**\_ type de \_ liste \_ de commandes D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) indique le type de liste de commandes en cours de création. Il peut s’agir d’une liste de commandes directe, d’un bundle, d’une liste de commandes de calcul ou d’une liste de commandes de copie.

### <a name="id3d12commandallocator"></a>ID3D12CommandAllocator

Un allocateur de commande permet à l’application de gérer la mémoire allouée pour les listes de commandes. L’allocateur de commande est créé en appelant [**CreateCommandAllocator**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator). Lors de la création d’une liste de commandes, le type de liste de commandes de l’allocateur, spécifié par le [**\_ type de \_ liste \_ de commandes D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type), doit correspondre au type de liste de commandes en cours de création. Un allocateur donné peut être associé à une seule liste de commandes en *cours d’enregistrement* à la fois, même si l’un des allocateurs de commandes peut être utilisé pour créer un nombre quelconque d’objets [**GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) .

Pour récupérer la mémoire allouée par un allocateur de commande, une application appelle [**ID3D12CommandAllocator :: Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset). Cela permet de réutiliser l’allocateur pour les nouveaux commandes, mais ne réduit pas sa taille sous-jacente. Mais avant cela, l’application doit s’assurer que le GPU n’exécute plus les listes de commandes associées à l’allocateur. dans le cas contraire, l’appel échoue. Notez également que cette API n’est pas de thread libre et ne peut donc pas être appelée sur le même allocateur en même temps à partir de plusieurs threads.

### <a name="id3d12pipelinestate"></a>ID3D12PipelineState

État initial du pipeline pour la liste de commandes. Dans Microsoft Direct3D 12, la plupart des États de pipeline de graphiques sont définis dans une liste de commandes à l’aide de l’objet [**ID3D12PipelineState**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinestate) . Une application crée un grand nombre de ces éléments, généralement pendant l’initialisation de l’application, puis l’État est mis à jour en modifiant l’objet d’État actuellement lié à l’aide de [**ID3D12GraphicsCommandList :: SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate). Pour plus d’informations sur les objets d’état de pipeline, consultez [gestion de l’état des pipelines graphiques dans Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).

Notez que les offres groupées n’héritent pas de l’état du pipeline défini par les appels précédents dans les listes de commandes directes qui sont leurs parents.

Si ce paramètre a la valeur NULL, un État par défaut est utilisé.

## <a name="recording-command-lists"></a>Enregistrement des listes de commandes

Immédiatement après sa création, les listes de commandes sont dans l’état d’enregistrement. Vous pouvez également réutiliser une liste de commandes existante en appelant I [**D3D12GraphicsCommandList :: Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset), qui laisse également la liste de commandes dans l’État Recording. Contrairement à [**ID3D12CommandAllocator :: Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset), vous pouvez appeler **Reset** lorsque la liste de commandes est toujours en cours d’exécution. Un modèle classique consiste à soumettre une liste de commandes, puis à la réinitialiser immédiatement pour réutiliser la mémoire allouée pour une autre liste de commandes. Notez qu’une seule liste de commandes associée à chaque allocateur de commande peut être dans un état d’enregistrement à un moment donné.

Une fois qu’une liste de commandes est dans l’État enregistrement, il vous suffit d’appeler les méthodes de l’interface [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) pour ajouter des commandes à la liste. La plupart de ces méthodes activent les fonctionnalités Direct3D courantes qui seront familières aux développeurs Microsoft Direct3D 11. les autres API sont nouvelles pour Direct3D 12.

Après avoir ajouté des commandes à la liste de commandes, vous faites passer la liste de commandes de l’état d’enregistrement en appelant [**Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close).

Les allocateurs de commandes peuvent croître, mais ils ne peuvent pas être réduits, et la réutilisation des allocateurs doit être envisagée pour optimiser l’efficacité de votre application. Vous pouvez enregistrer plusieurs listes dans le même allocateur avant sa réinitialisation, à condition qu’une seule liste soit enregistrée à un moment donné. Vous pouvez visualiser chaque liste en tant que propriétaire d’une partie de l’allocateur, ce qui indique ce que [**ID3D12CommandQueue :: ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) exécutera.

Une stratégie de regroupement d’allocateur simple doit viser approximativement des `numCommandLists * MaxFrameLatency` allocateurs. Par exemple, si vous enregistrez 6 listes et que vous autorisez jusqu’à 3 images latentes, vous pouvez raisonnablement vous attendre à obtenir 18-20 allocators. Une stratégie de regroupement plus avancée, qui réutilise des allocateurs pour plusieurs listes sur le même thread, peut viser des `numRecordingThreads * MaxFrameLatency` allocateurs. À l’aide de l’exemple précédent, si 2 listes ont été enregistrées sur le thread A, 2 sur le thread B, 1 sur le thread C, et 1 sur le thread D, vous pouvez faire en sorte que les allocations 12-14 soient réalistes.

Utilisez une clôture pour déterminer quand un allocateur donné peut être réutilisé.

Comme les listes de commandes peuvent être réinitialisées immédiatement après l’exécution, elles peuvent être regroupées de façon triviale, et rajoutées au pool après chaque appel à [**ID3D12CommandQueue :: ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).

## <a name="example"></a>Exemple

Les extraits de code suivants illustrent la création et l’enregistrement d’une liste de commandes. Notez que cet exemple comprend les fonctionnalités Direct3D 12 suivantes :

-   Objets d’état de pipeline : ils permettent de définir la plupart des paramètres d’État du pipeline de rendu à partir d’une liste de commandes. Pour plus d’informations, consultez [gestion de l’état des pipelines graphiques dans Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).
-   Tas de descripteur : les applications utilisent des tas de descripteurs pour gérer la liaison de pipeline aux ressources mémoire.
-   Barrière des ressources : cette valeur est utilisée pour gérer la transition des ressources d’un État à un autre, par exemple d’une vue de cible de rendu vers une vue de ressource de nuanceur. Pour plus d’informations, consultez [utilisation de barrières de ressources pour synchroniser les États des ressources](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md).

Par exemple,


```C++
void D3D12HelloTriangle::LoadAssets()
{
    // Create an empty root signature.
    {
        CD3DX12_ROOT_SIGNATURE_DESC rootSignatureDesc;
        rootSignatureDesc.Init(0, nullptr, 0, nullptr, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT);

        ComPtr<ID3DBlob> signature;
        ComPtr<ID3DBlob> error;
        ThrowIfFailed(D3D12SerializeRootSignature(&rootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
        ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_rootSignature)));
    }

    // Create the pipeline state, which includes compiling and loading shaders.
    {
        ComPtr<ID3DBlob> vertexShader;
        ComPtr<ID3DBlob> pixelShader;

#if defined(_DEBUG)
        // Enable better shader debugging with the graphics debugging tools.
        UINT compileFlags = D3DCOMPILE_DEBUG | D3DCOMPILE_SKIP_OPTIMIZATION;
#else
        UINT compileFlags = 0;
#endif

        ThrowIfFailed(D3DCompileFromFile(GetAssetFullPath(L"shaders.hlsl").c_str(), nullptr, nullptr, "VSMain", "vs_5_0", compileFlags, 0, &vertexShader, nullptr));
        ThrowIfFailed(D3DCompileFromFile(GetAssetFullPath(L"shaders.hlsl").c_str(), nullptr, nullptr, "PSMain", "ps_5_0", compileFlags, 0, &pixelShader, nullptr));

        // Define the vertex input layout.
        D3D12_INPUT_ELEMENT_DESC inputElementDescs[] =
        {
            { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 0, D3D12_INPUT_CLASSIFICATION_PER_VERTEX_DATA, 0 },
            { "COLOR", 0, DXGI_FORMAT_R32G32B32A32_FLOAT, 0, 12, D3D12_INPUT_CLASSIFICATION_PER_VERTEX_DATA, 0 }
        };

        // Describe and create the graphics pipeline state object (PSO).
        D3D12_GRAPHICS_PIPELINE_STATE_DESC psoDesc = {};
        psoDesc.InputLayout = { inputElementDescs, _countof(inputElementDescs) };
        psoDesc.pRootSignature = m_rootSignature.Get();
        psoDesc.VS = { reinterpret_cast<UINT8*>(vertexShader->GetBufferPointer()), vertexShader->GetBufferSize() };
        psoDesc.PS = { reinterpret_cast<UINT8*>(pixelShader->GetBufferPointer()), pixelShader->GetBufferSize() };
        psoDesc.RasterizerState = CD3DX12_RASTERIZER_DESC(D3D12_DEFAULT);
        psoDesc.BlendState = CD3DX12_BLEND_DESC(D3D12_DEFAULT);
        psoDesc.DepthStencilState.DepthEnable = FALSE;
        psoDesc.DepthStencilState.StencilEnable = FALSE;
        psoDesc.SampleMask = UINT_MAX;
        psoDesc.PrimitiveTopologyType = D3D12_PRIMITIVE_TOPOLOGY_TYPE_TRIANGLE;
        psoDesc.NumRenderTargets = 1;
        psoDesc.RTVFormats[0] = DXGI_FORMAT_R8G8B8A8_UNORM;
        psoDesc.SampleDesc.Count = 1;
        ThrowIfFailed(m_device->CreateGraphicsPipelineState(&psoDesc, IID_PPV_ARGS(&m_pipelineState)));
    }

    // Create the command list.
    ThrowIfFailed(m_device->CreateCommandList(0, D3D12_COMMAND_LIST_TYPE_DIRECT, m_commandAllocator.Get(), m_pipelineState.Get(), IID_PPV_ARGS(&m_commandList)));

    // Command lists are created in the recording state, but there is nothing
    // to record yet. The main loop expects it to be closed, so close it now.
    ThrowIfFailed(m_commandList->Close());

    // Create the vertex buffer.
    {
        // Define the geometry for a triangle.
        Vertex triangleVertices[] =
        {
            { { 0.0f, 0.25f * m_aspectRatio, 0.0f }, { 1.0f, 0.0f, 0.0f, 1.0f } },
            { { 0.25f, -0.25f * m_aspectRatio, 0.0f }, { 0.0f, 1.0f, 0.0f, 1.0f } },
            { { -0.25f, -0.25f * m_aspectRatio, 0.0f }, { 0.0f, 0.0f, 1.0f, 1.0f } }
        };

        const UINT vertexBufferSize = sizeof(triangleVertices);

        // Note: using upload heaps to transfer static data like vert buffers is not 
        // recommended. Every time the GPU needs it, the upload heap will be marshalled 
        // over. Please read up on Default Heap usage. An upload heap is used here for 
        // code simplicity and because there are very few verts to actually transfer.
        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &CD3DX12_RESOURCE_DESC::Buffer(vertexBufferSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_vertexBuffer)));

        // Copy the triangle data to the vertex buffer.
        UINT8* pVertexDataBegin;
        CD3DX12_RANGE readRange(0, 0);        // We do not intend to read from this resource on the CPU.
        ThrowIfFailed(m_vertexBuffer->Map(0, &readRange, reinterpret_cast<void**>(&pVertexDataBegin)));
        memcpy(pVertexDataBegin, triangleVertices, sizeof(triangleVertices));
        m_vertexBuffer->Unmap(0, nullptr);

        // Initialize the vertex buffer view.
        m_vertexBufferView.BufferLocation = m_vertexBuffer->GetGPUVirtualAddress();
        m_vertexBufferView.StrideInBytes = sizeof(Vertex);
        m_vertexBufferView.SizeInBytes = vertexBufferSize;
    }

    // Create synchronization objects and wait until assets have been uploaded to the GPU.
    {
        ThrowIfFailed(m_device->CreateFence(0, D3D12_FENCE_FLAG_NONE, IID_PPV_ARGS(&m_fence)));
        m_fenceValue = 1;

        // Create an event handle to use for frame synchronization.
        m_fenceEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);
        if (m_fenceEvent == nullptr)
        {
            ThrowIfFailed(HRESULT_FROM_WIN32(GetLastError()));
        }

        // Wait for the command list to execute; we are reusing the same command 
        // list in our main loop but for now, we just want to wait for setup to 
        // complete before continuing.
        WaitForPreviousFrame();
    }
}
```



Une fois qu’une liste de commandes a été créée et enregistrée, elle peut être exécutée à l’aide d’une file d’attente de commandes. Pour plus d’informations, consultez [exécution et synchronisation de listes de commandes](executing-and-synchronizing-command-lists.md).

## <a name="reference-counting"></a>Décompte de références

La plupart des API D3D12 continuent à utiliser le décompte de références suivant les conventions COM. L’une des exceptions notables concerne les API de liste de commandes Graphics D3D12. Toutes les API sur [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) ne contiennent pas de références aux objets passés à ces API. Cela signifie que les applications sont chargées de s’assurer qu’une liste de commandes n’est jamais soumise pour l’exécution qui fait référence à une ressource détruite.

## <a name="command-list-errors"></a>Erreurs de liste de commandes

La plupart des API sur [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) ne retournent pas d’erreurs. Les erreurs rencontrées lors de la création de la liste de commandes sont différées jusqu’à [**ID3D12GraphicsCommandList :: Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close). La seule exception est la \_ Suppression de l’appareil d’erreur dxgi \_ \_ , qui est encore différée. Notez que cela diffère de D3D11, où de nombreuses erreurs de validation de paramètres sont supprimées silencieusement et ne sont jamais retournées à l’appelant.

Les applications peuvent s’attendre à \_ voir \_ des erreurs de suppression d’appareil dxgi dans les appels d’API suivants :

-   Toute méthode de création de ressource
-   [**ID3D12Resource :: Map**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map)
-   [**IDXGISwapChain1::Present1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)
-   [**GetDeviceRemovedReason**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdeviceremovedreason)

## <a name="command-list-api-restrictions"></a>Restrictions de l’API de liste de commandes

Certaines API de liste de commandes peuvent être appelées uniquement sur certains types de listes de commandes. Le tableau ci-dessous montre les API de liste de commandes qui peuvent être appelées sur chaque type de liste de commandes. Il montre également les API qui sont valides pour appeler dans une [**passe de rendu D3D12**](./direct3d-12-render-passes.md). 

| Nom de l’API                                         | Graphiques | Compute | Copier | Bundle | Dans la passe de rendu |
|--------------------------------------------------|:--------:|:-------:|:----:|:------:|:--------------:|
| AtomicCopyBufferUINT                             | ✓        | ✓       | ✓    |        |                |
| AtomicCopyBufferUINT64                           | ✓        | ✓       | ✓    |        |                |
| BeginQuery                                       | ✓        |         |      |        | ✓              |
| BeginRenderPass                                  | ✓        |         |      |        |                |
| BuildRaytracingAccelerationStructure             | ✓        | ✓       |      |        |                |
| ClearDepthStencilView                            | ✓        |         |      |        |                |
| ClearRenderTargetView                            | ✓        |         |      |        |                |
| ClearState                                       | ✓        | ✓       |      |        |                |
| ClearUnorderedAccessViewFloat                    | ✓        | ✓       |      |        |                |
| ClearUnorderedAccessViewUint                     | ✓        | ✓       |      |        |                |
| CopyBufferRegion                                 | ✓        | ✓       | ✓    |        |                |
| CopyRaytracingAccelerationStructure              | ✓        | ✓       |      |        |                |
| CopyResource                                     | ✓        | ✓       | ✓    |        |                |
| CopyTextureRegion                                | ✓        | ✓       | ✓    |        |                |
| CopyTiles                                        | ✓        | ✓       | ✓    |        |                |
| DiscardResource                                  | ✓        | ✓       |      |        |                |
| Dispatch                                         | ✓        | ✓       |      | ✓      |                |
| DispatchRays                                     | ✓        | ✓       |      | ✓      |                |
| DrawIndexedInstanced                             | ✓        |         |      | ✓      | ✓              |
| DrawInstanced                                    | ✓        |         |      | ✓      | ✓              |
| EmitRaytracingAccelerationStructurePostbuildInfo | ✓        | ✓       |      |        |                |
| EndQuery                                         | ✓        | ✓       | ✓    |        | ✓              |
| EndRenderPass                                    | ✓        |         |      |        | ✓              |
| ExecuteBundle                                    | ✓        |         |      |        | ✓              |
| ExecuteIndirect                                  | ✓        | ✓       |      | ✓      | ✓              |
| ExecuteMetaCommand                               | ✓        | ✓       |      |        |                |
| IASetIndexBuffer                                 | ✓        |         |      | ✓      | ✓              |
| IASetPrimitiveTopology                           | ✓        |         |      | ✓      | ✓              |
| IASetVertexBuffers                               | ✓        |         |      | ✓      | ✓              |
| InitializeMetaCommand                            | ✓        | ✓       |      |        |                |
| OMSetBlendFactor                                 | ✓        |         |      | ✓      | ✓              |
| OMSetDepthBounds                                 | ✓        |         |      | ✓      | ✓              |
| OMSetRenderTargets                               | ✓        |         |      |        |                |
| OMSetStencilRef                                  | ✓        |         |      | ✓      | ✓              |
| ResolveQueryData                                 | ✓        | ✓       | ✓    |        |                |
| ResolveSubresource                               | ✓        |         |      |        |                |
| ResolveSubresourceRegion                         | ✓        |         |      |        |                |
| ResourceBarrier                                  | ✓        | ✓       | ✓    |        | ✓              |
| RSSetScissorRects                                | ✓        |         |      |        | ✓              |
| RSSetShadingRate                                 | ✓        |         |      | ✓      | ✓              |
| RSSetShadingRateImage                            | ✓        |         |      | ✓      | ✓              |
| RSSetViewports                                   | ✓        |         |      |        | ✓              |
| SetComputeRoot32BitConstant                      | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRoot32BitConstants                     | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRootConstantBufferView                 | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRootDescriptorTable                    | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRootShaderResourceView                 | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRootSignature                          | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRootUnorderedAccessView                | ✓        | ✓       |      | ✓      | ✓              |
| SetDescriptorHeaps                               | ✓        | ✓       |      | ✓      | ✓              |
| SetGraphicsRoot32BitConstant                     | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRoot32BitConstants                    | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRootConstantBufferView                | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRootDescriptorTable                   | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRootShaderResourceView                | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRootSignature                         | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRootUnorderedAccessView               | ✓        |         |      | ✓      | ✓              |
| SetPipelineState                                 | ✓        | ✓       |      | ✓      | ✓              |
| SetPipelineState1                                | ✓        | ✓       |      | ✓      |                |
| SetPredication                                   | ✓        | ✓       |      |        | ✓              |
| SetProtectedResourceSession                      | ✓        | ✓       | ✓    |        |                |
| SetSamplePositions                               | ✓        |         |      | ✓      | ✓              |
| SetViewInstanceMask                              | ✓        |         |      | ✓      | ✓              |
| SOSetTargets                                     | ✓        |         |      |        | ✓              |
| WriteBufferImmediate                             | ✓        | ✓       | ✓    | ✓      | ✓              |

## <a name="bundle-restrictions"></a>Restrictions de Bundle

Les restrictions permettent aux pilotes Direct3D 12 d’effectuer la majeure partie du travail associé aux offres groupées au moment de l’enregistrement, ce qui permet l’exécution de l’API [**ExecuteBundle**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) avec une faible charge. Tous les objets d’état de pipeline référencés par un bundle doivent avoir les mêmes formats de cible de rendu, format de mémoire tampon de profondeur et descriptions d’exemples.

Les appels d’API de liste de commandes suivants ne sont pas autorisés sur les listes de commandes créées avec le type de liste de commandes type : D3D12 \_ \_ \_ \_ Bundle :

-   Toute méthode Clear
-   Toute méthode de copie
-   [**DiscardResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource)
-   [**ExecuteBundle**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle)
-   [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)
-   [**ResolveSubresource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource)
-   [**SetPredication**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)
-   [**BeginQuery**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery)
-   [**EndQuery**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)
-   [**SOSetTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets)
-   [**OMSetRenderTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)
-   [**RSSetViewports**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports)
-   [**RSSetScissorRects**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects)

[**SetDescriptorHeaps**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps) peut être appelé sur un bundle, mais les tas du descripteur de Bundle doivent correspondre au tas du descripteur de liste de commandes appelant.

Si l’une de ces API est appelée sur un bundle, le runtime supprime l’appel. La couche de débogage génère une erreur à chaque fois que cela se produit.

## <a name="related-topics"></a>Rubriques connexes

[Envoi de travail dans Direct3D 12](command-queues-and-command-lists.md)