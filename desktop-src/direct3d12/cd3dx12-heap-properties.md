---
title: Structure CD3DX12_HEAP_PROPERTIES (D3dx12. h)
description: Structure d’assistance pour permettre l’initialisation facile d’une structure de \_ Propriétés de tas D3D12 \_ .
ms.assetid: AC759F25-D643-412D-AA83-3A2C040BE64B
keywords:
- Structure CD3DX12_HEAP_PROPERTIES
topic_type:
- apiref
api_name:
- CD3DX12_HEAP_PROPERTIES
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90cc5f5cee6bf70aad064396589aad8a483f2c50
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106520311"
---
# <a name="cd3dx12_heap_properties-structure"></a><span data-ttu-id="da7a6-104">Structure des propriétés du \_ tas CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="da7a6-104">CD3DX12\_HEAP\_PROPERTIES structure</span></span>

<span data-ttu-id="da7a6-105">Structure d’assistance pour permettre l’initialisation facile d’une structure [**de \_ \_ Propriétés de tas D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) .</span><span class="sxs-lookup"><span data-stu-id="da7a6-105">A helper structure to enable easy initialization of a [**D3D12\_HEAP\_PROPERTIES**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="da7a6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da7a6-106">Syntax</span></span>


```C++
struct CD3DX12_HEAP_PROPERTIES  : public D3D12_HEAP_PROPERTIES{
       CD3DX12_HEAP_PROPERTIES();
       explicit CD3DX12_HEAP_PROPERTIES(const D3D12_HEAP_PROPERTIES &o);
       CD3DX12_HEAP_PROPERTIES(D3D12_CPU_PAGE_PROPERTY cpuPageProperty, D3D12_MEMORY_POOL memoryPoolPreference, UINT creationNodeMask = 1, UINT nodeMask = 1);
       explicit CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE type, UINT creationNodeMask = 1, UINT nodeMask = 1);
       operator const D3D12_HEAP_PROPERTIES&() const;
  bool inline operator==( const D3D12_HEAP_PROPERTIES& l, const D3D12_HEAP_PROPERTIES& r );
  bool inline operator!=( const D3D12_HEAP_PROPERTIES& l, const D3D12_HEAP_PROPERTIES& r );
};
```



## <a name="members"></a><span data-ttu-id="da7a6-107">Membres</span><span class="sxs-lookup"><span data-stu-id="da7a6-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="da7a6-108">**\_Propriétés du tas CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="da7a6-108">**CD3DX12\_HEAP\_PROPERTIES()**</span></span>
</dt> <dd>

<span data-ttu-id="da7a6-109">Crée une nouvelle instance non initialisée des propriétés du tas CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="da7a6-109">Creates a new, uninitialized, instance of a CD3DX12\_HEAP\_PROPERTIES.</span></span>

</dd> <dt>

<span data-ttu-id="da7a6-110">**Propriétés du tas CD3DX12 explicites \_ \_ (propriétés du tas const D3D12 \_ \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="da7a6-110">**explicit CD3DX12\_HEAP\_PROPERTIES(const D3D12\_HEAP\_PROPERTIES &o)**</span></span>
</dt> <dd>

<span data-ttu-id="da7a6-111">Crée une nouvelle instance d’une CD3DX12 \_ de \_ Propriétés de tas, initialisée avec le contenu d’une autre structure de [**\_ \_ Propriétés de tas D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) .</span><span class="sxs-lookup"><span data-stu-id="da7a6-111">Creates a new instance of a CD3DX12\_HEAP\_PROPERTIES, initialized with the contents of another [**D3D12\_HEAP\_PROPERTIES**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) structure.</span></span>

</dd> <dt>

<span data-ttu-id="da7a6-112">**CD3DX12 \_ Heap \_ Properties (D3D12 \_ CPU \_ page \_ Property CpuPageProperty, D3D12 \_ Memory \_ pool MEMORYPOOLPREFERENCE, uint creationNodeMask = 1, uint nodeMask = 1)**</span><span class="sxs-lookup"><span data-stu-id="da7a6-112">**CD3DX12\_HEAP\_PROPERTIES(D3D12\_CPU\_PAGE\_PROPERTY cpuPageProperty, D3D12\_MEMORY\_POOL memoryPoolPreference, UINT creationNodeMask = 1, UINT nodeMask = 1)**</span></span>
</dt> <dd>

<span data-ttu-id="da7a6-113">Crée une nouvelle instance d’une CD3DX12 \_ de \_ Propriétés de tas, en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="da7a6-113">Creates a new instance of a CD3DX12\_HEAP\_PROPERTIES, initializing the following parameters:</span></span>

<span data-ttu-id="da7a6-114">[**D3D12 \_ \_ \_ Propriété de page**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) de l’UC cpuPageProperty</span><span class="sxs-lookup"><span data-stu-id="da7a6-114">[**D3D12\_CPU\_PAGE\_PROPERTY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty</span></span>

<span data-ttu-id="da7a6-115">[**D3D12 \_ \_Pool de mémoire**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference</span><span class="sxs-lookup"><span data-stu-id="da7a6-115">[**D3D12\_MEMORY\_POOL**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference</span></span>

<span data-ttu-id="da7a6-116">possibilité UINT creationNodeMask = 1</span><span class="sxs-lookup"><span data-stu-id="da7a6-116">(opt) UINT creationNodeMask = 1</span></span>

<span data-ttu-id="da7a6-117">possibilité UINT nodeMask = 1</span><span class="sxs-lookup"><span data-stu-id="da7a6-117">(opt) UINT nodeMask = 1</span></span>

</dd> <dt>

<span data-ttu-id="da7a6-118">**Propriétés du tas CD3DX12 explicites \_ \_ (type \_ de tas D3D12 \_ , uint CREATIONNODEMASK = 1, uint nodeMask = 1)**</span><span class="sxs-lookup"><span data-stu-id="da7a6-118">**explicit CD3DX12\_HEAP\_PROPERTIES(D3D12\_HEAP\_TYPE type, UINT creationNodeMask = 1, UINT nodeMask = 1)**</span></span>
</dt> <dd>

<span data-ttu-id="da7a6-119">Crée une nouvelle instance d’une CD3DX12 \_ de \_ Propriétés de tas, en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="da7a6-119">Creates a new instance of a CD3DX12\_HEAP\_PROPERTIES, initializing the following parameters:</span></span>

<span data-ttu-id="da7a6-120">[**D3D12 \_ Type \_ de segment de mémoire**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)</span><span class="sxs-lookup"><span data-stu-id="da7a6-120">[**D3D12\_HEAP\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) type</span></span>

<span data-ttu-id="da7a6-121">possibilité UINT creationNodeMask = 1</span><span class="sxs-lookup"><span data-stu-id="da7a6-121">(opt) UINT creationNodeMask = 1</span></span>

<span data-ttu-id="da7a6-122">possibilité UINT nodeMask = 1</span><span class="sxs-lookup"><span data-stu-id="da7a6-122">(opt) UINT nodeMask = 1</span></span>

</dd> <dt>

<span data-ttu-id="da7a6-123">**D3D12 \_ \_ (), const, propriétés de segment de mémoire& () const**</span><span class="sxs-lookup"><span data-stu-id="da7a6-123">**operator const D3D12\_HEAP\_PROPERTIES&() const**</span></span>
</dt> <dd>

<span data-ttu-id="da7a6-124">Définit le & opérateur de passage par référence pour le type de structure parent.</span><span class="sxs-lookup"><span data-stu-id="da7a6-124">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> <dt>

<span data-ttu-id="da7a6-125">**Inline, opérateur = = (const D3D12 \_ segment \_ Properties& l, const D3D12 \_ segment \_ Properties& r)**</span><span class="sxs-lookup"><span data-stu-id="da7a6-125">**inline operator==( const D3D12\_HEAP\_PROPERTIES& l, const D3D12\_HEAP\_PROPERTIES& r )**</span></span>
</dt> <dd>

<span data-ttu-id="da7a6-126">Teste l’égalité entre les \_ \_ instances de propriétés de tas D3D12 spécifiées, en fonction de l’égalité de tous les champs membres.</span><span class="sxs-lookup"><span data-stu-id="da7a6-126">Tests for equality between the specified D3D12\_HEAP\_PROPERTIES instances, based on equality of all member fields.</span></span>

</dd> <dt>

<span data-ttu-id="da7a6-127">**Inline, opérateur ! = (const D3D12 \_ segment \_ Properties& l, const D3D12 \_ segment \_ Properties& r)**</span><span class="sxs-lookup"><span data-stu-id="da7a6-127">**inline operator!=( const D3D12\_HEAP\_PROPERTIES& l, const D3D12\_HEAP\_PROPERTIES& r )**</span></span>
</dt> <dd>

<span data-ttu-id="da7a6-128">Teste l’inégalité entre les instances de propriétés de tas D3D12 spécifiées \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="da7a6-128">Tests for inequality between the specified D3D12\_HEAP\_PROPERTIES instances.</span></span> <span data-ttu-id="da7a6-129">Implémenté par l’inverse de la valeur **Operator = =** .</span><span class="sxs-lookup"><span data-stu-id="da7a6-129">Implemented by taking the inverse of the **operator==** value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="da7a6-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da7a6-130">Requirements</span></span>



| <span data-ttu-id="da7a6-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da7a6-131">Requirement</span></span> | <span data-ttu-id="da7a6-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="da7a6-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="da7a6-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="da7a6-133">Header</span></span><br/> | <dl> <span data-ttu-id="da7a6-134"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="da7a6-134"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da7a6-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da7a6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da7a6-136">**\_Propriétés du tas D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="da7a6-136">**D3D12\_HEAP\_PROPERTIES**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)
</dt> <dt>

[<span data-ttu-id="da7a6-137">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="da7a6-137">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





