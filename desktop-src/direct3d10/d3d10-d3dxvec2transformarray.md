---
description: Transforme un tableau (x, y, 0, 1) en une matrice donnée.
ms.assetid: 66c8909c-6c20-4b32-9546-fcf2d0e824fa
title: D3DXVec2TransformArray, fonction (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c5aef5ecaa720e8c859d37f03ce88223187d16f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870114"
---
# <a name="d3dxvec2transformarray-function-d3dx10mathh"></a><span data-ttu-id="0ab51-103">D3DXVec2TransformArray, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="0ab51-103">D3DXVec2TransformArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="0ab51-104">Transforme un tableau (x, y, 0, 1) en une matrice donnée.</span><span class="sxs-lookup"><span data-stu-id="0ab51-104">Transforms an array (x, y, 0, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ab51-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ab51-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="0ab51-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0ab51-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ab51-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0ab51-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ab51-108">Type : **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="0ab51-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="0ab51-109">Pointeur vers la structure [**D3DXVECTOR4**](d3d10-d3dxvector4.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="0ab51-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0ab51-110">En *Progress* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0ab51-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ab51-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0ab51-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0ab51-112">STRIDE entre les vecteurs dans le flux de données de sortie.</span><span class="sxs-lookup"><span data-stu-id="0ab51-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="0ab51-113">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0ab51-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ab51-114">Type : **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="0ab51-114">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="0ab51-115">Pointeur vers le [**D3DXVECTOR2**](d3d10-d3dxvector2.md)source.</span><span class="sxs-lookup"><span data-stu-id="0ab51-115">Pointer to the source [**D3DXVECTOR2**](d3d10-d3dxvector2.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ab51-116">*VStride* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0ab51-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ab51-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0ab51-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0ab51-118">STRIDE entre les vecteurs dans le flux de données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="0ab51-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="0ab51-119">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0ab51-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ab51-120">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="0ab51-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0ab51-121">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) source.</span><span class="sxs-lookup"><span data-stu-id="0ab51-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0ab51-122">*n* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0ab51-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ab51-123">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0ab51-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0ab51-124">Nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="0ab51-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ab51-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0ab51-125">Return value</span></span>

<span data-ttu-id="0ab51-126">Type : **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="0ab51-126">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="0ab51-127">Pointeur vers une structure D3DXVECTOR4 qui est le tableau transformé.</span><span class="sxs-lookup"><span data-stu-id="0ab51-127">Pointer to a D3DXVECTOR4 structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ab51-128">Notes</span><span class="sxs-lookup"><span data-stu-id="0ab51-128">Remarks</span></span>

<span data-ttu-id="0ab51-129">Cette fonction transforme le tableau (x, y, 0, 1) par la matrice pM.</span><span class="sxs-lookup"><span data-stu-id="0ab51-129">This function transforms the array pV (x, y, 0, 1) by the matrix pM.</span></span>

<span data-ttu-id="0ab51-130">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="0ab51-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="0ab51-131">De cette façon, la fonction [**D3DXVec2Transform**](d3d10-d3dxvec2transform.md) peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="0ab51-131">In this way, the [**D3DXVec2Transform**](d3d10-d3dxvec2transform.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ab51-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0ab51-132">Requirements</span></span>



| <span data-ttu-id="0ab51-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0ab51-133">Requirement</span></span> | <span data-ttu-id="0ab51-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ab51-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ab51-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="0ab51-135">Header</span></span><br/>  | <dl> <span data-ttu-id="0ab51-136"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ab51-136"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="0ab51-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0ab51-137">Library</span></span><br/> | <dl> <span data-ttu-id="0ab51-138"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0ab51-138"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0ab51-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ab51-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ab51-140">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="0ab51-140">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
