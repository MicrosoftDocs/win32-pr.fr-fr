---
title: Structure CD3DX12_HEAP_DESC (D3dx12. h)
description: Structure d’assistance pour permettre l’initialisation facile d’une \_ structure DESC du tas D3D12 \_ .
ms.assetid: 38E0BA60-2BB0-4AC1-870A-10AB16E4C6E6
keywords:
- Structure CD3DX12_HEAP_DESC
topic_type:
- apiref
api_name:
- CD3DX12_HEAP_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5b2537d2571355f26c46f03aed3489fb2b6069
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539864"
---
# <a name="cd3dx12_heap_desc-structure"></a><span data-ttu-id="f0b37-104">\_Structure DESC du tas CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="f0b37-104">CD3DX12\_HEAP\_DESC structure</span></span>

<span data-ttu-id="f0b37-105">Structure d’assistance pour permettre l’initialisation facile d’une structure [**\_ \_ desc du tas D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) .</span><span class="sxs-lookup"><span data-stu-id="f0b37-105">A helper structure to enable easy initialization of a [**D3D12\_HEAP\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0b37-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0b37-106">Syntax</span></span>


```C++
struct CD3DX12_HEAP_DESC  : public D3D12_HEAP_DESC{
   CD3DX12_HEAP_DESC();
   explicit CD3DX12_HEAP_DESC(const D3D12_HEAP_DESC &o);
   CD3DX12_HEAP_DESC(UINT64 size, D3D12_HEAP_PROPERTIES properties, UINT64 alignment = 0, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(UINT64 size, D3D12_HEAP_TYPE type, UINT64 alignment = 0, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(UINT64 size, D3D12_CPU_PAGE_PROPERTY cpuPageProperty, D3D12_MEMORY_POOL memoryPoolPreference, UINT64 alignment = 0, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_HEAP_PROPERTIES properties, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_HEAP_TYPE type, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_CPU_PAGE_PROPERTY cpuPageProperty, D3D12_MEMORY_POOL memoryPoolPreference, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   operator const D3D12_HEAP_DESC&() const;
};
```



## <a name="members"></a><span data-ttu-id="f0b37-107">Membres</span><span class="sxs-lookup"><span data-stu-id="f0b37-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="f0b37-108">**CD3DX12 \_ \_ , description du tas ()**</span><span class="sxs-lookup"><span data-stu-id="f0b37-108">**CD3DX12\_HEAP\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="f0b37-109">Crée une nouvelle instance, non initialisée, d’une \_ Description du tas CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="f0b37-109">Creates a new, uninitialized, instance of a CD3DX12\_HEAP\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="f0b37-110">**DESC du \_ tas CD3DX12 explicite \_ (const D3D12 \_ segment \_ desc &o)**</span><span class="sxs-lookup"><span data-stu-id="f0b37-110">**explicit CD3DX12\_HEAP\_DESC(const D3D12\_HEAP\_DESC &o)**</span></span>
</dt> <dd>

<span data-ttu-id="f0b37-111">Crée une nouvelle instance d’une \_ Description du tas CD3DX12 \_ , initialisée avec le contenu d’une autre structure [**\_ \_ desc du tas D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) .</span><span class="sxs-lookup"><span data-stu-id="f0b37-111">Creates a new instance of a CD3DX12\_HEAP\_DESC, initialized with the contents of another [**D3D12\_HEAP\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f0b37-112">**\_Description du tas CD3DX12 \_ (taille de UInt64, propriétés des propriétés du \_ tas D3D12 \_ , alignement de UInt64 = 0, indicateurs de \_ tas D3D12 \_ indicateurs = \_ indicateur de tas D3D12 \_ \_ aucun)**</span><span class="sxs-lookup"><span data-stu-id="f0b37-112">**CD3DX12\_HEAP\_DESC(UINT64 size, D3D12\_HEAP\_PROPERTIES properties, UINT64 alignment = 0, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="f0b37-113">Crée une nouvelle instance d’une \_ Description du tas CD3DX12 \_ , en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="f0b37-113">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="f0b37-114">Taille de UINT64</span><span class="sxs-lookup"><span data-stu-id="f0b37-114">UINT64 size</span></span>

<span data-ttu-id="f0b37-115">[**D3D12 \_ Propriétés des \_ Propriétés du tas**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)</span><span class="sxs-lookup"><span data-stu-id="f0b37-115">[**D3D12\_HEAP\_PROPERTIES**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) properties</span></span>

<span data-ttu-id="f0b37-116">possibilité -Alignement de UINT64 = 0</span><span class="sxs-lookup"><span data-stu-id="f0b37-116">(opt) UINT64 alignment = 0</span></span>

<span data-ttu-id="f0b37-117">possibilité [**D3D12 \_ Indicateurs \_ de tas**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) indicateurs = \_ indicateur de tas D3D12 \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="f0b37-117">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="f0b37-118">**\_Description du tas CD3DX12 (taille de type de segment de mémoire \_ , type de \_ tas D3D12 \_ , alignement de UInt64 = 0, indicateurs de \_ tas D3D12 \_ indicateurs = \_ indicateur de tas D3D12 \_ \_ aucun)**</span><span class="sxs-lookup"><span data-stu-id="f0b37-118">**CD3DX12\_HEAP\_DESC(UINT64 size, D3D12\_HEAP\_TYPE type, UINT64 alignment = 0, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="f0b37-119">Crée une nouvelle instance d’une \_ Description du tas CD3DX12 \_ , en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="f0b37-119">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="f0b37-120">Taille de UINT64</span><span class="sxs-lookup"><span data-stu-id="f0b37-120">UINT64 size</span></span>

<span data-ttu-id="f0b37-121">[**D3D12 \_ Type \_ de segment de mémoire**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)</span><span class="sxs-lookup"><span data-stu-id="f0b37-121">[**D3D12\_HEAP\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) type</span></span>

<span data-ttu-id="f0b37-122">possibilité -Alignement de UINT64 = 0</span><span class="sxs-lookup"><span data-stu-id="f0b37-122">(opt) UINT64 alignment = 0</span></span>

<span data-ttu-id="f0b37-123">possibilité [**D3D12 \_ Indicateurs \_ de tas**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) indicateurs = \_ indicateur de tas D3D12 \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="f0b37-123">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="f0b37-124">**CD3DX12 \_ Heap \_ desc (taille de UINT64, \_ propriété de page D3D12 CPU \_ \_ cpuPageProperty, D3D12 \_ pool de mémoire \_ memoryPoolPreference, UInt64 Alignment = 0, D3D12 \_ segment \_ Flags Flags = D3D12 \_ indicateur de tas \_ \_ None)**</span><span class="sxs-lookup"><span data-stu-id="f0b37-124">**CD3DX12\_HEAP\_DESC(UINT64 size, D3D12\_CPU\_PAGE\_PROPERTY cpuPageProperty, D3D12\_MEMORY\_POOL memoryPoolPreference, UINT64 alignment = 0, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="f0b37-125">Crée une nouvelle instance d’une \_ Description du tas CD3DX12 \_ , en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="f0b37-125">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="f0b37-126">Taille de UINT64</span><span class="sxs-lookup"><span data-stu-id="f0b37-126">UINT64 size</span></span>

<span data-ttu-id="f0b37-127">[**D3D12 \_ \_ \_ Propriété de page**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) de l’UC cpuPageProperty</span><span class="sxs-lookup"><span data-stu-id="f0b37-127">[**D3D12\_CPU\_PAGE\_PROPERTY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty</span></span>

<span data-ttu-id="f0b37-128">[**D3D12 \_ \_Pool de mémoire**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference</span><span class="sxs-lookup"><span data-stu-id="f0b37-128">[**D3D12\_MEMORY\_POOL**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference</span></span>

<span data-ttu-id="f0b37-129">possibilité -Alignement de UINT64 = 0</span><span class="sxs-lookup"><span data-stu-id="f0b37-129">(opt) UINT64 alignment = 0</span></span>

<span data-ttu-id="f0b37-130">possibilité [**D3D12 \_ Indicateurs \_ de tas**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) indicateurs = \_ indicateur de tas D3D12 \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="f0b37-130">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="f0b37-131">**CD3DX12 \_ segment \_ desc (CONSt D3D12 \_ Resource \_ allocation \_ info& resAllocInfo, propriétés \_ Propriétés du tas D3D12 \_ , D3D12 \_ segments \_ indicateurs indicateurs = D3D12, \_ indicateur de tas \_ \_ aucun)**</span><span class="sxs-lookup"><span data-stu-id="f0b37-131">**CD3DX12\_HEAP\_DESC(const D3D12\_RESOURCE\_ALLOCATION\_INFO& resAllocInfo, D3D12\_HEAP\_PROPERTIES properties, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="f0b37-132">Crée une nouvelle instance d’une \_ Description du tas CD3DX12 \_ , en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="f0b37-132">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="f0b37-133">[**D3D12 \_ \_ \_ Informations d’allocation de ressources**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span><span class="sxs-lookup"><span data-stu-id="f0b37-133">[**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span></span>

<span data-ttu-id="f0b37-134">[**D3D12 \_ Propriétés des \_ Propriétés du tas**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)</span><span class="sxs-lookup"><span data-stu-id="f0b37-134">[**D3D12\_HEAP\_PROPERTIES**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) properties</span></span>

<span data-ttu-id="f0b37-135">possibilité [**D3D12 \_ Indicateurs \_ de tas**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) indicateurs = \_ indicateur de tas D3D12 \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="f0b37-135">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="f0b37-136">**CD3DX12 \_ segment \_ desc (CONSt D3D12 \_ Resource \_ allocation \_ info& resAllocInfo, D3D12 type \_ \_ de tas, D3D12 \_ segment \_ Flags Flags = D3D12 \_ Heap \_ drapeau \_ None)**</span><span class="sxs-lookup"><span data-stu-id="f0b37-136">**CD3DX12\_HEAP\_DESC(const D3D12\_RESOURCE\_ALLOCATION\_INFO& resAllocInfo, D3D12\_HEAP\_TYPE type, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="f0b37-137">Crée une nouvelle instance d’une \_ Description du tas CD3DX12 \_ , en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="f0b37-137">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="f0b37-138">[**D3D12 \_ \_ \_ Informations d’allocation de ressources**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span><span class="sxs-lookup"><span data-stu-id="f0b37-138">[**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span></span>

<span data-ttu-id="f0b37-139">[**D3D12 \_ Type \_ de segment de mémoire**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)</span><span class="sxs-lookup"><span data-stu-id="f0b37-139">[**D3D12\_HEAP\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) type</span></span>

<span data-ttu-id="f0b37-140">possibilité [**D3D12 \_ Indicateurs \_ de tas**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) indicateurs = \_ indicateur de tas D3D12 \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="f0b37-140">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="f0b37-141">**CD3DX12 \_ Heap \_ desc (CONSt D3D12 \_ Resource \_ allocation \_ info& resAllocInfo, D3D12 \_ CPU \_ page \_ Property cpuPageProperty, \_ D3D12 \_ pool Memory memoryPoolPreference, D3D12 \_ Heap \_ Flags Flags = D3D12 \_ Heap \_ drapeau \_ None)**</span><span class="sxs-lookup"><span data-stu-id="f0b37-141">**CD3DX12\_HEAP\_DESC(const D3D12\_RESOURCE\_ALLOCATION\_INFO& resAllocInfo, D3D12\_CPU\_PAGE\_PROPERTY cpuPageProperty, D3D12\_MEMORY\_POOL memoryPoolPreference, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="f0b37-142">Crée une nouvelle instance d’une \_ Description du tas CD3DX12 \_ , en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="f0b37-142">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="f0b37-143">[**D3D12 \_ \_ \_ Informations d’allocation de ressources**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span><span class="sxs-lookup"><span data-stu-id="f0b37-143">[**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span></span>

<span data-ttu-id="f0b37-144">[**D3D12 \_ \_ \_ Propriété de page**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) de l’UC cpuPageProperty</span><span class="sxs-lookup"><span data-stu-id="f0b37-144">[**D3D12\_CPU\_PAGE\_PROPERTY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty</span></span>

<span data-ttu-id="f0b37-145">[**D3D12 \_ \_Pool de mémoire**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference</span><span class="sxs-lookup"><span data-stu-id="f0b37-145">[**D3D12\_MEMORY\_POOL**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference</span></span>

<span data-ttu-id="f0b37-146">possibilité [**D3D12 \_ Indicateurs \_ de tas**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) indicateurs = \_ indicateur de tas D3D12 \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="f0b37-146">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="f0b37-147">**const D3D12 \_ \_ , description du tas& () const**</span><span class="sxs-lookup"><span data-stu-id="f0b37-147">**operator const D3D12\_HEAP\_DESC&() const**</span></span>
</dt> <dd>

<span data-ttu-id="f0b37-148">Définit le & opérateur de passage par référence pour le type de \_ structure DESC du tas CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="f0b37-148">Defines the & pass-by-reference operator for the CD3DX12\_HEAP\_DESC structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f0b37-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0b37-149">Requirements</span></span>



| <span data-ttu-id="f0b37-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f0b37-150">Requirement</span></span> | <span data-ttu-id="f0b37-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="f0b37-151">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f0b37-152">En-tête</span><span class="sxs-lookup"><span data-stu-id="f0b37-152">Header</span></span><br/> | <dl> <span data-ttu-id="f0b37-153"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0b37-153"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0b37-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0b37-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0b37-155">**\_Description du tas D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="f0b37-155">**D3D12\_HEAP\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc)
</dt> <dt>

[<span data-ttu-id="f0b37-156">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="f0b37-156">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





