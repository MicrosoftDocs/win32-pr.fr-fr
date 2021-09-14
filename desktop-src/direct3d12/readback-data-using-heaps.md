---
title: Lire les données à l’aide d’une mémoire tampon
description: Pour lire des données à partir du GPU (par exemple, pour capturer une capture d’écran), vous utilisez un segment de mémoire readback.
ms.assetid: 2F515B2C-3317-4AA8-81E1-7762ED895F77
ms.localizationpriority: high
ms.topic: article
ms.date: 12/17/2018
ms.openlocfilehash: 752d97d517a48a38adabc7c8fe51d11d47c1d8d3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012903"
---
# <a name="read-back-data-via-a-buffer"></a>Lire les données à l’aide d’une mémoire tampon

Pour lire des données à partir du GPU (par exemple, pour capturer une capture d’écran), vous utilisez un segment de mémoire readback. Cette technique est liée au [chargement de données de texture par le biais d’une mémoire tampon](upload-and-readback-of-texture-data.md), à quelques différences près.

- Pour lire les données, vous créez un segment de mémoire avec le **D3D12_HEAP_TYPE** défini sur [D3D12_HEAP_TYPE_READBACK](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)au lieu de **D3D12_HEAP_TYPE_UPLOAD**.
- La ressource sur le tas de lecture différé doit toujours être un **D3D12_RESOURCE_DIMENSION_BUFFER**.
- Vous utilisez une clôture pour détecter le moment où le GPU termine le traitement d’une trame (quand il a terminé d’écrire des données dans votre tampon de sortie). Cela est important, car la méthode [**ID3D12Resource :: Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) ne se synchronise pas avec le GPU (à l’inverse, l’équivalent Direct3D 11 *est* synchronisé). Les appels de **carte** Direct3D 12 se comportent comme si vous appeliez l’équivalent Direct3D 11 avec l’indicateur NO_OVERWRITE.
- Une fois que les données sont prêtes (y compris les cloisonnements de ressources nécessaires), appelez [**ID3D12Resource :: Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) pour rendre les données readback visibles au processeur.

## <a name="code-example"></a>Exemple de code

L’exemple de code ci-dessous montre la structure générale du processus de lecture des données du GPU vers le processeur via une mémoire tampon.

```cppwinrt

// The output buffer (created below) is on a default heap, so only the GPU can access it.

D3D12_HEAP_PROPERTIES defaultHeapProperties{ CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT) };
D3D12_RESOURCE_DESC outputBufferDesc{ CD3DX12_RESOURCE_DESC::Buffer(outputBufferSize, D3D12_RESOURCE_FLAG_ALLOW_UNORDERED_ACCESS) };
winrt::com_ptr<::ID3D12Resource> outputBuffer;
winrt::check_hresult(d3d12Device->CreateCommittedResource(
    &defaultHeapProperties,
    D3D12_HEAP_FLAG_NONE,
    &outputBufferDesc,
    D3D12_RESOURCE_STATE_COPY_DEST,
    nullptr,
    __uuidof(outputBuffer),
    outputBuffer.put_void()));

// The readback buffer (created below) is on a readback heap, so that the CPU can access it.

D3D12_HEAP_PROPERTIES readbackHeapProperties{ CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_READBACK) };
D3D12_RESOURCE_DESC readbackBufferDesc{ CD3DX12_RESOURCE_DESC::Buffer(outputBufferSize) };
winrt::com_ptr<::ID3D12Resource> readbackBuffer;
winrt::check_hresult(d3d12Device->CreateCommittedResource(
    &readbackHeapProperties,
    D3D12_HEAP_FLAG_NONE,
    &readbackBufferDesc,
    D3D12_RESOURCE_STATE_COPY_DEST,
    nullptr,
    __uuidof(readbackBuffer),
    readbackBuffer.put_void()));

{
    D3D12_RESOURCE_BARRIER outputBufferResourceBarrier
    {
        CD3DX12_RESOURCE_BARRIER::Transition(
            outputBuffer.get(),
            D3D12_RESOURCE_STATE_COPY_DEST,
            D3D12_RESOURCE_STATE_COPY_SOURCE)
    };
    commandList->ResourceBarrier(1, &outputBufferResourceBarrier);
}

commandList->CopyResource(readbackBuffer.get(), outputBuffer.get());

// Code goes here to close, execute (and optionally reset) the command list, and also
// to use a fence to wait for the command queue.

// The code below assumes that the GPU wrote FLOATs to the buffer.

D3D12_RANGE readbackBufferRange{ 0, outputBufferSize };
FLOAT * pReadbackBufferData{};
winrt::check_hresult(
    readbackBuffer->Map
    (
        0,
        &readbackBufferRange,
        reinterpret_cast<void**>(&pReadbackBufferData)
    )
);

// Code goes here to access the data via pReadbackBufferData.

D3D12_RANGE emptyRange{ 0, 0 };
readbackBuffer->Unmap
(
    0,
    &emptyRange
);
```

Pour une implémentation complète d’une routine de capture d’écran qui lit la texture de la cible de rendu et l’écrit sur le disque sous la forme d’un fichier, consultez *DirectX Tool Kit for DX12* [Screengrab](https://github.com/microsoft/DirectXTK12/blob/master/Src/ScreenGrab.cpp).

## <a name="related-topics"></a>Rubriques connexes

* [Sous-allocation dans une mémoire tampon](large-buffers.md)
