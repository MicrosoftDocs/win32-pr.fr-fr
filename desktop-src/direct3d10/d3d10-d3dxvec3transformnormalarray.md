---
description: Transforme un tableau (x, y, z, 0) en une matrice donnée.
ms.assetid: 7f0a41ce-bd3a-4e35-9a5d-8178a4e7bd44
title: D3DXVec3TransformNormalArray, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformNormalArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: facb5591becd27d3fff283e8d531118ca433d5d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527278"
---
# <a name="d3dxvec3transformnormalarray-function-d3dx10mathh"></a><span data-ttu-id="c8c63-103">D3DXVec3TransformNormalArray, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="c8c63-103">D3DXVec3TransformNormalArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="c8c63-104">Transforme un tableau (x, y, z, 0) en une matrice donnée.</span><span class="sxs-lookup"><span data-stu-id="c8c63-104">Transforms an array (x, y, z, 0) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8c63-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c8c63-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="c8c63-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c8c63-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8c63-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c8c63-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8c63-108">Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="c8c63-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="c8c63-109">Pointeur vers le tableau [**D3DXVECTOR3**](d3d10-d3dxvector3.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="c8c63-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) array that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c8c63-110">En *Progress* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c8c63-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8c63-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8c63-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c8c63-112">STRIDE entre les vecteurs dans le flux de données de sortie.</span><span class="sxs-lookup"><span data-stu-id="c8c63-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="c8c63-113">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c8c63-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8c63-114">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c8c63-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="c8c63-115">Pointeur vers le tableau D3DXVECTOR3 source.</span><span class="sxs-lookup"><span data-stu-id="c8c63-115">Pointer to the source D3DXVECTOR3 array.</span></span>

</dd> <dt>

<span data-ttu-id="c8c63-116">*VStride* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c8c63-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8c63-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8c63-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c8c63-118">STRIDE entre les vecteurs dans le flux de données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="c8c63-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="c8c63-119">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c8c63-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8c63-120">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c8c63-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c8c63-121">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) source.</span><span class="sxs-lookup"><span data-stu-id="c8c63-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c8c63-122">*n* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c8c63-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8c63-123">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8c63-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c8c63-124">Nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="c8c63-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8c63-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c8c63-125">Return value</span></span>

<span data-ttu-id="c8c63-126">Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="c8c63-126">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="c8c63-127">Pointeur vers un tableau D3DXVECTOR3 qui est le tableau transformé.</span><span class="sxs-lookup"><span data-stu-id="c8c63-127">Pointer to a D3DXVECTOR3 array that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8c63-128">Notes</span><span class="sxs-lookup"><span data-stu-id="c8c63-128">Remarks</span></span>

<span data-ttu-id="c8c63-129">Cette fonction transforme le vecteur (pV->x, pV->y, pV->z, 0) par la matrice vers laquelle pointe pM.</span><span class="sxs-lookup"><span data-stu-id="c8c63-129">This function transforms the vector (pV->x, pV->y, pV->z, 0) by the matrix pointed to by pM.</span></span>

<span data-ttu-id="c8c63-130">Si vous souhaitez transformer un normal, la matrice que vous transmettez à cette fonction doit être la transposer de l’inverse de la matrice que vous utiliseriez pour transformer un point.</span><span class="sxs-lookup"><span data-stu-id="c8c63-130">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="c8c63-131">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="c8c63-131">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="c8c63-132">De cette façon, la fonction **D3DXVec3TransformNormalArray** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="c8c63-132">In this way, the **D3DXVec3TransformNormalArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8c63-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c8c63-133">Requirements</span></span>



| <span data-ttu-id="c8c63-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c8c63-134">Requirement</span></span> | <span data-ttu-id="c8c63-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8c63-135">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8c63-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="c8c63-136">Header</span></span><br/> | <dl> <span data-ttu-id="c8c63-137"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8c63-137"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8c63-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8c63-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8c63-139">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="c8c63-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
