---
description: Décrit un plan.
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
ms.openlocfilehash: 9949aec16e90a53e01e536255c20f442052bb98b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323238"
---
# <a name="d3dxplane-structure-d3dx10mathh"></a><span data-ttu-id="d5d27-103">D3DXPLANE, structure (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="d5d27-103">D3DXPLANE structure (D3DX10Math.h)</span></span>

<span data-ttu-id="d5d27-104">Décrit un plan.</span><span class="sxs-lookup"><span data-stu-id="d5d27-104">Describes a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5d27-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5d27-105">Syntax</span></span>


```C++
typedef struct D3DXPLANE {
  FLOAT a;
  FLOAT b;
  FLOAT c;
  FLOAT d;
} D3DXPLANE, *LPD3DXPLANE;
```



## <a name="members"></a><span data-ttu-id="d5d27-106">Membres</span><span class="sxs-lookup"><span data-stu-id="d5d27-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d5d27-107">**un**</span><span class="sxs-lookup"><span data-stu-id="d5d27-107">**a**</span></span>
</dt> <dd>

<span data-ttu-id="d5d27-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d5d27-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d5d27-109">Coefficient du plan de découpage dans l’équation du plan général.</span><span class="sxs-lookup"><span data-stu-id="d5d27-109">The a coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="d5d27-110">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="d5d27-110">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d5d27-111">**b**</span><span class="sxs-lookup"><span data-stu-id="d5d27-111">**b**</span></span>
</dt> <dd>

<span data-ttu-id="d5d27-112">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d5d27-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d5d27-113">Coefficient b du plan de découpage dans l’équation du plan général.</span><span class="sxs-lookup"><span data-stu-id="d5d27-113">The b coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="d5d27-114">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="d5d27-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d5d27-115">**c**</span><span class="sxs-lookup"><span data-stu-id="d5d27-115">**c**</span></span>
</dt> <dd>

<span data-ttu-id="d5d27-116">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d5d27-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d5d27-117">Coefficient c du plan de découpage dans l’équation du plan général.</span><span class="sxs-lookup"><span data-stu-id="d5d27-117">The c coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="d5d27-118">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="d5d27-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d5d27-119">**d**</span><span class="sxs-lookup"><span data-stu-id="d5d27-119">**d**</span></span>
</dt> <dd>

<span data-ttu-id="d5d27-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d5d27-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d5d27-121">Coefficient d du plan de découpage dans l’équation du plan général.</span><span class="sxs-lookup"><span data-stu-id="d5d27-121">The d coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="d5d27-122">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="d5d27-122">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d5d27-123">Notes</span><span class="sxs-lookup"><span data-stu-id="d5d27-123">Remarks</span></span>

<span data-ttu-id="d5d27-124">Les membres de la structure **D3DXPLANE** prennent la forme de l’équation plan générale.</span><span class="sxs-lookup"><span data-stu-id="d5d27-124">The members of the **D3DXPLANE** structure take the form of the general plane equation.</span></span> <span data-ttu-id="d5d27-125">Elles s’inscrivent dans l’équation plan générale, de sorte que ax + by + CZ + DW = 0.</span><span class="sxs-lookup"><span data-stu-id="d5d27-125">They fit into the general plane equation so that ax + by + cz + dw = 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5d27-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5d27-126">Requirements</span></span>



| <span data-ttu-id="d5d27-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5d27-127">Requirement</span></span> | <span data-ttu-id="d5d27-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5d27-128">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5d27-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="d5d27-129">Header</span></span><br/> | <dl> <span data-ttu-id="d5d27-130"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5d27-130"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5d27-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5d27-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5d27-132">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="d5d27-132">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
