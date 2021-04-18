---
description: Empaqueter des données de partitionnement de maillage dans un Atlas.
ms.assetid: 4da85626-c36c-44d9-990b-0db80ed04423
title: D3DXUVAtlasPack, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasPack
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 31de326160120fe14a71841cb5f2d18e1c8d4e57
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106536243"
---
# <a name="d3dxuvatlaspack-function"></a><span data-ttu-id="b0207-103">D3DXUVAtlasPack fonction)</span><span class="sxs-lookup"><span data-stu-id="b0207-103">D3DXUVAtlasPack function</span></span>

<span data-ttu-id="b0207-104">Empaqueter des données de partitionnement de maillage dans un Atlas.</span><span class="sxs-lookup"><span data-stu-id="b0207-104">Pack mesh partitioning data into an atlas.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0207-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b0207-105">Syntax</span></span>


```C++
HRESULT D3DXUVAtlasPack(
  _In_       LPD3DXMESH      pMesh,
  _In_       UINT            dwWidth,
  _In_       UINT            dwHeight,
  _In_       FLOAT           fGutter,
  _In_       DWORD           dwTextureIndex,
       const DWORD           *pdwPartitionResultAdjacency,
  _In_       LPD3DXUVATLASCB pCallback,
  _In_       FLOAT           fCallbackFrequency,
  _In_       LPVOID          pUserContent,
  _In_       DWORD           dwOptions,
  _In_       LPD3DXBUFFER    pFacePartitioning
);
```



## <a name="parameters"></a><span data-ttu-id="b0207-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b0207-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0207-107">*pMesh* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b0207-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0207-108">Type : **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="b0207-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="b0207-109">Pointeur vers un maillage d’entrée (voir [**ID3DXMesh**](id3dxmesh.md)) qui contient la géométrie de l’objet pour le calcul de l’Atlas.</span><span class="sxs-lookup"><span data-stu-id="b0207-109">Pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the atlas.</span></span> <span data-ttu-id="b0207-110">Au minimum, la maille doit contenir des données de position et des coordonnées de texture 2D.</span><span class="sxs-lookup"><span data-stu-id="b0207-110">At a minimum, the mesh must contain position data and 2D texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="b0207-111">*dwWidth* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b0207-111">*dwWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0207-112">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0207-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b0207-113">Largeur de la texture.</span><span class="sxs-lookup"><span data-stu-id="b0207-113">Texture width.</span></span>

</dd> <dt>

<span data-ttu-id="b0207-114">*dwHeight* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b0207-114">*dwHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0207-115">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0207-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b0207-116">Hauteur de la texture.</span><span class="sxs-lookup"><span data-stu-id="b0207-116">Texture height.</span></span>

</dd> <dt>

<span data-ttu-id="b0207-117">*fGutter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b0207-117">*fGutter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0207-118">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0207-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b0207-119">Distance minimale, dans les texels, entre deux graphiques sur l’Atlas.</span><span class="sxs-lookup"><span data-stu-id="b0207-119">The minimum distance, in texels, between two charts on the atlas.</span></span> <span data-ttu-id="b0207-120">La reliure est toujours mise à l’échelle en largeur ; ainsi, si une marge de 2,5 est utilisée sur une texture 512 x 512, la distance minimale entre deux graphiques 2,5 est de/512,0.</span><span class="sxs-lookup"><span data-stu-id="b0207-120">The gutter is always scaled by the width; so, if a gutter of 2.5 is used on a 512x512 texture, then the minimum distance between two charts is 2.5 / 512.0 texels.</span></span>

</dd> <dt>

<span data-ttu-id="b0207-121">*dwTextureIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b0207-121">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0207-122">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0207-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b0207-123">Index de coordonnées de texture de base zéro qui identifie le jeu de coordonnées de texture à utiliser.</span><span class="sxs-lookup"><span data-stu-id="b0207-123">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="b0207-124">*pdwPartitionResultAdjacency*</span><span class="sxs-lookup"><span data-stu-id="b0207-124">*pdwPartitionResultAdjacency*</span></span> 
</dt> <dd>

