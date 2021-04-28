---
description: 'D3DXVec4BaryCentric, fonction (D3DX10Math. h) : retourne un point dans les coordonnées Barycentric, à l’aide des vecteurs 4D spécifiés.'
ms.assetid: 44406135-3270-4f2e-bb53-29affb2510f2
title: D3DXVec4BaryCentric, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4BaryCentric
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 935432d1634a7fd35401d92471b1f366075ac8b7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102987"
---
# <a name="d3dxvec4barycentric-function-d3dx10mathh"></a><span data-ttu-id="591b6-103">D3DXVec4BaryCentric, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="591b6-103">D3DXVec4BaryCentric function (D3DX10Math.h)</span></span>

<span data-ttu-id="591b6-104">Retourne un point dans les coordonnées Barycentric, à l’aide des vecteurs 4D spécifiés.</span><span class="sxs-lookup"><span data-stu-id="591b6-104">Returns a point in Barycentric coordinates, using the specified 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="591b6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="591b6-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4BaryCentric(
  _In_       D3DXVECTOR4 *pOut,
  _In_ const D3DXVECTOR4 *pV1,
  _In_ const D3DXVECTOR4 *pV2,
  _In_ const D3DXVECTOR4 *pV3,
  _In_       FLOAT       f,
  _In_       FLOAT       g
);
```



## <a name="parameters"></a><span data-ttu-id="591b6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="591b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="591b6-107">*moue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="591b6-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="591b6-108">Type : **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="591b6-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="591b6-109">Pointeur vers le [**D3DXVECTOR4**](d3d10-d3dxvector4.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="591b6-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="591b6-110">*pV1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="591b6-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="591b6-111">Type : **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="591b6-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="591b6-112">Pointeur vers une structure D3DXVECTOR4 source.</span><span class="sxs-lookup"><span data-stu-id="591b6-112">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="591b6-113">*pV2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="591b6-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="591b6-114">Type : **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="591b6-114">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="591b6-115">Pointeur vers une structure D3DXVECTOR4 source.</span><span class="sxs-lookup"><span data-stu-id="591b6-115">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="591b6-116">*pV3* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="591b6-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="591b6-117">Type : **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="591b6-117">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="591b6-118">Pointeur vers une structure D3DXVECTOR4 source.</span><span class="sxs-lookup"><span data-stu-id="591b6-118">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="591b6-119">*f* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="591b6-119">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="591b6-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="591b6-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="591b6-121">Facteur de pondération.</span><span class="sxs-lookup"><span data-stu-id="591b6-121">Weighting factor.</span></span> <span data-ttu-id="591b6-122">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="591b6-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="591b6-123">*g* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="591b6-123">*g* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="591b6-124">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="591b6-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="591b6-125">Facteur de pondération.</span><span class="sxs-lookup"><span data-stu-id="591b6-125">Weighting factor.</span></span> <span data-ttu-id="591b6-126">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="591b6-126">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="591b6-127">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="591b6-127">Return value</span></span>

<span data-ttu-id="591b6-128">Type : **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="591b6-128">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="591b6-129">Pointeur vers une structure D3DXVECTOR4 dans les coordonnées Barycentric.</span><span class="sxs-lookup"><span data-stu-id="591b6-129">Pointer to a D3DXVECTOR4 structure in Barycentric coordinates.</span></span>

## <a name="remarks"></a><span data-ttu-id="591b6-130">Notes </span><span class="sxs-lookup"><span data-stu-id="591b6-130">Remarks</span></span>

<span data-ttu-id="591b6-131">La fonction D3DXVec4BaryCentric fournit un moyen de comprendre les points dans et autour d’un triangle, indépendamment de l’endroit où le triangle est réellement situé.</span><span class="sxs-lookup"><span data-stu-id="591b6-131">The D3DXVec4BaryCentric function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="591b6-132">Cette fonction retourne le point résultant à l’aide de l’équation suivante : v1 + f (V2-V1) + g (v3-v1).</span><span class="sxs-lookup"><span data-stu-id="591b6-132">This function returns the resulting point by using the following equation: V1 + f(V2-V1) + g(V3-V1).</span></span>

<span data-ttu-id="591b6-133">Tout point dans le plan V1V2V3 peut être représenté par la coordonnée Barycentric (f, g). Le paramètre f contrôle combien v2 est pondéré dans le résultat et le paramètre g contrôle combien v3 est pondéré dans le résultat.</span><span class="sxs-lookup"><span data-stu-id="591b6-133">Any point in the plane V1V2V3 can be represented by the Barycentric coordinate (f,g).The parameter f controls how much V2 gets weighted into the result and the parameter g controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="591b6-134">Enfin, 1-f-g contrôle la quantité de v1 qui est pondérée dans le résultat.</span><span class="sxs-lookup"><span data-stu-id="591b6-134">Lastly, 1-f-g controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="591b6-135">Notez les relations suivantes.</span><span class="sxs-lookup"><span data-stu-id="591b6-135">Note the following relations.</span></span>

-   <span data-ttu-id="591b6-136">Si (f>= 0 &, & g>= 0 &, & 1-f-g>= 0), le point se trouve à l’intérieur du triangle V1V2V3.</span><span class="sxs-lookup"><span data-stu-id="591b6-136">If (f>=0 &, & g>=0 &, & 1-f-g>=0), the point is inside the triangle V1V2V3.</span></span>
-   <span data-ttu-id="591b6-137">Si (f = = 0 &, & g>= 0 &, & 1-f-g>= 0), le point se trouve sur la ligne V1V3.</span><span class="sxs-lookup"><span data-stu-id="591b6-137">If (f==0 &, & g>=0 &, & 1-f-g>=0), the point is on the line V1V3.</span></span>
-   <span data-ttu-id="591b6-138">Si (f>= 0 &, & g = = 0 &, & 1-f-g>= 0), le point se trouve sur la ligne V1V2.</span><span class="sxs-lookup"><span data-stu-id="591b6-138">If (f>=0 &, & g==0 &, & 1-f-g>=0), the point is on the line V1V2.</span></span>
-   <span data-ttu-id="591b6-139">Si (f>= 0 &, & g>= 0 &, & 1-f-g = = 0), le point se trouve sur la ligne V2V3.</span><span class="sxs-lookup"><span data-stu-id="591b6-139">If (f>=0 &, & g>=0 &, & 1-f-g==0), the point is on the line V2V3.</span></span>

<span data-ttu-id="591b6-140">Les coordonnées Barycentric sont une forme de coordonnées générales.</span><span class="sxs-lookup"><span data-stu-id="591b6-140">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="591b6-141">Dans ce contexte, l’utilisation de coordonnées Barycentric représente une modification des systèmes de coordonnées.</span><span class="sxs-lookup"><span data-stu-id="591b6-141">In this context, using Barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="591b6-142">Ce qui est vrai pour les coordonnées cartésiennes contient la valeur true pour les coordonnées Barycentric.</span><span class="sxs-lookup"><span data-stu-id="591b6-142">What holds true for Cartesian coordinates holds true for Barycentric coordinates.</span></span>

<span data-ttu-id="591b6-143">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="591b6-143">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="591b6-144">De cette façon, la fonction D3DXVec4BaryCentric peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="591b6-144">In this way, the D3DXVec4BaryCentric function can be used as a parameter for another function.</span></span>

<span data-ttu-id="591b6-145">Les coordonnées Barycentric définissent un point à l’intérieur d’un triangle en termes de sommets du triangle.</span><span class="sxs-lookup"><span data-stu-id="591b6-145">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="591b6-146">Pour une description plus détaillée des coordonnées Barycentric, consultez [la description des coordonnées Barycentric de MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="591b6-146">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="591b6-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="591b6-147">Requirements</span></span>



| <span data-ttu-id="591b6-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="591b6-148">Requirement</span></span> | <span data-ttu-id="591b6-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="591b6-149">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="591b6-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="591b6-150">Header</span></span><br/> | <dl> <span data-ttu-id="591b6-151"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="591b6-151"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="591b6-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="591b6-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="591b6-153">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="591b6-153">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
