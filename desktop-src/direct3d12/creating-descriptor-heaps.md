---
title: Création de tas de descripteurs
description: Pour créer et configurer un tas de descripteur, vous devez sélectionner un type de tas de descripteur, déterminer le nombre de descripteurs qu’il contient et définir des indicateurs qui indiquent s’il est visible par l’UC et/ou nuanceur visible.
ms.assetid: 58677023-692C-4BA4-90B7-D568F3DD3F73
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e472a0749634d5cbaa9cbf1cde5e11202d4c4f9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548513"
---
# <a name="creating-descriptor-heaps"></a><span data-ttu-id="6c939-103">Création de tas de descripteurs</span><span class="sxs-lookup"><span data-stu-id="6c939-103">Creating Descriptor Heaps</span></span>

<span data-ttu-id="6c939-104">Pour créer et configurer un tas de descripteur, vous devez sélectionner un type de tas de descripteur, déterminer le nombre de descripteurs qu’il contient et définir des indicateurs qui indiquent s’il est visible par l’UC et/ou nuanceur visible.</span><span class="sxs-lookup"><span data-stu-id="6c939-104">To create and configure a descriptor heap, you must select a descriptor heap type, determine how many descriptors it contains, and set flags that indicate whether it is CPU visible and/or shader visible.</span></span>

