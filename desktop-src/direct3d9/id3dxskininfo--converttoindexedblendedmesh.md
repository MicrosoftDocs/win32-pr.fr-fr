---
description: Prend une maille et retourne un nouveau maillage avec des poids de fusion par vertex, des index et une table de combinaisons de segments. Le tableau décrit les palettes osseuses qui affectent les sous-ensembles de la maille.
ms.assetid: e4758a3b-8a45-4ed3-aa62-9713d12afc56
title: 'ID3DXSkinInfo :: ConvertToIndexedBlendedMesh, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.ConvertToIndexedBlendedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 87c8a4b943a647e52d7260f1ff53b32b40756761
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535836"
---
# <a name="id3dxskininfoconverttoindexedblendedmesh-method"></a><span data-ttu-id="608bc-104">ID3DXSkinInfo :: ConvertToIndexedBlendedMesh, méthode</span><span class="sxs-lookup"><span data-stu-id="608bc-104">ID3DXSkinInfo::ConvertToIndexedBlendedMesh method</span></span>

<span data-ttu-id="608bc-105">Prend une maille et retourne un nouveau maillage avec des poids de fusion par vertex, des index et une table de combinaisons de segments.</span><span class="sxs-lookup"><span data-stu-id="608bc-105">Takes a mesh and returns a new mesh with per-vertex blend weights, indices, and a bone combination table.</span></span> <span data-ttu-id="608bc-106">Le tableau décrit les palettes osseuses qui affectent les sous-ensembles de la maille.</span><span class="sxs-lookup"><span data-stu-id="608bc-106">The table describes which bone palettes affect which subsets of the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="608bc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="608bc-107">Syntax</span></span>


