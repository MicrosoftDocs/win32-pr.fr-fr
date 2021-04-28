---
description: 'D3DXQuaternionBaryCentric, fonction (D3dx9math. h) : retourne un Quaternion dans les coordonnées Barycentric.'
ms.assetid: 8fcd2e16-1bf1-4e18-afc9-17c92f2bbac5
title: D3DXQuaternionBaryCentric, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionBaryCentric
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2ce0cfc7b3a59dc2a3cae6fa240015e70a035695
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094107"
---
# <a name="d3dxquaternionbarycentric-function-d3dx9mathh"></a><span data-ttu-id="cbf50-103">D3DXQuaternionBaryCentric, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="cbf50-103">D3DXQuaternionBaryCentric function (D3dx9math.h)</span></span>

<span data-ttu-id="cbf50-104">Retourne un Quaternion dans les coordonnées Barycentric.</span><span class="sxs-lookup"><span data-stu-id="cbf50-104">Returns a quaternion in barycentric coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbf50-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cbf50-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionBaryCentric(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2,
  _In_    const D3DXQUATERNION *pQ3,
  _In_          FLOAT          f,
  _In_          FLOAT          g
);
```



## <a name="parameters"></a><span data-ttu-id="cbf50-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cbf50-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbf50-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="cbf50-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cbf50-108">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="cbf50-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="cbf50-109">Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="cbf50-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="cbf50-110">*pQ1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cbf50-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbf50-111">Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="cbf50-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="cbf50-112">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) source.</span><span class="sxs-lookup"><span data-stu-id="cbf50-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="cbf50-113">*pQ2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cbf50-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbf50-114">Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="cbf50-114">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="cbf50-115">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) source.</span><span class="sxs-lookup"><span data-stu-id="cbf50-115">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="cbf50-116">*pQ3* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cbf50-116">*pQ3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbf50-117">Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="cbf50-117">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="cbf50-118">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) source.</span><span class="sxs-lookup"><span data-stu-id="cbf50-118">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="cbf50-119">*f* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cbf50-119">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbf50-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cbf50-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cbf50-121">Facteur de pondération.</span><span class="sxs-lookup"><span data-stu-id="cbf50-121">Weighting factor.</span></span> <span data-ttu-id="cbf50-122">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="cbf50-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="cbf50-123">*g* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cbf50-123">*g* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbf50-124">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cbf50-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cbf50-125">Facteur de pondération.</span><span class="sxs-lookup"><span data-stu-id="cbf50-125">Weighting factor.</span></span> <span data-ttu-id="cbf50-126">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="cbf50-126">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbf50-127">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cbf50-127">Return value</span></span>

<span data-ttu-id="cbf50-128">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="cbf50-128">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="cbf50-129">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) dans les coordonnées Barycentric.</span><span class="sxs-lookup"><span data-stu-id="cbf50-129">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure in Barycentric coordinates.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbf50-130">Notes </span><span class="sxs-lookup"><span data-stu-id="cbf50-130">Remarks</span></span>

<span data-ttu-id="cbf50-131">Pour calculer les coordonnées Barycentric, la fonction **D3DXQuaternionBaryCentric** implémente la série d’opérations d’interpolation linéaire sphérique suivantes :</span><span class="sxs-lookup"><span data-stu-id="cbf50-131">To compute the barycentric coordinates, the **D3DXQuaternionBaryCentric** function implements the following series of spherical linear interpolation operations:</span></span>


```
Slerp(Slerp(Q1, Q2, f+g), Slerp(Q1, Q3, f+g), g/(f+g))
```



<span data-ttu-id="cbf50-132">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="cbf50-132">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="cbf50-133">De cette façon, la fonction **D3DXQuaternionBaryCentric** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="cbf50-133">In this way, the **D3DXQuaternionBaryCentric** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="cbf50-134">Utilisez [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.</span><span class="sxs-lookup"><span data-stu-id="cbf50-134">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

<span data-ttu-id="cbf50-135">Les coordonnées Barycentric définissent un point à l’intérieur d’un triangle en termes de sommets du triangle.</span><span class="sxs-lookup"><span data-stu-id="cbf50-135">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="cbf50-136">Pour une description plus détaillée des coordonnées Barycentric, consultez [la description des coordonnées Barycentric de MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="cbf50-136">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="cbf50-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cbf50-137">Requirements</span></span>



| <span data-ttu-id="cbf50-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cbf50-138">Requirement</span></span> | <span data-ttu-id="cbf50-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="cbf50-139">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cbf50-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="cbf50-140">Header</span></span><br/>  | <dl> <span data-ttu-id="cbf50-141"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbf50-141"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="cbf50-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cbf50-142">Library</span></span><br/> | <dl> <span data-ttu-id="cbf50-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cbf50-143"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cbf50-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cbf50-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbf50-145">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="cbf50-145">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
