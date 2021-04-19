---
description: Détermine si un rayon croise ce maillage.
ms.assetid: 74565d4a-94e6-4faa-bf70-9c1b35e5e5d8
title: ID3DX10Mesh::Intersect, méthode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Intersect
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8ceed03ab21debf61371da9e53b5150d2dc83e4a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106543563"
---
# <a name="id3dx10meshintersect-method"></a><span data-ttu-id="3724f-103">ID3DX10Mesh :: Intersect, méthode</span><span class="sxs-lookup"><span data-stu-id="3724f-103">ID3DX10Mesh::Intersect method</span></span>

<span data-ttu-id="3724f-104">Détermine si un rayon croise ce maillage.</span><span class="sxs-lookup"><span data-stu-id="3724f-104">Determines if a ray intersects with this mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="3724f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3724f-105">Syntax</span></span>


```C++
HRESULT Intersect(
  [in]  D3DXVECTOR3 *pRayPos,
  [in]  D3DXVECTOR3 *pRayDir,
  [in]  UINT        *pHitCount,
  [in]  UINT        *pFaceIndex,
  [in]  float       *pU,
  [in]  float       *pV,
  [in]  float       *pDist,
  [out] ID3D10Blob  **ppAllHits
);
```



## <a name="parameters"></a><span data-ttu-id="3724f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3724f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3724f-107">*pRayPos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3724f-107">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3724f-108">Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="3724f-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="3724f-109">Pointeur vers une structure [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , en spécifiant le point de départ du rayon.</span><span class="sxs-lookup"><span data-stu-id="3724f-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="3724f-110">*pRayDir* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3724f-110">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3724f-111">Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="3724f-111">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="3724f-112">Pointeur vers une structure [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , en spécifiant la direction du rayon.</span><span class="sxs-lookup"><span data-stu-id="3724f-112">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="3724f-113">*pHitCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3724f-113">*pHitCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3724f-114">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3724f-114">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3724f-115">Nombre de fois que le rayon est croisé avec la maille.</span><span class="sxs-lookup"><span data-stu-id="3724f-115">The number of times the ray intersected with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="3724f-116">*pFaceIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3724f-116">*pFaceIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3724f-117">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3724f-117">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3724f-118">Pointeur vers une valeur d’index du visage le plus proche de l’origine du rayon, si pHit a la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="3724f-118">Pointer to an index value of the face closest to the ray origin, if pHit is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="3724f-119">*pu* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3724f-119">*pU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3724f-120">Type : **float \***</span><span class="sxs-lookup"><span data-stu-id="3724f-120">Type: **float\***</span></span>

<span data-ttu-id="3724f-121">Pointeur vers une coordonnée d’accès Barycentric, U.</span><span class="sxs-lookup"><span data-stu-id="3724f-121">Pointer to a barycentric hit coordinate, U.</span></span>

</dd> <dt>

<span data-ttu-id="3724f-122">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3724f-122">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3724f-123">Type : **float \***</span><span class="sxs-lookup"><span data-stu-id="3724f-123">Type: **float\***</span></span>

<span data-ttu-id="3724f-124">Pointeur vers une coordonnée d’accès Barycentric, V.</span><span class="sxs-lookup"><span data-stu-id="3724f-124">Pointer to a barycentric hit coordinate, V.</span></span>

</dd> <dt>

<span data-ttu-id="3724f-125">*pDist* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3724f-125">*pDist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3724f-126">Type : **float \***</span><span class="sxs-lookup"><span data-stu-id="3724f-126">Type: **float\***</span></span>

<span data-ttu-id="3724f-127">Pointeur désignant une distance de paramètres d’intersection de rayon.</span><span class="sxs-lookup"><span data-stu-id="3724f-127">Pointer to a ray intersection parameter distance.</span></span>

</dd> <dt>

<span data-ttu-id="3724f-128">*ppAllHits* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3724f-128">*ppAllHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3724f-129">Type : **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="3724f-129">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="3724f-130">Pointeur vers une [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob), contenant un tableau de structures d' [**\_ \_ informations d’intersection d3dx10**](d3dx10-intersect-info.md) .</span><span class="sxs-lookup"><span data-stu-id="3724f-130">Pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob), containing an array of [**D3DX10\_INTERSECT\_INFO**](d3dx10-intersect-info.md) structures.</span></span> <span data-ttu-id="3724f-131">Il s’agit d’une liste de tous les accès qui se sont produits dans le test d’intersection.</span><span class="sxs-lookup"><span data-stu-id="3724f-131">This is a list of all the hits that occurred in the intersection test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3724f-132">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3724f-132">Return value</span></span>

<span data-ttu-id="3724f-133">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3724f-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3724f-134">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="3724f-134">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3724f-135">Notes</span><span class="sxs-lookup"><span data-stu-id="3724f-135">Remarks</span></span>

<span data-ttu-id="3724f-136">Cette API fournit un moyen de comprendre les points dans et autour d’un triangle, indépendamment de l’endroit où le triangle est réellement situé.</span><span class="sxs-lookup"><span data-stu-id="3724f-136">This API provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="3724f-137">Cette fonction retourne le point résultant à l’aide de l’équation suivante : v1 + U (V2-V1) + V (v3-v1).</span><span class="sxs-lookup"><span data-stu-id="3724f-137">This function returns the resulting point by using the following equation: V1 + U(V2 - V1) + V(V3 - V1).</span></span>

<span data-ttu-id="3724f-138">Tout point dans le plan V1V2V3 peut être représenté par la coordonnée Barycentric (U, V).</span><span class="sxs-lookup"><span data-stu-id="3724f-138">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="3724f-139">Le paramètre U contrôle combien v2 est pondéré dans le résultat, et le paramètre V contrôle combien v3 est pondéré dans le résultat.</span><span class="sxs-lookup"><span data-stu-id="3724f-139">The parameter U controls how much V2 gets weighted into the result, and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="3724f-140">Enfin, la valeur de \[ 1-(U + V) \] contrôle la quantité de valeurs v1 pondérée dans le résultat.</span><span class="sxs-lookup"><span data-stu-id="3724f-140">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="3724f-141">Les coordonnées Barycentric sont une forme de coordonnées générales.</span><span class="sxs-lookup"><span data-stu-id="3724f-141">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="3724f-142">Dans ce contexte, l’utilisation de coordonnées Barycentric représente une modification des systèmes de coordonnées.</span><span class="sxs-lookup"><span data-stu-id="3724f-142">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="3724f-143">Ce qui est vrai pour les coordonnées cartésiennes contient la valeur true pour les coordonnées Barycentric.</span><span class="sxs-lookup"><span data-stu-id="3724f-143">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="3724f-144">Les coordonnées Barycentric définissent un point à l’intérieur d’un triangle en termes de sommets du triangle.</span><span class="sxs-lookup"><span data-stu-id="3724f-144">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="3724f-145">Pour une description plus détaillée des coordonnées Barycentric, consultez [la description des coordonnées Barycentric de MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="3724f-145">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="3724f-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3724f-146">Requirements</span></span>



| <span data-ttu-id="3724f-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3724f-147">Requirement</span></span> | <span data-ttu-id="3724f-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="3724f-148">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3724f-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="3724f-149">Header</span></span><br/>  | <dl> <span data-ttu-id="3724f-150"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="3724f-150"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="3724f-151">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3724f-151">Library</span></span><br/> | <dl> <span data-ttu-id="3724f-152"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3724f-152"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3724f-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3724f-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3724f-154">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="3724f-154">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="3724f-155">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="3724f-155">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
