---
description: D3DXIntersectTri, fonction (D3DX9Mesh. h)-calcule l’intersection d’un rayon et d’un triangle.
ms.assetid: f335a71d-7203-4ea1-a6bf-407b28c712e6
title: D3DXIntersectTri, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIntersectTri
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 33d45beda51a7a2c80debafbab864c2accb33653
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098267"
---
# <a name="d3dxintersecttri-function-d3dx9meshh"></a><span data-ttu-id="cd9fb-103">D3DXIntersectTri, fonction (D3DX9Mesh. h)</span><span class="sxs-lookup"><span data-stu-id="cd9fb-103">D3DXIntersectTri function (D3DX9Mesh.h)</span></span>

<span data-ttu-id="cd9fb-104">Calcule l’intersection d’un rayon et d’un triangle.</span><span class="sxs-lookup"><span data-stu-id="cd9fb-104">Computes the intersection of a ray and a triangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd9fb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cd9fb-105">Syntax</span></span>


```C++
BOOL D3DXIntersectTri(
  _In_  const D3DXVECTOR3 *p0,
  _In_  const D3DXVECTOR3 *p1,
  _In_  const D3DXVECTOR3 *p2,
  _In_  const D3DXVECTOR3 *pRayPos,
  _In_  const D3DXVECTOR3 *pRayDir,
  _Out_       FLOAT       *pU,
  _Out_       FLOAT       *pV,
  _Out_       FLOAT       *pDist
);
```



## <a name="parameters"></a><span data-ttu-id="cd9fb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cd9fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd9fb-107">*P0* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cd9fb-107">*p0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd9fb-108">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="cd9fb-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="cd9fb-109">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , décrivant la première position du sommet de triangle.</span><span class="sxs-lookup"><span data-stu-id="cd9fb-109">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the first triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="cd9fb-110">*P1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cd9fb-110">*p1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd9fb-111">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="cd9fb-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="cd9fb-112">Pointeur désignant une structure [**D3DXVECTOR3**](d3dxvector3.md) , décrivant la deuxième position du sommet du triangle.</span><span class="sxs-lookup"><span data-stu-id="cd9fb-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the second triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="cd9fb-113">*P2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cd9fb-113">*p2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd9fb-114">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="cd9fb-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="cd9fb-115">Pointeur désignant une structure [**D3DXVECTOR3**](d3dxvector3.md) , décrivant la troisième position du sommet de triangle.</span><span class="sxs-lookup"><span data-stu-id="cd9fb-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the third triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="cd9fb-116">*pRayPos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cd9fb-116">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd9fb-117">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="cd9fb-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="cd9fb-118">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , en spécifiant le point de départ du rayon.</span><span class="sxs-lookup"><span data-stu-id="cd9fb-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="cd9fb-119">*pRayDir* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cd9fb-119">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd9fb-120">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="cd9fb-120">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="cd9fb-121">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , en spécifiant la direction du rayon.</span><span class="sxs-lookup"><span data-stu-id="cd9fb-121">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="cd9fb-122">*pu* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cd9fb-122">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd9fb-123">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="cd9fb-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cd9fb-124">Coordonnées d’accès Barycentric, U.</span><span class="sxs-lookup"><span data-stu-id="cd9fb-124">Barycentric hit coordinates, U.</span></span>

</dd> <dt>

<span data-ttu-id="cd9fb-125">*PV* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cd9fb-125">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd9fb-126">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="cd9fb-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cd9fb-127">Coordonnées d’accès Barycentric, V.</span><span class="sxs-lookup"><span data-stu-id="cd9fb-127">Barycentric hit coordinates, V.</span></span>

</dd> <dt>

<span data-ttu-id="cd9fb-128">*pDist* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cd9fb-128">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd9fb-129">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="cd9fb-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cd9fb-130">Distance des paramètres d’intersection de rayon.</span><span class="sxs-lookup"><span data-stu-id="cd9fb-130">Ray-intersection parameter distance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd9fb-131">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cd9fb-131">Return value</span></span>

<span data-ttu-id="cd9fb-132">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cd9fb-132">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cd9fb-133">Retourne la **valeur true** si le rayon croise la zone du triangle.</span><span class="sxs-lookup"><span data-stu-id="cd9fb-133">Returns **TRUE** if the ray intersects the area of the triangle.</span></span> <span data-ttu-id="cd9fb-134">Sinon, retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="cd9fb-134">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd9fb-135">Notes </span><span class="sxs-lookup"><span data-stu-id="cd9fb-135">Remarks</span></span>

<span data-ttu-id="cd9fb-136">La fonction [**D3DXIntersect**](d3dxintersect.md) fournit un moyen de comprendre les points dans et autour d’un triangle, indépendamment de l’endroit où le triangle est réellement situé.</span><span class="sxs-lookup"><span data-stu-id="cd9fb-136">The [**D3DXIntersect**](d3dxintersect.md) function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="cd9fb-137">Cette fonction retourne le point résultant à l’aide de l’équation suivante : v1 + U (V2-V1) + V (v3-v1).</span><span class="sxs-lookup"><span data-stu-id="cd9fb-137">This function returns the resulting point by using the following equation: V1 + U(V2 - V1) + V(V3 - V1).</span></span>

<span data-ttu-id="cd9fb-138">Tout point dans le plan V1V2V3 peut être représenté par la coordonnée Barycentric (U, V).</span><span class="sxs-lookup"><span data-stu-id="cd9fb-138">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="cd9fb-139">Le paramètre U contrôle combien v2 est pondéré dans le résultat, et le paramètre V contrôle combien v3 est pondéré dans le résultat.</span><span class="sxs-lookup"><span data-stu-id="cd9fb-139">The parameter U controls how much V2 gets weighted into the result, and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="cd9fb-140">Enfin, la valeur de \[ 1-(U + V) \] contrôle la quantité de valeurs v1 pondérée dans le résultat.</span><span class="sxs-lookup"><span data-stu-id="cd9fb-140">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="cd9fb-141">Les coordonnées Barycentric sont une forme de coordonnées générales.</span><span class="sxs-lookup"><span data-stu-id="cd9fb-141">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="cd9fb-142">Dans ce contexte, l’utilisation de coordonnées Barycentric représente une modification des systèmes de coordonnées.</span><span class="sxs-lookup"><span data-stu-id="cd9fb-142">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="cd9fb-143">Ce qui est vrai pour les coordonnées cartésiennes contient la valeur true pour les coordonnées Barycentric.</span><span class="sxs-lookup"><span data-stu-id="cd9fb-143">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="cd9fb-144">Les coordonnées Barycentric définissent un point à l’intérieur d’un triangle en termes de sommets du triangle.</span><span class="sxs-lookup"><span data-stu-id="cd9fb-144">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="cd9fb-145">Pour une description plus détaillée des coordonnées Barycentric, consultez [la description des coordonnées Barycentric de MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="cd9fb-145">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd9fb-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cd9fb-146">Requirements</span></span>



| <span data-ttu-id="cd9fb-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cd9fb-147">Requirement</span></span> | <span data-ttu-id="cd9fb-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd9fb-148">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd9fb-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="cd9fb-149">Header</span></span><br/>  | <dl> <span data-ttu-id="cd9fb-150"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd9fb-150"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="cd9fb-151">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cd9fb-151">Library</span></span><br/> | <dl> <span data-ttu-id="cd9fb-152"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd9fb-152"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cd9fb-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd9fb-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd9fb-154">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="cd9fb-154">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
