---
title: Structure CD3DX12_RANGE_UINT64 (D3dx12. h)
description: Une structure d’assistance pour faciliter l’initialisation d’une structure de \_ plage D3D12 \_ UINT64.
ms.assetid: 789A2C46-B7D4-462E-9C10-69FD63D27491
keywords:
- Structure CD3DX12_RANGE_UINT64
topic_type:
- apiref
api_name:
- CD3DX12_RANGE_UINT64
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89c408197afb1254cae922c402939f6f169708d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539923"
---
# <a name="cd3dx12_range_uint64-structure"></a><span data-ttu-id="e70d1-104">CD3DX12 \_ plage \_ UINT64 (structure)</span><span class="sxs-lookup"><span data-stu-id="e70d1-104">CD3DX12\_RANGE\_UINT64 structure</span></span>

<span data-ttu-id="e70d1-105">Une structure d’assistance pour faciliter l’initialisation d’une structure [**de \_ plage D3D12 \_ UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) .</span><span class="sxs-lookup"><span data-stu-id="e70d1-105">A helper structure to enable easy initialization of a [**D3D12\_RANGE\_UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="e70d1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e70d1-106">Syntax</span></span>


```C++
struct CD3DX12_RANGE_UINT64  : public D3D12_RANGE_UINT64{
  CD3DX12_RANGE_UINT64 CD3DX12_RANGE_UINT64();
  CD3DX12_RANGE_UINT64 explicit CD3DX12_RANGE_UINT64(const D3D12_RANGE_UINT64 &o);
  CD3DX12_RANGE_UINT64 CD3DX12_RANGE_UINT64(UINT64 begin, UINT64 end);
                       operator const D3D12_RANGE_UINT64&() const;
};
```



## <a name="members"></a><span data-ttu-id="e70d1-107">Membres</span><span class="sxs-lookup"><span data-stu-id="e70d1-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e70d1-108">**\_Plage CD3DX12 \_ UINT64 ()**</span><span class="sxs-lookup"><span data-stu-id="e70d1-108">**CD3DX12\_RANGE\_UINT64()**</span></span>
</dt> <dd>

<span data-ttu-id="e70d1-109">Crée une nouvelle instance non initialisée d’une \_ plage CD3DX12 \_ UINT64.</span><span class="sxs-lookup"><span data-stu-id="e70d1-109">Creates a new, uninitialized, instance of a CD3DX12\_RANGE\_UINT64.</span></span>

</dd> <dt>

<span data-ttu-id="e70d1-110">**plage CD3DX12 \_ explicite \_ UInt64 (const D3D12 \_ plage \_ UInt64 &o)**</span><span class="sxs-lookup"><span data-stu-id="e70d1-110">**explicit CD3DX12\_RANGE\_UINT64(const D3D12\_RANGE\_UINT64 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="e70d1-111">Crée une nouvelle instance d’une \_ plage CD3DX12 \_ UInt64, initialisée avec des valeurs copiées à partir d’une structure de [**\_ plage D3D12 \_ UInt64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) .</span><span class="sxs-lookup"><span data-stu-id="e70d1-111">Creates a new instance of a CD3DX12\_RANGE\_UINT64, initialized with values copied from a [**D3D12\_RANGE\_UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e70d1-112">**\_Plage CD3DX12 \_ UINT64 (UInt64 Begin, UInt64 end)**</span><span class="sxs-lookup"><span data-stu-id="e70d1-112">**CD3DX12\_RANGE\_UINT64(UINT64 begin, UINT64 end)**</span></span>
</dt> <dd>

<span data-ttu-id="e70d1-113">Crée une nouvelle instance d’un \_ stencil de profondeur CD3DX12 \_ \_ DESC1, initialisée avec les valeurs passées dans la liste de paramètres.</span><span class="sxs-lookup"><span data-stu-id="e70d1-113">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with the values passed in the parameter list.</span></span>

</dd> <dt>

<span data-ttu-id="e70d1-114">**@ const D3D12 \_ plage \_ UINT64& () const**</span><span class="sxs-lookup"><span data-stu-id="e70d1-114">**operator const D3D12\_RANGE\_UINT64&() const**</span></span>
</dt> <dd>

<span data-ttu-id="e70d1-115">Conversion implicite en une \_ structure de plage D3D12 \_ UINT64.</span><span class="sxs-lookup"><span data-stu-id="e70d1-115">Implicit conversion to a D3D12\_RANGE\_UINT64 structure.</span></span> <span data-ttu-id="e70d1-116">Étant donné que D3D12 \_ Range \_ UInt64 est le type sous-jacent de la \_ plage CD3DX12 \_ UInt64, l’objet est simplement retourné en tant que référence de plage D3D12 const \_ \_ à lui-même.</span><span class="sxs-lookup"><span data-stu-id="e70d1-116">Because D3D12\_RANGE\_UINT64 is the underlying type of CD3DX12\_RANGE\_UINT64, the object is simply returned as a const D3D12\_RANGE\_UINT64 reference to itself.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e70d1-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e70d1-117">Requirements</span></span>



| <span data-ttu-id="e70d1-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e70d1-118">Requirement</span></span> | <span data-ttu-id="e70d1-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="e70d1-119">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e70d1-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="e70d1-120">Header</span></span><br/> | <dl> <span data-ttu-id="e70d1-121"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="e70d1-121"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e70d1-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e70d1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e70d1-123">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="e70d1-123">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="e70d1-124">**\_Plage D3D12 \_ UINT64**</span><span class="sxs-lookup"><span data-stu-id="e70d1-124">**D3D12\_RANGE\_UINT64**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64)
</dt> </dl>

 

 





