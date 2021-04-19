---
title: Structure CD3DX12_DESCRIPTOR_RANGE1 (D3dx12. h)
description: Structure d’assistance pour faciliter l’initialisation d’une \_ structure RANGE1 de descripteur D3D12 \_ .
ms.assetid: 9D073158-5907-4D1C-8D75-72B304277DAD
keywords:
- Structure CD3DX12_DESCRIPTOR_RANGE1
topic_type:
- apiref
api_name:
- CD3DX12_DESCRIPTOR_RANGE1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6386d8094d573fba9cd3af44b0148215ee621e2f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106537242"
---
# <a name="cd3dx12_descriptor_range1-structure"></a><span data-ttu-id="3a38d-104">\_Structure RANGE1 du descripteur CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="3a38d-104">CD3DX12\_DESCRIPTOR\_RANGE1 structure</span></span>

<span data-ttu-id="3a38d-105">Structure d’assistance pour faciliter l’initialisation d’une structure [**\_ \_ RANGE1 de descripteur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) .</span><span class="sxs-lookup"><span data-stu-id="3a38d-105">A helper structure to enable easy initialization of a [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a38d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a38d-106">Syntax</span></span>


```C++
struct CD3DX12_DESCRIPTOR_RANGE1  : public D3D12_DESCRIPTOR_RANGE1{
       CD3DX12_DESCRIPTOR_RANGE1();
       explicit CD3DX12_DESCRIPTOR_RANGE1(const D3D12_DESCRIPTOR_RANGE1 &o);
       CD3DX12_DESCRIPTOR_RANGE1(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void inline Init(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void static inline Init(D3D12_DESCRIPTOR_RANGE1 &range, D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
};
```



## <a name="members"></a><span data-ttu-id="3a38d-107">Membres</span><span class="sxs-lookup"><span data-stu-id="3a38d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="3a38d-108">**\_Descripteur CD3DX12 \_ RANGE1 ()**</span><span class="sxs-lookup"><span data-stu-id="3a38d-108">**CD3DX12\_DESCRIPTOR\_RANGE1()**</span></span>
</dt> <dd>

<span data-ttu-id="3a38d-109">Crée une nouvelle instance non initialisée d’un \_ descripteur CD3DX12 \_ RANGE1.</span><span class="sxs-lookup"><span data-stu-id="3a38d-109">Creates a new, uninitialized, instance of a CD3DX12\_DESCRIPTOR\_RANGE1.</span></span>

</dd> <dt>

<span data-ttu-id="3a38d-110">**descripteur CD3DX12 explicite \_ \_ range1 (const D3D12 \_ Descriptor \_ range1 &o)**</span><span class="sxs-lookup"><span data-stu-id="3a38d-110">**explicit CD3DX12\_DESCRIPTOR\_RANGE1(const D3D12\_DESCRIPTOR\_RANGE1 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="3a38d-111">Crée une nouvelle instance d’un \_ descripteur CD3DX12 \_ range1, initialisée avec le contenu d’une autre structure [**\_ \_ range1 du descripteur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) .</span><span class="sxs-lookup"><span data-stu-id="3a38d-111">Creates a new instance of a CD3DX12\_DESCRIPTOR\_RANGE1, initialized with the contents of another [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="3a38d-112">**CD3DX12 descripteur \_ \_ RANGE1 (D3D12 \_ descripteur de \_ \_ type RANGETYPE, uint NUMDESCRIPTORS, uint baseShaderRegister, uint registerSpace = 0, D3D12 \_ plage du descripteur indicateurs \_ \_ = D3D12 \_ plage de descripteurs \_ \_ \_ aucun, uint offsetInDescriptorsFromTableStart = D3D12 décalage de la \_ plage du descripteur \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3a38d-112">**CD3DX12\_DESCRIPTOR\_RANGE1(D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12\_DESCRIPTOR\_RANGE\_FLAGS flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="3a38d-113">Crée une nouvelle instance d’un \_ descripteur CD3DX12 \_ RANGE1, en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="3a38d-113">Creates a new instance of a CD3DX12\_DESCRIPTOR\_RANGE1, initializing the following parameters:</span></span>

<span data-ttu-id="3a38d-114">[**D3D12 \_ \_ \_ Type de plage de descripteur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span><span class="sxs-lookup"><span data-stu-id="3a38d-114">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="3a38d-115">UINT numDescriptors</span><span class="sxs-lookup"><span data-stu-id="3a38d-115">UINT numDescriptors</span></span>

<span data-ttu-id="3a38d-116">UINT baseShaderRegister</span><span class="sxs-lookup"><span data-stu-id="3a38d-116">UINT baseShaderRegister</span></span>

<span data-ttu-id="3a38d-117">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="3a38d-117">UINT registerSpace = 0</span></span>

<span data-ttu-id="3a38d-118">[**D3D12 \_ Identificateurs de \_ plage \_ de descripteurs**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) = \_ indicateur de plage de descripteurs D3D12 \_ \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="3a38d-118">[**D3D12\_DESCRIPTOR\_RANGE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE</span></span>

<span data-ttu-id="3a38d-119">UINT offsetInDescriptorsFromTableStart = D3D12 \_ descripteur de décalage de la plage de descripteurs \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="3a38d-119">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> <dt>

<span data-ttu-id="3a38d-120">**Inline init ( \_ type de plage de descripteur D3D12 \_ \_ RangeType, UINT NumDescriptors, UINT BaseShaderRegister, uint registerSpace = 0, D3D12 \_ plage de descripteur indicateurs \_ \_ = D3D12 \_ plage de descripteurs \_ \_ \_ aucun, uint offsetInDescriptorsFromTableStart = D3D12 ajout de décalage de la \_ plage du descripteur \_ \_ \_ )**</span><span class="sxs-lookup"><span data-stu-id="3a38d-120">**inline Init(D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12\_DESCRIPTOR\_RANGE\_FLAGS flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="3a38d-121">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="3a38d-121">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="3a38d-122">[**D3D12 \_ \_ \_ Type de plage de descripteur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span><span class="sxs-lookup"><span data-stu-id="3a38d-122">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="3a38d-123">UINT numDescriptors</span><span class="sxs-lookup"><span data-stu-id="3a38d-123">UINT numDescriptors</span></span>

<span data-ttu-id="3a38d-124">UINT baseShaderRegister</span><span class="sxs-lookup"><span data-stu-id="3a38d-124">UINT baseShaderRegister</span></span>

<span data-ttu-id="3a38d-125">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="3a38d-125">UINT registerSpace = 0</span></span>

<span data-ttu-id="3a38d-126">[**D3D12 \_ Identificateurs de \_ plage \_ de descripteurs**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) = \_ indicateur de plage de descripteurs D3D12 \_ \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="3a38d-126">[**D3D12\_DESCRIPTOR\_RANGE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE</span></span>

<span data-ttu-id="3a38d-127">UINT offsetInDescriptorsFromTableStart = D3D12 \_ descripteur de décalage de la plage de descripteurs \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="3a38d-127">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> <dt>

<span data-ttu-id="3a38d-128">**static Inline init (D3D12 \_ descripteur \_ RANGE1 &plage, D3D12 \_ descripteur \_ \_ type RANGETYPE, uint NUMDESCRIPTORS, uint baseShaderRegister, uint registerSpace = 0, D3D12 \_ plage du descripteur indicateurs = D3D12 plage du descripteur \_ \_ \_ \_ \_ \_ None, uint offsetInDescriptorsFromTableStart = D3D12 de décalage de la \_ plage du descripteur \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3a38d-128">**static inline Init(D3D12\_DESCRIPTOR\_RANGE1 &range, D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12\_DESCRIPTOR\_RANGE\_FLAGS flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="3a38d-129">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="3a38d-129">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="3a38d-130">[**D3D12 \_ Plage de &\_ RANGE1 du DEscripteur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)</span><span class="sxs-lookup"><span data-stu-id="3a38d-130">[**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) &range</span></span>

<span data-ttu-id="3a38d-131">[**D3D12 \_ \_ \_ Type de plage de descripteur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span><span class="sxs-lookup"><span data-stu-id="3a38d-131">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="3a38d-132">UINT numDescriptors</span><span class="sxs-lookup"><span data-stu-id="3a38d-132">UINT numDescriptors</span></span>

<span data-ttu-id="3a38d-133">UINT baseShaderRegister</span><span class="sxs-lookup"><span data-stu-id="3a38d-133">UINT baseShaderRegister</span></span>

<span data-ttu-id="3a38d-134">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="3a38d-134">UINT registerSpace = 0</span></span>

<span data-ttu-id="3a38d-135">[**D3D12 \_ Identificateurs de \_ plage \_ de descripteurs**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) = \_ indicateur de plage de descripteurs D3D12 \_ \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="3a38d-135">[**D3D12\_DESCRIPTOR\_RANGE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE</span></span>

<span data-ttu-id="3a38d-136">UINT offsetInDescriptorsFromTableStart = D3D12 \_ descripteur de décalage de la plage de descripteurs \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="3a38d-136">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3a38d-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a38d-137">Requirements</span></span>



| <span data-ttu-id="3a38d-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a38d-138">Requirement</span></span> | <span data-ttu-id="3a38d-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a38d-139">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3a38d-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="3a38d-140">Header</span></span><br/> | <dl> <span data-ttu-id="3a38d-141"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a38d-141"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a38d-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a38d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a38d-143">**\_Descripteur D3D12 \_ RANGE1**</span><span class="sxs-lookup"><span data-stu-id="3a38d-143">**D3D12\_DESCRIPTOR\_RANGE1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)
</dt> <dt>

[<span data-ttu-id="3a38d-144">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="3a38d-144">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





