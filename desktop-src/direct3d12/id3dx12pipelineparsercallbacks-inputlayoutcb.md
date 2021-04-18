---
title: Méthode ID3DX12PipelineParserCallbacks InputLayoutCb (D3DX12. h)
description: Appelle le rappel de sous-objet de la disposition d’entrée d’un objet qui implémente cette interface.
ms.assetid: A21AB7A1-6E51-42CB-BA98-C0BD08D43009
keywords:
- Méthode InputLayoutCb
- Méthode InputLayoutCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode InputLayoutCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.InputLayoutCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bc28276ef893247577cf41de8f4aba5582c101d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522606"
---
# <a name="id3dx12pipelineparsercallbacksinputlayoutcb-method"></a><span data-ttu-id="e7ed0-106">ID3DX12PipelineParserCallbacks :: InputLayoutCb, méthode</span><span class="sxs-lookup"><span data-stu-id="e7ed0-106">ID3DX12PipelineParserCallbacks::InputLayoutCb method</span></span>

<span data-ttu-id="e7ed0-107">Appelle le rappel de sous-objet de la disposition d’entrée d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="e7ed0-107">Calls the input layout subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7ed0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7ed0-108">Syntax</span></span>


```C++
void InputLayoutCb(
  [ref] const D3D12_INPUT_LAYOUT_DESC &InputLayout
);
```



## <a name="parameters"></a><span data-ttu-id="e7ed0-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7ed0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7ed0-110">*InputLayout* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="e7ed0-110">*InputLayout* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="e7ed0-111">Type : **const [**D3D12 \_ disposition d’entrée \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc)**</span><span class="sxs-lookup"><span data-stu-id="e7ed0-111">Type: **const [**D3D12\_INPUT\_LAYOUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc)**</span></span>

<span data-ttu-id="e7ed0-112">Détails du sous-objet de disposition d’entrée analysé à partir d’un flux d’état de pipeline.</span><span class="sxs-lookup"><span data-stu-id="e7ed0-112">Details of the input layout subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7ed0-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e7ed0-113">Return value</span></span>

<span data-ttu-id="e7ed0-114">Retourne la valeur Nothing.</span><span class="sxs-lookup"><span data-stu-id="e7ed0-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7ed0-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7ed0-115">Requirements</span></span>



| <span data-ttu-id="e7ed0-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7ed0-116">Requirement</span></span> | <span data-ttu-id="e7ed0-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7ed0-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e7ed0-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="e7ed0-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e7ed0-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7ed0-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="e7ed0-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e7ed0-120">Library</span></span><br/> | <dl> <span data-ttu-id="e7ed0-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7ed0-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="e7ed0-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e7ed0-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="e7ed0-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7ed0-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7ed0-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7ed0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7ed0-125">Interfaces d’assistance pour Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="e7ed0-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="e7ed0-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="e7ed0-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="e7ed0-127">**Description de la \_ disposition d’entrée D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e7ed0-127">**D3D12\_INPUT\_LAYOUT\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc)
</dt> </dl>

 

 





