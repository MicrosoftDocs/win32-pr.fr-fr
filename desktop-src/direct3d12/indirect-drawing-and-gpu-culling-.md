---
title: Dessin indirect et élimination du GPU
description: L’exemple D3D12ExecuteIndirect montre comment utiliser des commandes indirectes pour dessiner du contenu. Il montre également comment ces commandes peuvent être manipulées sur le GPU dans un nuanceur de calcul avant leur émission.
ms.assetid: 09F90837-D6BF-498E-8018-5C28EDD9BDC3
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b016170fbd3b675d5d5a20c1de87f24b04d4804
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/05/2021
ms.locfileid: "104548507"
---
# <a name="indirect-drawing-and-gpu-culling"></a><span data-ttu-id="5e799-104">Dessin indirect et élimination du GPU</span><span class="sxs-lookup"><span data-stu-id="5e799-104">Indirect drawing and GPU culling</span></span>

<span data-ttu-id="5e799-105">L’exemple D3D12ExecuteIndirect montre comment utiliser des commandes indirectes pour dessiner du contenu.</span><span class="sxs-lookup"><span data-stu-id="5e799-105">The D3D12ExecuteIndirect sample demonstrates how to use indirect commands to draw content.</span></span> <span data-ttu-id="5e799-106">Il montre également comment ces commandes peuvent être manipulées sur le GPU dans un nuanceur de calcul avant leur émission.</span><span class="sxs-lookup"><span data-stu-id="5e799-106">It also demonstrates how these commands can be manipulated on the GPU in a compute shader before they are issued.</span></span>

