---
description: Récupère les coordonnées Barycentric texels.
ms.assetid: f380a37f-b9c1-4433-b1d6-e9feeca79b30
title: 'ID3DXTextureGutterHelper :: GetBaryMap, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetBaryMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 246117569b9106de18a31d08613146a3aa0d88c2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523839"
---
# <a name="id3dxtexturegutterhelpergetbarymap-method"></a><span data-ttu-id="eff2c-103">ID3DXTextureGutterHelper :: GetBaryMap, méthode</span><span class="sxs-lookup"><span data-stu-id="eff2c-103">ID3DXTextureGutterHelper::GetBaryMap method</span></span>

<span data-ttu-id="eff2c-104">Récupère les coordonnées Barycentric texels.</span><span class="sxs-lookup"><span data-stu-id="eff2c-104">Retrieves texel barycentric coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="eff2c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eff2c-105">Syntax</span></span>


```C++
HRESULT GetBaryMap(
  [in, out] D3DXVECTOR2 *pBaryData
);
```



## <a name="parameters"></a><span data-ttu-id="eff2c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eff2c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eff2c-107">*pBaryData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="eff2c-107">*pBaryData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="eff2c-108">Type : **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="eff2c-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="eff2c-109">Pointeur vers une structure [**D3DXVECTOR2**](d3dxvector2.md) qui contient les deux premières coordonnées Barycentric de chaque Texel.</span><span class="sxs-lookup"><span data-stu-id="eff2c-109">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that contains the first two barycentric coordinates of each texel.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eff2c-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eff2c-110">Return value</span></span>

<span data-ttu-id="eff2c-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="eff2c-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="eff2c-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="eff2c-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="eff2c-113">Si la méthode échoue, la valeur suivante est retournée. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="eff2c-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="eff2c-114">Notes</span><span class="sxs-lookup"><span data-stu-id="eff2c-114">Remarks</span></span>

<span data-ttu-id="eff2c-115">La troisième coordonnée Barycentric est donnée par :</span><span class="sxs-lookup"><span data-stu-id="eff2c-115">The third barycentric coordinate is given by:</span></span>


```
    1 - ( pBaryData.x + pBaryData.y )
```



<span data-ttu-id="eff2c-116">Les coordonnées Barycentric sont toujours spécifiées en ce qui concerne le triangle retourné par [**ID3DXTextureGutterHelper :: GetFaceMap**](id3dxtexturegutterhelper--getfacemap.md).</span><span class="sxs-lookup"><span data-stu-id="eff2c-116">Barycentric coordinates are always specified with respect to the triangle returned by [**ID3DXTextureGutterHelper::GetFaceMap**](id3dxtexturegutterhelper--getfacemap.md).</span></span>

<span data-ttu-id="eff2c-117">Les coordonnées Barycentric retournées par cette méthode sont valides uniquement pour les texels valides (non de classe 0).</span><span class="sxs-lookup"><span data-stu-id="eff2c-117">The barycentric coordinates returned by this method are valid only for valid (non-class 0) texels.</span></span> <span data-ttu-id="eff2c-118">[**ID3DXTextureGutterHelper :: GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) retourne des valeurs non nulles pour les texels valides.</span><span class="sxs-lookup"><span data-stu-id="eff2c-118">[**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) will return nonzero values for valid texels.</span></span>

<span data-ttu-id="eff2c-119">Les [**texels de classe 2**](id3dxtexturegutterhelper.md) sont mappés au point le plus proche sur le triangle dans l’espace Texel.</span><span class="sxs-lookup"><span data-stu-id="eff2c-119">[**Class 2 texels**](id3dxtexturegutterhelper.md) are mapped to the nearest point on the triangle in texel space.</span></span>

<span data-ttu-id="eff2c-120">L’application doit allouer et gérer pBaryData.</span><span class="sxs-lookup"><span data-stu-id="eff2c-120">The application must allocate and manage pBaryData.</span></span>

<span data-ttu-id="eff2c-121">Les coordonnées Barycentric définissent un point à l’intérieur d’un triangle en termes de sommets du triangle.</span><span class="sxs-lookup"><span data-stu-id="eff2c-121">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="eff2c-122">Pour une description plus détaillée des coordonnées Barycentric, consultez [la description des coordonnées Barycentric de MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="eff2c-122">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="eff2c-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eff2c-123">Requirements</span></span>



| <span data-ttu-id="eff2c-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eff2c-124">Requirement</span></span> | <span data-ttu-id="eff2c-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="eff2c-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eff2c-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="eff2c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="eff2c-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="eff2c-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="eff2c-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="eff2c-128">Library</span></span><br/> | <dl> <span data-ttu-id="eff2c-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eff2c-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="eff2c-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eff2c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eff2c-131">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="eff2c-131">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




