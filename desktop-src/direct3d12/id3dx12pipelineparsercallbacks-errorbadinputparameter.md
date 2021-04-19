---
title: Méthode ID3DX12PipelineParserCallbacks ErrorBadInputParameter (D3DX12. h)
description: Appelle le rappel d’erreur de paramètre d’entrée incorrect d’un objet qui implémente cette interface.
ms.assetid: CB1F9A77-B120-4D72-99D3-16594E668520
keywords:
- Méthode ErrorBadInputParameter
- Méthode ErrorBadInputParameter, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode ErrorBadInputParameter
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.ErrorBadInputParameter
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5181e8d9fb83b7338adc3af5c0ce44aec1b447d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531351"
---
# <a name="id3dx12pipelineparsercallbackserrorbadinputparameter-method"></a><span data-ttu-id="c5bfd-106">ID3DX12PipelineParserCallbacks :: ErrorBadInputParameter, méthode</span><span class="sxs-lookup"><span data-stu-id="c5bfd-106">ID3DX12PipelineParserCallbacks::ErrorBadInputParameter method</span></span>

<span data-ttu-id="c5bfd-107">Appelle le rappel d’erreur de paramètre d’entrée incorrect d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="c5bfd-107">Calls the bad input parameter error callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5bfd-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c5bfd-108">Syntax</span></span>


```C++
void ErrorBadInputParameter(
   
        UINT
           ParameterIndex
);
```



## <a name="parameters"></a><span data-ttu-id="c5bfd-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c5bfd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5bfd-110">*ParameterIndex*</span><span class="sxs-lookup"><span data-stu-id="c5bfd-110">*ParameterIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="c5bfd-111">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="c5bfd-111">Type: **UINT**</span></span>

<span data-ttu-id="c5bfd-112">Position du paramètre qui contient une entrée incorrecte.</span><span class="sxs-lookup"><span data-stu-id="c5bfd-112">The position of the parameter that contains bad input.</span></span> <span data-ttu-id="c5bfd-113">Le paramètre le plus à gauche se trouve à la position 1, et non à la position 0.</span><span class="sxs-lookup"><span data-stu-id="c5bfd-113">The left-most parameter is at position 1, not position 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5bfd-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c5bfd-114">Return value</span></span>

<span data-ttu-id="c5bfd-115">Retourne la valeur Nothing.</span><span class="sxs-lookup"><span data-stu-id="c5bfd-115">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5bfd-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5bfd-116">Requirements</span></span>



| <span data-ttu-id="c5bfd-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c5bfd-117">Requirement</span></span> | <span data-ttu-id="c5bfd-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5bfd-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c5bfd-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="c5bfd-119">Header</span></span><br/>  | <dl> <span data-ttu-id="c5bfd-120"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5bfd-120"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="c5bfd-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c5bfd-121">Library</span></span><br/> | <dl> <span data-ttu-id="c5bfd-122"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5bfd-122"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="c5bfd-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c5bfd-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="c5bfd-124"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5bfd-124"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5bfd-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5bfd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5bfd-126">Interfaces d’assistance pour Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="c5bfd-126">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="c5bfd-127">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="c5bfd-127">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





