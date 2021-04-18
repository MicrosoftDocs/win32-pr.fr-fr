---
title: Méthode ID3DX12PipelineParserCallbacks PSCb (D3DX12. h)
description: Appelle le rappel de sous-objet de nuanceur de pixels d’un objet qui implémente cette interface.
ms.assetid: 3397B018-C26A-426F-88BB-89013BACBEEA
keywords:
- Méthode PSCb
- Méthode PSCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode PSCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.PSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c972702c215556b953797a6e332f8e86c480b094
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522755"
---
# <a name="id3dx12pipelineparsercallbackspscb-method"></a><span data-ttu-id="d7c53-106">ID3DX12PipelineParserCallbacks ::P méthode SCb</span><span class="sxs-lookup"><span data-stu-id="d7c53-106">ID3DX12PipelineParserCallbacks::PSCb method</span></span>

<span data-ttu-id="d7c53-107">Appelle le rappel de sous-objet de nuanceur de pixels d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="d7c53-107">Calls the pixel shader subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7c53-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7c53-108">Syntax</span></span>


```C++
void PSCb(
  [ref] const D3D12_SHADER_BYTECODE &PS
);
```



## <a name="parameters"></a><span data-ttu-id="d7c53-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7c53-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7c53-110">*PS* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="d7c53-110">*PS* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="d7c53-111">Type : **const [**D3D12 \_ Shader \_ bytecode**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span><span class="sxs-lookup"><span data-stu-id="d7c53-111">Type: **const [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span></span>

<span data-ttu-id="d7c53-112">Détails du sous-objet de nuanceur de pixels analysé à partir d’un flux d’état de pipeline.</span><span class="sxs-lookup"><span data-stu-id="d7c53-112">Details of the pixel shader subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7c53-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d7c53-113">Return value</span></span>

<span data-ttu-id="d7c53-114">Retourne la valeur Nothing.</span><span class="sxs-lookup"><span data-stu-id="d7c53-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7c53-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7c53-115">Requirements</span></span>



| <span data-ttu-id="d7c53-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7c53-116">Requirement</span></span> | <span data-ttu-id="d7c53-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7c53-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d7c53-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="d7c53-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d7c53-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7c53-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="d7c53-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d7c53-120">Library</span></span><br/> | <dl> <span data-ttu-id="d7c53-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7c53-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="d7c53-122">DLL</span><span class="sxs-lookup"><span data-stu-id="d7c53-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="d7c53-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7c53-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7c53-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7c53-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7c53-125">Interfaces d’assistance pour Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="d7c53-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="d7c53-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="d7c53-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="d7c53-127">**\_Bytecode de nuanceur D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="d7c53-127">**D3D12\_SHADER\_BYTECODE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





