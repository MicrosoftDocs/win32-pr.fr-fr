---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY (D3dx12. h)
description: Structure d’assistance utilisée pour décrire la topologie primitive comme un objet unique approprié pour une description de flux.
ms.assetid: 7DC73B75-2B8D-4DAB-A0AA-6DF6F4039093
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e597da8ea1ed4a4291142065e8e06f89d2664e03
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106529248"
---
# <a name="cd3dx12_pipeline_state_stream_primitive_topology-structure"></a><span data-ttu-id="54b03-104">\_Structure de \_ la \_ \_ topologie primitive du flux d’État du pipeline CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="54b03-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY structure</span></span>

<span data-ttu-id="54b03-105">Structure d’assistance utilisée pour décrire la topologie primitive comme un objet unique approprié pour une description de flux.</span><span class="sxs-lookup"><span data-stu-id="54b03-105">A helper structure used to describe the primitive topology as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="54b03-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="54b03-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY {
                                                   CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY;
                                                   CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY(D3D12_PRIMITIVE_TOPOLOGY_TYPE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY operator=(D3D12_PRIMITIVE_TOPOLOGY_TYPE const& i);
                                                   operator D3D12_PRIMITIVE_TOPOLOGY_TYPE() const;
};
```



## <a name="members"></a><span data-ttu-id="54b03-107">Membres</span><span class="sxs-lookup"><span data-stu-id="54b03-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="54b03-108">**\_ \_ \_ Topologie primitive du flux d’état \_ du pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="54b03-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY**</span></span>
</dt> <dd>

<span data-ttu-id="54b03-109">Crée une nouvelle instance non initialisée d’une \_ topologie primitive de flux d’état de pipeline CD3DX12 \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="54b03-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY.</span></span>

</dd> <dt>

<span data-ttu-id="54b03-110">**\_Topologie primitive du flux d’État du pipeline CD3DX12 \_ \_ \_ \_ ( \_ type de topologie D3D12 primitif \_ \_ const &i)**</span><span class="sxs-lookup"><span data-stu-id="54b03-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY(D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="54b03-111">Crée une nouvelle instance d’une \_ topologie primitive de flux d’état de pipeline CD3DX12 \_ \_ \_ \_ , initialisée avec un type de sous-objet de type de sous-objet de sous-objet d'  **État de \_ pipeline \_ \_ \_ \_ \_ D3D12** et des données de sous-objet copiées à partir de i, une structure de [**\_ \_ \_ type de topologie primitive D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) .</span><span class="sxs-lookup"><span data-stu-id="54b03-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_PRIMITIVE\_TOPOLOGY** and subobject data copied from *i*, a [**D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) structure.</span></span>

</dd> <dt>

<span data-ttu-id="54b03-112">**opérateur = (D3D12 \_ \_ type de topologie primitif \_ const& i)**</span><span class="sxs-lookup"><span data-stu-id="54b03-112">**operator=(D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="54b03-113">Opérateur d’assignation de copie.</span><span class="sxs-lookup"><span data-stu-id="54b03-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="54b03-114">**D3D12 \_ , opérateur \_ \_ type de topologie primitif () const**</span><span class="sxs-lookup"><span data-stu-id="54b03-114">**operator D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE() const**</span></span>
</dt> <dd>

<span data-ttu-id="54b03-115">Conversion implicite en une structure de [**\_ \_ \_ type de topologie primitive D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) .</span><span class="sxs-lookup"><span data-stu-id="54b03-115">Implicit conversion to a [**D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="54b03-116">Notes</span><span class="sxs-lookup"><span data-stu-id="54b03-116">Remarks</span></span>

<span data-ttu-id="54b03-117">\_ \_ \_ \_ La topologie primitive du flux d’État du pipeline CD3DX12 \_ est une spécialisation typedef du modèle de sous- [**objet de flux d' \_ \_ état \_ \_ du pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) , et est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="54b03-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_PRIMITIVE_TOPOLOGY_TYPE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_PRIMITIVE_TOPOLOGY>
    CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY;
          
```



## <a name="requirements"></a><span data-ttu-id="54b03-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="54b03-118">Requirements</span></span>



| <span data-ttu-id="54b03-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="54b03-119">Requirement</span></span> | <span data-ttu-id="54b03-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="54b03-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="54b03-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="54b03-121">Header</span></span><br/> | <dl> <span data-ttu-id="54b03-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="54b03-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54b03-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54b03-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54b03-124">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="54b03-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="54b03-125">**Sous \_ - \_ \_ objet de flux d’État du pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="54b03-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="54b03-126">**\_Type de \_ \_ sous-objet état \_ du pipeline D3D12**</span><span class="sxs-lookup"><span data-stu-id="54b03-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

