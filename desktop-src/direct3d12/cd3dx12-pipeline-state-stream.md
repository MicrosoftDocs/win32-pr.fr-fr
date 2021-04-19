---
title: Structure CD3DX12_PIPELINE_STATE_STREAM (D3dx12. h)
description: Structure d’assistance pour la création et l’utilisation des graphiques et des États de pipeline de calcul via une interface combinée. Consultez D3D12 \_ Graphics \_ pipeline \_ State \_ DESC et D3D12 \_ Compute \_ pipeline \_ State \_ desc. | Structure CD3DX12_PIPELINE_STATE_STREAM (D3dx12. h)
ms.assetid: C0CEFC67-72B3-4A8D-9C88-381990FC9898
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d52b9090fa1d3870027bbe360164627472c039e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106537240"
---
# <a name="cd3dx12_pipeline_state_stream-structure"></a><span data-ttu-id="defb6-106">\_Structure du \_ flux d’État du PIPELINe CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="defb6-106">CD3DX12\_PIPELINE\_STATE\_STREAM structure</span></span>

<span data-ttu-id="defb6-107">Structure d’assistance pour la création et l’utilisation des graphiques et des États de pipeline de calcul via une interface combinée.</span><span class="sxs-lookup"><span data-stu-id="defb6-107">A helper structure for creating and working with graphics and compute pipeline states through a combined interface.</span></span> <span data-ttu-id="defb6-108">Consultez [**D3D12 \_ Graphics \_ pipeline \_ State \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) et [**D3D12 \_ Compute \_ pipeline \_ State \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).</span><span class="sxs-lookup"><span data-stu-id="defb6-108">See [**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) and [**D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).</span></span>

