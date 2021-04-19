---
title: Structure CD3DX12_RESOURCE_BARRIER (D3dx12. h)
description: Structure d’assistance pour faciliter l’initialisation d’une \_ structure de barrière de ressources D3D12 \_ .
ms.assetid: 89E0F38C-8802-46E6-9583-95C5D853CD99
keywords:
- Structure CD3DX12_RESOURCE_BARRIER
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_BARRIER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eaa9b19a8bc7dcebba5982313bb362dbcee6157
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106528574"
---
# <a name="cd3dx12_resource_barrier-structure"></a><span data-ttu-id="0e650-104">CD3DX12 \_ structure de cloisonnement des ressources \_</span><span class="sxs-lookup"><span data-stu-id="0e650-104">CD3DX12\_RESOURCE\_BARRIER structure</span></span>

<span data-ttu-id="0e650-105">Structure d’assistance pour faciliter l’initialisation d’une structure de [**\_ \_ barrière de ressources D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier) .</span><span class="sxs-lookup"><span data-stu-id="0e650-105">A helper structure to enable easy initialization of a [**D3D12\_RESOURCE\_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e650-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e650-106">Syntax</span></span>


```C++
struct CD3DX12_RESOURCE_BARRIER  : public D3D12_RESOURCE_BARRIER{
                           CD3DX12_RESOURCE_BARRIER();
                           explicit CD3DX12_RESOURCE_BARRIER(const D3D12_RESOURCE_BARRIER &o);
  CD3DX12_RESOURCE_BARRIER static inline Transition(ID3D12Resource* pResource, D3D12_RESOURCE_STATES stateBefore, D3D12_RESOURCE_STATES stateAfter, UINT subresource = D3D12_RESOURCE_BARRIER_ALL_SUBRESOURCES, D3D12_RESOURCE_BARRIER_FLAGS flags = D3D12_RESOURCE_BARRIER_FLAG_NONE);
  CD3DX12_RESOURCE_BARRIER static inline Aliasing(ID3D12Resource* pResourceBefore, ID3D12Resource* pResourceAfter);
  CD3DX12_RESOURCE_BARRIER static inline UAV(ID3D12Resource* pResource);
                           operator const D3D12_RESOURCE_BARRIER&() const;
};
```



## <a name="members"></a><span data-ttu-id="0e650-107">Membres</span><span class="sxs-lookup"><span data-stu-id="0e650-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="0e650-108">**\_Barrière des ressources CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="0e650-108">**CD3DX12\_RESOURCE\_BARRIER()**</span></span>
</dt> <dd>

<span data-ttu-id="0e650-109">Crée une nouvelle instance non initialisée d’un \_ cloisonnement de ressources CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="0e650-109">Creates a new, uninitialized, instance of a CD3DX12\_RESOURCE\_BARRIER.</span></span>

</dd> <dt>

<span data-ttu-id="0e650-110">**\_barrière de ressources CD3DX12 explicite \_ (barrière de ressources const D3D12 \_ \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="0e650-110">**explicit CD3DX12\_RESOURCE\_BARRIER(const D3D12\_RESOURCE\_BARRIER &o)**</span></span>
</dt> <dd>

<span data-ttu-id="0e650-111">Crée une nouvelle instance d’une \_ barrière de ressources CD3DX12 \_ , initialisée avec le contenu d’un autre [**\_ \_ cloisonnement de ressources D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier).</span><span class="sxs-lookup"><span data-stu-id="0e650-111">Creates a new instance of a CD3DX12\_RESOURCE\_BARRIER, initialized with the contents of another [**D3D12\_RESOURCE\_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier).</span></span>

</dd> <dt>

<span data-ttu-id="0e650-112">**Transition statique statique (ID3D12Resource \* présource, D3D12 \_ États des ressources \_ stateBefore, D3D12 des \_ États des ressources \_ stateAfter, uint Resource = D3D12 Resource \_ \_ barrière toutes les sous- \_ \_ ressources, D3D12 \_ indicateurs de barrière des ressources \_ \_ indicateurs = D3D12 \_ indicateur de barrière des ressources \_ \_ \_ aucun)**</span><span class="sxs-lookup"><span data-stu-id="0e650-112">**static inline Transition(ID3D12Resource\* pResource, D3D12\_RESOURCE\_STATES stateBefore, D3D12\_RESOURCE\_STATES stateAfter, UINT subresource = D3D12\_RESOURCE\_BARRIER\_ALL\_SUBRESOURCES, D3D12\_RESOURCE\_BARRIER\_FLAGS flags = D3D12\_RESOURCE\_BARRIER\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="0e650-113">Les transitions entre les États des ressources, à l’aide des paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="0e650-113">Transitions between resource states, using the following parameters:</span></span>

<span data-ttu-id="0e650-114">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* Préversion</span><span class="sxs-lookup"><span data-stu-id="0e650-114">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pResource</span></span>

<span data-ttu-id="0e650-115">[**D3D12 \_ \_États des ressources**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) stateBefore</span><span class="sxs-lookup"><span data-stu-id="0e650-115">[**D3D12\_RESOURCE\_STATES**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) stateBefore</span></span>

<span data-ttu-id="0e650-116">[**D3D12 \_ \_États des ressources**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) stateAfter</span><span class="sxs-lookup"><span data-stu-id="0e650-116">[**D3D12\_RESOURCE\_STATES**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) stateAfter</span></span>

<span data-ttu-id="0e650-117">possibilité UINT Resource = D3D12 Resource [ **\_ \_ barrière \_ toutes les \_** sous-ressources](constants.md)</span><span class="sxs-lookup"><span data-stu-id="0e650-117">(opt) UINT subresource = [**D3D12\_RESOURCE\_BARRIER\_ALL\_SUBRESOURCES**](constants.md)</span></span>

<span data-ttu-id="0e650-118">possibilité [**D3D12 \_ Indicateurs \_ de \_ cloisonnement des ressources**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags) indicateurs = \_ indicateur de cloisonnement des ressources D3D12 \_ \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="0e650-118">(opt) [**D3D12\_RESOURCE\_BARRIER\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags) flags = D3D12\_RESOURCE\_BARRIER\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="0e650-119">**Alias Inline statique (ID3D12Resource \* pResourceBefore, ID3D12Resource \* pResourceAfter)**</span><span class="sxs-lookup"><span data-stu-id="0e650-119">**static inline Aliasing(ID3D12Resource\* pResourceBefore, ID3D12Resource\* pResourceAfter)**</span></span>
</dt> <dd>

<span data-ttu-id="0e650-120">Crée des alias pour la ressource avant et après la transition de barrière.</span><span class="sxs-lookup"><span data-stu-id="0e650-120">Creates aliases for the resource before and after the barrier transition.</span></span> <span data-ttu-id="0e650-121">Paramètres :</span><span class="sxs-lookup"><span data-stu-id="0e650-121">Parameters:</span></span>

<span data-ttu-id="0e650-122">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pResourceBefore</span><span class="sxs-lookup"><span data-stu-id="0e650-122">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pResourceBefore</span></span>

<span data-ttu-id="0e650-123">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pResourceAfter</span><span class="sxs-lookup"><span data-stu-id="0e650-123">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pResourceAfter</span></span>

</dd> <dt>

<span data-ttu-id="0e650-124">**static Inline UAV ( \* présource ID3D12Resource)**</span><span class="sxs-lookup"><span data-stu-id="0e650-124">**static inline UAV(ID3D12Resource\* pResource)**</span></span>
</dt> <dd>

<span data-ttu-id="0e650-125">Crée un mode d’accès non ordonné (UAV) pour la ressource.</span><span class="sxs-lookup"><span data-stu-id="0e650-125">Creates an unordered-access-view (UAV) for the resource.</span></span> <span data-ttu-id="0e650-126">Paramètres :</span><span class="sxs-lookup"><span data-stu-id="0e650-126">Parameters:</span></span>

<span data-ttu-id="0e650-127">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* Préversion</span><span class="sxs-lookup"><span data-stu-id="0e650-127">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pResource</span></span>

</dd> <dt>

<span data-ttu-id="0e650-128">**D3D12, const \_ \_ , opérateur de& cloisonnement de ressources () const**</span><span class="sxs-lookup"><span data-stu-id="0e650-128">**operator const D3D12\_RESOURCE\_BARRIER&() const**</span></span>
</dt> <dd>

<span data-ttu-id="0e650-129">Définit le & opérateur de passage par référence pour le type de structure parent.</span><span class="sxs-lookup"><span data-stu-id="0e650-129">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0e650-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e650-130">Requirements</span></span>



| <span data-ttu-id="0e650-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e650-131">Requirement</span></span> | <span data-ttu-id="0e650-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e650-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0e650-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="0e650-133">Header</span></span><br/> | <dl> <span data-ttu-id="0e650-134"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e650-134"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e650-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e650-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e650-136">**\_Barrière des ressources D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="0e650-136">**D3D12\_RESOURCE\_BARRIER**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier)
</dt> <dt>

[<span data-ttu-id="0e650-137">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="0e650-137">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





