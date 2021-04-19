---
title: Méthode ID3DX12PipelineParserCallbacks SampleMaskCb (D3DX12. h)
description: Appelle l’exemple de rappel de sous-objet de masque d’un objet qui implémente cette interface.
ms.assetid: 4D729414-1E04-407B-B32F-ECE1EA9FF414
keywords:
- Méthode SampleMaskCb
- Méthode SampleMaskCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode SampleMaskCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.SampleMaskCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0124b228056089e21c078ffce25ce59eef0e3dee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525853"
---
# <a name="id3dx12pipelineparsercallbackssamplemaskcb-method"></a><span data-ttu-id="688e1-106">ID3DX12PipelineParserCallbacks :: SampleMaskCb, méthode</span><span class="sxs-lookup"><span data-stu-id="688e1-106">ID3DX12PipelineParserCallbacks::SampleMaskCb method</span></span>

<span data-ttu-id="688e1-107">Appelle l’exemple de rappel de sous-objet de masque d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="688e1-107">Calls the sample mask subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="688e1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="688e1-108">Syntax</span></span>


```C++
void SampleMaskCb(
   
        UINT
           SampleMask
);
```



## <a name="parameters"></a><span data-ttu-id="688e1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="688e1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="688e1-110">*SampleMask*</span><span class="sxs-lookup"><span data-stu-id="688e1-110">*SampleMask*</span></span> 
</dt> <dd>

<span data-ttu-id="688e1-111">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="688e1-111">Type: **UINT**</span></span>

<span data-ttu-id="688e1-112">Détails de l’exemple de sous-objet de masque analysé à partir d’un flux d’état de pipeline.</span><span class="sxs-lookup"><span data-stu-id="688e1-112">Details of the sample mask subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="688e1-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="688e1-113">Return value</span></span>

<span data-ttu-id="688e1-114">Retourne la valeur Nothing.</span><span class="sxs-lookup"><span data-stu-id="688e1-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="688e1-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="688e1-115">Requirements</span></span>



| <span data-ttu-id="688e1-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="688e1-116">Requirement</span></span> | <span data-ttu-id="688e1-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="688e1-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="688e1-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="688e1-118">Header</span></span><br/>  | <dl> <span data-ttu-id="688e1-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="688e1-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="688e1-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="688e1-120">Library</span></span><br/> | <dl> <span data-ttu-id="688e1-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="688e1-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="688e1-122">DLL</span><span class="sxs-lookup"><span data-stu-id="688e1-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="688e1-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="688e1-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="688e1-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="688e1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="688e1-125">Interfaces d’assistance pour Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="688e1-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="688e1-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="688e1-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