<span data-ttu-id="defb6-109">\_ \_ Le flux d’État du pipeline CD3DX12 \_ prend en charge Windows 10 Creators Update et versions ultérieures, mais ne prend pas en charge les nouvelles fonctionnalités de la mise à jour des créateurs de automne, telles que l’instanciation</span><span class="sxs-lookup"><span data-stu-id="defb6-109">CD3DX12\_PIPELINE\_STATE\_STREAM supports Windows 10 Creators Update and newer but doesn't support new features of the Fall Creators update, such as view instancing.</span></span> <span data-ttu-id="defb6-110">Pour prendre en charge les fonctionnalités de la mise à jour des créateurs de automne, utilisez à la place [**CD3DX12 \_ pipeline \_ State \_ STREAM1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) .</span><span class="sxs-lookup"><span data-stu-id="defb6-110">To support features of the Fall Creators update, use [**CD3DX12\_PIPELINE\_STATE\_STREAM1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="defb6-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="defb6-111">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM {
  CD3DX12_PIPELINE_STATE_STREAM                       CD3DX12_PIPELINE_STATE_STREAM();
  CD3DX12_PIPELINE_STATE_STREAM                       CD3DX12_PIPELINE_STATE_STREAM(const D3D12_GRAPHICS_PIPELINE_STATE_DESC& Desc);
  CD3DX12_PIPELINE_STATE_STREAM                       CD3DX12_PIPELINE_STATE_STREAM(const D3D12_COMPUTE_PIPELINE_STATE_DESC& Desc);
  D3D12_GRAPHICS_PIPELINE_STATE_DESC                  GraphicsDescV0();
  D3D12_COMPUTE_PIPELINE_STATE_DESC                   ComputeDescV0();
  CD3DX12_PIPELINE_STATE_STREAM_FLAGS                 Flags;
  CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK             NodeMask;
  CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE        pRootSignature;
  CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT          InputLayout;
  CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE    IBStripCutValue;
  CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY    PrimitiveTopologyType;
  CD3DX12_PIPELINE_STATE_STREAM_VS                    VS;
  CD3DX12_PIPELINE_STATE_STREAM_GS                    GS;
  CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT         StreamOutput;
  CD3DX12_PIPELINE_STATE_STREAM_HS                    HS;
  CD3DX12_PIPELINE_STATE_STREAM_DS                    DS;
  CD3DX12_PIPELINE_STATE_STREAM_PS                    PS;
  CD3DX12_PIPELINE_STATE_STREAM_CS                    CS;
  CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC            BlendState;
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1        DepthStencilState;
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT  DSVFormat;
  CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER            RasterizerState;
  CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS RTVFormats;
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC           SampleDesc;
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK           SampleMask;
  CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO            CachedPSO;
};
```



## <a name="members"></a><span data-ttu-id="defb6-112">Membres</span><span class="sxs-lookup"><span data-stu-id="defb6-112">Members</span></span>

<dl> <dt>

<span data-ttu-id="defb6-113">**\_Flux d’État du pipeline CD3DX12 \_ \_ ()**</span><span class="sxs-lookup"><span data-stu-id="defb6-113">**CD3DX12\_PIPELINE\_STATE\_STREAM()**</span></span>
</dt> <dd>

<span data-ttu-id="defb6-114">Crée une nouvelle instance non initialisée d’un \_ flux d’état de pipeline CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="defb6-114">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM.</span></span>

</dd> <dt>

<span data-ttu-id="defb6-115">**\_Flux d’État du pipeline CD3DX12 \_ \_ (const D3D12 \_ Graphics \_ pipeline \_ State \_ desc& DESC)**</span><span class="sxs-lookup"><span data-stu-id="defb6-115">**CD3DX12\_PIPELINE\_STATE\_STREAM(const D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC& Desc)**</span></span>
</dt> <dd>

<span data-ttu-id="defb6-116">Crée une nouvelle instance d’un \_ flux d’état de pipeline CD3DX12 \_ \_ , initialisée avec les valeurs copiées à partir d’une structure de flux d' **\_ \_ état \_ de pipeline CD3DX12** .</span><span class="sxs-lookup"><span data-stu-id="defb6-116">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM, initialized with values copied from a **CD3DX12\_PIPELINE\_STATE\_STREAM** structure.</span></span>

</dd> <dt>

<span data-ttu-id="defb6-117">**\_Flux d’État du pipeline CD3DX12 \_ \_ (const D3D12 \_ Compute \_ pipeline \_ State \_ desc& DESC)**</span><span class="sxs-lookup"><span data-stu-id="defb6-117">**CD3DX12\_PIPELINE\_STATE\_STREAM(const D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC& Desc)**</span></span>
</dt> <dd>

<span data-ttu-id="defb6-118">Crée une nouvelle instance d’un \_ flux d’état de pipeline CD3DX12 \_ \_ , initialisée avec les valeurs copiées à partir d’une structure de flux d' **\_ \_ état \_ de pipeline CD3DX12** .</span><span class="sxs-lookup"><span data-stu-id="defb6-118">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM, initialized with values copied from a **CD3DX12\_PIPELINE\_STATE\_STREAM** structure.</span></span>

</dd> <dt>

<span data-ttu-id="defb6-119">**GraphicsDescV0()**</span><span class="sxs-lookup"><span data-stu-id="defb6-119">**GraphicsDescV0()**</span></span>
</dt> <dd>

<span data-ttu-id="defb6-120">retourne le contenu de l' \_ objet de flux d’état de pipeline CD3DX12 \_ \_ en tant que \_ structure DESC d’état de pipeline D3D12 Graphics \_ \_ \_ par valeur.</span><span class="sxs-lookup"><span data-stu-id="defb6-120">returns the contents of the CD3DX12\_PIPELINE\_STATE\_STREAM object as a D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC structure by value.</span></span> <span data-ttu-id="defb6-121">Notez que la \_ \_ Description de l’état du pipeline Graphics D3D12 \_ \_ n’inclut pas le membre **CS** , donc cette valeur est perdue lors de la conversion.</span><span class="sxs-lookup"><span data-stu-id="defb6-121">Note that D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC does not include the **CS** member, so this value is lost in the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="defb6-122">**ComputeDescV0()**</span><span class="sxs-lookup"><span data-stu-id="defb6-122">**ComputeDescV0()**</span></span>
</dt> <dd>

<span data-ttu-id="defb6-123">retourne le contenu de l' \_ objet de flux d’État du pipeline CD3DX12 \_ \_ en tant que \_ structure DESC de l’état du pipeline de calcul D3D12 \_ \_ \_ par valeur.</span><span class="sxs-lookup"><span data-stu-id="defb6-123">returns the contents of the CD3DX12\_PIPELINE\_STATE\_STREAM object as a D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC structure by value.</span></span> <span data-ttu-id="defb6-124">Notez que la \_ Description de \_ l’état du pipeline de calcul D3D12 \_ \_ n’inclut pas les membres **InputLayout**, **IBStripCutValue**, **PrimitiveTopologyType**, **vs**, **GS**, **StreamOutput**, **HS**, **DS**, **PS**, **BlendState**, **DepthStencilState**, **DSVFormat**, **RasterizerState**, **NumRootSignature**, **RTVFormats**, **SampleDesc** ou **SampleMask** . par conséquent, ces valeurs sont perdues lors de la conversion.</span><span class="sxs-lookup"><span data-stu-id="defb6-124">Note that D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC does not include the **InputLayout**, **IBStripCutValue**, **PrimitiveTopologyType**, **VS**, **GS**, **StreamOutput**, **HS**, **DS**, **PS**, **BlendState**, **DepthStencilState**, **DSVFormat**, **RasterizerState**, **NumRootSignature**, **RTVFormats**, **SampleDesc**, or **SampleMask** members, so these values are lost in the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="defb6-125">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="defb6-125">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="defb6-126">Décrit les indicateurs d’État du pipeline, qui contrôlent les fonctionnalités telles que « outil de débogage ».</span><span class="sxs-lookup"><span data-stu-id="defb6-126">Describes the pipeline state flags, which control features such as "tool debug".</span></span>

</dd> <dt>

<span data-ttu-id="defb6-127">**NodeMask**</span><span class="sxs-lookup"><span data-stu-id="defb6-127">**NodeMask**</span></span>
</dt> <dd>

<span data-ttu-id="defb6-128">Décrit le masque de nœud d’état de pipeline, qui est utilisé pour identifier les nœuds (adaptateurs physiques du périphérique) auxquels le PSO s’applique dans les scénarios à plusieurs adaptateurs ; chaque bit du masque correspond à un nœud unique.</span><span class="sxs-lookup"><span data-stu-id="defb6-128">Describes the pipeline state node mask, which is used to identify the nodes (physical adapters of the device) that the PSO applies to in Multi-Adapter scenarios; each bit in the mask corresponds to a single node.</span></span> <span data-ttu-id="defb6-129">Pour les scénarios à un seul adaptateur, définissez cette valeur sur 0.</span><span class="sxs-lookup"><span data-stu-id="defb6-129">For single-adapter scenarios, set this value to 0.</span></span>

</dd> <dt>

<span data-ttu-id="defb6-130">**pRootSignature**</span><span class="sxs-lookup"><span data-stu-id="defb6-130">**pRootSignature**</span></span>
</dt> <dd>

<span data-ttu-id="defb6-131">Décrit la signature racine.</span><span class="sxs-lookup"><span data-stu-id="defb6-131">Describes the root signature.</span></span>

</dd> <dt>

<span data-ttu-id="defb6-132">**InputLayout**</span><span class="sxs-lookup"><span data-stu-id="defb6-132">**InputLayout**</span></span>
</dt> <dd>

<span data-ttu-id="defb6-133">Décrit le format de mémoire tampon d’entrée pour l’étape assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="defb6-133">Describes the input-buffer format for the input-assembler stage</span></span>

</dd> <dt>

<span data-ttu-id="defb6-134">**IBStripCutValue**</span><span class="sxs-lookup"><span data-stu-id="defb6-134">**IBStripCutValue**</span></span>
</dt> <dd>

<span data-ttu-id="defb6-135">Décrit la valeur d’index spéciale de la mémoire tampon d’entrée qui indique une coupure (discontinuation) lors de l’utilisation de la topologie de la bande triangulaire.</span><span class="sxs-lookup"><span data-stu-id="defb6-135">Describes the special index value of the input buffer that indicates a cut (discontinuity) when using triangle-strip topology.</span></span>

</dd> <dt>

<span data-ttu-id="defb6-136">**PrimitiveTopologyType**</span><span class="sxs-lookup"><span data-stu-id="defb6-136">**PrimitiveTopologyType**</span></span>
</dt> <dd>

<span data-ttu-id="defb6-137">Décrit la topologie primitive et son ordre.</span><span class="sxs-lookup"><span data-stu-id="defb6-137">Describes the primitive topology and its order.</span></span>

</dd> <dt>

<span data-ttu-id="defb6-138">**COMPARATIF**</span><span class="sxs-lookup"><span data-stu-id="defb6-138">**VS**</span></span>
</dt> <dd>

<span data-ttu-id="defb6-139">Décrit le nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="defb6-139">Describes the vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="defb6-140">**GS**</span><span class="sxs-lookup"><span data-stu-id="defb6-140">**GS**</span></span>
</dt> <dd>

<span data-ttu-id="defb6-141">Décrit le nuanceur Geometry.</span><span class="sxs-lookup"><span data-stu-id="defb6-141">Describes the geometry shader.</span></span>

</dd> <dt>

<span data-ttu-id="defb6-142">**StreamOutput**</span><span class="sxs-lookup"><span data-stu-id="defb6-142">**StreamOutput**</span></span>
</dt> <dd>

<span data-ttu-id="defb6-143">Décrit la mémoire tampon de sortie de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="defb6-143">Describes the streaming output-buffer.</span></span>

</dd> <dt>

<span data-ttu-id="defb6-144">**SH**</span><span class="sxs-lookup"><span data-stu-id="defb6-144">**HS**</span></span>
</dt> <dd>

<span data-ttu-id="defb6-145">Décrit le nuanceur de coque.</span><span class="sxs-lookup"><span data-stu-id="defb6-145">Describes the hull shader.</span></span>

</dd> <dt>

<span data-ttu-id="defb6-146">**Source de données**</span><span class="sxs-lookup"><span data-stu-id="defb6-146">**DS**</span></span>
</dt> <dd>

<span data-ttu-id="defb6-147">Décrit le nuanceur de domaine.</span><span class="sxs-lookup"><span data-stu-id="defb6-147">Describes the domain shader.</span></span>

</dd> <dt>

<span data-ttu-id="defb6-148">**PS**</span><span class="sxs-lookup"><span data-stu-id="defb6-148">**PS**</span></span>
</dt> <dd>

<span data-ttu-id="defb6-149">Décrit le nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="defb6-149">Describes the pixel shader.</span></span>

</dd> <dt>

<span data-ttu-id="defb6-150">**CS**</span><span class="sxs-lookup"><span data-stu-id="defb6-150">**CS**</span></span>
</dt> <dd>

<span data-ttu-id="defb6-151">Décrit le nuanceur de calcul.</span><span class="sxs-lookup"><span data-stu-id="defb6-151">Describes the compute shader.</span></span>

</dd> <dt>

<span data-ttu-id="defb6-152">**BlendState**</span><span class="sxs-lookup"><span data-stu-id="defb6-152">**BlendState**</span></span>
</dt> <dd>

<span data-ttu-id="defb6-153">Décrit l’état de fusion.</span><span class="sxs-lookup"><span data-stu-id="defb6-153">Describes the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="defb6-154">**DepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="defb6-154">**DepthStencilState**</span></span>
</dt> <dd>

<span data-ttu-id="defb6-155">Décrit l’état du gabarit de profondeur.</span><span class="sxs-lookup"><span data-stu-id="defb6-155">Describes the depth-stencil state.</span></span>

</dd> <dt>

<span data-ttu-id="defb6-156">**DSVFormat**</span><span class="sxs-lookup"><span data-stu-id="defb6-156">**DSVFormat**</span></span>
</dt> <dd>

<span data-ttu-id="defb6-157">Décrit le format de stencil de profondeur.</span><span class="sxs-lookup"><span data-stu-id="defb6-157">Describes the depth-stencil format.</span></span>

</dd> <dt>

<span data-ttu-id="defb6-158">**RasterizerState**</span><span class="sxs-lookup"><span data-stu-id="defb6-158">**RasterizerState**</span></span>
</dt> <dd>

<span data-ttu-id="defb6-159">Décrit l’état du rastériseur.</span><span class="sxs-lookup"><span data-stu-id="defb6-159">Describes the rasterizer state.</span></span>

</dd> <dt>

<span data-ttu-id="defb6-160">**RTVFormats**</span><span class="sxs-lookup"><span data-stu-id="defb6-160">**RTVFormats**</span></span>
</dt> <dd>

<span data-ttu-id="defb6-161">Décrit les formats de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="defb6-161">Describes the render target formats.</span></span>

</dd> <dt>

<span data-ttu-id="defb6-162">**SampleDesc**</span><span class="sxs-lookup"><span data-stu-id="defb6-162">**SampleDesc**</span></span>
</dt> <dd>

<span data-ttu-id="defb6-163">Décrit le nombre d’échantillons et la qualité.</span><span class="sxs-lookup"><span data-stu-id="defb6-163">Describes the sample count and quality.</span></span>

</dd> <dt>

<span data-ttu-id="defb6-164">**SampleMask**</span><span class="sxs-lookup"><span data-stu-id="defb6-164">**SampleMask**</span></span>
</dt> <dd>

<span data-ttu-id="defb6-165">Décrit l’exemple de masque utilisé avec l’état de fusion.</span><span class="sxs-lookup"><span data-stu-id="defb6-165">Describes the sample mask used with the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="defb6-166">**CachedPSO**</span><span class="sxs-lookup"><span data-stu-id="defb6-166">**CachedPSO**</span></span>
</dt> <dd>

<span data-ttu-id="defb6-167">Décrit un PSO mis en cache.</span><span class="sxs-lookup"><span data-stu-id="defb6-167">Describes a cached PSO.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="defb6-168">Notes</span><span class="sxs-lookup"><span data-stu-id="defb6-168">Remarks</span></span>

<span data-ttu-id="defb6-169">Le \_ flux d’État du pipeline CD3DX12 \_ \_ prend en charge Windows 10 Creators Update et versions ultérieures, mais ne prend pas en charge les types de sous-objets ajoutés à la mise à jour de Windows 10 automne, comme pour l’instanciation de vues.</span><span class="sxs-lookup"><span data-stu-id="defb6-169">CD3DX12\_PIPELINE\_STATE\_STREAM supports Windows 10 Creators Update and newer, but doesn not support subobject types added in Windows 10 Fall Creators update, such as for view instancing.</span></span> <span data-ttu-id="defb6-170">Pour prendre en charge les types de sous-objets ajoutés à la mise à jour des créateurs de automne, utilisez à la place [**CD3DX12 \_ pipeline \_ State \_ STREAM1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) .</span><span class="sxs-lookup"><span data-stu-id="defb6-170">To support subobject types added in the Fall Creators update, use [**CD3DX12\_PIPELINE\_STATE\_STREAM1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) instead.</span></span>

<span data-ttu-id="defb6-171">Les variables membres accessibles de cette structure sont tous les typedefs du \_ modèle de sous-objet de flux d’État du pipeline CD3DX12 \_ \_ \_ , qui combine le marqueur de type de sous-objet et les données de sous-objet dans un objet unique approprié pour une description de flux.</span><span class="sxs-lookup"><span data-stu-id="defb6-171">The accessible member variables of this structure are all typedefs of the CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT template, which combines the subobject type-marker and subobject data into a single object suitable for a stream description.</span></span>

<span data-ttu-id="defb6-172">Ces typedefs sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="defb6-172">Those typedefs are:</span></span>

<span data-ttu-id="defb6-173"><dl> </dl></span><span class="sxs-lookup"><span data-stu-id="defb6-173"><dl> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="defb6-174">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="defb6-174">Requirements</span></span>



| <span data-ttu-id="defb6-175">Condition requise</span><span class="sxs-lookup"><span data-stu-id="defb6-175">Requirement</span></span> | <span data-ttu-id="defb6-176">Valeur</span><span class="sxs-lookup"><span data-stu-id="defb6-176">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="defb6-177">En-tête</span><span class="sxs-lookup"><span data-stu-id="defb6-177">Header</span></span><br/> | <dl> <span data-ttu-id="defb6-178"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="defb6-178"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="defb6-179">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="defb6-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="defb6-180">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="defb6-180">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="defb6-181">**\_État du pipeline CD3DX12 \_ \_ STREAM1**</span><span class="sxs-lookup"><span data-stu-id="defb6-181">**CD3DX12\_PIPELINE\_STATE\_STREAM1**</span></span>](cd3dx12-pipeline-state-stream1.md)
</dt> <dt>

[<span data-ttu-id="defb6-182">**Description de l' \_ \_ État du pipeline GRAPHICs D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="defb6-182">**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)
</dt> <dt>

[<span data-ttu-id="defb6-183">**\_Description de l' \_ État du pipeline de calcul D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="defb6-183">**D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)
</dt> </dl>

 

 





