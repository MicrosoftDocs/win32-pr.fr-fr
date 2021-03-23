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
# <a name="multi-engine-n-body-gravity-simulation"></a><span data-ttu-id="96db8-103">Simulation de gravité n-corps multi-moteur</span><span class="sxs-lookup"><span data-stu-id="96db8-103">Multi-engine n-body gravity simulation</span></span>

<span data-ttu-id="96db8-104">L’exemple **D3D12nBodyGravity** montre comment effectuer un travail de calcul de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="96db8-104">The **D3D12nBodyGravity** sample demonstrates how to do compute work asynchronously.</span></span> <span data-ttu-id="96db8-105">L’exemple fait tourner un certain nombre de threads, chacun avec une file d’attente de commandes Compute, et planifie le travail de calcul sur le GPU qui effectue une simulation de gravité en n corps.</span><span class="sxs-lookup"><span data-stu-id="96db8-105">The sample spins up a number of threads each with a compute command queue and schedules compute work on the GPU that performs an n-body gravity simulation.</span></span> <span data-ttu-id="96db8-106">Chaque thread opère sur deux mémoires tampons complètes de données de position et de vélocité.</span><span class="sxs-lookup"><span data-stu-id="96db8-106">Each thread operates on two buffers full of position and velocity data.</span></span> <span data-ttu-id="96db8-107">À chaque itération, le nuanceur de calcul lit les données de position et de vélocité actuelles d’une mémoire tampon et écrit l’itération suivante dans l’autre mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="96db8-107">With each iteration, the compute shader reads the current position and velocity data from one buffer and writes the next iteration into the other buffer.</span></span> <span data-ttu-id="96db8-108">Lorsque l’itération est terminée, le nuanceur de calcul permute la mémoire tampon qui sert à lire les données de position/vélocité et qui est le UAV pour l’écriture des mises à jour de position/vélocité en modifiant l’état de la ressource sur chaque mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="96db8-108">When the iteration completes, the compute shader swaps which buffer is the SRV for reading position/velocity data and which is the UAV for writing position/velocity updates by changing the resource state on each buffer.</span></span>

