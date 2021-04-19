---
title: Structure CD3DX12_PIPELINE_STATE_STREAM1 (D3dx12. h)
description: Structure d’assistance pour la création et l’utilisation des graphiques et des États de pipeline de calcul via une interface combinée. Consultez D3D12 \_ Graphics \_ pipeline \_ State \_ DESC et D3D12 \_ Compute \_ pipeline \_ State \_ desc. | Structure CD3DX12_PIPELINE_STATE_STREAM1 (D3dx12. h)
ms.assetid: 4D3E4D99-E820-4220-92F3-4924791E780F
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM1
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdd04f58f4f123850c60b67ff9358f6f1f934373
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525857"
---
# <a name="cd3dx12_pipeline_state_stream1-structure"></a><span data-ttu-id="fb586-106">\_Structure STREAM1 de l’état du pipeline CD3DX12 \_ \_</span><span class="sxs-lookup"><span data-stu-id="fb586-106">CD3DX12\_PIPELINE\_STATE\_STREAM1 structure</span></span>

<span data-ttu-id="fb586-107">Structure d’assistance pour la création et l’utilisation des graphiques et des États de pipeline de calcul via une interface combinée.</span><span class="sxs-lookup"><span data-stu-id="fb586-107">A helper structure for creating and working with graphics and compute pipeline states through a combined interface.</span></span> <span data-ttu-id="fb586-108">Consultez [**D3D12 \_ Graphics \_ pipeline \_ State \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) et [**D3D12 \_ Compute \_ pipeline \_ State \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).</span><span class="sxs-lookup"><span data-stu-id="fb586-108">See [**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) and [**D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).</span></span>

<span data-ttu-id="fb586-109">\_ \_ L’état du pipeline CD3DX12 \_ STREAM1 prend en charge la mise à jour des créateurs de automne Windows 10 avec de nouvelles fonctionnalités telles que l’instanciation de vues.</span><span class="sxs-lookup"><span data-stu-id="fb586-109">CD3DX12\_PIPELINE\_STATE\_STREAM1 supports the Windows 10 Fall Creators Update with new features such as view instancing.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb586-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb586-110">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM1 {
  CD3DX12_PIPELINE_STATE_STREAM1                      CD3DX12_PIPELINE_STATE_STREAM1();
  CD3DX12_PIPELINE_STATE_STREAM1                      CD3DX12_PIPELINE_STATE_STREAM1(const D3D12_GRAPHICS_PIPELINE_STATE_DESC& Desc);
  CD3DX12_PIPELINE_STATE_STREAM1                      CD3DX12_PIPELINE_STATE_STREAM1(const D3D12_COMPUTE_PIPELINE_STATE_DESC& Desc);
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



## <a name="members"></a><span data-ttu-id="fb586-111">Membres</span><span class="sxs-lookup"><span data-stu-id="fb586-111">Members</span></span>

<dl> <dt>

<span data-ttu-id="fb586-112">**\_État du pipeline CD3DX12 \_ \_ STREAM1 ()**</span><span class="sxs-lookup"><span data-stu-id="fb586-112">**CD3DX12\_PIPELINE\_STATE\_STREAM1()**</span></span>
</dt> <dd>

<span data-ttu-id="fb586-113">Crée une nouvelle instance non initialisée d’un \_ État de pipeline \_ CD3DX12 \_ STREAM1.</span><span class="sxs-lookup"><span data-stu-id="fb586-113">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM1.</span></span>

</dd> <dt>

<span data-ttu-id="fb586-114">**\_État du pipeline CD3DX12 \_ \_ STREAM1 (const D3D12 \_ Graphics \_ pipeline \_ State \_ desc& DESC)**</span><span class="sxs-lookup"><span data-stu-id="fb586-114">**CD3DX12\_PIPELINE\_STATE\_STREAM1(const D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC& Desc)**</span></span>
</dt> <dd>

