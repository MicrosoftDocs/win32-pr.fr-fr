---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_GS (D3dx12. h)
description: Structure d’assistance utilisée pour décrire un nuanceur Geometry en tant qu’objet unique approprié pour une description de flux.
ms.assetid: EAE81688-DAEE-4F7C-A80D-E33B364B2E8C
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_GS
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_GS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df5ab5854ceddfb1a969742924c8063450e611bc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539425"
---
# <a name="cd3dx12_pipeline_state_stream_gs-structure"></a><span data-ttu-id="23f06-104">\_Structure de \_ \_ flux \_ GS d’État du pipeline CD3DX12</span><span class="sxs-lookup"><span data-stu-id="23f06-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_GS structure</span></span>

<span data-ttu-id="23f06-105">Structure d’assistance utilisée pour décrire un nuanceur Geometry en tant qu’objet unique approprié pour une description de flux.</span><span class="sxs-lookup"><span data-stu-id="23f06-105">A helper structure used to describe a geometry shader as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="23f06-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="23f06-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_GS {
                                   CD3DX12_PIPELINE_STATE_STREAM_GS;
                                   CD3DX12_PIPELINE_STATE_STREAM_GS(D3D12_SHADER_BYTECODE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_GS operator=(D3D12_SHADER_BYTECODE const& i);
                                   operator D3D12_SHADER_BYTECODE() const;
};
```



## <a name="members"></a><span data-ttu-id="23f06-107">Membres</span><span class="sxs-lookup"><span data-stu-id="23f06-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="23f06-108">**\_Flux d’état de pipeline CD3DX12 \_ \_ \_ GS**</span><span class="sxs-lookup"><span data-stu-id="23f06-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_GS**</span></span>
</dt> <dd>

<span data-ttu-id="23f06-109">Crée une nouvelle instance non initialisée d’un \_ flux d’état de pipeline CD3DX12 \_ \_ \_ GS.</span><span class="sxs-lookup"><span data-stu-id="23f06-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_GS.</span></span>

</dd> <dt>

<span data-ttu-id="23f06-110">**CD3DX12 \_ pipeline \_ State \_ Stream \_ GS (D3D12 \_ SHADER \_ bytecode const &i)**</span><span class="sxs-lookup"><span data-stu-id="23f06-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_GS(D3D12\_SHADER\_BYTECODE const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="23f06-111">Crée une nouvelle instance d’un \_ flux d’état de pipeline CD3DX12 \_ \_ \_ GS, initialisé avec un type de sous-objet de type de sous-objet d' **État de \_ pipeline D3D12 \_ \_ \_ \_ GS** et des données de sous-objet copiées à partir de *i*, une structure de [**\_ \_ bytecode de nuanceur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .</span><span class="sxs-lookup"><span data-stu-id="23f06-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_GS, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_GS** and subobject data copied from *i*, a [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

</dd> <dt>

<span data-ttu-id="23f06-112">**Operator = (D3D12 \_ Shader \_ bytecode const& i)**</span><span class="sxs-lookup"><span data-stu-id="23f06-112">**operator=(D3D12\_SHADER\_BYTECODE const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="23f06-113">Opérateur d’assignation de copie.</span><span class="sxs-lookup"><span data-stu-id="23f06-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="23f06-114">**Operator D3D12 \_ Shader \_ bytecode () const**</span><span class="sxs-lookup"><span data-stu-id="23f06-114">**operator D3D12\_SHADER\_BYTECODE() const**</span></span>
</dt> <dd>

<span data-ttu-id="23f06-115">Conversion implicite en une structure de [**\_ \_ bytecode de nuanceur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .</span><span class="sxs-lookup"><span data-stu-id="23f06-115">Implicit conversion to a [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23f06-116">Notes</span><span class="sxs-lookup"><span data-stu-id="23f06-116">Remarks</span></span>

<span data-ttu-id="23f06-117">CD3DX12 \_ pipeline \_ \_ Stream état \_ GS est une spécialisation typedef du modèle de sous-objet de [**flux d' \_ État de pipeline \_ \_ \_ CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) , et est défini comme suit :</span><span class="sxs-lookup"><span data-stu-id="23f06-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_GS is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_SHADER_BYTECODE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_GS>
    CD3DX12_PIPELINE_STATE_STREAM_GS;
          
```



## <a name="requirements"></a><span data-ttu-id="23f06-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="23f06-118">Requirements</span></span>



| <span data-ttu-id="23f06-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="23f06-119">Requirement</span></span> | <span data-ttu-id="23f06-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="23f06-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="23f06-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="23f06-121">Header</span></span><br/> | <dl> <span data-ttu-id="23f06-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="23f06-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23f06-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23f06-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23f06-124">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="23f06-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="23f06-125">**Sous \_ - \_ \_ objet de flux d’État du pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="23f06-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="23f06-126">**\_Type de \_ \_ sous-objet état \_ du pipeline D3D12**</span><span class="sxs-lookup"><span data-stu-id="23f06-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

