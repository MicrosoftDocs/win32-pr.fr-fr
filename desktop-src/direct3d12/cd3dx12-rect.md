---
title: Structure CD3DX12_RECT (D3dx12. h)
description: Une structure d’assistance pour permettre l’initialisation facile d’une \_ structure D3D12 Rect.
ms.assetid: FBF01294-1448-4D9A-BA6B-27D5D59C2958
keywords:
- Structure CD3DX12_RECT
topic_type:
- apiref
api_name:
- CD3DX12_RECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e6d8c133f14b531433ceb2239377ea85ba212af
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535163"
---
# <a name="cd3dx12_rect-structure"></a><span data-ttu-id="b6edf-104">CD3DX12 \_ Rect, structure</span><span class="sxs-lookup"><span data-stu-id="b6edf-104">CD3DX12\_RECT structure</span></span>

<span data-ttu-id="b6edf-105">Une structure d’assistance pour permettre l’initialisation facile d’une structure [**D3D12 \_ Rect**](d3d12-rect.md) .</span><span class="sxs-lookup"><span data-stu-id="b6edf-105">A helper structure to enable easy initialization of a [**D3D12\_RECT**](d3d12-rect.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6edf-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6edf-106">Syntax</span></span>


```C++
struct CD3DX12_RECT  : public D3D12_RECT{
   CD3DX12_RECT();
   explicit CD3DX12_RECT(const D3D12_RECT& o);
   explicit CD3DX12_RECT(LONG Left, LONG Top, LONG Right, LONG Bottom);
   ~CD3DX12_RECT();
   operator const D3D12_RECT&() const;
};
```



## <a name="members"></a><span data-ttu-id="b6edf-107">Membres</span><span class="sxs-lookup"><span data-stu-id="b6edf-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b6edf-108">**CD3DX12 \_ Rect ()**</span><span class="sxs-lookup"><span data-stu-id="b6edf-108">**CD3DX12\_RECT()**</span></span>
</dt> <dd>

<span data-ttu-id="b6edf-109">Crée une nouvelle instance non initialisée d’un CD3DX12 \_ Rect.</span><span class="sxs-lookup"><span data-stu-id="b6edf-109">Creates a new, uninitialized, instance of a CD3DX12\_RECT.</span></span>

</dd> <dt>

<span data-ttu-id="b6edf-110">**CD3DX12 \_ rectangulaire (const D3D12 \_ Rect& o) explicite**</span><span class="sxs-lookup"><span data-stu-id="b6edf-110">**explicit CD3DX12\_RECT(const D3D12\_RECT& o)**</span></span>
</dt> <dd>

<span data-ttu-id="b6edf-111">Crée une nouvelle instance d’un CD3DX12 \_ Rect, initialisée avec le contenu d’une autre structure [**D3D12 \_ Rect**](d3d12-rect.md) .</span><span class="sxs-lookup"><span data-stu-id="b6edf-111">Creates a new instance of a CD3DX12\_RECT, initialized with the contents of another [**D3D12\_RECT**](d3d12-rect.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b6edf-112">**CD3DX12 explicite \_ Rect (long gauche, long haut, long Right, long Bottom)**</span><span class="sxs-lookup"><span data-stu-id="b6edf-112">**explicit CD3DX12\_RECT(LONG Left, LONG Top, LONG Right, LONG Bottom)**</span></span>
</dt> <dd>

<span data-ttu-id="b6edf-113">Crée une nouvelle instance d’un CD3DX12 \_ Rect, en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="b6edf-113">Creates a new instance of a CD3DX12\_RECT, initializing the following parameters:</span></span>

<span data-ttu-id="b6edf-114">LONGUE gauche</span><span class="sxs-lookup"><span data-stu-id="b6edf-114">LONG Left</span></span>

<span data-ttu-id="b6edf-115">LONG haut</span><span class="sxs-lookup"><span data-stu-id="b6edf-115">LONG Top</span></span>

<span data-ttu-id="b6edf-116">LONG droit</span><span class="sxs-lookup"><span data-stu-id="b6edf-116">LONG Right</span></span>

<span data-ttu-id="b6edf-117">LONG bas</span><span class="sxs-lookup"><span data-stu-id="b6edf-117">LONG Bottom</span></span>

</dd> <dt>

<span data-ttu-id="b6edf-118">**~ CD3DX12 \_ Rect ()**</span><span class="sxs-lookup"><span data-stu-id="b6edf-118">**~CD3DX12\_RECT()**</span></span>
</dt> <dd>

<span data-ttu-id="b6edf-119">Détruit une instance d’un CD3DX12 \_ Rect.</span><span class="sxs-lookup"><span data-stu-id="b6edf-119">Destroys an instance of a CD3DX12\_RECT.</span></span>

</dd> <dt>

<span data-ttu-id="b6edf-120">**const, opérateur D3D12 \_ RECT& () const**</span><span class="sxs-lookup"><span data-stu-id="b6edf-120">**operator const D3D12\_RECT&() const**</span></span>
</dt> <dd>

<span data-ttu-id="b6edf-121">Définit le & opérateur de passage par référence pour le type de structure parent.</span><span class="sxs-lookup"><span data-stu-id="b6edf-121">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b6edf-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6edf-122">Requirements</span></span>



| <span data-ttu-id="b6edf-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6edf-123">Requirement</span></span> | <span data-ttu-id="b6edf-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6edf-124">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b6edf-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="b6edf-125">Header</span></span><br/> | <dl> <span data-ttu-id="b6edf-126"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6edf-126"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6edf-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6edf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6edf-128">**D3D12 \_ Rect**</span><span class="sxs-lookup"><span data-stu-id="b6edf-128">**D3D12\_RECT**</span></span>](d3d12-rect.md)
</dt> <dt>

[<span data-ttu-id="b6edf-129">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="b6edf-129">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





