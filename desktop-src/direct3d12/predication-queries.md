---
title: Requêtes de prédicat
description: L’exemple D3D12PredicationQueries illustre l’élimination d’occlusion à l’aide de tas et de prédicats de requête DirectX 12. La procédure pas à pas décrit le code supplémentaire nécessaire pour étendre l’exemple HelloConstBuffer afin de gérer les requêtes de prédicat.
ms.assetid: F61817BB-45BC-4977-BE4A-EE0FDAFBCB57
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad14e55864ee8d568acc0c9eb46134834d27ff54
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/05/2021
ms.locfileid: "104548487"
---
# <a name="predication-queries"></a><span data-ttu-id="760b1-104">Requêtes de prédicat</span><span class="sxs-lookup"><span data-stu-id="760b1-104">Predication queries</span></span>

<span data-ttu-id="760b1-105">L’exemple **D3D12PredicationQueries** illustre l’élimination d’occlusion à l’aide de tas et de prédicats de requête DirectX 12.</span><span class="sxs-lookup"><span data-stu-id="760b1-105">The **D3D12PredicationQueries** sample demonstrates occlusion culling using DirectX 12 query heaps and predication.</span></span> <span data-ttu-id="760b1-106">La procédure pas à pas décrit le code supplémentaire nécessaire pour étendre l’exemple **HelloConstBuffer** afin de gérer les requêtes de prédicat.</span><span class="sxs-lookup"><span data-stu-id="760b1-106">The walkthrough describes the additional code needed to extend the **HelloConstBuffer** sample to handle predication queries.</span></span>

