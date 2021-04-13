---
description: Met à l’échelle un vecteur 2D.
ms.assetid: 1887bc48-3766-42d7-840b-1e29d78db4ce
title: D3DXVec2Scale, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Scale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 941e85763b15724e3c810c0416b5b142c9d95913
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322817"
---
# <a name="d3dxvec2scale-function"></a><span data-ttu-id="567ea-103">D3DXVec2Scale fonction)</span><span class="sxs-lookup"><span data-stu-id="567ea-103">D3DXVec2Scale function</span></span>

<span data-ttu-id="567ea-104">Met à l’échelle un vecteur 2D.</span><span class="sxs-lookup"><span data-stu-id="567ea-104">Scales a 2D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="567ea-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="567ea-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Scale(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="567ea-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="567ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="567ea-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="567ea-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="567ea-108">Type : **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="567ea-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="567ea-109">Pointeur vers la structure [**D3DXVECTOR2**](d3dxvector2.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="567ea-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="567ea-110">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="567ea-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="567ea-111">Type : **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="567ea-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="567ea-112">Pointeur vers la structure [**D3DXVECTOR2**](d3dxvector2.md) source.</span><span class="sxs-lookup"><span data-stu-id="567ea-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="567ea-113"> \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="567ea-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="567ea-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="567ea-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="567ea-115">Valeur de mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="567ea-115">Scaling value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="567ea-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="567ea-116">Return value</span></span>

<span data-ttu-id="567ea-117">Type : **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="567ea-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="567ea-118">Pointeur vers une structure [**D3DXVECTOR2**](d3dxvector2.md) qui est le vecteur mis à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="567ea-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the scaled vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="567ea-119">Notes</span><span class="sxs-lookup"><span data-stu-id="567ea-119">Remarks</span></span>

<span data-ttu-id="567ea-120">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="567ea-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="567ea-121">De cette façon, la fonction **D3DXVec2Scale** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="567ea-121">In this way, the **D3DXVec2Scale** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="567ea-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="567ea-122">Requirements</span></span>



| <span data-ttu-id="567ea-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="567ea-123">Requirement</span></span> | <span data-ttu-id="567ea-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="567ea-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="567ea-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="567ea-125">Header</span></span><br/>  | <dl> <span data-ttu-id="567ea-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="567ea-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="567ea-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="567ea-127">Library</span></span><br/> | <dl> <span data-ttu-id="567ea-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="567ea-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="567ea-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="567ea-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="567ea-130">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="567ea-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="567ea-131">**D3DXVec2Add**</span><span class="sxs-lookup"><span data-stu-id="567ea-131">**D3DXVec2Add**</span></span>](d3dxvec2add.md)
</dt> <dt>

[<span data-ttu-id="567ea-132">**D3DXVec2Subtract**</span><span class="sxs-lookup"><span data-stu-id="567ea-132">**D3DXVec2Subtract**</span></span>](d3dxvec2subtract.md)
</dt> </dl>

 

 
