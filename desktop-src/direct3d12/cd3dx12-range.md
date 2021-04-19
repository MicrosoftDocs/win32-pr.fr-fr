---
title: Structure CD3DX12_RANGE (D3dx12. h)
description: Structure d’assistance pour faciliter l’initialisation d’une \_ structure de plage D3D12.
ms.assetid: 5D5192BF-D14C-487B-A214-F8428E82AF0E
keywords:
- Structure CD3DX12_RANGE
topic_type:
- apiref
api_name:
- CD3DX12_RANGE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b6b92cd24a981d48252f5ad457f7ac0320e2d7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106528575"
---
# <a name="cd3dx12_range-structure"></a><span data-ttu-id="bf1be-104">Structure de la \_ plage CD3DX12</span><span class="sxs-lookup"><span data-stu-id="bf1be-104">CD3DX12\_RANGE structure</span></span>

<span data-ttu-id="bf1be-105">Structure d’assistance pour faciliter l’initialisation d’une structure de [**\_ plage D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) .</span><span class="sxs-lookup"><span data-stu-id="bf1be-105">A helper structure to enable easy initialization of a [**D3D12\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf1be-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bf1be-106">Syntax</span></span>


```C++
struct CD3DX12_RANGE  : public D3D12_RANGE{
   CD3DX12_RANGE();
   explicit CD3DX12_RANGE(const D3D12_RANGE &o);
   CD3DX12_RANGE(SIZE_T begin, SIZE_T end);
   operator const D3D12_RANGE&() const;
};
```



## <a name="members"></a><span data-ttu-id="bf1be-107">Membres</span><span class="sxs-lookup"><span data-stu-id="bf1be-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="bf1be-108">**\_Plage CD3DX12 ()**</span><span class="sxs-lookup"><span data-stu-id="bf1be-108">**CD3DX12\_RANGE()**</span></span>
</dt> <dd>

<span data-ttu-id="bf1be-109">Crée une nouvelle instance non initialisée d’une \_ plage CD3DX12.</span><span class="sxs-lookup"><span data-stu-id="bf1be-109">Creates a new, uninitialized, instance of a CD3DX12\_RANGE.</span></span>

</dd> <dt>

<span data-ttu-id="bf1be-110">**plage CD3DX12 explicite \_ (const D3D12 \_ Range &o)**</span><span class="sxs-lookup"><span data-stu-id="bf1be-110">**explicit CD3DX12\_RANGE(const D3D12\_RANGE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="bf1be-111">Crée une nouvelle instance d’une \_ plage CD3DX12, initialisée avec le contenu d’une autre structure de [**\_ plage D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) .</span><span class="sxs-lookup"><span data-stu-id="bf1be-111">Creates a new instance of a CD3DX12\_RANGE, initialized with the contents of another [**D3D12\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) structure.</span></span>

</dd> <dt>

<span data-ttu-id="bf1be-112">**\_Plage CD3DX12 (taille \_ t début, taille \_ t fin)**</span><span class="sxs-lookup"><span data-stu-id="bf1be-112">**CD3DX12\_RANGE(SIZE\_T begin, SIZE\_T end)**</span></span>
</dt> <dd>

<span data-ttu-id="bf1be-113">Crée une nouvelle instance d’une \_ plage CD3DX12, en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="bf1be-113">Creates a new instance of a CD3DX12\_RANGE, initializing the following parameters:</span></span>

<span data-ttu-id="bf1be-114">TAILLE \_ T début</span><span class="sxs-lookup"><span data-stu-id="bf1be-114">SIZE\_T begin</span></span>

<span data-ttu-id="bf1be-115">Fin de la taille \_ T</span><span class="sxs-lookup"><span data-stu-id="bf1be-115">SIZE\_T end</span></span>

</dd> <dt>

<span data-ttu-id="bf1be-116">**\_const, opérateur D3D12& () const**</span><span class="sxs-lookup"><span data-stu-id="bf1be-116">**operator const D3D12\_RANGE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="bf1be-117">Définit le & opérateur de passage par référence pour le type de structure parent.</span><span class="sxs-lookup"><span data-stu-id="bf1be-117">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bf1be-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf1be-118">Requirements</span></span>



| <span data-ttu-id="bf1be-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf1be-119">Requirement</span></span> | <span data-ttu-id="bf1be-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf1be-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bf1be-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="bf1be-121">Header</span></span><br/> | <dl> <span data-ttu-id="bf1be-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf1be-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf1be-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf1be-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf1be-124">**\_Plage D3D12**</span><span class="sxs-lookup"><span data-stu-id="bf1be-124">**D3D12\_RANGE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)
</dt> <dt>

[<span data-ttu-id="bf1be-125">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="bf1be-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