<span data-ttu-id="fb586-115">Crée une nouvelle instance d’un \_ État de pipeline CD3DX12 \_ \_ STREAM1, initialisée avec les valeurs copiées à partir d’une structure STREAM1 d' **\_ \_ état \_ de pipeline CD3DX12** .</span><span class="sxs-lookup"><span data-stu-id="fb586-115">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM1, initialized with values copied from a **CD3DX12\_PIPELINE\_STATE\_STREAM1** structure.</span></span>

</dd> <dt>

<span data-ttu-id="fb586-116">**\_État du pipeline CD3DX12 \_ \_ STREAM1 (const D3D12 calcul de l' \_ état du \_ pipeline \_ \_& DESC)**</span><span class="sxs-lookup"><span data-stu-id="fb586-116">**CD3DX12\_PIPELINE\_STATE\_STREAM1(const D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC& Desc)**</span></span>
</dt> <dd>

<span data-ttu-id="fb586-117">Crée une nouvelle instance d’un \_ État de pipeline CD3DX12 \_ \_ STREAM1, initialisée avec les valeurs copiées à partir d’une structure STREAM1 d' **\_ \_ état \_ de pipeline CD3DX12** .</span><span class="sxs-lookup"><span data-stu-id="fb586-117">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM1, initialized with values copied from a **CD3DX12\_PIPELINE\_STATE\_STREAM1** structure.</span></span>

</dd> <dt>

<span data-ttu-id="fb586-118">**GraphicsDescV0()**</span><span class="sxs-lookup"><span data-stu-id="fb586-118">**GraphicsDescV0()**</span></span>
</dt> <dd>

<span data-ttu-id="fb586-119">retourne le contenu de l' \_ objet STREAM1 de l’état du pipeline CD3DX12 \_ \_ en tant que \_ structure DESC de l’état du \_ pipeline D3D12 \_ \_ par valeur.</span><span class="sxs-lookup"><span data-stu-id="fb586-119">returns the contents of the CD3DX12\_PIPELINE\_STATE\_STREAM1 object as a D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC structure by value.</span></span> <span data-ttu-id="fb586-120">Notez que la \_ \_ Description de l’état du pipeline Graphics D3D12 \_ \_ n’inclut pas le membre **CS** , donc cette valeur est perdue lors de la conversion.</span><span class="sxs-lookup"><span data-stu-id="fb586-120">Note that D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC does not include the **CS** member, so this value is lost in the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="fb586-121">**ComputeDescV0()**</span><span class="sxs-lookup"><span data-stu-id="fb586-121">**ComputeDescV0()**</span></span>
</dt> <dd>

<span data-ttu-id="fb586-122">retourne le contenu de l' \_ objet STREAM1 de l’état du pipeline CD3DX12 \_ \_ en tant que \_ structure DESC de l’état du pipeline de calcul D3D12 \_ \_ \_ par valeur.</span><span class="sxs-lookup"><span data-stu-id="fb586-122">returns the contents of the CD3DX12\_PIPELINE\_STATE\_STREAM1 object as a D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC structure by value.</span></span> <span data-ttu-id="fb586-123">Notez que la \_ Description de \_ l’état du pipeline de calcul D3D12 \_ \_ n’inclut pas les membres **InputLayout**, **IBStripCutValue**, **PrimitiveTopologyType**, **vs**, **GS**, **StreamOutput**, **HS**, **DS**, **PS**, **BlendState**, **DepthStencilState**, **DSVFormat**, **RasterizerState**, **NumRootSignature**, **RTVFormats**, **SampleDesc** ou **SampleMask** . par conséquent, ces valeurs sont perdues lors de la conversion.</span><span class="sxs-lookup"><span data-stu-id="fb586-123">Note that D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC does not include the **InputLayout**, **IBStripCutValue**, **PrimitiveTopologyType**, **VS**, **GS**, **StreamOutput**, **HS**, **DS**, **PS**, **BlendState**, **DepthStencilState**, **DSVFormat**, **RasterizerState**, **NumRootSignature**, **RTVFormats**, **SampleDesc**, or **SampleMask** members, so these values are lost in the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="fb586-124">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="fb586-124">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="fb586-125">Décrit les indicateurs d’État du pipeline, qui contrôlent les fonctionnalités telles que « outil de débogage ».</span><span class="sxs-lookup"><span data-stu-id="fb586-125">Describes the pipeline state flags, which control features such as "tool debug".</span></span>

</dd> <dt>

<span data-ttu-id="fb586-126">**NodeMask**</span><span class="sxs-lookup"><span data-stu-id="fb586-126">**NodeMask**</span></span>
</dt> <dd>

<span data-ttu-id="fb586-127">Décrit le masque de nœud d’état de pipeline, qui est utilisé pour identifier les nœuds (adaptateurs physiques du périphérique) auxquels le PSO s’applique dans les scénarios à plusieurs adaptateurs ; chaque bit du masque correspond à un nœud unique.</span><span class="sxs-lookup"><span data-stu-id="fb586-127">Describes the pipeline state node mask, which is used to identify the nodes (physical adapters of the device) that the PSO applies to in Multi-Adapter scenarios; each bit in the mask corresponds to a single node.</span></span> <span data-ttu-id="fb586-128">Pour les scénarios à un seul adaptateur, définissez cette valeur sur 0.</span><span class="sxs-lookup"><span data-stu-id="fb586-128">For single-adapter scenarios, set this value to 0.</span></span>

</dd> <dt>

<span data-ttu-id="fb586-129">**pRootSignature**</span><span class="sxs-lookup"><span data-stu-id="fb586-129">**pRootSignature**</span></span>
</dt> <dd>

<span data-ttu-id="fb586-130">Décrit la signature racine.</span><span class="sxs-lookup"><span data-stu-id="fb586-130">Describes the root signature.</span></span>

</dd> <dt>

<span data-ttu-id="fb586-131">**InputLayout**</span><span class="sxs-lookup"><span data-stu-id="fb586-131">**InputLayout**</span></span>
</dt> <dd>

<span data-ttu-id="fb586-132">Décrit le format de mémoire tampon d’entrée pour l’étape assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fb586-132">Describes the input-buffer format for the input-assembler stage</span></span>

</dd> <dt>

<span data-ttu-id="fb586-133">**IBStripCutValue**</span><span class="sxs-lookup"><span data-stu-id="fb586-133">**IBStripCutValue**</span></span>
</dt> <dd>

<span data-ttu-id="fb586-134">Décrit la valeur d’index spéciale de la mémoire tampon d’entrée qui indique une coupure (discontinuation) lors de l’utilisation de la topologie de la bande triangulaire.</span><span class="sxs-lookup"><span data-stu-id="fb586-134">Describes the special index value of the input buffer that indicates a cut (discontinuity) when using triangle-strip topology.</span></span>

</dd> <dt>

<span data-ttu-id="fb586-135">**PrimitiveTopologyType**</span><span class="sxs-lookup"><span data-stu-id="fb586-135">**PrimitiveTopologyType**</span></span>
</dt> <dd>

<span data-ttu-id="fb586-136">Décrit la topologie primitive et son ordre.</span><span class="sxs-lookup"><span data-stu-id="fb586-136">Describes the primitive topology and its order.</span></span>

</dd> <dt>

<span data-ttu-id="fb586-137">**COMPARATIF**</span><span class="sxs-lookup"><span data-stu-id="fb586-137">**VS**</span></span>
</dt> <dd>

<span data-ttu-id="fb586-138">Décrit le nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="fb586-138">Describes the vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="fb586-139">**GS**</span><span class="sxs-lookup"><span data-stu-id="fb586-139">**GS**</span></span>
</dt> <dd>

<span data-ttu-id="fb586-140">Décrit le nuanceur Geometry.</span><span class="sxs-lookup"><span data-stu-id="fb586-140">Describes the geometry shader.</span></span>

</dd> <dt>

<span data-ttu-id="fb586-141">**StreamOutput**</span><span class="sxs-lookup"><span data-stu-id="fb586-141">**StreamOutput**</span></span>
</dt> <dd>

<span data-ttu-id="fb586-142">Décrit la mémoire tampon de sortie de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="fb586-142">Describes the streaming output-buffer.</span></span>

</dd> <dt>

<span data-ttu-id="fb586-143">**SH**</span><span class="sxs-lookup"><span data-stu-id="fb586-143">**HS**</span></span>
</dt> <dd>

<span data-ttu-id="fb586-144">Décrit le nuanceur de coque.</span><span class="sxs-lookup"><span data-stu-id="fb586-144">Describes the hull shader.</span></span>

</dd> <dt>

<span data-ttu-id="fb586-145">**Source de données**</span><span class="sxs-lookup"><span data-stu-id="fb586-145">**DS**</span></span>
</dt> <dd>

<span data-ttu-id="fb586-146">Décrit le nuanceur de domaine.</span><span class="sxs-lookup"><span data-stu-id="fb586-146">Describes the domain shader.</span></span>

</dd> <dt>

<span data-ttu-id="fb586-147">**PS**</span><span class="sxs-lookup"><span data-stu-id="fb586-147">**PS**</span></span>
</dt> <dd>

<span data-ttu-id="fb586-148">Décrit le nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="fb586-148">Describes the pixel shader.</span></span>

</dd> <dt>

<span data-ttu-id="fb586-149">**CS**</span><span class="sxs-lookup"><span data-stu-id="fb586-149">**CS**</span></span>
</dt> <dd>

<span data-ttu-id="fb586-150">Décrit le nuanceur de calcul.</span><span class="sxs-lookup"><span data-stu-id="fb586-150">Describes the compute shader.</span></span>

</dd> <dt>

<span data-ttu-id="fb586-151">**BlendState**</span><span class="sxs-lookup"><span data-stu-id="fb586-151">**BlendState**</span></span>
</dt> <dd>

<span data-ttu-id="fb586-152">Décrit l’état de fusion.</span><span class="sxs-lookup"><span data-stu-id="fb586-152">Describes the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="fb586-153">**DepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="fb586-153">**DepthStencilState**</span></span>
</dt> <dd>

<span data-ttu-id="fb586-154">Décrit l’état du gabarit de profondeur.</span><span class="sxs-lookup"><span data-stu-id="fb586-154">Describes the depth-stencil state.</span></span>

</dd> <dt>

<span data-ttu-id="fb586-155">**DSVFormat**</span><span class="sxs-lookup"><span data-stu-id="fb586-155">**DSVFormat**</span></span>
</dt> <dd>

<span data-ttu-id="fb586-156">Décrit le format de stencil de profondeur.</span><span class="sxs-lookup"><span data-stu-id="fb586-156">Describes the depth-stencil format.</span></span>

</dd> <dt>

<span data-ttu-id="fb586-157">**RasterizerState**</span><span class="sxs-lookup"><span data-stu-id="fb586-157">**RasterizerState**</span></span>
</dt> <dd>

<span data-ttu-id="fb586-158">Décrit l’état du rastériseur.</span><span class="sxs-lookup"><span data-stu-id="fb586-158">Describes the rasterizer state.</span></span>

</dd> <dt>

<span data-ttu-id="fb586-159">**RTVFormats**</span><span class="sxs-lookup"><span data-stu-id="fb586-159">**RTVFormats**</span></span>
</dt> <dd>

<span data-ttu-id="fb586-160">Décrit les formats de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="fb586-160">Describes the render target formats.</span></span>

</dd> <dt>

<span data-ttu-id="fb586-161">**SampleDesc**</span><span class="sxs-lookup"><span data-stu-id="fb586-161">**SampleDesc**</span></span>
</dt> <dd>

<span data-ttu-id="fb586-162">Décrit le nombre d’échantillons et la qualité.</span><span class="sxs-lookup"><span data-stu-id="fb586-162">Describes the sample count and quality.</span></span>

</dd> <dt>

<span data-ttu-id="fb586-163">**SampleMask**</span><span class="sxs-lookup"><span data-stu-id="fb586-163">**SampleMask**</span></span>
</dt> <dd>

<span data-ttu-id="fb586-164">Décrit l’exemple de masque utilisé avec l’état de fusion.</span><span class="sxs-lookup"><span data-stu-id="fb586-164">Describes the sample mask used with the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="fb586-165">**CachedPSO**</span><span class="sxs-lookup"><span data-stu-id="fb586-165">**CachedPSO**</span></span>
</dt> <dd>

<span data-ttu-id="fb586-166">Décrit un PSO mis en cache.</span><span class="sxs-lookup"><span data-stu-id="fb586-166">Describes a cached PSO.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fb586-167">Notes</span><span class="sxs-lookup"><span data-stu-id="fb586-167">Remarks</span></span>

<span data-ttu-id="fb586-168">[**CD3DX12 \_ Le \_ \_ flux de l’état du pipeline**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM**) prend en charge la mise à jour des créateurs de automne Windows 10, mais ne prend pas en charge les types de sous-objets ajoutés à la mise à jour des créateurs de Windows 10</span><span class="sxs-lookup"><span data-stu-id="fb586-168">[**CD3DX12\_PIPELINE\_STATE\_STREAM**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM**) supports the Windows 10 Fall Creators Update, but doesn't support subobject types added in Windows 10 Fall Creators update, such as for view instancing.</span></span> <span data-ttu-id="fb586-169">Pour prendre en charge les nouveaux types de sous-objet, utilisez à la \_ place l’état du pipeline CD3DX12 \_ \_ STREAM1.</span><span class="sxs-lookup"><span data-stu-id="fb586-169">To support the new subobject types, use CD3DX12\_PIPELINE\_STATE\_STREAM1 instead.</span></span>

<span data-ttu-id="fb586-170">Les variables membres accessibles de cette structure sont tous les typedefs du \_ modèle de sous-objet de flux d’État du pipeline CD3DX12 \_ \_ \_ , qui combine le marqueur de type de sous-objet et les données de sous-objet dans un objet unique approprié pour une description de flux.</span><span class="sxs-lookup"><span data-stu-id="fb586-170">The accessible member variables of this structure are all typedefs of the CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT template, which combines the subobject type-marker and subobject data into a single object suitable for a stream description.</span></span>

<span data-ttu-id="fb586-171">Ces typedefs sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="fb586-171">Those typedefs are:</span></span>

<span data-ttu-id="fb586-172"><dl> </dl></span><span class="sxs-lookup"><span data-stu-id="fb586-172"><dl> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="fb586-173">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb586-173">Requirements</span></span>



| <span data-ttu-id="fb586-174">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fb586-174">Requirement</span></span> | <span data-ttu-id="fb586-175">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb586-175">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fb586-176">En-tête</span><span class="sxs-lookup"><span data-stu-id="fb586-176">Header</span></span><br/> | <dl> <span data-ttu-id="fb586-177"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb586-177"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb586-178">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb586-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb586-179">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="fb586-179">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="fb586-180">**\_Flux d’État du pipeline CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fb586-180">**CD3DX12\_PIPELINE\_STATE\_STREAM**</span></span>](cd3dx12-pipeline-state-stream.md)
</dt> <dt>

[<span data-ttu-id="fb586-181">**Description de l' \_ \_ État du pipeline GRAPHICs D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fb586-181">**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)
</dt> <dt>

[<span data-ttu-id="fb586-182">**\_Description de l' \_ État du pipeline de calcul D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fb586-182">**D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)
</dt> </dl>

 

 





