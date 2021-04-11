---
description: Croise le rayon spécifié avec le sous-ensemble de maillage donné. Cela offre des fonctionnalités similaires à D3DXIntersect.
ms.assetid: 4a757b9e-18eb-424e-9f3e-cdf917c23787
title: D3DXIntersectSubset, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIntersectSubset
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 621f45d7c2a6d8ff162f539ef62153d3ae70f6e9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211757"
---
# <a name="d3dxintersectsubset-function"></a><span data-ttu-id="6aabc-104">D3DXIntersectSubset fonction)</span><span class="sxs-lookup"><span data-stu-id="6aabc-104">D3DXIntersectSubset function</span></span>

<span data-ttu-id="6aabc-105">Croise le rayon spécifié avec le sous-ensemble de maillage donné.</span><span class="sxs-lookup"><span data-stu-id="6aabc-105">Intersects the specified ray with the given mesh subset.</span></span> <span data-ttu-id="6aabc-106">Cela offre des fonctionnalités similaires à [**D3DXIntersect**](d3dxintersect.md).</span><span class="sxs-lookup"><span data-stu-id="6aabc-106">This provides similar functionality to [**D3DXIntersect**](d3dxintersect.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6aabc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6aabc-107">Syntax</span></span>


```C++
HRESULT D3DXIntersectSubset(
  _In_        LPD3DXBASEMESH pMesh,
  _In_        DWORD          AttribId,
  _In_  const D3DXVECTOR3    *pRayPos,
  _In_  const D3DXVECTOR3    *pRayDir,
  _Out_       BOOL           *pHit,
  _Out_       DWORD          *pFaceIndex,
  _Out_       FLOAT          *pU,
  _Out_       FLOAT          *pV,
  _Out_       FLOAT          *pDist,
  _Out_       LPD3DXBUFFER   *ppAllHits,
  _Out_       DWORD          *pCountOfHits
);
```



## <a name="parameters"></a><span data-ttu-id="6aabc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6aabc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6aabc-109">*pMesh* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6aabc-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6aabc-110">Type : **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="6aabc-110">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="6aabc-111">Pointeur vers une interface [**ID3DXBaseMesh**](id3dxbasemesh.md) représentant le maillage à tester.</span><span class="sxs-lookup"><span data-stu-id="6aabc-111">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) interface, representing the mesh to be tested.</span></span> <span data-ttu-id="6aabc-112">La maille doit être triée par attribut.</span><span class="sxs-lookup"><span data-stu-id="6aabc-112">The mesh must be attribute sorted.</span></span>

</dd> <dt>

<span data-ttu-id="6aabc-113">*AttribId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6aabc-113">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6aabc-114">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6aabc-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6aabc-115">Identificateur d’attribut du sous-ensemble avec lequel effectuer l’intersection.</span><span class="sxs-lookup"><span data-stu-id="6aabc-115">Attribute identifier of the subset to intersect with.</span></span>

</dd> <dt>

<span data-ttu-id="6aabc-116">*pRayPos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6aabc-116">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6aabc-117">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="6aabc-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="6aabc-118">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , en spécifiant le point de départ du rayon.</span><span class="sxs-lookup"><span data-stu-id="6aabc-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="6aabc-119">*pRayDir* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6aabc-119">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6aabc-120">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="6aabc-120">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="6aabc-121">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , en spécifiant la direction du rayon.</span><span class="sxs-lookup"><span data-stu-id="6aabc-121">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="6aabc-122">*pHit* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6aabc-122">*pHit* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6aabc-123">Type : **[ **bool**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6aabc-123">Type: **[**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6aabc-124">Pointeur vers un booléen.</span><span class="sxs-lookup"><span data-stu-id="6aabc-124">Pointer to a BOOL.</span></span> <span data-ttu-id="6aabc-125">Si le rayon croise une face triangulaire sur le maillage, cette valeur est définie sur **true**.</span><span class="sxs-lookup"><span data-stu-id="6aabc-125">If the ray intersects a triangular face on the mesh, this value will be set to **TRUE**.</span></span> <span data-ttu-id="6aabc-126">Sinon, cette valeur est définie sur **false**.</span><span class="sxs-lookup"><span data-stu-id="6aabc-126">Otherwise, this value is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="6aabc-127">*pFaceIndex* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6aabc-127">*pFaceIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6aabc-128">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6aabc-128">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6aabc-129">Pointeur vers une valeur d’index du visage le plus proche de l’origine du rayon, si pHit a la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="6aabc-129">Pointer to an index value of the face closest to the ray origin, if pHit is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="6aabc-130">*pu* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6aabc-130">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6aabc-131">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6aabc-131">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6aabc-132">Pointeur vers une coordonnée d’accès Barycentric, U.</span><span class="sxs-lookup"><span data-stu-id="6aabc-132">Pointer to a barycentric hit coordinate, U.</span></span>

</dd> <dt>

<span data-ttu-id="6aabc-133">*PV* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6aabc-133">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6aabc-134">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6aabc-134">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6aabc-135">Pointeur vers une coordonnée d’accès Barycentric, V.</span><span class="sxs-lookup"><span data-stu-id="6aabc-135">Pointer to a barycentric hit coordinate, V.</span></span>

</dd> <dt>

<span data-ttu-id="6aabc-136">*pDist* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6aabc-136">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6aabc-137">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6aabc-137">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6aabc-138">Pointeur désignant une distance de paramètres d’intersection de rayon.</span><span class="sxs-lookup"><span data-stu-id="6aabc-138">Pointer to a ray intersection parameter distance.</span></span>

</dd> <dt>

<span data-ttu-id="6aabc-139">*ppAllHits* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6aabc-139">*ppAllHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6aabc-140">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="6aabc-140">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="6aabc-141">Tableau de structures [**D3DXINTERSECTINFO**](d3dxintersectinfo.md) , représentant tous les accès, pas seulement les correspondances les plus proches.</span><span class="sxs-lookup"><span data-stu-id="6aabc-141">Array of [**D3DXINTERSECTINFO**](d3dxintersectinfo.md) structures, representing all hits, not just closest hits.</span></span>

</dd> <dt>

<span data-ttu-id="6aabc-142">*pCountOfHits* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6aabc-142">*pCountOfHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6aabc-143">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6aabc-143">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6aabc-144">Nombre d’éléments dans le tableau retourné par ppAllHits.</span><span class="sxs-lookup"><span data-stu-id="6aabc-144">Number of elements in the array returned from ppAllHits.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6aabc-145">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6aabc-145">Return value</span></span>

<span data-ttu-id="6aabc-146">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6aabc-146">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6aabc-147">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6aabc-147">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6aabc-148">Si la fonction échoue, la valeur de retour peut être la valeur suivante : E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="6aabc-148">If the function fails, the return value can be the following value: E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="6aabc-149">Notes</span><span class="sxs-lookup"><span data-stu-id="6aabc-149">Remarks</span></span>

<span data-ttu-id="6aabc-150">La fonction **D3DXIntersectSubset** fournit un moyen de comprendre les points dans et autour d’un triangle, indépendamment de l’endroit où le triangle est réellement situé.</span><span class="sxs-lookup"><span data-stu-id="6aabc-150">The **D3DXIntersectSubset** function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="6aabc-151">Cette fonction retourne le point résultant à l’aide de l’équation suivante : v1 + U (V2-V1) + V (v3-v1).</span><span class="sxs-lookup"><span data-stu-id="6aabc-151">This function returns the resulting point by using the following equation: V1 + U(V2 - V1) + V(V3 - V1).</span></span>

<span data-ttu-id="6aabc-152">Tout point dans le plan V1V2V3 peut être représenté par la coordonnée Barycentric (U, V).</span><span class="sxs-lookup"><span data-stu-id="6aabc-152">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="6aabc-153">Le paramètre U contrôle combien v2 est pondéré dans le résultat et le paramètre V contrôle combien v3 est pondéré dans le résultat.</span><span class="sxs-lookup"><span data-stu-id="6aabc-153">The parameter U controls how much V2 gets weighted into the result and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="6aabc-154">Enfin, la valeur de \[ 1-(U + V) \] contrôle la quantité de valeurs v1 pondérée dans le résultat.</span><span class="sxs-lookup"><span data-stu-id="6aabc-154">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="6aabc-155">Les coordonnées Barycentric sont une forme de coordonnées générales.</span><span class="sxs-lookup"><span data-stu-id="6aabc-155">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="6aabc-156">Dans ce contexte, l’utilisation de coordonnées Barycentric représente une modification des systèmes de coordonnées.</span><span class="sxs-lookup"><span data-stu-id="6aabc-156">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="6aabc-157">Ce qui est vrai pour les coordonnées cartésiennes contient la valeur true pour les coordonnées Barycentric.</span><span class="sxs-lookup"><span data-stu-id="6aabc-157">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="6aabc-158">Les coordonnées Barycentric définissent un point à l’intérieur d’un triangle en termes de sommets du triangle.</span><span class="sxs-lookup"><span data-stu-id="6aabc-158">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="6aabc-159">Pour une description plus détaillée des coordonnées Barycentric, consultez [la description des coordonnées Barycentric de MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="6aabc-159">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="6aabc-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6aabc-160">Requirements</span></span>



| <span data-ttu-id="6aabc-161">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6aabc-161">Requirement</span></span> | <span data-ttu-id="6aabc-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="6aabc-162">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6aabc-163">En-tête</span><span class="sxs-lookup"><span data-stu-id="6aabc-163">Header</span></span><br/>  | <dl> <span data-ttu-id="6aabc-164"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="6aabc-164"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6aabc-165">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6aabc-165">Library</span></span><br/> | <dl> <span data-ttu-id="6aabc-166"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6aabc-166"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6aabc-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6aabc-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6aabc-168">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="6aabc-168">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
