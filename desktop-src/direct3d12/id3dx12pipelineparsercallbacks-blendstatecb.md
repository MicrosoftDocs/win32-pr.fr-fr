---
title: Méthode ID3DX12PipelineParserCallbacks BlendStateCb (D3DX12. h)
description: Appelle le rappel de sous-objet de description de l’état de fusion d’un objet qui implémente cette interface.
ms.assetid: C00C733B-4123-4795-9A93-973F30BE456B
keywords:
- Méthode BlendStateCb
- Méthode BlendStateCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode BlendStateCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.BlendStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 119733fbe82203a6e423fb0ef9b07d3ecff70619
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106529623"
---
# <a name="id3dx12pipelineparsercallbacksblendstatecb-method"></a><span data-ttu-id="b78df-106">ID3DX12PipelineParserCallbacks :: BlendStateCb, méthode</span><span class="sxs-lookup"><span data-stu-id="b78df-106">ID3DX12PipelineParserCallbacks::BlendStateCb method</span></span>

<span data-ttu-id="b78df-107">Appelle le rappel de sous-objet de description de l’état de fusion d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="b78df-107">Calls the blend state description subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="b78df-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b78df-108">Syntax</span></span>


```C++
void BlendStateCb(
  [ref] const D3D12_BLEND_DESC &BlendState
);
```



## <a name="parameters"></a><span data-ttu-id="b78df-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b78df-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b78df-110">*BlendState* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="b78df-110">*BlendState* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="b78df-111">Type : **const [**D3D12 \_ Blend \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)**</span><span class="sxs-lookup"><span data-stu-id="b78df-111">Type: **const [**D3D12\_BLEND\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)**</span></span>

<span data-ttu-id="b78df-112">Détails du sous-objet de description de l’état de fusion analysé à partir d’un flux d’État du pipeline.</span><span class="sxs-lookup"><span data-stu-id="b78df-112">Details of the blend state description subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b78df-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b78df-113">Return value</span></span>

<span data-ttu-id="b78df-114">Retourne la valeur Nothing.</span><span class="sxs-lookup"><span data-stu-id="b78df-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="b78df-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b78df-115">Requirements</span></span>



| <span data-ttu-id="b78df-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b78df-116">Requirement</span></span> | <span data-ttu-id="b78df-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="b78df-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b78df-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="b78df-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b78df-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="b78df-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="b78df-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b78df-120">Library</span></span><br/> | <dl> <span data-ttu-id="b78df-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b78df-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="b78df-122">DLL</span><span class="sxs-lookup"><span data-stu-id="b78df-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="b78df-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b78df-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b78df-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b78df-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b78df-125">Interfaces d’assistance pour Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="b78df-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="b78df-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="b78df-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="b78df-127">**D3D12 \_ Blend \_ desc**</span><span class="sxs-lookup"><span data-stu-id="b78df-127">**D3D12\_BLEND\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)
</dt> </dl>

 

 





