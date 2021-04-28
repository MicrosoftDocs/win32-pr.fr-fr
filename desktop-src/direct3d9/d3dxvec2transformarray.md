---
description: D3DXVec2TransformArray, fonction (D3dx9math. h)-transforme un tableau (x, y, 0, 1) en une matrice donnée.
ms.assetid: ba8c1983-bd65-4249-9451-69d813e4a3a4
title: D3DXVec2TransformArray, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 38e60c6bb8084e7f8e1c0ee71379af552e73c09d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097927"
---
# <a name="d3dxvec2transformarray-function-d3dx9mathh"></a><span data-ttu-id="39f78-103">D3DXVec2TransformArray, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="39f78-103">D3DXVec2TransformArray function (D3dx9math.h)</span></span>

<span data-ttu-id="39f78-104">Transforme un tableau (x, y, 0, 1) en une matrice donnée.</span><span class="sxs-lookup"><span data-stu-id="39f78-104">Transforms an array (x, y, 0, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="39f78-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39f78-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec2TransformArray(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR2 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="39f78-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="39f78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39f78-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="39f78-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="39f78-108">Type : **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="39f78-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="39f78-109">Pointeur vers la structure [**D3DXVECTOR4**](d3dxvector4.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="39f78-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="39f78-110">En *Progress* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="39f78-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39f78-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="39f78-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="39f78-112">STRIDE entre les vecteurs dans le flux de données de sortie.</span><span class="sxs-lookup"><span data-stu-id="39f78-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="39f78-113">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="39f78-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39f78-114">Type : **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="39f78-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="39f78-115">Pointeur vers la structure [**D3DXVECTOR2**](d3dxvector2.md) source.</span><span class="sxs-lookup"><span data-stu-id="39f78-115">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="39f78-116">*VStride* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="39f78-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39f78-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="39f78-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="39f78-118">STRIDE entre les vecteurs dans le flux de données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="39f78-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="39f78-119">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="39f78-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39f78-120">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="39f78-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="39f78-121">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) source.</span><span class="sxs-lookup"><span data-stu-id="39f78-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="39f78-122">*n* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="39f78-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39f78-123">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="39f78-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="39f78-124">Nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="39f78-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39f78-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="39f78-125">Return value</span></span>

<span data-ttu-id="39f78-126">Type : **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="39f78-126">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="39f78-127">Pointeur vers une structure [**D3DXVECTOR4**](d3dxvector4.md) qui est le tableau transformé.</span><span class="sxs-lookup"><span data-stu-id="39f78-127">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="39f78-128">Notes </span><span class="sxs-lookup"><span data-stu-id="39f78-128">Remarks</span></span>

<span data-ttu-id="39f78-129">Cette fonction transforme *le tableau (* x, y, 0, 1) par la matrice *PM*.</span><span class="sxs-lookup"><span data-stu-id="39f78-129">This function transforms the array *pV* (x, y, 0, 1) by the matrix *pM*.</span></span>

<span data-ttu-id="39f78-130">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="39f78-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="39f78-131">De cette façon, la fonction [**D3DXVec2Transform**](d3dxvec2transform.md) peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="39f78-131">In this way, the [**D3DXVec2Transform**](d3dxvec2transform.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="39f78-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39f78-132">Requirements</span></span>



| <span data-ttu-id="39f78-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39f78-133">Requirement</span></span> | <span data-ttu-id="39f78-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="39f78-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="39f78-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="39f78-135">Header</span></span><br/>  | <dl> <span data-ttu-id="39f78-136"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="39f78-136"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="39f78-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="39f78-137">Library</span></span><br/> | <dl> <span data-ttu-id="39f78-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="39f78-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="39f78-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39f78-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39f78-140">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="39f78-140">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="39f78-141">**D3DXVec2TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="39f78-141">**D3DXVec2TransformCoord**</span></span>](d3dxvec2transformcoord.md)
</dt> <dt>

[<span data-ttu-id="39f78-142">**D3DXVec2TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="39f78-142">**D3DXVec2TransformNormal**</span></span>](d3dxvec2transformnormal.md)
</dt> </dl>

 

 
