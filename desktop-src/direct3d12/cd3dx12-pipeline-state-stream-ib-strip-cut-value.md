---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE (D3dx12. h)
description: Structure d’assistance utilisée pour décrire la valeur de coupe de la bande de mémoire tampon d’index comme un objet unique approprié pour une description de flux.
ms.assetid: AF8F0919-4601-4A95-832A-5E1DA0304939
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c14924828c924b3bbbca3bb1a5f822437ec4c9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538316"
---
# <a name="cd3dx12_pipeline_state_stream_ib_strip_cut_value-structure"></a><span data-ttu-id="a9e1b-104">\_Flux d’État du pipeline CD3DX12-structure de \_ \_ \_ \_ \_ valeur de coupe \_</span><span class="sxs-lookup"><span data-stu-id="a9e1b-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE structure</span></span>

<span data-ttu-id="a9e1b-105">Structure d’assistance utilisée pour décrire la valeur de coupe de la bande de mémoire tampon d’index comme un objet unique approprié pour une description de flux.</span><span class="sxs-lookup"><span data-stu-id="a9e1b-105">A helper structure used to describe the index buffer strip cut value as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9e1b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a9e1b-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE {
                                                   CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE;
                                                   CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE operator=(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE const& i);
                                                   operator D3D12_INDEX_BUFFER_STRIP_CUT_VALUE() const;
};
```



## <a name="members"></a><span data-ttu-id="a9e1b-107">Membres</span><span class="sxs-lookup"><span data-stu-id="a9e1b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a9e1b-108">**CD3DX12 de \_ flux d’état de pipeline \_ IB- \_ \_ \_ \_ valeur de coupe \_**</span><span class="sxs-lookup"><span data-stu-id="a9e1b-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE**</span></span>
</dt> <dd>

<span data-ttu-id="a9e1b-109">Crée une nouvelle instance non initialisée d’un \_ flux d’état de pipeline CD3DX12 valeur de coupe de la \_ \_ \_ \_ barrette IB \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a9e1b-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE.</span></span>

</dd> <dt>

<span data-ttu-id="a9e1b-110">**\_Flux d’État du pipeline CD3DX12- \_ \_ \_ \_ \_ valeur de coupe de bande IB \_ (valeur de coupe de la \_ bande tampon d’index D3D12 \_ \_ \_ \_ const &i)**</span><span class="sxs-lookup"><span data-stu-id="a9e1b-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE(D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="a9e1b-111">Crée une nouvelle instance d’un \_ flux d’état de pipeline CD3DX12 \_ \_ \_ \_ \_ \_ , initialisée avec un type de sous-objet **d' \_ État de pipeline D3D12, \_ type de \_ \_ sous \_ \_ \_ \_** -objet de sous-objet IB de la valeur de coupe et des données de sous-objet copiées à partir de *i*, une structure de valeur de coupe de la [**\_ \_ bande de mémoire tampon \_ \_ \_ d’index D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value) .</span><span class="sxs-lookup"><span data-stu-id="a9e1b-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_IB\_STRIP\_CUT\_VALUE** and subobject data copied from *i*, a [**D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a9e1b-112">**Operator = (valeur de coupe de la \_ bande tampon d’index D3D12 \_ \_ \_ \_ const& i)**</span><span class="sxs-lookup"><span data-stu-id="a9e1b-112">**operator=(D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="a9e1b-113">Opérateur d’assignation de copie.</span><span class="sxs-lookup"><span data-stu-id="a9e1b-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="a9e1b-114">**\_ \_ valeur de coupe de la bande de la mémoire tampon d’index D3D12 \_ \_ \_ () const**</span><span class="sxs-lookup"><span data-stu-id="a9e1b-114">**operator D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE() const**</span></span>
</dt> <dd>

<span data-ttu-id="a9e1b-115">Conversion implicite en une structure de [**\_ \_ \_ \_ \_ valeur de coupe de mémoire tampon d’index D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value) .</span><span class="sxs-lookup"><span data-stu-id="a9e1b-115">Implicit conversion to a [**D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a9e1b-116">Notes</span><span class="sxs-lookup"><span data-stu-id="a9e1b-116">Remarks</span></span>

<span data-ttu-id="a9e1b-117">\_Flux d’État du pipeline CD3DX12 \_ \_ \_ \_ \_ \_ la valeur de coupe de la bande IB est une spécialisation typedef du modèle de sous-objet de flux d' [**\_ État du pipeline \_ \_ \_ CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) , et est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="a9e1b-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_INDEX_BUFFER_STRIP_CUT_VALUE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_IB_STRIP_CUT_VALUE>
    CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE;
          
```



## <a name="requirements"></a><span data-ttu-id="a9e1b-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a9e1b-118">Requirements</span></span>



| <span data-ttu-id="a9e1b-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a9e1b-119">Requirement</span></span> | <span data-ttu-id="a9e1b-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9e1b-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a9e1b-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="a9e1b-121">Header</span></span><br/> | <dl> <span data-ttu-id="a9e1b-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9e1b-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9e1b-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9e1b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9e1b-124">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="a9e1b-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="a9e1b-125">**Sous \_ - \_ \_ objet de flux d’État du pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="a9e1b-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="a9e1b-126">**\_Type de \_ \_ sous-objet état \_ du pipeline D3D12**</span><span class="sxs-lookup"><span data-stu-id="a9e1b-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

