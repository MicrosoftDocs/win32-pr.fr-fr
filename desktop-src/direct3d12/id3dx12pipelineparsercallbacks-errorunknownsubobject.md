---
title: Méthode ID3DX12PipelineParserCallbacks ErrorUnknownSubobject (D3DX12. h)
description: Appelle le rappel d’erreur de sous-objet inconnu d’un objet qui implémente cette interface.
ms.assetid: 612D7C44-4DC5-4DEA-B369-09C27123D45E
keywords:
- Méthode ErrorUnknownSubobject
- Méthode ErrorUnknownSubobject, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode ErrorUnknownSubobject
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.ErrorUnknownSubobject
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e294e3face085c5298f3cc624d7c0ef70dcf865
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535193"
---
# <a name="id3dx12pipelineparsercallbackserrorunknownsubobject-method"></a><span data-ttu-id="4aecc-106">ID3DX12PipelineParserCallbacks :: ErrorUnknownSubobject, méthode</span><span class="sxs-lookup"><span data-stu-id="4aecc-106">ID3DX12PipelineParserCallbacks::ErrorUnknownSubobject method</span></span>

<span data-ttu-id="4aecc-107">Appelle le rappel d’erreur de sous-objet inconnu d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="4aecc-107">Calls the unknown subobject error callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="4aecc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4aecc-108">Syntax</span></span>


```C++
void ErrorUnknownSubobject(
   
        UINT
           UnknownTypeValue
);
```



## <a name="parameters"></a><span data-ttu-id="4aecc-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4aecc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4aecc-110">*UnknownTypeValue*</span><span class="sxs-lookup"><span data-stu-id="4aecc-110">*UnknownTypeValue*</span></span> 
</dt> <dd>

<span data-ttu-id="4aecc-111">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="4aecc-111">Type: **UINT**</span></span>

<span data-ttu-id="4aecc-112">Type de sous-objet non reconnu du sous-objet tenté.</span><span class="sxs-lookup"><span data-stu-id="4aecc-112">The unrecognized subobject type of the attempted subobject.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4aecc-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4aecc-113">Return value</span></span>

<span data-ttu-id="4aecc-114">Retourne la valeur Nothing.</span><span class="sxs-lookup"><span data-stu-id="4aecc-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="4aecc-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4aecc-115">Requirements</span></span>



| <span data-ttu-id="4aecc-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4aecc-116">Requirement</span></span> | <span data-ttu-id="4aecc-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="4aecc-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4aecc-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="4aecc-118">Header</span></span><br/>  | <dl> <span data-ttu-id="4aecc-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="4aecc-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="4aecc-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4aecc-120">Library</span></span><br/> | <dl> <span data-ttu-id="4aecc-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4aecc-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="4aecc-122">DLL</span><span class="sxs-lookup"><span data-stu-id="4aecc-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="4aecc-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4aecc-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4aecc-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4aecc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4aecc-125">Interfaces d’assistance pour Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="4aecc-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="4aecc-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="4aecc-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





