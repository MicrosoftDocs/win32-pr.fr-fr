---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER (D3dx12. h)
description: Génère un \_ \_ \_ objet de flux d’état de pipeline CD3DX12 interne à partir des détails de sous-objet passés dans les fonctions membres correspondantes. Ce struct implémente l’interface ID3DX12PipelineParserCallbacks.
ms.assetid: 7D4FFD1D-9FA3-4482-A67B-E742611030BC
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44cc6228f690abd677e1adc8552293e440452ec5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106529595"
---
# <a name="cd3dx12_pipeline_state_stream_parse_helper-structure"></a><span data-ttu-id="c0c53-105">\_ \_ \_ \_ \_ Structure d’assistance d’analyse du flux d’État du pipeline CD3DX12</span><span class="sxs-lookup"><span data-stu-id="c0c53-105">CD3DX12\_PIPELINE\_STATE\_STREAM\_PARSE\_HELPER structure</span></span>

<span data-ttu-id="c0c53-106">Génère un \_ \_ \_ objet de flux d’état de pipeline CD3DX12 interne à partir des détails de sous-objet passés dans les fonctions membres correspondantes.</span><span class="sxs-lookup"><span data-stu-id="c0c53-106">Builds an internal CD3DX12\_PIPELINE\_STATE\_STREAM object from subobject details passed into the corresponding member functions.</span></span> <span data-ttu-id="c0c53-107">Ce struct implémente l’interface [**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md) .</span><span class="sxs-lookup"><span data-stu-id="c0c53-107">This struct implements the [**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0c53-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0c53-108">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER  : public ID3DX12PipelineParserCallbacks{
  CD3DX12_PIPELINE_STATE_STREAM1 PipelineStream;
  void                           FlagsCb(D3D12_PIPELINE_STATE_FLAGS Flags);
  void                           NodeMaskCb(UINT NodeMask);
  void                           RootSignatureCb(ID3D12RootSignature* pRootSignature);
  void                           InputLayoutCb(const D3D12_INPUT_LAYOUT_DESC& InputLayout);
  void                           IBStripCutValueCb(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE IBStripCutValue);
  void                           PrimitiveTopologyTypeCb(D3D12_PRIMITIVE_TOPOLOGY_TYPE PrimitiveTopologyType);
  void                           VSCb(const D3D12_SHADER_BYTECODE& VS);
  void                           GSCb(const D3D12_SHADER_BYTECODE& GS);
  void                           StreamOutputCb(const D3D12_STREAM_OUTPUT_DESC& StreamOutput);
  void                           HSCb(const D3D12_SHADER_BYTECODE& HS);
  void                           DSCb(const D3D12_SHADER_BYTECODE& DS);
  void                           PSCb(const D3D12_SHADER_BYTECODE& PS);
  void                           CSCb(const D3D12_SHADER_BYTECODE& CS);
  void                           BlendStateCb(const D3D12_BLEND_DESC& BlendState);
  void                           DepthStencilStateCb(const D3D12_DEPTH_STENCIL_DESC& DepthStencilState);
  void                           DepthStencilState1Cb(const D3D12_DEPTH_STENCIL_DESC1& DepthStencilState);
  void                           DSVFormatCb(DXGI_FORMAT DSVFormat);
  void                           RasterizerStateCb(const D3D12_RASTERIZER_DESC& RasterizerState);
  void                           RTVFormatsCb(const D3D12_RT_FORMAT_ARRAY& RTVFormats);
  void                           SampleDescCb(const DXGI_SAMPLE_DESC& SampleDesc);
  void                           SampleMaskCb(UINT SampleMask);
  void                           ViewInstancingCb(const D3D12_VIEW_INSTANCING_DESC& ViewInstancingDesc);
  void                           CachedPSOCb(const D3D12_CACHED_PIPELINE_STATE& CachedPSO);
  void                           ErrorBadInputParameter(UINT);
  void                           ErrorDuplicateSubobject(D3D12_PIPELINE_STATE_SUBOBJECT_TYPE);
  void                           ErrorUnknownSubobject(UINT);
};
```



## <a name="members"></a><span data-ttu-id="c0c53-109">Membres</span><span class="sxs-lookup"><span data-stu-id="c0c53-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="c0c53-110">**PipelineStream**</span><span class="sxs-lookup"><span data-stu-id="c0c53-110">**PipelineStream**</span></span>
</dt> <dd>

<span data-ttu-id="c0c53-111">L’état interne du [**\_ pipeline CD3DX12 \_ \_ STREAM1**](cd3dx12-pipeline-state-stream1.md).</span><span class="sxs-lookup"><span data-stu-id="c0c53-111">The internal [**CD3DX12\_PIPELINE\_STATE\_STREAM1**](cd3dx12-pipeline-state-stream1.md).</span></span> <span data-ttu-id="c0c53-112">Son état actuel représente l’effet cumulatif des méthodes de rappel qui ont été appelées sur cet objet.</span><span class="sxs-lookup"><span data-stu-id="c0c53-112">Its current state represents the cumulative effect of callback methods that have been called on this object.</span></span>

</dd> <dt>

<span data-ttu-id="c0c53-113">**FlagsCb ( \_ indicateurs d’indicateurs d’état de pipeline D3D12 \_ \_ )**</span><span class="sxs-lookup"><span data-stu-id="c0c53-113">**FlagsCb(D3D12\_PIPELINE\_STATE\_FLAGS Flags)**</span></span>
</dt> <dd>

<span data-ttu-id="c0c53-114">Initialise le membre **Flags** de **PipelineStream** à l’aide de la valeur du paramètre *Flags* .</span><span class="sxs-lookup"><span data-stu-id="c0c53-114">Initializes the **Flags** member of **PipelineStream** using the value of the *Flags* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c0c53-115">**NodeMaskCb (UINT NodeMask)**</span><span class="sxs-lookup"><span data-stu-id="c0c53-115">**NodeMaskCb(UINT NodeMask)**</span></span>
</dt> <dd>

<span data-ttu-id="c0c53-116">Initialise le membre **NodeMask** de **PipelineStream** à l’aide de la valeur du paramètre *NodeMask* .</span><span class="sxs-lookup"><span data-stu-id="c0c53-116">Initializes the **NodeMask** member of **PipelineStream** using the value of the *Nodemask* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c0c53-117">**RootSignatureCb (ID3D12RootSignature \* pRootSignature)**</span><span class="sxs-lookup"><span data-stu-id="c0c53-117">**RootSignatureCb(ID3D12RootSignature\* pRootSignature)**</span></span>
</dt> <dd>

<span data-ttu-id="c0c53-118">Initialise le membre **pRootSignature** de **PipelineStream** à l’aide de la valeur du paramètre *pRootSignature* .</span><span class="sxs-lookup"><span data-stu-id="c0c53-118">Initializes the **pRootSignature** member of **PipelineStream** using the value of the *pRootSignature* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c0c53-119">**InputLayoutCb (const D3D12 \_ disposition d’entrée \_ \_ desc& InputLayout)**</span><span class="sxs-lookup"><span data-stu-id="c0c53-119">**InputLayoutCb(const D3D12\_INPUT\_LAYOUT\_DESC& InputLayout)**</span></span>
</dt> <dd>

<span data-ttu-id="c0c53-120">Initialise le membre **InputLayout** de **PipelineStream** à l’aide de la valeur du paramètre *InputLayout* .</span><span class="sxs-lookup"><span data-stu-id="c0c53-120">Initializes the **InputLayout** member of **PipelineStream** using the value of the *InputLayout* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c0c53-121">**IBStripCutValueCb (valeur de coupe de la bande de la \_ mémoire tampon d’index D3D12 \_ \_ \_ \_ IBStripCutValue)**</span><span class="sxs-lookup"><span data-stu-id="c0c53-121">**IBStripCutValueCb(D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE IBStripCutValue)**</span></span>
</dt> <dd>

<span data-ttu-id="c0c53-122">Initialise le membre **IBStripCutValue** de **PipelineStream** à l’aide de la valeur du paramètre *IBStripCutValue* .</span><span class="sxs-lookup"><span data-stu-id="c0c53-122">Initializes the **IBStripCutValue** member of **PipelineStream** using the value of the *IBStripCutValue* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c0c53-123">**PrimitiveTopologyTypeCb ( \_ type de topologie D3D12 primitif \_ \_ PrimitiveTopologyType)**</span><span class="sxs-lookup"><span data-stu-id="c0c53-123">**PrimitiveTopologyTypeCb(D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE PrimitiveTopologyType)**</span></span>
</dt> <dd>

<span data-ttu-id="c0c53-124">Initialise le membre **PrimitiveTopologyType** de **PipelineStream** à l’aide de la valeur du paramètre *PrimitiveTopologyType* .</span><span class="sxs-lookup"><span data-stu-id="c0c53-124">Initializes the **PrimitiveTopologyType** member of **PipelineStream** using the value of the *PrimitiveTopologyType* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c0c53-125">**VSCb (pseudo-code de nuanceur const D3D12 \_ \_& vs)**</span><span class="sxs-lookup"><span data-stu-id="c0c53-125">**VSCb(const D3D12\_SHADER\_BYTECODE& VS)**</span></span>
</dt> <dd>

<span data-ttu-id="c0c53-126">Initialise le membre **vs** (vertex shader) de **PipelineStream** à l’aide de la valeur du paramètre *vs* .</span><span class="sxs-lookup"><span data-stu-id="c0c53-126">Initializes the **VS** (vertex shader) member of **PipelineStream** using the value of the *VS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c0c53-127">**GSCb (code de nuanceur const D3D12 \_ \_& GS)**</span><span class="sxs-lookup"><span data-stu-id="c0c53-127">**GSCb(const D3D12\_SHADER\_BYTECODE& GS)**</span></span>
</dt> <dd>

<span data-ttu-id="c0c53-128">Initialise le membre **GS** (Geometry Shader) de **PipelineStream** à l’aide de la valeur du paramètre *GS* .</span><span class="sxs-lookup"><span data-stu-id="c0c53-128">Initializes the **GS** (geometry shader) member of **PipelineStream** using the value of the *GS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c0c53-129">**StreamOutputCb (const D3D12 \_ flux de \_ sortie \_ desc& StreamOutput)**</span><span class="sxs-lookup"><span data-stu-id="c0c53-129">**StreamOutputCb(const D3D12\_STREAM\_OUTPUT\_DESC& StreamOutput)**</span></span>
</dt> <dd>

<span data-ttu-id="c0c53-130">Initialise le membre **StreamOutput** de **PipelineStream** à l’aide de la valeur du paramètre *StreamOutput* .</span><span class="sxs-lookup"><span data-stu-id="c0c53-130">Initializes the **StreamOutput** member of **PipelineStream** using the value of the *StreamOutput* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c0c53-131">**HSCb (code de nuanceur const D3D12 \_ \_& HS)**</span><span class="sxs-lookup"><span data-stu-id="c0c53-131">**HSCb(const D3D12\_SHADER\_BYTECODE& HS)**</span></span>
</dt> <dd>

<span data-ttu-id="c0c53-132">Initialise le membre **HS** (coque Shader) de **PipelineStream** à l’aide de la valeur du paramètre *HS* .</span><span class="sxs-lookup"><span data-stu-id="c0c53-132">Initializes the **HS** (hull shader) member of **PipelineStream** using the value of the *HS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c0c53-133">**DSCb (code de nuanceur const D3D12 \_ \_& DS)**</span><span class="sxs-lookup"><span data-stu-id="c0c53-133">**DSCb(const D3D12\_SHADER\_BYTECODE& DS)**</span></span>
</dt> <dd>

<span data-ttu-id="c0c53-134">Initialise le membre **DS** (Domain Shader) de **PipelineStream** à l’aide de la valeur du paramètre *DS* .</span><span class="sxs-lookup"><span data-stu-id="c0c53-134">Initializes the **DS** (domain shader) member of **PipelineStream** using the value of the *DS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c0c53-135">**PSCb (code de nuanceur const D3D12 \_ \_& PS)**</span><span class="sxs-lookup"><span data-stu-id="c0c53-135">**PSCb(const D3D12\_SHADER\_BYTECODE& PS)**</span></span>
</dt> <dd>

<span data-ttu-id="c0c53-136">Initialise le membre **PS** (Pixel Shader) de **PipelineStream** à l’aide de la valeur du paramètre *PS* .</span><span class="sxs-lookup"><span data-stu-id="c0c53-136">Initializes the **PS** (pixel shader) member of **PipelineStream** using the value of the *PS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c0c53-137">**CSCb (code de nuanceur const D3D12 \_ \_& CS)**</span><span class="sxs-lookup"><span data-stu-id="c0c53-137">**CSCb(const D3D12\_SHADER\_BYTECODE& CS)**</span></span>
</dt> <dd>

<span data-ttu-id="c0c53-138">Initialise le membre **CS** de **PipelineStream** à l’aide de la valeur du paramètre *CS* .</span><span class="sxs-lookup"><span data-stu-id="c0c53-138">Initializes the **CS** member of **PipelineStream** using the value of the *CS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c0c53-139">**BlendStateCb (const D3D12 \_ Blend \_ desc& BlendState)**</span><span class="sxs-lookup"><span data-stu-id="c0c53-139">**BlendStateCb(const D3D12\_BLEND\_DESC& BlendState)**</span></span>
</dt> <dd>

<span data-ttu-id="c0c53-140">Initialise le membre **BlendState** de **PipelineStream** à l’aide de la valeur du paramètre *BlendState* .</span><span class="sxs-lookup"><span data-stu-id="c0c53-140">Initializes the **BlendState** member of **PipelineStream** using the value of the *BlendState* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c0c53-141">**DepthStencilStateCb (const D3D12 \_ \_ Description du stencil \_& DepthStencilState)**</span><span class="sxs-lookup"><span data-stu-id="c0c53-141">**DepthStencilStateCb(const D3D12\_DEPTH\_STENCIL\_DESC& DepthStencilState)**</span></span>
</dt> <dd>

<span data-ttu-id="c0c53-142">Initialise le membre **DepthStencilState** de **PipelineStream** à l’aide de la valeur du paramètre *DepthStencilState* , [**une \_ \_ \_ Description du stencil de profondeur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc).</span><span class="sxs-lookup"><span data-stu-id="c0c53-142">Initializes the **DepthStencilState** member of **PipelineStream** using the value of the *DepthStencilState* parameter, a [**D3D12\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc).</span></span>

</dd> <dt>

<span data-ttu-id="c0c53-143">**DepthStencilState1Cb (const D3D12 \_ Depth \_ STENCIL \_ DESC1& DepthStencilState)**</span><span class="sxs-lookup"><span data-stu-id="c0c53-143">**DepthStencilState1Cb(const D3D12\_DEPTH\_STENCIL\_DESC1& DepthStencilState)**</span></span>
</dt> <dd>

<span data-ttu-id="c0c53-144">Initialise le membre **DepthStencilState** de **PipelineStream** à l’aide de la valeur du paramètre *DepthStencilState* , un [**stencil de profondeur D3D12 \_ \_ \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1).</span><span class="sxs-lookup"><span data-stu-id="c0c53-144">Initializes the **DepthStencilState** member of **PipelineStream** using the value of the *DepthStencilState* parameter, a [**D3D12\_DEPTH\_STENCIL\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1).</span></span>

</dd> <dt>

<span data-ttu-id="c0c53-145">**DSVFormatCb (DXGI \_ format DSVFormat)**</span><span class="sxs-lookup"><span data-stu-id="c0c53-145">**DSVFormatCb(DXGI\_FORMAT DSVFormat)**</span></span>
</dt> <dd>

<span data-ttu-id="c0c53-146">Initialise le membre **DSVFormat** de **PipelineStream** à l’aide de la valeur du paramètre *DSVFormat* .</span><span class="sxs-lookup"><span data-stu-id="c0c53-146">Initializes the **DSVFormat** member of **PipelineStream** using the value of the *DSVFormat* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c0c53-147">**RasterizerStateCb (const D3D12 \_ rastériseur \_ desc& RasterizerState)**</span><span class="sxs-lookup"><span data-stu-id="c0c53-147">**RasterizerStateCb(const D3D12\_RASTERIZER\_DESC& RasterizerState)**</span></span>
</dt> <dd>

<span data-ttu-id="c0c53-148">Initialise le membre **RasterizerState** de **PipelineStream** à l’aide de la valeur du paramètre *RasterizerState* .</span><span class="sxs-lookup"><span data-stu-id="c0c53-148">Initializes the **RasterizerState** member of **PipelineStream** using the value of the *RasterizerState* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c0c53-149">**RTVFormatsCb (const D3D12 \_ RT \_ FORMAT \_ tableau& RTVFormats)**</span><span class="sxs-lookup"><span data-stu-id="c0c53-149">**RTVFormatsCb(const D3D12\_RT\_FORMAT\_ARRAY& RTVFormats)**</span></span>
</dt> <dd>

<span data-ttu-id="c0c53-150">Initialise le membre **RTVFormats** de **PipelineStream** à l’aide de la valeur du paramètre *RTVFormats* .</span><span class="sxs-lookup"><span data-stu-id="c0c53-150">Initializes the **RTVFormats** member of **PipelineStream** using the value of the *RTVFormats* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c0c53-151">**SampleDescCb (const DXGI \_ \_ , exemple DESC& SampleDesc)**</span><span class="sxs-lookup"><span data-stu-id="c0c53-151">**SampleDescCb(const DXGI\_SAMPLE\_DESC& SampleDesc)**</span></span>
</dt> <dd>

<span data-ttu-id="c0c53-152">Initialise le membre **SampleDesc** de **PipelineStream** à l’aide de la valeur du paramètre *SampleDesc* .</span><span class="sxs-lookup"><span data-stu-id="c0c53-152">Initializes the **SampleDesc** member of **PipelineStream** using the value of the *SampleDesc* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c0c53-153">**SampleMaskCb (UINT SampleMask)**</span><span class="sxs-lookup"><span data-stu-id="c0c53-153">**SampleMaskCb(UINT SampleMask)**</span></span>
</dt> <dd>

<span data-ttu-id="c0c53-154">Initialise le membre **SampleMask** de **PipelineStream** à l’aide de la valeur du paramètre *SampleMask* .</span><span class="sxs-lookup"><span data-stu-id="c0c53-154">Initializes the **SampleMask** member of **PipelineStream** using the value of the *SampleMask* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c0c53-155">**ViewInstancingCb (const D3D12 \_ View \_ INSTANCING \_ desc& ViewInstancingDesc)**</span><span class="sxs-lookup"><span data-stu-id="c0c53-155">**ViewInstancingCb(const D3D12\_VIEW\_INSTANCING\_DESC& ViewInstancingDesc)**</span></span>
</dt> <dd>

<span data-ttu-id="c0c53-156">Initialise le membre **ViewInstancingDesc** de **PipelineStream** à l’aide de la valeur du paramètre *ViewInstancingDesc* .</span><span class="sxs-lookup"><span data-stu-id="c0c53-156">Initializes the **ViewInstancingDesc** member of **PipelineStream** using the value of the *ViewInstancingDesc* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c0c53-157">**CachedPSOCb (const D3D12 \_ État du \_ pipeline mis en cache \_& CachedPSO)**</span><span class="sxs-lookup"><span data-stu-id="c0c53-157">**CachedPSOCb(const D3D12\_CACHED\_PIPELINE\_STATE& CachedPSO)**</span></span>
</dt> <dd>

<span data-ttu-id="c0c53-158">Initialise le membre **CachedPSO** de **PipelineStream** à l’aide de la valeur du paramètre *CachedPSO* .</span><span class="sxs-lookup"><span data-stu-id="c0c53-158">Initializes the **CachedPSO** member of **PipelineStream** using the value of the *CachedPSO* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c0c53-159">**ErrorBadInputParameter (UINT)**</span><span class="sxs-lookup"><span data-stu-id="c0c53-159">**ErrorBadInputParameter(UINT)**</span></span>
</dt> <dd>

<span data-ttu-id="c0c53-160">Ne fait rien.</span><span class="sxs-lookup"><span data-stu-id="c0c53-160">Does nothing.</span></span>

</dd> <dt>

<span data-ttu-id="c0c53-161">**ErrorDuplicateSubobject ( \_ type de \_ sous-objet état du pipeline D3D12 \_ \_ )**</span><span class="sxs-lookup"><span data-stu-id="c0c53-161">**ErrorDuplicateSubobject(D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE)**</span></span>
</dt> <dd>

<span data-ttu-id="c0c53-162">Ne fait rien.</span><span class="sxs-lookup"><span data-stu-id="c0c53-162">Does nothing.</span></span>

</dd> <dt>

<span data-ttu-id="c0c53-163">**ErrorUnknownSubobject (UINT)**</span><span class="sxs-lookup"><span data-stu-id="c0c53-163">**ErrorUnknownSubobject(UINT)**</span></span>
</dt> <dd>

<span data-ttu-id="c0c53-164">Ne fait rien.</span><span class="sxs-lookup"><span data-stu-id="c0c53-164">Does nothing.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c0c53-165">Notes</span><span class="sxs-lookup"><span data-stu-id="c0c53-165">Remarks</span></span>

<span data-ttu-id="c0c53-166">Lorsqu’il est passé en tant que deuxième paramètre à la fonction [**D3DX12ParsePipelineStream**](d3dx12parsepipelinestream.md) , les détails de l’objet STREAM1 interne de l' [**\_ \_ état \_ du pipeline CD3DX12**](cd3dx12-pipeline-state-stream1.md) sont clonés à partir du flux de données d' [**\_ État du pipeline \_ \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc) passé comme premier paramètre.</span><span class="sxs-lookup"><span data-stu-id="c0c53-166">When passed as the second parameter to the [**D3DX12ParsePipelineStream**](d3dx12parsepipelinestream.md) function, the details of the internal [**CD3DX12\_PIPELINE\_STATE\_STREAM1**](cd3dx12-pipeline-state-stream1.md) object are cloned from the [**D3D12\_PIPELINE\_STATE\_STREAM\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc) passed as the first parameter.</span></span> <span data-ttu-id="c0c53-167">Ce processus valide la description du flux source.</span><span class="sxs-lookup"><span data-stu-id="c0c53-167">This process validates the source stream description.</span></span> <span data-ttu-id="c0c53-168">Si D3DX12ParsePipelineStream retourne la valeur **\_ OK**, la description du flux source et les **STREAM1PipelineStream d' \_ \_ État de \_ pipeline CD3DX12** résultants sont valides ; sinon, les deux ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="c0c53-168">If D3DX12ParsePipelineStream returns **S\_OK**, then both the source stream description and the resulting **CD3DX12\_PIPELINE\_STATE\_STREAM1PipelineStream** are valid; otherwise both are invalid.</span></span> <span data-ttu-id="c0c53-169">Les flux non valides et les autres erreurs sont signalés uniquement via la valeur de retour de D3DX12ParsePipelineStream ; Cette structure implémente les rappels d’erreur pour ne rien faire.</span><span class="sxs-lookup"><span data-stu-id="c0c53-169">Invalid streams and other errors are reported only through the return value of D3DX12ParsePipelineStream; this structure implements the error callbacks to do nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0c53-170">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0c53-170">Requirements</span></span>



| <span data-ttu-id="c0c53-171">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0c53-171">Requirement</span></span> | <span data-ttu-id="c0c53-172">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0c53-172">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c0c53-173">En-tête</span><span class="sxs-lookup"><span data-stu-id="c0c53-173">Header</span></span><br/> | <dl> <span data-ttu-id="c0c53-174"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0c53-174"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0c53-175">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0c53-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0c53-176">Structures d’assistance pour Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="c0c53-176">Helper Structures for Direct3D 12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="c0c53-177">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="c0c53-177">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





