---
description: D3DXPLANE structure (D3DX10Math. h)-décrit un plan.
ms.assetid: c6da7343-a4f3-4cac-855b-14bd70c0d3c2
title: D3DXPLANE, structure (D3DX10Math. h)
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
- D3DX10Math.h
ms.openlocfilehash: 440246fb47a851f9f5339c72a484a2cb59e8f662
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103327"
---
# <a name="d3dxplane-structure-d3dx10mathh"></a><span data-ttu-id="922a4-103">D3DXPLANE, structure (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="922a4-103">D3DXPLANE structure (D3DX10Math.h)</span></span>

<span data-ttu-id="922a4-104">Décrit un plan.</span><span class="sxs-lookup"><span data-stu-id="922a4-104">Describes a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="922a4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="922a4-105">Syntax</span></span>


```C++
typedef struct D3DXPLANE {
  FLOAT a;
  FLOAT b;
  FLOAT c;
  FLOAT d;
} D3DXPLANE, *LPD3DXPLANE;
```



## <a name="members"></a><span data-ttu-id="922a4-106">Membres</span><span class="sxs-lookup"><span data-stu-id="922a4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="922a4-107">**un**</span><span class="sxs-lookup"><span data-stu-id="922a4-107">**a**</span></span>
</dt> <dd>

<span data-ttu-id="922a4-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="922a4-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="922a4-109">Coefficient du plan de découpage dans l’équation du plan général.</span><span class="sxs-lookup"><span data-stu-id="922a4-109">The a coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="922a4-110">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="922a4-110">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="922a4-111">**b**</span><span class="sxs-lookup"><span data-stu-id="922a4-111">**b**</span></span>
</dt> <dd>

<span data-ttu-id="922a4-112">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="922a4-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="922a4-113">Coefficient b du plan de découpage dans l’équation du plan général.</span><span class="sxs-lookup"><span data-stu-id="922a4-113">The b coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="922a4-114">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="922a4-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="922a4-115">**c**</span><span class="sxs-lookup"><span data-stu-id="922a4-115">**c**</span></span>
</dt> <dd>

<span data-ttu-id="922a4-116">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="922a4-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="922a4-117">Coefficient c du plan de découpage dans l’équation du plan général.</span><span class="sxs-lookup"><span data-stu-id="922a4-117">The c coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="922a4-118">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="922a4-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="922a4-119">**d**</span><span class="sxs-lookup"><span data-stu-id="922a4-119">**d**</span></span>
</dt> <dd>

<span data-ttu-id="922a4-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="922a4-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="922a4-121">Coefficient d du plan de découpage dans l’équation du plan général.</span><span class="sxs-lookup"><span data-stu-id="922a4-121">The d coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="922a4-122">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="922a4-122">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="922a4-123">Notes </span><span class="sxs-lookup"><span data-stu-id="922a4-123">Remarks</span></span>

<span data-ttu-id="922a4-124">Les membres de la structure **D3DXPLANE** prennent la forme de l’équation plan générale.</span><span class="sxs-lookup"><span data-stu-id="922a4-124">The members of the **D3DXPLANE** structure take the form of the general plane equation.</span></span> <span data-ttu-id="922a4-125">Elles s’inscrivent dans l’équation plan générale, de sorte que ax + by + CZ + DW = 0.</span><span class="sxs-lookup"><span data-stu-id="922a4-125">They fit into the general plane equation so that ax + by + cz + dw = 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="922a4-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="922a4-126">Requirements</span></span>



| <span data-ttu-id="922a4-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="922a4-127">Requirement</span></span> | <span data-ttu-id="922a4-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="922a4-128">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="922a4-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="922a4-129">Header</span></span><br/> | <dl> <span data-ttu-id="922a4-130"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="922a4-130"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="922a4-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="922a4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="922a4-132">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="922a4-132">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
