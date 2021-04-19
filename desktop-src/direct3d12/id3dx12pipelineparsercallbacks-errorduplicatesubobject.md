---
title: Méthode ID3DX12PipelineParserCallbacks ErrorDuplicateSubobject (D3DX12. h)
description: Appelle le rappel d’erreur de sous-objet dupliqué d’un objet qui implémente cette interface.
ms.assetid: 625C72C4-7BFB-4DAD-8D39-EDDBC7189499
keywords:
- Méthode ErrorDuplicateSubobject
- Méthode ErrorDuplicateSubobject, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode ErrorDuplicateSubobject
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.ErrorDuplicateSubobject
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43b00dae4675ff05a43e566a8ead815ea24f6c16
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525894"
---
# <a name="id3dx12pipelineparsercallbackserrorduplicatesubobject-method"></a><span data-ttu-id="2c803-106">ID3DX12PipelineParserCallbacks :: ErrorDuplicateSubobject, méthode</span><span class="sxs-lookup"><span data-stu-id="2c803-106">ID3DX12PipelineParserCallbacks::ErrorDuplicateSubobject method</span></span>

<span data-ttu-id="2c803-107">Appelle le rappel d’erreur de sous-objet dupliqué d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="2c803-107">Calls the duplicate subobject error callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c803-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2c803-108">Syntax</span></span>


```C++
void ErrorDuplicateSubobject(
   D3D12_PIPELINE_STATE_SUBOBJECT_TYPE DuplicateType
);
```



## <a name="parameters"></a><span data-ttu-id="2c803-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2c803-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c803-110">*DuplicateType*</span><span class="sxs-lookup"><span data-stu-id="2c803-110">*DuplicateType*</span></span> 
</dt> <dd>

<span data-ttu-id="2c803-111">Type : **[ **\_ type de \_ \_ \_ sous-objet état du pipeline D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)**</span><span class="sxs-lookup"><span data-stu-id="2c803-111">Type: **[**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)**</span></span>

<span data-ttu-id="2c803-112">Type de sous-objet qui a été dupliqué.</span><span class="sxs-lookup"><span data-stu-id="2c803-112">The subobject type that was duplicated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c803-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2c803-113">Return value</span></span>

<span data-ttu-id="2c803-114">Retourne la valeur Nothing.</span><span class="sxs-lookup"><span data-stu-id="2c803-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c803-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c803-115">Requirements</span></span>



| <span data-ttu-id="2c803-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c803-116">Requirement</span></span> | <span data-ttu-id="2c803-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c803-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2c803-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="2c803-118">Header</span></span><br/>  | <dl> <span data-ttu-id="2c803-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c803-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="2c803-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2c803-120">Library</span></span><br/> | <dl> <span data-ttu-id="2c803-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2c803-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="2c803-122">DLL</span><span class="sxs-lookup"><span data-stu-id="2c803-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="2c803-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c803-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c803-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c803-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c803-125">Interfaces d’assistance pour Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="2c803-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="2c803-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="2c803-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="2c803-127">**\_Type de \_ \_ sous-objet état \_ du pipeline D3D12**</span><span class="sxs-lookup"><span data-stu-id="2c803-127">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

