---
title: Interface ID3DX12PipelineParserCallbacks (D3DX12. h)
description: Interface qui représente une collection d’analyseurs et les rappels d’erreur utilisés par la fonction d’assistance D3DX12parsePipelineStream.
ms.assetid: CBC04D17-2E19-4755-B1CB-FC42BF5083E5
keywords:
- Interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, Description
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b0061746da589c30e4745dfa3e4dc573f7b5d52
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538347"
---
# <a name="id3dx12pipelineparsercallbacks-interface"></a><span data-ttu-id="4c908-105">Interface ID3DX12PipelineParserCallbacks</span><span class="sxs-lookup"><span data-stu-id="4c908-105">ID3DX12PipelineParserCallbacks interface</span></span>

<span data-ttu-id="4c908-106">Interface qui représente une collection d’analyseurs et les rappels d’erreur utilisés par la fonction d’assistance [**D3DX12parsePipelineStream**](d3dx12parsepipelinestream.md) .</span><span class="sxs-lookup"><span data-stu-id="4c908-106">An interface that represents a collection of parser and error callbacks used by the [**D3DX12parsePipelineStream**](d3dx12parsepipelinestream.md) helper function.</span></span>

-   [<span data-ttu-id="4c908-107">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4c908-107">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4c908-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4c908-108">Methods</span></span>

<span data-ttu-id="4c908-109">L’interface **ID3DX12PipelineParserCallbacks** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="4c908-109">The **ID3DX12PipelineParserCallbacks** interface has these methods.</span></span>



| <span data-ttu-id="4c908-110">Méthode</span><span class="sxs-lookup"><span data-stu-id="4c908-110">Method</span></span>                                                                                    | <span data-ttu-id="4c908-111">Description</span><span class="sxs-lookup"><span data-stu-id="4c908-111">Description</span></span>                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4c908-112">**BlendStateCb**</span><span class="sxs-lookup"><span data-stu-id="4c908-112">**BlendStateCb**</span></span>](id3dx12pipelineparsercallbacks-blendstatecb.md)                       | <span data-ttu-id="4c908-113">Appelle le rappel de sous-objet de description de l’état de fusion d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="4c908-113">Calls the blend state description subobject callback of an object that implements this interface.</span></span><br/>                                                                 |
| [<span data-ttu-id="4c908-114">**CachedPSOCb**</span><span class="sxs-lookup"><span data-stu-id="4c908-114">**CachedPSOCb**</span></span>](id3dx12pipelineparsercallbacks-cachedpsocb.md)                         | <span data-ttu-id="4c908-115">Appelle le rappel d’objet de sous-objet PSO mis en cache (objet d’état de pipeline) d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="4c908-115">Calls the cached PSO (Pipeline State Object) subobject callback of an object that implements this interface.</span></span><br/>                                                      |
| [<span data-ttu-id="4c908-116">**CSCb**</span><span class="sxs-lookup"><span data-stu-id="4c908-116">**CSCb**</span></span>](id3dx12pipelineparsercallbacks-cscb.md)                                       | <span data-ttu-id="4c908-117">Appelle le rappel du sous-objet de nuanceur de calcul d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="4c908-117">Calls the compute shader subobject callback of an object that implements this interface.</span></span><br/>                                                                          |
| [<span data-ttu-id="4c908-118">**DepthStencilState1Cb**</span><span class="sxs-lookup"><span data-stu-id="4c908-118">**DepthStencilState1Cb**</span></span>](id3dx12pipelineparsercallbacks-depthstencilstate1cb.md)       | <span data-ttu-id="4c908-119">Appelle l’état du stencil de profondeur ([**D3D12 \_ Depth \_ stencil \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)) rappel de sous-objet d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="4c908-119">Calls the depth stencil state ([**D3D12\_DEPTH\_STENCIL\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)) subobject callback of an object that implements this interface.</span></span><br/> |
| [<span data-ttu-id="4c908-120">**DepthStencilStateCb**</span><span class="sxs-lookup"><span data-stu-id="4c908-120">**DepthStencilStateCb**</span></span>](id3dx12pipelineparsercallbacks-dsvformatcb.md)                 | <span data-ttu-id="4c908-121">Appelle le rappel de format de valeur de stencil de profondeur d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="4c908-121">Calls the depth stencil value format subobject callback of an object that implements this interface.</span></span><br/>                                                              |
| [<span data-ttu-id="4c908-122">**DepthStencilStateCb**</span><span class="sxs-lookup"><span data-stu-id="4c908-122">**DepthStencilStateCb**</span></span>](id3dx12pipelineparsercallbacks-depthstencilstatecb.md)         | <span data-ttu-id="4c908-123">Appelle le rappel de sous-objet d’État du stencil de profondeur d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="4c908-123">Calls the depth stencil state subobject callback of an object that implements this interface.</span></span><br/>                                                                     |
| [<span data-ttu-id="4c908-124">**DSCb**</span><span class="sxs-lookup"><span data-stu-id="4c908-124">**DSCb**</span></span>](id3dx12pipelineparsercallbacks-dscb.md)                                       | <span data-ttu-id="4c908-125">Appelle le rappel de sous-objet de nuanceur de domaine d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="4c908-125">Calls the domain shader subobject callback of an object that implements this interface.</span></span><br/>                                                                           |
| [<span data-ttu-id="4c908-126">**ErrorBadInputParameter**</span><span class="sxs-lookup"><span data-stu-id="4c908-126">**ErrorBadInputParameter**</span></span>](id3dx12pipelineparsercallbacks-errorbadinputparameter.md)   | <span data-ttu-id="4c908-127">Appelle le rappel d’erreur de paramètre d’entrée incorrect d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="4c908-127">Calls the bad input parameter error callback of an object that implements this interface.</span></span><br/>                                                                         |
| [<span data-ttu-id="4c908-128">**ErrorDuplicateSubobject**</span><span class="sxs-lookup"><span data-stu-id="4c908-128">**ErrorDuplicateSubobject**</span></span>](id3dx12pipelineparsercallbacks-errorduplicatesubobject.md) | <span data-ttu-id="4c908-129">Appelle le rappel d’erreur de sous-objet dupliqué d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="4c908-129">Calls the duplicate subobject error callback of an object that implements this interface.</span></span><br/>                                                                         |
| [<span data-ttu-id="4c908-130">**ErrorUnknownSubobject**</span><span class="sxs-lookup"><span data-stu-id="4c908-130">**ErrorUnknownSubobject**</span></span>](id3dx12pipelineparsercallbacks-errorunknownsubobject.md)     | <span data-ttu-id="4c908-131">Appelle le rappel d’erreur de sous-objet inconnu d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="4c908-131">Calls the unknown subobject error callback of an object that implements this interface.</span></span><br/>                                                                           |
| [<span data-ttu-id="4c908-132">**FlagsCb**</span><span class="sxs-lookup"><span data-stu-id="4c908-132">**FlagsCb**</span></span>](id3dx12pipelineparsercallbacks-flagscb.md)                                 | <span data-ttu-id="4c908-133">Appelle le rappel de sous-objet d’indicateurs d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="4c908-133">Calls the flags subobject callback of an object that implements this interface.</span></span><br/>                                                                                   |
| [<span data-ttu-id="4c908-134">**GSCb**</span><span class="sxs-lookup"><span data-stu-id="4c908-134">**GSCb**</span></span>](id3dx12pipelineparsercallbacks-gscb.md)                                       | <span data-ttu-id="4c908-135">Appelle le rappel de sous-objet de nuanceur Geometry d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="4c908-135">Calls the geometry shader subobject callback of an object that implements this interface.</span></span><br/>                                                                         |
| [<span data-ttu-id="4c908-136">**HSCb**</span><span class="sxs-lookup"><span data-stu-id="4c908-136">**HSCb**</span></span>](id3dx12pipelineparsercallbacks-hscb.md)                                       | <span data-ttu-id="4c908-137">Appelle le rappel de sous-objet de nuanceur de coque d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="4c908-137">Calls the hull shader subobject callback of an object that implements this interface.</span></span><br/>                                                                             |
| [<span data-ttu-id="4c908-138">**IBStripCutValueCb**</span><span class="sxs-lookup"><span data-stu-id="4c908-138">**IBStripCutValueCb**</span></span>](id3dx12pipelineparsercallbacks-ibstripcutvaluecb.md)             | <span data-ttu-id="4c908-139">Appelle le rappel de sous-objet de valeur de coupe de la mémoire tampon d’index d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="4c908-139">Calls the index buffer strip-cut value subobject callback of an object that implements this interface.</span></span><br/>                                                            |
| [<span data-ttu-id="4c908-140">**InputLayoutCb**</span><span class="sxs-lookup"><span data-stu-id="4c908-140">**InputLayoutCb**</span></span>](id3dx12pipelineparsercallbacks-inputlayoutcb.md)                     | <span data-ttu-id="4c908-141">Appelle le rappel de sous-objet de la disposition d’entrée d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="4c908-141">Calls the input layout subobject callback of an object that implements this interface.</span></span><br/>                                                                            |
| [<span data-ttu-id="4c908-142">**NodemaskCb**</span><span class="sxs-lookup"><span data-stu-id="4c908-142">**NodemaskCb**</span></span>](id3dx12pipelineparsercallbacks-nodemaskcb.md)                           | <span data-ttu-id="4c908-143">Appelle le rappel de sous-objet nodemask d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="4c908-143">Calls the nodemask subobject callback of an object that implements this interface.</span></span><br/>                                                                                |
| [<span data-ttu-id="4c908-144">**PrimitiveTopologyTypeCb**</span><span class="sxs-lookup"><span data-stu-id="4c908-144">**PrimitiveTopologyTypeCb**</span></span>](id3dx12pipelineparsercallbacks-primitivetopologytypecb.md) | <span data-ttu-id="4c908-145">Appelle le rappel de sous-objet de type de topologie primitif d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="4c908-145">Calls the primitive topology type subobject callback of an object that implements this interface.</span></span><br/>                                                                 |
| [<span data-ttu-id="4c908-146">**PSCb**</span><span class="sxs-lookup"><span data-stu-id="4c908-146">**PSCb**</span></span>](id3dx12pipelineparsercallbacks-pscb.md)                                       | <span data-ttu-id="4c908-147">Appelle le rappel de sous-objet de nuanceur de pixels d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="4c908-147">Calls the pixel shader subobject callback of an object that implements this interface.</span></span><br/>                                                                            |
| [<span data-ttu-id="4c908-148">**RasterizerStateCb**</span><span class="sxs-lookup"><span data-stu-id="4c908-148">**RasterizerStateCb**</span></span>](id3dx12pipelineparsercallbacks-rasterizerstatecb.md)             | <span data-ttu-id="4c908-149">Appelle le rappel de sous-objet de description de l’état de rastériseur d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="4c908-149">Calls the rasterizer state description subobject callback of an object that implements this interface.</span></span><br/>                                                            |
| [<span data-ttu-id="4c908-150">**RootSignatureCB**</span><span class="sxs-lookup"><span data-stu-id="4c908-150">**RootSignatureCB**</span></span>](id3dx12pipelineparsercallbacks-rootsignaturecb.md)                 | <span data-ttu-id="4c908-151">Appelle le rappel de sous-objet de signature racine d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="4c908-151">Calls the root signature subobject callback of an object that implements this interface.</span></span><br/>                                                                          |
| [<span data-ttu-id="4c908-152">**RTVFormatsCb**</span><span class="sxs-lookup"><span data-stu-id="4c908-152">**RTVFormatsCb**</span></span>](id3dx12pipelineparsercallbacks-rtvformatscb.md)                       | <span data-ttu-id="4c908-153">Appelle le rappel de sous-objet du tableau de format de la cible de rendu d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="4c908-153">Calls the render target format array subobject callback of an object that implements this interface.</span></span><br/>                                                              |
| [<span data-ttu-id="4c908-154">**SampleDescCb**</span><span class="sxs-lookup"><span data-stu-id="4c908-154">**SampleDescCb**</span></span>](id3dx12pipelineparsercallbacks-sampledesccb.md)                       | <span data-ttu-id="4c908-155">Appelle l’exemple de rappel de sous-objet de description d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="4c908-155">Calls the sample description subobject callback of an object that implements this interface.</span></span><br/>                                                                      |
| [<span data-ttu-id="4c908-156">**SampleMaskCb**</span><span class="sxs-lookup"><span data-stu-id="4c908-156">**SampleMaskCb**</span></span>](id3dx12pipelineparsercallbacks-samplemaskcb.md)                       | <span data-ttu-id="4c908-157">Appelle l’exemple de rappel de sous-objet de masque d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="4c908-157">Calls the sample mask subobject callback of an object that implements this interface.</span></span><br/>                                                                             |
| [<span data-ttu-id="4c908-158">**StreamOutputCb**</span><span class="sxs-lookup"><span data-stu-id="4c908-158">**StreamOutputCb**</span></span>](id3dx12pipelineparsercallbacks-streamoutputcb.md)                   | <span data-ttu-id="4c908-159">Appelle le rappel de sortie de flux de sous-objet d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="4c908-159">Calls the stream output description subobject callback of an object that implements this interface.</span></span><br/>                                                               |
| [<span data-ttu-id="4c908-160">**VSCb**</span><span class="sxs-lookup"><span data-stu-id="4c908-160">**VSCb**</span></span>](id3dx12pipelineparsercallbacks-vscb.md)                                       | <span data-ttu-id="4c908-161">Appelle le rappel de sous-objet de nuanceur vertex d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="4c908-161">Calls the vertex shader subobject callback of an object that implements this interface.</span></span><br/>                                                                           |



 

## <a name="requirements"></a><span data-ttu-id="4c908-162">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4c908-162">Requirements</span></span>



| <span data-ttu-id="4c908-163">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4c908-163">Requirement</span></span> | <span data-ttu-id="4c908-164">Valeur</span><span class="sxs-lookup"><span data-stu-id="4c908-164">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4c908-165">En-tête</span><span class="sxs-lookup"><span data-stu-id="4c908-165">Header</span></span><br/>  | <dl> <span data-ttu-id="4c908-166"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c908-166"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="4c908-167">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4c908-167">Library</span></span><br/> | <dl> <span data-ttu-id="4c908-168"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c908-168"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="4c908-169">DLL</span><span class="sxs-lookup"><span data-stu-id="4c908-169">DLL</span></span><br/>     | <dl> <span data-ttu-id="4c908-170"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c908-170"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c908-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c908-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c908-172">Interfaces d’assistance pour Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="4c908-172">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="4c908-173">**D3DX12parsePipelineStream**</span><span class="sxs-lookup"><span data-stu-id="4c908-173">**D3DX12parsePipelineStream**</span></span>](d3dx12parsepipelinestream.md)
</dt> </dl>

 

 





