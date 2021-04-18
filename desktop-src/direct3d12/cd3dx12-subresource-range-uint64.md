---
title: Structure CD3DX12_SUBRESOURCE_RANGE_UINT64 (D3dx12. h)
description: Une structure d’assistance pour faciliter l’initialisation d’une structure de sous- \_ ressource D3D12 \_ \_ UINT64.
ms.assetid: 607A60ED-98D2-4A77-9A7A-6B54342EA101
keywords:
- Structure CD3DX12_SUBRESOURCE_RANGE_UINT64
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_RANGE_UINT64
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2aea83d993c0c7b58ded8d0b92374d1dcbacdcc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527090"
---
# <a name="cd3dx12_subresource_range_uint64-structure"></a><span data-ttu-id="5ca29-104">CD3DX12, plage de sous- \_ ressource \_ UINT64, \_ structure</span><span class="sxs-lookup"><span data-stu-id="5ca29-104">CD3DX12\_SUBRESOURCE\_RANGE\_UINT64 structure</span></span>

<span data-ttu-id="5ca29-105">Une structure d’assistance pour faciliter l’initialisation d’une structure de sous- [**\_ ressource D3D12 \_ \_ UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) .</span><span class="sxs-lookup"><span data-stu-id="5ca29-105">A helper structure to enable easy initialization of a [**D3D12\_SUBRESOURCE\_RANGE\_UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ca29-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ca29-106">Syntax</span></span>


```C++
struct CD3DX12_SUBRESOURCE_RANGE_UINT64  : public D3D12_SUBRESOURCE_RANGE_UINT64{
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64();
  CD3DX12_SUBRESOURCE_RANGE_UINT64 explicit CD3DX12_SUBRESOURCE_RANGE_UINT64(const D3D12_SUBRESOURCE_RANGE_UINT64 &o);
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64(UINT subresource, const D3D12_RANGE_UINT64& range);
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64(UINT subresource, UINT64 begin, UINT64 end);
                                   operator const D3D12_SUBRESOURCE_RANGE_UINT64&() const;
};
```



## <a name="members"></a><span data-ttu-id="5ca29-107">Membres</span><span class="sxs-lookup"><span data-stu-id="5ca29-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="5ca29-108">**\_ \_ Plage de sous-ressources CD3DX12 \_ UINT64 ()**</span><span class="sxs-lookup"><span data-stu-id="5ca29-108">**CD3DX12\_SUBRESOURCE\_RANGE\_UINT64()**</span></span>
</dt> <dd>

<span data-ttu-id="5ca29-109">Crée une nouvelle instance non initialisée d’une plage de sous- \_ ressources \_ CD3DX12 \_ UINT64.</span><span class="sxs-lookup"><span data-stu-id="5ca29-109">Creates a new, uninitialized, instance of a CD3DX12\_SUBRESOURCE\_RANGE\_UINT64.</span></span>

</dd> <dt>

<span data-ttu-id="5ca29-110">**\_plage de sous-ressources CD3DX12 explicite \_ \_ UInt64 (const D3D12, plage de sous- \_ ressources \_ \_ UInt64 &o)**</span><span class="sxs-lookup"><span data-stu-id="5ca29-110">**explicit CD3DX12\_SUBRESOURCE\_RANGE\_UINT64(const D3D12\_SUBRESOURCE\_RANGE\_UINT64 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="5ca29-111">Crée une nouvelle instance d’une plage de sous- \_ ressources CD3DX12 \_ \_ UInt64, initialisée avec des valeurs copiées à partir d’une structure de sous- [**\_ ressource D3D12 \_ \_ UInt64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) .</span><span class="sxs-lookup"><span data-stu-id="5ca29-111">Creates a new instance of a CD3DX12\_SUBRESOURCE\_RANGE\_UINT64, initialized with values copied from a [**D3D12\_SUBRESOURCE\_RANGE\_UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5ca29-112">**\_Plage de sous-ressources CD3DX12 \_ \_ UInt64 (uint Resource, const D3D12 \_ plage \_ UInt64& plage)**</span><span class="sxs-lookup"><span data-stu-id="5ca29-112">**CD3DX12\_SUBRESOURCE\_RANGE\_UINT64(UINT subresource, const D3D12\_RANGE\_UINT64& range)**</span></span>
</dt> <dd>

<span data-ttu-id="5ca29-113">Crée une nouvelle instance d’un \_ stencil de profondeur CD3DX12 \_ \_ DESC1, initialisée avec les valeurs passées dans la liste de paramètres.</span><span class="sxs-lookup"><span data-stu-id="5ca29-113">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with the values passed in the parameter list.</span></span>

</dd> <dt>

<span data-ttu-id="5ca29-114">**CD3DX12 \_ sous-ressource de \_ groupe \_ de ressources UINT64 (uint Resource, UInt64 Begin, UInt64 end)**</span><span class="sxs-lookup"><span data-stu-id="5ca29-114">**CD3DX12\_SUBRESOURCE\_RANGE\_UINT64(UINT subresource, UINT64 begin, UINT64 end)**</span></span>
</dt> <dd>

<span data-ttu-id="5ca29-115">Crée une nouvelle instance d’un \_ stencil de profondeur CD3DX12 \_ \_ DESC1, initialisée avec les valeurs passées dans la liste de paramètres.</span><span class="sxs-lookup"><span data-stu-id="5ca29-115">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with the values passed in the parameter list.</span></span>

</dd> <dt>

<span data-ttu-id="5ca29-116">**D3D12, opérateur const \_ \_ , plage \_ de sous-ressources UINT64& () const**</span><span class="sxs-lookup"><span data-stu-id="5ca29-116">**operator const D3D12\_SUBRESOURCE\_RANGE\_UINT64&() const**</span></span>
</dt> <dd>

<span data-ttu-id="5ca29-117">Conversion implicite en une \_ structure UINT64 de la plage de sous-ressources D3D12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5ca29-117">Implicit conversion to a D3D12\_SUBRESOURCE\_RANGE\_UINT64 structure.</span></span> <span data-ttu-id="5ca29-118">Étant donné que \_ \_ la plage \_ de sous-ressources D3D12 UInt64 est le type sous-jacent de la plage de sous- \_ ressources CD3DX12 \_ \_ UInt64, l’objet est simplement retourné en tant que référence de stencil de profondeur D3D12 const \_ \_ \_ à lui-même.</span><span class="sxs-lookup"><span data-stu-id="5ca29-118">Because D3D12\_SUBRESOURCE\_RANGE\_UINT64 is the underlying type of CD3DX12\_SUBRESOURCE\_RANGE\_UINT64, the object is simply returned as a const D3D12\_DEPTH\_STENCIL\_DESC1 reference to itself.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ca29-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ca29-119">Requirements</span></span>



| <span data-ttu-id="5ca29-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5ca29-120">Requirement</span></span> | <span data-ttu-id="5ca29-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ca29-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5ca29-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="5ca29-122">Header</span></span><br/> | <dl> <span data-ttu-id="5ca29-123"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ca29-123"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ca29-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ca29-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ca29-125">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="5ca29-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="5ca29-126">**Plage de sous- \_ ressources D3D12 \_ \_ UINT64**</span><span class="sxs-lookup"><span data-stu-id="5ca29-126">**D3D12\_SUBRESOURCE\_RANGE\_UINT64**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64)
</dt> </dl>

 

 





