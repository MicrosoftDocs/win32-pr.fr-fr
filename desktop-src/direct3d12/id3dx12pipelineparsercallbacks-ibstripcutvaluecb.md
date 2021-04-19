---
title: Méthode ID3DX12PipelineParserCallbacks IBStripCutValueCb (D3DX12. h)
description: Appelle le rappel de sous-objet de valeur de coupe de la mémoire tampon d’index d’un objet qui implémente cette interface.
ms.assetid: 702CA90A-FF20-4554-9469-C86428C203BC
keywords:
- Méthode IBStripCutValueCb
- Méthode IBStripCutValueCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode IBStripCutValueCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.IBStripCutValueCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f79fca93e76f43b97ffc8e133594805214fe84cc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106544404"
---
# <a name="id3dx12pipelineparsercallbacksibstripcutvaluecb-method"></a><span data-ttu-id="4d7c6-106">ID3DX12PipelineParserCallbacks :: IBStripCutValueCb, méthode</span><span class="sxs-lookup"><span data-stu-id="4d7c6-106">ID3DX12PipelineParserCallbacks::IBStripCutValueCb method</span></span>

<span data-ttu-id="4d7c6-107">Appelle le rappel de sous-objet de valeur de coupe de la mémoire tampon d’index d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="4d7c6-107">Calls the index buffer strip-cut value subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d7c6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4d7c6-108">Syntax</span></span>


```C++
void IBStripCutValueCb(
   D3D12_INDEX_BUFFER_STRIP_CUT_VALUE IBStripCutValue
);
```



## <a name="parameters"></a><span data-ttu-id="4d7c6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4d7c6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d7c6-110">*IBStripCutValue*</span><span class="sxs-lookup"><span data-stu-id="4d7c6-110">*IBStripCutValue*</span></span> 
</dt> <dd>

<span data-ttu-id="4d7c6-111">Type : valeur de coupe de la **[ **\_ \_ bande de mémoire tampon \_ \_ \_ d’index D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)**</span><span class="sxs-lookup"><span data-stu-id="4d7c6-111">Type: **[**D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)**</span></span>

<span data-ttu-id="4d7c6-112">Détails du sous-objet de valeur coupe-bande de la mémoire tampon d’index analysé à partir d’un flux d’État du pipeline.</span><span class="sxs-lookup"><span data-stu-id="4d7c6-112">Details of the index buffer strip-cut value subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d7c6-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4d7c6-113">Return value</span></span>

<span data-ttu-id="4d7c6-114">Retourne la valeur Nothing.</span><span class="sxs-lookup"><span data-stu-id="4d7c6-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d7c6-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4d7c6-115">Requirements</span></span>



| <span data-ttu-id="4d7c6-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4d7c6-116">Requirement</span></span> | <span data-ttu-id="4d7c6-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="4d7c6-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4d7c6-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="4d7c6-118">Header</span></span><br/>  | <dl> <span data-ttu-id="4d7c6-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d7c6-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="4d7c6-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4d7c6-120">Library</span></span><br/> | <dl> <span data-ttu-id="4d7c6-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4d7c6-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="4d7c6-122">DLL</span><span class="sxs-lookup"><span data-stu-id="4d7c6-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="4d7c6-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d7c6-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d7c6-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d7c6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d7c6-125">Interfaces d’assistance pour Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="4d7c6-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="4d7c6-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="4d7c6-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="4d7c6-127">**Valeur de coupe de la \_ \_ bande de mémoire tampon d’index \_ D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4d7c6-127">**D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)
</dt> </dl>

 

 