<span data-ttu-id="b0207-125">Type : **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="b0207-125">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b0207-126">Pointeur vers un tableau de trois DWORD par visage qui spécifient les trois voisins pour chaque face de la maille.</span><span class="sxs-lookup"><span data-stu-id="b0207-126">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="b0207-127">Elle doit être dérivée de la ppPartitionResultAdjacency retournée par [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md).</span><span class="sxs-lookup"><span data-stu-id="b0207-127">It should be derived from the ppPartitionResultAdjacency returned from [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md).</span></span> <span data-ttu-id="b0207-128">Cette valeur ne peut pas être **null**, car Pack doit savoir où les graphiques ont été coupés dans l’étape de la partition afin de trouver les bords de chaque graphique.</span><span class="sxs-lookup"><span data-stu-id="b0207-128">This value cannot be **NULL**, because Pack needs to know where charts were cut in the partition step in order to find the edges of each chart.</span></span>

</dd> <dt>

<span data-ttu-id="b0207-129">*pCallback* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b0207-129">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0207-130">Type : **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="b0207-130">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="b0207-131">Pointeur vers une fonction de rappel (voir [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) qui est utile pour surveiller la progression.</span><span class="sxs-lookup"><span data-stu-id="b0207-131">A pointer to a callback function (see [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) that is useful for monitoring progress.</span></span>

</dd> <dt>

<span data-ttu-id="b0207-132">*fCallbackFrequency* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b0207-132">*fCallbackFrequency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0207-133">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0207-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b0207-134">Spécifiez la fréquence à laquelle D3DX appellera le rappel. une valeur par défaut raisonnable est 0,0001 f.</span><span class="sxs-lookup"><span data-stu-id="b0207-134">Specify how often D3DX will call the callback; a reasonable default value is 0.0001f.</span></span>

</dd> <dt>

<span data-ttu-id="b0207-135">*pUserContent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b0207-135">*pUserContent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0207-136">Type : **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0207-136">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b0207-137">Pointeur void à retourner à la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="b0207-137">A void pointer to be passed back to the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="b0207-138">*dwOptions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b0207-138">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0207-139">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0207-139">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b0207-140">Ce paramètre d’options est actuellement réservé.</span><span class="sxs-lookup"><span data-stu-id="b0207-140">This options parameter is currently reserved.</span></span>

</dd> <dt>

<span data-ttu-id="b0207-141">*pFacePartitioning* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b0207-141">*pFacePartitioning* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0207-142">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="b0207-142">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)**</span></span>

<span data-ttu-id="b0207-143">Pointeur vers un [**ID3DXBuffer**](id3dxbuffer.md) contenant le tableau du partitionnement de visages final.</span><span class="sxs-lookup"><span data-stu-id="b0207-143">A pointer to an [**ID3DXBuffer**](id3dxbuffer.md) containing the array of the final face-partitioning.</span></span> <span data-ttu-id="b0207-144">Chaque élément contient un DWORD par face.</span><span class="sxs-lookup"><span data-stu-id="b0207-144">Each element contains one DWORD per face.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0207-145">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b0207-145">Return value</span></span>

<span data-ttu-id="b0207-146">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b0207-146">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b0207-147">Si la fonction est réussie, la valeur de retour est D3D \_ OK ; sinon, la valeur est D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b0207-147">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0207-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b0207-148">Requirements</span></span>



| <span data-ttu-id="b0207-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b0207-149">Requirement</span></span> | <span data-ttu-id="b0207-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="b0207-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0207-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="b0207-151">Header</span></span><br/>  | <dl> <span data-ttu-id="b0207-152"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0207-152"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b0207-153">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b0207-153">Library</span></span><br/> | <dl> <span data-ttu-id="b0207-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0207-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b0207-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0207-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0207-156">UVAtlas, fonctions</span><span class="sxs-lookup"><span data-stu-id="b0207-156">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> </dl>

 

 
