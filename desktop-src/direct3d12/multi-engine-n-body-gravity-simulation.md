---
title: Simulation de gravité n-corps multi-moteur
description: L’exemple D3D12nBodyGravity montre comment effectuer un travail de calcul de manière asynchrone.
ms.assetid: B20C5575-0616-43F7-9AC9-5F802E5597B5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60782519de6f655882717c4ea657668129a6ce3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548517"
---
# <a name="multi-engine-n-body-gravity-simulation"></a>Simulation de gravité n-corps multi-moteur

L’exemple **D3D12nBodyGravity** montre comment effectuer un travail de calcul de manière asynchrone. L’exemple fait tourner un certain nombre de threads, chacun avec une file d’attente de commandes Compute, et planifie le travail de calcul sur le GPU qui effectue une simulation de gravité en n corps. Chaque thread opère sur deux mémoires tampons complètes de données de position et de vélocité. À chaque itération, le nuanceur de calcul lit les données de position et de vélocité actuelles d’une mémoire tampon et écrit l’itération suivante dans l’autre mémoire tampon. Lorsque l’itération est terminée, le nuanceur de calcul permute la mémoire tampon qui sert à lire les données de position/vélocité et qui est le UAV pour l’écriture des mises à jour de position/vélocité en modifiant l’état de la ressource sur chaque mémoire tampon.