-   [<span data-ttu-id="5e799-107">Définir les commandes indirectes</span><span class="sxs-lookup"><span data-stu-id="5e799-107">Define the indirect commands</span></span>](#define-the-indirect-commands)
-   [<span data-ttu-id="5e799-108">Créer un graphique et une signature racine de calcul</span><span class="sxs-lookup"><span data-stu-id="5e799-108">Create a graphics and compute root signature</span></span>](#create-a-graphics-and-compute-root-signature)
-   [<span data-ttu-id="5e799-109">Créer une vue de ressource de nuanceur (SRV) pour le nuanceur de calcul</span><span class="sxs-lookup"><span data-stu-id="5e799-109">Create a shader resource view (SRV) for the compute shader</span></span>](#create-a-shader-resource-view-srv-for-the-compute-shader)
-   [<span data-ttu-id="5e799-110">Créer les mémoires tampons de commande indirectes</span><span class="sxs-lookup"><span data-stu-id="5e799-110">Create the indirect command buffers</span></span>](#create-the-indirect-command-buffers)
-   [<span data-ttu-id="5e799-111">Créer le calcul UAVs</span><span class="sxs-lookup"><span data-stu-id="5e799-111">Create the compute UAVs</span></span>](#create-the-compute-uavs)
-   [<span data-ttu-id="5e799-112">Dessin du frame</span><span class="sxs-lookup"><span data-stu-id="5e799-112">Drawing the frame</span></span>](#drawing-the-frame)
-   [<span data-ttu-id="5e799-113">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="5e799-113">Run the sample</span></span>](#run-the-sample)
-   [<span data-ttu-id="5e799-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5e799-114">Related topics</span></span>](#related-topics)

<span data-ttu-id="5e799-115">L’exemple crée une mémoire tampon de commande qui décrit 1024 appels de dessin.</span><span class="sxs-lookup"><span data-stu-id="5e799-115">The sample creates a command buffer that describes 1024 draw calls.</span></span> <span data-ttu-id="5e799-116">Chaque appel de dessin restitue un triangle avec une couleur, une position et une vélocité aléatoires.</span><span class="sxs-lookup"><span data-stu-id="5e799-116">Each draw call renders a triangle with a random color, position, and velocity.</span></span> <span data-ttu-id="5e799-117">Les triangles s’animent de façon infinie sur l’écran.</span><span class="sxs-lookup"><span data-stu-id="5e799-117">The triangles animate endlessly across the screen.</span></span> <span data-ttu-id="5e799-118">Cet exemple comporte deux modes.</span><span class="sxs-lookup"><span data-stu-id="5e799-118">There are two modes in this sample.</span></span> <span data-ttu-id="5e799-119">Dans le premier mode, un nuanceur de calcul inspecte les commandes indirectes et décide s’il faut ou non ajouter cette commande à une vue d’accès non ordonnée (UAV) décrivant les commandes qui doivent être exécutées.</span><span class="sxs-lookup"><span data-stu-id="5e799-119">In the first mode, a compute shader inspects the indirect commands and decides whether or not to add that command to an unordered access view (UAV) describing which commands that should be executed.</span></span> <span data-ttu-id="5e799-120">Dans le deuxième mode, toutes les commandes sont simplement exécutées.</span><span class="sxs-lookup"><span data-stu-id="5e799-120">In the second mode, all commands are simply executed.</span></span> <span data-ttu-id="5e799-121">Le fait d’appuyer sur la barre d’espace permet de basculer entre les modes.</span><span class="sxs-lookup"><span data-stu-id="5e799-121">Pressing the spacebar will toggle between modes.</span></span>

## <a name="define-the-indirect-commands"></a><span data-ttu-id="5e799-122">Définir les commandes indirectes</span><span class="sxs-lookup"><span data-stu-id="5e799-122">Define the indirect commands</span></span>

<span data-ttu-id="5e799-123">Nous commençons par définir à quoi ressemblent les commandes indirectes.</span><span class="sxs-lookup"><span data-stu-id="5e799-123">We start out by defining what the indirect commands should look like.</span></span> <span data-ttu-id="5e799-124">Dans cet exemple, les commandes que vous souhaitez exécuter sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="5e799-124">In this sample the commands we want to execute are to:</span></span>

<dl> 1. <span data-ttu-id="5e799-125">Mettez à jour la vue de la mémoire tampon constante (CBV).</span><span class="sxs-lookup"><span data-stu-id="5e799-125">Update the constant buffer view (CBV).</span></span>  
2. <span data-ttu-id="5e799-126">Dessinez le triangle.</span><span class="sxs-lookup"><span data-stu-id="5e799-126">Draw the triangle.</span></span>  
</dl>

<span data-ttu-id="5e799-127">Ces commandes de dessin sont représentées par la structure suivante dans la définition de la classe **D3D12ExecuteIndirect** .</span><span class="sxs-lookup"><span data-stu-id="5e799-127">These drawing commands are represented by the following structure in the **D3D12ExecuteIndirect** class definition.</span></span> <span data-ttu-id="5e799-128">Les commandes sont exécutées de façon séquentielle dans l’ordre dans lequel elles sont définies dans cette structure.</span><span class="sxs-lookup"><span data-stu-id="5e799-128">Commands are executed sequentially in the order they are defined in this structure.</span></span>

``` syntax
  
// Data structure to match the command signature used for ExecuteIndirect.
struct IndirectCommand
{
       D3D12_GPU_VIRTUAL_ADDRESS cbv;
       D3D12_DRAW_ARGUMENTS drawArguments;
};
```



| <span data-ttu-id="5e799-129">Workflow d’appel</span><span class="sxs-lookup"><span data-stu-id="5e799-129">Call flow</span></span>                                              | <span data-ttu-id="5e799-130">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e799-130">Parameters</span></span> |
|--------------------------------------------------------|------------|
| <span data-ttu-id="5e799-131">\_Adresse virtuelle du GPU D3D12 \_ \_ (tout simplement UINT64)</span><span class="sxs-lookup"><span data-stu-id="5e799-131">D3D12\_GPU\_VIRTUAL\_ADDRESS (simply a UINT64)</span></span>         |            |
| [<span data-ttu-id="5e799-132">**\_Arguments de dessin D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="5e799-132">**D3D12\_DRAW\_ARGUMENTS**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_draw_arguments) |            |



 

<span data-ttu-id="5e799-133">Pour accompagner la structure de données, une signature de commande est également créée, qui indique au GPU comment interpréter les données transmises à l’API [**ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) .</span><span class="sxs-lookup"><span data-stu-id="5e799-133">To accompany the data structure, a command signature is also created which instructs the GPU how to interpret the data passed in to the [**ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) API.</span></span> <span data-ttu-id="5e799-134">Cela, et la plus grande partie du code suivant, est ajouté à la méthode **LoadAssets** .</span><span class="sxs-lookup"><span data-stu-id="5e799-134">This, and the most of the following code, is added to the **LoadAssets** method.</span></span>

``` syntax
// Create the command signature used for indirect drawing.
{
       // Each command consists of a CBV update and a DrawInstanced call.
       D3D12_INDIRECT_ARGUMENT_DESC argumentDescs[2] = {};
       argumentDescs[0].Type = D3D12_INDIRECT_ARGUMENT_TYPE_CONSTANT_BUFFER_VIEW;
       argumentDescs[0].ConstantBufferView.RootParameterIndex = Cbv;
       argumentDescs[1].Type = D3D12_INDIRECT_ARGUMENT_TYPE_DRAW;

       D3D12_COMMAND_SIGNATURE_DESC commandSignatureDesc = {};
       commandSignatureDesc.pArgumentDescs = argumentDescs;
       commandSignatureDesc.NumArgumentDescs = _countof(argumentDescs);
       commandSignatureDesc.ByteStride = sizeof(IndirectCommand);

       ThrowIfFailed(m_device->CreateCommandSignature(&commandSignatureDesc, m_rootSignature.Get(), IID_PPV_ARGS(&m_commandSignature)));
}
```



| <span data-ttu-id="5e799-135">Workflow d’appel</span><span class="sxs-lookup"><span data-stu-id="5e799-135">Call flow</span></span>                                                               | <span data-ttu-id="5e799-136">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e799-136">Parameters</span></span>                                                              |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="5e799-137">**Description de l' \_ argument D3D12 indirect \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5e799-137">**D3D12\_INDIRECT\_ARGUMENT\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_indirect_argument_desc) | [<span data-ttu-id="5e799-138">**\_Type d' \_ argument \_ indirect D3D12**</span><span class="sxs-lookup"><span data-stu-id="5e799-138">**D3D12\_INDIRECT\_ARGUMENT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_indirect_argument_type) |
| [<span data-ttu-id="5e799-139">**Description de la signature de la \_ commande D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5e799-139">**D3D12\_COMMAND\_SIGNATURE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_signature_desc) |                                                                         |
| [<span data-ttu-id="5e799-140">**CreateCommandSignature**</span><span class="sxs-lookup"><span data-stu-id="5e799-140">**CreateCommandSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandsignature)   |                                                                         |



 

## <a name="create-a-graphics-and-compute-root-signature"></a><span data-ttu-id="5e799-141">Créer un graphique et une signature racine de calcul</span><span class="sxs-lookup"><span data-stu-id="5e799-141">Create a graphics and compute root signature</span></span>

<span data-ttu-id="5e799-142">Nous créons également un graphique et une signature racine de calcul.</span><span class="sxs-lookup"><span data-stu-id="5e799-142">We also create both a graphics and a compute root signature.</span></span> <span data-ttu-id="5e799-143">La signature racine Graphics définit simplement un CBV racine.</span><span class="sxs-lookup"><span data-stu-id="5e799-143">The graphics root signature just defines a root CBV.</span></span> <span data-ttu-id="5e799-144">Notez que nous allons mapper l’index de ce paramètre racine dans [**l' \_ argument indirect D3D12 \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_indirect_argument_desc) (indiqué ci-dessus) lorsque la signature de la commande est définie.</span><span class="sxs-lookup"><span data-stu-id="5e799-144">Note that we map the index of this root parameter in the [**D3D12\_INDIRECT\_ARGUMENT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_indirect_argument_desc) (shown above) when the command signature is defined.</span></span> <span data-ttu-id="5e799-145">La signature de la racine de calcul définit :</span><span class="sxs-lookup"><span data-stu-id="5e799-145">The compute root signature defines:</span></span>

-   <span data-ttu-id="5e799-146">Un tableau de descripteurs commun avec trois emplacements (deux SRV et un UAV) :</span><span class="sxs-lookup"><span data-stu-id="5e799-146">A common descriptor table with three slots (two SRV’s and one UAV):</span></span>
    -   <span data-ttu-id="5e799-147">Un SRV expose les mémoires tampons constantes au nuanceur de calcul</span><span class="sxs-lookup"><span data-stu-id="5e799-147">One SRV exposes the constant buffers to the compute shader</span></span>
    -   <span data-ttu-id="5e799-148">Un SRV expose le tampon de commande au nuanceur de calcul</span><span class="sxs-lookup"><span data-stu-id="5e799-148">One SRV exposes the command buffer to the compute shader</span></span>
    -   <span data-ttu-id="5e799-149">Le UAV est l’emplacement où le nuanceur de calcul enregistre les commandes pour les triangles visibles</span><span class="sxs-lookup"><span data-stu-id="5e799-149">The UAV is where the compute shader saves the commands for the visible triangles</span></span>
-   <span data-ttu-id="5e799-150">Quatre constantes racine :</span><span class="sxs-lookup"><span data-stu-id="5e799-150">Four root constants:</span></span>
    -   <span data-ttu-id="5e799-151">Moitié de la largeur d’un côté du triangle</span><span class="sxs-lookup"><span data-stu-id="5e799-151">Half the width of one side of the triangle</span></span>
    -   <span data-ttu-id="5e799-152">Position z des sommets du triangle</span><span class="sxs-lookup"><span data-stu-id="5e799-152">The z position of the triangle vertices</span></span>
    -   <span data-ttu-id="5e799-153">Décalage +/-x du plan d’élimination dans un espace homogène \[ -1, 1\]</span><span class="sxs-lookup"><span data-stu-id="5e799-153">The +/- x offset of the culling plane in homogenous space \[-1,1\]</span></span>
    -   <span data-ttu-id="5e799-154">Nombre de commandes indirectes dans la mémoire tampon de commande</span><span class="sxs-lookup"><span data-stu-id="5e799-154">The number of indirect commands in the command buffer</span></span>

``` syntax
// Create the root signatures.
{
       CD3DX12_ROOT_PARAMETER rootParameters[GraphicsRootParametersCount];
       rootParameters[Cbv].InitAsConstantBufferView(0, 0, D3D12_SHADER_VISIBILITY_VERTEX);

       CD3DX12_ROOT_SIGNATURE_DESC rootSignatureDesc;
       rootSignatureDesc.Init(_countof(rootParameters), rootParameters, 0, nullptr, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT);

       ComPtr<ID3DBlob> signature;
       ComPtr<ID3DBlob> error;
       ThrowIfFailed(D3D12SerializeRootSignature(&rootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
       ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_rootSignature)));

       // Create compute signature.
       CD3DX12_DESCRIPTOR_RANGE ranges[2];
       ranges[0].Init(D3D12_DESCRIPTOR_RANGE_TYPE_SRV, 2, 0);
       ranges[1].Init(D3D12_DESCRIPTOR_RANGE_TYPE_UAV, 1, 0);

       CD3DX12_ROOT_PARAMETER computeRootParameters[ComputeRootParametersCount];
       computeRootParameters[SrvUavTable].InitAsDescriptorTable(2, ranges);
       computeRootParameters[RootConstants].InitAsConstants(4, 0);

       CD3DX12_ROOT_SIGNATURE_DESC computeRootSignatureDesc;
       computeRootSignatureDesc.Init(_countof(computeRootParameters), computeRootParameters);

       ThrowIfFailed(D3D12SerializeRootSignature(&computeRootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
       ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_computeRootSignature)));
}
```



| <span data-ttu-id="5e799-155">Workflow d’appel</span><span class="sxs-lookup"><span data-stu-id="5e799-155">Call flow</span></span>                                                             | <span data-ttu-id="5e799-156">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e799-156">Parameters</span></span>                                                            |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="5e799-157">**\_Paramètre racine \_ CD3DX12**</span><span class="sxs-lookup"><span data-stu-id="5e799-157">**CD3DX12\_ROOT\_PARAMETER**</span></span>](cd3dx12-root-parameter.md)            | [<span data-ttu-id="5e799-158">**\_Visibilité du nuanceur D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="5e799-158">**D3D12\_SHADER\_VISIBILITY**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)          |
| [<span data-ttu-id="5e799-159">**Description de la \_ signature racine CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5e799-159">**CD3DX12\_ROOT\_SIGNATURE\_DESC**</span></span>](cd3dx12-root-signature-desc.md) | [<span data-ttu-id="5e799-160">**\_Indicateurs de \_ signature \_ racine D3D12**</span><span class="sxs-lookup"><span data-stu-id="5e799-160">**D3D12\_ROOT\_SIGNATURE\_FLAGS**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags)   |
| <span data-ttu-id="5e799-161">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5e799-161">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span></span>                                   |                                                                       |
| [<span data-ttu-id="5e799-162">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="5e799-162">**D3D12SerializeRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [<span data-ttu-id="5e799-163">**\_Version de \_ signature \_ racine D3D**</span><span class="sxs-lookup"><span data-stu-id="5e799-163">**D3D\_ROOT\_SIGNATURE\_VERSION**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [<span data-ttu-id="5e799-164">**CreateRootSignature**</span><span class="sxs-lookup"><span data-stu-id="5e799-164">**CreateRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |
| [<span data-ttu-id="5e799-165">**\_Plage du descripteur CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="5e799-165">**CD3DX12\_DESCRIPTOR\_RANGE**</span></span>](cd3dx12-descriptor-range.md)        | [<span data-ttu-id="5e799-166">**\_Type de plage du descripteur D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5e799-166">**D3D12\_DESCRIPTOR\_RANGE\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) |
| [<span data-ttu-id="5e799-167">**\_Paramètre racine \_ CD3DX12**</span><span class="sxs-lookup"><span data-stu-id="5e799-167">**CD3DX12\_ROOT\_PARAMETER**</span></span>](cd3dx12-root-parameter.md)            | [<span data-ttu-id="5e799-168">**\_Visibilité du nuanceur D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="5e799-168">**D3D12\_SHADER\_VISIBILITY**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)          |
| [<span data-ttu-id="5e799-169">**Description de la \_ signature racine CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5e799-169">**CD3DX12\_ROOT\_SIGNATURE\_DESC**</span></span>](cd3dx12-root-signature-desc.md) | [<span data-ttu-id="5e799-170">**\_Indicateurs de \_ signature \_ racine D3D12**</span><span class="sxs-lookup"><span data-stu-id="5e799-170">**D3D12\_ROOT\_SIGNATURE\_FLAGS**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags)   |
| <span data-ttu-id="5e799-171">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5e799-171">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span></span>                                   |                                                                       |
| [<span data-ttu-id="5e799-172">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="5e799-172">**D3D12SerializeRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [<span data-ttu-id="5e799-173">**\_Version de \_ signature \_ racine D3D**</span><span class="sxs-lookup"><span data-stu-id="5e799-173">**D3D\_ROOT\_SIGNATURE\_VERSION**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [<span data-ttu-id="5e799-174">**CreateRootSignature**</span><span class="sxs-lookup"><span data-stu-id="5e799-174">**CreateRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |



 

## <a name="create-a-shader-resource-view-srv-for-the-compute-shader"></a><span data-ttu-id="5e799-175">Créer une vue de ressource de nuanceur (SRV) pour le nuanceur de calcul</span><span class="sxs-lookup"><span data-stu-id="5e799-175">Create a shader resource view (SRV) for the compute shader</span></span>

<span data-ttu-id="5e799-176">Après avoir créé les objets d’état de pipeline, les mémoires tampons de vertex, un stencil de profondeur et les mémoires tampons constantes, l’exemple crée ensuite une vue de ressource de nuanceur (SRV) de la mémoire tampon constante afin que le nuanceur de calcul puisse accéder aux données dans la mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="5e799-176">After creating the pipeline state objects, vertex buffers, a depth stencil, and the constant buffers, the sample then creates a shader resource view (SRV) of the constant buffer so that the compute shader can access the data in the constant buffer.</span></span>

``` syntax
// Create shader resource views (SRV) of the constant buffers for the
// compute shader to read from.
       D3D12_SHADER_RESOURCE_VIEW_DESC srvDesc = {};
       srvDesc.Format = DXGI_FORMAT_UNKNOWN;
       srvDesc.ViewDimension = D3D12_SRV_DIMENSION_BUFFER;
       srvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
       srvDesc.Buffer.NumElements = TriangleCount;
       srvDesc.Buffer.StructureByteStride = sizeof(ConstantBufferData);
       srvDesc.Buffer.Flags = D3D12_BUFFER_SRV_FLAG_NONE;

       CD3DX12_CPU_DESCRIPTOR_HANDLE cbvSrvHandle(m_cbvSrvUavHeap->GetCPUDescriptorHandleForHeapStart(), CbvSrvOffset, m_cbvSrvUavDescriptorSize);
       for (UINT frame = 0; frame < FrameCount; frame++)
       {
              srvDesc.Buffer.FirstElement = frame * TriangleCount;
              m_device->CreateShaderResourceView(m_constantBuffer.Get(), &srvDesc, cbvSrvHandle);
              cbvSrvHandle.Offset(CbvSrvUavDescriptorCountPerFrame, m_cbvSrvUavDescriptorSize);
       }
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5e799-177">Workflow d’appel</span><span class="sxs-lookup"><span data-stu-id="5e799-177">Call flow</span></span></th>
<th><span data-ttu-id="5e799-178">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e799-178">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5e799-179"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-179"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="5e799-180"><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-180"><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span></span><br /><span data-ttu-id="5e799-181">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-181">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a></span></span><br /><span data-ttu-id="5e799-182">
<a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a></span><span class="sxs-lookup"><span data-stu-id="5e799-182">
<a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5e799-183"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-183"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span></span></td>
<td><span data-ttu-id="5e799-184"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-184"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5e799-185"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>CreateShaderResourceView</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-185"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>CreateShaderResourceView</strong></a></span></span></td>

</tr>
</tbody>
</table>



 

## <a name="create-the-indirect-command-buffers"></a><span data-ttu-id="5e799-186">Créer les mémoires tampons de commande indirectes</span><span class="sxs-lookup"><span data-stu-id="5e799-186">Create the indirect command buffers</span></span>

<span data-ttu-id="5e799-187">Nous créons ensuite les mémoires tampons de commande indirectes et définissons leur contenu à l’aide du code suivant.</span><span class="sxs-lookup"><span data-stu-id="5e799-187">We then create the indirect command buffers and define their content using the following code.</span></span> <span data-ttu-id="5e799-188">Nous dessinons les mêmes sommets de triangle 1024 fois, mais vous pointez vers un emplacement de mémoire tampon constante différent avec chaque appel de dessin.</span><span class="sxs-lookup"><span data-stu-id="5e799-188">We draw the same triangle vertices 1024 times, but point to a different constant buffer location with each draw call.</span></span>

``` syntax
       D3D12_GPU_VIRTUAL_ADDRESS gpuAddress = m_constantBuffer->GetGPUVirtualAddress();
       UINT commandIndex = 0;

       for (UINT frame = 0; frame < FrameCount; frame++)
       {
              for (UINT n = 0; n < TriangleCount; n++)
              {
                    commands[commandIndex].cbv = gpuAddress;
                    commands[commandIndex].drawArguments.VertexCountPerInstance = 3;
                    commands[commandIndex].drawArguments.InstanceCount = 1;
                    commands[commandIndex].drawArguments.StartVertexLocation = 0;
                    commands[commandIndex].drawArguments.StartInstanceLocation = 0;

                    commandIndex++;
                    gpuAddress += sizeof(ConstantBufferData);
              }
       }
```



| <span data-ttu-id="5e799-189">Workflow d’appel</span><span class="sxs-lookup"><span data-stu-id="5e799-189">Call flow</span></span>                    | <span data-ttu-id="5e799-190">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e799-190">Parameters</span></span>                                                          |
|------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="5e799-191">\_ \_ Adresse virtuelle du GPU D3D12 \_</span><span class="sxs-lookup"><span data-stu-id="5e799-191">D3D12\_GPU\_VIRTUAL\_ADDRESS</span></span> | [<span data-ttu-id="5e799-192">**GetGPUVirtualAddress**</span><span class="sxs-lookup"><span data-stu-id="5e799-192">**GetGPUVirtualAddress**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress) |



 

<span data-ttu-id="5e799-193">Après avoir chargé les tampons de commande dans le GPU, nous créons également un SRV de ceux-ci pour que le nuanceur de calcul les lise.</span><span class="sxs-lookup"><span data-stu-id="5e799-193">After uploading the command buffers to the GPU, we also create an SRV of them for the compute shader to read from.</span></span> <span data-ttu-id="5e799-194">Cela est très similaire au SRV créé de la mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="5e799-194">This is very similar to the SRV created of the constant buffer.</span></span>

``` syntax
// Create SRVs for the command buffers.
       D3D12_SHADER_RESOURCE_VIEW_DESC srvDesc = {};
       srvDesc.Format = DXGI_FORMAT_UNKNOWN;
       srvDesc.ViewDimension = D3D12_SRV_DIMENSION_BUFFER;
       srvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
       srvDesc.Buffer.NumElements = TriangleCount;
       srvDesc.Buffer.StructureByteStride = sizeof(IndirectCommand);
       srvDesc.Buffer.Flags = D3D12_BUFFER_SRV_FLAG_NONE;

       CD3DX12_CPU_DESCRIPTOR_HANDLE commandsHandle(m_cbvSrvUavHeap->GetCPUDescriptorHandleForHeapStart(), CommandsOffset, m_cbvSrvUavDescriptorSize);
       for (UINT frame = 0; frame < FrameCount; frame++)
       {
              srvDesc.Buffer.FirstElement = frame * TriangleCount;
              m_device->CreateShaderResourceView(m_commandBuffer.Get(), &srvDesc, commandsHandle);
              commandsHandle.Offset(CbvSrvUavDescriptorCountPerFrame, m_cbvSrvUavDescriptorSize);
       }
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5e799-195">Workflow d’appel</span><span class="sxs-lookup"><span data-stu-id="5e799-195">Call flow</span></span></th>
<th><span data-ttu-id="5e799-196">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e799-196">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5e799-197"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-197"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="5e799-198"><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-198"><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span></span><br /><span data-ttu-id="5e799-199">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-199">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a></span></span><br /><span data-ttu-id="5e799-200">
<a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a></span><span class="sxs-lookup"><span data-stu-id="5e799-200">
<a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a></span></span><br /><span data-ttu-id="5e799-201">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_srv_flags"><strong>D3D12_BUFFER_SRV_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-201">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_srv_flags"><strong>D3D12_BUFFER_SRV_FLAG</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5e799-202"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-202"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span></span></td>
<td><span data-ttu-id="5e799-203"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-203"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5e799-204"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>CreateShaderResourceView</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-204"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>CreateShaderResourceView</strong></a></span></span></td>

</tr>
</tbody>
</table>



 

## <a name="create-the-compute-uavs"></a><span data-ttu-id="5e799-205">Créer le calcul UAVs</span><span class="sxs-lookup"><span data-stu-id="5e799-205">Create the compute UAVs</span></span>

<span data-ttu-id="5e799-206">Nous devons créer le UAVs qui stockera les résultats du travail de calcul.</span><span class="sxs-lookup"><span data-stu-id="5e799-206">We need to create the UAVs that will store the results of the compute work.</span></span> <span data-ttu-id="5e799-207">Lorsqu’un triangle est considéré par le nuanceur de calcul comme visible pour la cible de rendu, il est ajouté à ce UAV, puis utilisé par l’API [**ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) .</span><span class="sxs-lookup"><span data-stu-id="5e799-207">When a triangle is deemed by the compute shader to be visible to the render target, it will be appended to this UAV and then consumed by the [**ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) API.</span></span>

``` syntax
CD3DX12_CPU_DESCRIPTOR_HANDLE processedCommandsHandle(m_cbvSrvUavHeap->GetCPUDescriptorHandleForHeapStart(), ProcessedCommandsOffset, m_cbvSrvUavDescriptorSize);
for (UINT frame = 0; frame < FrameCount; frame++)
{
       // Allocate a buffer large enough to hold all of the indirect commands
       // for a single frame as well as a UAV counter.
       commandBufferDesc = CD3DX12_RESOURCE_DESC::Buffer(CommandBufferSizePerFrame + sizeof(UINT), D3D12_RESOURCE_FLAG_ALLOW_UNORDERED_ACCESS);
       CD3DX12_HEAP_PROPERTIES heapProps(D3D12_HEAP_TYPE_DEFAULT);
       ThrowIfFailed(m_device->CreateCommittedResource(
             &heapProps,
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
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5e799-208">Workflow d’appel</span><span class="sxs-lookup"><span data-stu-id="5e799-208">Call flow</span></span></th>
<th><span data-ttu-id="5e799-209">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e799-209">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5e799-210"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-210"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span></span></td>
<td><span data-ttu-id="5e799-211"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-211"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5e799-212"><a href="cd3dx12-resource-desc.md"><strong>CD3DX12_RESOURCE_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-212"><a href="cd3dx12-resource-desc.md"><strong>CD3DX12_RESOURCE_DESC</strong></a></span></span></td>
<td><span data-ttu-id="5e799-213"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags"><strong>D3D12_RESOURCE_FLAGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-213"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags"><strong>D3D12_RESOURCE_FLAGS</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5e799-214"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-214"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span></span></td>
<td><dl><span data-ttu-id="5e799-215"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-215"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span></span><br /><span data-ttu-id="5e799-216">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-216">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span></span><br /><span data-ttu-id="5e799-217">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-217">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a></span></span><br /><span data-ttu-id="5e799-218">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-218">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5e799-219"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_unordered_access_view_desc"><strong>D3D12_UNORDERED_ACCESS_VIEW_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-219"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_unordered_access_view_desc"><strong>D3D12_UNORDERED_ACCESS_VIEW_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="5e799-220"><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-220"><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span></span><br /><span data-ttu-id="5e799-221">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_uav_dimension"><strong>D3D12_UAV_DIMENSION</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-221">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_uav_dimension"><strong>D3D12_UAV_DIMENSION</strong></a></span></span><br /><span data-ttu-id="5e799-222">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags"><strong>D3D12_BUFFER_UAV_FLAGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-222">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags"><strong>D3D12_BUFFER_UAV_FLAGS</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5e799-223"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview"><strong>CreateUnorderedAccessView</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-223"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview"><strong>CreateUnorderedAccessView</strong></a></span></span></td>

</tr>
</tbody>
</table>



 

## <a name="drawing-the-frame"></a><span data-ttu-id="5e799-224">Dessin du frame</span><span class="sxs-lookup"><span data-stu-id="5e799-224">Drawing the frame</span></span>

<span data-ttu-id="5e799-225">Lorsqu’il est temps de dessiner le cadre, si nous sommes en mode lorsque le nuanceur de calcul est appelé et que les commandes indirectes sont traitées par le GPU, nous [**distribuerons**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch) d’abord ce travail pour remplir notre mémoire tampon de commande pour [**ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect).</span><span class="sxs-lookup"><span data-stu-id="5e799-225">When it comes time to draw the frame, if we are in the mode when the compute shader is being invoked and indirect commands are being processed by the GPU, we will first [**Dispatch**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch) that work to populate our command buffer for [**ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect).</span></span> <span data-ttu-id="5e799-226">Les extraits de code suivants sont ajoutés à la méthode **PopulateCommandLists** .</span><span class="sxs-lookup"><span data-stu-id="5e799-226">The following code snippets are added to the **PopulateCommandLists** method.</span></span>

``` syntax
// Record the compute commands that will cull triangles and prevent them from being processed by the vertex shader.
if (m_enableCulling)
{
       UINT frameDescriptorOffset = m_frameIndex * CbvSrvUavDescriptorCountPerFrame;
       D3D12_GPU_DESCRIPTOR_HANDLE cbvSrvUavHandle = m_cbvSrvUavHeap->GetGPUDescriptorHandleForHeapStart();

       m_computeCommandList->SetComputeRootSignature(m_computeRootSignature.Get());

       ID3D12DescriptorHeap* ppHeaps[] = { m_cbvSrvUavHeap.Get() };
       m_computeCommandList->SetDescriptorHeaps(_countof(ppHeaps), ppHeaps);

       m_computeCommandList->SetComputeRootDescriptorTable(
              SrvUavTable,
              CD3DX12_GPU_DESCRIPTOR_HANDLE(cbvSrvUavHandle, CbvSrvOffset + frameDescriptorOffset, m_cbvSrvUavDescriptorSize));

       m_computeCommandList->SetComputeRoot32BitConstants(RootConstants, 4, reinterpret_cast<void*>(&m_csRootConstants), 0);

       // Reset the UAV counter for this frame.
       m_computeCommandList->CopyBufferRegion(m_processedCommandBuffers[m_frameIndex].Get(), CommandBufferSizePerFrame, m_processedCommandBufferCounterReset.Get(), 0, sizeof(UINT));

       D3D12_RESOURCE_BARRIER barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_processedCommandBuffers[m_frameIndex].Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_UNORDERED_ACCESS);
       m_computeCommandList->ResourceBarrier(1, &barrier);

       m_computeCommandList->Dispatch(static_cast<UINT>(ceil(TriangleCount / float(ComputeThreadBlockSize))), 1, 1);
}

ThrowIfFailed(m_computeCommandList->Close());
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5e799-227">Workflow d’appel</span><span class="sxs-lookup"><span data-stu-id="5e799-227">Call flow</span></span></th>
<th><span data-ttu-id="5e799-228">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e799-228">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5e799-229"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle"><strong>D3D12_GPU_DESCRIPTOR_HANDLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-229"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle"><strong>D3D12_GPU_DESCRIPTOR_HANDLE</strong></a></span></span></td>
<td><span data-ttu-id="5e799-230"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart"><strong>GetGPUDescriptorHandleForHeapStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-230"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart"><strong>GetGPUDescriptorHandleForHeapStart</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5e799-231"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature"><strong>SetComputeRootSignature</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-231"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature"><strong>SetComputeRootSignature</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="5e799-232"><a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap"><strong>ID3D12DescriptorHeap</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-232"><a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap"><strong>ID3D12DescriptorHeap</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="5e799-233"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps"><strong>SetDescriptorHeaps</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-233"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps"><strong>SetDescriptorHeaps</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="5e799-234"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable"><strong>SetComputeRootDescriptorTable</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-234"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable"><strong>SetComputeRootDescriptorTable</strong></a></span></span></td>
<td><span data-ttu-id="5e799-235"><a href="cd3dx12-gpu-descriptor-handle.md"><strong>CD3DX12_GPU_DESCRIPTOR_HANDLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-235"><a href="cd3dx12-gpu-descriptor-handle.md"><strong>CD3DX12_GPU_DESCRIPTOR_HANDLE</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5e799-236"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants"><strong>SetComputeRoot32BitConstants</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-236"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants"><strong>SetComputeRoot32BitConstants</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="5e799-237"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion"><strong>CopyBufferRegion</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-237"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion"><strong>CopyBufferRegion</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="5e799-238"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier"><strong>D3D12_RESOURCE_BARRIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-238"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier"><strong>D3D12_RESOURCE_BARRIER</strong></a></span></span></td>
<td><dl><span data-ttu-id="5e799-239"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-239"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span></span><br /><span data-ttu-id="5e799-240">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-240">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5e799-241"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-241"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="5e799-242"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch"><strong>Dispatch</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-242"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch"><strong>Dispatch</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="5e799-243"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close"><strong>Fermer</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-243"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close"><strong>Close</strong></a></span></span></td>

</tr>
</tbody>
</table>



 

<span data-ttu-id="5e799-244">Ensuite, nous allons exécuter les commandes dans UAV (élimination du GPU activée) ou dans le tampon de commandes complet (élimination du GPU désactivée).</span><span class="sxs-lookup"><span data-stu-id="5e799-244">Then we will execute the commands in either the UAV (GPU culling enabled) or the full command buffer (GPU culling disabled).</span></span>

``` syntax
// Record the rendering commands.
{
       // Set necessary state.
       m_commandList->SetGraphicsRootSignature(m_rootSignature.Get());

       ID3D12DescriptorHeap* ppHeaps[] = { m_cbvSrvUavHeap.Get() };
       m_commandList->SetDescriptorHeaps(_countof(ppHeaps), ppHeaps);

       m_commandList->RSSetViewports(1, &m_viewport);
       m_commandList->RSSetScissorRects(1, m_enableCulling ? &m_cullingScissorRect : &m_scissorRect);

       // Indicate that the command buffer will be used for indirect drawing
       // and that the back buffer will be used as a render target.
       D3D12_RESOURCE_BARRIER barriers[2] = {
              CD3DX12_RESOURCE_BARRIER::Transition(
                    m_enableCulling ? m_processedCommandBuffers[m_frameIndex].Get() : m_commandBuffer.Get(),
                    m_enableCulling ? D3D12_RESOURCE_STATE_UNORDERED_ACCESS : D3D12_RESOURCE_STATE_NON_PIXEL_SHADER_RESOURCE,
                    D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT),
              CD3DX12_RESOURCE_BARRIER::Transition(
                    m_renderTargets[m_frameIndex].Get(),
                    D3D12_RESOURCE_STATE_PRESENT,
                    D3D12_RESOURCE_STATE_RENDER_TARGET)
       };

       m_commandList->ResourceBarrier(_countof(barriers), barriers);

       CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
       CD3DX12_CPU_DESCRIPTOR_HANDLE dsvHandle(m_dsvHeap->GetCPUDescriptorHandleForHeapStart());
       m_commandList->OMSetRenderTargets(1, &rtvHandle, FALSE, &dsvHandle);

       // Record commands.
       const float clearColor[] = { 0.0f, 0.2f, 0.4f, 1.0f };
       m_commandList->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
       m_commandList->ClearDepthStencilView(dsvHandle, D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

       m_commandList->IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP);
       m_commandList->IASetVertexBuffers(0, 1, &m_vertexBufferView);

       if (m_enableCulling)
       {
              // Draw the triangles that have not been culled.
              m_commandList->ExecuteIndirect(
                    m_commandSignature.Get(),
                    TriangleCount,
                    m_processedCommandBuffers[m_frameIndex].Get(),
                    0,
                    m_processedCommandBuffers[m_frameIndex].Get(),
                    CommandBufferSizePerFrame);
       }
       else
       {
              // Draw all of the triangles.
              m_commandList->ExecuteIndirect(
                    m_commandSignature.Get(),
                    TriangleCount,
                    m_commandBuffer.Get(),
                    CommandBufferSizePerFrame * m_frameIndex,
                    nullptr,
                    0);
       }

       // Indicate that the command buffer may be used by the compute shader
       // and that the back buffer will now be used to present.
       barriers[0].Transition.StateBefore = D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT;
       barriers[0].Transition.StateAfter = m_enableCulling ? D3D12_RESOURCE_STATE_COPY_DEST : D3D12_RESOURCE_STATE_NON_PIXEL_SHADER_RESOURCE;
       barriers[1].Transition.StateBefore = D3D12_RESOURCE_STATE_RENDER_TARGET;
       barriers[1].Transition.StateAfter = D3D12_RESOURCE_STATE_PRESENT;

       m_commandList->ResourceBarrier(_countof(barriers), barriers);

       ThrowIfFailed(m_commandList->Close());
}
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5e799-245">Workflow d’appel</span><span class="sxs-lookup"><span data-stu-id="5e799-245">Call flow</span></span></th>
<th><span data-ttu-id="5e799-246">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e799-246">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5e799-247"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature"><strong>SetGraphicsRootSignature</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-247"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature"><strong>SetGraphicsRootSignature</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="5e799-248"><a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap"><strong>ID3D12DescriptorHeap</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-248"><a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap"><strong>ID3D12DescriptorHeap</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="5e799-249"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps"><strong>SetDescriptorHeaps</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-249"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps"><strong>SetDescriptorHeaps</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="5e799-250"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports"><strong>RSSetViewports</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-250"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports"><strong>RSSetViewports</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="5e799-251"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects"><strong>RSSetScissorRects</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-251"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects"><strong>RSSetScissorRects</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="5e799-252"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier"><strong>D3D12_RESOURCE_BARRIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-252"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier"><strong>D3D12_RESOURCE_BARRIER</strong></a></span></span></td>
<td><dl><span data-ttu-id="5e799-253"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-253"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span></span><br /><span data-ttu-id="5e799-254">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-254">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5e799-255"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-255"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="5e799-256"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-256"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span></span></td>
<td><span data-ttu-id="5e799-257"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-257"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5e799-258"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets"><strong>OMSetRenderTargets</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-258"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets"><strong>OMSetRenderTargets</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="5e799-259"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview"><strong>ClearRenderTargetView</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-259"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview"><strong>ClearRenderTargetView</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="5e799-260"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview"><strong>ClearDepthStencilView</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-260"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview"><strong>ClearDepthStencilView</strong></a></span></span></td>
<td><span data-ttu-id="5e799-261"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_clear_flags"><strong>D3D12_CLEAR_FLAGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-261"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_clear_flags"><strong>D3D12_CLEAR_FLAGS</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5e799-262"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology"><strong>IASetPrimitiveTopology</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-262"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology"><strong>IASetPrimitiveTopology</strong></a></span></span></td>
<td><span data-ttu-id="5e799-263"><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology"><strong>D3D_PRIMITIVE_TOPOLOGY</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-263"><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology"><strong>D3D_PRIMITIVE_TOPOLOGY</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5e799-264"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers"><strong>IASetVertexBuffers</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-264"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers"><strong>IASetVertexBuffers</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="5e799-265"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect"><strong>ExecuteIndirect</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-265"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect"><strong>ExecuteIndirect</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="5e799-266"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-266"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span></span></td>
<td><span data-ttu-id="5e799-267"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-267"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5e799-268"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close"><strong>Fermer</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e799-268"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close"><strong>Close</strong></a></span></span></td>

</tr>
</tbody>
</table>



 

<span data-ttu-id="5e799-269">Si nous sommes en mode d’élimination du GPU, la file d’attente de commandes Graphics attend la fin du travail de calcul avant de commencer à exécuter les commandes indirectes.</span><span class="sxs-lookup"><span data-stu-id="5e799-269">If we are in GPU culling mode, we will have the graphics command queue wait for the compute work to complete before it begins executing the indirect commands.</span></span> <span data-ttu-id="5e799-270">Dans la méthode **OnRender** , l’extrait de code suivant est ajouté.</span><span class="sxs-lookup"><span data-stu-id="5e799-270">In the **OnRender** method the following snippet is added.</span></span>

``` syntax
// Execute the compute work.
if (m_enableCulling)
{
       ID3D12CommandList* ppCommandLists[] = { m_computeCommandList.Get() };
       m_computeCommandQueue->ExecuteCommandLists(_countof(ppCommandLists), ppCommandLists);
       m_computeCommandQueue->Signal(m_computeFence.Get(), m_fenceValues[m_frameIndex]);

       // Execute the rendering work only when the compute work is complete.
       m_commandQueue->Wait(m_computeFence.Get(), m_fenceValues[m_frameIndex]);
}

// Execute the rendering work.
ID3D12CommandList* ppCommandLists[] = { m_commandList.Get() };
m_commandQueue->ExecuteCommandLists(_countof(ppCommandLists), ppCommandLists);
```



| <span data-ttu-id="5e799-271">Workflow d’appel</span><span class="sxs-lookup"><span data-stu-id="5e799-271">Call flow</span></span>                                                             | <span data-ttu-id="5e799-272">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e799-272">Parameters</span></span> |
|-----------------------------------------------------------------------|------------|
| [<span data-ttu-id="5e799-273">**ID3D12CommandList**</span><span class="sxs-lookup"><span data-stu-id="5e799-273">**ID3D12CommandList**</span></span>](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist)                        |            |
| [<span data-ttu-id="5e799-274">**ExecuteCommandLists**</span><span class="sxs-lookup"><span data-stu-id="5e799-274">**ExecuteCommandLists**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) |            |
| [<span data-ttu-id="5e799-275">**Témoin**</span><span class="sxs-lookup"><span data-stu-id="5e799-275">**Signal**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-signal)                           |            |
| [<span data-ttu-id="5e799-276">**Wait**</span><span class="sxs-lookup"><span data-stu-id="5e799-276">**Wait**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-wait)                               |            |
| [<span data-ttu-id="5e799-277">**ID3D12CommandList**</span><span class="sxs-lookup"><span data-stu-id="5e799-277">**ID3D12CommandList**</span></span>](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist)                        |            |
| [<span data-ttu-id="5e799-278">**ExecuteCommandLists**</span><span class="sxs-lookup"><span data-stu-id="5e799-278">**ExecuteCommandLists**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) |            |



 

## <a name="run-the-sample"></a><span data-ttu-id="5e799-279">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="5e799-279">Run the sample</span></span>

<span data-ttu-id="5e799-280">L’exemple avec l’élimination de la primitive GPU.</span><span class="sxs-lookup"><span data-stu-id="5e799-280">The sample with GPU primitive culling.</span></span>

![capture d’écran de l’exemple indirect Exectue avec l’élimination du GPU](images/executeindirect-withculling.png)

<span data-ttu-id="5e799-282">L’exemple sans l’élimination de la primitive GPU.</span><span class="sxs-lookup"><span data-stu-id="5e799-282">The sample without GPU primitive culling.</span></span>

![capture d’écran de l’exemple Exectue indirect sans élimination du GPU](images/executeindirect-withoutculling.png)

## <a name="related-topics"></a><span data-ttu-id="5e799-284">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5e799-284">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e799-285">Guide pas à pas du code D3D12</span><span class="sxs-lookup"><span data-stu-id="5e799-285">D3D12 Code Walk-Throughs</span></span>](d3d12-code-walk-throughs.md)
</dt> <dt>

[<span data-ttu-id="5e799-286">Didacticiels vidéo sur DirectX Advanced Learning : exécuter des éliminations de GPU indirectes et Async</span><span class="sxs-lookup"><span data-stu-id="5e799-286">DirectX advanced learning video tutorials : Execute Indirect and Async GPU culling</span></span>](https://www.youtube.com/watch?v=fKD-VKJeeds)
</dt> <dt>

[<span data-ttu-id="5e799-287">Dessin indirect</span><span class="sxs-lookup"><span data-stu-id="5e799-287">Indirect Drawing</span></span>](indirect-drawing.md)
</dt> </dl>

 

 
