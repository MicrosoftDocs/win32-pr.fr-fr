---
description: Définit les coordonnées Barycentric texels.
ms.assetid: 6c7c74aa-71a3-45aa-9b18-6409fbd63bda
title: 'ID3DXTextureGutterHelper :: SetBaryMap, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetBaryMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5e3de61913041a4e59e075ea42dacc308c1ce5f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211906"
---
# <a name="id3dxtexturegutterhelpersetbarymap-method"></a><span data-ttu-id="85f09-103">ID3DXTextureGutterHelper :: SetBaryMap, méthode</span><span class="sxs-lookup"><span data-stu-id="85f09-103">ID3DXTextureGutterHelper::SetBaryMap method</span></span>

<span data-ttu-id="85f09-104">Définit les coordonnées Barycentric texels.</span><span class="sxs-lookup"><span data-stu-id="85f09-104">Sets texel barycentric coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="85f09-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="85f09-105">Syntax</span></span>


```C++
HRESULT SetBaryMap(
  [in] D3DXVECTOR2 *pBaryData
);
```



## <a name="parameters"></a><span data-ttu-id="85f09-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="85f09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85f09-107">*pBaryData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="85f09-107">*pBaryData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85f09-108">Type : **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="85f09-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="85f09-109">Pointeur vers une structure [**D3DXVECTOR2**](d3dxvector2.md) qui contient les deux premières coordonnées Barycentric de chaque Texel.</span><span class="sxs-lookup"><span data-stu-id="85f09-109">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that contains the first two barycentric coordinates of each texel.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85f09-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="85f09-110">Return value</span></span>

<span data-ttu-id="85f09-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="85f09-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="85f09-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="85f09-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="85f09-113">Si la méthode échoue, la valeur suivante est retournée. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="85f09-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="85f09-114">Notes</span><span class="sxs-lookup"><span data-stu-id="85f09-114">Remarks</span></span>

<span data-ttu-id="85f09-115">La troisième coordonnée Barycentric est donnée par :</span><span class="sxs-lookup"><span data-stu-id="85f09-115">The third barycentric coordinate is given by:</span></span>


```
1 - ( pBaryData.x + pBaryData.y )
```



<span data-ttu-id="85f09-116">L’entrée de coordonnées Barycentric pour cette méthode est valide uniquement pour les texels valides (non de classe 0).</span><span class="sxs-lookup"><span data-stu-id="85f09-116">The barycentric coordinates input to this method are valid only for valid (non-class 0) texels.</span></span> <span data-ttu-id="85f09-117">[**ID3DXTextureGutterHelper :: GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) retourne des valeurs non nulles pour les texels valides.</span><span class="sxs-lookup"><span data-stu-id="85f09-117">[**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) will return non-zero values for valid texels.</span></span>

<span data-ttu-id="85f09-118">Les coordonnées Barycentric définissent un point à l’intérieur d’un triangle en termes de sommets du triangle.</span><span class="sxs-lookup"><span data-stu-id="85f09-118">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="85f09-119">Pour une description plus détaillée des coordonnées Barycentric, consultez [la description des coordonnées Barycentric de MathWorld](http://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="85f09-119">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](http://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="85f09-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="85f09-120">Requirements</span></span>



| <span data-ttu-id="85f09-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="85f09-121">Requirement</span></span> | <span data-ttu-id="85f09-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="85f09-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="85f09-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="85f09-123">Header</span></span><br/>  | <dl> <span data-ttu-id="85f09-124"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="85f09-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="85f09-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="85f09-125">Library</span></span><br/> | <dl> <span data-ttu-id="85f09-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="85f09-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="85f09-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85f09-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85f09-128">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="85f09-128">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




