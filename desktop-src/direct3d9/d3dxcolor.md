---
description: D3DXCOLOR structure (D3dx9math. h)-décrit les valeurs de couleur.
ms.assetid: 53d3176a-f727-498e-8bea-0e30e0a1c66e
title: D3DXCOLOR, structure (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCOLOR
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 58b02abc49b695169674a2579b73dc2359801a73
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115927"
---
# <a name="d3dxcolor-structure-d3dx9mathh"></a><span data-ttu-id="b32ed-103">D3DXCOLOR, structure (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="b32ed-103">D3DXCOLOR structure (D3dx9math.h)</span></span>

<span data-ttu-id="b32ed-104">Décrit les valeurs de couleur.</span><span class="sxs-lookup"><span data-stu-id="b32ed-104">Describes color values.</span></span>

## <a name="syntax"></a><span data-ttu-id="b32ed-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b32ed-105">Syntax</span></span>


```C++
typedef struct D3DXCOLOR {
  FLOAT r;
  FLOAT g;
  FLOAT b;
  FLOAT a;
} D3DXCOLOR, *LPD3DXCOLOR;
```



## <a name="members"></a><span data-ttu-id="b32ed-106">Membres</span><span class="sxs-lookup"><span data-stu-id="b32ed-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b32ed-107">**r**</span><span class="sxs-lookup"><span data-stu-id="b32ed-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="b32ed-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b32ed-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b32ed-109">Composant rouge de la couleur.</span><span class="sxs-lookup"><span data-stu-id="b32ed-109">Red component of the color.</span></span>

</dd> <dt>

<span data-ttu-id="b32ed-110">**activée**</span><span class="sxs-lookup"><span data-stu-id="b32ed-110">**g**</span></span>
</dt> <dd>

<span data-ttu-id="b32ed-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b32ed-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b32ed-112">Composant vert de la couleur.</span><span class="sxs-lookup"><span data-stu-id="b32ed-112">Green component of the color.</span></span>

</dd> <dt>

<span data-ttu-id="b32ed-113">**b**</span><span class="sxs-lookup"><span data-stu-id="b32ed-113">**b**</span></span>
</dt> <dd>

<span data-ttu-id="b32ed-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b32ed-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b32ed-115">Composant bleu de la couleur.</span><span class="sxs-lookup"><span data-stu-id="b32ed-115">Blue component of the color.</span></span>

</dd> <dt>

<span data-ttu-id="b32ed-116">**un**</span><span class="sxs-lookup"><span data-stu-id="b32ed-116">**a**</span></span>
</dt> <dd>

<span data-ttu-id="b32ed-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b32ed-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b32ed-118">Composant alpha de la couleur.</span><span class="sxs-lookup"><span data-stu-id="b32ed-118">Alpha component of the color.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b32ed-119">Notes </span><span class="sxs-lookup"><span data-stu-id="b32ed-119">Remarks</span></span>

<span data-ttu-id="b32ed-120">Les programmeurs C++ peuvent tirer parti de la surcharge d’opérateur et de la conversion de type avec les [**Extensions D3DXCOLOR**](d3dxcolor-extensions.md), qui implémentent des constructeurs surchargés, ainsi que des opérateurs d’assignation, unaires et binaires (y compris l’égalité).</span><span class="sxs-lookup"><span data-stu-id="b32ed-120">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXCOLOR Extensions**](d3dxcolor-extensions.md), which implement overloaded constructors, as well as assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="b32ed-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b32ed-121">Requirements</span></span>



| <span data-ttu-id="b32ed-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b32ed-122">Requirement</span></span> | <span data-ttu-id="b32ed-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="b32ed-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b32ed-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="b32ed-124">Header</span></span><br/> | <dl> <span data-ttu-id="b32ed-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b32ed-125"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b32ed-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b32ed-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b32ed-127">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="b32ed-127">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
