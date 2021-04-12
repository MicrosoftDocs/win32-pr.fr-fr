---
description: Définit un volume.
ms.assetid: 415a96bc-1621-4691-b87a-98ca22f0bf07
title: D3DBOX, structure (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBOX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 882f6aadf0d49284b30132d4f08a9c583e5c9d73
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211711"
---
# <a name="d3dbox-structure"></a><span data-ttu-id="9df7e-103">D3DBOX, structure</span><span class="sxs-lookup"><span data-stu-id="9df7e-103">D3DBOX structure</span></span>

<span data-ttu-id="9df7e-104">Définit un volume.</span><span class="sxs-lookup"><span data-stu-id="9df7e-104">Defines a volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="9df7e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9df7e-105">Syntax</span></span>


```C++
typedef struct D3DBOX {
  UINT Left;
  UINT Top;
  UINT Right;
  UINT Bottom;
  UINT Front;
  UINT Back;
} D3DBOX, *LPD3DBOX;
```



## <a name="members"></a><span data-ttu-id="9df7e-106">Membres</span><span class="sxs-lookup"><span data-stu-id="9df7e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9df7e-107">**Left**</span><span class="sxs-lookup"><span data-stu-id="9df7e-107">**Left**</span></span>
</dt> <dd>

<span data-ttu-id="9df7e-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9df7e-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9df7e-109">Position du côté gauche de la zone sur l’axe x.</span><span class="sxs-lookup"><span data-stu-id="9df7e-109">Position of the left side of the box on the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="9df7e-110">**Top**</span><span class="sxs-lookup"><span data-stu-id="9df7e-110">**Top**</span></span>
</dt> <dd>

<span data-ttu-id="9df7e-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9df7e-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9df7e-112">Position du haut de la zone sur l’axe y.</span><span class="sxs-lookup"><span data-stu-id="9df7e-112">Position of the top of the box on the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="9df7e-113">**Right**</span><span class="sxs-lookup"><span data-stu-id="9df7e-113">**Right**</span></span>
</dt> <dd>

<span data-ttu-id="9df7e-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9df7e-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9df7e-115">Position du côté droit de la zone sur l’axe x.</span><span class="sxs-lookup"><span data-stu-id="9df7e-115">Position of the right side of the box on the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="9df7e-116">**Bas**</span><span class="sxs-lookup"><span data-stu-id="9df7e-116">**Bottom**</span></span>
</dt> <dd>

<span data-ttu-id="9df7e-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9df7e-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9df7e-118">Position du bas de la zone sur l’axe y.</span><span class="sxs-lookup"><span data-stu-id="9df7e-118">Position of the bottom of the box on the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="9df7e-119">**Front**</span><span class="sxs-lookup"><span data-stu-id="9df7e-119">**Front**</span></span>
</dt> <dd>

<span data-ttu-id="9df7e-120">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9df7e-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9df7e-121">Position du premier plan de la zone sur l’axe z.</span><span class="sxs-lookup"><span data-stu-id="9df7e-121">Position of the front of the box on the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="9df7e-122">**Précédent**</span><span class="sxs-lookup"><span data-stu-id="9df7e-122">**Back**</span></span>
</dt> <dd>

<span data-ttu-id="9df7e-123">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9df7e-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9df7e-124">Position du arrière de la boîte sur l’axe z.</span><span class="sxs-lookup"><span data-stu-id="9df7e-124">Position of the back of the box on the z-axis.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9df7e-125">Notes</span><span class="sxs-lookup"><span data-stu-id="9df7e-125">Remarks</span></span>

<span data-ttu-id="9df7e-126">**D3DBOX** comprend les bords gauche, supérieur et avant ; Toutefois, les bords droit, inférieur et arrière ne sont pas inclus.</span><span class="sxs-lookup"><span data-stu-id="9df7e-126">**D3DBOX** includes the left, top, and front edges; however, the right, bottom, and back edges are not included.</span></span> <span data-ttu-id="9df7e-127">Par exemple, une zone de 100 unités de largeur et commençant à 0 (y compris les points jusqu’à 99) sont exprimées avec la valeur 0 pour le membre de gauche et la valeur 100 pour le membre de droite.</span><span class="sxs-lookup"><span data-stu-id="9df7e-127">For example, a box that is 100 units wide and begins at 0 (thus, including the points up to and including 99) would be expressed with a value of 0 for the Left member and a value of 100 for the Right member.</span></span> <span data-ttu-id="9df7e-128">Notez qu’une valeur de 99 n’est pas utilisée pour le membre approprié.</span><span class="sxs-lookup"><span data-stu-id="9df7e-128">Note that a value of 99 is not used for the Right member.</span></span>

<span data-ttu-id="9df7e-129">Les restrictions sur l’ordre des côtés observées pour les **D3DBOX** sont de gauche à droite, de haut en bas et de premier plan à précédent.</span><span class="sxs-lookup"><span data-stu-id="9df7e-129">The restrictions on side ordering observed for **D3DBOX** are left to right, top to bottom, and front to back.</span></span>

## <a name="requirements"></a><span data-ttu-id="9df7e-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9df7e-130">Requirements</span></span>



| <span data-ttu-id="9df7e-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9df7e-131">Requirement</span></span> | <span data-ttu-id="9df7e-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="9df7e-132">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9df7e-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="9df7e-133">Header</span></span><br/> | <dl> <span data-ttu-id="9df7e-134"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="9df7e-134"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9df7e-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9df7e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9df7e-136">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="9df7e-136">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
