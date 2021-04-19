---
title: Méthode ID3DX12PipelineParserCallbacks StreamOutputCb (D3DX12. h)
description: Appelle le rappel de sortie de flux de sous-objet d’un objet qui implémente cette interface.
ms.assetid: 93447ABE-A942-4562-A532-600EC63072DA
keywords:
- Méthode StreamOutputCb
- Méthode StreamOutputCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode StreamOutputCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.StreamOutputCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae32f084edd2b6af374aa9b1cac4e563ef8a2eb6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535788"
---
# <a name="id3dx12pipelineparsercallbacksstreamoutputcb-method"></a><span data-ttu-id="1abbc-106">ID3DX12PipelineParserCallbacks :: StreamOutputCb, méthode</span><span class="sxs-lookup"><span data-stu-id="1abbc-106">ID3DX12PipelineParserCallbacks::StreamOutputCb method</span></span>

<span data-ttu-id="1abbc-107">Appelle le rappel de sortie de flux de sous-objet d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="1abbc-107">Calls the stream output description subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="1abbc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1abbc-108">Syntax</span></span>


```C++
void StreamOutputCb(
  [ref] const D3D12_STREAM_OUTPUT_DESC &StreamOutput
);
```



## <a name="parameters"></a><span data-ttu-id="1abbc-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1abbc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1abbc-110">*StreamOutput* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="1abbc-110">*StreamOutput* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="1abbc-111">Type : **const [**D3D12 \_ flux de \_ sortie \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)**</span><span class="sxs-lookup"><span data-stu-id="1abbc-111">Type: **const [**D3D12\_STREAM\_OUTPUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)**</span></span>

<span data-ttu-id="1abbc-112">Détails du sous-objet de description de sortie de flux analysé à partir d’un flux d’état de pipeline.</span><span class="sxs-lookup"><span data-stu-id="1abbc-112">Details of the stream output description subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1abbc-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1abbc-113">Return value</span></span>

<span data-ttu-id="1abbc-114">Retourne la valeur Nothing.</span><span class="sxs-lookup"><span data-stu-id="1abbc-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="1abbc-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1abbc-115">Requirements</span></span>



| <span data-ttu-id="1abbc-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1abbc-116">Requirement</span></span> | <span data-ttu-id="1abbc-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="1abbc-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1abbc-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="1abbc-118">Header</span></span><br/>  | <dl> <span data-ttu-id="1abbc-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="1abbc-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="1abbc-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1abbc-120">Library</span></span><br/> | <dl> <span data-ttu-id="1abbc-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1abbc-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="1abbc-122">DLL</span><span class="sxs-lookup"><span data-stu-id="1abbc-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="1abbc-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1abbc-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1abbc-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1abbc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1abbc-125">Interfaces d’assistance pour Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="1abbc-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="1abbc-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="1abbc-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="1abbc-127">**Description de la \_ sortie du flux D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1abbc-127">**D3D12\_STREAM\_OUTPUT\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)
</dt> </dl>

 

 





