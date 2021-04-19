---
title: Méthode ID3DX12PipelineParserCallbacks DepthStencilStateCb (D3DX12. h) (DSV)
description: Appelle le rappel de format de valeur de stencil de profondeur d’un objet qui implémente cette interface.
ms.assetid: BDD3AB24-34C6-41C8-984D-78A45867BF24
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
ms.openlocfilehash: fd40b138c357c143deafffe01252b3c8b3e87cda
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106535436"
---
# <a name="id3dx12pipelineparsercallbacks-depthstencilstatecb-method-d3dx12h-for-depth-stencil-value"></a><span data-ttu-id="93c1e-106">Méthode ID3DX12PipelineParserCallbacks DepthStencilStateCb (D3DX12. h) pour la valeur du stencil de profondeur</span><span class="sxs-lookup"><span data-stu-id="93c1e-106">ID3DX12PipelineParserCallbacks DepthStencilStateCb method (D3DX12.h) for depth stencil value</span></span>

<span data-ttu-id="93c1e-107">Appelle le rappel de format de valeur de stencil de profondeur d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="93c1e-107">Calls the depth stencil value format subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="93c1e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="93c1e-108">Syntax</span></span>


```C++
void DepthStencilStateCb(
   DXGI_FORMAT DepthStencilState
);
```



## <a name="parameters"></a><span data-ttu-id="93c1e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="93c1e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93c1e-110">*DepthStencilState*</span><span class="sxs-lookup"><span data-stu-id="93c1e-110">*DepthStencilState*</span></span> 
</dt> <dd>

<span data-ttu-id="93c1e-111">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="93c1e-111">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="93c1e-112">Détails du sous-objet de format de valeur du stencil de profondeur analysé à partir d’un flux d’État du pipeline.</span><span class="sxs-lookup"><span data-stu-id="93c1e-112">Details of the depth stencil value format subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93c1e-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="93c1e-113">Return value</span></span>

<span data-ttu-id="93c1e-114">Retourne la valeur Nothing.</span><span class="sxs-lookup"><span data-stu-id="93c1e-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="93c1e-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="93c1e-115">Requirements</span></span>



| <span data-ttu-id="93c1e-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="93c1e-116">Requirement</span></span> | <span data-ttu-id="93c1e-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="93c1e-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="93c1e-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="93c1e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="93c1e-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="93c1e-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="93c1e-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="93c1e-120">Library</span></span><br/> | <dl> <span data-ttu-id="93c1e-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="93c1e-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="93c1e-122">DLL</span><span class="sxs-lookup"><span data-stu-id="93c1e-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="93c1e-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93c1e-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93c1e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93c1e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93c1e-125">Interfaces d’assistance pour Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="93c1e-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="93c1e-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="93c1e-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="93c1e-127">**\_format dxgi**</span><span class="sxs-lookup"><span data-stu-id="93c1e-127">**DXGI\_FORMAT**</span></span>](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
</dt> </dl>

 

