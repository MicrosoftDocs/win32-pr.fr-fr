---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 (D3dx12. h)
description: Structure d’assistance utilisée pour décrire une description de stencil de profondeur comme un objet unique approprié pour une description de flux. | Structure CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 (D3dx12. h)
ms.assetid: 7D3554D9-610D-43B5-94F0-68167E966A86
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee95e9e37ad1dfced119848c76f071564aaa9435
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522572"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil1-structure"></a><span data-ttu-id="241f8-105">\_ \_ \_ \_ Structure STENCIL1 de profondeur du flux d’État du pipeline CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="241f8-105">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1 structure</span></span>

<span data-ttu-id="241f8-106">Structure d’assistance utilisée pour décrire une description de stencil de profondeur comme un objet unique approprié pour une description de flux.</span><span class="sxs-lookup"><span data-stu-id="241f8-106">A helper structure used to describe a depth stencil description as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="241f8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="241f8-107">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 {
                                               CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1;
                                               CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1(CD3DX12_DEPTH_STENCIL_DESC1 const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 operator=(CD3DX12_DEPTH_STENCIL_DESC1 const& i);
                                               operator CD3DX12_DEPTH_STENCIL_DESC1() const;
};
```



## <a name="members"></a><span data-ttu-id="241f8-108">Membres</span><span class="sxs-lookup"><span data-stu-id="241f8-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="241f8-109">**\_Profondeur du flux d’État du pipeline CD3DX12 \_ \_ \_ \_ STENCIL1**</span><span class="sxs-lookup"><span data-stu-id="241f8-109">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1**</span></span>
</dt> <dd>

<span data-ttu-id="241f8-110">Crée une nouvelle instance non initialisée d’un \_ STENCIL1 de profondeur du flux d’État du pipeline CD3DX12 \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="241f8-110">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1.</span></span>

</dd> <dt>

<span data-ttu-id="241f8-111">**CD3DX12 \_ de la profondeur du flux d’État du pipeline \_ \_ \_ \_ STENCIL1 ( \_ stencil de profondeur CD3DX12 \_ \_ DESC1 const &i)**</span><span class="sxs-lookup"><span data-stu-id="241f8-111">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1(CD3DX12\_DEPTH\_STENCIL\_DESC1 const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="241f8-112">Crée une instance d’une profondeur de \_ flux d’état de pipeline CD3DX12 \_ \_ \_ \_ STENCIL1, initialisée avec un type de sous-objet de **D3D12 \_ profondeur de type de sous-objet d’état de pipeline \_ \_ \_ \_ \_ STENCIL1** et des données de sous-objet copiées à partir de *i*, une structure CD3DX12 de [**\_ stencil de profondeur \_ \_ DESC1**](cd3dx12-depth-stencil-desc1.md) .</span><span class="sxs-lookup"><span data-stu-id="241f8-112">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DEPTH\_STENCIL1** and subobject data copied from *i*, a [**CD3DX12\_DEPTH\_STENCIL\_DESC1**](cd3dx12-depth-stencil-desc1.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="241f8-113">**Operator = (CD3DX12 de \_ profondeur du \_ stencil \_ DESC1 const& i)**</span><span class="sxs-lookup"><span data-stu-id="241f8-113">**operator=(CD3DX12\_DEPTH\_STENCIL\_DESC1 const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="241f8-114">Opérateur d’assignation de copie.</span><span class="sxs-lookup"><span data-stu-id="241f8-114">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="241f8-115">**CD3DX12 \_ de profondeur \_ de l’opérateur \_ DESC1 () const**</span><span class="sxs-lookup"><span data-stu-id="241f8-115">**operator CD3DX12\_DEPTH\_STENCIL\_DESC1() const**</span></span>
</dt> <dd>

<span data-ttu-id="241f8-116">Conversion implicite en [**structure \_ \_ \_ DESC1 du stencil de profondeur CD3DX12**](cd3dx12-depth-stencil-desc1.md) .</span><span class="sxs-lookup"><span data-stu-id="241f8-116">Implicit conversion to a [**CD3DX12\_DEPTH\_STENCIL\_DESC1**](cd3dx12-depth-stencil-desc1.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="241f8-117">Notes</span><span class="sxs-lookup"><span data-stu-id="241f8-117">Remarks</span></span>

<span data-ttu-id="241f8-118">\_ \_ \_ \_ La profondeur du flux d’État du pipeline CD3DX12 \_ STENCIL1 est une spécialisation typedef du modèle de sous- [**objet de flux d' \_ \_ état \_ \_ du pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) et est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="241f8-118">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1 is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_DEPTH_STENCIL_DESC1, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL1, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1;
          
```



## <a name="requirements"></a><span data-ttu-id="241f8-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="241f8-119">Requirements</span></span>



| <span data-ttu-id="241f8-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="241f8-120">Requirement</span></span> | <span data-ttu-id="241f8-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="241f8-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="241f8-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="241f8-122">Header</span></span><br/> | <dl> <span data-ttu-id="241f8-123"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="241f8-123"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="241f8-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="241f8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="241f8-125">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="241f8-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="241f8-126">**Sous \_ - \_ \_ objet de flux d’État du pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="241f8-126">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="241f8-127">**\_Type de \_ \_ sous-objet état \_ du pipeline D3D12**</span><span class="sxs-lookup"><span data-stu-id="241f8-127">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

