---
description: Détermine si un rayon croise une maille.
ms.assetid: 325f5b40-80ba-4400-a143-bae41146ab07
title: D3DXIntersect, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIntersect
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc877fb1301e01b05184625ba2e92a2c680cfa9f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106545279"
---
# <a name="d3dxintersect-function"></a><span data-ttu-id="5a75e-103">D3DXIntersect fonction)</span><span class="sxs-lookup"><span data-stu-id="5a75e-103">D3DXIntersect function</span></span>

<span data-ttu-id="5a75e-104">Détermine si un rayon croise une maille.</span><span class="sxs-lookup"><span data-stu-id="5a75e-104">Determines if a ray intersects with a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a75e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5a75e-105">Syntax</span></span>


```C++
HRESULT D3DXIntersect(
  _In_        LPD3DXBASEMESH pMesh,
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



## <a name="parameters"></a><span data-ttu-id="5a75e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5a75e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a75e-107">*pMesh* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5a75e-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a75e-108">Type : **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="5a75e-108">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="5a75e-109">Pointeur vers une interface [**ID3DXBaseMesh**](id3dxbasemesh.md) représentant le maillage à tester.</span><span class="sxs-lookup"><span data-stu-id="5a75e-109">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) interface, representing the mesh to be tested.</span></span>

</dd> <dt>

<span data-ttu-id="5a75e-110">*pRayPos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5a75e-110">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a75e-111">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="5a75e-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="5a75e-112">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , en spécifiant le point de départ du rayon.</span><span class="sxs-lookup"><span data-stu-id="5a75e-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="5a75e-113">*pRayDir* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5a75e-113">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a75e-114">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="5a75e-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="5a75e-115">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , en spécifiant la direction du rayon.</span><span class="sxs-lookup"><span data-stu-id="5a75e-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="5a75e-116">*pHit* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5a75e-116">*pHit* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a75e-117">Type : **[ **bool**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a75e-117">Type: **[**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5a75e-118">Pointeur vers un booléen.</span><span class="sxs-lookup"><span data-stu-id="5a75e-118">Pointer to a BOOL.</span></span> <span data-ttu-id="5a75e-119">Si le rayon croise une face triangulaire sur le maillage, cette valeur est définie sur **true**.</span><span class="sxs-lookup"><span data-stu-id="5a75e-119">If the ray intersects a triangular face on the mesh, this value will be set to **TRUE**.</span></span> <span data-ttu-id="5a75e-120">Sinon, cette valeur est définie sur **false**.</span><span class="sxs-lookup"><span data-stu-id="5a75e-120">Otherwise, this value is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="5a75e-121">*pFaceIndex* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5a75e-121">*pFaceIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a75e-122">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a75e-122">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5a75e-123">Pointeur vers une valeur d’index du visage le plus proche de l’origine du rayon, si pHit a la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="5a75e-123">Pointer to an index value of the face closest to the ray origin, if pHit is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="5a75e-124">*pu* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5a75e-124">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a75e-125">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a75e-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5a75e-126">Pointeur vers une coordonnée d’accès Barycentric, U.</span><span class="sxs-lookup"><span data-stu-id="5a75e-126">Pointer to a barycentric hit coordinate, U.</span></span>

</dd> <dt>

<span data-ttu-id="5a75e-127">*PV* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5a75e-127">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a75e-128">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a75e-128">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5a75e-129">Pointeur vers une coordonnée d’accès Barycentric, V.</span><span class="sxs-lookup"><span data-stu-id="5a75e-129">Pointer to a barycentric hit coordinate, V.</span></span>

</dd> <dt>

<span data-ttu-id="5a75e-130">*pDist* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5a75e-130">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a75e-131">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a75e-131">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5a75e-132">Pointeur désignant une distance de paramètres d’intersection de rayon.</span><span class="sxs-lookup"><span data-stu-id="5a75e-132">Pointer to a ray intersection parameter distance.</span></span>

</dd> <dt>

<span data-ttu-id="5a75e-133">*ppAllHits* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5a75e-133">*ppAllHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a75e-134">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a75e-134">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="5a75e-135">Pointeur vers un objet [**ID3DXBuffer**](id3dxbuffer.md) , contenant un tableau de structures [**D3DXINTERSECTINFO**](d3dxintersectinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="5a75e-135">Pointer to an [**ID3DXBuffer**](id3dxbuffer.md) object, containing an array of [**D3DXINTERSECTINFO**](d3dxintersectinfo.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="5a75e-136">*pCountOfHits* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5a75e-136">*pCountOfHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a75e-137">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a75e-137">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5a75e-138">Pointeur vers une valeur DWORD qui contient le nombre d’entrées dans le tableau ppAllHits.</span><span class="sxs-lookup"><span data-stu-id="5a75e-138">Pointer to a DWORD that contains the number of entries in the ppAllHits array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a75e-139">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5a75e-139">Return value</span></span>

<span data-ttu-id="5a75e-140">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5a75e-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5a75e-141">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5a75e-141">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5a75e-142">Si la fonction échoue, la valeur de retour peut être : E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="5a75e-142">If the function fails, the return value can be: E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a75e-143">Notes</span><span class="sxs-lookup"><span data-stu-id="5a75e-143">Remarks</span></span>

<span data-ttu-id="5a75e-144">La fonction **D3DXIntersect** fournit un moyen de comprendre les points dans et autour d’un triangle, indépendamment de l’endroit où le triangle est réellement situé.</span><span class="sxs-lookup"><span data-stu-id="5a75e-144">The **D3DXIntersect** function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="5a75e-145">Cette fonction retourne le point résultant à l’aide de l’équation suivante : v1 + U (V2-V1) + V (v3-v1).</span><span class="sxs-lookup"><span data-stu-id="5a75e-145">This function returns the resulting point by using the following equation: V1 + U(V2 - V1) + V(V3 - V1).</span></span>

<span data-ttu-id="5a75e-146">Tout point dans le plan V1V2V3 peut être représenté par la coordonnée Barycentric (U, V).</span><span class="sxs-lookup"><span data-stu-id="5a75e-146">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="5a75e-147">Le paramètre U contrôle combien v2 est pondéré dans le résultat, et le paramètre V contrôle combien v3 est pondéré dans le résultat.</span><span class="sxs-lookup"><span data-stu-id="5a75e-147">The parameter U controls how much V2 gets weighted into the result, and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="5a75e-148">Enfin, la valeur de \[ 1-(U + V) \] contrôle la quantité de valeurs v1 pondérée dans le résultat.</span><span class="sxs-lookup"><span data-stu-id="5a75e-148">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="5a75e-149">Les coordonnées Barycentric sont une forme de coordonnées générales.</span><span class="sxs-lookup"><span data-stu-id="5a75e-149">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="5a75e-150">Dans ce contexte, l’utilisation de coordonnées Barycentric représente une modification des systèmes de coordonnées.</span><span class="sxs-lookup"><span data-stu-id="5a75e-150">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="5a75e-151">Ce qui est vrai pour les coordonnées cartésiennes contient la valeur true pour les coordonnées Barycentric.</span><span class="sxs-lookup"><span data-stu-id="5a75e-151">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="5a75e-152">Les coordonnées Barycentric définissent un point à l’intérieur d’un triangle en termes de sommets du triangle.</span><span class="sxs-lookup"><span data-stu-id="5a75e-152">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="5a75e-153">Pour une description plus détaillée des coordonnées Barycentric, consultez [la description des coordonnées Barycentric de MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="5a75e-153">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a75e-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a75e-154">Requirements</span></span>



| <span data-ttu-id="5a75e-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a75e-155">Requirement</span></span> | <span data-ttu-id="5a75e-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a75e-156">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a75e-157">En-tête</span><span class="sxs-lookup"><span data-stu-id="5a75e-157">Header</span></span><br/>  | <dl> <span data-ttu-id="5a75e-158"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a75e-158"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="5a75e-159">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5a75e-159">Library</span></span><br/> | <dl> <span data-ttu-id="5a75e-160"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a75e-160"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5a75e-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a75e-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a75e-162">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="5a75e-162">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
