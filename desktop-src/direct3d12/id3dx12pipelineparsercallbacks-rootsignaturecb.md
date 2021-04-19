---
title: Méthode ID3DX12PipelineParserCallbacks RootSignatureCb (D3DX12. h)
description: Appelle le rappel de sous-objet de signature racine d’un objet qui implémente cette interface.
ms.assetid: FD467001-41B1-4A73-8E54-12C6B5EEAC3E
keywords:
- Méthode RootSignatureCb
- Méthode RootSignatureCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode RootSignatureCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RootSignatureCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78160ff1e61432a0711876934215ff15afb918de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106545262"
---
# <a name="id3dx12pipelineparsercallbacksrootsignaturecb-method"></a><span data-ttu-id="f5f12-106">ID3DX12PipelineParserCallbacks :: RootSignatureCb, méthode</span><span class="sxs-lookup"><span data-stu-id="f5f12-106">ID3DX12PipelineParserCallbacks::RootSignatureCb method</span></span>

<span data-ttu-id="f5f12-107">Appelle le rappel de sous-objet de signature racine d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="f5f12-107">Calls the root signature subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5f12-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5f12-108">Syntax</span></span>


```C++
void RootSignatureCb(
   ID3D12RootSignature *RootSignature
);
```



## <a name="parameters"></a><span data-ttu-id="f5f12-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5f12-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5f12-110">*RootSignature*</span><span class="sxs-lookup"><span data-stu-id="f5f12-110">*RootSignature*</span></span> 
</dt> <dd>

<span data-ttu-id="f5f12-111">Type : **[ **ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)\***</span><span class="sxs-lookup"><span data-stu-id="f5f12-111">Type: **[**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)\***</span></span>

<span data-ttu-id="f5f12-112">Détails du sous-objet de signature racine analysé à partir d’un flux d’État du pipeline.</span><span class="sxs-lookup"><span data-stu-id="f5f12-112">Details of the root signature subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5f12-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f5f12-113">Return value</span></span>

<span data-ttu-id="f5f12-114">Retourne la valeur Nothing.</span><span class="sxs-lookup"><span data-stu-id="f5f12-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5f12-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5f12-115">Requirements</span></span>



| <span data-ttu-id="f5f12-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5f12-116">Requirement</span></span> | <span data-ttu-id="f5f12-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5f12-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f5f12-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="f5f12-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f5f12-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5f12-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="f5f12-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f5f12-120">Library</span></span><br/> | <dl> <span data-ttu-id="f5f12-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5f12-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="f5f12-122">DLL</span><span class="sxs-lookup"><span data-stu-id="f5f12-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="f5f12-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5f12-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5f12-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5f12-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5f12-125">Interfaces d’assistance pour Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="f5f12-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="f5f12-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="f5f12-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="f5f12-127">**ID3D12RootSignature**</span><span class="sxs-lookup"><span data-stu-id="f5f12-127">**ID3D12RootSignature**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)
</dt> </dl>

 

