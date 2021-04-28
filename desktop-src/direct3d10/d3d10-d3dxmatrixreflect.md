---
description: 'D3DXMatrixReflect, fonction (D3DX10Math. h) : crée une matrice qui reflète le système de coordonnées d’un plan.'
ms.assetid: bd2c5905-780e-4fac-a848-d7dbcfc390c6
title: D3DXMatrixReflect, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixReflect
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f96224c881dcd5db2cc1c356003ab96e8a626900
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103407"
---
# <a name="d3dxmatrixreflect-function-d3dx10mathh"></a><span data-ttu-id="3e579-103">D3DXMatrixReflect, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="3e579-103">D3DXMatrixReflect function (D3DX10Math.h)</span></span>

<span data-ttu-id="3e579-104">Crée une matrice qui reflète le système de coordonnées d’un plan.</span><span class="sxs-lookup"><span data-stu-id="3e579-104">Builds a matrix that reflects the coordinate system about a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e579-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3e579-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixReflect(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXPLANE  *pPlane
);
```



## <a name="parameters"></a><span data-ttu-id="3e579-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3e579-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e579-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3e579-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e579-108">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="3e579-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="3e579-109">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="3e579-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="3e579-110">*pPlane* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3e579-110">*pPlane* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e579-111">Type : **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="3e579-111">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="3e579-112">Pointeur vers le [**D3DXPLANE**](d3d10-d3dxplane.md)source.</span><span class="sxs-lookup"><span data-stu-id="3e579-112">Pointer to the source [**D3DXPLANE**](d3d10-d3dxplane.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e579-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3e579-113">Return value</span></span>

<span data-ttu-id="3e579-114">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="3e579-114">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="3e579-115">Pointeur vers une structure D3DXMATRIX qui reflète le système de coordonnées du plan source.</span><span class="sxs-lookup"><span data-stu-id="3e579-115">Pointer to a D3DXMATRIX structure that reflects the coordinate system about the source plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e579-116">Notes </span><span class="sxs-lookup"><span data-stu-id="3e579-116">Remarks</span></span>

<span data-ttu-id="3e579-117">Cette fonction normalise l’équation plan avant de créer la matrice réfléchie.</span><span class="sxs-lookup"><span data-stu-id="3e579-117">This function normalizes the plane equation before it creates the reflected matrix.</span></span>

<span data-ttu-id="3e579-118">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="3e579-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="3e579-119">De cette façon, la fonction D3DXMatrixReflect peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="3e579-119">In this way, the D3DXMatrixReflect function can be used as a parameter for another function.</span></span>

<span data-ttu-id="3e579-120">Cette fonction utilise la formule suivante pour calculer la matrice retournée.</span><span class="sxs-lookup"><span data-stu-id="3e579-120">This function uses the following formula to compute the returned matrix.</span></span>


```
P = normalize(Plane);
    
-2 * P.a * P.a + 1  -2 * P.b * P.a      -2 * P.c * P.a        0
-2 * P.a * P.b      -2 * P.b * P.b + 1  -2 * P.c * P.b        0
-2 * P.a * P.c      -2 * P.b * P.c      -2 * P.c * P.c + 1    0
-2 * P.a * P.d      -2 * P.b * P.d      -2 * P.c * P.d        1
```



## <a name="requirements"></a><span data-ttu-id="3e579-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e579-121">Requirements</span></span>



| <span data-ttu-id="3e579-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3e579-122">Requirement</span></span> | <span data-ttu-id="3e579-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e579-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e579-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="3e579-124">Header</span></span><br/>  | <dl> <span data-ttu-id="3e579-125"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e579-125"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="3e579-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3e579-126">Library</span></span><br/> | <dl> <span data-ttu-id="3e579-127"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3e579-127"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3e579-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e579-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e579-129">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="3e579-129">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
