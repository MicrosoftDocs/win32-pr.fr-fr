---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL (D3dx12. h)
description: Structure d’assistance utilisée pour décrire une description de stencil de profondeur comme un objet unique approprié pour une description de flux. | Structure CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL (D3dx12. h)
ms.assetid: 4FB54EA5-FCC6-4B64-A747-27DFE4C1D2DC
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb24779aeff950bd213ce18774f55493777df9c9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539426"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil-structure"></a><span data-ttu-id="b06f4-105">\_Structure du \_ \_ stencil de profondeur du flux d’État du \_ pipeline CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="b06f4-105">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL structure</span></span>

<span data-ttu-id="b06f4-106">Structure d’assistance utilisée pour décrire une description de stencil de profondeur comme un objet unique approprié pour une description de flux.</span><span class="sxs-lookup"><span data-stu-id="b06f4-106">A helper structure used to describe a depth stencil description as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="b06f4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b06f4-107">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL {
                                              CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL;
                                              CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL(CD3DX12_DEPTH_STENCIL_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL operator=(CD3DX12_DEPTH_STENCIL_DESC const& i);
                                              operator CD3DX12_DEPTH_STENCIL_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="b06f4-108">Membres</span><span class="sxs-lookup"><span data-stu-id="b06f4-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="b06f4-109">**\_Stencil de \_ \_ profondeur du flux d’État du pipeline CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b06f4-109">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL**</span></span>
</dt> <dd>

<span data-ttu-id="b06f4-110">Crée une nouvelle instance non initialisée d’un \_ stencil de profondeur de flux d’état de pipeline CD3DX12 \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b06f4-110">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL.</span></span>

</dd> <dt>

<span data-ttu-id="b06f4-111">**CD3DX12 \_ \_ stencil de profondeur du flux d’État du pipeline \_ \_ \_ (CD3DX12 \_ \_ \_ desc const &i)**</span><span class="sxs-lookup"><span data-stu-id="b06f4-111">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL(CD3DX12\_DEPTH\_STENCIL\_DESC const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="b06f4-112">Crée une nouvelle instance d’un \_ stencil de profondeur de flux d’état de pipeline CD3DX12 \_ \_ \_ \_ , initialisée avec un type de sous-objet du **stencil de profondeur de D3D12 d’État du \_ pipeline et des données de \_ \_ \_ sous \_ \_** -objet copiées à partir de *i*, une structure [**\_ \_ \_ desc du stencil de profondeur CD3DX12**](cd3dx12-depth-stencil-desc.md) .</span><span class="sxs-lookup"><span data-stu-id="b06f4-112">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DEPTH\_STENCIL** and subobject data copied from *i*, a [**CD3DX12\_DEPTH\_STENCIL\_DESC**](cd3dx12-depth-stencil-desc.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b06f4-113">**Operator = (CD3DX12 de \_ profondeur du \_ stencil \_ const& i)**</span><span class="sxs-lookup"><span data-stu-id="b06f4-113">**operator=(CD3DX12\_DEPTH\_STENCIL\_DESC const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="b06f4-114">Opérateur d’assignation de copie.</span><span class="sxs-lookup"><span data-stu-id="b06f4-114">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="b06f4-115">**CD3DX12 \_ \_ \_ () const du stencil de profondeur de l’opérateur**</span><span class="sxs-lookup"><span data-stu-id="b06f4-115">**operator CD3DX12\_DEPTH\_STENCIL\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="b06f4-116">Conversion implicite en [**structure \_ \_ \_ desc du stencil de profondeur CD3DX12**](cd3dx12-depth-stencil-desc.md) .</span><span class="sxs-lookup"><span data-stu-id="b06f4-116">Implicit conversion to a [**CD3DX12\_DEPTH\_STENCIL\_DESC**](cd3dx12-depth-stencil-desc.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b06f4-117">Notes</span><span class="sxs-lookup"><span data-stu-id="b06f4-117">Remarks</span></span>

<span data-ttu-id="b06f4-118">\_ \_ \_ \_ \_ Le stencil de profondeur du flux d’État du pipeline CD3DX12 est une spécialisation typedef du modèle de sous- [**objet de flux d' \_ \_ état \_ \_ du pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) , et est défini comme suit :</span><span class="sxs-lookup"><span data-stu-id="b06f4-118">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_DEPTH_STENCIL_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL;
          
```



## <a name="requirements"></a><span data-ttu-id="b06f4-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b06f4-119">Requirements</span></span>



| <span data-ttu-id="b06f4-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b06f4-120">Requirement</span></span> | <span data-ttu-id="b06f4-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="b06f4-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b06f4-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="b06f4-122">Header</span></span><br/> | <dl> <span data-ttu-id="b06f4-123"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="b06f4-123"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b06f4-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b06f4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b06f4-125">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="b06f4-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="b06f4-126">**Sous \_ - \_ \_ objet de flux d’État du pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="b06f4-126">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="b06f4-127">**\_Type de \_ \_ sous-objet état \_ du pipeline D3D12**</span><span class="sxs-lookup"><span data-stu-id="b06f4-127">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