-   [<span data-ttu-id="760b1-107">Créer un tas de descripteur de stencil de profondeur et un tas de requêtes d’occlusion</span><span class="sxs-lookup"><span data-stu-id="760b1-107">Create a depth stencil descriptor heap and an occlusion query heap</span></span>](#create-a-depth-stencil-descriptor-heap-and-an-occlusion-query-heap)
-   [<span data-ttu-id="760b1-108">Activer la fusion alpha</span><span class="sxs-lookup"><span data-stu-id="760b1-108">Enable alpha blending</span></span>](#enable-alpha-blending)
-   [<span data-ttu-id="760b1-109">Désactiver les écritures de couleur et de profondeur</span><span class="sxs-lookup"><span data-stu-id="760b1-109">Disable color and depth writes</span></span>](#disable-color-and-depth-writes)
-   [<span data-ttu-id="760b1-110">Créer une mémoire tampon pour stocker les résultats de la requête</span><span class="sxs-lookup"><span data-stu-id="760b1-110">Create a buffer to store the results of the query</span></span>](#create-a-buffer-to-store-the-results-of-the-query)
-   [<span data-ttu-id="760b1-111">Dessinez les quatre cœurs et exécutez et résolvez la requête d’occlusion</span><span class="sxs-lookup"><span data-stu-id="760b1-111">Draw the quads and perform and resolve the occlusion query</span></span>](#draw-the-quads-and-perform-and-resolve-the-occlusion-query)
-   [<span data-ttu-id="760b1-112">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="760b1-112">Run the sample</span></span>](#run-the-sample)
-   [<span data-ttu-id="760b1-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="760b1-113">Related topics</span></span>](#related-topics)

## <a name="create-a-depth-stencil-descriptor-heap-and-an-occlusion-query-heap"></a><span data-ttu-id="760b1-114">Créer un tas de descripteur de stencil de profondeur et un tas de requêtes d’occlusion</span><span class="sxs-lookup"><span data-stu-id="760b1-114">Create a depth stencil descriptor heap and an occlusion query heap</span></span>

<span data-ttu-id="760b1-115">Dans la méthode **LoadPipeline** , créez un tas de descripteur de stencil de profondeur.</span><span class="sxs-lookup"><span data-stu-id="760b1-115">In the **LoadPipeline** method create a depth stencil descriptor heap.</span></span>

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
<th><span data-ttu-id="760b1-116">Workflow d’appel</span><span class="sxs-lookup"><span data-stu-id="760b1-116">Call flow</span></span></th>
<th><span data-ttu-id="760b1-117">Paramètres</span><span class="sxs-lookup"><span data-stu-id="760b1-117">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="760b1-118"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc"><strong>D3D12_DESCRIPTOR_HEAP_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="760b1-118"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc"><strong>D3D12_DESCRIPTOR_HEAP_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="760b1-119"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type"><strong>D3D12_DESCRIPTOR_HEAP_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="760b1-119"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type"><strong>D3D12_DESCRIPTOR_HEAP_TYPE</strong></a></span></span><br />
<span data-ttu-id="760b1-120">[<strong>D3D12_DESCRIPTOR_HEAP_FLAG</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_descriptor_heap_flags)</span><span class="sxs-lookup"><span data-stu-id="760b1-120">[<strong>D3D12_DESCRIPTOR_HEAP_FLAG</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="760b1-121"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap"><strong>CreateDescriptorHeap</strong></a></span><span class="sxs-lookup"><span data-stu-id="760b1-121"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap"><strong>CreateDescriptorHeap</strong></a></span></span></td>

</tr>
</tbody>
</table>



 

<span data-ttu-id="760b1-122">Dans la méthode **LoadAssets** , créez un tas pour les requêtes d’occlusion.</span><span class="sxs-lookup"><span data-stu-id="760b1-122">In the **LoadAssets** method create a heap for occlusion queries.</span></span>

``` syntax
     // Describe and create a heap for occlusion queries.
              D3D12_QUERY_HEAP_DESC queryHeapDesc = {};
              queryHeapDesc.Count = 1;
              queryHeapDesc.Type = D3D12_QUERY_HEAP_TYPE_OCCLUSION;
              ThrowIfFailed(m_device->CreateQueryHeap(&queryHeapDesc, IID_PPV_ARGS(&m_queryHeap)));
```



| <span data-ttu-id="760b1-123">Workflow d’appel</span><span class="sxs-lookup"><span data-stu-id="760b1-123">Call flow</span></span>                                                 | <span data-ttu-id="760b1-124">Paramètres</span><span class="sxs-lookup"><span data-stu-id="760b1-124">Parameters</span></span>                                                |
|-----------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="760b1-125">**Description du tas de la \_ requête D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="760b1-125">**D3D12\_QUERY\_HEAP\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_heap_desc) | [<span data-ttu-id="760b1-126">**\_Type de \_ segment de requête D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="760b1-126">**D3D12\_QUERY\_HEAP\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type) |
| [<span data-ttu-id="760b1-127">**CreateQueryHeap**</span><span class="sxs-lookup"><span data-stu-id="760b1-127">**CreateQueryHeap**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createqueryheap)   |                                                           |



 

## <a name="enable-alpha-blending"></a><span data-ttu-id="760b1-128">Activer la fusion alpha</span><span class="sxs-lookup"><span data-stu-id="760b1-128">Enable alpha blending</span></span>

<span data-ttu-id="760b1-129">Cet exemple dessine deux Quad et illustre une requête d’occlusion binaire.</span><span class="sxs-lookup"><span data-stu-id="760b1-129">This sample draws two quads and illustrates a binary occlusion query.</span></span> <span data-ttu-id="760b1-130">Le quadruple au premier plan s’anime à travers l’écran, et celui à l’arrière sera parfois bloqués.</span><span class="sxs-lookup"><span data-stu-id="760b1-130">The quad in front animates across the screen, and the one in back will occasionally be occluded.</span></span> <span data-ttu-id="760b1-131">Dans la méthode **LoadAssets** , la fusion alpha est activée pour cet exemple afin que nous puissions voir à quel point D3D prend en compte les quadruples bloqués.</span><span class="sxs-lookup"><span data-stu-id="760b1-131">In the **LoadAssets** method, alpha blending is enabled for this sample so that we can see at what point D3D considers the quad in back occluded.</span></span>

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
<th><span data-ttu-id="760b1-132">Workflow d’appel</span><span class="sxs-lookup"><span data-stu-id="760b1-132">Call flow</span></span></th>
<th><span data-ttu-id="760b1-133">Paramètres</span><span class="sxs-lookup"><span data-stu-id="760b1-133">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="760b1-134"><a href="cd3dx12-blend-desc.md"><strong>CD3DX12_BLEND_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="760b1-134"><a href="cd3dx12-blend-desc.md"><strong>CD3DX12_BLEND_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="760b1-135"><a href="cd3dx12-default.md"><strong>CD3DX12_DEFAULT</strong></a></span><span class="sxs-lookup"><span data-stu-id="760b1-135"><a href="cd3dx12-default.md"><strong>CD3DX12_DEFAULT</strong></a></span></span><br />
<span data-ttu-id="760b1-136">[<strong>D3D12_BLEND</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_blend)</span><span class="sxs-lookup"><span data-stu-id="760b1-136">[<strong>D3D12_BLEND</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_blend)</span></span><br />
<span data-ttu-id="760b1-137">[<strong>D3D12_BLEND_OP</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_blend_op)</span><span class="sxs-lookup"><span data-stu-id="760b1-137">[<strong>D3D12_BLEND_OP</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_blend_op)</span></span><br />
<span data-ttu-id="760b1-138">[<strong>D3D12_LOGIC_OP</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_logic_op)</span><span class="sxs-lookup"><span data-stu-id="760b1-138">[<strong>D3D12_LOGIC_OP</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_logic_op)</span></span><br />
<span data-ttu-id="760b1-139">[<strong>D3D12_COLOR_WRITE_ENABLE</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_color_write_enable)</span><span class="sxs-lookup"><span data-stu-id="760b1-139">[<strong>D3D12_COLOR_WRITE_ENABLE</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_color_write_enable)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="disable-color-and-depth-writes"></a><span data-ttu-id="760b1-140">Désactiver les écritures de couleur et de profondeur</span><span class="sxs-lookup"><span data-stu-id="760b1-140">Disable color and depth writes</span></span>

<span data-ttu-id="760b1-141">La requête d’occlusion est effectuée en rendant un quadruple qui couvre la même zone que le quadruple dont vous souhaitez tester la visibilité.</span><span class="sxs-lookup"><span data-stu-id="760b1-141">The occlusion query is performed by rendering a quad that covers the same area as the quad whose visibility we want to test.</span></span> <span data-ttu-id="760b1-142">Dans des scènes plus complexes, la requête serait probablement un volume englobant, plutôt qu’un simple quadruple.</span><span class="sxs-lookup"><span data-stu-id="760b1-142">In more complex scenes, the query would likely be a bounding volume, rather than a simple quad.</span></span> <span data-ttu-id="760b1-143">Dans les deux cas, un nouvel état de pipeline est créé, ce qui désactive l’écriture dans la cible de rendu et la mémoire tampon z afin que la requête d’occlusion proprement dite n’affecte pas la sortie visible de la passe de rendu.</span><span class="sxs-lookup"><span data-stu-id="760b1-143">In either case, a new pipeline state is created that disables writing to the render target and the z buffer so that the occlusion query itself does not affect the visible output of the rendering pass.</span></span>

<span data-ttu-id="760b1-144">Dans la méthode **LoadAssets** , désactivez les écritures de couleur et les écritures de profondeur pour l’état de la requête d’occlusion.</span><span class="sxs-lookup"><span data-stu-id="760b1-144">In the **LoadAssets** method, disable color writes and depth writes for the occlusion query's state.</span></span>

``` syntax
 // Disable color writes and depth writes for the occlusion query's state.
              psoDesc.BlendState.RenderTarget[0].RenderTargetWriteMask = 0;
              psoDesc.DepthStencilState.DepthWriteMask = D3D12_DEPTH_WRITE_MASK_ZERO;

              ThrowIfFailed(m_device->CreateGraphicsPipelineState(&psoDesc, IID_PPV_ARGS(&m_queryState)));
```



| <span data-ttu-id="760b1-145">Workflow d’appel</span><span class="sxs-lookup"><span data-stu-id="760b1-145">Call flow</span></span>                                                                            | <span data-ttu-id="760b1-146">Paramètres</span><span class="sxs-lookup"><span data-stu-id="760b1-146">Parameters</span></span>                                                  |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="760b1-147">**Description de l' \_ \_ État du pipeline GRAPHICs D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="760b1-147">**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) | [<span data-ttu-id="760b1-148">**\_Masque d' \_ écriture de profondeur D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="760b1-148">**D3D12\_DEPTH\_WRITE\_MASK**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_depth_write_mask) |
| [<span data-ttu-id="760b1-149">**CreateGraphicsPipelineState**</span><span class="sxs-lookup"><span data-stu-id="760b1-149">**CreateGraphicsPipelineState**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate)      |                                                             |



 

## <a name="create-a-buffer-to-store-the-results-of-the-query"></a><span data-ttu-id="760b1-150">Créer une mémoire tampon pour stocker les résultats de la requête</span><span class="sxs-lookup"><span data-stu-id="760b1-150">Create a buffer to store the results of the query</span></span>

<span data-ttu-id="760b1-151">Dans la méthode **LoadAssets** , une mémoire tampon doit être créée pour stocker les résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="760b1-151">In the **LoadAssets** method a buffer needs to be created to store the results of the query.</span></span> <span data-ttu-id="760b1-152">Chaque requête nécessite 8 octets d’espace dans la mémoire du GPU.</span><span class="sxs-lookup"><span data-stu-id="760b1-152">Each query requires 8 bytes of space in GPU memory.</span></span> <span data-ttu-id="760b1-153">Cet exemple exécute une seule requête et, pour des raisons de simplicité et de lisibilité, crée une mémoire tampon exactement de cette taille (même si cet appel de fonction allouera une page de 64 Ko de mémoire GPU, la plupart des applications réelles créeraient probablement une mémoire tampon plus grande).</span><span class="sxs-lookup"><span data-stu-id="760b1-153">This sample only performs one query and for simplicity and readability creates a buffer exactly that size (even though this function call will allocate a 64K page of GPU memory - most real apps would likely create a larger buffer).</span></span>

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
<th><span data-ttu-id="760b1-154">Workflow d’appel</span><span class="sxs-lookup"><span data-stu-id="760b1-154">Call flow</span></span></th>
<th><span data-ttu-id="760b1-155">Paramètres</span><span class="sxs-lookup"><span data-stu-id="760b1-155">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="760b1-156"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="760b1-156"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span></span></td>
<td><dl><span data-ttu-id="760b1-157"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span><span class="sxs-lookup"><span data-stu-id="760b1-157"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span></span><br />
<span data-ttu-id="760b1-158">[<strong>D3D12_HEAP_TYPE</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_heap_type)</span><span class="sxs-lookup"><span data-stu-id="760b1-158">[<strong>D3D12_HEAP_TYPE</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)</span></span><br />
<span data-ttu-id="760b1-159">[<strong>D3D12_HEAP_FLAG</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_heap_flags)</span><span class="sxs-lookup"><span data-stu-id="760b1-159">[<strong>D3D12_HEAP_FLAG</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags)</span></span><br />
<span data-ttu-id="760b1-160">[<strong>CD3DX12_RESOURCE_DESC</strong>] (cd3dx12-resource-desc.md)</span><span class="sxs-lookup"><span data-stu-id="760b1-160">[<strong>CD3DX12_RESOURCE_DESC</strong>](cd3dx12-resource-desc.md)</span></span><br />
<span data-ttu-id="760b1-161">[<strong>D3D12_RESOURCE_STATES</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_resource_states)</span><span class="sxs-lookup"><span data-stu-id="760b1-161">[<strong>D3D12_RESOURCE_STATES</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="draw-the-quads-and-perform-and-resolve-the-occlusion-query"></a><span data-ttu-id="760b1-162">Dessinez les quatre cœurs et exécutez et résolvez la requête d’occlusion</span><span class="sxs-lookup"><span data-stu-id="760b1-162">Draw the quads and perform and resolve the occlusion query</span></span>

<span data-ttu-id="760b1-163">Une fois l’installation terminée, la boucle principale est mise à jour dans la méthode **PopulateCommandLists** .</span><span class="sxs-lookup"><span data-stu-id="760b1-163">Having done the setup, the main loop is updated in the **PopulateCommandLists** method.</span></span>

<dl> 1. <span data-ttu-id="760b1-164">Dessinez les quadruples de l’arrière vers l’avant pour que l’effet de transparence fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="760b1-164">Draw the quads from back to front to make the transparency effect work properly.</span></span> <span data-ttu-id="760b1-165">Le fait de redessiner le Quad à l’avant est prédicat sur le résultat de la requête du frame précédent et est une technique relativement courante.</span><span class="sxs-lookup"><span data-stu-id="760b1-165">Drawing the quad in back to front is predicated on the result of the previous frame’s query and is a fairly common technique for this.</span></span>  
2. <span data-ttu-id="760b1-166">Modifiez l’PSO pour désactiver les écritures de la cible de rendu et du stencil de profondeur.</span><span class="sxs-lookup"><span data-stu-id="760b1-166">Change the PSO to disable render target and depth stencil writes.</span></span>  
3. <span data-ttu-id="760b1-167">Exécutez la requête d’occlusion.</span><span class="sxs-lookup"><span data-stu-id="760b1-167">Perform the occlusion query.</span></span>  
4. <span data-ttu-id="760b1-168">Résolvez la requête d’occlusion.</span><span class="sxs-lookup"><span data-stu-id="760b1-168">Resolve the occlusion query.</span></span>  
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
<th><span data-ttu-id="760b1-169">Workflow d’appel</span><span class="sxs-lookup"><span data-stu-id="760b1-169">Call flow</span></span></th>
<th><span data-ttu-id="760b1-170">Paramètres</span><span class="sxs-lookup"><span data-stu-id="760b1-170">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="760b1-171"><a href="cd3dx12-gpu-descriptor-handle.md"><strong>CD3DX12_GPU_DESCRIPTOR_HANDLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="760b1-171"><a href="cd3dx12-gpu-descriptor-handle.md"><strong>CD3DX12_GPU_DESCRIPTOR_HANDLE</strong></a></span></span></td>
<td><span data-ttu-id="760b1-172"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart"><strong>GetGPUDescriptorHandleForHeapStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="760b1-172"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart"><strong>GetGPUDescriptorHandleForHeapStart</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="760b1-173"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology"><strong>IASetPrimitiveTopology</strong></a></span><span class="sxs-lookup"><span data-stu-id="760b1-173"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology"><strong>IASetPrimitiveTopology</strong></a></span></span></td>
<td><span data-ttu-id="760b1-174"><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology"><strong>D3D_PRIMITIVE_TOPOLOGY</strong></a></span><span class="sxs-lookup"><span data-stu-id="760b1-174"><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology"><strong>D3D_PRIMITIVE_TOPOLOGY</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="760b1-175"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers"><strong>IASetVertexBuffers</strong></a></span><span class="sxs-lookup"><span data-stu-id="760b1-175"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers"><strong>IASetVertexBuffers</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="760b1-176"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></span><span class="sxs-lookup"><span data-stu-id="760b1-176"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="760b1-177"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication"><strong>SetPredication</strong></a></span><span class="sxs-lookup"><span data-stu-id="760b1-177"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication"><strong>SetPredication</strong></a></span></span></td>
<td><span data-ttu-id="760b1-178"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op"><strong>D3D12_PREDICATION_OP</strong></a></span><span class="sxs-lookup"><span data-stu-id="760b1-178"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op"><strong>D3D12_PREDICATION_OP</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="760b1-179"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></span><span class="sxs-lookup"><span data-stu-id="760b1-179"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="760b1-180"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication"><strong>SetPredication</strong></a></span><span class="sxs-lookup"><span data-stu-id="760b1-180"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication"><strong>SetPredication</strong></a></span></span></td>
<td><span data-ttu-id="760b1-181"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op"><strong>D3D12_PREDICATION_OP</strong></a></span><span class="sxs-lookup"><span data-stu-id="760b1-181"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op"><strong>D3D12_PREDICATION_OP</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="760b1-182"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></span><span class="sxs-lookup"><span data-stu-id="760b1-182"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="760b1-183"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></span><span class="sxs-lookup"><span data-stu-id="760b1-183"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="760b1-184"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></span><span class="sxs-lookup"><span data-stu-id="760b1-184"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="760b1-185"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate"><strong>SetPipelineState</strong></a></span><span class="sxs-lookup"><span data-stu-id="760b1-185"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate"><strong>SetPipelineState</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="760b1-186"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery"><strong>BeginQuery</strong></a></span><span class="sxs-lookup"><span data-stu-id="760b1-186"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery"><strong>BeginQuery</strong></a></span></span></td>
<td><span data-ttu-id="760b1-187"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="760b1-187"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="760b1-188"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></span><span class="sxs-lookup"><span data-stu-id="760b1-188"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="760b1-189"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery"><strong>EndQuery</strong></a></span><span class="sxs-lookup"><span data-stu-id="760b1-189"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery"><strong>EndQuery</strong></a></span></span></td>
<td><span data-ttu-id="760b1-190"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="760b1-190"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="760b1-191"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span><span class="sxs-lookup"><span data-stu-id="760b1-191"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span></span></td>
<td><dl><span data-ttu-id="760b1-192"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="760b1-192"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span></span><br />
<span data-ttu-id="760b1-193">[<strong>D3D12_RESOURCE_STATES</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_resource_states)</span><span class="sxs-lookup"><span data-stu-id="760b1-193">[<strong>D3D12_RESOURCE_STATES</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="760b1-194"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata"><strong>ResolveQueryData</strong></a></span><span class="sxs-lookup"><span data-stu-id="760b1-194"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata"><strong>ResolveQueryData</strong></a></span></span></td>
<td><span data-ttu-id="760b1-195"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="760b1-195"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="760b1-196"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span><span class="sxs-lookup"><span data-stu-id="760b1-196"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span></span></td>
<td><dl><span data-ttu-id="760b1-197"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="760b1-197"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span></span><br />
<span data-ttu-id="760b1-198">[<strong>D3D12_RESOURCE_STATES</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_resource_states)</span><span class="sxs-lookup"><span data-stu-id="760b1-198">[<strong>D3D12_RESOURCE_STATES</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="run-the-sample"></a><span data-ttu-id="760b1-199">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="760b1-199">Run the sample</span></span>

<span data-ttu-id="760b1-200">Non bloqués :</span><span class="sxs-lookup"><span data-stu-id="760b1-200">Not occluded:</span></span>

![deux zones non bloqués](images/not-occluded.png)

<span data-ttu-id="760b1-202">Bloqués</span><span class="sxs-lookup"><span data-stu-id="760b1-202">Occluded:</span></span>

![bloqués entièrement](images/occluded.png)

<span data-ttu-id="760b1-204">Bloqués partiel :</span><span class="sxs-lookup"><span data-stu-id="760b1-204">Partially occluded:</span></span>

![une seule zone partiellement bloqués](images/partially-occluded.png)

## <a name="related-topics"></a><span data-ttu-id="760b1-206">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="760b1-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="760b1-207">Guide pas à pas du code D3D12</span><span class="sxs-lookup"><span data-stu-id="760b1-207">D3D12 Code Walk-Throughs</span></span>](d3d12-code-walk-throughs.md)
</dt> <dt>

[<span data-ttu-id="760b1-208">Prédication</span><span class="sxs-lookup"><span data-stu-id="760b1-208">Predication</span></span>](predication.md)
</dt> <dt>

[<span data-ttu-id="760b1-209">Requêtes</span><span class="sxs-lookup"><span data-stu-id="760b1-209">Queries</span></span>](queries.md)
</dt> </dl>

 

 
