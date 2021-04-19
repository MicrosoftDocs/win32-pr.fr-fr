---
title: Méthode ID3DX12PipelineParserCallbacks VSCb (D3DX12. h)
description: Appelle le rappel de sous-objet de nuanceur vertex d’un objet qui implémente cette interface.
ms.assetid: 65A185B7-C790-4254-A3C5-EBBE9C38CA4E
keywords:
- Méthode VSCb
- Méthode VSCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode VSCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.VSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eef9ab27b2f9fd4b93190e2eea453397de297013
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527738"
---
# <a name="id3dx12pipelineparsercallbacksvscb-method"></a><span data-ttu-id="c5943-106">ID3DX12PipelineParserCallbacks :: VSCb, méthode</span><span class="sxs-lookup"><span data-stu-id="c5943-106">ID3DX12PipelineParserCallbacks::VSCb method</span></span>

<span data-ttu-id="c5943-107">Appelle le rappel de sous-objet de nuanceur vertex d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="c5943-107">Calls the vertex shader subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5943-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c5943-108">Syntax</span></span>


```C++
void VSCb(
  [ref] const D3D12_SHADER_BYTECODE &VS
);
```



## <a name="parameters"></a><span data-ttu-id="c5943-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c5943-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5943-110">*Vs* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="c5943-110">*VS* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="c5943-111">Type : **const [**D3D12 \_ Shader \_ bytecode**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span><span class="sxs-lookup"><span data-stu-id="c5943-111">Type: **const [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span></span>

<span data-ttu-id="c5943-112">Détails du sous-objet Vertex Shader analysé à partir d’un flux d’État du pipeline.</span><span class="sxs-lookup"><span data-stu-id="c5943-112">Details of the vertex shader subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5943-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c5943-113">Return value</span></span>

<span data-ttu-id="c5943-114">Retourne la valeur Nothing.</span><span class="sxs-lookup"><span data-stu-id="c5943-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5943-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5943-115">Requirements</span></span>



| <span data-ttu-id="c5943-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c5943-116">Requirement</span></span> | <span data-ttu-id="c5943-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5943-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c5943-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="c5943-118">Header</span></span><br/>  | <dl> <span data-ttu-id="c5943-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5943-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="c5943-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c5943-120">Library</span></span><br/> | <dl> <span data-ttu-id="c5943-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5943-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="c5943-122">DLL</span><span class="sxs-lookup"><span data-stu-id="c5943-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="c5943-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5943-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5943-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5943-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5943-125">Interfaces d’assistance pour Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="c5943-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="c5943-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="c5943-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="c5943-127">**\_Bytecode de nuanceur D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="c5943-127">**D3D12\_SHADER\_BYTECODE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





