---
description: Détermine si un rayon entre en intersection avec un sous-ensemble de ce maillage.
ms.assetid: 31f90141-60be-4c7f-8d6a-a1a97ff26d9d
title: ID3DX10Mesh::IntersectSubset, méthode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.IntersectSubset
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a08d4db92dc75f40d0073367dda9a9ea26863418
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211861"
---
# <a name="id3dx10meshintersectsubset-method"></a><span data-ttu-id="2f950-103">ID3DX10Mesh :: IntersectSubset, méthode</span><span class="sxs-lookup"><span data-stu-id="2f950-103">ID3DX10Mesh::IntersectSubset method</span></span>

<span data-ttu-id="2f950-104">Détermine si un rayon entre en intersection avec un sous-ensemble de ce maillage.</span><span class="sxs-lookup"><span data-stu-id="2f950-104">Determines if a ray intersects with a subset of this mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f950-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2f950-105">Syntax</span></span>


```C++
HRESULT IntersectSubset(
  [in]  UINT        AttribId,
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



## <a name="parameters"></a><span data-ttu-id="2f950-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2f950-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f950-107">*AttribId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2f950-107">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f950-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f950-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f950-109">ID d’attribut identifiant le sous-ensemble du maillage.</span><span class="sxs-lookup"><span data-stu-id="2f950-109">Attribute ID identifying the subset of the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="2f950-110">*pRayPos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2f950-110">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f950-111">Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="2f950-111">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="2f950-112">Pointeur vers une structure [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , en spécifiant le point de départ du rayon.</span><span class="sxs-lookup"><span data-stu-id="2f950-112">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="2f950-113">*pRayDir* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2f950-113">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f950-114">Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="2f950-114">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="2f950-115">Pointeur vers une structure [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , en spécifiant la direction du rayon.</span><span class="sxs-lookup"><span data-stu-id="2f950-115">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="2f950-116">*pHitCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2f950-116">*pHitCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f950-117">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2f950-117">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2f950-118">Nombre de fois que le rayon est croisé avec la maille.</span><span class="sxs-lookup"><span data-stu-id="2f950-118">The number of times the ray intersected with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="2f950-119">*pFaceIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2f950-119">*pFaceIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f950-120">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2f950-120">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2f950-121">Pointeur vers une valeur d’index du visage le plus proche de l’origine du rayon, si pHit a la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="2f950-121">Pointer to an index value of the face closest to the ray origin, if pHit is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="2f950-122">*pu* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2f950-122">*pU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f950-123">Type : **float \***</span><span class="sxs-lookup"><span data-stu-id="2f950-123">Type: **float\***</span></span>

<span data-ttu-id="2f950-124">Pointeur vers une coordonnée d’accès Barycentric, U.</span><span class="sxs-lookup"><span data-stu-id="2f950-124">Pointer to a barycentric hit coordinate, U.</span></span>

</dd> <dt>

<span data-ttu-id="2f950-125">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2f950-125">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f950-126">Type : **float \***</span><span class="sxs-lookup"><span data-stu-id="2f950-126">Type: **float\***</span></span>

<span data-ttu-id="2f950-127">Pointeur vers une coordonnée d’accès Barycentric, V.</span><span class="sxs-lookup"><span data-stu-id="2f950-127">Pointer to a barycentric hit coordinate, V.</span></span>

</dd> <dt>

<span data-ttu-id="2f950-128">*pDist* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2f950-128">*pDist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f950-129">Type : **float \***</span><span class="sxs-lookup"><span data-stu-id="2f950-129">Type: **float\***</span></span>

<span data-ttu-id="2f950-130">Pointeur désignant une distance de paramètres d’intersection de rayon.</span><span class="sxs-lookup"><span data-stu-id="2f950-130">Pointer to a ray intersection parameter distance.</span></span>

</dd> <dt>

<span data-ttu-id="2f950-131">*ppAllHits* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2f950-131">*ppAllHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f950-132">Type : **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="2f950-132">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="2f950-133">Pointeur vers une [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob), contenant un tableau de structures d' [**\_ \_ informations d’intersection d3dx10**](d3dx10-intersect-info.md) .</span><span class="sxs-lookup"><span data-stu-id="2f950-133">Pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob), containing an array of [**D3DX10\_INTERSECT\_INFO**](d3dx10-intersect-info.md) structures.</span></span> <span data-ttu-id="2f950-134">Il s’agit d’une liste de tous les accès qui se sont produits dans le test d’intersection.</span><span class="sxs-lookup"><span data-stu-id="2f950-134">This is a list of all the hits that occurred in the intersection test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f950-135">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2f950-135">Return value</span></span>

<span data-ttu-id="2f950-136">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2f950-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2f950-137">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="2f950-137">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2f950-138">Notes</span><span class="sxs-lookup"><span data-stu-id="2f950-138">Remarks</span></span>

<span data-ttu-id="2f950-139">Cette API fournit un moyen de comprendre les points dans et autour d’un triangle, indépendamment de l’endroit où le triangle est réellement situé.</span><span class="sxs-lookup"><span data-stu-id="2f950-139">This API provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="2f950-140">Cette fonction retourne le point résultant à l’aide de l’équation suivante : v1 + U (V2-V1) + V (v3-v1).</span><span class="sxs-lookup"><span data-stu-id="2f950-140">This function returns the resulting point by using the following equation: V1 + U(V2 - V1) + V(V3 - V1).</span></span>

<span data-ttu-id="2f950-141">Tout point dans le plan V1V2V3 peut être représenté par la coordonnée Barycentric (U, V).</span><span class="sxs-lookup"><span data-stu-id="2f950-141">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="2f950-142">Le paramètre U contrôle combien v2 est pondéré dans le résultat, et le paramètre V contrôle combien v3 est pondéré dans le résultat.</span><span class="sxs-lookup"><span data-stu-id="2f950-142">The parameter U controls how much V2 gets weighted into the result, and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="2f950-143">Enfin, la valeur de \[ 1-(U + V) \] contrôle la quantité de valeurs v1 pondérée dans le résultat.</span><span class="sxs-lookup"><span data-stu-id="2f950-143">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="2f950-144">Les coordonnées Barycentric sont une forme de coordonnées générales.</span><span class="sxs-lookup"><span data-stu-id="2f950-144">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="2f950-145">Dans ce contexte, l’utilisation de coordonnées Barycentric représente une modification des systèmes de coordonnées.</span><span class="sxs-lookup"><span data-stu-id="2f950-145">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="2f950-146">Ce qui est vrai pour les coordonnées cartésiennes contient la valeur true pour les coordonnées Barycentric.</span><span class="sxs-lookup"><span data-stu-id="2f950-146">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="2f950-147">Les coordonnées Barycentric définissent un point à l’intérieur d’un triangle en termes de sommets du triangle.</span><span class="sxs-lookup"><span data-stu-id="2f950-147">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="2f950-148">Pour une description plus détaillée des coordonnées Barycentric, consultez [la description des coordonnées Barycentric de MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="2f950-148">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="2f950-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f950-149">Requirements</span></span>



| <span data-ttu-id="2f950-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f950-150">Requirement</span></span> | <span data-ttu-id="2f950-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f950-151">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2f950-152">En-tête</span><span class="sxs-lookup"><span data-stu-id="2f950-152">Header</span></span><br/>  | <dl> <span data-ttu-id="2f950-153"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f950-153"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="2f950-154">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2f950-154">Library</span></span><br/> | <dl> <span data-ttu-id="2f950-155"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f950-155"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f950-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f950-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f950-157">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="2f950-157">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="2f950-158">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="2f950-158">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
