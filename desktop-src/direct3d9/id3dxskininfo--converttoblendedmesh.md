---
description: Prend un maillage et retourne un nouveau maillage avec des poids de fusion par vertex et une table de combinaisons de segments. Le tableau décrit les segments qui affectent les sous-ensembles de la maille.
ms.assetid: c26a9e84-5731-4394-a047-5f1ffe7688d9
title: 'ID3DXSkinInfo :: ConvertToBlendedMesh, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.ConvertToBlendedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 051c51291416dd7e190c83433a9bf84baeb92957
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523857"
---
# <a name="id3dxskininfoconverttoblendedmesh-method"></a><span data-ttu-id="7f2f8-104">ID3DXSkinInfo :: ConvertToBlendedMesh, méthode</span><span class="sxs-lookup"><span data-stu-id="7f2f8-104">ID3DXSkinInfo::ConvertToBlendedMesh method</span></span>

<span data-ttu-id="7f2f8-105">Prend un maillage et retourne un nouveau maillage avec des poids de fusion par vertex et une table de combinaisons de segments.</span><span class="sxs-lookup"><span data-stu-id="7f2f8-105">Takes a mesh and returns a new mesh with per-vertex blend weights and a bone combination table.</span></span> <span data-ttu-id="7f2f8-106">Le tableau décrit les segments qui affectent les sous-ensembles de la maille.</span><span class="sxs-lookup"><span data-stu-id="7f2f8-106">The table describes which bones affect which subsets of the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f2f8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f2f8-107">Syntax</span></span>


