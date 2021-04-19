---
description: Vecteurs de calcul tangent, Binormal et normal pour une maille.
ms.assetid: 54edb9a5-440d-4191-a58f-296e5b804e0c
title: D3DXComputeTangentFrame, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangentFrame
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4b95d8f046499716a2c7972593093dfb409b11f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538064"
---
# <a name="d3dxcomputetangentframe-function"></a><span data-ttu-id="256bd-103">D3DXComputeTangentFrame fonction)</span><span class="sxs-lookup"><span data-stu-id="256bd-103">D3DXComputeTangentFrame function</span></span>

<span data-ttu-id="256bd-104">Vecteurs de calcul tangent, Binormal et normal pour une maille.</span><span class="sxs-lookup"><span data-stu-id="256bd-104">Compute tangent, binormal, and normal vectors for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="256bd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="256bd-105">Syntax</span></span>


```C++
HRESULT D3DXComputeTangentFrame(
  _In_ ID3DXMesh *pMesh,
  _In_ DWORD     dwOptions
);
```



## <a name="parameters"></a><span data-ttu-id="256bd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="256bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="256bd-107">*pMesh* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="256bd-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="256bd-108">Type : **[ **ID3DXMesh**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="256bd-108">Type: **[**ID3DXMesh**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="256bd-109">Pointeur vers un objet de maillage [**ID3DXMesh**](id3dxmesh.md) d’entrée.</span><span class="sxs-lookup"><span data-stu-id="256bd-109">Pointer to an input [**ID3DXMesh**](id3dxmesh.md) mesh object.</span></span>

</dd> <dt>

<span data-ttu-id="256bd-110">*dwOptions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="256bd-110">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="256bd-111">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="256bd-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="256bd-112">Combinaison d’un ou plusieurs indicateurs [**D3DXTANGENT**](./d3dxtangent.md) .</span><span class="sxs-lookup"><span data-stu-id="256bd-112">Combination of one or more [**D3DXTANGENT**](./d3dxtangent.md) flags.</span></span>

<span data-ttu-id="256bd-113">Utilisez la **valeur null** pour spécifier les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="256bd-113">Use **NULL** to specify the following options:</span></span>

-   <span data-ttu-id="256bd-114">Pondérez la longueur du vecteur normal par l’angle, en radians, sous-tendus par les deux bords quittant le sommet.</span><span class="sxs-lookup"><span data-stu-id="256bd-114">Weight the normal vector length by the angle, in radians, subtended by the two edges leaving the vertex.</span></span>
-   <span data-ttu-id="256bd-115">Calculez les coordonnées Cartésienles orthogonales à partir des coordonnées de texture UV.</span><span class="sxs-lookup"><span data-stu-id="256bd-115">Compute orthogonal Cartesian coordinates from the UV texture coordinates.</span></span>
-   <span data-ttu-id="256bd-116">Les textures ne sont pas encapsulées dans les directions U ou V</span><span class="sxs-lookup"><span data-stu-id="256bd-116">Textures are not wrapped in either U or V directions</span></span>
-   <span data-ttu-id="256bd-117">Les dérivés partiels en ce qui concerne les coordonnées de texture sont normalisés.</span><span class="sxs-lookup"><span data-stu-id="256bd-117">Partial derivatives with respect to texture coordinates are normalized.</span></span>
-   <span data-ttu-id="256bd-118">Les vertex sont triés dans le sens inverse des aiguilles d’une passe autour de chaque triangle.</span><span class="sxs-lookup"><span data-stu-id="256bd-118">Vertices are ordered in a counterclockwise direction around each triangle.</span></span>
-   <span data-ttu-id="256bd-119">Utilisez des vecteurs normaux par vertex déjà présents dans le maillage d’entrée.</span><span class="sxs-lookup"><span data-stu-id="256bd-119">Use per-vertex normal vectors already present in the input mesh.</span></span>
-   <span data-ttu-id="256bd-120">Les résultats seront stockés dans le maillage d’entrée d’origine.</span><span class="sxs-lookup"><span data-stu-id="256bd-120">The results will be stored in the original input mesh.</span></span> <span data-ttu-id="256bd-121">La fonction échoue si de nouveaux vertex doivent être créés.</span><span class="sxs-lookup"><span data-stu-id="256bd-121">The function will fail if new vertices need to be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="256bd-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="256bd-122">Return value</span></span>

