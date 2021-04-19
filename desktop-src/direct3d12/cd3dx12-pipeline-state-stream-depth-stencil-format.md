---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT (D3dx12. h)
description: Structure d’assistance utilisée pour décrire le format de stencil de profondeur comme un objet unique approprié pour une description de flux.
ms.assetid: 512DB46E-D8F0-482B-9174-C786FB91AFD2
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dc7ae2703ac80ac155c04d42624a081723288bf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525860"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil_format-structure"></a><span data-ttu-id="115cc-104">\_Structure du \_ \_ format du \_ stencil de profondeur du flux d' \_ État du pipeline CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="115cc-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT structure</span></span>

<span data-ttu-id="115cc-105">Structure d’assistance utilisée pour décrire le format de stencil de profondeur comme un objet unique approprié pour une description de flux.</span><span class="sxs-lookup"><span data-stu-id="115cc-105">A helper structure used to describe the depth stencil format as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="115cc-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="115cc-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT {
                                                     CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT;
                                                     CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT(DXGI_FORMAT const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT operator=(DXGI_FORMAT const& i);
                                                     operator DXGI_FORMAT() const;
};
```



## <a name="members"></a><span data-ttu-id="115cc-107">Membres</span><span class="sxs-lookup"><span data-stu-id="115cc-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="115cc-108">**\_Format du \_ \_ stencil de profondeur du flux d’État du \_ \_ pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="115cc-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT**</span></span>
</dt> <dd>

<span data-ttu-id="115cc-109">Crée une nouvelle instance non initialisée d’un \_ format de stencil de profondeur de flux d’état de pipeline CD3DX12 \_ \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="115cc-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT.</span></span>

</dd> <dt>

<span data-ttu-id="115cc-110">**\_ \_ Format de stencil de profondeur du flux d’État du pipeline CD3DX12 \_ \_ \_ \_ ( \_ format dxgi const &i)**</span><span class="sxs-lookup"><span data-stu-id="115cc-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT(DXGI\_FORMAT const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="115cc-111">Crée une nouvelle instance d’un \_ format de stencil de profondeur de flux d’état de pipeline CD3DX12 \_ \_ \_ \_ \_ , initialisée avec un type de sous-objet d' **État de pipeline D3D12 et des données de \_ \_ \_ \_ sous \_ \_ \_** -objet copiées à partir de *i*, une énumération de [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) .</span><span class="sxs-lookup"><span data-stu-id="115cc-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DEPTH\_STENCIL\_FORMAT** and subobject data copied from *i*, a [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="115cc-112">**opérateur = (DXGI \_ format const& i)**</span><span class="sxs-lookup"><span data-stu-id="115cc-112">**operator=(DXGI\_FORMAT const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="115cc-113">Opérateur d’assignation de copie.</span><span class="sxs-lookup"><span data-stu-id="115cc-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="115cc-114">**\_const, opérateur de format dxgi ()**</span><span class="sxs-lookup"><span data-stu-id="115cc-114">**operator DXGI\_FORMAT() const**</span></span>
</dt> <dd>

<span data-ttu-id="115cc-115">Conversion implicite en une énumération de [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) .</span><span class="sxs-lookup"><span data-stu-id="115cc-115">Implicit conversion to a [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) enumeration.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="115cc-116">Notes</span><span class="sxs-lookup"><span data-stu-id="115cc-116">Remarks</span></span>

<span data-ttu-id="115cc-117">\_ \_ \_ \_ \_ \_ Le format de stencil de profondeur du flux d’État du pipeline CD3DX12 est une spécialisation typedef du modèle de sous- [**objet de flux d' \_ \_ état \_ \_ du pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) , et est défini comme suit :</span><span class="sxs-lookup"><span data-stu-id="115cc-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<DXGI_FORMAT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL_FORMAT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT;
          
```



## <a name="requirements"></a><span data-ttu-id="115cc-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="115cc-118">Requirements</span></span>



| <span data-ttu-id="115cc-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="115cc-119">Requirement</span></span> | <span data-ttu-id="115cc-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="115cc-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="115cc-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="115cc-121">Header</span></span><br/> | <dl> <span data-ttu-id="115cc-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="115cc-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="115cc-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="115cc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="115cc-124">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="115cc-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="115cc-125">**Sous \_ - \_ \_ objet de flux d’État du pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="115cc-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="115cc-126">**\_Type de \_ \_ sous-objet état \_ du pipeline D3D12**</span><span class="sxs-lookup"><span data-stu-id="115cc-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

