---
title: Méthode ID3DX12PipelineParserCallbacks PrimitiveTopologyTypeCb (D3DX12. h)
description: Appelle le rappel de sous-objet de type de topologie primitif d’un objet qui implémente cette interface.
ms.assetid: FF9D8D5C-3A6A-40D8-8EA4-3EA305EB4568
keywords:
- Méthode PrimitiveTopologyTypeCb
- Méthode PrimitiveTopologyTypeCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode PrimitiveTopologyTypeCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.PrimitiveTopologyTypeCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b01a2d73edd6ac94719905757d75a756c905c832
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527119"
---
# <a name="id3dx12pipelineparsercallbacksprimitivetopologytypecb-method"></a><span data-ttu-id="aceba-106">ID3DX12PipelineParserCallbacks ::P méthode rimitiveTopologyTypeCb</span><span class="sxs-lookup"><span data-stu-id="aceba-106">ID3DX12PipelineParserCallbacks::PrimitiveTopologyTypeCb method</span></span>

<span data-ttu-id="aceba-107">Appelle le rappel de sous-objet de type de topologie primitif d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="aceba-107">Calls the primitive topology type subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="aceba-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aceba-108">Syntax</span></span>


```C++
void PrimitiveTopologyTypeCb(
   D3D12_PRIMITIVE_TOPOLOGY_TYPE PrimitiveTopologyType
);
```



## <a name="parameters"></a><span data-ttu-id="aceba-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aceba-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aceba-110">*PrimitiveTopologyType*</span><span class="sxs-lookup"><span data-stu-id="aceba-110">*PrimitiveTopologyType*</span></span> 
</dt> <dd>

<span data-ttu-id="aceba-111">Type : **[ **\_ \_ \_ type de topologie primitive D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)**</span><span class="sxs-lookup"><span data-stu-id="aceba-111">Type: **[**D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)**</span></span>

<span data-ttu-id="aceba-112">Détails du sous-objet de type de topologie primitif analysé à partir d’un flux d’état de pipeline.</span><span class="sxs-lookup"><span data-stu-id="aceba-112">Details of the primitive topology type subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aceba-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="aceba-113">Return value</span></span>

<span data-ttu-id="aceba-114">Retourne la valeur Nothing.</span><span class="sxs-lookup"><span data-stu-id="aceba-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="aceba-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aceba-115">Requirements</span></span>



| <span data-ttu-id="aceba-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aceba-116">Requirement</span></span> | <span data-ttu-id="aceba-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="aceba-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="aceba-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="aceba-118">Header</span></span><br/>  | <dl> <span data-ttu-id="aceba-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="aceba-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="aceba-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="aceba-120">Library</span></span><br/> | <dl> <span data-ttu-id="aceba-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aceba-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="aceba-122">DLL</span><span class="sxs-lookup"><span data-stu-id="aceba-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="aceba-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aceba-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aceba-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aceba-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aceba-125">Interfaces d’assistance pour Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="aceba-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="aceba-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="aceba-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="aceba-127">**\_Type de \_ topologie primitive \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="aceba-127">**D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)
</dt> </dl>

 

 





