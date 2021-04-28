---
description: D3DXVec2TransformCoordArray, fonction (D3DX10Math. h)-transforme un tableau (x, y, 0, 1) en une matrice donnée et projette le résultat dans w = 1.
ms.assetid: dba68678-2ab4-4f64-9975-5e9f2a20f66a
title: D3DXVec2TransformCoordArray, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformCoordArray
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f36b5fb5a5263f83c42ac66cc5f606fa1c4b75ab
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108327"
---
# <a name="d3dxvec2transformcoordarray-function-d3dx10mathh"></a><span data-ttu-id="aee4c-103">D3DXVec2TransformCoordArray, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="aee4c-103">D3DXVec2TransformCoordArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="aee4c-104">Transforme un tableau (x, y, 0, 1) en une matrice donnée et projette le résultat dans w = 1.</span><span class="sxs-lookup"><span data-stu-id="aee4c-104">Transforms an array (x, y, 0, 1) by a given matrix, and projects the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="aee4c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aee4c-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformCoordArray(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR2 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="aee4c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aee4c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aee4c-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="aee4c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="aee4c-108">Type : **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="aee4c-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="aee4c-109">Pointeur vers le [**D3DXVECTOR2**](d3d10-d3dxvector2.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="aee4c-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="aee4c-110">En *Progress* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="aee4c-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aee4c-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aee4c-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aee4c-112">STRIDE entre les vecteurs dans le flux de données de sortie.</span><span class="sxs-lookup"><span data-stu-id="aee4c-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="aee4c-113">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="aee4c-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aee4c-114">Type : **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="aee4c-114">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="aee4c-115">Pointeur vers le tableau D3DXVECTOR2 source.</span><span class="sxs-lookup"><span data-stu-id="aee4c-115">Pointer to the source D3DXVECTOR2 array.</span></span>

</dd> <dt>

<span data-ttu-id="aee4c-116">*VStride* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="aee4c-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aee4c-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aee4c-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aee4c-118">STRIDE entre les vecteurs dans le flux de données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="aee4c-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="aee4c-119">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="aee4c-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aee4c-120">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="aee4c-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="aee4c-121">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) source.</span><span class="sxs-lookup"><span data-stu-id="aee4c-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="aee4c-122">*n* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="aee4c-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aee4c-123">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aee4c-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aee4c-124">Nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="aee4c-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aee4c-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="aee4c-125">Return value</span></span>

<span data-ttu-id="aee4c-126">Type : **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="aee4c-126">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="aee4c-127">Pointeur vers un tableau transformé [**D3DXVECTOR4**](d3d10-d3dxvector4.md) .</span><span class="sxs-lookup"><span data-stu-id="aee4c-127">Pointer to a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="aee4c-128">Notes </span><span class="sxs-lookup"><span data-stu-id="aee4c-128">Remarks</span></span>

<span data-ttu-id="aee4c-129">Cette fonction transforme le tableau (x, y, 0, 1) par la matrice pM, en reprojetant le résultat dans w = 1.</span><span class="sxs-lookup"><span data-stu-id="aee4c-129">This function transforms the array pV (x, y, 0, 1) by the matrix pM, projecting the result back into w = 1.</span></span>

<span data-ttu-id="aee4c-130">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="aee4c-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="aee4c-131">De cette façon, la fonction D3DXVec2TransformCoordArray peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="aee4c-131">In this way, the D3DXVec2TransformCoordArray function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="aee4c-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aee4c-132">Requirements</span></span>



| <span data-ttu-id="aee4c-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aee4c-133">Requirement</span></span> | <span data-ttu-id="aee4c-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="aee4c-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aee4c-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="aee4c-135">Header</span></span><br/>  | <dl> <span data-ttu-id="aee4c-136"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="aee4c-136"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="aee4c-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="aee4c-137">Library</span></span><br/> | <dl> <span data-ttu-id="aee4c-138"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aee4c-138"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="aee4c-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aee4c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aee4c-140">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="aee4c-140">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
