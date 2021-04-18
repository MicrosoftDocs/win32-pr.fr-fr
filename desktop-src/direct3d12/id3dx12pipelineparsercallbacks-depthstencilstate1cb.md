---
title: Méthode ID3DX12PipelineParserCallbacks DepthStencilState1Cb (D3DX12. h)
description: Appelle l’état du stencil de profondeur (D3D12 \_ Depth \_ stencil \_ DESC1) rappel de sous-objet d’un objet qui implémente cette interface.
ms.assetid: C1AE06E5-B1FF-44C2-9C56-1540B97AD883
keywords:
- Méthode DepthStencilState1Cb
- Méthode DepthStencilState1Cb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode DepthStencilState1Cb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.DepthStencilState1Cb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a42cf85f60dcf27a5751f77a346931bfad6b03e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106520305"
---
# <a name="id3dx12pipelineparsercallbacksdepthstencilstate1cb-method"></a><span data-ttu-id="43507-106">ID3DX12PipelineParserCallbacks ::D méthode epthStencilState1Cb</span><span class="sxs-lookup"><span data-stu-id="43507-106">ID3DX12PipelineParserCallbacks::DepthStencilState1Cb method</span></span>

<span data-ttu-id="43507-107">Appelle l’état du stencil de profondeur ([**D3D12 \_ Depth \_ stencil \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)) rappel de sous-objet d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="43507-107">Calls the depth stencil state ([**D3D12\_DEPTH\_STENCIL\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)) subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="43507-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="43507-108">Syntax</span></span>


```C++
void DepthStencilState1Cb(
  [ref] const D3D12_DEPTH_STENCIL_DESC1 &DepthStencilState
);
```



## <a name="parameters"></a><span data-ttu-id="43507-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="43507-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43507-110">*DepthStencilState* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="43507-110">*DepthStencilState* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="43507-111">Type : **const [**D3D12 de \_ profondeur du \_ stencil \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)**</span><span class="sxs-lookup"><span data-stu-id="43507-111">Type: **const [**D3D12\_DEPTH\_STENCIL\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)**</span></span>

<span data-ttu-id="43507-112">Détails du sous-objet état du stencil de profondeur analysé à partir d’un flux d’État du pipeline.</span><span class="sxs-lookup"><span data-stu-id="43507-112">Details of the depth stencil state subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43507-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="43507-113">Return value</span></span>

<span data-ttu-id="43507-114">Retourne la valeur Nothing.</span><span class="sxs-lookup"><span data-stu-id="43507-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="43507-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43507-115">Requirements</span></span>



| <span data-ttu-id="43507-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43507-116">Requirement</span></span> | <span data-ttu-id="43507-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="43507-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="43507-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="43507-118">Header</span></span><br/>  | <dl> <span data-ttu-id="43507-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="43507-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="43507-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="43507-120">Library</span></span><br/> | <dl> <span data-ttu-id="43507-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="43507-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="43507-122">DLL</span><span class="sxs-lookup"><span data-stu-id="43507-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="43507-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43507-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43507-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43507-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43507-125">Interfaces d’assistance pour Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="43507-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="43507-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="43507-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="43507-127">**D3D12 \_ du \_ stencil de profondeur \_ DESC1**</span><span class="sxs-lookup"><span data-stu-id="43507-127">**D3D12\_DEPTH\_STENCIL\_DESC1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)
</dt> </dl>

 

 





