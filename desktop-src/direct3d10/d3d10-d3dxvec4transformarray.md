---
description: Transforme un tableau (x, y, z, w) en une matrice donnée.
ms.assetid: afd5cccb-e22f-4726-a84e-9eac1c1c277f
title: D3DXVec4TransformArray, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4TransformArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 5571fb19786e19a61c85741bcf6d4acb5231e977
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523211"
---
# <a name="d3dxvec4transformarray-function-d3dx10mathh"></a><span data-ttu-id="4e180-103">D3DXVec4TransformArray, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="4e180-103">D3DXVec4TransformArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="4e180-104">Transforme un tableau (x, y, z, w) en une matrice donnée.</span><span class="sxs-lookup"><span data-stu-id="4e180-104">Transforms an array (x, y, z, w) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e180-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e180-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4TransformArray(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR4 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="4e180-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e180-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e180-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4e180-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e180-108">Type : **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="4e180-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="4e180-109">Pointeur vers le tableau [**D3DXVECTOR4**](d3d10-d3dxvector4.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="4e180-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) array that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="4e180-110">En *Progress* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4e180-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e180-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e180-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e180-112">STRIDE entre les vecteurs dans le flux de données de sortie.</span><span class="sxs-lookup"><span data-stu-id="4e180-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="4e180-113">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4e180-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e180-114">Type : **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="4e180-114">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="4e180-115">Pointeur vers le tableau D3DXVECTOR4 source.</span><span class="sxs-lookup"><span data-stu-id="4e180-115">Pointer to the source D3DXVECTOR4 array.</span></span>

</dd> <dt>

<span data-ttu-id="4e180-116">*VStride* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4e180-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e180-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e180-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e180-118">STRIDE entre les vecteurs dans le flux de données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="4e180-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="4e180-119">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4e180-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e180-120">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="4e180-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4e180-121">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) source.</span><span class="sxs-lookup"><span data-stu-id="4e180-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4e180-122">*n* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4e180-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e180-123">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e180-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e180-124">Nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="4e180-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e180-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4e180-125">Return value</span></span>

<span data-ttu-id="4e180-126">Type : **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="4e180-126">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="4e180-127">Pointeur vers une structure [**D3DXVECTOR4**](d3d10-d3dxvector4.md) qui est le tableau transformé.</span><span class="sxs-lookup"><span data-stu-id="4e180-127">Pointer to a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e180-128">Notes</span><span class="sxs-lookup"><span data-stu-id="4e180-128">Remarks</span></span>

<span data-ttu-id="4e180-129">Cette fonction transforme le tableau pV (x, y, z, w) par la matrice pM.</span><span class="sxs-lookup"><span data-stu-id="4e180-129">This function transforms the array pV (x, y, z, w) by the matrix pM.</span></span>

<span data-ttu-id="4e180-130">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="4e180-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="4e180-131">De cette façon, la fonction **D3DXVec4TransformArray** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="4e180-131">In this way, the **D3DXVec4TransformArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e180-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e180-132">Requirements</span></span>



| <span data-ttu-id="4e180-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e180-133">Requirement</span></span> | <span data-ttu-id="4e180-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e180-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e180-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="4e180-135">Header</span></span><br/> | <dl> <span data-ttu-id="4e180-136"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e180-136"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e180-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e180-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e180-138">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="4e180-138">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
