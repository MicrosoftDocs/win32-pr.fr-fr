---
description: Utilise l’efficacité du traçage de rayon dans les simulations de transfert luminance (PRT) précalculées pour déterminer si un rayon croise une maille.
ms.assetid: e506aed3-bf14-4f29-845b-2091f5b00950
title: 'ID3DXPRTEngine :: ClosestRayIntersects, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ClosestRayIntersects
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4fd802f636077c9ec2a9f0f1060ffd43493aabf1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211921"
---
# <a name="id3dxprtengineclosestrayintersects-method"></a><span data-ttu-id="b1499-103">ID3DXPRTEngine :: ClosestRayIntersects, méthode</span><span class="sxs-lookup"><span data-stu-id="b1499-103">ID3DXPRTEngine::ClosestRayIntersects method</span></span>

<span data-ttu-id="b1499-104">Utilise l’efficacité du traçage de rayon dans les simulations de transfert luminance (PRT) précalculées pour déterminer si un rayon croise une maille.</span><span class="sxs-lookup"><span data-stu-id="b1499-104">Uses efficient ray-tracing in precomputed radiance transfer (PRT) simulations to determine whether a ray intersects a mesh.</span></span> <span data-ttu-id="b1499-105">Si une intersection est trouvée, la méthode retourne l’index du trait de filet le plus proche atteint par le rayon et les coordonnées Barycentric du point d’intersection.</span><span class="sxs-lookup"><span data-stu-id="b1499-105">If an intersection is found, the method returns the index of the closest mesh face hit by the ray and the barycentric coordinates of the intersection point.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1499-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1499-106">Syntax</span></span>


```C++
BOOL ClosestRayIntersects(
  [in]  const D3DXVECTOR3 *pRayPos,
  [in]  const D3DXVECTOR3 *pRayDir,
  [in]        DWORD       *pFaceIndex,
  [out]       FLOAT       *pU,
  [out]       FLOAT       *pV,
  [out]       FLOAT       *pDist
);
```



## <a name="parameters"></a><span data-ttu-id="b1499-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b1499-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1499-108">*pRayPos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b1499-108">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1499-109">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b1499-109">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="b1499-110">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , en spécifiant le point de départ du rayon.</span><span class="sxs-lookup"><span data-stu-id="b1499-110">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="b1499-111">*pRayDir* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b1499-111">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1499-112">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b1499-112">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="b1499-113">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , en spécifiant la direction normalisée du rayon.</span><span class="sxs-lookup"><span data-stu-id="b1499-113">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the normalized direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="b1499-114">*pFaceIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b1499-114">*pFaceIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1499-115">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b1499-115">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b1499-116">Pointeur vers l’index du visage de maillage actuel qui est atteint pour la première fois par le rayon donné, en se basant sur l’empilement de tous les visages de maillage de blocage devant le maillage actuel.</span><span class="sxs-lookup"><span data-stu-id="b1499-116">Pointer to the index of the current mesh face that is first hit by the given ray, based upon stacking all blocker mesh faces in front of the current mesh.</span></span>

</dd> <dt>

<span data-ttu-id="b1499-117">*pu* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b1499-117">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1499-118">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b1499-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b1499-119">Pointeur vers une coordonnée d’accès Barycentric, U, pour le vertex 0 du triangle.</span><span class="sxs-lookup"><span data-stu-id="b1499-119">Pointer to a barycentric hit coordinate, U, for vertex 0 of the triangle.</span></span>

</dd> <dt>

<span data-ttu-id="b1499-120">*PV* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b1499-120">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1499-121">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b1499-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b1499-122">Pointeur vers une coordonnée d’accès Barycentric, V, pour le vertex 1 du triangle.</span><span class="sxs-lookup"><span data-stu-id="b1499-122">Pointer to a barycentric hit coordinate, V, for vertex 1 of the triangle.</span></span>

</dd> <dt>

<span data-ttu-id="b1499-123">*pDist* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b1499-123">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1499-124">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b1499-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b1499-125">Pointeur désignant la distance entre le point d’intersection et le rayon.</span><span class="sxs-lookup"><span data-stu-id="b1499-125">Pointer to the distance of the intersection point along the ray.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1499-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b1499-126">Return value</span></span>

<span data-ttu-id="b1499-127">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1499-127">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1499-128">Retourne la **valeur true** si le rayon croise le maillage actuel ; Sinon, retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="b1499-128">Returns **TRUE** if the ray intersects the current mesh; otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1499-129">Notes</span><span class="sxs-lookup"><span data-stu-id="b1499-129">Remarks</span></span>

<span data-ttu-id="b1499-130">Utilisez [**ID3DXPRTEngine :: SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) pour définir les distances minimale et maximale de l’intersection avec le rayon.</span><span class="sxs-lookup"><span data-stu-id="b1499-130">Use [**ID3DXPRTEngine::SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) to set minimum and maximum distances of intersection with the ray.</span></span>

<span data-ttu-id="b1499-131">La coordonnée Barycentric du troisième vertex (Vertex 2) du triangle est 1-(U + V).</span><span class="sxs-lookup"><span data-stu-id="b1499-131">The barycentric coordinate of the third vertex (vertex 2) of the triangle is 1 - ( U + V ).</span></span>

<span data-ttu-id="b1499-132">Cette méthode s’exécute plus lentement que [**ID3DXPRTEngine :: ShadowRayIntersects**](id3dxprtengine--shadowrayintersects.md).</span><span class="sxs-lookup"><span data-stu-id="b1499-132">This method executes slower than [**ID3DXPRTEngine::ShadowRayIntersects**](id3dxprtengine--shadowrayintersects.md).</span></span> <span data-ttu-id="b1499-133">Utilisez **ID3DXPRTEngine :: ShadowRayIntersects** si l’emplacement du point d’intersection n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b1499-133">Use **ID3DXPRTEngine::ShadowRayIntersects** if the location of the intersection point is not needed.</span></span>

<span data-ttu-id="b1499-134">Les coordonnées Barycentric définissent un point à l’intérieur d’un triangle en termes de sommets du triangle.</span><span class="sxs-lookup"><span data-stu-id="b1499-134">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="b1499-135">Pour une description plus détaillée des coordonnées Barycentric, consultez [la description des coordonnées Barycentric de MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="b1499-135">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="b1499-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b1499-136">Requirements</span></span>



| <span data-ttu-id="b1499-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b1499-137">Requirement</span></span> | <span data-ttu-id="b1499-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1499-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1499-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="b1499-139">Header</span></span><br/>  | <dl> <span data-ttu-id="b1499-140"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1499-140"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b1499-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b1499-141">Library</span></span><br/> | <dl> <span data-ttu-id="b1499-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1499-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b1499-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1499-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1499-144">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="b1499-144">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="b1499-145">**ID3DXPRTEngine::ShadowRayIntersects**</span><span class="sxs-lookup"><span data-stu-id="b1499-145">**ID3DXPRTEngine::ShadowRayIntersects**</span></span>](id3dxprtengine--shadowrayintersects.md)
</dt> <dt>

[<span data-ttu-id="b1499-146">**ID3DXPRTEngine::SetMinMaxIntersection**</span><span class="sxs-lookup"><span data-stu-id="b1499-146">**ID3DXPRTEngine::SetMinMaxIntersection**</span></span>](id3dxprtengine--setminmaxintersection.md)
</dt> </dl>

 

 