-   [<span data-ttu-id="6c939-105">Types de tas de descripteur</span><span class="sxs-lookup"><span data-stu-id="6c939-105">Descriptor Heap types</span></span>](#descriptor-heap-types)
-   [<span data-ttu-id="6c939-106">Propriétés du tas du descripteur</span><span class="sxs-lookup"><span data-stu-id="6c939-106">Descriptor Heap Properties</span></span>](#descriptor-heap-properties)
-   [<span data-ttu-id="6c939-107">Handles de descripteur</span><span class="sxs-lookup"><span data-stu-id="6c939-107">Descriptor Handles</span></span>](#descriptor-handles)
-   [<span data-ttu-id="6c939-108">Méthodes du tas du descripteur</span><span class="sxs-lookup"><span data-stu-id="6c939-108">Descriptor Heap Methods</span></span>](#descriptor-heap-methods)
-   [<span data-ttu-id="6c939-109">Wrapper de tas de descripteur minimal</span><span class="sxs-lookup"><span data-stu-id="6c939-109">Minimal descriptor heap wrapper</span></span>](#minimal-descriptor-heap-wrapper)
-   [<span data-ttu-id="6c939-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6c939-110">Related topics</span></span>](#related-topics)

## <a name="descriptor-heap-types"></a><span data-ttu-id="6c939-111">Types de tas de descripteur</span><span class="sxs-lookup"><span data-stu-id="6c939-111">Descriptor Heap types</span></span>

<span data-ttu-id="6c939-112">Le type de segment de mémoire est déterminé par un membre de l’énumération du [**\_ type de \_ tas \_ du descripteur D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type) :</span><span class="sxs-lookup"><span data-stu-id="6c939-112">The type of heap is determined by one member of the [**D3D12\_DESCRIPTOR\_HEAP\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type) enum:</span></span>

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

## <a name="descriptor-heap-properties"></a><span data-ttu-id="6c939-113">Propriétés du tas du descripteur</span><span class="sxs-lookup"><span data-stu-id="6c939-113">Descriptor Heap Properties</span></span>

<span data-ttu-id="6c939-114">Les propriétés du tas sont définies sur la structure [**\_ desc du \_ tas \_ du descripteur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) , qui fait référence à la fois au [**\_ \_ \_ type de tas**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type) du descripteur D3D12 et aux enums du [**\_ \_ tas \_ de descripteurs D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags) .</span><span class="sxs-lookup"><span data-stu-id="6c939-114">Heap properties are set on the [**D3D12\_DESCRIPTOR\_HEAP\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) structure, which references both the [**D3D12\_DESCRIPTOR\_HEAP\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type) and [**D3D12\_DESCRIPTOR\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags) enums.</span></span>

<span data-ttu-id="6c939-115">Le \_ nuanceur de l’indicateur de tas du descripteur d’indicateur D3D12 \_ \_ \_ \_ visible peut éventuellement être défini sur un tas de descripteur pour indiquer qu’il est lié à une liste de commandes pour référence par des nuanceurs.</span><span class="sxs-lookup"><span data-stu-id="6c939-115">The flag D3D12\_DESCRIPTOR\_HEAP\_FLAG\_SHADER\_VISIBLE can optionally be set on a descriptor heap to indicate it is be bound on a command list for reference by shaders.</span></span> <span data-ttu-id="6c939-116">Les tas de descripteurs créés *sans* cet indicateur permettent aux applications d’organiser les descripteurs dans la mémoire du processeur avant de les copier dans un tas de descripteur visible du nuanceur, par commodité.</span><span class="sxs-lookup"><span data-stu-id="6c939-116">Descriptor heaps created *without* this flag allow applications the option to stage descriptors in CPU memory before copying them to a shader visible descriptor heap, as a convenience.</span></span> <span data-ttu-id="6c939-117">Toutefois, il est également intéressant pour les applications de créer directement des descripteurs dans des tas de descripteurs visibles par le nuanceur, sans qu’il soit nécessaire d’effectuer un stage sur le processeur.</span><span class="sxs-lookup"><span data-stu-id="6c939-117">But it is also fine for applications to directly create descriptors into shader visible descriptor heaps with no requirement to stage anything on the CPU.</span></span>

<span data-ttu-id="6c939-118">Cet indicateur s’applique uniquement aux échantillonneurs CBV, SRV, UAV et.</span><span class="sxs-lookup"><span data-stu-id="6c939-118">This flag only applies to CBV, SRV, UAV and samplers.</span></span> <span data-ttu-id="6c939-119">Elle ne s’applique pas aux autres types de tas de descripteurs, car les nuanceurs ne référencent pas directement les autres types.</span><span class="sxs-lookup"><span data-stu-id="6c939-119">It does not apply to other descriptor heap types since shaders do not directly reference the other types.</span></span>

<span data-ttu-id="6c939-120">Par exemple, décrivez et créez un tas de descripteur d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="6c939-120">For example, describe and create a sampler descriptor heap.</span></span>


```C++
// Describe and create a sampler descriptor heap.
D3D12_DESCRIPTOR_HEAP_DESC samplerHeapDesc = {};
samplerHeapDesc.NumDescriptors = 1;
samplerHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER;
samplerHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE;
ThrowIfFailed(m_device->CreateDescriptorHeap(&samplerHeapDesc, IID_PPV_ARGS(&m_samplerHeap)));
```



<span data-ttu-id="6c939-121">Décrire et créer une vue de mémoire tampon constante (CBV), un tas de vue de ressource de nuanceur (SRV) et un tas de descripteurs de vue d’accès non ordonné (UAV).</span><span class="sxs-lookup"><span data-stu-id="6c939-121">Describe and create a constant buffer view (CBV), Shader resource view (SRV), and unordered access view (UAV) descriptor heap.</span></span>


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



## <a name="descriptor-handles"></a><span data-ttu-id="6c939-122">Handles de descripteur</span><span class="sxs-lookup"><span data-stu-id="6c939-122">Descriptor Handles</span></span>

<span data-ttu-id="6c939-123">Le [**\_ \_ \_ handle**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) du descripteur GPU D3D12 et les structures de [**\_ \_ \_ handle du**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) descripteur d’UC D3D12 identifient les descripteurs spécifiques dans un tas de descripteur.</span><span class="sxs-lookup"><span data-stu-id="6c939-123">The [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) and [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structures identify specific descriptors in a descriptor heap.</span></span> <span data-ttu-id="6c939-124">Un handle est un peu comme un pointeur, mais l’application ne doit pas le déréférencer manuellement. dans le cas contraire, le comportement n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="6c939-124">A handle is a bit like a pointer, but the application must not dereference it manually; otherwise, the behavior is undefined.</span></span> <span data-ttu-id="6c939-125">L’utilisation des handles doit traverser l’API.</span><span class="sxs-lookup"><span data-stu-id="6c939-125">The use of the handles must go through the API.</span></span> <span data-ttu-id="6c939-126">Un handle lui-même peut être copié librement ou passé dans des API qui opèrent sur des descripteurs/use.</span><span class="sxs-lookup"><span data-stu-id="6c939-126">A handle itself can be copied freely or passed into APIs that operate on/use descriptors.</span></span> <span data-ttu-id="6c939-127">Étant donné qu’il n’existe pas de comptage de référence, l’application doit s’assurer qu’elle n’utilise pas de handle après la suppression du tas de descripteur sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="6c939-127">There is no ref counting, so the application must ensure that it does not use a handle after the underlying descriptor heap has been deleted.</span></span>

<span data-ttu-id="6c939-128">Les applications peuvent déterminer la taille incrémentielle des descripteurs pour un type de tas de descripteur donné, afin qu’ils puissent générer des handles à n’importe quel emplacement dans un tas de descripteur, en commençant par le handle de la base.</span><span class="sxs-lookup"><span data-stu-id="6c939-128">Applications can find out the increment size of the descriptors for a given descriptor heap type, so that they can generate handles to any location in a descriptor heap manually starting from the handle to the base.</span></span> <span data-ttu-id="6c939-129">Les applications ne doivent jamais coder en dur les tailles d’incrément de handle de descripteur et doivent toujours les interroger pour une instance d’appareil donnée ; dans le cas contraire, le comportement n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="6c939-129">Applications must never hardcode descriptor handle increment sizes, and should always query them for a given device instance; otherwise, the behavior is undefined.</span></span> <span data-ttu-id="6c939-130">Les applications ne doivent pas non plus utiliser les tailles et les handles d’incrément pour effectuer leur propre examen ou manipulation des données du tas du descripteur, car les résultats de cette opération ne sont pas définis.</span><span class="sxs-lookup"><span data-stu-id="6c939-130">Applications must also not use the increment sizes and handles to do their own examination or manipulation of descriptor heap data, as the results from doing so are undefined.</span></span> <span data-ttu-id="6c939-131">Les handles ne peuvent pas être utilisés en tant que pointeurs, mais plutôt en tant que proxies pour les pointeurs afin d’éviter les déréférencements accidentels.</span><span class="sxs-lookup"><span data-stu-id="6c939-131">The handles may not actually be used as pointers, but rather as proxies for pointers so as to avoid accidental dereferencing.</span></span>

> [!Note]
>
> <span data-ttu-id="6c939-132">Il existe une structure d’assistance, \_ \_ handle de descripteur GPU CD3DX12 \_ , définie dans l’en-tête d3dx12. h, qui hérite de la structure de [**\_ \_ \_ handle du descripteur GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) et fournit l’initialisation et d’autres opérations utiles.</span><span class="sxs-lookup"><span data-stu-id="6c939-132">There is a helper structure, CD3DX12\_GPU\_DESCRIPTOR\_HANDLE, defined in the header d3dx12.h, which inherits the [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) structure and provides initialization and other useful operations.</span></span> <span data-ttu-id="6c939-133">De même, la \_ \_ structure d’assistance du handle du descripteur de processeur CD3DX12 \_ est définie pour la structure de [**\_ \_ \_ handle du descripteur de processeur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) .</span><span class="sxs-lookup"><span data-stu-id="6c939-133">Similarly the CD3DX12\_CPU\_DESCRIPTOR\_HANDLE helper structure is defined for the [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structure.</span></span>

 

<span data-ttu-id="6c939-134">Ces deux structures d’assistance sont utilisées lors du remplissage des listes de commandes.</span><span class="sxs-lookup"><span data-stu-id="6c939-134">Both of these helper structures are used when populating command lists.</span></span>


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



## <a name="descriptor-heap-methods"></a><span data-ttu-id="6c939-135">Méthodes du tas du descripteur</span><span class="sxs-lookup"><span data-stu-id="6c939-135">Descriptor Heap Methods</span></span>

<span data-ttu-id="6c939-136">Les tas de descripteurs ([**ID3D12DescriptorHeap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap)) héritent de [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable).</span><span class="sxs-lookup"><span data-stu-id="6c939-136">Descriptor heaps ([**ID3D12DescriptorHeap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap)) inherit from [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable).</span></span> <span data-ttu-id="6c939-137">Cela impose la responsabilité de la gestion de la résidence des tas de descripteurs sur les applications, tout comme les tas de ressources.</span><span class="sxs-lookup"><span data-stu-id="6c939-137">This imposes the responsibility for the residency management of descriptor heaps on applications, just like resource heaps.</span></span> <span data-ttu-id="6c939-138">Les méthodes de gestion des dépassements s’appliquent uniquement aux tas visibles du nuanceur, car les tas non visibles par le nuanceur ne sont pas visibles directement pour le GPU.</span><span class="sxs-lookup"><span data-stu-id="6c939-138">The residency management methods only apply to shader visible heaps since the non shader visible heaps are not visible to the GPU directly.</span></span>

<span data-ttu-id="6c939-139">La méthode [**ID3D12Device :: GetDescriptorHandleIncrementSize**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize) permet aux applications de décaler manuellement des handles dans un tas (en produisant des handles dans n’importe quel emplacement dans un tas de descripteur).</span><span class="sxs-lookup"><span data-stu-id="6c939-139">The [**ID3D12Device::GetDescriptorHandleIncrementSize**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize) method allows applications to manually offset handles into a heap (producing handles into anywhere in a descriptor heap).</span></span> <span data-ttu-id="6c939-140">Le handle de l’emplacement de début du tas provient de [**ID3D12DescriptorHeap :: GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart) / [**ID3D12DescriptorHeap :: GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart).</span><span class="sxs-lookup"><span data-stu-id="6c939-140">The heap start location’s handle comes from [**ID3D12DescriptorHeap::GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)/[**ID3D12DescriptorHeap::GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart).</span></span> <span data-ttu-id="6c939-141">Le décalage s’effectue en ajoutant la taille d’incrément \* du nombre de descripteurs à décaler au début du tas du descripteur.</span><span class="sxs-lookup"><span data-stu-id="6c939-141">Offsetting is done by adding the increment size \* the number of descriptors to offset to the descriptor heap start .</span></span> <span data-ttu-id="6c939-142">Notez que la taille de l’incrément ne peut pas être considérée comme une taille d’octet puisque les applications ne doivent pas déréférencer des handles comme s’il s’agissait de mémoire : la mémoire pointée a une disposition non standardisée et peut varier même pour un appareil donné.</span><span class="sxs-lookup"><span data-stu-id="6c939-142">Note that the increment size cannot be thought of as a byte size since applications must not dereference handles as if they are memory – the memory pointed to has a non-standardized layout and can vary even for a given device.</span></span>

<span data-ttu-id="6c939-143">[**GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart) retourne un handle de processeur pour les tas de descripteurs visibles par l’UC.</span><span class="sxs-lookup"><span data-stu-id="6c939-143">[**GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart) returns a CPU handle for CPU visible descriptor heaps.</span></span> <span data-ttu-id="6c939-144">Elle retourne un handle NULL (et la couche de débogage signale une erreur) si le tas du descripteur n’est pas visible par l’UC.</span><span class="sxs-lookup"><span data-stu-id="6c939-144">It returns a NULL handle (and the debug layer will report an error) if the descriptor heap is not CPU visible.</span></span>

<span data-ttu-id="6c939-145">[**GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart) retourne un handle GPU pour les tas de descripteurs visibles du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="6c939-145">[**GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart) returns a GPU handle for shader visible descriptor heaps.</span></span> <span data-ttu-id="6c939-146">Elle retourne un handle NULL (et la couche de débogage signale une erreur) si le tas du descripteur n’est pas visible par le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="6c939-146">It returns a NULL handle (and the debug layer will report an error) if the descriptor heap is not shader visible.</span></span>

<span data-ttu-id="6c939-147">Par exemple, la création de vues de cible de rendu pour afficher du texte D2D à l’aide d’un appareil 11on12.</span><span class="sxs-lookup"><span data-stu-id="6c939-147">For example, creating render target views to display D2D text using an 11on12 device.</span></span>


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



## <a name="minimal-descriptor-heap-wrapper"></a><span data-ttu-id="6c939-148">Wrapper de tas de descripteur minimal</span><span class="sxs-lookup"><span data-stu-id="6c939-148">Minimal descriptor heap wrapper</span></span>

<span data-ttu-id="6c939-149">Les développeurs d’applications souhaiteront probablement créer leur propre code d’assistance pour gérer les tas et les handles de descripteur.</span><span class="sxs-lookup"><span data-stu-id="6c939-149">Application developers will likely want to build their own helper code for managing descriptor handles and heaps.</span></span> <span data-ttu-id="6c939-150">Un exemple de base est illustré ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="6c939-150">A basic example is shown below.</span></span> <span data-ttu-id="6c939-151">Des wrappers plus sophistiqués peuvent, par exemple, effectuer le suivi des types de descripteurs dans un segment de mémoire et stocker les arguments de création du descripteur.</span><span class="sxs-lookup"><span data-stu-id="6c939-151">More sophisticated wrappers could, for example, keep track of what types of descriptors are where in a heap and store the descriptor creation arguments.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="6c939-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6c939-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c939-153">Tas de descripteurs</span><span class="sxs-lookup"><span data-stu-id="6c939-153">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 