<span data-ttu-id="256bd-123">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="256bd-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="256bd-124">Si la fonction est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="256bd-124">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="256bd-125">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="256bd-125">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="256bd-126">Notes</span><span class="sxs-lookup"><span data-stu-id="256bd-126">Remarks</span></span>

<span data-ttu-id="256bd-127">Cette fonction appelle simplement [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) avec les paramètres d’entrée suivants :</span><span class="sxs-lookup"><span data-stu-id="256bd-127">This function simply calls [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) with the following input parameters:</span></span>


```
D3DXComputeTangentFrameEx(pMesh, D3DDECLUSAGE_TEXCOORD, 0,   
      D3DDECLUSAGE_BINORMAL, 0, D3DDECLUSAGE_TANGENT, 0, 
      D3DDECLUSAGE_NORMAL, 0, 
      dwOptions | D3DXTANGENT_GENERATE_IN_PLACE,
      NULL, 0.01f, 0.25f, 0.01f, NULL, NULL);
```



<span data-ttu-id="256bd-128">Les singularités sont gérées en fonction des besoins en regroupant les bords et en fractionnant les vertex.</span><span class="sxs-lookup"><span data-stu-id="256bd-128">Singularities are handled as required by grouping edges and splitting vertices.</span></span> <span data-ttu-id="256bd-129">Si des vertex doivent être fractionnés, la fonction échoue.</span><span class="sxs-lookup"><span data-stu-id="256bd-129">If any vertices need to be split, the function will fail.</span></span> <span data-ttu-id="256bd-130">Le vecteur normal calculé à chaque vertex est toujours normalisé pour avoir une longueur d’unité.</span><span class="sxs-lookup"><span data-stu-id="256bd-130">The computed normal vector at each vertex is always normalized to have unit length.</span></span>

<span data-ttu-id="256bd-131">La solution la plus robuste pour calculer les coordonnées Cartésienles orthogonales consiste à ne pas définir les indicateurs D3DXTANGENT \_ \_ de manière orthogonale à partir de \_ vous et D3DXTANGENT \_ à orthogonaliser \_ à partir de \_ V, afin que les coordonnées orthogonales soient calculées à partir des coordonnées de la texture UV.</span><span class="sxs-lookup"><span data-stu-id="256bd-131">The most robust solution for computing orthogonal Cartesian coordinates is to not set flags D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U and D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V, so that orthogonal coordinates are computed from both UV texture coordinates.</span></span> <span data-ttu-id="256bd-132">Toutefois, dans ce cas, si U ou V est égal à zéro, la fonction calcule les coordonnées orthogonales à l’aide \_ de D3DXTANGENT orthogonale \_ à partir de \_ V ou \_ de D3DXTANGENT orthogonale \_ à partir de \_ U, respectivement.</span><span class="sxs-lookup"><span data-stu-id="256bd-132">However, in this case, if either U or V is zero, then the function will compute orthogonal coordinates using D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V or D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="256bd-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="256bd-133">Requirements</span></span>



| <span data-ttu-id="256bd-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="256bd-134">Requirement</span></span> | <span data-ttu-id="256bd-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="256bd-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="256bd-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="256bd-136">Header</span></span><br/>  | <dl> <span data-ttu-id="256bd-137"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="256bd-137"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="256bd-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="256bd-138">Library</span></span><br/> | <dl> <span data-ttu-id="256bd-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="256bd-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="256bd-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="256bd-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="256bd-141">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="256bd-141">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="256bd-142">**D3DXComputeTangentFrameEx**</span><span class="sxs-lookup"><span data-stu-id="256bd-142">**D3DXComputeTangentFrameEx**</span></span>](d3dxcomputetangentframeex.md)
</dt> <dt>

[<span data-ttu-id="256bd-143">**D3DXTANGENT**</span><span class="sxs-lookup"><span data-stu-id="256bd-143">**D3DXTANGENT**</span></span>](./d3dxtangent.md)
</dt> </dl>

 

 
