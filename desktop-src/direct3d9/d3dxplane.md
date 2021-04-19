---
description: Décrit un plan.
ms.assetid: ffca4650-9788-4559-8f6b-a4e5db29ce55
title: D3DXPLANE, structure (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPLANE
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 260f9555313aea3443f0728f2b50189228429803
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525852"
---
# <a name="d3dxplane-structure-d3dx9mathh"></a><span data-ttu-id="5d2a9-103">D3DXPLANE, structure (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="5d2a9-103">D3DXPLANE structure (D3dx9math.h)</span></span>

<span data-ttu-id="5d2a9-104">Décrit un plan.</span><span class="sxs-lookup"><span data-stu-id="5d2a9-104">Describes a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d2a9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d2a9-105">Syntax</span></span>


```C++
typedef struct D3DXPLANE {
  FLOAT a;
  FLOAT b;
  FLOAT c;
  FLOAT d;
} D3DXPLANE, *LPD3DXPLANE;
```



## <a name="members"></a><span data-ttu-id="5d2a9-106">Membres</span><span class="sxs-lookup"><span data-stu-id="5d2a9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5d2a9-107">**un**</span><span class="sxs-lookup"><span data-stu-id="5d2a9-107">**a**</span></span>
</dt> <dd>

<span data-ttu-id="5d2a9-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5d2a9-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5d2a9-109">Coefficient du plan de découpage dans l’équation du plan général.</span><span class="sxs-lookup"><span data-stu-id="5d2a9-109">The a coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="5d2a9-110">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="5d2a9-110">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5d2a9-111">**b**</span><span class="sxs-lookup"><span data-stu-id="5d2a9-111">**b**</span></span>
</dt> <dd>

<span data-ttu-id="5d2a9-112">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5d2a9-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5d2a9-113">Coefficient b du plan de découpage dans l’équation du plan général.</span><span class="sxs-lookup"><span data-stu-id="5d2a9-113">The b coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="5d2a9-114">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="5d2a9-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5d2a9-115">**c**</span><span class="sxs-lookup"><span data-stu-id="5d2a9-115">**c**</span></span>
</dt> <dd>

<span data-ttu-id="5d2a9-116">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5d2a9-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5d2a9-117">Coefficient c du plan de découpage dans l’équation du plan général.</span><span class="sxs-lookup"><span data-stu-id="5d2a9-117">The c coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="5d2a9-118">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="5d2a9-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5d2a9-119">**d**</span><span class="sxs-lookup"><span data-stu-id="5d2a9-119">**d**</span></span>
</dt> <dd>

<span data-ttu-id="5d2a9-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5d2a9-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5d2a9-121">Coefficient d du plan de découpage dans l’équation du plan général.</span><span class="sxs-lookup"><span data-stu-id="5d2a9-121">The d coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="5d2a9-122">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="5d2a9-122">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d2a9-123">Notes</span><span class="sxs-lookup"><span data-stu-id="5d2a9-123">Remarks</span></span>

<span data-ttu-id="5d2a9-124">Les membres de la structure **D3DXPLANE** prennent la forme de l’équation plan générale.</span><span class="sxs-lookup"><span data-stu-id="5d2a9-124">The members of the **D3DXPLANE** structure take the form of the general plane equation.</span></span> <span data-ttu-id="5d2a9-125">Elles s’intègrent à l’équation plan générale, **de** sorte que x + **b** y + **c** z + **d** w = 0.</span><span class="sxs-lookup"><span data-stu-id="5d2a9-125">They fit into the general plane equation so that **a** x + **b** y + **c** z + **d** w = 0.</span></span>

<span data-ttu-id="5d2a9-126">Les programmeurs C++ peuvent tirer parti de la surcharge d’opérateur et de la conversion de type avec les [**Extensions D3DXPLANE**](d3dxplane-extensions.md) qui implémentent des constructeurs surchargés et des opérateurs d’assignation, unaires et binaires (y compris l’égalité).</span><span class="sxs-lookup"><span data-stu-id="5d2a9-126">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXPLANE Extensions**](d3dxplane-extensions.md) which implement overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d2a9-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d2a9-127">Requirements</span></span>



| <span data-ttu-id="5d2a9-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d2a9-128">Requirement</span></span> | <span data-ttu-id="5d2a9-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d2a9-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d2a9-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="5d2a9-130">Header</span></span><br/> | <dl> <span data-ttu-id="5d2a9-131"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d2a9-131"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d2a9-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d2a9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d2a9-133">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="5d2a9-133">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