-   [<span data-ttu-id="96db8-109">Créer les signatures racines</span><span class="sxs-lookup"><span data-stu-id="96db8-109">Create the root signatures</span></span>](#create-the-root-signatures)
-   [<span data-ttu-id="96db8-110">Créer les mémoires tampons SRV et UAV</span><span class="sxs-lookup"><span data-stu-id="96db8-110">Create the SRV and UAV buffers</span></span>](#create-the-srv-and-uav-buffers)
-   [<span data-ttu-id="96db8-111">Créer les CBV et les mémoires tampons de vertex</span><span class="sxs-lookup"><span data-stu-id="96db8-111">Create the CBV and vertex buffers</span></span>](#create-the-cbv-and-vertex-buffers)
-   [<span data-ttu-id="96db8-112">Synchroniser les threads de rendu et de calcul</span><span class="sxs-lookup"><span data-stu-id="96db8-112">Synchronize the rendering and compute threads</span></span>](#synchronize-the-rendering-and-compute-threads)
-   [<span data-ttu-id="96db8-113">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="96db8-113">Run the sample</span></span>](#run-the-sample)
-   [<span data-ttu-id="96db8-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="96db8-114">Related topics</span></span>](#related-topics)

## <a name="create-the-root-signatures"></a><span data-ttu-id="96db8-115">Créer les signatures racines</span><span class="sxs-lookup"><span data-stu-id="96db8-115">Create the root signatures</span></span>

<span data-ttu-id="96db8-116">Nous commençons par créer un graphique et une signature racine de calcul, dans la méthode **LoadAssets** .</span><span class="sxs-lookup"><span data-stu-id="96db8-116">We start out by creating both a graphics and a compute root signature, in the **LoadAssets** method.</span></span> <span data-ttu-id="96db8-117">Les deux signatures racines ont une vue de mémoire tampon constante racine (CBV) et une table de descripteurs SRV (Shader Resource View).</span><span class="sxs-lookup"><span data-stu-id="96db8-117">Both root signatures have a root constant buffer view (CBV) and a shader resource view (SRV) descriptor table.</span></span> <span data-ttu-id="96db8-118">La signature de la racine de calcul a également une table de descripteurs de vue d’accès non triée (UAV).</span><span class="sxs-lookup"><span data-stu-id="96db8-118">The compute root signature also has an unordered access view (UAV) descriptor table.</span></span>

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



| <span data-ttu-id="96db8-119">Workflow d’appel</span><span class="sxs-lookup"><span data-stu-id="96db8-119">Call flow</span></span>                                                             | <span data-ttu-id="96db8-120">Paramètres</span><span class="sxs-lookup"><span data-stu-id="96db8-120">Parameters</span></span>                                                            |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="96db8-121">**\_Plage du descripteur CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="96db8-121">**CD3DX12\_DESCRIPTOR\_RANGE**</span></span>](cd3dx12-descriptor-range.md)        | [<span data-ttu-id="96db8-122">**\_Type de plage du descripteur D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="96db8-122">**D3D12\_DESCRIPTOR\_RANGE\_TYPE**</span></span>](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) |
| [<span data-ttu-id="96db8-123">**\_Paramètre racine \_ CD3DX12**</span><span class="sxs-lookup"><span data-stu-id="96db8-123">**CD3DX12\_ROOT\_PARAMETER**</span></span>](cd3dx12-root-parameter.md)            | [<span data-ttu-id="96db8-124">**\_Visibilité du nuanceur D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="96db8-124">**D3D12\_SHADER\_VISIBILITY**</span></span>](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_visibility)          |
| [<span data-ttu-id="96db8-125">**Description de la \_ signature racine CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="96db8-125">**CD3DX12\_ROOT\_SIGNATURE\_DESC**</span></span>](cd3dx12-root-signature-desc.md) | [<span data-ttu-id="96db8-126">**\_Indicateurs de \_ signature \_ racine D3D12**</span><span class="sxs-lookup"><span data-stu-id="96db8-126">**D3D12\_ROOT\_SIGNATURE\_FLAGS**</span></span>](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_signature_flags)   |
| <span data-ttu-id="96db8-127">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="96db8-127">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span></span>                                   |                                                                       |
| [<span data-ttu-id="96db8-128">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="96db8-128">**D3D12SerializeRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [<span data-ttu-id="96db8-129">**\_Version de \_ signature \_ racine D3D**</span><span class="sxs-lookup"><span data-stu-id="96db8-129">**D3D\_ROOT\_SIGNATURE\_VERSION**</span></span>](/windows/win32/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [<span data-ttu-id="96db8-130">**CreateRootSignature**</span><span class="sxs-lookup"><span data-stu-id="96db8-130">**CreateRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |
| [<span data-ttu-id="96db8-131">**Description de la \_ signature racine CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="96db8-131">**CD3DX12\_ROOT\_SIGNATURE\_DESC**</span></span>](cd3dx12-root-signature-desc.md) |                                                                       |
| [<span data-ttu-id="96db8-132">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="96db8-132">**D3D12SerializeRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [<span data-ttu-id="96db8-133">**\_Version de \_ signature \_ racine D3D**</span><span class="sxs-lookup"><span data-stu-id="96db8-133">**D3D\_ROOT\_SIGNATURE\_VERSION**</span></span>](/windows/win32/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [<span data-ttu-id="96db8-134">**CreateRootSignature**</span><span class="sxs-lookup"><span data-stu-id="96db8-134">**CreateRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |



 

## <a name="create-the-srv-and-uav-buffers"></a><span data-ttu-id="96db8-135">Créer les mémoires tampons SRV et UAV</span><span class="sxs-lookup"><span data-stu-id="96db8-135">Create the SRV and UAV buffers</span></span>

<span data-ttu-id="96db8-136">Les mémoires tampons SRV et UAV se composent d’un tableau de données de position et de vélocité.</span><span class="sxs-lookup"><span data-stu-id="96db8-136">The SRV and UAV buffers consist of an array of position and velocity data.</span></span>

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



| <span data-ttu-id="96db8-137">Workflow d’appel</span><span class="sxs-lookup"><span data-stu-id="96db8-137">Call flow</span></span>                       | <span data-ttu-id="96db8-138">Paramètres</span><span class="sxs-lookup"><span data-stu-id="96db8-138">Parameters</span></span> |
|---------------------------------|------------|
| [<span data-ttu-id="96db8-139">**XMFLOAT4**</span><span class="sxs-lookup"><span data-stu-id="96db8-139">**XMFLOAT4**</span></span>](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) |            |



 

## <a name="create-the-cbv-and-vertex-buffers"></a><span data-ttu-id="96db8-140">Créer les CBV et les mémoires tampons de vertex</span><span class="sxs-lookup"><span data-stu-id="96db8-140">Create the CBV and vertex buffers</span></span>

<span data-ttu-id="96db8-141">Pour le pipeline Graphics, le CBV est un **struct** contenant deux matrices utilisées par le nuanceur Geometry.</span><span class="sxs-lookup"><span data-stu-id="96db8-141">For the graphics pipeline, the CBV is a **struct** containing two matrices used by the geometry shader.</span></span> <span data-ttu-id="96db8-142">Le nuanceur Geometry prend la position de chaque particule dans le système et génère une valeur Quad pour la représenter à l’aide de ces matrices.</span><span class="sxs-lookup"><span data-stu-id="96db8-142">The geometry shader takes the position of each particle in the system and generates a quad to represent it using these matrices.</span></span>

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



| <span data-ttu-id="96db8-143">Workflow d’appel</span><span class="sxs-lookup"><span data-stu-id="96db8-143">Call flow</span></span>                       | <span data-ttu-id="96db8-144">Paramètres</span><span class="sxs-lookup"><span data-stu-id="96db8-144">Parameters</span></span> |
|---------------------------------|------------|
| [<span data-ttu-id="96db8-145">**XMMATRIX**</span><span class="sxs-lookup"><span data-stu-id="96db8-145">**XMMATRIX**</span></span>](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) |            |



 

<span data-ttu-id="96db8-146">Par conséquent, la mémoire tampon de vertex utilisée par le nuanceur vertex ne contient en fait pas de données positionnelles.</span><span class="sxs-lookup"><span data-stu-id="96db8-146">As a result, the vertex buffer used by the vertex shader actually does not contain any positional data.</span></span>

``` syntax
 // "Vertex" definition for particles. Triangle vertices are generated 
       // by the geometry shader. Color data will be assigned to those 
       // vertices via this struct.
       struct ParticleVertex
       {
              XMFLOAT4 color;
       };
```



| <span data-ttu-id="96db8-147">Workflow d’appel</span><span class="sxs-lookup"><span data-stu-id="96db8-147">Call flow</span></span>                       | <span data-ttu-id="96db8-148">Paramètres</span><span class="sxs-lookup"><span data-stu-id="96db8-148">Parameters</span></span> |
|---------------------------------|------------|
| [<span data-ttu-id="96db8-149">**XMFLOAT4**</span><span class="sxs-lookup"><span data-stu-id="96db8-149">**XMFLOAT4**</span></span>](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) |            |



 

<span data-ttu-id="96db8-150">Pour le pipeline de calcul, CBV est un **struct** contenant des constantes utilisées par la simulation de gravité à n corps dans le nuanceur de calcul.</span><span class="sxs-lookup"><span data-stu-id="96db8-150">For the compute pipeline, the CBV is a **struct** containing some constants used by the n-body gravity simulation in the compute shader.</span></span>

``` syntax
 struct ConstantBufferCS
       {
              UINT param[4];
              float paramf[4];
       };
```

## <a name="synchronize-the-rendering-and-compute-threads"></a><span data-ttu-id="96db8-151">Synchroniser les threads de rendu et de calcul</span><span class="sxs-lookup"><span data-stu-id="96db8-151">Synchronize the rendering and compute threads</span></span>

<span data-ttu-id="96db8-152">Une fois les tampons initialisés, le travail de rendu et de calcul commence.</span><span class="sxs-lookup"><span data-stu-id="96db8-152">After the buffers are all initialized, the rendering and compute work will begin.</span></span> <span data-ttu-id="96db8-153">Le thread de calcul va changer l’état des deux mémoires tampons de position/vélocité entre SRV et UAV lorsqu’il itère sur la simulation, et le thread de rendu doit s’assurer qu’il planifie le travail sur le pipeline graphique qui opère sur le SRV.</span><span class="sxs-lookup"><span data-stu-id="96db8-153">The compute thread will be changing the state of the two position/velocity buffers back and forth between SRV and UAV as it iterates on the simulation, and the rendering thread needs to ensure that it schedules work on the graphics pipeline that operates on the SRV.</span></span> <span data-ttu-id="96db8-154">Les délimiteurs sont utilisés pour synchroniser l’accès aux deux mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="96db8-154">Fences are used to synchronize access to the two buffers.</span></span>

<span data-ttu-id="96db8-155">Sur le thread de rendu :</span><span class="sxs-lookup"><span data-stu-id="96db8-155">On the Render thread:</span></span>

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



| <span data-ttu-id="96db8-156">Workflow d’appel</span><span class="sxs-lookup"><span data-stu-id="96db8-156">Call flow</span></span>                                                              | <span data-ttu-id="96db8-157">Paramètres</span><span class="sxs-lookup"><span data-stu-id="96db8-157">Parameters</span></span> |
|------------------------------------------------------------------------|------------|
| [<span data-ttu-id="96db8-158">**Interlockedexchang**</span><span class="sxs-lookup"><span data-stu-id="96db8-158">**InterlockedExchange**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedexchange)                  |            |
| [<span data-ttu-id="96db8-159">**InterlockedGetValue**</span><span class="sxs-lookup"><span data-stu-id="96db8-159">**InterlockedGetValue**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedcompareexchange)           |            |
| [<span data-ttu-id="96db8-160">**GetCompletedValue**</span><span class="sxs-lookup"><span data-stu-id="96db8-160">**GetCompletedValue**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue)             |            |
| [<span data-ttu-id="96db8-161">**Wait**</span><span class="sxs-lookup"><span data-stu-id="96db8-161">**Wait**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait)                                |            |
| [<span data-ttu-id="96db8-162">**ID3D12CommandList**</span><span class="sxs-lookup"><span data-stu-id="96db8-162">**ID3D12CommandList**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist)                         |            |
| [<span data-ttu-id="96db8-163">**ExecuteCommandLists**</span><span class="sxs-lookup"><span data-stu-id="96db8-163">**ExecuteCommandLists**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)  |            |
| [<span data-ttu-id="96db8-164">**IDXGISwapChain1::Present1**</span><span class="sxs-lookup"><span data-stu-id="96db8-164">**IDXGISwapChain1::Present1**</span></span>](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) |            |



 

<span data-ttu-id="96db8-165">Pour simplifier l’exemple un peu, le thread de calcul attend que le GPU termine chaque itération avant de planifier davantage de travail de calcul.</span><span class="sxs-lookup"><span data-stu-id="96db8-165">To simplify the sample a bit, the compute thread waits for the GPU to complete each iteration before scheduling any more compute work.</span></span> <span data-ttu-id="96db8-166">En pratique, les applications souhaiteront probablement garder la file d’attente de calcul pleine pour obtenir des performances maximales du GPU.</span><span class="sxs-lookup"><span data-stu-id="96db8-166">In practice, applications will likely want to keep the compute queue full to achieve maximum performance from the GPU.</span></span>

<span data-ttu-id="96db8-167">Sur le thread Compute :</span><span class="sxs-lookup"><span data-stu-id="96db8-167">On the Compute thread:</span></span>

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



| <span data-ttu-id="96db8-168">Workflow d’appel</span><span class="sxs-lookup"><span data-stu-id="96db8-168">Call flow</span></span>                                                                   | <span data-ttu-id="96db8-169">Paramètres</span><span class="sxs-lookup"><span data-stu-id="96db8-169">Parameters</span></span> |
|-----------------------------------------------------------------------------|------------|
| [<span data-ttu-id="96db8-170">**ID3D12CommandQueue**</span><span class="sxs-lookup"><span data-stu-id="96db8-170">**ID3D12CommandQueue**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue)                            |            |
| [<span data-ttu-id="96db8-171">**ID3D12CommandAllocator**</span><span class="sxs-lookup"><span data-stu-id="96db8-171">**ID3D12CommandAllocator**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12commandallocator)                    |            |
| [<span data-ttu-id="96db8-172">**ID3D12GraphicsCommandList**</span><span class="sxs-lookup"><span data-stu-id="96db8-172">**ID3D12GraphicsCommandList**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)              |            |
| [<span data-ttu-id="96db8-173">**ID3D12Fence**</span><span class="sxs-lookup"><span data-stu-id="96db8-173">**ID3D12Fence**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12fence)                                          |            |
| [<span data-ttu-id="96db8-174">**InterlockedGetValue**</span><span class="sxs-lookup"><span data-stu-id="96db8-174">**InterlockedGetValue**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedcompareexchange)                |            |
| [<span data-ttu-id="96db8-175">**Fermer**</span><span class="sxs-lookup"><span data-stu-id="96db8-175">**Close**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)                            |            |
| [<span data-ttu-id="96db8-176">**ID3D12CommandList**</span><span class="sxs-lookup"><span data-stu-id="96db8-176">**ID3D12CommandList**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist)                              |            |
| [<span data-ttu-id="96db8-177">**ExecuteCommandLists**</span><span class="sxs-lookup"><span data-stu-id="96db8-177">**ExecuteCommandLists**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)       |            |
| [<span data-ttu-id="96db8-178">**InterlockedIncrement**</span><span class="sxs-lookup"><span data-stu-id="96db8-178">**InterlockedIncrement**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedincrement)                     |            |
| [<span data-ttu-id="96db8-179">**Témoin**</span><span class="sxs-lookup"><span data-stu-id="96db8-179">**Signal**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)                                 |            |
| [<span data-ttu-id="96db8-180">**SetEventOnCompletion**</span><span class="sxs-lookup"><span data-stu-id="96db8-180">**SetEventOnCompletion**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion)            |            |
| [<span data-ttu-id="96db8-181">**WaitForSingleObject**</span><span class="sxs-lookup"><span data-stu-id="96db8-181">**WaitForSingleObject**</span></span>](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)                         |            |
| [<span data-ttu-id="96db8-182">**InterlockedGetValue**</span><span class="sxs-lookup"><span data-stu-id="96db8-182">**InterlockedGetValue**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedcompareexchange)                |            |
| [<span data-ttu-id="96db8-183">**GetCompletedValue**</span><span class="sxs-lookup"><span data-stu-id="96db8-183">**GetCompletedValue**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue)                  |            |
| [<span data-ttu-id="96db8-184">**Wait**</span><span class="sxs-lookup"><span data-stu-id="96db8-184">**Wait**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait)                                     |            |
| [<span data-ttu-id="96db8-185">**Interlockedexchang**</span><span class="sxs-lookup"><span data-stu-id="96db8-185">**InterlockedExchange**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedexchange)                       |            |
| [<span data-ttu-id="96db8-186">**ID3D12CommandAllocator :: Reset**</span><span class="sxs-lookup"><span data-stu-id="96db8-186">**ID3D12CommandAllocator::Reset**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset)       |            |
| [<span data-ttu-id="96db8-187">**ID3D12GraphicsCommandList :: Reset**</span><span class="sxs-lookup"><span data-stu-id="96db8-187">**ID3D12GraphicsCommandList::Reset**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset) |            |



 

## <a name="run-the-sample"></a><span data-ttu-id="96db8-188">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="96db8-188">Run the sample</span></span>

![capture d’écran de la dernière simulation de gravité n Body](images/nbodygravity.png)

## <a name="related-topics"></a><span data-ttu-id="96db8-190">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="96db8-190">Related topics</span></span>

[<span data-ttu-id="96db8-191">Guide pas à pas du code D3D12</span><span class="sxs-lookup"><span data-stu-id="96db8-191">D3D12 Code Walk-Throughs</span></span>](d3d12-code-walk-throughs.md)

[<span data-ttu-id="96db8-192">Synchronisation multi-moteur</span><span class="sxs-lookup"><span data-stu-id="96db8-192">Multi-engine synchronization</span></span>](./user-mode-heap-synchronization.md)