---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT (D3dx12. h)
description: Structure d’assistance utilisée pour décrire une disposition d’entrée sous la forme d’un objet unique approprié pour une description de flux de données.
ms.assetid: CEAD9FA6-4FB0-492E-9E81-8C4900A1FBC5
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ba382552d700ddddee02cdc1343936e6bcf6837
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535795"
---
# <a name="cd3dx12_pipeline_state_stream_input_layout-structure"></a><span data-ttu-id="c0008-104">\_Structure de \_ \_ \_ disposition d’entrée de flux d’état de pipeline CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="c0008-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT structure</span></span>

<span data-ttu-id="c0008-105">Structure d’assistance utilisée pour décrire une disposition d’entrée sous la forme d’un objet unique approprié pour une description de flux de données.</span><span class="sxs-lookup"><span data-stu-id="c0008-105">A helper structure used to describe an input layout as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0008-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0008-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT {
                                             CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT;
                                             CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT(D3D12_INPUT_LAYOUT_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT operator=(D3D12_INPUT_LAYOUT_DESC const& i);
                                             operator D3D12_INPUT_LAYOUT_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="c0008-107">Membres</span><span class="sxs-lookup"><span data-stu-id="c0008-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c0008-108">**\_ \_ \_ \_ Disposition d’entrée de flux d’état de pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="c0008-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT**</span></span>
</dt> <dd>

<span data-ttu-id="c0008-109">Crée une nouvelle instance non initialisée d’une \_ \_ \_ \_ disposition d’entrée de flux d’état de pipeline CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="c0008-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT.</span></span>

</dd> <dt>

<span data-ttu-id="c0008-110">**\_ \_ \_ \_ Disposition d’entrée de flux d’état de pipeline CD3DX12 \_ ( \_ disposition d’entrée D3D12 \_ \_ desc const &i)**</span><span class="sxs-lookup"><span data-stu-id="c0008-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT(D3D12\_INPUT\_LAYOUT\_DESC const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="c0008-111">Crée une nouvelle instance d’une \_ disposition d’entrée de flux d’état de pipeline CD3DX12 \_ \_ \_ \_ , initialisée avec un type de sous-objet de type de sous-objet de sous-objet d' **État de pipeline D3D12 et des données de \_ \_ \_ \_ sous \_ \_** -objet copiées à partir de *i*, une structure de [**\_ \_ disposition \_ d’entrée de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) .</span><span class="sxs-lookup"><span data-stu-id="c0008-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_INPUT\_LAYOUT** and subobject data copied from *i*, a [**D3D12\_INPUT\_LAYOUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c0008-112">**Operator = (D3D12 \_ d’entrée \_ disposition \_ DESC const& i)**</span><span class="sxs-lookup"><span data-stu-id="c0008-112">**operator=(D3D12\_INPUT\_LAYOUT\_DESC const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="c0008-113">Opérateur d’assignation de copie.</span><span class="sxs-lookup"><span data-stu-id="c0008-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="c0008-114">**D3D12 \_ d’entrée \_ de l’opérateur \_ desc () const**</span><span class="sxs-lookup"><span data-stu-id="c0008-114">**operator D3D12\_INPUT\_LAYOUT\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="c0008-115">Conversion implicite en une structure [**\_ \_ \_ desc d’entrée D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) .</span><span class="sxs-lookup"><span data-stu-id="c0008-115">Implicit conversion to a [**D3D12\_INPUT\_LAYOUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c0008-116">Notes</span><span class="sxs-lookup"><span data-stu-id="c0008-116">Remarks</span></span>

<span data-ttu-id="c0008-117">\_ \_ \_ \_ La disposition d’entrée de flux d’état de pipeline CD3DX12 \_ est une spécialisation typedef du modèle de sous- [**objet de flux d' \_ État de pipeline \_ \_ \_ CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) , et est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="c0008-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_INPUT_LAYOUT_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_INPUT_LAYOUT>
    CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT;
          
```



## <a name="requirements"></a><span data-ttu-id="c0008-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0008-118">Requirements</span></span>



| <span data-ttu-id="c0008-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0008-119">Requirement</span></span> | <span data-ttu-id="c0008-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0008-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c0008-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="c0008-121">Header</span></span><br/> | <dl> <span data-ttu-id="c0008-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0008-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0008-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0008-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0008-124">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="c0008-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="c0008-125">**Sous \_ - \_ \_ objet de flux d’État du pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="c0008-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="c0008-126">**\_Type de \_ \_ sous-objet état \_ du pipeline D3D12**</span><span class="sxs-lookup"><span data-stu-id="c0008-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

