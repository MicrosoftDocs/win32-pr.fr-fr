---
description: Transforme un tableau (x, y, z, 1) en une matrice donnée.
ms.assetid: f64c55df-ea93-4c93-be89-eee650e6ecf0
title: D3DXVec3TransformArray, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 9ae223d4e1b8c424230ba12719f25258dae18548
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043150"
---
# <a name="d3dxvec3transformarray-function-d3dx10mathh"></a><span data-ttu-id="b147f-103">D3DXVec3TransformArray, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="b147f-103">D3DXVec3TransformArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="b147f-104">Transforme un tableau (x, y, z, 1) en une matrice donnée.</span><span class="sxs-lookup"><span data-stu-id="b147f-104">Transforms an array (x, y, z, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="b147f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b147f-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec3TransformArray(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR3 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="b147f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b147f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b147f-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b147f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b147f-108">Type : **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="b147f-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="b147f-109">Pointeur vers le tableau [**D3DXVECTOR4**](d3d10-d3dxvector4.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="b147f-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) array that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b147f-110">En *Progress* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b147f-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b147f-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b147f-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b147f-112">STRIDE entre les vecteurs dans le flux de données de sortie.</span><span class="sxs-lookup"><span data-stu-id="b147f-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="b147f-113">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b147f-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b147f-114">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b147f-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="b147f-115">Pointeur vers le tableau [**D3DXVECTOR3**](d3d10-d3dxvector3.md) source.</span><span class="sxs-lookup"><span data-stu-id="b147f-115">Pointer to the source [**D3DXVECTOR3**](d3d10-d3dxvector3.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="b147f-116">*VStride* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b147f-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b147f-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b147f-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b147f-118">STRIDE entre les vecteurs dans le flux de données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b147f-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="b147f-119">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b147f-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b147f-120">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="b147f-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b147f-121">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) source.</span><span class="sxs-lookup"><span data-stu-id="b147f-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b147f-122">*n* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b147f-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b147f-123">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b147f-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b147f-124">Nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="b147f-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b147f-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b147f-125">Return value</span></span>

<span data-ttu-id="b147f-126">Type : **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="b147f-126">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="b147f-127">Pointeur vers un tableau transformé [**D3DXVECTOR4**](d3d10-d3dxvector4.md) .</span><span class="sxs-lookup"><span data-stu-id="b147f-127">Pointer to a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="b147f-128">Notes</span><span class="sxs-lookup"><span data-stu-id="b147f-128">Remarks</span></span>

<span data-ttu-id="b147f-129">Cette fonction transforme le tableau (x, y, z, 1) par la matrice pM.</span><span class="sxs-lookup"><span data-stu-id="b147f-129">This function transforms the array pV (x, y, z, 1) by the matrix pM.</span></span>

<span data-ttu-id="b147f-130">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="b147f-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="b147f-131">De cette façon, la fonction D3DXVec3TransformArray peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="b147f-131">In this way, the D3DXVec3TransformArray function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b147f-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b147f-132">Requirements</span></span>



| <span data-ttu-id="b147f-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b147f-133">Requirement</span></span> | <span data-ttu-id="b147f-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="b147f-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b147f-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="b147f-135">Header</span></span><br/> | <dl> <span data-ttu-id="b147f-136"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b147f-136"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b147f-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b147f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b147f-138">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="b147f-138">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
