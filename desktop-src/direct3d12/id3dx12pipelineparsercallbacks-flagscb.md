---
title: Méthode ID3DX12PipelineParserCallbacks FlagsCb (D3DX12. h)
description: Appelle le rappel de sous-objet d’indicateurs d’un objet qui implémente cette interface.
ms.assetid: 81DD8CF3-87BA-4380-BECD-70A80580048A
keywords:
- Méthode FlagsCb
- Méthode FlagsCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode FlagsCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.FlagsCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f30ac5a0ca3a749144e263a1d993166b8e13ddac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523207"
---
# <a name="id3dx12pipelineparsercallbacksflagscb-method"></a><span data-ttu-id="476f7-106">ID3DX12PipelineParserCallbacks :: FlagsCb, méthode</span><span class="sxs-lookup"><span data-stu-id="476f7-106">ID3DX12PipelineParserCallbacks::FlagsCb method</span></span>

<span data-ttu-id="476f7-107">Appelle le rappel de sous-objet d’indicateurs d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="476f7-107">Calls the flags subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="476f7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="476f7-108">Syntax</span></span>


```C++
void FlagsCb(
   D3D12_PIPELINE_STATE_FLAGS Flags
);
```



## <a name="parameters"></a><span data-ttu-id="476f7-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="476f7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="476f7-110">*Indicateurs*</span><span class="sxs-lookup"><span data-stu-id="476f7-110">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="476f7-111">Type : **[ **\_ indicateurs d' \_ état \_ du pipeline D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)**</span><span class="sxs-lookup"><span data-stu-id="476f7-111">Type: **[**D3D12\_PIPELINE\_STATE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)**</span></span>

<span data-ttu-id="476f7-112">Détails du sous-objet Flags analysé à partir d’un flux d’État du pipeline.</span><span class="sxs-lookup"><span data-stu-id="476f7-112">Details of the flags subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="476f7-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="476f7-113">Return value</span></span>

<span data-ttu-id="476f7-114">Retourne la valeur Nothing.</span><span class="sxs-lookup"><span data-stu-id="476f7-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="476f7-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="476f7-115">Requirements</span></span>



| <span data-ttu-id="476f7-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="476f7-116">Requirement</span></span> | <span data-ttu-id="476f7-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="476f7-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="476f7-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="476f7-118">Header</span></span><br/>  | <dl> <span data-ttu-id="476f7-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="476f7-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="476f7-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="476f7-120">Library</span></span><br/> | <dl> <span data-ttu-id="476f7-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="476f7-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="476f7-122">DLL</span><span class="sxs-lookup"><span data-stu-id="476f7-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="476f7-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="476f7-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="476f7-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="476f7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="476f7-125">Interfaces d’assistance pour Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="476f7-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="476f7-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="476f7-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="476f7-127">**\_Indicateurs d’État du pipeline D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="476f7-127">**D3D12\_PIPELINE\_STATE\_FLAGS**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)
</dt> </dl>

 

 





