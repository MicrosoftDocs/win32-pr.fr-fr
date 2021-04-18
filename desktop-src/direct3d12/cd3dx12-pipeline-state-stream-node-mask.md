---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK (D3dx12. h)
description: Structure d’assistance utilisée pour décrire un masque de nœud comme un objet unique approprié pour une description de flux.
ms.assetid: 5C770D9A-D692-46CF-8D60-EE5EB04998C8
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9c364ecd20459d8c20bdd3d30b969cc3b9ae46d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522571"
---
# <a name="cd3dx12_pipeline_state_stream_node_mask-structure"></a><span data-ttu-id="b5772-104">\_Structure de \_ \_ masque de nœud de flux d’état de \_ pipeline CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="b5772-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_NODE\_MASK structure</span></span>

<span data-ttu-id="b5772-105">Structure d’assistance utilisée pour décrire un masque de nœud comme un objet unique approprié pour une description de flux.</span><span class="sxs-lookup"><span data-stu-id="b5772-105">A helper structure used to describe a node mask as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5772-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5772-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK {
                                          CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK;
                                          CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK(UINT const &i);
  CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK operator=(UINT const& i);
                                          operator UINT() const;
};
```



## <a name="members"></a><span data-ttu-id="b5772-107">Membres</span><span class="sxs-lookup"><span data-stu-id="b5772-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b5772-108">**\_Masque de \_ \_ nœud du flux d’État du pipeline CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b5772-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_NODE\_MASK**</span></span>
</dt> <dd>

<span data-ttu-id="b5772-109">Crée une nouvelle instance non initialisée d’un \_ masque de nœud de flux d’état de pipeline CD3DX12 \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b5772-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_NODE\_MASK.</span></span>

</dd> <dt>

<span data-ttu-id="b5772-110">**\_Masque de nœud du flux d’État du pipeline CD3DX12 \_ \_ \_ \_ (uint const &i)**</span><span class="sxs-lookup"><span data-stu-id="b5772-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_NODE\_MASK(UINT const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="b5772-111">Crée une nouvelle instance d’un \_ masque de nœud de flux d’état de pipeline CD3DX12 \_ \_ \_ \_ , initialisée avec un type de sous-objet de type de sous-objet d' **État de pipeline D3D12 et des données de \_ \_ \_ \_ sous \_ \_** -objet copiées à partir de *i*, un masque de nœud **uint** .</span><span class="sxs-lookup"><span data-stu-id="b5772-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_NODE\_MASK, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_NODE\_MASK** and subobject data copied from *i*, a **UINT** node mask.</span></span>

</dd> <dt>

<span data-ttu-id="b5772-112">**opérateur = (UINT const& i)**</span><span class="sxs-lookup"><span data-stu-id="b5772-112">**operator=(UINT const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="b5772-113">Opérateur d’assignation de copie.</span><span class="sxs-lookup"><span data-stu-id="b5772-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="b5772-114">**const, opérateur ()**</span><span class="sxs-lookup"><span data-stu-id="b5772-114">**operator UINT() const**</span></span>
</dt> <dd>

<span data-ttu-id="b5772-115">Conversion implicite en masque de nœud **uint** .</span><span class="sxs-lookup"><span data-stu-id="b5772-115">Implicit conversion to a **UINT** node mask.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b5772-116">Notes</span><span class="sxs-lookup"><span data-stu-id="b5772-116">Remarks</span></span>

<span data-ttu-id="b5772-117">\_ \_ \_ \_ \_ Le masque de nœud de flux d’état de pipeline CD3DX12 est une spécialisation typedef du modèle de sous- [**objet de flux d' \_ \_ état \_ \_ de pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) , et est défini comme suit :</span><span class="sxs-lookup"><span data-stu-id="b5772-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_NODE\_MASK is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<UINT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_NODE_MASK>
    CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK;
          
```



## <a name="requirements"></a><span data-ttu-id="b5772-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5772-118">Requirements</span></span>



| <span data-ttu-id="b5772-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5772-119">Requirement</span></span> | <span data-ttu-id="b5772-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5772-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b5772-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="b5772-121">Header</span></span><br/> | <dl> <span data-ttu-id="b5772-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5772-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5772-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5772-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5772-124">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="b5772-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="b5772-125">**Sous \_ - \_ \_ objet de flux d’État du pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="b5772-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="b5772-126">**\_Type de \_ \_ sous-objet état \_ du pipeline D3D12**</span><span class="sxs-lookup"><span data-stu-id="b5772-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

