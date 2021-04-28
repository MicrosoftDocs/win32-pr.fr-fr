---
description: D3DXVec3TransformNormalArray, fonction (D3dx9math. h)-transforme un tableau (x, y, z, 0) en une matrice donnée.
ms.assetid: c12fad52-d541-483f-a919-e6031aa4f761
title: D3DXVec3TransformNormalArray, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformNormalArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 74da959002bfbd0c488e630f09c89e848708b1b1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097727"
---
# <a name="d3dxvec3transformnormalarray-function-d3dx9mathh"></a><span data-ttu-id="26107-103">D3DXVec3TransformNormalArray, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="26107-103">D3DXVec3TransformNormalArray function (D3dx9math.h)</span></span>

<span data-ttu-id="26107-104">Transforme un tableau (x, y, z, 0) en une matrice donnée.</span><span class="sxs-lookup"><span data-stu-id="26107-104">Transforms an array (x, y, z, 0) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="26107-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26107-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformNormalArray(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR3 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="26107-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="26107-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26107-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="26107-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="26107-108">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="26107-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="26107-109">Pointeur vers le tableau [**D3DXVECTOR3**](d3dxvector3.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="26107-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) array that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="26107-110">En *Progress* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="26107-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26107-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="26107-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="26107-112">STRIDE entre les vecteurs dans le flux de données de sortie.</span><span class="sxs-lookup"><span data-stu-id="26107-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="26107-113">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="26107-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26107-114">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="26107-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="26107-115">Pointeur vers le tableau [**D3DXVECTOR3**](d3dxvector3.md) source.</span><span class="sxs-lookup"><span data-stu-id="26107-115">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="26107-116">*VStride* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="26107-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26107-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="26107-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="26107-118">STRIDE entre les vecteurs dans le flux de données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="26107-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="26107-119">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="26107-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26107-120">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="26107-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="26107-121">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) source.</span><span class="sxs-lookup"><span data-stu-id="26107-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="26107-122">*n* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="26107-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26107-123">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="26107-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="26107-124">Nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="26107-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26107-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="26107-125">Return value</span></span>

<span data-ttu-id="26107-126">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="26107-126">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="26107-127">Pointeur vers un tableau [**D3DXVECTOR3**](d3dxvector3.md) qui est le tableau transformé.</span><span class="sxs-lookup"><span data-stu-id="26107-127">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) array that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="26107-128">Notes </span><span class="sxs-lookup"><span data-stu-id="26107-128">Remarks</span></span>

<span data-ttu-id="26107-129">Cette fonction transforme le vecteur (*PV*->x, *PV*->y, *PV*->z, 0) par la matrice vers laquelle pointe *PM*.</span><span class="sxs-lookup"><span data-stu-id="26107-129">This function transforms the vector (*pV*->x, *pV*->y, *pV*->z, 0) by the matrix pointed to by *pM*.</span></span>

<span data-ttu-id="26107-130">Si vous souhaitez transformer un normal, la matrice que vous transmettez à cette fonction doit être la transposer de l’inverse de la matrice que vous utiliseriez pour transformer un point.</span><span class="sxs-lookup"><span data-stu-id="26107-130">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="26107-131">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="26107-131">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="26107-132">De cette façon, la fonction **D3DXVec3TransformNormalArray** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="26107-132">In this way, the **D3DXVec3TransformNormalArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="26107-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26107-133">Requirements</span></span>



| <span data-ttu-id="26107-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26107-134">Requirement</span></span> | <span data-ttu-id="26107-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="26107-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="26107-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="26107-136">Header</span></span><br/>  | <dl> <span data-ttu-id="26107-137"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="26107-137"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="26107-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="26107-138">Library</span></span><br/> | <dl> <span data-ttu-id="26107-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="26107-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="26107-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26107-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26107-141">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="26107-141">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
