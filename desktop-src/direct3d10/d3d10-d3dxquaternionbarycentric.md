---
description: 'D3DXQuaternionBaryCentric, fonction (D3DX10Math. h) : retourne un Quaternion dans les coordonnées Barycentric.'
ms.assetid: 0a8d8d5a-f486-4457-86e9-27e76eaf1bc4
title: D3DXQuaternionBaryCentric, fonction (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 00d8e41a0173b7b26083f38beb82417365ef7067
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108777"
---
# <a name="d3dxquaternionbarycentric-function-d3dx10mathh"></a><span data-ttu-id="d57bf-103">D3DXQuaternionBaryCentric, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="d57bf-103">D3DXQuaternionBaryCentric function (D3DX10Math.h)</span></span>

<span data-ttu-id="d57bf-104">Retourne un Quaternion dans les coordonnées Barycentric.</span><span class="sxs-lookup"><span data-stu-id="d57bf-104">Returns a quaternion in barycentric coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="d57bf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d57bf-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="d57bf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d57bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d57bf-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d57bf-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d57bf-108">Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="d57bf-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d57bf-109">Pointeur vers le [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="d57bf-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d57bf-110">*pQ1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d57bf-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d57bf-111">Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="d57bf-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d57bf-112">Pointeur vers une structure D3DXQUATERNION source.</span><span class="sxs-lookup"><span data-stu-id="d57bf-112">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="d57bf-113">*pQ2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d57bf-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d57bf-114">Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="d57bf-114">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d57bf-115">Pointeur vers une structure D3DXQUATERNION source.</span><span class="sxs-lookup"><span data-stu-id="d57bf-115">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="d57bf-116">*pQ3* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d57bf-116">*pQ3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d57bf-117">Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="d57bf-117">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d57bf-118">Pointeur vers une structure D3DXQUATERNION source.</span><span class="sxs-lookup"><span data-stu-id="d57bf-118">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="d57bf-119">*f* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d57bf-119">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d57bf-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d57bf-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d57bf-121">Facteur de pondération.</span><span class="sxs-lookup"><span data-stu-id="d57bf-121">Weighting factor.</span></span> <span data-ttu-id="d57bf-122">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="d57bf-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d57bf-123">*g* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d57bf-123">*g* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d57bf-124">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d57bf-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d57bf-125">Facteur de pondération.</span><span class="sxs-lookup"><span data-stu-id="d57bf-125">Weighting factor.</span></span> <span data-ttu-id="d57bf-126">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="d57bf-126">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d57bf-127">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d57bf-127">Return value</span></span>

<span data-ttu-id="d57bf-128">Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="d57bf-128">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d57bf-129">Pointeur vers une structure D3DXQUATERNION dans les coordonnées Barycentric.</span><span class="sxs-lookup"><span data-stu-id="d57bf-129">Pointer to a D3DXQUATERNION structure in Barycentric coordinates.</span></span>

## <a name="remarks"></a><span data-ttu-id="d57bf-130">Notes </span><span class="sxs-lookup"><span data-stu-id="d57bf-130">Remarks</span></span>

<span data-ttu-id="d57bf-131">Pour calculer les coordonnées Barycentric, la fonction D3DXQuaternionBaryCentric implémente la série d’opérations d’interpolation linéaire sphérique suivantes :</span><span class="sxs-lookup"><span data-stu-id="d57bf-131">To compute the barycentric coordinates, the D3DXQuaternionBaryCentric function implements the following series of spherical linear interpolation operations:</span></span>


```
Slerp(Slerp(Q1, Q2, f+g), Slerp(Q1, Q3, f+g), g/(f+g))
```



<span data-ttu-id="d57bf-132">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="d57bf-132">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="d57bf-133">De cette façon, la fonction D3DXQuaternionBaryCentric peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="d57bf-133">In this way, the D3DXQuaternionBaryCentric function can be used as a parameter for another function.</span></span>

<span data-ttu-id="d57bf-134">Utilisez [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.</span><span class="sxs-lookup"><span data-stu-id="d57bf-134">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

<span data-ttu-id="d57bf-135">Les coordonnées Barycentric définissent un point à l’intérieur d’un triangle en termes de sommets du triangle.</span><span class="sxs-lookup"><span data-stu-id="d57bf-135">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="d57bf-136">Pour une description plus détaillée des coordonnées Barycentric, consultez [la description des coordonnées Barycentric de MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="d57bf-136">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="d57bf-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d57bf-137">Requirements</span></span>



| <span data-ttu-id="d57bf-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d57bf-138">Requirement</span></span> | <span data-ttu-id="d57bf-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="d57bf-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d57bf-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="d57bf-140">Header</span></span><br/>  | <dl> <span data-ttu-id="d57bf-141"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d57bf-141"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="d57bf-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d57bf-142">Library</span></span><br/> | <dl> <span data-ttu-id="d57bf-143"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d57bf-143"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d57bf-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d57bf-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d57bf-145">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="d57bf-145">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
