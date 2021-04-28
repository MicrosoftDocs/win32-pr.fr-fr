---
description: D3DXVec2TransformNormalArray, fonction (D3dx9math. h)-transforme un tableau (x, y, 0, 0) en une matrice donnée.
ms.assetid: 9f5d8fdc-f3e1-41dc-be4e-9ffc6be1947f
title: D3DXVec2TransformNormalArray, fonction (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 71706551e73ed9bd52b41aae127625cd09b6d7f8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097889"
---
# <a name="d3dxvec2transformnormalarray-function-d3dx9mathh"></a><span data-ttu-id="a991f-103">D3DXVec2TransformNormalArray, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="a991f-103">D3DXVec2TransformNormalArray function (D3dx9math.h)</span></span>

<span data-ttu-id="a991f-104">Transforme un tableau (x, y, 0, 0) en une matrice donnée.</span><span class="sxs-lookup"><span data-stu-id="a991f-104">Transforms an array (x, y, 0, 0) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="a991f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a991f-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="a991f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a991f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a991f-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a991f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a991f-108">Type : **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="a991f-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="a991f-109">Pointeur vers la structure [**D3DXVECTOR2**](d3dxvector2.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="a991f-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a991f-110">En *Progress* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a991f-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a991f-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a991f-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a991f-112">STRIDE entre les vecteurs dans le flux de données de sortie.</span><span class="sxs-lookup"><span data-stu-id="a991f-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="a991f-113">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a991f-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a991f-114">Type : **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="a991f-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="a991f-115">Pointeur vers le tableau [**D3DXVECTOR2**](d3dxvector2.md) source.</span><span class="sxs-lookup"><span data-stu-id="a991f-115">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="a991f-116">*VStride* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a991f-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a991f-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a991f-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a991f-118">STRIDE entre les vecteurs dans le flux de données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="a991f-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="a991f-119">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a991f-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a991f-120">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="a991f-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a991f-121">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) source.</span><span class="sxs-lookup"><span data-stu-id="a991f-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a991f-122">*n* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a991f-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a991f-123">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a991f-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a991f-124">Nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="a991f-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a991f-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a991f-125">Return value</span></span>

<span data-ttu-id="a991f-126">Type : **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="a991f-126">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="a991f-127">Pointeur vers une structure [**D3DXVECTOR2**](d3dxvector2.md) qui est le tableau transformé.</span><span class="sxs-lookup"><span data-stu-id="a991f-127">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="a991f-128">Notes </span><span class="sxs-lookup"><span data-stu-id="a991f-128">Remarks</span></span>

<span data-ttu-id="a991f-129">Cette fonction transforme le vecteur (*PV-*>x, *PV-*>y, 0, 0) par la matrice désignée par *PM.*</span><span class="sxs-lookup"><span data-stu-id="a991f-129">This function transforms the vector (*pV-*>x, *pV-*>y, 0, 0) by the matrix pointed to by *pM.*</span></span>

<span data-ttu-id="a991f-130">Si vous souhaitez transformer un normal, la matrice que vous transmettez à cette fonction doit être la transposer de l’inverse de la matrice que vous utiliseriez pour transformer un point.</span><span class="sxs-lookup"><span data-stu-id="a991f-130">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="a991f-131">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="a991f-131">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="a991f-132">De cette façon, la fonction **D3DXVec2TransformNormalArray** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="a991f-132">In this way, the **D3DXVec2TransformNormalArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a991f-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a991f-133">Requirements</span></span>



| <span data-ttu-id="a991f-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a991f-134">Requirement</span></span> | <span data-ttu-id="a991f-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="a991f-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a991f-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="a991f-136">Header</span></span><br/>  | <dl> <span data-ttu-id="a991f-137"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a991f-137"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a991f-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a991f-138">Library</span></span><br/> | <dl> <span data-ttu-id="a991f-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a991f-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a991f-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a991f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a991f-141">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="a991f-141">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
