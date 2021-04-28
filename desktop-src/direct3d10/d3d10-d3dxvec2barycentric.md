---
description: 'D3DXVec2BaryCentric, fonction (D3DX10Math. h) : retourne un point dans les coordonnées Barycentric, à l’aide des vecteurs 2D spécifiés.'
ms.assetid: 8eceb2c0-26a0-4a7f-9830-85327dcb31ab
title: D3DXVec2BaryCentric, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2BaryCentric
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5b78d08c67fed04af9ef0d54d0c6895106b99208
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108440"
---
# <a name="d3dxvec2barycentric-function-d3dx10mathh"></a><span data-ttu-id="cd2af-103">D3DXVec2BaryCentric, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="cd2af-103">D3DXVec2BaryCentric function (D3DX10Math.h)</span></span>

<span data-ttu-id="cd2af-104">Retourne un point dans les coordonnées Barycentric, à l’aide des vecteurs 2D spécifiés.</span><span class="sxs-lookup"><span data-stu-id="cd2af-104">Returns a point in Barycentric coordinates, using the specified 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd2af-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cd2af-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2BaryCentric(
  _In_       D3DXVECTOR2 *pOut,
  _In_ const D3DXVECTOR2 *pV1,
  _In_ const D3DXVECTOR2 *pV2,
  _In_ const D3DXVECTOR2 *pV3,
  _In_       FLOAT       f,
  _In_       FLOAT       g
);
```



## <a name="parameters"></a><span data-ttu-id="cd2af-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cd2af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd2af-107">*moue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cd2af-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd2af-108">Type : **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="cd2af-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="cd2af-109">Pointeur vers le [**D3DXVECTOR2**](d3d10-d3dxvector2.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="cd2af-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="cd2af-110">*pV1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cd2af-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd2af-111">Type : **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="cd2af-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="cd2af-112">Pointeur vers une structure D3DXVECTOR2 source.</span><span class="sxs-lookup"><span data-stu-id="cd2af-112">Pointer to a source D3DXVECTOR2 structure.</span></span>

</dd> <dt>

<span data-ttu-id="cd2af-113">*pV2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cd2af-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd2af-114">Type : **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="cd2af-114">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="cd2af-115">Pointeur vers une structure D3DXVECTOR2 source.</span><span class="sxs-lookup"><span data-stu-id="cd2af-115">Pointer to a source D3DXVECTOR2 structure.</span></span>

</dd> <dt>

<span data-ttu-id="cd2af-116">*pV3* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cd2af-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd2af-117">Type : **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="cd2af-117">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="cd2af-118">Pointeur vers une structure D3DXVECTOR2 source.</span><span class="sxs-lookup"><span data-stu-id="cd2af-118">Pointer to a source D3DXVECTOR2 structure.</span></span>

</dd> <dt>

<span data-ttu-id="cd2af-119">*f* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cd2af-119">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd2af-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cd2af-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cd2af-121">Facteur de pondération.</span><span class="sxs-lookup"><span data-stu-id="cd2af-121">Weighting factor.</span></span> <span data-ttu-id="cd2af-122">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="cd2af-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="cd2af-123">*g* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cd2af-123">*g* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd2af-124">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cd2af-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cd2af-125">Facteur de pondération.</span><span class="sxs-lookup"><span data-stu-id="cd2af-125">Weighting factor.</span></span> <span data-ttu-id="cd2af-126">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="cd2af-126">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd2af-127">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cd2af-127">Return value</span></span>

<span data-ttu-id="cd2af-128">Type : **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="cd2af-128">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="cd2af-129">Pointeur vers une structure D3DXVECTOR2 dans les coordonnées Barycentric.</span><span class="sxs-lookup"><span data-stu-id="cd2af-129">Pointer to a D3DXVECTOR2 structure in Barycentric coordinates.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd2af-130">Notes </span><span class="sxs-lookup"><span data-stu-id="cd2af-130">Remarks</span></span>

<span data-ttu-id="cd2af-131">La fonction D3DXVec2BaryCentric fournit un moyen de comprendre les points dans et autour d’un triangle, indépendamment de l’endroit où le triangle est réellement situé.</span><span class="sxs-lookup"><span data-stu-id="cd2af-131">The D3DXVec2BaryCentric function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="cd2af-132">Cette fonction retourne le point résultant à l’aide de l’équation suivante : v1 + f (V2-V1) + g (v3-v1).</span><span class="sxs-lookup"><span data-stu-id="cd2af-132">This function returns the resulting point by using the following equation: V1 + f(V2-V1) + g(V3-V1).</span></span>

<span data-ttu-id="cd2af-133">Tout point dans le plan V1V2V3 peut être représenté par la coordonnée Barycentric (f, g). Le paramètre f contrôle combien v2 est pondéré dans le résultat, et le paramètre g contrôle combien v3 est pondéré dans le résultat.</span><span class="sxs-lookup"><span data-stu-id="cd2af-133">Any point in the plane V1V2V3 can be represented by the Barycentric coordinate (f,g).The parameter f controls how much V2 gets weighted into the result, and the parameter g controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="cd2af-134">Enfin, 1-f-g contrôle la quantité de v1 qui est pondérée dans le résultat.</span><span class="sxs-lookup"><span data-stu-id="cd2af-134">Lastly, 1-f-g controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="cd2af-135">Notez les relations suivantes.</span><span class="sxs-lookup"><span data-stu-id="cd2af-135">Note the following relations.</span></span>

-   <span data-ttu-id="cd2af-136">Si (f>= 0 &, & g>= 0 &, & 1-f-g>= 0), le point se trouve à l’intérieur du triangle V1V2V3.</span><span class="sxs-lookup"><span data-stu-id="cd2af-136">If (f>=0 &, & g>=0 &, & 1-f-g>=0), the point is inside the triangle V1V2V3.</span></span>
-   <span data-ttu-id="cd2af-137">Si (f = = 0 &, & g>= 0 &, & 1-f-g>= 0), le point se trouve sur la ligne V1V3.</span><span class="sxs-lookup"><span data-stu-id="cd2af-137">If (f==0 &, & g>=0 &, & 1-f-g>=0), the point is on the line V1V3.</span></span>
-   <span data-ttu-id="cd2af-138">Si (f>= 0 &, & g = = 0 &, & 1-f-g>= 0), le point se trouve sur la ligne V1V2.</span><span class="sxs-lookup"><span data-stu-id="cd2af-138">If (f>=0 &, & g==0 &, & 1-f-g>=0), the point is on the line V1V2.</span></span>
-   <span data-ttu-id="cd2af-139">Si (f>= 0 &, & g>= 0 &, & 1-f-g = = 0), le point se trouve sur la ligne V2V3.</span><span class="sxs-lookup"><span data-stu-id="cd2af-139">If (f>=0 &, & g>=0 &, & 1-f-g==0), the point is on the line V2V3.</span></span>

<span data-ttu-id="cd2af-140">Les coordonnées Barycentric sont une forme de coordonnées générales.</span><span class="sxs-lookup"><span data-stu-id="cd2af-140">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="cd2af-141">Dans ce contexte, l’utilisation de coordonnées Barycentric représente une modification des systèmes de coordonnées.</span><span class="sxs-lookup"><span data-stu-id="cd2af-141">In this context, using Barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="cd2af-142">Ce qui est vrai pour les coordonnées cartésiennes contient la valeur true pour les coordonnées Barycentric.</span><span class="sxs-lookup"><span data-stu-id="cd2af-142">What holds true for Cartesian coordinates holds true for Barycentric coordinates.</span></span>

<span data-ttu-id="cd2af-143">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="cd2af-143">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="cd2af-144">De cette façon, la fonction D3DXVec2BaryCentric peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="cd2af-144">In this way, the D3DXVec2BaryCentric function can be used as a parameter for another function.</span></span>

<span data-ttu-id="cd2af-145">Les coordonnées Barycentric définissent un point à l’intérieur d’un triangle en termes de sommets du triangle.</span><span class="sxs-lookup"><span data-stu-id="cd2af-145">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="cd2af-146">Pour une description plus détaillée des coordonnées Barycentric, consultez [la description des coordonnées Barycentric de MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="cd2af-146">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd2af-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cd2af-147">Requirements</span></span>



| <span data-ttu-id="cd2af-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cd2af-148">Requirement</span></span> | <span data-ttu-id="cd2af-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd2af-149">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd2af-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="cd2af-150">Header</span></span><br/>  | <dl> <span data-ttu-id="cd2af-151"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd2af-151"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="cd2af-152">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cd2af-152">Library</span></span><br/> | <dl> <span data-ttu-id="cd2af-153"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd2af-153"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cd2af-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd2af-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd2af-155">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="cd2af-155">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
