---
title: Méthode ID3DX12PipelineParserCallbacks RasterizerStateCb (D3DX12. h)
description: Appelle le rappel de sous-objet de description de l’état de rastériseur d’un objet qui implémente cette interface.
ms.assetid: 125FC6EC-B749-4EE2-9D34-14BD12993BDC
keywords:
- Méthode RasterizerStateCb
- Méthode RasterizerStateCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode RasterizerStateCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RasterizerStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a970e8061ed9199ba5a6a334c7b670218e93936
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539462"
---
# <a name="id3dx12pipelineparsercallbacksrasterizerstatecb-method"></a><span data-ttu-id="195cf-106">ID3DX12PipelineParserCallbacks :: RasterizerStateCb, méthode</span><span class="sxs-lookup"><span data-stu-id="195cf-106">ID3DX12PipelineParserCallbacks::RasterizerStateCb method</span></span>

<span data-ttu-id="195cf-107">Appelle le rappel de sous-objet de description de l’état de rastériseur d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="195cf-107">Calls the rasterizer state description subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="195cf-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="195cf-108">Syntax</span></span>


```C++
void RasterizerStateCb(
  [ref] const D3D12_RASTERIZER_DESC &RasterizerState
);
```



## <a name="parameters"></a><span data-ttu-id="195cf-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="195cf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="195cf-110">*RasterizerState* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="195cf-110">*RasterizerState* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="195cf-111">Type : **const [**D3D12 \_ rastériseur \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)**</span><span class="sxs-lookup"><span data-stu-id="195cf-111">Type: **const [**D3D12\_RASTERIZER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)**</span></span>

<span data-ttu-id="195cf-112">Détails du sous-objet de description de l’état du rastériseur analysé à partir d’un flux d’État du pipeline.</span><span class="sxs-lookup"><span data-stu-id="195cf-112">Details of the rasterizer state description subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="195cf-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="195cf-113">Return value</span></span>

<span data-ttu-id="195cf-114">Retourne la valeur Nothing.</span><span class="sxs-lookup"><span data-stu-id="195cf-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="195cf-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="195cf-115">Requirements</span></span>



| <span data-ttu-id="195cf-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="195cf-116">Requirement</span></span> | <span data-ttu-id="195cf-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="195cf-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="195cf-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="195cf-118">Header</span></span><br/>  | <dl> <span data-ttu-id="195cf-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="195cf-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="195cf-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="195cf-120">Library</span></span><br/> | <dl> <span data-ttu-id="195cf-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="195cf-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="195cf-122">DLL</span><span class="sxs-lookup"><span data-stu-id="195cf-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="195cf-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="195cf-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="195cf-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="195cf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="195cf-125">Interfaces d’assistance pour Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="195cf-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="195cf-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="195cf-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="195cf-127">**D3D12 \_ rastériseur \_ desc**</span><span class="sxs-lookup"><span data-stu-id="195cf-127">**D3D12\_RASTERIZER\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)
</dt> </dl>

 

 





