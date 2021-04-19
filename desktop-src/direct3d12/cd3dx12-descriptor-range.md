---
title: Structure CD3DX12_DESCRIPTOR_RANGE (D3dx12. h)
description: Structure d’assistance pour faciliter l’initialisation d’une \_ structure de plage de descripteur D3D12 \_ .
ms.assetid: F066ECA5-5E52-4483-B773-B43C5F12809B
keywords:
- Structure CD3DX12_DESCRIPTOR_RANGE
topic_type:
- apiref
api_name:
- CD3DX12_DESCRIPTOR_RANGE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b511af1766daaefa7f92d33b71841b3a69c99927
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539428"
---
# <a name="cd3dx12_descriptor_range-structure"></a><span data-ttu-id="34951-104">Structure de la \_ plage du descripteur CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="34951-104">CD3DX12\_DESCRIPTOR\_RANGE structure</span></span>

<span data-ttu-id="34951-105">Structure d’assistance pour faciliter l’initialisation d’une structure de [**\_ \_ plage de descripteur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) .</span><span class="sxs-lookup"><span data-stu-id="34951-105">A helper structure to enable easy initialization of a [**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="34951-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="34951-106">Syntax</span></span>


```C++
struct CD3DX12_DESCRIPTOR_RANGE  : public D3D12_DESCRIPTOR_RANGE{
       CD3DX12_DESCRIPTOR_RANGE();
       explicit CD3DX12_DESCRIPTOR_RANGE(const D3D12_DESCRIPTOR_RANGE &o);
       CD3DX12_DESCRIPTOR_RANGE(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void inline Init(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void static inline Init(D3D12_DESCRIPTOR_RANGE &range, D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
};
```



## <a name="members"></a><span data-ttu-id="34951-107">Membres</span><span class="sxs-lookup"><span data-stu-id="34951-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="34951-108">**\_Plage du descripteur CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="34951-108">**CD3DX12\_DESCRIPTOR\_RANGE()**</span></span>
</dt> <dd>

<span data-ttu-id="34951-109">Crée une nouvelle instance non initialisée d’une \_ plage de descripteurs D3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="34951-109">Creates a new, uninitialized, instance of a D3DX12\_DESCRIPTOR\_RANGE.</span></span>

</dd> <dt>

<span data-ttu-id="34951-110">**plage du \_ descripteur CD3DX12 explicite \_ ( \_ plage du descripteur const D3D12 \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="34951-110">**explicit CD3DX12\_DESCRIPTOR\_RANGE(const D3D12\_DESCRIPTOR\_RANGE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="34951-111">Crée une nouvelle instance d’une \_ plage de descripteurs D3DX12 \_ , initialisée avec le contenu d’une autre structure de la [**\_ \_ plage du descripteur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) .</span><span class="sxs-lookup"><span data-stu-id="34951-111">Creates a new instance of a D3DX12\_DESCRIPTOR\_RANGE, initialized with the contents of another [**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) structure.</span></span>

</dd> <dt>

<span data-ttu-id="34951-112">**\_Plage du descripteur CD3DX12 \_ ( \_ type de plage de descripteur D3D12 \_ \_ RANGETYPE, uint NUMDESCRIPTORS, uint baseShaderRegister, UINT RegisterSpace = 0, uint offsetInDescriptorsFromTableStart = D3D12 \_ \_ Append décalage de la plage du descripteur \_ \_ )**</span><span class="sxs-lookup"><span data-stu-id="34951-112">**CD3DX12\_DESCRIPTOR\_RANGE(D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="34951-113">Crée une nouvelle instance d’une \_ plage de descripteurs D3DX12 \_ , en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="34951-113">Creates a new instance of a D3DX12\_DESCRIPTOR\_RANGE, initializing the following parameters:</span></span>

<span data-ttu-id="34951-114">[**D3D12 \_ \_ \_ Type de plage de descripteur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span><span class="sxs-lookup"><span data-stu-id="34951-114">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="34951-115">UINT numDescriptors</span><span class="sxs-lookup"><span data-stu-id="34951-115">UINT numDescriptors</span></span>

<span data-ttu-id="34951-116">UINT baseShaderRegister</span><span class="sxs-lookup"><span data-stu-id="34951-116">UINT baseShaderRegister</span></span>

<span data-ttu-id="34951-117">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="34951-117">UINT registerSpace = 0</span></span>

<span data-ttu-id="34951-118">UINT offsetInDescriptorsFromTableStart = D3D12 \_ descripteur de décalage de la plage de descripteurs \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="34951-118">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> <dt>

<span data-ttu-id="34951-119">**Inline init ( \_ type de plage de descripteur D3D12 \_ \_ RangeType, UINT NumDescriptors, UINT BaseShaderRegister, uint registerSpace = 0, uint offsetInDescriptorsFromTableStart = D3D12 de décalage de la \_ plage du descripteur \_ \_ \_ append)**</span><span class="sxs-lookup"><span data-stu-id="34951-119">**inline Init(D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="34951-120">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="34951-120">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="34951-121">[**D3D12 \_ \_ \_ Type de plage de descripteur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span><span class="sxs-lookup"><span data-stu-id="34951-121">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="34951-122">UINT numDescriptors</span><span class="sxs-lookup"><span data-stu-id="34951-122">UINT numDescriptors</span></span>

<span data-ttu-id="34951-123">UINT baseShaderRegister</span><span class="sxs-lookup"><span data-stu-id="34951-123">UINT baseShaderRegister</span></span>

<span data-ttu-id="34951-124">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="34951-124">UINT registerSpace = 0</span></span>

<span data-ttu-id="34951-125">UINT offsetInDescriptorsFromTableStart = D3D12 \_ descripteur de décalage de la plage de descripteurs \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="34951-125">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> <dt>

<span data-ttu-id="34951-126">**static Inline init ( \_ plage du descripteur D3D12 \_ &Range, D3D12 \_ descripteur \_ \_ type RANGETYPE, uint NUMDESCRIPTORS, uint baseShaderRegister, UINT RegisterSpace = 0, uint offsetInDescriptorsFromTableStart = D3D12 décalage de la \_ plage du descripteur \_ \_ \_ append)**</span><span class="sxs-lookup"><span data-stu-id="34951-126">**static inline Init(D3D12\_DESCRIPTOR\_RANGE &range, D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="34951-127">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="34951-127">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="34951-128">[**D3D12 \_ Plage \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) de &de la plage de descripteurs</span><span class="sxs-lookup"><span data-stu-id="34951-128">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) &range</span></span>

<span data-ttu-id="34951-129">[**D3D12 \_ \_ \_ Type de plage de descripteur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span><span class="sxs-lookup"><span data-stu-id="34951-129">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="34951-130">UINT numDescriptors</span><span class="sxs-lookup"><span data-stu-id="34951-130">UINT numDescriptors</span></span>

<span data-ttu-id="34951-131">UINT baseShaderRegister</span><span class="sxs-lookup"><span data-stu-id="34951-131">UINT baseShaderRegister</span></span>

<span data-ttu-id="34951-132">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="34951-132">UINT registerSpace = 0</span></span>

<span data-ttu-id="34951-133">UINT offsetInDescriptorsFromTableStart = D3D12 \_ descripteur de décalage de la plage de descripteurs \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="34951-133">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="34951-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="34951-134">Requirements</span></span>



| <span data-ttu-id="34951-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="34951-135">Requirement</span></span> | <span data-ttu-id="34951-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="34951-136">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="34951-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="34951-137">Header</span></span><br/> | <dl> <span data-ttu-id="34951-138"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="34951-138"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34951-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34951-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34951-140">**\_Plage du descripteur D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="34951-140">**D3D12\_DESCRIPTOR\_RANGE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)
</dt> <dt>

[<span data-ttu-id="34951-141">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="34951-141">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





