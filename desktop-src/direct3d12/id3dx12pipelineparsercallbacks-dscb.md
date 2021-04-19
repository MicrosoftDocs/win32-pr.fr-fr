---
title: Méthode ID3DX12PipelineParserCallbacks DSCb (D3DX12. h)
description: Appelle le rappel de sous-objet de nuanceur de domaine d’un objet qui implémente cette interface.
ms.assetid: F4877211-4122-4418-9323-3F68B0BB3363
keywords:
- Méthode DSCb
- Méthode DSCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode DSCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.DSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cf5f68ca6e6e4891fa391a142d45a1496a42ede
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106543566"
---
# <a name="id3dx12pipelineparsercallbacksdscb-method"></a><span data-ttu-id="b1bce-106">ID3DX12PipelineParserCallbacks ::D méthode SCb</span><span class="sxs-lookup"><span data-stu-id="b1bce-106">ID3DX12PipelineParserCallbacks::DSCb method</span></span>

<span data-ttu-id="b1bce-107">Appelle le rappel de sous-objet de nuanceur de domaine d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="b1bce-107">Calls the domain shader subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1bce-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1bce-108">Syntax</span></span>


```C++
void DSCb(
  [ref] const D3D12_SHADER_BYTECODE &DS
);
```



## <a name="parameters"></a><span data-ttu-id="b1bce-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b1bce-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1bce-110">*Service d’annuaire* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="b1bce-110">*DS* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="b1bce-111">Type : **const [**D3D12 \_ Shader \_ bytecode**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span><span class="sxs-lookup"><span data-stu-id="b1bce-111">Type: **const [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span></span>

<span data-ttu-id="b1bce-112">Détails du sous-objet du nuanceur de domaine analysé à partir d’un flux d’État du pipeline.</span><span class="sxs-lookup"><span data-stu-id="b1bce-112">Details of the domain shader subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1bce-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b1bce-113">Return value</span></span>

<span data-ttu-id="b1bce-114">Retourne la valeur Nothing.</span><span class="sxs-lookup"><span data-stu-id="b1bce-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1bce-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b1bce-115">Requirements</span></span>



| <span data-ttu-id="b1bce-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b1bce-116">Requirement</span></span> | <span data-ttu-id="b1bce-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1bce-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b1bce-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="b1bce-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b1bce-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1bce-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="b1bce-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b1bce-120">Library</span></span><br/> | <dl> <span data-ttu-id="b1bce-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1bce-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="b1bce-122">DLL</span><span class="sxs-lookup"><span data-stu-id="b1bce-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="b1bce-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1bce-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1bce-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1bce-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1bce-125">Interfaces d’assistance pour Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="b1bce-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="b1bce-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="b1bce-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="b1bce-127">**\_Bytecode de nuanceur D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="b1bce-127">**D3D12\_SHADER\_BYTECODE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





