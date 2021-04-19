---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS (D3dx12. h)
description: Structure d’assistance utilisée pour décrire les formats de cible de rendu sous la forme d’un objet unique approprié pour une description de flux.
ms.assetid: 8C5C2279-7985-41B6-87EA-ABB0007DAFD4
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a64f051ba56edf176c87bbc99551cd974fc3a43
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535164"
---
# <a name="cd3dx12_pipeline_state_stream_render_target_formats-structure"></a><span data-ttu-id="1f80b-104">\_Structure de \_ \_ \_ \_ formats cibles de rendu du flux \_ d’État du pipeline CD3DX12</span><span class="sxs-lookup"><span data-stu-id="1f80b-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS structure</span></span>

<span data-ttu-id="1f80b-105">Structure d’assistance utilisée pour décrire les formats de cible de rendu sous la forme d’un objet unique approprié pour une description de flux.</span><span class="sxs-lookup"><span data-stu-id="1f80b-105">A helper structure used to describe the render target formats as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f80b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f80b-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS {
                                                      CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS;
                                                      CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS(D3D12_RT_FORMAT_ARRAY const &i);
  CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS operator=(D3D12_RT_FORMAT_ARRAY const& i);
                                                      operator D3D12_RT_FORMAT_ARRAY() const;
};
```



## <a name="members"></a><span data-ttu-id="1f80b-107">Membres</span><span class="sxs-lookup"><span data-stu-id="1f80b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="1f80b-108">**\_ \_ \_ \_ Formats cibles de rendu du flux d' \_ état \_ du pipeline CD3DX12**</span><span class="sxs-lookup"><span data-stu-id="1f80b-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS**</span></span>
</dt> <dd>

<span data-ttu-id="1f80b-109">Crée une nouvelle instance non initialisée d’un \_ flux d’état de pipeline CD3DX12 \_ \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1f80b-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS.</span></span>

</dd> <dt>

<span data-ttu-id="1f80b-110">**\_ \_ Formats cibles de rendu du flux d’État du pipeline CD3DX12 \_ \_ \_ \_ (D3D12 \_ RT \_ format \_ const &i)**</span><span class="sxs-lookup"><span data-stu-id="1f80b-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS(D3D12\_RT\_FORMAT\_ARRAY const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="1f80b-111">Crée une nouvelle instance d’un flux de données d' \_ État de pipeline CD3DX12 \_ \_ \_ \_ \_ . les formats cibles sont initialisés avec un type de sous-objet de **type de sous-objet d’état de pipeline D3D12. les \_ \_ \_ \_ \_ \_ \_ formats cibles** et les données de sous-objet copiés à partir de *i*, une structure de [**\_ \_ \_ tableau de format D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .</span><span class="sxs-lookup"><span data-stu-id="1f80b-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_RENDER\_TARGET\_FORMATS** and subobject data copied from *i*, a [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1f80b-112">**Operator = (D3D12 \_ RT \_ format \_ tableau const& i)**</span><span class="sxs-lookup"><span data-stu-id="1f80b-112">**operator=(D3D12\_RT\_FORMAT\_ARRAY const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="1f80b-113">Opérateur d’assignation de copie.</span><span class="sxs-lookup"><span data-stu-id="1f80b-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="1f80b-114">**Operator D3D12 \_ RT \_ format \_ tableau () const**</span><span class="sxs-lookup"><span data-stu-id="1f80b-114">**operator D3D12\_RT\_FORMAT\_ARRAY() const**</span></span>
</dt> <dd>

<span data-ttu-id="1f80b-115">Conversion implicite en structure de [**\_ tableau de \_ format \_ D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .</span><span class="sxs-lookup"><span data-stu-id="1f80b-115">Implicit conversion to a [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1f80b-116">Notes</span><span class="sxs-lookup"><span data-stu-id="1f80b-116">Remarks</span></span>

<span data-ttu-id="1f80b-117">\_ \_ \_ \_ \_ \_ Les formats de cible de rendu du flux d’État du pipeline CD3DX12 sont une spécialisation typedef du modèle de sous- [**objet de flux d' \_ \_ état \_ \_ de pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) , et sont définis comme suit :</span><span class="sxs-lookup"><span data-stu-id="1f80b-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_RT_FORMAT_ARRAY, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_RENDER_TARGET_FORMATS>
    CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS;
          
```



## <a name="requirements"></a><span data-ttu-id="1f80b-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f80b-118">Requirements</span></span>



| <span data-ttu-id="1f80b-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f80b-119">Requirement</span></span> | <span data-ttu-id="1f80b-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f80b-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1f80b-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="1f80b-121">Header</span></span><br/> | <dl> <span data-ttu-id="1f80b-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f80b-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f80b-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f80b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f80b-124">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="1f80b-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="1f80b-125">**Sous \_ - \_ \_ objet de flux d’État du pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="1f80b-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="1f80b-126">**\_Type de \_ \_ sous-objet état \_ du pipeline D3D12**</span><span class="sxs-lookup"><span data-stu-id="1f80b-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

