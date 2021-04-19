---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE (D3dx12. h)
description: Structure d’assistance utilisée pour décrire la signature racine comme un objet unique approprié pour une description de flux.
ms.assetid: 351A78DC-9BDE-43B4-9A72-D65EE15CA441
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61a97402fa267693de23ed2085b3d41973dc409e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106545894"
---
# <a name="cd3dx12_pipeline_state_stream_root_signature-structure"></a><span data-ttu-id="65e65-104">Structure de la signature de la \_ racine du flux d’État du pipeline CD3DX12 \_ \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="65e65-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE structure</span></span>

<span data-ttu-id="65e65-105">Structure d’assistance utilisée pour décrire la signature racine comme un objet unique approprié pour une description de flux.</span><span class="sxs-lookup"><span data-stu-id="65e65-105">A helper structure used to describe the root signature as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="65e65-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65e65-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE {
                                               CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE;
                                               CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE(ID3D12RootSignature* const &i);
  CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE operator=(ID3D12RootSignature* const& i);
                                               operator ID3D12RootSignature*() const;
};
```



## <a name="members"></a><span data-ttu-id="65e65-107">Membres</span><span class="sxs-lookup"><span data-stu-id="65e65-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="65e65-108">**\_ \_ \_ Signature racine du flux d’état \_ du pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="65e65-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE**</span></span>
</dt> <dd>

<span data-ttu-id="65e65-109">Crée une nouvelle instance non initialisée d’une \_ signature racine de flux d’état de pipeline CD3DX12 \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="65e65-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE.</span></span>

</dd> <dt>

<span data-ttu-id="65e65-110">**\_Signature racine du flux d’État du pipeline CD3DX12 \_ \_ \_ \_ (ID3D12RootSignature \* const &i)**</span><span class="sxs-lookup"><span data-stu-id="65e65-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE(ID3D12RootSignature\* const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="65e65-111">Crée une nouvelle instance d’une \_ signature racine de flux d’état de pipeline CD3DX12 \_ \_ \_ \_ , initialisée avec un type de sous-objet de type de sous-objet d' **État de pipeline D3D12 et des données de \_ \_ \_ \_ sous \_ \_** -objet copiées à partir de *i*, une structure [**ID3D12RootSignature**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) .</span><span class="sxs-lookup"><span data-stu-id="65e65-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_ROOT\_SIGNATURE** and subobject data copied from *i*, a [**ID3D12RootSignature**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) structure.</span></span>

</dd> <dt>

<span data-ttu-id="65e65-112">**opérateur = (ID3D12RootSignature \* const& i)**</span><span class="sxs-lookup"><span data-stu-id="65e65-112">**operator=(ID3D12RootSignature\* const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="65e65-113">Opérateur d’assignation de copie.</span><span class="sxs-lookup"><span data-stu-id="65e65-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="65e65-114">**\*const, opérateur ID3D12RootSignature ()**</span><span class="sxs-lookup"><span data-stu-id="65e65-114">**operator ID3D12RootSignature\*() const**</span></span>
</dt> <dd>

<span data-ttu-id="65e65-115">Conversion implicite en pointeur de structure [**ID3D12RootSignature**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) .</span><span class="sxs-lookup"><span data-stu-id="65e65-115">Implicit conversion to a [**ID3D12RootSignature**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) structure pointer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65e65-116">Notes</span><span class="sxs-lookup"><span data-stu-id="65e65-116">Remarks</span></span>

<span data-ttu-id="65e65-117">\_ \_ \_ \_ La signature racine du flux d’État du pipeline CD3DX12 \_ est une spécialisation typedef du modèle de sous- [**objet de flux d' \_ \_ état \_ \_ du pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) , et est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="65e65-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<ID3D12RootSignature*, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_ROOT_SIGNATURE>
    CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE;
          
```



## <a name="requirements"></a><span data-ttu-id="65e65-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65e65-118">Requirements</span></span>



| <span data-ttu-id="65e65-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65e65-119">Requirement</span></span> | <span data-ttu-id="65e65-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="65e65-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="65e65-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="65e65-121">Header</span></span><br/> | <dl> <span data-ttu-id="65e65-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="65e65-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65e65-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65e65-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65e65-124">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="65e65-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="65e65-125">**Sous \_ - \_ \_ objet de flux d’État du pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="65e65-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="65e65-126">**\_Type de \_ \_ sous-objet état \_ du pipeline D3D12**</span><span class="sxs-lookup"><span data-stu-id="65e65-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

