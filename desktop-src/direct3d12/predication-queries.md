---
title: Requêtes de prédicat
description: L’exemple D3D12PredicationQueries illustre l’élimination d’occlusion à l’aide de tas et de prédicats de requête DirectX 12. La procédure pas à pas décrit le code supplémentaire nécessaire pour étendre l’exemple HelloConstBuffer afin de gérer les requêtes de prédicat.
ms.assetid: F61817BB-45BC-4977-BE4A-EE0FDAFBCB57
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d37bd4653ec7610e36214cce31955f1742e5b27a42a381cc2aa7d758daaf5b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733392"
---
# <a name="predication-queries"></a>Requêtes de prédicat

L’exemple **D3D12PredicationQueries** illustre l’élimination d’occlusion à l’aide de tas et de prédicats de requête DirectX 12. La procédure pas à pas décrit le code supplémentaire nécessaire pour étendre l’exemple **HelloConstBuffer** afin de gérer les requêtes de prédicat.

-   [Créer un tas de descripteur de stencil de profondeur et un tas de requêtes d’occlusion](#create-a-depth-stencil-descriptor-heap-and-an-occlusion-query-heap)
-   [Activer la fusion alpha](#enable-alpha-blending)
-   [Désactiver les écritures de couleur et de profondeur](#disable-color-and-depth-writes)
-   [Créer une mémoire tampon pour stocker les résultats de la requête](#create-a-buffer-to-store-the-results-of-the-query)
-   [Dessinez les quatre cœurs et exécutez et résolvez la requête d’occlusion](#draw-the-quads-and-perform-and-resolve-the-occlusion-query)
-   [Exécuter l’exemple](#run-the-sample)
-   [Rubriques connexes](#related-topics)

## <a name="create-a-depth-stencil-descriptor-heap-and-an-occlusion-query-heap"></a>Créer un tas de descripteur de stencil de profondeur et un tas de requêtes d’occlusion

Dans la méthode **LoadPipeline** , créez un tas de descripteur de stencil de profondeur.

``` syntax
              // Describe and create a depth stencil view (DSV) descriptor heap.
              D3D12_DESCRIPTOR_HEAP_DESC dsvHeapDesc = {};
              dsvHeapDesc.NumDescriptors = 1;
              dsvHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_DSV;
              dsvHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_NONE;
              ThrowIfFailed(m_device->CreateDescriptorHeap(&dsvHeapDesc, IID_PPV_ARGS(&m_dsvHeap)));
```



<table>
<thead>
<tr class="header">
<th>Workflow d’appel</th>
<th>Paramètres</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc"><strong>D3D12_DESCRIPTOR_HEAP_DESC</strong></a></td>
<td><dl><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type"><strong>D3D12_DESCRIPTOR_HEAP_TYPE</strong></a><br />
[<strong>D3D12_DESCRIPTOR_HEAP_FLAG</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_descriptor_heap_flags)<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap"><strong>CreateDescriptorHeap</strong></a></td>

</tr>
</tbody>
</table>



 

Dans la méthode **LoadAssets** , créez un tas pour les requêtes d’occlusion.

``` syntax
     // Describe and create a heap for occlusion queries.
              D3D12_QUERY_HEAP_DESC queryHeapDesc = {};
              queryHeapDesc.Count = 1;
              queryHeapDesc.Type = D3D12_QUERY_HEAP_TYPE_OCCLUSION;
              ThrowIfFailed(m_device->CreateQueryHeap(&queryHeapDesc, IID_PPV_ARGS(&m_queryHeap)));
```



| Workflow d’appel                                                 | Paramètres                                                |
|-----------------------------------------------------------|-----------------------------------------------------------|
| [**Description du tas de la \_ requête D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_heap_desc) | [**\_Type de \_ segment de requête D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type) |
| [**CreateQueryHeap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createqueryheap)   |                                                           |



 

## <a name="enable-alpha-blending"></a>Activer la fusion alpha

Cet exemple dessine deux Quad et illustre une requête d’occlusion binaire. Le quadruple au premier plan s’anime à travers l’écran, et celui à l’arrière sera parfois bloqués. Dans la méthode **LoadAssets** , la fusion alpha est activée pour cet exemple afin que nous puissions voir à quel point D3D prend en compte les quadruples bloqués.

``` syntax
     // Enable alpha blending so we can visualize the occlusion query results.
              CD3DX12_BLEND_DESC blendDesc(CD3DX12_DEFAULT);
              blendDesc.RenderTarget[0] =
              {
                     TRUE, FALSE,
                     D3D12_BLEND_SRC_ALPHA, D3D12_BLEND_INV_SRC_ALPHA, D3D12_BLEND_OP_ADD,
                     D3D12_BLEND_ONE, D3D12_BLEND_ZERO, D3D12_BLEND_OP_ADD,
                     D3D12_LOGIC_OP_NOOP,
                     D3D12_COLOR_WRITE_ENABLE_ALL,
              };
```



<table>
<thead>
<tr class="header">
<th>Workflow d’appel</th>
<th>Paramètres</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="cd3dx12-blend-desc.md"><strong>CD3DX12_BLEND_DESC</strong></a></td>
<td><dl><a href="cd3dx12-default.md"><strong>CD3DX12_DEFAULT</strong></a><br />
[<strong>D3D12_BLEND</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_blend)<br />
[<strong>D3D12_BLEND_OP</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_blend_op)<br />
[<strong>D3D12_LOGIC_OP</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_logic_op)<br />
[<strong>D3D12_COLOR_WRITE_ENABLE</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_color_write_enable)<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="disable-color-and-depth-writes"></a>Désactiver les écritures de couleur et de profondeur

La requête d’occlusion est effectuée en rendant un quadruple qui couvre la même zone que le quadruple dont vous souhaitez tester la visibilité. Dans des scènes plus complexes, la requête serait probablement un volume englobant, plutôt qu’un simple quadruple. Dans les deux cas, un nouvel état de pipeline est créé, ce qui désactive l’écriture dans la cible de rendu et la mémoire tampon z afin que la requête d’occlusion proprement dite n’affecte pas la sortie visible de la passe de rendu.

Dans la méthode **LoadAssets** , désactivez les écritures de couleur et les écritures de profondeur pour l’état de la requête d’occlusion.

``` syntax
 // Disable color writes and depth writes for the occlusion query's state.
              psoDesc.BlendState.RenderTarget[0].RenderTargetWriteMask = 0;
              psoDesc.DepthStencilState.DepthWriteMask = D3D12_DEPTH_WRITE_MASK_ZERO;

              ThrowIfFailed(m_device->CreateGraphicsPipelineState(&psoDesc, IID_PPV_ARGS(&m_queryState)));
```



| Workflow d’appel                                                                            | Paramètres                                                  |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [**Description de l' \_ \_ État du pipeline GRAPHICs D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) | [**\_Masque d' \_ écriture de profondeur D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_depth_write_mask) |
| [**CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate)      |                                                             |



 

## <a name="create-a-buffer-to-store-the-results-of-the-query"></a>Créer une mémoire tampon pour stocker les résultats de la requête

Dans la méthode **LoadAssets** , une mémoire tampon doit être créée pour stocker les résultats de la requête. Chaque requête nécessite 8 octets d’espace dans la mémoire du GPU. Cet exemple exécute une seule requête et, pour des raisons de simplicité et de lisibilité, crée une mémoire tampon exactement de cette taille (même si cet appel de fonction allouera une page de 64 Ko de mémoire GPU, la plupart des applications réelles créeraient probablement une mémoire tampon plus grande).

``` syntax
 // Create the query result buffer.
              CD3DX12_HEAP_PROPERTIES heapProps(D3D12_HEAP_TYPE_DEFAULT);
              auto queryBufferDesc = CD3DX12_RESOURCE_DESC::Buffer(8);
              ThrowIfFailed(m_device->CreateCommittedResource(
                     &heapProps,
                     D3D12_HEAP_FLAG_NONE,
                     &queryBufferDesc,
                     D3D12_RESOURCE_STATE_GENERIC_READ,
                     nullptr,
                     IID_PPV_ARGS(&m_queryResult)
                     ));
```



<table>
<thead>
<tr class="header">
<th>Workflow d’appel</th>
<th>Paramètres</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></td>
<td><dl><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a><br />
[<strong>D3D12_HEAP_TYPE</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_heap_type)<br />
[<strong>D3D12_HEAP_FLAG</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_heap_flags)<br />
[<strong>CD3DX12_RESOURCE_DESC</strong>] (cd3dx12-resource-desc.md)<br />
[<strong>D3D12_RESOURCE_STATES</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_resource_states)<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="draw-the-quads-and-perform-and-resolve-the-occlusion-query"></a>Dessinez les quatre cœurs et exécutez et résolvez la requête d’occlusion

Une fois l’installation terminée, la boucle principale est mise à jour dans la méthode **PopulateCommandLists** .

<dl> 1. Dessinez les quadruples de l’arrière vers l’avant pour que l’effet de transparence fonctionne correctement. Le fait de redessiner le Quad à l’avant est prédicat sur le résultat de la requête du frame précédent et est une technique relativement courante.  
2. Modifiez l’PSO pour désactiver les écritures de la cible de rendu et du stencil de profondeur.  
3. Exécutez la requête d’occlusion.  
4. Résolvez la requête d’occlusion.  
</dl>

``` syntax
       // Draw the quads and perform the occlusion query.
       {
              CD3DX12_GPU_DESCRIPTOR_HANDLE cbvFarQuad(m_cbvHeap->GetGPUDescriptorHandleForHeapStart(), m_frameIndex * CbvCountPerFrame, m_cbvSrvDescriptorSize);
              CD3DX12_GPU_DESCRIPTOR_HANDLE cbvNearQuad(cbvFarQuad, m_cbvSrvDescriptorSize);

              m_commandList->IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP);
              m_commandList->IASetVertexBuffers(0, 1, &m_vertexBufferView);

              // Draw the far quad conditionally based on the result of the occlusion query
              // from the previous frame.
              m_commandList->SetGraphicsRootDescriptorTable(0, cbvFarQuad);
              m_commandList->SetPredication(m_queryResult.Get(), 0, D3D12_PREDICATION_OP_EQUAL_ZERO);
              m_commandList->DrawInstanced(4, 1, 0, 0);

              // Disable predication and always draw the near quad.
              m_commandList->SetPredication(nullptr, 0, D3D12_PREDICATION_OP_EQUAL_ZERO);
              m_commandList->SetGraphicsRootDescriptorTable(0, cbvNearQuad);
              m_commandList->DrawInstanced(4, 1, 4, 0);

              // Run the occlusion query with the bounding box quad.
              m_commandList->SetGraphicsRootDescriptorTable(0, cbvFarQuad);
              m_commandList->SetPipelineState(m_queryState.Get());
              m_commandList->BeginQuery(m_queryHeap.Get(), D3D12_QUERY_TYPE_BINARY_OCCLUSION, 0);
              m_commandList->DrawInstanced(4, 1, 8, 0);
              m_commandList->EndQuery(m_queryHeap.Get(), D3D12_QUERY_TYPE_BINARY_OCCLUSION, 0);

              // Resolve the occlusion query and store the results in the query result buffer
              // to be used on the subsequent frame.
              m_commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_queryResult.Get(), D3D12_RESOURCE_STATE_GENERIC_READ, D3D12_RESOURCE_STATE_COPY_DEST));
              m_commandList->ResolveQueryData(m_queryHeap.Get(), D3D12_QUERY_TYPE_BINARY_OCCLUSION, 0, 1, m_queryResult.Get(), 0);
              m_commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_queryResult.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_GENERIC_READ));
       }
```



<table>
<thead>
<tr class="header">
<th>Workflow d’appel</th>
<th>Paramètres</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="cd3dx12-gpu-descriptor-handle.md"><strong>CD3DX12_GPU_DESCRIPTOR_HANDLE</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart"><strong>GetGPUDescriptorHandleForHeapStart</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology"><strong>IASetPrimitiveTopology</strong></a></td>
<td><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology"><strong>D3D_PRIMITIVE_TOPOLOGY</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers"><strong>IASetVertexBuffers</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication"><strong>SetPredication</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op"><strong>D3D12_PREDICATION_OP</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication"><strong>SetPredication</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op"><strong>D3D12_PREDICATION_OP</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate"><strong>SetPipelineState</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery"><strong>BeginQuery</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery"><strong>EndQuery</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></td>
<td><dl><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a><br />
[<strong>D3D12_RESOURCE_STATES</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_resource_states)<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata"><strong>ResolveQueryData</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></td>
<td><dl><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a><br />
[<strong>D3D12_RESOURCE_STATES</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_resource_states)<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="run-the-sample"></a>Exécution de l'exemple

Non bloqués :

![deux zones non bloqués](images/not-occluded.png)

Bloqués

![bloqués entièrement](images/occluded.png)

Bloqués partiel :

![une seule zone partiellement bloqués](images/partially-occluded.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Walk-Throughs de code D3D12](d3d12-code-walk-throughs.md)
</dt> <dt>

[Prédicat](predication.md)
</dt> <dt>

[Requêtes](queries.md)
</dt> </dl>

 

 
