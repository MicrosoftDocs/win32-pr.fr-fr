---
title: Structure CD3DX12_BOX (D3dx12. h)
description: Structure d’assistance pour faciliter l’initialisation d’une \_ structure de zone D3D12.
ms.assetid: 7E1A352C-D664-4538-BA78-91493980559D
keywords:
- Structure CD3DX12_BOX
topic_type:
- apiref
api_name:
- CD3DX12_BOX
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.topic: reference
ms.localizationpriority: low
ms.date: 05/31/2018
ms.openlocfilehash: c689c9bfe611651248280f7536bd91a9f4d003d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106537243"
---
# <a name="cd3dx12_box-structure"></a><span data-ttu-id="809d5-104">\_Structure de la boîte de CD3DX12</span><span class="sxs-lookup"><span data-stu-id="809d5-104">CD3DX12\_BOX structure</span></span>

<span data-ttu-id="809d5-105">Structure d’assistance pour faciliter l’initialisation d’une structure de [**\_ zone D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) .</span><span class="sxs-lookup"><span data-stu-id="809d5-105">A helper structure to enable easy initialization of a [**D3D12\_BOX**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="809d5-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="809d5-106">Syntax</span></span>


```C++
struct CD3DX12_BOX  : public D3D12_BOX{
   CD3DX12_BOX();
   explicit CD3DX12_BOX(const D3D12_BOX& o);
   explicit CD3DX12_BOX(LONG Left, LONG Right);
   explicit CD3DX12_BOX(LONG Left, LONG Top, LONG Right, LONG Bottom);
   explicit CD3DX12_BOX(LONG Left, LONG Top, LONG Front, LONG Right, LONG Bottom, LONG Back);
   ~CD3DX12_BOX();
   operator const D3D12_BOX&() const;
};
```



## <a name="members"></a><span data-ttu-id="809d5-107">Membres</span><span class="sxs-lookup"><span data-stu-id="809d5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="809d5-108">**CD3DX12 \_ Box ()**</span><span class="sxs-lookup"><span data-stu-id="809d5-108">**CD3DX12\_BOX()**</span></span>
</dt> <dd>

<span data-ttu-id="809d5-109">Crée une nouvelle instance non initialisée d’une \_ zone CD3DX12.</span><span class="sxs-lookup"><span data-stu-id="809d5-109">Creates a new, uninitialized, instance of a CD3DX12\_BOX.</span></span>

</dd> <dt>

<span data-ttu-id="809d5-110">**zone CD3DX12 explicite \_ (const D3D12 \_ Box& o)**</span><span class="sxs-lookup"><span data-stu-id="809d5-110">**explicit CD3DX12\_BOX(const D3D12\_BOX& o)**</span></span>
</dt> <dd>

<span data-ttu-id="809d5-111">Crée une nouvelle instance d’une \_ zone CD3DX12, initialisée avec le contenu d’une autre structure de [**\_ zone D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) .</span><span class="sxs-lookup"><span data-stu-id="809d5-111">Creates a new instance of a CD3DX12\_BOX, initialized with the contents of another [**D3D12\_BOX**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) structure.</span></span>

</dd> <dt>

<span data-ttu-id="809d5-112">**zone CD3DX12 explicite \_ (longue gauche, long droit)**</span><span class="sxs-lookup"><span data-stu-id="809d5-112">**explicit CD3DX12\_BOX(LONG Left, LONG Right)**</span></span>
</dt> <dd>

<span data-ttu-id="809d5-113">Crée une nouvelle instance d’une \_ zone CD3DX12, en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="809d5-113">Creates a new instance of a CD3DX12\_BOX, initializing the following parameters:</span></span>

<span data-ttu-id="809d5-114">LONGUE gauche</span><span class="sxs-lookup"><span data-stu-id="809d5-114">LONG Left</span></span>

<span data-ttu-id="809d5-115">LONG droit</span><span class="sxs-lookup"><span data-stu-id="809d5-115">LONG Right</span></span>

</dd> <dt>

<span data-ttu-id="809d5-116">**zone CD3DX12 explicite \_ (longue gauche, long haut, long droit, long Bottom)**</span><span class="sxs-lookup"><span data-stu-id="809d5-116">**explicit CD3DX12\_BOX(LONG Left, LONG Top, LONG Right, LONG Bottom)**</span></span>
</dt> <dd>

<span data-ttu-id="809d5-117">Crée une nouvelle instance d’une \_ zone CD3DX12, en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="809d5-117">Creates a new instance of a CD3DX12\_BOX, initializing the following parameters:</span></span>

<span data-ttu-id="809d5-118">LONGUE gauche</span><span class="sxs-lookup"><span data-stu-id="809d5-118">LONG Left</span></span>

<span data-ttu-id="809d5-119">LONG haut</span><span class="sxs-lookup"><span data-stu-id="809d5-119">LONG Top</span></span>

<span data-ttu-id="809d5-120">LONG droit</span><span class="sxs-lookup"><span data-stu-id="809d5-120">LONG Right</span></span>

<span data-ttu-id="809d5-121">LONG bas</span><span class="sxs-lookup"><span data-stu-id="809d5-121">LONG Bottom</span></span>

</dd> <dt>

<span data-ttu-id="809d5-122">**zone CD3DX12 explicite \_ (longue gauche, longue, longue, longue, longue, longue, longue, longue, long)**</span><span class="sxs-lookup"><span data-stu-id="809d5-122">**explicit CD3DX12\_BOX(LONG Left, LONG Top, LONG Front, LONG Right, LONG Bottom, LONG Back)**</span></span>
</dt> <dd>

<span data-ttu-id="809d5-123">Crée une nouvelle instance d’une \_ zone CD3DX12, en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="809d5-123">Creates a new instance of a CD3DX12\_BOX, initializing the following parameters:</span></span>

<span data-ttu-id="809d5-124">LONGUE gauche</span><span class="sxs-lookup"><span data-stu-id="809d5-124">LONG Left</span></span>

<span data-ttu-id="809d5-125">LONG haut</span><span class="sxs-lookup"><span data-stu-id="809d5-125">LONG Top</span></span>

<span data-ttu-id="809d5-126">LONG avant</span><span class="sxs-lookup"><span data-stu-id="809d5-126">LONG Front</span></span>

<span data-ttu-id="809d5-127">LONG droit</span><span class="sxs-lookup"><span data-stu-id="809d5-127">LONG Right</span></span>

<span data-ttu-id="809d5-128">LONG bas</span><span class="sxs-lookup"><span data-stu-id="809d5-128">LONG Bottom</span></span>

<span data-ttu-id="809d5-129">Retour à LONG terme</span><span class="sxs-lookup"><span data-stu-id="809d5-129">LONG Back</span></span>

</dd> <dt>

<span data-ttu-id="809d5-130">**~ CD3DX12 \_ Box ()**</span><span class="sxs-lookup"><span data-stu-id="809d5-130">**~CD3DX12\_BOX()**</span></span>
</dt> <dd>

<span data-ttu-id="809d5-131">Détruit une instance d’une zone CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="809d5-131">Destroys an instance of a CD3DX12\_BOX.</span></span>

</dd> <dt>

<span data-ttu-id="809d5-132">**\_const D3D12, zone& () const**</span><span class="sxs-lookup"><span data-stu-id="809d5-132">**operator const D3D12\_BOX&() const**</span></span>
</dt> <dd>

<span data-ttu-id="809d5-133">Définit le & opérateur de passage par référence pour le type de structure parent.</span><span class="sxs-lookup"><span data-stu-id="809d5-133">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="809d5-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="809d5-134">Requirements</span></span>



| <span data-ttu-id="809d5-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="809d5-135">Requirement</span></span> | <span data-ttu-id="809d5-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="809d5-136">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="809d5-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="809d5-137">Header</span></span><br/> | <dl> <span data-ttu-id="809d5-138"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="809d5-138"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="809d5-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="809d5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="809d5-140">**\_Zone D3D12**</span><span class="sxs-lookup"><span data-stu-id="809d5-140">**D3D12\_BOX**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box)
</dt> <dt>

[<span data-ttu-id="809d5-141">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="809d5-141">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





