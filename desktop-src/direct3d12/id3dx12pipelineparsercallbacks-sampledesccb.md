---
title: Méthode ID3DX12PipelineParserCallbacks SampleDescCb (D3DX12. h)
description: Appelle l’exemple de rappel de sous-objet de description d’un objet qui implémente cette interface.
ms.assetid: 32F112D3-97B1-45C2-8744-9F27DC95C249
keywords:
- Méthode SampleDescCb
- Méthode SampleDescCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode SampleDescCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.SampleDescCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0644837720dd8c81dc1c7577a1d6506ebdf61c24
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106524841"
---
# <a name="id3dx12pipelineparsercallbackssampledesccb-method"></a><span data-ttu-id="c8bcc-106">ID3DX12PipelineParserCallbacks :: SampleDescCb, méthode</span><span class="sxs-lookup"><span data-stu-id="c8bcc-106">ID3DX12PipelineParserCallbacks::SampleDescCb method</span></span>

<span data-ttu-id="c8bcc-107">Appelle l’exemple de rappel de sous-objet de description d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="c8bcc-107">Calls the sample description subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8bcc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c8bcc-108">Syntax</span></span>


```C++
void SampleDescCb(
  [ref] const DXGI_SAMPLE_DESC &SampleDesc
);
```



## <a name="parameters"></a><span data-ttu-id="c8bcc-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c8bcc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8bcc-110">*SampleDesc* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="c8bcc-110">*SampleDesc* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="c8bcc-111">Type : **const [**dxgi \_ exemple \_ desc**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc)**</span><span class="sxs-lookup"><span data-stu-id="c8bcc-111">Type: **const [**DXGI\_SAMPLE\_DESC**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc)**</span></span>

<span data-ttu-id="c8bcc-112">Détails de l’exemple de sous-objet Description analysé à partir d’un flux d’État du pipeline.</span><span class="sxs-lookup"><span data-stu-id="c8bcc-112">Details of the sample description subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8bcc-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c8bcc-113">Return value</span></span>

<span data-ttu-id="c8bcc-114">Retourne la valeur Nothing.</span><span class="sxs-lookup"><span data-stu-id="c8bcc-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8bcc-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c8bcc-115">Requirements</span></span>



| <span data-ttu-id="c8bcc-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c8bcc-116">Requirement</span></span> | <span data-ttu-id="c8bcc-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8bcc-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c8bcc-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="c8bcc-118">Header</span></span><br/>  | <dl> <span data-ttu-id="c8bcc-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8bcc-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="c8bcc-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c8bcc-120">Library</span></span><br/> | <dl> <span data-ttu-id="c8bcc-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8bcc-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="c8bcc-122">DLL</span><span class="sxs-lookup"><span data-stu-id="c8bcc-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="c8bcc-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8bcc-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8bcc-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8bcc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8bcc-125">Interfaces d’assistance pour Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="c8bcc-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="c8bcc-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="c8bcc-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="c8bcc-127">**\_exemple dxgi \_ desc**</span><span class="sxs-lookup"><span data-stu-id="c8bcc-127">**DXGI\_SAMPLE\_DESC**</span></span>](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc)
</dt> </dl>

 

