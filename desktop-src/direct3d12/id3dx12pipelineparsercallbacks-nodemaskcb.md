---
title: Méthode ID3DX12PipelineParserCallbacks NodemaskCb (D3DX12. h)
description: Appelle le rappel de sous-objet nodemask d’un objet qui implémente cette interface.
ms.assetid: F5A408B7-A777-4BBC-A2A3-1BC3551E65ED
keywords:
- Méthode NodemaskCb
- Méthode NodemaskCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode NodemaskCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.NodemaskCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdf1cc03f60259c395ca8c459ddd5a308e3dcd6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106520304"
---
# <a name="id3dx12pipelineparsercallbacksnodemaskcb-method"></a><span data-ttu-id="d1fa3-106">ID3DX12PipelineParserCallbacks :: NodemaskCb, méthode</span><span class="sxs-lookup"><span data-stu-id="d1fa3-106">ID3DX12PipelineParserCallbacks::NodemaskCb method</span></span>

<span data-ttu-id="d1fa3-107">Appelle le rappel de sous-objet nodemask d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="d1fa3-107">Calls the nodemask subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1fa3-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1fa3-108">Syntax</span></span>


```C++
void NodemaskCb(
   
        UINT
       Nodemask
);
```



## <a name="parameters"></a><span data-ttu-id="d1fa3-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d1fa3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1fa3-110">*Nodemask*</span><span class="sxs-lookup"><span data-stu-id="d1fa3-110">*Nodemask*</span></span> 
</dt> <dd>

<span data-ttu-id="d1fa3-111">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="d1fa3-111">Type: **UINT**</span></span>

<span data-ttu-id="d1fa3-112">Détails du sous-objet nodemask analysé à partir d’un flux d’État du pipeline.</span><span class="sxs-lookup"><span data-stu-id="d1fa3-112">Details of the nodemask subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1fa3-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d1fa3-113">Return value</span></span>

<span data-ttu-id="d1fa3-114">Retourne la valeur Nothing.</span><span class="sxs-lookup"><span data-stu-id="d1fa3-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1fa3-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1fa3-115">Requirements</span></span>



| <span data-ttu-id="d1fa3-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1fa3-116">Requirement</span></span> | <span data-ttu-id="d1fa3-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1fa3-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d1fa3-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="d1fa3-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d1fa3-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1fa3-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="d1fa3-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d1fa3-120">Library</span></span><br/> | <dl> <span data-ttu-id="d1fa3-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1fa3-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="d1fa3-122">DLL</span><span class="sxs-lookup"><span data-stu-id="d1fa3-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="d1fa3-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1fa3-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1fa3-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1fa3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1fa3-125">Interfaces d’assistance pour Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="d1fa3-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="d1fa3-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="d1fa3-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