-   [Créer les signatures racines](#create-the-root-signatures)
-   [Créer les mémoires tampons SRV et UAV](#create-the-srv-and-uav-buffers)
-   [Créer les CBV et les mémoires tampons de vertex](#create-the-cbv-and-vertex-buffers)
-   [Synchroniser les threads de rendu et de calcul](#synchronize-the-rendering-and-compute-threads)
-   [Exécution de l'exemple](#run-the-sample)
-   [Rubriques connexes](#related-topics)

## <a name="create-the-root-signatures"></a>Créer les signatures racines

Nous commençons par créer un graphique et une signature racine de calcul, dans la méthode **LoadAssets** . Les deux signatures racines ont une vue de mémoire tampon constante racine (CBV) et une table de descripteurs SRV (Shader Resource View). La signature de la racine de calcul a également une table de descripteurs de vue d’accès non triée (UAV).

``` syntax
 // Create the root signatures.
       {
              CD3DX12_DESCRIPTOR_RANGE ranges[2];
              ranges[0].Init(D3D12_DESCRIPTOR_RANGE_TYPE_SRV, 1, 0);
              ranges[1].Init(D3D12_DESCRIPTOR_RANGE_TYPE_UAV, 1, 0);

              CD3DX12_ROOT_PARAMETER rootParameters[RootParametersCount];
              rootParameters[RootParameterCB].InitAsConstantBufferView(0, 0, D3D12_SHADER_VISIBILITY_ALL);
              rootParameters[RootParameterSRV].InitAsDescriptorTable(1, &ranges[0], D3D12_SHADER_VISIBILITY_VERTEX);
              rootParameters[RootParameterUAV].InitAsDescriptorTable(1, &ranges[1], D3D12_SHADER_VISIBILITY_ALL);

              // The rendering pipeline does not need the UAV parameter.
              CD3DX12_ROOT_SIGNATURE_DESC rootSignatureDesc;
              rootSignatureDesc.Init(_countof(rootParameters) - 1, rootParameters, 0, nullptr, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT);

              ComPtr<ID3DBlob> signature;
              ComPtr<ID3DBlob> error;
              ThrowIfFailed(D3D12SerializeRootSignature(&rootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
              ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_rootSignature)));

              // Create compute signature. Must change visibility for the SRV.
              rootParameters[RootParameterSRV].ShaderVisibility = D3D12_SHADER_VISIBILITY_ALL;

              CD3DX12_ROOT_SIGNATURE_DESC computeRootSignatureDesc(_countof(rootParameters), rootParameters, 0, nullptr);
              ThrowIfFailed(D3D12SerializeRootSignature(&computeRootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));

              ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_computeRootSignature)));
       }
```



| Workflow d’appel                                                             | Paramètres                                                            |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------|
| [**\_Plage du descripteur CD3DX12 \_**](cd3dx12-descriptor-range.md)        | [**\_Type de plage du descripteur D3D12 \_ \_**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) |
| [**\_Paramètre racine \_ CD3DX12**](cd3dx12-root-parameter.md)            | [**\_Visibilité du nuanceur D3D12 \_**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_visibility)          |
| [**Description de la \_ signature racine CD3DX12 \_ \_**](cd3dx12-root-signature-desc.md) | [**\_Indicateurs de \_ signature \_ racine D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_signature_flags)   |
| [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))                                   |                                                                       |
| [**D3D12SerializeRootSignature**](/windows/win32/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [**\_Version de \_ signature \_ racine D3D**](/windows/win32/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [**CreateRootSignature**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |
| [**Description de la \_ signature racine CD3DX12 \_ \_**](cd3dx12-root-signature-desc.md) |                                                                       |
| [**D3D12SerializeRootSignature**](/windows/win32/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [**\_Version de \_ signature \_ racine D3D**](/windows/win32/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [**CreateRootSignature**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |



 

## <a name="create-the-srv-and-uav-buffers"></a>Créer les mémoires tampons SRV et UAV

Les mémoires tampons SRV et UAV se composent d’un tableau de données de position et de vélocité.

``` syntax
 // Position and velocity data for the particles in the system.
       // Two buffers full of Particle data are utilized in this sample.
       // The compute thread alternates writing to each of them.
       // The render thread renders using the buffer that is not currently
       // in use by the compute shader.
       struct Particle
       {
              XMFLOAT4 position;
              XMFLOAT4 velocity;
       };
```



| Workflow d’appel                       | Paramètres |
|---------------------------------|------------|
| [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) |            |



 

## <a name="create-the-cbv-and-vertex-buffers"></a>Créer les CBV et les mémoires tampons de vertex

Pour le pipeline Graphics, le CBV est un **struct** contenant deux matrices utilisées par le nuanceur Geometry. Le nuanceur Geometry prend la position de chaque particule dans le système et génère une valeur Quad pour la représenter à l’aide de ces matrices.

``` syntax
 struct ConstantBufferGS
       {
              XMMATRIX worldViewProjection;
              XMMATRIX inverseView;

              // Constant buffers are 256-byte aligned in GPU memory. Padding is added
              // for convenience when computing the struct's size.
              float padding[32];
       };
```



| Workflow d’appel                       | Paramètres |
|---------------------------------|------------|
| [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) |            |



 

Par conséquent, la mémoire tampon de vertex utilisée par le nuanceur vertex ne contient en fait pas de données positionnelles.

``` syntax
 // "Vertex" definition for particles. Triangle vertices are generated 
       // by the geometry shader. Color data will be assigned to those 
       // vertices via this struct.
       struct ParticleVertex
       {
              XMFLOAT4 color;
       };
```



| Workflow d’appel                       | Paramètres |
|---------------------------------|------------|
| [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) |            |



 

Pour le pipeline de calcul, CBV est un **struct** contenant des constantes utilisées par la simulation de gravité à n corps dans le nuanceur de calcul.

``` syntax
 struct ConstantBufferCS
       {
              UINT param[4];
              float paramf[4];
       };
```

## <a name="synchronize-the-rendering-and-compute-threads"></a>Synchroniser les threads de rendu et de calcul

Une fois les tampons initialisés, le travail de rendu et de calcul commence. Le thread de calcul va changer l’état des deux mémoires tampons de position/vélocité entre SRV et UAV lorsqu’il itère sur la simulation, et le thread de rendu doit s’assurer qu’il planifie le travail sur le pipeline graphique qui opère sur le SRV. Les délimiteurs sont utilisés pour synchroniser l’accès aux deux mémoires tampons.

Sur le thread de rendu :

``` syntax
// Render the scene.
void D3D12nBodyGravity::OnRender()
{
       // Let the compute thread know that a new frame is being rendered.
       for (int n = 0; n < ThreadCount; n++)
       {
              InterlockedExchange(&m_renderContextFenceValues[n], m_renderContextFenceValue);
       }

       // Compute work must be completed before the frame can render or else the SRV 
       // will be in the wrong state.
       for (UINT n = 0; n < ThreadCount; n++)
       {
              UINT64 threadFenceValue = InterlockedGetValue(&m_threadFenceValues[n]);
              if (m_threadFences[n]->GetCompletedValue() < threadFenceValue)
              {
                     // Instruct the rendering command queue to wait for the current 
                     // compute work to complete.
                     ThrowIfFailed(m_commandQueue->Wait(m_threadFences[n].Get(), threadFenceValue));
              }
       }

       // Record all the commands we need to render the scene into the command list.
       PopulateCommandList();

       // Execute the command list.
       ID3D12CommandList* ppCommandLists[] = { m_commandList.Get() };
       m_commandQueue->ExecuteCommandLists(_countof(ppCommandLists), ppCommandLists);

       // Present the frame.
       ThrowIfFailed(m_swapChain->Present(0, 0));

       MoveToNextFrame();
}
```



| Workflow d’appel                                                              | Paramètres |
|------------------------------------------------------------------------|------------|
| [**Interlockedexchang**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedexchange)                  |            |
| [**InterlockedGetValue**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedcompareexchange)           |            |
| [**GetCompletedValue**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue)             |            |
| [**Wait**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait)                                |            |
| [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist)                         |            |
| [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)  |            |
| [**IDXGISwapChain1::Present1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) |            |



 

Pour simplifier l’exemple un peu, le thread de calcul attend que le GPU termine chaque itération avant de planifier davantage de travail de calcul. En pratique, les applications souhaiteront probablement garder la file d’attente de calcul pleine pour obtenir des performances maximales du GPU.

Sur le thread Compute :

``` syntax
DWORD D3D12nBodyGravity::AsyncComputeThreadProc(int threadIndex)
{
       ID3D12CommandQueue* pCommandQueue = m_computeCommandQueue[threadIndex].Get();
       ID3D12CommandAllocator* pCommandAllocator = m_computeAllocator[threadIndex].Get();
       ID3D12GraphicsCommandList* pCommandList = m_computeCommandList[threadIndex].Get();
       ID3D12Fence* pFence = m_threadFences[threadIndex].Get();

       while (0 == InterlockedGetValue(&m_terminating))
       {
              // Run the particle simulation.
              Simulate(threadIndex);

              // Close and execute the command list.
              ThrowIfFailed(pCommandList->Close());
              ID3D12CommandList* ppCommandLists[] = { pCommandList };

              pCommandQueue->ExecuteCommandLists(1, ppCommandLists);

              // Wait for the compute shader to complete the simulation.
              UINT64 threadFenceValue = InterlockedIncrement(&m_threadFenceValues[threadIndex]);
              ThrowIfFailed(pCommandQueue->Signal(pFence, threadFenceValue));
              ThrowIfFailed(pFence->SetEventOnCompletion(threadFenceValue, m_threadFenceEvents[threadIndex]));
              WaitForSingleObject(m_threadFenceEvents[threadIndex], INFINITE);

              // Wait for the render thread to be done with the SRV so that
              // the next frame in the simulation can run.
              UINT64 renderContextFenceValue = InterlockedGetValue(&m_renderContextFenceValues[threadIndex]);
              if (m_renderContextFence->GetCompletedValue() < renderContextFenceValue)
              {
                     ThrowIfFailed(pCommandQueue->Wait(m_renderContextFence.Get(), renderContextFenceValue));
                     InterlockedExchange(&m_renderContextFenceValues[threadIndex], 0);
              }

              // Swap the indices to the SRV and UAV.
              m_srvIndex[threadIndex] = 1 - m_srvIndex[threadIndex];

              // Prepare for the next frame.
              ThrowIfFailed(pCommandAllocator->Reset());
              ThrowIfFailed(pCommandList->Reset(pCommandAllocator, m_computeState.Get()));
       }

       return 0;
}
```



| Workflow d’appel                                                                   | Paramètres |
|-----------------------------------------------------------------------------|------------|
| [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue)                            |            |
| [**ID3D12CommandAllocator**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandallocator)                    |            |
| [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)              |            |
| [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence)                                          |            |
| [**InterlockedGetValue**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedcompareexchange)                |            |
| [**Fermer**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)                            |            |
| [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist)                              |            |
| [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)       |            |
| [**InterlockedIncrement**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedincrement)                     |            |
| [**Témoin**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)                                 |            |
| [**SetEventOnCompletion**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion)            |            |
| [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)                         |            |
| [**InterlockedGetValue**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedcompareexchange)                |            |
| [**GetCompletedValue**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue)                  |            |
| [**Wait**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait)                                     |            |
| [**Interlockedexchang**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedexchange)                       |            |
| [**ID3D12CommandAllocator :: Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset)       |            |
| [**ID3D12GraphicsCommandList :: Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset) |            |



 

## <a name="run-the-sample"></a>Exécution de l'exemple

![capture d’écran de la dernière simulation de gravité n Body](images/nbodygravity.png)

## <a name="related-topics"></a>Rubriques connexes

[Guide pas à pas du code D3D12](d3d12-code-walk-throughs.md)

[Synchronisation multi-moteur](./user-mode-heap-synchronization.md)