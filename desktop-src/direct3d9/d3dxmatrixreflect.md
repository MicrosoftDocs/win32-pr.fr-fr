---
description: Crée une matrice qui reflète le système de coordonnées d’un plan.
ms.assetid: f6dc3834-42f2-4ad0-8098-8c5e25e10d58
title: D3DXMatrixReflect, fonction (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2e54c5f93164e5fccee0d74199a1843a1476e69a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953796"
---
# <a name="d3dxmatrixreflect-function-d3dx9mathh"></a><span data-ttu-id="99c10-103">D3DXMatrixReflect, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="99c10-103">D3DXMatrixReflect function (D3dx9math.h)</span></span>

<span data-ttu-id="99c10-104">Crée une matrice qui reflète le système de coordonnées d’un plan.</span><span class="sxs-lookup"><span data-stu-id="99c10-104">Builds a matrix that reflects the coordinate system about a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="99c10-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99c10-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixReflect(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXPLANE  *pPlane
);
```



## <a name="parameters"></a><span data-ttu-id="99c10-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99c10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99c10-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="99c10-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="99c10-108">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="99c10-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="99c10-109">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="99c10-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="99c10-110">*pPlane* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="99c10-110">*pPlane* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99c10-111">Type : **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="99c10-111">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="99c10-112">Pointeur vers la structure [**D3DXPLANE**](d3dxplane.md) source.</span><span class="sxs-lookup"><span data-stu-id="99c10-112">Pointer to the source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99c10-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="99c10-113">Return value</span></span>

<span data-ttu-id="99c10-114">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="99c10-114">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="99c10-115">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) qui reflète le système de coordonnées du plan source.</span><span class="sxs-lookup"><span data-stu-id="99c10-115">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that reflects the coordinate system about the source plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="99c10-116">Notes</span><span class="sxs-lookup"><span data-stu-id="99c10-116">Remarks</span></span>

<span data-ttu-id="99c10-117">Cette fonction normalise l’équation plan avant de créer la matrice réfléchie.</span><span class="sxs-lookup"><span data-stu-id="99c10-117">This function normalizes the plane equation before it creates the reflected matrix.</span></span>

<span data-ttu-id="99c10-118">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="99c10-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="99c10-119">De cette façon, la fonction **D3DXMatrixReflect** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="99c10-119">In this way, the **D3DXMatrixReflect** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="99c10-120">Cette fonction utilise la formule suivante pour calculer la matrice retournée.</span><span class="sxs-lookup"><span data-stu-id="99c10-120">This function uses the following formula to compute the returned matrix.</span></span>


```
P = normalize(Plane);
    
-2 * P.a * P.a + 1  -2 * P.b * P.a      -2 * P.c * P.a        0
-2 * P.a * P.b      -2 * P.b * P.b + 1  -2 * P.c * P.b        0
-2 * P.a * P.c      -2 * P.b * P.c      -2 * P.c * P.c + 1    0
-2 * P.a * P.d      -2 * P.b * P.d      -2 * P.c * P.d        1
```



## <a name="requirements"></a><span data-ttu-id="99c10-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99c10-121">Requirements</span></span>



| <span data-ttu-id="99c10-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99c10-122">Requirement</span></span> | <span data-ttu-id="99c10-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="99c10-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="99c10-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="99c10-124">Header</span></span><br/>  | <dl> <span data-ttu-id="99c10-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="99c10-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="99c10-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="99c10-126">Library</span></span><br/> | <dl> <span data-ttu-id="99c10-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99c10-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="99c10-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99c10-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99c10-129">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="99c10-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




