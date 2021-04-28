---
description: D3DXVec2TransformNormal, fonction (D3DX10Math. h)-transforme le vecteur 2D normal par la matrice donnée.
ms.assetid: fc238bb1-155f-4018-9c92-16352726920d
title: D3DXVec2TransformNormal, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformNormal
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 403562ab779ebf532e1c1ebcec4ce21a2beadd7a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108297"
---
# <a name="d3dxvec2transformnormal-function-d3dx10mathh"></a><span data-ttu-id="7182a-103">D3DXVec2TransformNormal, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="7182a-103">D3DXVec2TransformNormal function (D3DX10Math.h)</span></span>

<span data-ttu-id="7182a-104">Transforme le vecteur 2D normal par la matrice donnée.</span><span class="sxs-lookup"><span data-stu-id="7182a-104">Transforms the 2D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="7182a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7182a-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformNormal(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="7182a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7182a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7182a-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7182a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7182a-108">Type : **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="7182a-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="7182a-109">Pointeur vers le [**D3DXVECTOR2**](d3d10-d3dxvector2.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="7182a-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7182a-110">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7182a-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7182a-111">Type : **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="7182a-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="7182a-112">Pointeur vers la structure D3DXVECTOR2 source.</span><span class="sxs-lookup"><span data-stu-id="7182a-112">Pointer to the source D3DXVECTOR2 structure.</span></span>

</dd> <dt>

<span data-ttu-id="7182a-113">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7182a-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7182a-114">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="7182a-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7182a-115">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) source.</span><span class="sxs-lookup"><span data-stu-id="7182a-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7182a-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7182a-116">Return value</span></span>

<span data-ttu-id="7182a-117">Type : **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="7182a-117">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="7182a-118">Pointeur vers une structure D3DXVECTOR2 qui est le vecteur transformé.</span><span class="sxs-lookup"><span data-stu-id="7182a-118">Pointer to a D3DXVECTOR2 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="7182a-119">Notes </span><span class="sxs-lookup"><span data-stu-id="7182a-119">Remarks</span></span>

<span data-ttu-id="7182a-120">Cette fonction transforme le vecteur (pV->x, pV->y, 0, 0) par la matrice désignée par pM.</span><span class="sxs-lookup"><span data-stu-id="7182a-120">This function transforms the vector (pV->x, pV->y, 0, 0) by the matrix pointed to by pM.</span></span>

<span data-ttu-id="7182a-121">Si vous souhaitez transformer un normal, la matrice que vous transmettez à cette fonction doit être la transposer de l’inverse de la matrice que vous utiliseriez pour transformer un point.</span><span class="sxs-lookup"><span data-stu-id="7182a-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="7182a-122">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="7182a-122">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="7182a-123">De cette façon, la fonction **D3DXVec2TransformNormal** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="7182a-123">In this way, the **D3DXVec2TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7182a-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7182a-124">Requirements</span></span>



| <span data-ttu-id="7182a-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7182a-125">Requirement</span></span> | <span data-ttu-id="7182a-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="7182a-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7182a-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="7182a-127">Header</span></span><br/>  | <dl> <span data-ttu-id="7182a-128"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7182a-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="7182a-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7182a-129">Library</span></span><br/> | <dl> <span data-ttu-id="7182a-130"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7182a-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7182a-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7182a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7182a-132">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="7182a-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
