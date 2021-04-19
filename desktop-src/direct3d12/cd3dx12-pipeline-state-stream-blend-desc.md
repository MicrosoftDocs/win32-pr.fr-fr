---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC (D3dx12. h)
description: Structure d’assistance utilisée pour décrire une description de Blend comme un objet unique approprié pour une description de flux.
ms.assetid: A629B05D-0A70-4C96-9F66-1508F2667BF6
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d251be9cc1423babc58e1d3c3be87c5345308874
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531319"
---
# <a name="cd3dx12_pipeline_state_stream_blend_desc-structure"></a><span data-ttu-id="a4e79-104">\_Structure de \_ \_ \_ mélange DESC du flux d’État du pipeline CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="a4e79-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC structure</span></span>

<span data-ttu-id="a4e79-105">Structure d’assistance utilisée pour décrire une description de Blend comme un objet unique approprié pour une description de flux.</span><span class="sxs-lookup"><span data-stu-id="a4e79-105">A helper structure used to describe a blend description as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4e79-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4e79-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC {
                                           CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC;
                                           CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC(CD3DX12_BLEND_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC operator=(CD3DX12_BLEND_DESC const& i);
                                           operator CD3DX12_BLEND_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="a4e79-107">Membres</span><span class="sxs-lookup"><span data-stu-id="a4e79-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a4e79-108">**\_ \_ \_ \_ Mélange DESC du flux d’État du pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="a4e79-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC**</span></span>
</dt> <dd>

<span data-ttu-id="a4e79-109">Crée une nouvelle instance non initialisée d’un \_ flux d’état de pipeline CD3DX12 \_ \_ \_ \_ desc.</span><span class="sxs-lookup"><span data-stu-id="a4e79-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="a4e79-110">**\_Flux d' \_ État de pipeline CD3DX12 \_ \_ \_ desc (CD3DX12 \_ Blend \_ desc const &i)**</span><span class="sxs-lookup"><span data-stu-id="a4e79-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC(CD3DX12\_BLEND\_DESC const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="a4e79-111">Crée une nouvelle instance d’un \_ flux d’état de pipeline CD3DX12 \_ \_ \_ Blend \_ , initialisé avec un type de sous-objet de **type de sous-objet d’état de \_ pipeline D3D12 \_ \_ \_ \_ Blend** et des données de sous-objet copiées à partir de *i*, une structure [**CD3DX12 \_ Blend \_ desc**](cd3dx12-blend-desc.md) .</span><span class="sxs-lookup"><span data-stu-id="a4e79-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_BLEND** and subobject data copied from *i*, a [**CD3DX12\_BLEND\_DESC**](cd3dx12-blend-desc.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a4e79-112">**opérateur = (CD3DX12 \_ Blend \_ desc const& i)**</span><span class="sxs-lookup"><span data-stu-id="a4e79-112">**operator=(CD3DX12\_BLEND\_DESC const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="a4e79-113">Opérateur d’assignation de copie.</span><span class="sxs-lookup"><span data-stu-id="a4e79-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="a4e79-114">**opérateur CD3DX12 \_ Blend \_ desc () const**</span><span class="sxs-lookup"><span data-stu-id="a4e79-114">**operator CD3DX12\_BLEND\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="a4e79-115">Conversion implicite en une structure [**CD3DX12 \_ Blend \_ desc**](cd3dx12-blend-desc.md) .</span><span class="sxs-lookup"><span data-stu-id="a4e79-115">Implicit conversion to a [**CD3DX12\_BLEND\_DESC**](cd3dx12-blend-desc.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a4e79-116">Notes</span><span class="sxs-lookup"><span data-stu-id="a4e79-116">Remarks</span></span>

<span data-ttu-id="a4e79-117">CD3DX12 \_ pipeline \_ \_ Stream State \_ Blend \_ est une spécialisation typedef du modèle de sous-objet de [**\_ flux d' \_ état \_ \_ de pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) , et est défini comme suit :</span><span class="sxs-lookup"><span data-stu-id="a4e79-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_BLEND_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_BLEND, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC;
          
```



## <a name="requirements"></a><span data-ttu-id="a4e79-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4e79-118">Requirements</span></span>



| <span data-ttu-id="a4e79-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a4e79-119">Requirement</span></span> | <span data-ttu-id="a4e79-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4e79-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a4e79-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="a4e79-121">Header</span></span><br/> | <dl> <span data-ttu-id="a4e79-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4e79-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4e79-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4e79-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4e79-124">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="a4e79-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="a4e79-125">**Sous \_ - \_ \_ objet de flux d’État du pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="a4e79-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="a4e79-126">**\_Type de \_ \_ sous-objet état \_ du pipeline D3D12**</span><span class="sxs-lookup"><span data-stu-id="a4e79-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

