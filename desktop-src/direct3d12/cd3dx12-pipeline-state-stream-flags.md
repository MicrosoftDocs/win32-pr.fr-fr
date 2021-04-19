---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_FLAGS (D3dx12. h)
description: Structure d’assistance utilisée pour décrire les indicateurs d’état de pipeline sous la forme d’un objet unique approprié pour une description de flux.
ms.assetid: EF67936B-315A-4B3F-9E07-7CF4C5EE47CF
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_FLAGS
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_FLAGS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 034f4a63c774ca41f28fbe9e6c2945fddee47c4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106520354"
---
# <a name="cd3dx12_pipeline_state_stream_flags-structure"></a><span data-ttu-id="60e07-104">\_Structure d' \_ \_ indicateurs du flux d’État du pipeline CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="60e07-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS structure</span></span>

<span data-ttu-id="60e07-105">Structure d’assistance utilisée pour décrire les indicateurs d’état de pipeline sous la forme d’un objet unique approprié pour une description de flux.</span><span class="sxs-lookup"><span data-stu-id="60e07-105">A helper structure used to describe pipeline state flags as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="60e07-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60e07-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_FLAGS {
                                      CD3DX12_PIPELINE_STATE_STREAM_FLAGS;
                                      CD3DX12_PIPELINE_STATE_STREAM_FLAGS(D3D12_PIPELINE_STATE_FLAGS const &i);
  CD3DX12_PIPELINE_STATE_STREAM_FLAGS operator=(D3D12_PIPELINE_STATE_FLAGS const& i);
                                      operator D3D12_PIPELINE_STATE_FLAGS() const;
};
```



## <a name="members"></a><span data-ttu-id="60e07-107">Membres</span><span class="sxs-lookup"><span data-stu-id="60e07-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="60e07-108">**\_Indicateurs du \_ flux d’État du PIPELINe CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="60e07-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS**</span></span>
</dt> <dd>

<span data-ttu-id="60e07-109">Crée une nouvelle instance non initialisée d’un \_ indicateur de flux d’état de pipeline CD3DX12 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="60e07-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS.</span></span>

</dd> <dt>

<span data-ttu-id="60e07-110">**Indicateurs de flux d’État du pipeline CD3DX12 \_ \_ \_ \_ ( \_ indicateurs d’état de pipeline D3D12 \_ \_ const &i)**</span><span class="sxs-lookup"><span data-stu-id="60e07-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS(D3D12\_PIPELINE\_STATE\_FLAGS const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="60e07-111">Crée une nouvelle instance d’indicateurs de \_ flux d’état de pipeline CD3DX12 \_ \_ \_ , initialisée avec un type de sous-objet des indicateurs de type de sous-objet d' **État de pipeline D3D12 et des données de \_ \_ \_ \_ sous \_** -objet copiées à partir de *i*, une structure d' [**indicateurs d' \_ \_ état \_ de pipeline D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags) .</span><span class="sxs-lookup"><span data-stu-id="60e07-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_FLAGS** and subobject data copied from *i*, a [**D3D12\_PIPELINE\_STATE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags) structure.</span></span>

</dd> <dt>

<span data-ttu-id="60e07-112">**Operator = (D3D12 \_ pipeline \_ State \_ flags const& i)**</span><span class="sxs-lookup"><span data-stu-id="60e07-112">**operator=(D3D12\_PIPELINE\_STATE\_FLAGS const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="60e07-113">Opérateur d’assignation de copie.</span><span class="sxs-lookup"><span data-stu-id="60e07-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="60e07-114">**D3D12 \_ , opérateur \_ indicateurs d’état de pipeline \_ () const**</span><span class="sxs-lookup"><span data-stu-id="60e07-114">**operator D3D12\_PIPELINE\_STATE\_FLAGS() const**</span></span>
</dt> <dd>

<span data-ttu-id="60e07-115">Conversion implicite en une structure d' [**\_ indicateurs d' \_ état \_ de pipeline D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags) .</span><span class="sxs-lookup"><span data-stu-id="60e07-115">Implicit conversion to a [**D3D12\_PIPELINE\_STATE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="60e07-116">Notes</span><span class="sxs-lookup"><span data-stu-id="60e07-116">Remarks</span></span>

<span data-ttu-id="60e07-117">\_ \_ \_ \_ Les indicateurs de flux d’état de pipeline CD3DX12 sont une spécialisation typedef du modèle de sous- [**objet de flux d' \_ \_ état \_ \_ de pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) , et sont définis comme suit :</span><span class="sxs-lookup"><span data-stu-id="60e07-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_PIPELINE_STATE_FLAGS, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_FLAGS>
    CD3DX12_PIPELINE_STATE_STREAM_FLAGS;
          
```



## <a name="requirements"></a><span data-ttu-id="60e07-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60e07-118">Requirements</span></span>



| <span data-ttu-id="60e07-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60e07-119">Requirement</span></span> | <span data-ttu-id="60e07-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="60e07-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="60e07-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="60e07-121">Header</span></span><br/> | <dl> <span data-ttu-id="60e07-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="60e07-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60e07-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60e07-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60e07-124">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="60e07-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="60e07-125">**Sous \_ - \_ \_ objet de flux d’État du pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="60e07-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="60e07-126">**\_Type de \_ \_ sous-objet état \_ du pipeline D3D12**</span><span class="sxs-lookup"><span data-stu-id="60e07-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

