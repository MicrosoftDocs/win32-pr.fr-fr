---
title: Exemple de code dans la référence D3D12
description: Explique l’utilisation de l’exemple de code dans la documentation de Direct3D 12.
ms.assetid: C2323482-D06D-43B7-9BDE-BFB9A6A6B70D
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d65dd8db64dd829a7a318717e44a64ea189c7a3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012936"
---
# <a name="example-code-in-the-d3d12-reference"></a>Exemple de code dans la référence D3D12

Explique l’utilisation de l’exemple de code dans la documentation de Direct3D 12.

-   [Exemple de code d’extrait](#example-snippet-code)
-   [Rubriques connexes](#related-topics)

## <a name="example-snippet-code"></a>Exemple de code d’extrait

L’exemple de code présenté dans la référence Direct3D 12 n’est pas un code compilable ou en mode d’exécution, il s’agit simplement d’un extrait de code qui donne un exemple de la façon dont l’API est appelée. Certains exemples répertorient les variables globales et les membres de classe utilisés par les appels, par exemple :

Objets de pipeline globaux.


```C++
D3D12_VIEWPORT m_viewport;
D3D12_RECT m_scissorRect;
ComPtr<IDXGISwapChain3> m_swapChain;
ComPtr<ID3D12Device> m_device;
ComPtr<ID3D12Resource> m_renderTargets[FrameCount];
ComPtr<ID3D12CommandAllocator> m_commandAllocator;
ComPtr<ID3D12CommandQueue> m_commandQueue;
ComPtr<ID3D12RootSignature> m_rootSignature;
ComPtr<ID3D12DescriptorHeap> m_rtvHeap;
ComPtr<ID3D12PipelineState> m_pipelineState;
ComPtr<ID3D12GraphicsCommandList> m_commandList;
UINT m_rtvDescriptorSize;
```



Remplissage des listes de commandes.


```C++
// Command list allocators can only be reset when the associated 
// command lists have finished execution on the GPU; apps should use 
// fences to determine GPU execution progress.
ThrowIfFailed(m_commandAllocator->Reset());

// However, when ExecuteCommandList() is called on a particular command 
// list, that command list can then be reset at any time and must be before 
// re-recording.
ThrowIfFailed(m_commandList->Reset(m_commandAllocator.Get(), m_pipelineState.Get()));

// Set necessary state.
m_commandList->SetGraphicsRootSignature(m_rootSignature.Get());
m_commandList->RSSetViewports(1, &m_viewport);
m_commandList->RSSetScissorRects(1, &m_scissorRect);

// Indicate that the back buffer will be used as a render target.
auto barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET);
m_commandList->ResourceBarrier(1, &barrier);

CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
m_commandList->OMSetRenderTargets(1, &rtvHandle, FALSE, nullptr);

// Record commands.
const float clearColor[] = { 0.0f, 0.2f, 0.4f, 1.0f };
m_commandList->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
m_commandList->IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST);
m_commandList->IASetVertexBuffers(0, 1, &m_vertexBufferView);
m_commandList->DrawInstanced(3, 1, 0, 0);

// Indicate that the back buffer will now be used to present.
m_commandList->ResourceBarrier(1, &barrier);
barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT);
ThrowIfFailed(m_commandList->Close());
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’un composant Direct3D 12 de base](creating-a-basic-direct3d-12-component.md)
</dt> <dt>

[Référence de Direct3D 12](direct3d-12-reference.md)
</dt> <dt>

[Walk-Throughs de code D3D12](d3d12-code-walk-throughs.md)
</dt> <dt>

[Exemples fonctionnels](working-samples.md)
</dt> </dl>

 

 




