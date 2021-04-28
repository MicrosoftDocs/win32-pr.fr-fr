---
description: D3DXIntersectTri, fonction (D3DX10math. h)-calcule l’intersection d’un rayon et d’un triangle.
ms.assetid: 819f2543-8046-47c9-93b8-7d888264786f
title: D3DXIntersectTri, fonction (D3DX10math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c8bf502cca48701a7d71a083e515f9988cafe303
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113237"
---
# <a name="d3dxintersecttri-function-d3dx10mathh"></a><span data-ttu-id="817cb-103">D3DXIntersectTri, fonction (D3DX10math. h)</span><span class="sxs-lookup"><span data-stu-id="817cb-103">D3DXIntersectTri function (D3DX10math.h)</span></span>

<span data-ttu-id="817cb-104">Calcule l’intersection d’un rayon et d’un triangle.</span><span class="sxs-lookup"><span data-stu-id="817cb-104">Computes the intersection of a ray and a triangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="817cb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="817cb-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="817cb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="817cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="817cb-107">*P0* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="817cb-107">*p0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="817cb-108">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="817cb-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="817cb-109">Pointeur vers une structure [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , décrivant la première position du sommet de triangle.</span><span class="sxs-lookup"><span data-stu-id="817cb-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the first triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="817cb-110">*P1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="817cb-110">*p1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="817cb-111">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="817cb-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="817cb-112">Pointeur désignant une structure [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , décrivant la deuxième position du sommet du triangle.</span><span class="sxs-lookup"><span data-stu-id="817cb-112">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the second triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="817cb-113">*P2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="817cb-113">*p2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="817cb-114">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="817cb-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="817cb-115">Pointeur désignant une structure [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , décrivant la troisième position du sommet de triangle.</span><span class="sxs-lookup"><span data-stu-id="817cb-115">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the third triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="817cb-116">*pRayPos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="817cb-116">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="817cb-117">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="817cb-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="817cb-118">Pointeur vers une structure [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , en spécifiant le point de départ du rayon.</span><span class="sxs-lookup"><span data-stu-id="817cb-118">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="817cb-119">*pRayDir* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="817cb-119">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="817cb-120">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="817cb-120">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="817cb-121">Pointeur vers une structure [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , en spécifiant la direction du rayon.</span><span class="sxs-lookup"><span data-stu-id="817cb-121">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="817cb-122">*pu* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="817cb-122">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="817cb-123">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="817cb-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="817cb-124">Coordonnées d’accès Barycentric, U.</span><span class="sxs-lookup"><span data-stu-id="817cb-124">Barycentric hit coordinates, U.</span></span>

</dd> <dt>

<span data-ttu-id="817cb-125">*PV* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="817cb-125">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="817cb-126">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="817cb-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="817cb-127">Coordonnées d’accès Barycentric, V.</span><span class="sxs-lookup"><span data-stu-id="817cb-127">Barycentric hit coordinates, V.</span></span>

</dd> <dt>

<span data-ttu-id="817cb-128">*pDist* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="817cb-128">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="817cb-129">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="817cb-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="817cb-130">Distance des paramètres d’intersection de rayon.</span><span class="sxs-lookup"><span data-stu-id="817cb-130">Ray-intersection parameter distance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="817cb-131">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="817cb-131">Return value</span></span>

<span data-ttu-id="817cb-132">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="817cb-132">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="817cb-133">Retourne la **valeur true** si le rayon croise la zone du triangle.</span><span class="sxs-lookup"><span data-stu-id="817cb-133">Returns **TRUE** if the ray intersects the area of the triangle.</span></span> <span data-ttu-id="817cb-134">Sinon, retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="817cb-134">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="817cb-135">Notes </span><span class="sxs-lookup"><span data-stu-id="817cb-135">Remarks</span></span>

<span data-ttu-id="817cb-136">Tout point dans le plan V1V2V3 peut être représenté par la coordonnée Barycentric (U, V).</span><span class="sxs-lookup"><span data-stu-id="817cb-136">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="817cb-137">Le paramètre U contrôle combien v2 est pondéré dans le résultat, et le paramètre V contrôle combien v3 est pondéré dans le résultat.</span><span class="sxs-lookup"><span data-stu-id="817cb-137">The parameter U controls how much V2 gets weighted into the result, and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="817cb-138">Enfin, la valeur de \[ 1-(U + V) \] contrôle la quantité de valeurs v1 pondérée dans le résultat.</span><span class="sxs-lookup"><span data-stu-id="817cb-138">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="817cb-139">Les coordonnées Barycentric sont une forme de coordonnées générales.</span><span class="sxs-lookup"><span data-stu-id="817cb-139">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="817cb-140">Dans ce contexte, l’utilisation de coordonnées Barycentric représente une modification des systèmes de coordonnées.</span><span class="sxs-lookup"><span data-stu-id="817cb-140">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="817cb-141">Ce qui est vrai pour les coordonnées cartésiennes contient la valeur true pour les coordonnées Barycentric.</span><span class="sxs-lookup"><span data-stu-id="817cb-141">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="817cb-142">Les coordonnées Barycentric définissent un point à l’intérieur d’un triangle en termes de sommets du triangle.</span><span class="sxs-lookup"><span data-stu-id="817cb-142">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="817cb-143">Pour une description plus détaillée des coordonnées Barycentric, consultez [la description des coordonnées Barycentric de MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="817cb-143">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="817cb-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="817cb-144">Requirements</span></span>



| <span data-ttu-id="817cb-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="817cb-145">Requirement</span></span> | <span data-ttu-id="817cb-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="817cb-146">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="817cb-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="817cb-147">Header</span></span><br/>  | <dl> <span data-ttu-id="817cb-148"><dt>D3DX10math. h</dt></span><span class="sxs-lookup"><span data-stu-id="817cb-148"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="817cb-149">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="817cb-149">Library</span></span><br/> | <dl> <span data-ttu-id="817cb-150"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="817cb-150"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="817cb-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="817cb-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="817cb-152">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="817cb-152">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
