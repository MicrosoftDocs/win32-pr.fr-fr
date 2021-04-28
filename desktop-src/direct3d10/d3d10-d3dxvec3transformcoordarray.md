---
description: D3DXVec3TransformCoordArray, fonction (D3DX10Math. h)-transforme un tableau (x, y, z, 1) en une matrice donnée et projette le résultat dans w = 1.
ms.assetid: 259a885d-89be-4fea-a579-dac3dd76878f
title: D3DXVec3TransformCoordArray, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformCoordArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: c4a1edfd89b127d0782d3bab23c2390775422c69
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103107"
---
# <a name="d3dxvec3transformcoordarray-function-d3dx10mathh"></a><span data-ttu-id="93bea-103">D3DXVec3TransformCoordArray, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="93bea-103">D3DXVec3TransformCoordArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="93bea-104">Transforme un tableau (x, y, z, 1) en une matrice donnée et projette le résultat dans w = 1.</span><span class="sxs-lookup"><span data-stu-id="93bea-104">Transforms an array (x, y, z, 1) by a given matrix, and projects the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="93bea-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="93bea-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformCoordArray(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR3 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="93bea-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="93bea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93bea-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="93bea-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="93bea-108">Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="93bea-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="93bea-109">Pointeur vers le [**D3DXVECTOR3**](d3d10-d3dxvector3.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="93bea-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="93bea-110">En *Progress* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="93bea-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93bea-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="93bea-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="93bea-112">STRIDE entre les vecteurs dans le flux de données de sortie.</span><span class="sxs-lookup"><span data-stu-id="93bea-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="93bea-113">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="93bea-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93bea-114">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="93bea-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="93bea-115">Pointeur vers le tableau D3DXVECTOR3 source.</span><span class="sxs-lookup"><span data-stu-id="93bea-115">Pointer to the source D3DXVECTOR3 array.</span></span>

</dd> <dt>

<span data-ttu-id="93bea-116">*VStride* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="93bea-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93bea-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="93bea-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="93bea-118">STRIDE entre les vecteurs dans le flux de données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="93bea-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="93bea-119">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="93bea-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93bea-120">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="93bea-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="93bea-121">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) source.</span><span class="sxs-lookup"><span data-stu-id="93bea-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="93bea-122">*n* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="93bea-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93bea-123">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="93bea-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="93bea-124">Nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="93bea-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93bea-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="93bea-125">Return value</span></span>

<span data-ttu-id="93bea-126">Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="93bea-126">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="93bea-127">Pointeur vers une structure D3DXVECTOR3 qui est le tableau transformé.</span><span class="sxs-lookup"><span data-stu-id="93bea-127">Pointer to a D3DXVECTOR3 structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="93bea-128">Notes </span><span class="sxs-lookup"><span data-stu-id="93bea-128">Remarks</span></span>

<span data-ttu-id="93bea-129">Cette fonction transforme le tableau (x, y, z, 1) par la matrice pM, en reprojetant le résultat dans w = 1.</span><span class="sxs-lookup"><span data-stu-id="93bea-129">This function transforms the array pV (x, y, z, 1) by the matrix pM, projecting the result back into w = 1.</span></span>

<span data-ttu-id="93bea-130">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="93bea-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="93bea-131">De cette façon, la fonction [**D3DXVec3TransformCoord**](d3d10-d3dxvec3transformcoord.md) peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="93bea-131">In this way, the [**D3DXVec3TransformCoord**](d3d10-d3dxvec3transformcoord.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="93bea-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="93bea-132">Requirements</span></span>



| <span data-ttu-id="93bea-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="93bea-133">Requirement</span></span> | <span data-ttu-id="93bea-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="93bea-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93bea-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="93bea-135">Header</span></span><br/> | <dl> <span data-ttu-id="93bea-136"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="93bea-136"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93bea-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93bea-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93bea-138">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="93bea-138">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
