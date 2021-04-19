---
title: Méthode ID3DX12PipelineParserCallbacks RTVFormatsCb (D3DX12. h)
description: Appelle le rappel de sous-objet du tableau de format de la cible de rendu d’un objet qui implémente cette interface.
ms.assetid: 0D5F0BC4-D9E2-4B16-99B5-509454AF8C02
keywords:
- Méthode RTVFormatsCb
- Méthode RTVFormatsCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode RTVFormatsCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RTVFormatsCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caaa1df508e1a448de3851d408f9aad5ac94d957
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523205"
---
# <a name="id3dx12pipelineparsercallbacksrtvformatscb-method"></a><span data-ttu-id="2752c-106">ID3DX12PipelineParserCallbacks :: RTVFormatsCb, méthode</span><span class="sxs-lookup"><span data-stu-id="2752c-106">ID3DX12PipelineParserCallbacks::RTVFormatsCb method</span></span>

<span data-ttu-id="2752c-107">Appelle le rappel de sous-objet du tableau de format de la cible de rendu d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="2752c-107">Calls the render target format array subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="2752c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2752c-108">Syntax</span></span>


```C++
void RTVFormatsCb(
  [ref] const D3D12_RT_FORMAT_ARRAY &RTVFormats
);
```



## <a name="parameters"></a><span data-ttu-id="2752c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2752c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2752c-110">*RTVFormats* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="2752c-110">*RTVFormats* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="2752c-111">Type : **const [**D3D12 \_ RT \_ , \_ tableau**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)**</span><span class="sxs-lookup"><span data-stu-id="2752c-111">Type: **const [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)**</span></span>

<span data-ttu-id="2752c-112">Détails du sous-objet du tableau de format de la cible de rendu analysé à partir d’un flux d’État du pipeline.</span><span class="sxs-lookup"><span data-stu-id="2752c-112">Details of the render target format array subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2752c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2752c-113">Return value</span></span>

<span data-ttu-id="2752c-114">Retourne la valeur Nothing.</span><span class="sxs-lookup"><span data-stu-id="2752c-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="2752c-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2752c-115">Requirements</span></span>



| <span data-ttu-id="2752c-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2752c-116">Requirement</span></span> | <span data-ttu-id="2752c-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="2752c-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2752c-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="2752c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="2752c-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="2752c-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="2752c-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2752c-120">Library</span></span><br/> | <dl> <span data-ttu-id="2752c-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2752c-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="2752c-122">DLL</span><span class="sxs-lookup"><span data-stu-id="2752c-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="2752c-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2752c-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2752c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2752c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2752c-125">Interfaces d’assistance pour Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="2752c-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="2752c-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="2752c-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="2752c-127">**\_Tableau de \_ format D3D12 RT \_**</span><span class="sxs-lookup"><span data-stu-id="2752c-127">**D3D12\_RT\_FORMAT\_ARRAY**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)
</dt> </dl>

 

 





