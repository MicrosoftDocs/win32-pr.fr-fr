---
title: D3DX12ParsePipelineStream, fonction (D3dx12. h)
description: Analyse une description du flux d’État du pipeline, en appelant un rappel défini par l’utilisateur pour chaque instance de sous-objet analysée.
ms.assetid: BE4E8CC4-1E1F-4FE8-B109-05FAF93EB620
keywords:
- D3DX12ParsePipelineStream fonction)
topic_type:
- apiref
api_name:
- D3DX12ParsePipelineStream
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6778c29793f01ff7f1e5fd6424fb6795a29e64c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106520307"
---
# <a name="d3dx12parsepipelinestream-function"></a><span data-ttu-id="86158-104">D3DX12ParsePipelineStream fonction)</span><span class="sxs-lookup"><span data-stu-id="86158-104">D3DX12ParsePipelineStream function</span></span>

<span data-ttu-id="86158-105">Analyse une description du flux d’État du pipeline, en appelant un rappel défini par l’utilisateur pour chaque instance de sous-objet analysée.</span><span class="sxs-lookup"><span data-stu-id="86158-105">Parses a pipeline state stream description, calling a user-defined callback for each subobject instance parsed.</span></span>

## <a name="syntax"></a><span data-ttu-id="86158-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86158-106">Syntax</span></span>


```C++
HRESULT inline D3DX12ParsePipelineStream(
   const D3D12_PIPELINE_STATE_STREAM_DESC &Desc,
         ID3DX12PipelineParserCallbacks   *pCallbacks
);
```



## <a name="parameters"></a><span data-ttu-id="86158-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="86158-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86158-108">*Description* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="86158-108">*Desc* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="86158-109">Type : **const [**D3D12 \_ pipeline d’état de pipeline \_ \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc)**</span><span class="sxs-lookup"><span data-stu-id="86158-109">Type: **const [**D3D12\_PIPELINE\_STATE\_STREAM\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc)**</span></span>

<span data-ttu-id="86158-110">Description du flux d’état de pipeline à analyser.</span><span class="sxs-lookup"><span data-stu-id="86158-110">The pipeline state stream description to parse.</span></span>

</dd> <dt>

<span data-ttu-id="86158-111">*pCallbacks*</span><span class="sxs-lookup"><span data-stu-id="86158-111">*pCallbacks*</span></span> 
</dt> <dd>

<span data-ttu-id="86158-112">Type : **[ **ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)\***</span><span class="sxs-lookup"><span data-stu-id="86158-112">Type: **[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)\***</span></span>

<span data-ttu-id="86158-113">Structure qui spécifie les rappels à appeler pour chaque type de sous-objet et les rappels supplémentaires à appeler en cas d’erreur d’analyse.</span><span class="sxs-lookup"><span data-stu-id="86158-113">A structure that specifies the callbacks to call for each subobject type and additional callbacks to call in the event of a parsing error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86158-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="86158-114">Return value</span></span>

<span data-ttu-id="86158-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="86158-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="86158-116">Cette méthode retourne une erreur HRESULT réussie (**S \_ OK** ou **E \_ INVALIDARG** si un type de sous-objet inconnu est rencontré, si la description du flux est vide, null ou contient des sous-objets en double (y compris des sous-objets dérivés) ou si *pCallbacks* a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="86158-116">This method returns an HRESULT success (**S\_OK** or **E\_INVALIDARG** error if an unknown subobject type is encountered, if the stream description is empty, null, or contains duplicate subobjects (including derived subobjects), or if *pCallbacks* is null.</span></span> <span data-ttu-id="86158-117">Dans chaque cas où E \_ INVALIDARG est retourné, un rappel correspondant est d’abord appelé.</span><span class="sxs-lookup"><span data-stu-id="86158-117">In each case that E\_INVALIDARG is returned, a corresponding callback is first called.</span></span>

## <a name="requirements"></a><span data-ttu-id="86158-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86158-118">Requirements</span></span>



| <span data-ttu-id="86158-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="86158-119">Requirement</span></span> | <span data-ttu-id="86158-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="86158-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="86158-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="86158-121">Header</span></span><br/>  | <dl> <span data-ttu-id="86158-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="86158-122"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="86158-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="86158-123">Library</span></span><br/> | <dl> <span data-ttu-id="86158-124"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86158-124"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="86158-125">DLL</span><span class="sxs-lookup"><span data-stu-id="86158-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="86158-126"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86158-126"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86158-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86158-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86158-128">Fonctions d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="86158-128">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





