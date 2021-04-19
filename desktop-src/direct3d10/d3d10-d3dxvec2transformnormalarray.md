---
description: Transforme un tableau (x, y, 0, 0) en une matrice donnée.
ms.assetid: a53f998a-f2a5-4e4b-bc1c-c1f46284d78b
title: D3DXVec2TransformNormalArray, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformNormalArray
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4850961560ae810b9a21f58fbefa9b6b07227c77
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538062"
---
# <a name="d3dxvec2transformnormalarray-function-d3dx10mathh"></a><span data-ttu-id="33643-103">D3DXVec2TransformNormalArray, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="33643-103">D3DXVec2TransformNormalArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="33643-104">Transforme un tableau (x, y, 0, 0) en une matrice donnée.</span><span class="sxs-lookup"><span data-stu-id="33643-104">Transforms an array (x, y, 0, 0) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="33643-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33643-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformNormalArray(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR2 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="33643-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="33643-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33643-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="33643-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="33643-108">Type : **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="33643-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="33643-109">Pointeur vers le [**D3DXVECTOR2**](d3d10-d3dxvector2.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="33643-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="33643-110">En *Progress* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="33643-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33643-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33643-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="33643-112">STRIDE entre les vecteurs dans le flux de données de sortie.</span><span class="sxs-lookup"><span data-stu-id="33643-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="33643-113">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="33643-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33643-114">Type : **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="33643-114">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="33643-115">Pointeur vers le tableau D3DXVECTOR2 source.</span><span class="sxs-lookup"><span data-stu-id="33643-115">Pointer to the source D3DXVECTOR2 array.</span></span>

</dd> <dt>

<span data-ttu-id="33643-116">*VStride* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="33643-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33643-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33643-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="33643-118">STRIDE entre les vecteurs dans le flux de données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="33643-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="33643-119">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="33643-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33643-120">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="33643-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="33643-121">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) source.</span><span class="sxs-lookup"><span data-stu-id="33643-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="33643-122">*n* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="33643-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33643-123">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33643-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="33643-124">Nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="33643-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33643-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="33643-125">Return value</span></span>

<span data-ttu-id="33643-126">Type : **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="33643-126">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="33643-127">Pointeur vers une structure D3DXVECTOR2 qui est le tableau transformé.</span><span class="sxs-lookup"><span data-stu-id="33643-127">Pointer to a D3DXVECTOR2 structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="33643-128">Notes</span><span class="sxs-lookup"><span data-stu-id="33643-128">Remarks</span></span>

<span data-ttu-id="33643-129">Cette fonction transforme le vecteur (pV->x, pV->y, 0, 0) par la matrice désignée par pM.</span><span class="sxs-lookup"><span data-stu-id="33643-129">This function transforms the vector (pV->x, pV->y, 0, 0) by the matrix pointed to by pM.</span></span>

<span data-ttu-id="33643-130">Si vous souhaitez transformer un normal, la matrice que vous transmettez à cette fonction doit être la transposer de l’inverse de la matrice que vous utiliseriez pour transformer un point.</span><span class="sxs-lookup"><span data-stu-id="33643-130">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="33643-131">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="33643-131">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="33643-132">De cette façon, la fonction **D3DXVec2TransformNormalArray** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="33643-132">In this way, the **D3DXVec2TransformNormalArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="33643-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33643-133">Requirements</span></span>



| <span data-ttu-id="33643-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33643-134">Requirement</span></span> | <span data-ttu-id="33643-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="33643-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="33643-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="33643-136">Header</span></span><br/>  | <dl> <span data-ttu-id="33643-137"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="33643-137"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="33643-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="33643-138">Library</span></span><br/> | <dl> <span data-ttu-id="33643-139"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="33643-139"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="33643-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33643-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33643-141">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="33643-141">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
