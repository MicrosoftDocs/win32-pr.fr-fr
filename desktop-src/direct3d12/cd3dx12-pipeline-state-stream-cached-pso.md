---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO (D3dx12. h)
description: Structure d’assistance utilisée pour décrire un PSO mis en cache comme un objet unique approprié pour une description de flux.
ms.assetid: 86CDC60A-275D-4B71-BE6D-C863C72E9C05
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78ddb223dfd2baa7bc6bee1b5a36950fc47d65d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539427"
---
# <a name="cd3dx12_pipeline_state_stream_cached_pso-structure"></a><span data-ttu-id="7a8ad-104">CD3DX12 \_ - \_ \_ structure d' \_ PSO mise en cache de flux d’état de pipeline \_</span><span class="sxs-lookup"><span data-stu-id="7a8ad-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO structure</span></span>

<span data-ttu-id="7a8ad-105">Structure d’assistance utilisée pour décrire un PSO mis en cache comme un objet unique approprié pour une description de flux.</span><span class="sxs-lookup"><span data-stu-id="7a8ad-105">A helper structure used to describe a cached PSO as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a8ad-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7a8ad-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO {
                                           CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO;
                                           CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO(D3D12_CACHED_PIPELINE_STATE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO operator=(D3D12_CACHED_PIPELINE_STATE const& i);
                                           operator D3D12_CACHED_PIPELINE_STATE() const;
};
```



## <a name="members"></a><span data-ttu-id="7a8ad-107">Membres</span><span class="sxs-lookup"><span data-stu-id="7a8ad-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="7a8ad-108">**\_Flux d' \_ État du pipeline CD3DX12 \_ \_ mis en cache \_**</span><span class="sxs-lookup"><span data-stu-id="7a8ad-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO**</span></span>
</dt> <dd>

<span data-ttu-id="7a8ad-109">Crée une nouvelle instance non initialisée d’un \_ flux d’état de pipeline CD3DX12 \_ \_ \_ mis en cache pour un objet \_ PSO.</span><span class="sxs-lookup"><span data-stu-id="7a8ad-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO.</span></span>

</dd> <dt>

<span data-ttu-id="7a8ad-110">**\_Flux d' \_ État de pipeline CD3DX12 \_ \_ PSO mis en cache \_ (D3D12 d' \_ État de pipeline mis en cache \_ \_ const &i)**</span><span class="sxs-lookup"><span data-stu-id="7a8ad-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO(D3D12\_CACHED\_PIPELINE\_STATE const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="7a8ad-111">Crée une nouvelle instance d’un \_ flux d’état de pipeline CD3DX12 \_ \_ \_ mis en cache \_ PSO, initialisé avec un type de sous-objet de **type de sous-objet d’état de \_ pipeline D3D12 \_ \_ \_ \_ mis en cache \_ PSO** et des données de sous-objet copiées à partir de *i*, une structure d' [**\_ \_ \_ État de pipeline mise en cache D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state) .</span><span class="sxs-lookup"><span data-stu-id="7a8ad-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_CACHED\_PSO** and subobject data copied from *i*, a [**D3D12\_CACHED\_PIPELINE\_STATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7a8ad-112">**Operator = (D3D12 d' \_ État du pipeline mis en cache \_ \_ const& i)**</span><span class="sxs-lookup"><span data-stu-id="7a8ad-112">**operator=(D3D12\_CACHED\_PIPELINE\_STATE const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="7a8ad-113">Opérateur d’assignation de copie.</span><span class="sxs-lookup"><span data-stu-id="7a8ad-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="7a8ad-114">**D3D12 \_ \_ de pipeline \_ () const d’opérateur () const**</span><span class="sxs-lookup"><span data-stu-id="7a8ad-114">**operator D3D12\_CACHED\_PIPELINE\_STATE() const**</span></span>
</dt> <dd>

<span data-ttu-id="7a8ad-115">Conversion implicite en structure d' [**\_ \_ \_ État de pipeline mise en cache D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state) .</span><span class="sxs-lookup"><span data-stu-id="7a8ad-115">Implicit conversion to a [**D3D12\_CACHED\_PIPELINE\_STATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7a8ad-116">Notes</span><span class="sxs-lookup"><span data-stu-id="7a8ad-116">Remarks</span></span>

<span data-ttu-id="7a8ad-117">\_ \_ Flux d’état de pipeline CD3DX12 \_ \_ , PSO mis en cache \_ est une spécialisation typedef du modèle de sous- [**objet de flux d' \_ État de pipeline \_ \_ \_ CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) , et est défini comme suit :</span><span class="sxs-lookup"><span data-stu-id="7a8ad-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_CACHED_PIPELINE_STATE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_CACHED_PSO>
    CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO;
          
```



## <a name="requirements"></a><span data-ttu-id="7a8ad-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a8ad-118">Requirements</span></span>



| <span data-ttu-id="7a8ad-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a8ad-119">Requirement</span></span> | <span data-ttu-id="7a8ad-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a8ad-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7a8ad-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="7a8ad-121">Header</span></span><br/> | <dl> <span data-ttu-id="7a8ad-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a8ad-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a8ad-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a8ad-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a8ad-124">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="7a8ad-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="7a8ad-125">**Sous \_ - \_ \_ objet de flux d’État du pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="7a8ad-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="7a8ad-126">**\_Type de \_ \_ sous-objet état \_ du pipeline D3D12**</span><span class="sxs-lookup"><span data-stu-id="7a8ad-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

