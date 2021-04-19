---
title: Structure CD3DX12_ROOT_DESCRIPTOR_TABLE1 (D3dx12. h)
description: Structure d’assistance pour permettre l’initialisation simple d’une \_ \_ structure table1 de descripteur racine D3D12 \_ .
ms.assetid: 82AC1948-92AA-4A4D-B443-717E9BF3046D
keywords:
- Structure CD3DX12_ROOT_DESCRIPTOR_TABLE1
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR_TABLE1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e3538e5e1e199fdb6f8c7473af4996ccd7b7f1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106528772"
---
# <a name="cd3dx12_root_descriptor_table1-structure"></a><span data-ttu-id="1d24d-104">CD3DX12 \_ \_ structure table1 du descripteur racine \_</span><span class="sxs-lookup"><span data-stu-id="1d24d-104">CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1 structure</span></span>

<span data-ttu-id="1d24d-105">Structure d’assistance pour permettre l’initialisation simple d’une structure [**\_ \_ \_ table1 de descripteur racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) .</span><span class="sxs-lookup"><span data-stu-id="1d24d-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_DESCRIPTOR\_TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d24d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d24d-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_DESCRIPTOR_TABLE1  : public D3D12_ROOT_DESCRIPTOR_TABLE1{
       CD3DX12_ROOT_DESCRIPTOR_TABLE1();
       explicit CD3DX12_ROOT_DESCRIPTOR_TABLE1(const D3D12_ROOT_DESCRIPTOR_TABLE1 &o);
       CD3DX12_ROOT_DESCRIPTOR_TABLE1(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
  void inline Init(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
  void static inline Init(D3D12_ROOT_DESCRIPTOR_TABLE1 &rootDescriptorTable, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
};
```



## <a name="members"></a><span data-ttu-id="1d24d-107">Membres</span><span class="sxs-lookup"><span data-stu-id="1d24d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="1d24d-108">**\_Descripteur racine CD3DX12 \_ \_ table1 ()**</span><span class="sxs-lookup"><span data-stu-id="1d24d-108">**CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1()**</span></span>
</dt> <dd>

<span data-ttu-id="1d24d-109">Crée une nouvelle instance non initialisée d’un \_ \_ descripteur racine CD3DX12 \_ table1.</span><span class="sxs-lookup"><span data-stu-id="1d24d-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1.</span></span>

</dd> <dt>

<span data-ttu-id="1d24d-110">**\_descripteur racine CD3DX12 explicite \_ \_ table1 (const D3D12 \_ racine \_ descripteur \_ table1 &o)**</span><span class="sxs-lookup"><span data-stu-id="1d24d-110">**explicit CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1(const D3D12\_ROOT\_DESCRIPTOR\_TABLE1 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="1d24d-111">Crée une nouvelle instance d’un \_ \_ descripteur racine CD3DX12 \_ Table1, initialisée avec le contenu d’une autre structure [**\_ \_ \_ table1 de descripteur racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) .</span><span class="sxs-lookup"><span data-stu-id="1d24d-111">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1, initialized with the contents of another [**D3D12\_ROOT\_DESCRIPTOR\_TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1d24d-112">**\_Descripteur racine CD3DX12 \_ \_ table1 (uint numDescriptorRanges, const D3D12 \_ descripteur \_ RANGE1 \* \_ pDescriptorRanges)**</span><span class="sxs-lookup"><span data-stu-id="1d24d-112">**CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE1\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="1d24d-113">Crée une nouvelle instance d’un \_ \_ descripteur racine CD3DX12 \_ Table1, en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="1d24d-113">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1, initializing the following parameters:</span></span>

<span data-ttu-id="1d24d-114">UINT numDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="1d24d-114">UINT numDescriptorRanges</span></span>

<span data-ttu-id="1d24d-115">const [**D3D12 \_ descripteur \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="1d24d-115">const [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)\* \_pDescriptorRanges</span></span>

</dd> <dt>

<span data-ttu-id="1d24d-116">**Inline init (UINT numDescriptorRanges, const D3D12 \_ descripteur \_ RANGE1 \* \_ pDescriptorRanges)**</span><span class="sxs-lookup"><span data-stu-id="1d24d-116">**inline Init(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE1\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="1d24d-117">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="1d24d-117">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="1d24d-118">UINT numDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="1d24d-118">UINT numDescriptorRanges</span></span>

<span data-ttu-id="1d24d-119">const [**D3D12 \_ descripteur \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="1d24d-119">const [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)\* \_pDescriptorRanges</span></span>

</dd> <dt>

<span data-ttu-id="1d24d-120">**static Inline init ( \_ \_ descripteur racine D3D12 \_ table1 &RootDescriptorTable, uint numDescriptorRanges, const D3D12 \_ description \_ RANGE1 \* \_ pDescriptorRanges)**</span><span class="sxs-lookup"><span data-stu-id="1d24d-120">**static inline Init(D3D12\_ROOT\_DESCRIPTOR\_TABLE1 &rootDescriptorTable, UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE1\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="1d24d-121">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="1d24d-121">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="1d24d-122">[**D3D12 \_ \_Descripteur racine \_ table1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) &rootDescriptorTable</span><span class="sxs-lookup"><span data-stu-id="1d24d-122">[**D3D12\_ROOT\_DESCRIPTOR\_TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) &rootDescriptorTable</span></span>

<span data-ttu-id="1d24d-123">UINT numDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="1d24d-123">UINT numDescriptorRanges</span></span>

<span data-ttu-id="1d24d-124">const [**D3D12 \_ descripteur \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="1d24d-124">const [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)\* \_pDescriptorRanges</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1d24d-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d24d-125">Requirements</span></span>



| <span data-ttu-id="1d24d-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d24d-126">Requirement</span></span> | <span data-ttu-id="1d24d-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d24d-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1d24d-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="1d24d-128">Header</span></span><br/> | <dl> <span data-ttu-id="1d24d-129"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d24d-129"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d24d-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d24d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d24d-131">**\_Descripteur racine D3D12 \_ \_ table1**</span><span class="sxs-lookup"><span data-stu-id="1d24d-131">**D3D12\_ROOT\_DESCRIPTOR\_TABLE1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1)
</dt> <dt>

[<span data-ttu-id="1d24d-132">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="1d24d-132">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





