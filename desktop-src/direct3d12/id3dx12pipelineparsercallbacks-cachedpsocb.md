---
title: Méthode ID3DX12PipelineParserCallbacks CachedPSOCb (D3DX12. h)
description: Appelle le rappel d’objet de sous-objet PSO mis en cache (objet d’état de pipeline) d’un objet qui implémente cette interface.
ms.assetid: 9EF8C468-1D86-4F49-9091-36B6125F1B68
keywords:
- Méthode CachedPSOCb
- Méthode CachedPSOCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode CachedPSOCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.CachedPSOCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c168635a66eff012768a1eabbc803c6986a2c43
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525895"
---
# <a name="id3dx12pipelineparsercallbackscachedpsocb-method"></a><span data-ttu-id="38a0e-106">ID3DX12PipelineParserCallbacks :: CachedPSOCb, méthode</span><span class="sxs-lookup"><span data-stu-id="38a0e-106">ID3DX12PipelineParserCallbacks::CachedPSOCb method</span></span>

<span data-ttu-id="38a0e-107">Appelle le rappel d’objet de sous-objet PSO mis en cache (objet d’état de pipeline) d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="38a0e-107">Calls the cached PSO (Pipeline State Object) subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="38a0e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="38a0e-108">Syntax</span></span>


```C++
void CachedPSOCb(
  [ref] const D3D12_CACHED_PIPELINE_STATE &CachedPSO
);
```



## <a name="parameters"></a><span data-ttu-id="38a0e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="38a0e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38a0e-110">*CachedPSO* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="38a0e-110">*CachedPSO* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="38a0e-111">Type : **const [**D3D12 \_ \_ \_ État du pipeline mis en cache**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)**</span><span class="sxs-lookup"><span data-stu-id="38a0e-111">Type: **const [**D3D12\_CACHED\_PIPELINE\_STATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)**</span></span>

<span data-ttu-id="38a0e-112">Détails du sous-objet PSO mis en cache (objet d’État du pipeline) analysé à partir d’un flux d’État du pipeline.</span><span class="sxs-lookup"><span data-stu-id="38a0e-112">Details of the cached PSO (Pipeline State Object) subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38a0e-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="38a0e-113">Return value</span></span>

<span data-ttu-id="38a0e-114">Retourne la valeur Nothing.</span><span class="sxs-lookup"><span data-stu-id="38a0e-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="38a0e-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="38a0e-115">Requirements</span></span>



| <span data-ttu-id="38a0e-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="38a0e-116">Requirement</span></span> | <span data-ttu-id="38a0e-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="38a0e-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="38a0e-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="38a0e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="38a0e-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="38a0e-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="38a0e-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="38a0e-120">Library</span></span><br/> | <dl> <span data-ttu-id="38a0e-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="38a0e-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="38a0e-122">DLL</span><span class="sxs-lookup"><span data-stu-id="38a0e-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="38a0e-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38a0e-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38a0e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38a0e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38a0e-125">Interfaces d’assistance pour Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="38a0e-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="38a0e-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="38a0e-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="38a0e-127">**\_ \_ État du pipeline mis en cache D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="38a0e-127">**D3D12\_CACHED\_PIPELINE\_STATE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)
</dt> </dl>

 

 





