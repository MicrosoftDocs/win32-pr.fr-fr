---
title: Méthode ID3DX12PipelineParserCallbacks DepthStencilStateCb (D3DX12. h)
description: Appelle le rappel de sous-objet d’État du stencil de profondeur d’un objet qui implémente cette interface.
ms.assetid: 6E77A3B7-20D8-4D31-9D31-515CF4618157
keywords:
- Méthode DepthStencilStateCb
- Méthode DepthStencilStateCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode DepthStencilStateCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.DepthStencilStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 913dbddef0c509174d3600798a6e1380d6098808
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538490"
---
# <a name="id3dx12pipelineparsercallbacks-depthstencilstatecb-method-d3dx12h"></a><span data-ttu-id="f17ca-106">Méthode ID3DX12PipelineParserCallbacks DepthStencilStateCb (D3DX12. h)</span><span class="sxs-lookup"><span data-stu-id="f17ca-106">ID3DX12PipelineParserCallbacks DepthStencilStateCb method (D3DX12.h)</span></span>

<span data-ttu-id="f17ca-107">Appelle le rappel de sous-objet d’État du stencil de profondeur d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="f17ca-107">Calls the depth stencil state subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="f17ca-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f17ca-108">Syntax</span></span>


```C++
void DepthStencilStateCb(
  [ref] const D3D12_DEPTH_STENCIL_DESC &DepthStencilState
);
```



## <a name="parameters"></a><span data-ttu-id="f17ca-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f17ca-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f17ca-110">*DepthStencilState* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="f17ca-110">*DepthStencilState* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="f17ca-111">Type : **const [**D3D12 de \_ profondeur du \_ stencil \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)**</span><span class="sxs-lookup"><span data-stu-id="f17ca-111">Type: **const [**D3D12\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)**</span></span>

<span data-ttu-id="f17ca-112">Détails du sous-objet état du stencil de profondeur analysé à partir d’un flux d’État du pipeline.</span><span class="sxs-lookup"><span data-stu-id="f17ca-112">Details of the depth stencil state subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f17ca-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f17ca-113">Return value</span></span>

<span data-ttu-id="f17ca-114">Retourne la valeur Nothing.</span><span class="sxs-lookup"><span data-stu-id="f17ca-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="f17ca-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f17ca-115">Requirements</span></span>



| <span data-ttu-id="f17ca-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f17ca-116">Requirement</span></span> | <span data-ttu-id="f17ca-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f17ca-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f17ca-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="f17ca-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f17ca-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="f17ca-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="f17ca-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f17ca-120">Library</span></span><br/> | <dl> <span data-ttu-id="f17ca-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f17ca-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="f17ca-122">DLL</span><span class="sxs-lookup"><span data-stu-id="f17ca-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="f17ca-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f17ca-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f17ca-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f17ca-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f17ca-125">Interfaces d’assistance pour Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="f17ca-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="f17ca-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="f17ca-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="f17ca-127">**\_Description du \_ stencil de profondeur D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="f17ca-127">**D3D12\_DEPTH\_STENCIL\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> </dl>

 

 





