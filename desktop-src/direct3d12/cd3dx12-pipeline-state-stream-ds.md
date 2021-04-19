---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_DS (D3dx12. h)
description: Structure d’assistance utilisée pour décrire un nuanceur de domaine en tant qu’objet unique approprié pour une description de flux.
ms.assetid: 42F8B7C1-B754-4B07-BF04-DBF450A942E6
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_DS
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbae1d75894e1fb8ffaa5bf95a45cc1eb3b2d9f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539424"
---
# <a name="cd3dx12_pipeline_state_stream_ds-structure"></a><span data-ttu-id="c11d7-104">\_Structure du \_ flux d’État du PIPELINe CD3DX12 \_ \_</span><span class="sxs-lookup"><span data-stu-id="c11d7-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_DS structure</span></span>

<span data-ttu-id="c11d7-105">Structure d’assistance utilisée pour décrire un nuanceur de domaine en tant qu’objet unique approprié pour une description de flux.</span><span class="sxs-lookup"><span data-stu-id="c11d7-105">A helper structure used to describe a domain shader as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="c11d7-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c11d7-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DS {
                                   CD3DX12_PIPELINE_STATE_STREAM_DS;
                                   CD3DX12_PIPELINE_STATE_STREAM_DS(D3D12_SHADER_BYTECODE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DS operator=(D3D12_SHADER_BYTECODE const& i);
                                   operator D3D12_SHADER_BYTECODE() const;
};
```



## <a name="members"></a><span data-ttu-id="c11d7-107">Membres</span><span class="sxs-lookup"><span data-stu-id="c11d7-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c11d7-108">**CD3DX12 \_ de \_ flux d’État du pipeline \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c11d7-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DS**</span></span>
</dt> <dd>

<span data-ttu-id="c11d7-109">Crée une nouvelle instance non initialisée d’un \_ flux d’état de pipeline CD3DX12 \_ \_ \_ DS.</span><span class="sxs-lookup"><span data-stu-id="c11d7-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DS.</span></span>

</dd> <dt>

<span data-ttu-id="c11d7-110">**CD3DX12 \_ pipeline d’État du pipeline \_ \_ \_ DS (D3D12 \_ SHADER \_ bytecode const &i)**</span><span class="sxs-lookup"><span data-stu-id="c11d7-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DS(D3D12\_SHADER\_BYTECODE const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="c11d7-111">Crée une nouvelle instance d’un \_ flux de données d’État du pipeline CD3DX12 \_ \_ \_ , initialisée avec un type de sous-objet du type de sous-objet **État du pipeline D3D12 et des données de \_ \_ \_ \_ sous \_** -objet copiées à partir de *i*, une structure de [**\_ \_ bytecode de nuanceur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .</span><span class="sxs-lookup"><span data-stu-id="c11d7-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DS, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DS** and subobject data copied from *i*, a [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c11d7-112">**Operator = (D3D12 \_ Shader \_ bytecode const& i)**</span><span class="sxs-lookup"><span data-stu-id="c11d7-112">**operator=(D3D12\_SHADER\_BYTECODE const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="c11d7-113">Opérateur d’assignation de copie.</span><span class="sxs-lookup"><span data-stu-id="c11d7-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="c11d7-114">**Operator D3D12 \_ Shader \_ bytecode () const**</span><span class="sxs-lookup"><span data-stu-id="c11d7-114">**operator D3D12\_SHADER\_BYTECODE() const**</span></span>
</dt> <dd>

<span data-ttu-id="c11d7-115">Conversion implicite en une structure de [**\_ \_ bytecode de nuanceur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .</span><span class="sxs-lookup"><span data-stu-id="c11d7-115">Implicit conversion to a [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c11d7-116">Notes</span><span class="sxs-lookup"><span data-stu-id="c11d7-116">Remarks</span></span>

<span data-ttu-id="c11d7-117">CD3DX12 \_ pipeline \_ \_ Stream State \_ DS est une spécialisation typedef du modèle de sous-objet de [**flux d' \_ État de pipeline \_ \_ \_ CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) , et est défini comme suit :</span><span class="sxs-lookup"><span data-stu-id="c11d7-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_DS is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_SHADER_BYTECODE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DS>
    CD3DX12_PIPELINE_STATE_STREAM_DS;
          
```



## <a name="requirements"></a><span data-ttu-id="c11d7-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c11d7-118">Requirements</span></span>



| <span data-ttu-id="c11d7-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c11d7-119">Requirement</span></span> | <span data-ttu-id="c11d7-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="c11d7-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c11d7-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="c11d7-121">Header</span></span><br/> | <dl> <span data-ttu-id="c11d7-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="c11d7-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c11d7-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c11d7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c11d7-124">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="c11d7-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="c11d7-125">**Sous \_ - \_ \_ objet de flux d’État du pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="c11d7-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="c11d7-126">**\_Type de \_ \_ sous-objet état \_ du pipeline D3D12**</span><span class="sxs-lookup"><span data-stu-id="c11d7-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

