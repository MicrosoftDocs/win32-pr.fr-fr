---
title: Structure CD3DX12_RESOURCE_ALLOCATION_INFO (D3dx12. h)
description: Structure d’assistance pour faciliter l’initialisation d’une \_ structure d’informations d’allocation de ressources D3D12 \_ \_ .
ms.assetid: 81FC8D0E-2C15-42D3-9E06-1FE193F707C6
keywords:
- Structure CD3DX12_RESOURCE_ALLOCATION_INFO
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_ALLOCATION_INFO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08542c7460b2fadf381f85dc271167258e31fb46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535162"
---
# <a name="cd3dx12_resource_allocation_info-structure"></a><span data-ttu-id="f9e2c-104">\_Structure d' \_ informations d’allocation de ressources CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="f9e2c-104">CD3DX12\_RESOURCE\_ALLOCATION\_INFO structure</span></span>

<span data-ttu-id="f9e2c-105">Structure d’assistance pour faciliter l’initialisation d’une structure d' [**\_ informations d' \_ allocation \_ de ressources D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) .</span><span class="sxs-lookup"><span data-stu-id="f9e2c-105">A helper structure to enable easy initialization of a [**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9e2c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f9e2c-106">Syntax</span></span>


```C++
struct CD3DX12_RESOURCE_ALLOCATION_INFO  : public D3D12_RESOURCE_ALLOCATION_INFO{
   CD3DX12_RESOURCE_ALLOCATION_INFO();
   explicit CD3DX12_RESOURCE_ALLOCATION_INFO(const D3D12_RESOURCE_ALLOCATION_INFO& o);
   CD3DX12_RESOURCE_ALLOCATION_INFO(UINT64 size, UINT64 alignment);
   operator const D3D12_RESOURCE_ALLOCATION_INFO&() const;
};
```



## <a name="members"></a><span data-ttu-id="f9e2c-107">Membres</span><span class="sxs-lookup"><span data-stu-id="f9e2c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="f9e2c-108">**\_Informations d' \_ allocation de ressources CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="f9e2c-108">**CD3DX12\_RESOURCE\_ALLOCATION\_INFO()**</span></span>
</dt> <dd>

<span data-ttu-id="f9e2c-109">Crée une nouvelle instance non initialisée d’informations d’allocation de \_ ressources \_ CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="f9e2c-109">Creates a new, uninitialized, instance of a CD3DX12\_RESOURCE\_ALLOCATION\_INFO.</span></span>

</dd> <dt>

<span data-ttu-id="f9e2c-110">**informations d’allocation de ressources explicites CD3DX12 \_ \_ \_ (const D3D12 \_ resource \_ allocation \_ info& o)**</span><span class="sxs-lookup"><span data-stu-id="f9e2c-110">**explicit CD3DX12\_RESOURCE\_ALLOCATION\_INFO(const D3D12\_RESOURCE\_ALLOCATION\_INFO& o)**</span></span>
</dt> <dd>

<span data-ttu-id="f9e2c-111">Crée une nouvelle instance d’informations d' \_ allocation de ressources CD3DX12 \_ \_ , initialisée avec le contenu d’une autre structure d' [**\_ informations d' \_ allocation \_ de ressources D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) .</span><span class="sxs-lookup"><span data-stu-id="f9e2c-111">Creates a new instance of a CD3DX12\_RESOURCE\_ALLOCATION\_INFO, initialized with the contents of another [**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f9e2c-112">**\_Informations d' \_ allocation de ressources CD3DX12 \_ (taille UINT64, alignement UInt64)**</span><span class="sxs-lookup"><span data-stu-id="f9e2c-112">**CD3DX12\_RESOURCE\_ALLOCATION\_INFO(UINT64 size, UINT64 alignment)**</span></span>
</dt> <dd>

<span data-ttu-id="f9e2c-113">Crée une nouvelle instance d’informations d' \_ allocation de ressources CD3DX12 \_ \_ , en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="f9e2c-113">Creates a new instance of a CD3DX12\_RESOURCE\_ALLOCATION\_INFO, initializing the following parameters:</span></span>

<span data-ttu-id="f9e2c-114">Taille de UINT64</span><span class="sxs-lookup"><span data-stu-id="f9e2c-114">UINT64 size</span></span>

<span data-ttu-id="f9e2c-115">Alignement de UINT64</span><span class="sxs-lookup"><span data-stu-id="f9e2c-115">UINT64 alignment</span></span>

</dd> <dt>

<span data-ttu-id="f9e2c-116">**\_const D3D12 Resource \_ ALLOCATION \_ info& () const**</span><span class="sxs-lookup"><span data-stu-id="f9e2c-116">**operator const D3D12\_RESOURCE\_ALLOCATION\_INFO&() const**</span></span>
</dt> <dd>

<span data-ttu-id="f9e2c-117">Définit le & opérateur de passage par référence pour le type de structure parent.</span><span class="sxs-lookup"><span data-stu-id="f9e2c-117">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f9e2c-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9e2c-118">Requirements</span></span>



| <span data-ttu-id="f9e2c-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9e2c-119">Requirement</span></span> | <span data-ttu-id="f9e2c-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9e2c-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f9e2c-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="f9e2c-121">Header</span></span><br/> | <dl> <span data-ttu-id="f9e2c-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9e2c-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9e2c-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9e2c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9e2c-124">**\_Informations d' \_ allocation de ressources D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="f9e2c-124">**D3D12\_RESOURCE\_ALLOCATION\_INFO**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
</dt> <dt>

[<span data-ttu-id="f9e2c-125">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="f9e2c-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