```C++
HRESULT ConvertToBlendedMesh(
  [in]        LPD3DXMESH   pMesh,
  [in]        DWORD        Options,
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



## <a name="parameters"></a><span data-ttu-id="7f2f8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7f2f8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f2f8-109">*pMesh* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7f2f8-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f2f8-110">Type : **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="7f2f8-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="7f2f8-111">Maillage d’entrée.</span><span class="sxs-lookup"><span data-stu-id="7f2f8-111">Input mesh.</span></span> <span data-ttu-id="7f2f8-112">Consultez [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="7f2f8-112">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f2f8-113">*Options* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7f2f8-113">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f2f8-114">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f2f8-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7f2f8-115">Actuellement inutilisé.</span><span class="sxs-lookup"><span data-stu-id="7f2f8-115">Currently unused.</span></span>

</dd> <dt>

<span data-ttu-id="7f2f8-116">*pAdjacencyIn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7f2f8-116">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f2f8-117">Type : **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="7f2f8-117">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7f2f8-118">Informations d’adjacence de maillage d’entrée.</span><span class="sxs-lookup"><span data-stu-id="7f2f8-118">Input mesh adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="7f2f8-119">*pAdjacencyOut* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7f2f8-119">*pAdjacencyOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f2f8-120">Type : **[ **LPDWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f2f8-120">Type: **[**LPDWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7f2f8-121">Informations d’adjacence de maillage de sortie.</span><span class="sxs-lookup"><span data-stu-id="7f2f8-121">Output mesh adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="7f2f8-122">*pFaceRemap* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7f2f8-122">*pFaceRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f2f8-123">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7f2f8-123">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7f2f8-124">Tableau de DWORDs, un par visage, qui identifie la facette d’origine qui correspond à chaque visage dans le maillage fusionné.</span><span class="sxs-lookup"><span data-stu-id="7f2f8-124">An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the blended mesh.</span></span> <span data-ttu-id="7f2f8-125">Si la valeur fournie pour cet argument est **null**, les données de remappage de visage ne sont pas retournées.</span><span class="sxs-lookup"><span data-stu-id="7f2f8-125">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="7f2f8-126">*ppVertexRemap* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7f2f8-126">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f2f8-127">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="7f2f8-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="7f2f8-128">Adresse d’un pointeur vers une interface [**ID3DXBuffer**](id3dxbuffer.md) , qui contient une valeur DWORD pour chaque vertex qui spécifie la façon dont les nouveaux vertex sont mappés aux anciens vertex.</span><span class="sxs-lookup"><span data-stu-id="7f2f8-128">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="7f2f8-129">Ce remappage est utile si vous devez modifier des données externes en fonction du nouveau mappage de vertex.</span><span class="sxs-lookup"><span data-stu-id="7f2f8-129">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span> <span data-ttu-id="7f2f8-130">Ce paramètre est facultatif. La **valeur null** peut être utilisée.</span><span class="sxs-lookup"><span data-stu-id="7f2f8-130">This parameter is optional; **NULL** may be used.</span></span>

</dd> <dt>

<span data-ttu-id="7f2f8-131">*pMaxVertexInfl* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7f2f8-131">*pMaxVertexInfl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f2f8-132">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7f2f8-132">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7f2f8-133">Pointeur vers une valeur DWORD qui contient le nombre maximal d’influences osseuses requises par vertex pour cette méthode d’habillage.</span><span class="sxs-lookup"><span data-stu-id="7f2f8-133">Pointer to a DWORD that will contain the maximum number of bone influences required per vertex for this skinning method.</span></span>

</dd> <dt>

<span data-ttu-id="7f2f8-134">*pNumBoneCombinations* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7f2f8-134">*pNumBoneCombinations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f2f8-135">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7f2f8-135">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7f2f8-136">Pointeur vers le nombre d’os dans le tableau de combinaisons de segments.</span><span class="sxs-lookup"><span data-stu-id="7f2f8-136">Pointer to the number of bones in the bone combination table.</span></span>

</dd> <dt>

<span data-ttu-id="7f2f8-137">*ppBoneCombinationTable* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7f2f8-137">*ppBoneCombinationTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f2f8-138">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="7f2f8-138">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="7f2f8-139">Pointeur vers la table de combinaisons de segments.</span><span class="sxs-lookup"><span data-stu-id="7f2f8-139">Pointer to the bone combination table.</span></span> <span data-ttu-id="7f2f8-140">Les données sont organisées dans une structure [**D3DXBONECOMBINATION**](d3dxbonecombination.md) .</span><span class="sxs-lookup"><span data-stu-id="7f2f8-140">The data is organized in a [**D3DXBONECOMBINATION**](d3dxbonecombination.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7f2f8-141">*ppMesh* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7f2f8-141">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f2f8-142">Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="7f2f8-142">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="7f2f8-143">Pointeur vers le nouveau maillage.</span><span class="sxs-lookup"><span data-stu-id="7f2f8-143">Pointer to the new mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f2f8-144">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7f2f8-144">Return value</span></span>

<span data-ttu-id="7f2f8-145">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7f2f8-145">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7f2f8-146">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7f2f8-146">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7f2f8-147">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="7f2f8-147">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f2f8-148">Notes</span><span class="sxs-lookup"><span data-stu-id="7f2f8-148">Remarks</span></span>

<span data-ttu-id="7f2f8-149">Chaque élément du tableau de remappage spécifie l’index précédent pour cette position.</span><span class="sxs-lookup"><span data-stu-id="7f2f8-149">Each element in the remap array specifies the previous index for that position.</span></span> <span data-ttu-id="7f2f8-150">Par exemple, si un vertex était à la position 3 mais a été remappé à la position 5, le cinquième élément de pVertexRemap contiendra 3.</span><span class="sxs-lookup"><span data-stu-id="7f2f8-150">For example, if a vertex was in position 3 but has been remapped to position 5, then the fifth element of pVertexRemap will contain 3.</span></span>

<span data-ttu-id="7f2f8-151">Cette méthode ne s’exécute pas sur un matériel qui ne prend pas en charge la fusion de vertex à fonction fixe.</span><span class="sxs-lookup"><span data-stu-id="7f2f8-151">This method does not run on hardware that does not support fixed-function vertex blending.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f2f8-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f2f8-152">Requirements</span></span>



| <span data-ttu-id="7f2f8-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7f2f8-153">Requirement</span></span> | <span data-ttu-id="7f2f8-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f2f8-154">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f2f8-155">En-tête</span><span class="sxs-lookup"><span data-stu-id="7f2f8-155">Header</span></span><br/>  | <dl> <span data-ttu-id="7f2f8-156"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f2f8-156"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="7f2f8-157">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7f2f8-157">Library</span></span><br/> | <dl> <span data-ttu-id="7f2f8-158"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f2f8-158"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7f2f8-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f2f8-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f2f8-160">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="7f2f8-160">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