```C++
HRESULT ConvertToIndexedBlendedMesh(
  [in]        LPD3DXMESH   pMesh,
  [in]        DWORD        Options,
  [in]        DWORD        paletteSize,
  [in]  const DWORD        *pAdjacencyIn,
  [in]        LPDWORD      pAdjacencyOut,
  [out]       DWORD        *pFaceRemap,
  [out]       LPD3DXBUFFER *ppVertexRemap,
  [out]       DWORD        *pMaxVertexInfl,
  [out]       DWORD        *pNumBoneCombinations,
  [out]       LPD3DXBUFFER *ppBoneCombinationTable,
  [out]       LPD3DXMESH   *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="608bc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="608bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="608bc-109">*pMesh* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="608bc-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="608bc-110">Type : **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="608bc-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="608bc-111">Maillage d’entrée.</span><span class="sxs-lookup"><span data-stu-id="608bc-111">The input mesh.</span></span> <span data-ttu-id="608bc-112">Consultez [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="608bc-112">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="608bc-113">*Options* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="608bc-113">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="608bc-114">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="608bc-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="608bc-115">Actuellement inutilisé.</span><span class="sxs-lookup"><span data-stu-id="608bc-115">Currently unused.</span></span>

</dd> <dt>

<span data-ttu-id="608bc-116">*paletteSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="608bc-116">*paletteSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="608bc-117">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="608bc-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="608bc-118">Nombre de matrices osseuses disponibles pour le dépouillement de palette de matrice.</span><span class="sxs-lookup"><span data-stu-id="608bc-118">Number of bone matrices available for matrix palette skinning.</span></span>

</dd> <dt>

<span data-ttu-id="608bc-119">*pAdjacencyIn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="608bc-119">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="608bc-120">Type : **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="608bc-120">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="608bc-121">Informations d’adjacence de maillage d’entrée.</span><span class="sxs-lookup"><span data-stu-id="608bc-121">Input mesh adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="608bc-122">*pAdjacencyOut* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="608bc-122">*pAdjacencyOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="608bc-123">Type : **[ **LPDWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="608bc-123">Type: **[**LPDWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="608bc-124">Informations d’adjacence de maillage de sortie.</span><span class="sxs-lookup"><span data-stu-id="608bc-124">Output mesh adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="608bc-125">*pFaceRemap* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="608bc-125">*pFaceRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="608bc-126">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="608bc-126">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="608bc-127">Tableau de DWORDs, un par visage, qui identifie la facette d’origine qui correspond à chaque visage dans le maillage fusionné.</span><span class="sxs-lookup"><span data-stu-id="608bc-127">An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the blended mesh.</span></span> <span data-ttu-id="608bc-128">Si la valeur fournie pour cet argument est **null**, les données de remappage de visage ne sont pas retournées.</span><span class="sxs-lookup"><span data-stu-id="608bc-128">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="608bc-129">*ppVertexRemap* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="608bc-129">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="608bc-130">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="608bc-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="608bc-131">Adresse d’un pointeur vers une interface [**ID3DXBuffer**](id3dxbuffer.md) , qui contient une valeur DWORD pour chaque vertex qui spécifie la façon dont les nouveaux vertex sont mappés aux anciens vertex.</span><span class="sxs-lookup"><span data-stu-id="608bc-131">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="608bc-132">Ce remappage est utile si vous devez modifier des données externes en fonction du nouveau mappage de vertex.</span><span class="sxs-lookup"><span data-stu-id="608bc-132">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span> <span data-ttu-id="608bc-133">Ce paramètre est facultatif. La **valeur null** peut être utilisée.</span><span class="sxs-lookup"><span data-stu-id="608bc-133">This parameter is optional; **NULL** may be used.</span></span>

</dd> <dt>

<span data-ttu-id="608bc-134">*pMaxVertexInfl* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="608bc-134">*pMaxVertexInfl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="608bc-135">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="608bc-135">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="608bc-136">Pointeur vers une valeur DWORD qui contient le nombre maximal d’influences osseuses requises par vertex pour cette méthode d’habillage.</span><span class="sxs-lookup"><span data-stu-id="608bc-136">Pointer to a DWORD that will contain the maximum number of bone influences required per vertex for this skinning method.</span></span>

</dd> <dt>

<span data-ttu-id="608bc-137">*pNumBoneCombinations* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="608bc-137">*pNumBoneCombinations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="608bc-138">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="608bc-138">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="608bc-139">Pointeur vers le nombre d’os dans le tableau de combinaisons de segments.</span><span class="sxs-lookup"><span data-stu-id="608bc-139">Pointer to the number of bones in the bone combination table.</span></span>

</dd> <dt>

<span data-ttu-id="608bc-140">*ppBoneCombinationTable* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="608bc-140">*ppBoneCombinationTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="608bc-141">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="608bc-141">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="608bc-142">Pointeur vers la table de combinaisons de segments.</span><span class="sxs-lookup"><span data-stu-id="608bc-142">Pointer to the bone combination table.</span></span> <span data-ttu-id="608bc-143">Les données sont organisées dans une structure [**D3DXBONECOMBINATION**](d3dxbonecombination.md) .</span><span class="sxs-lookup"><span data-stu-id="608bc-143">The data is organized in a [**D3DXBONECOMBINATION**](d3dxbonecombination.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="608bc-144">*ppMesh* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="608bc-144">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="608bc-145">Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="608bc-145">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="608bc-146">Pointeur vers le nouveau maillage.</span><span class="sxs-lookup"><span data-stu-id="608bc-146">Pointer to the new mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="608bc-147">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="608bc-147">Return value</span></span>

<span data-ttu-id="608bc-148">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="608bc-148">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="608bc-149">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="608bc-149">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="608bc-150">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="608bc-150">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="608bc-151">Notes</span><span class="sxs-lookup"><span data-stu-id="608bc-151">Remarks</span></span>

<span data-ttu-id="608bc-152">Chaque élément dans les tableaux de remappage spécifie l’index précédent pour cette position.</span><span class="sxs-lookup"><span data-stu-id="608bc-152">Each element in the remap arrays specifies the previous index for that position.</span></span> <span data-ttu-id="608bc-153">Par exemple, si un vertex était à la position 3 mais a été remappé à la position 5, le cinquième élément de pVertexRemap contiendra 3.</span><span class="sxs-lookup"><span data-stu-id="608bc-153">For example, if a vertex was in position 3 but has been remapped to position 5, then the fifth element of pVertexRemap will contain 3.</span></span>

<span data-ttu-id="608bc-154">Cette méthode ne s’exécute pas sur un matériel qui ne prend pas en charge la fusion de vertex à fonction fixe.</span><span class="sxs-lookup"><span data-stu-id="608bc-154">This method does not run on hardware that does not support fixed-function vertex blending.</span></span>

## <a name="requirements"></a><span data-ttu-id="608bc-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="608bc-155">Requirements</span></span>



| <span data-ttu-id="608bc-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="608bc-156">Requirement</span></span> | <span data-ttu-id="608bc-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="608bc-157">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="608bc-158">En-tête</span><span class="sxs-lookup"><span data-stu-id="608bc-158">Header</span></span><br/>  | <dl> <span data-ttu-id="608bc-159"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="608bc-159"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="608bc-160">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="608bc-160">Library</span></span><br/> | <dl> <span data-ttu-id="608bc-161"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="608bc-161"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="608bc-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="608bc-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="608bc-163">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="608bc-163">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
