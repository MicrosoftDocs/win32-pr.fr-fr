---
description: Transforme un tableau (x, y, 0, 1) en une matrice donnée et projette le résultat dans w = 1.
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
ms.openlocfilehash: aa57d96b0497fea572e580cfe6d1af2a0184f09d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106542187"
---
# <a name="d3dxvec2transformcoordarray-function-d3dx10mathh"></a><span data-ttu-id="13c63-103">D3DXVec2TransformCoordArray, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="13c63-103">D3DXVec2TransformCoordArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="13c63-104">Transforme un tableau (x, y, 0, 1) en une matrice donnée et projette le résultat dans w = 1.</span><span class="sxs-lookup"><span data-stu-id="13c63-104">Transforms an array (x, y, 0, 1) by a given matrix, and projects the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="13c63-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="13c63-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="13c63-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="13c63-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13c63-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="13c63-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="13c63-108">Type : **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="13c63-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="13c63-109">Pointeur vers le [**D3DXVECTOR2**](d3d10-d3dxvector2.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="13c63-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="13c63-110">En *Progress* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="13c63-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13c63-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="13c63-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="13c63-112">STRIDE entre les vecteurs dans le flux de données de sortie.</span><span class="sxs-lookup"><span data-stu-id="13c63-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="13c63-113">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="13c63-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13c63-114">Type : **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="13c63-114">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="13c63-115">Pointeur vers le tableau D3DXVECTOR2 source.</span><span class="sxs-lookup"><span data-stu-id="13c63-115">Pointer to the source D3DXVECTOR2 array.</span></span>

</dd> <dt>

<span data-ttu-id="13c63-116">*VStride* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="13c63-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13c63-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="13c63-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="13c63-118">STRIDE entre les vecteurs dans le flux de données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="13c63-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="13c63-119">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="13c63-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13c63-120">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="13c63-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="13c63-121">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) source.</span><span class="sxs-lookup"><span data-stu-id="13c63-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="13c63-122">*n* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="13c63-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13c63-123">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="13c63-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="13c63-124">Nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="13c63-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13c63-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="13c63-125">Return value</span></span>

<span data-ttu-id="13c63-126">Type : **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="13c63-126">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="13c63-127">Pointeur vers un tableau transformé [**D3DXVECTOR4**](d3d10-d3dxvector4.md) .</span><span class="sxs-lookup"><span data-stu-id="13c63-127">Pointer to a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="13c63-128">Notes</span><span class="sxs-lookup"><span data-stu-id="13c63-128">Remarks</span></span>

<span data-ttu-id="13c63-129">Cette fonction transforme le tableau (x, y, 0, 1) par la matrice pM, en reprojetant le résultat dans w = 1.</span><span class="sxs-lookup"><span data-stu-id="13c63-129">This function transforms the array pV (x, y, 0, 1) by the matrix pM, projecting the result back into w = 1.</span></span>

<span data-ttu-id="13c63-130">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="13c63-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="13c63-131">De cette façon, la fonction D3DXVec2TransformCoordArray peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="13c63-131">In this way, the D3DXVec2TransformCoordArray function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="13c63-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="13c63-132">Requirements</span></span>



| <span data-ttu-id="13c63-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="13c63-133">Requirement</span></span> | <span data-ttu-id="13c63-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="13c63-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13c63-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="13c63-135">Header</span></span><br/>  | <dl> <span data-ttu-id="13c63-136"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="13c63-136"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="13c63-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="13c63-137">Library</span></span><br/> | <dl> <span data-ttu-id="13c63-138"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="13c63-138"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="13c63-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13c63-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13c63-140">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="13c63-140">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
