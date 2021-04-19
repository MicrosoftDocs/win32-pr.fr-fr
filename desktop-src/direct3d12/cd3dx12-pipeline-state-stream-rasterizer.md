---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER (D3dx12. h)
description: Structure d’assistance utilisée pour décrire une description de rastériseur comme un objet unique approprié pour une description de flux.
ms.assetid: 650C2DA3-63FB-44D1-BE9A-E21E13DA24DB
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f656ad354430b00e757ece0aa2ce482de1f06e2e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106544399"
---
# <a name="cd3dx12_pipeline_state_stream_rasterizer-structure"></a><span data-ttu-id="a4235-104">\_Structure de \_ \_ rastériseur du flux d’État du pipeline CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="a4235-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER structure</span></span>

<span data-ttu-id="a4235-105">Structure d’assistance utilisée pour décrire une description de rastériseur comme un objet unique approprié pour une description de flux.</span><span class="sxs-lookup"><span data-stu-id="a4235-105">A helper structure used to describe a rasterizer description as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4235-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4235-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER {
                                           CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER;
                                           CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER(CD3DX12_RASTERIZER_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER operator=(CD3DX12_RASTERIZER_DESC const& i);
                                           operator CD3DX12_RASTERIZER_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="a4235-107">Membres</span><span class="sxs-lookup"><span data-stu-id="a4235-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a4235-108">**\_Rastériseur de \_ flux d’état de PIPELINe CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a4235-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER**</span></span>
</dt> <dd>

<span data-ttu-id="a4235-109">Crée une nouvelle instance non initialisée d’un \_ rastériseur de flux d’état de pipeline CD3DX12 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a4235-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER.</span></span>

</dd> <dt>

<span data-ttu-id="a4235-110">**\_ \_ Rastériseur de flux d’état de pipeline CD3DX12 \_ \_ (CD3DX12 \_ rastériseur \_ desc const &i)**</span><span class="sxs-lookup"><span data-stu-id="a4235-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER(CD3DX12\_RASTERIZER\_DESC const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="a4235-111">Crée une nouvelle instance d’un \_ rastériseur de flux d’état de pipeline CD3DX12 \_ \_ \_ , initialisée avec un type de sous-objet de type de sous-objet d' **État de pipeline D3D12 et des données de \_ \_ \_ \_ sous \_** -objet copiées à partir de *i*, une structure de [**\_ rastériseur CD3DX12 \_ desc**](cd3dx12-rasterizer-desc.md) .</span><span class="sxs-lookup"><span data-stu-id="a4235-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_RASTERIZER** and subobject data copied from *i*, a [**CD3DX12\_RASTERIZER\_DESC**](cd3dx12-rasterizer-desc.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a4235-112">**Operator = (CD3DX12 \_ rastériseur \_ desc const& i)**</span><span class="sxs-lookup"><span data-stu-id="a4235-112">**operator=(CD3DX12\_RASTERIZER\_DESC const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="a4235-113">Opérateur d’assignation de copie.</span><span class="sxs-lookup"><span data-stu-id="a4235-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="a4235-114">**opérateur CD3DX12 \_ rastériseur \_ desc () const**</span><span class="sxs-lookup"><span data-stu-id="a4235-114">**operator CD3DX12\_RASTERIZER\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="a4235-115">Conversion implicite en une structure [**CD3DX12 \_ rastériseur \_ desc**](cd3dx12-rasterizer-desc.md) .</span><span class="sxs-lookup"><span data-stu-id="a4235-115">Implicit conversion to a [**CD3DX12\_RASTERIZER\_DESC**](cd3dx12-rasterizer-desc.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a4235-116">Notes</span><span class="sxs-lookup"><span data-stu-id="a4235-116">Remarks</span></span>

<span data-ttu-id="a4235-117">\_ \_ \_ \_ Le rastériseur de flux d’état de pipeline CD3DX12 est une spécialisation typedef du modèle de sous- [**objet de flux d' \_ \_ état \_ \_ de pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) , et est défini comme suit :</span><span class="sxs-lookup"><span data-stu-id="a4235-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_RASTERIZER_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_RASTERIZER, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER;
          
```



## <a name="requirements"></a><span data-ttu-id="a4235-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4235-118">Requirements</span></span>



| <span data-ttu-id="a4235-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a4235-119">Requirement</span></span> | <span data-ttu-id="a4235-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4235-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a4235-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="a4235-121">Header</span></span><br/> | <dl> <span data-ttu-id="a4235-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4235-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4235-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4235-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4235-124">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="a4235-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="a4235-125">**Sous \_ - \_ \_ objet de flux d’État du pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="a4235-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="a4235-126">**\_Type de \_ \_ sous-objet état \_ du pipeline D3D12**</span><span class="sxs-lookup"><span data-stu-id="a4235-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

