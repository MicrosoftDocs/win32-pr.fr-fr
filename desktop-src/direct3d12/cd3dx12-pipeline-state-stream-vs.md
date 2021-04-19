---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_VS (D3dx12. h)
description: Structure d’assistance utilisée pour décrire un nuanceur de sommets en tant qu’objet unique approprié pour une description de flux.
ms.assetid: 27EAB08C-D3B9-4920-B7D2-754AA3562A94
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_VS
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_VS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc7ea426c857893b98b25792ecc8e6c3d5803546
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106545264"
---
# <a name="cd3dx12_pipeline_state_stream_vs-structure"></a><span data-ttu-id="8248c-104">CD3DX12 \_ \_ \_ et structure du flux d’État du pipeline \_</span><span class="sxs-lookup"><span data-stu-id="8248c-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_VS structure</span></span>

<span data-ttu-id="8248c-105">Structure d’assistance utilisée pour décrire un nuanceur de sommets en tant qu’objet unique approprié pour une description de flux.</span><span class="sxs-lookup"><span data-stu-id="8248c-105">A helper structure used to describe a vertex shader as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="8248c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8248c-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_VS {
                                   CD3DX12_PIPELINE_STATE_STREAM_VS;
                                   CD3DX12_PIPELINE_STATE_STREAM_VS(D3D12_SHADER_BYTECODE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_VS operator=(D3D12_SHADER_BYTECODE const& i);
                                   operator D3D12_SHADER_BYTECODE() const;
};
```



## <a name="members"></a><span data-ttu-id="8248c-107">Membres</span><span class="sxs-lookup"><span data-stu-id="8248c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="8248c-108">**\_Flux d’état de pipeline CD3DX12 \_ \_ \_ et**</span><span class="sxs-lookup"><span data-stu-id="8248c-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_VS**</span></span>
</dt> <dd>

<span data-ttu-id="8248c-109">Crée une nouvelle instance non initialisée d’un \_ flux d’état de pipeline CD3DX12 \_ \_ \_ et</span><span class="sxs-lookup"><span data-stu-id="8248c-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_VS.</span></span>

</dd> <dt>

<span data-ttu-id="8248c-110">**\_Flux d’État du pipeline CD3DX12 par rapport au \_ \_ \_ \_ bytecode du nuanceur D3D12 \_ const &i)**</span><span class="sxs-lookup"><span data-stu-id="8248c-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_VS(D3D12\_SHADER\_BYTECODE const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="8248c-111">Crée une nouvelle instance d’un \_ flux d’état de pipeline CD3DX12 \_ \_ \_ par rapport à l’initialisation avec un type de sous-objet d’un type de sous-objet d' **État de pipeline D3D12 et des données de \_ \_ \_ \_ sous \_** -objet copiées à partir de *i*, une structure de [**\_ \_ bytecode de nuanceur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .</span><span class="sxs-lookup"><span data-stu-id="8248c-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_VS, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_VS** and subobject data copied from *i*, a [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8248c-112">**Operator = (D3D12 \_ Shader \_ bytecode const& i)**</span><span class="sxs-lookup"><span data-stu-id="8248c-112">**operator=(D3D12\_SHADER\_BYTECODE const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="8248c-113">Opérateur d’assignation de copie.</span><span class="sxs-lookup"><span data-stu-id="8248c-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="8248c-114">**Operator D3D12 \_ Shader \_ bytecode () const**</span><span class="sxs-lookup"><span data-stu-id="8248c-114">**operator D3D12\_SHADER\_BYTECODE() const**</span></span>
</dt> <dd>

<span data-ttu-id="8248c-115">Conversion implicite en une structure de [**\_ \_ bytecode de nuanceur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .</span><span class="sxs-lookup"><span data-stu-id="8248c-115">Implicit conversion to a [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8248c-116">Notes</span><span class="sxs-lookup"><span data-stu-id="8248c-116">Remarks</span></span>

<span data-ttu-id="8248c-117">CD3DX12 \_ \_ flux d’État du pipeline et \_ \_ est une spécialisation typedef du modèle de sous-objet de flux d' [**\_ État du pipeline \_ \_ \_ CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) , et est défini comme suit :</span><span class="sxs-lookup"><span data-stu-id="8248c-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_VS is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_SHADER_BYTECODE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_VS>
    CD3DX12_PIPELINE_STATE_STREAM_VS;
          
```



## <a name="requirements"></a><span data-ttu-id="8248c-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8248c-118">Requirements</span></span>



| <span data-ttu-id="8248c-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8248c-119">Requirement</span></span> | <span data-ttu-id="8248c-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="8248c-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8248c-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="8248c-121">Header</span></span><br/> | <dl> <span data-ttu-id="8248c-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="8248c-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8248c-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8248c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8248c-124">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="8248c-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="8248c-125">**Sous \_ - \_ \_ objet de flux d’État du pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="8248c-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="8248c-126">**\_Type de \_ \_ sous-objet état \_ du pipeline D3D12**</span><span class="sxs-lookup"><span data-stu-id="8248c-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

