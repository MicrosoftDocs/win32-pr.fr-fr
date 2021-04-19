---
description: Calcule les vecteurs de tangente pour les coordonnées de texture données dans l’étape de texture. Fourni pour prendre en charge les applications héritées. Utilisez D3DXComputeTangentFrameEx pour obtenir de meilleurs résultats.
ms.assetid: 39748459-3f9b-4b48-ae13-7143eb29c292
title: D3DXComputeTangent, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangent
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5cdb6a9dae3bdbad0f239fa61ba066d7b1bffb14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527733"
---
# <a name="d3dxcomputetangent-function"></a><span data-ttu-id="e94fd-105">D3DXComputeTangent fonction)</span><span class="sxs-lookup"><span data-stu-id="e94fd-105">D3DXComputeTangent function</span></span>

<span data-ttu-id="e94fd-106">Calcule les vecteurs de tangente pour les coordonnées de texture données dans l’étape de texture.</span><span class="sxs-lookup"><span data-stu-id="e94fd-106">Computes the tangent vectors for the texture coordinates given in the texture stage.</span></span> <span data-ttu-id="e94fd-107">Fourni pour prendre en charge les applications héritées.</span><span class="sxs-lookup"><span data-stu-id="e94fd-107">Provided to support legacy applications.</span></span> <span data-ttu-id="e94fd-108">Utilisez [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) pour obtenir de meilleurs résultats.</span><span class="sxs-lookup"><span data-stu-id="e94fd-108">Use [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) for better results.</span></span>

## <a name="syntax"></a><span data-ttu-id="e94fd-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e94fd-109">Syntax</span></span>


```C++
HRESULT D3DXComputeTangent(
  _In_       LPD3DXMESH Mesh,
  _In_       DWORD      TexStageIndex,
  _In_       DWORD      TangentIndex,
  _In_       DWORD      BinormIndex,
  _In_       DWORD      Wrap,
  _In_ const DWORD      *pAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="e94fd-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e94fd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e94fd-111">*Maille* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e94fd-111">*Mesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e94fd-112">Type : **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="e94fd-112">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="e94fd-113">Pointeur vers une interface [**ID3DXMesh**](id3dxmesh.md) qui représente le maillage d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e94fd-113">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface that represent the input mesh.</span></span>

</dd> <dt>

<span data-ttu-id="e94fd-114">*TexStageIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e94fd-114">*TexStageIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e94fd-115">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e94fd-115">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e94fd-116">Index qui représente l’étape de la texture.</span><span class="sxs-lookup"><span data-stu-id="e94fd-116">Index that represents the texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="e94fd-117">*TangentIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e94fd-117">*TangentIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e94fd-118">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e94fd-118">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e94fd-119">Index qui fournit l’index d’utilisation pour les données de tangente.</span><span class="sxs-lookup"><span data-stu-id="e94fd-119">Index that provides the usage index for the tangent data.</span></span> <span data-ttu-id="e94fd-120">La déclaration de vertex implique l’utilisation ; Cet index modifie l’utilisation avec l’index d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="e94fd-120">The vertex declaration implies the usage; this index modifies the usage with the usage index.</span></span> <span data-ttu-id="e94fd-121">Pour plus d’informations sur une déclaration de vertex, consultez la rubrique [déclaration de vertex (Direct3D 9)](vertex-declaration.md).</span><span class="sxs-lookup"><span data-stu-id="e94fd-121">For more information about a vertex declaration, see [Vertex Declaration (Direct3D 9)](vertex-declaration.md).</span></span>

</dd> <dt>

<span data-ttu-id="e94fd-122">*BinormIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e94fd-122">*BinormIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e94fd-123">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e94fd-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e94fd-124">Index qui fournit l’index d’utilisation pour les données binormales.</span><span class="sxs-lookup"><span data-stu-id="e94fd-124">Index that provides the usage index for the binormal data.</span></span> <span data-ttu-id="e94fd-125">La déclaration de vertex implique l’utilisation ; Cet index modifie l’utilisation avec l’index d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="e94fd-125">The vertex declaration implies the usage; this index modifies the usage with the usage index.</span></span> <span data-ttu-id="e94fd-126">Pour plus d’informations sur une déclaration de vertex, consultez la rubrique [déclaration de vertex (Direct3D 9)](vertex-declaration.md).</span><span class="sxs-lookup"><span data-stu-id="e94fd-126">For more information about a vertex declaration, see [Vertex Declaration (Direct3D 9)](vertex-declaration.md).</span></span>

</dd> <dt>

<span data-ttu-id="e94fd-127">*Retour à la ligne* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e94fd-127">*Wrap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e94fd-128">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e94fd-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e94fd-129">Définissez cette valeur sur 0 pour aucun habillage, ou sur 1 pour l’habillage dans les directions vous et V.</span><span class="sxs-lookup"><span data-stu-id="e94fd-129">Set this value to 0 for no wrapping, or to 1 for wrapping in the U and V directions.</span></span>

</dd> <dt>

<span data-ttu-id="e94fd-130">*pAdjacency* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e94fd-130">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e94fd-131">Type : **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="e94fd-131">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e94fd-132">Pointeur vers un tableau de trois DWORDs par visage à remplir avec des indices de face adjacente.</span><span class="sxs-lookup"><span data-stu-id="e94fd-132">Pointer to an array of three DWORDs per face to be filled with adjacent face indices.</span></span> <span data-ttu-id="e94fd-133">Le nombre d’octets dans ce tableau doit être au moins égal à ((3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)) \* sizeof (DWORD)).</span><span class="sxs-lookup"><span data-stu-id="e94fd-133">The number of bytes in this array must be at least ((3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)) \* sizeof(DWORD)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e94fd-134">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e94fd-134">Return value</span></span>

<span data-ttu-id="e94fd-135">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e94fd-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e94fd-136">Si la fonction est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e94fd-136">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e94fd-137">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="e94fd-137">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="e94fd-138">Notes</span><span class="sxs-lookup"><span data-stu-id="e94fd-138">Remarks</span></span>

<span data-ttu-id="e94fd-139">Si la déclaration de vertex de maillage spécifie des champs tangente ou binormal, **D3DXComputeTangent** met à jour les données de tangente ou binormal fournies par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e94fd-139">If the mesh vertex declaration specifies tangent or binormal fields, **D3DXComputeTangent** will update any user-supplied tangent or binormal data.</span></span> <span data-ttu-id="e94fd-140">Vous pouvez également définir TangentIndex sur [D3DX \_ default](other-d3dx-constants.md) pour ne pas mettre à jour les données tangentes fournies par l’utilisateur, ou définir BinormIndex sur D3DX \_ Default pour ne pas mettre à jour les données binormales fournies par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e94fd-140">Alternatively, set TangentIndex to [D3DX\_DEFAULT](other-d3dx-constants.md) to not update the user-supplied tangent data, or set BinormIndex to D3DX\_DEFAULT to not update the user-supplied binormal data.</span></span> <span data-ttu-id="e94fd-141">TexStageIndex ne peut pas être défini sur D3DX \_ default.</span><span class="sxs-lookup"><span data-stu-id="e94fd-141">TexStageIndex cannot be set to D3DX\_DEFAULT.</span></span>

<span data-ttu-id="e94fd-142">**D3DXComputeTangent** dépend de la déclaration de vertex de maillage contenant soit le champ binormal (BinormIndex), le champ tangente (TangentIndex), ou les deux.</span><span class="sxs-lookup"><span data-stu-id="e94fd-142">**D3DXComputeTangent** depends on the mesh vertex declaration containing either the binormal field (BinormIndex), the tangent field (TangentIndex), or both.</span></span> <span data-ttu-id="e94fd-143">Si les deux sont absents, cette fonction échoue.</span><span class="sxs-lookup"><span data-stu-id="e94fd-143">If both are missing, this function will fail.</span></span>

<span data-ttu-id="e94fd-144">Cette fonction appelle simplement [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) avec les paramètres d’entrée suivants :</span><span class="sxs-lookup"><span data-stu-id="e94fd-144">This function simply calls [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) with the following input parameters:</span></span>


```
D3DXComputeTangentFrameEx( Mesh,
                           D3DDECLUSAGE_TEXCOORD,
                           TexStageIndex,
                           ( BinormIndex == D3DX_DEFAULT ) ?
                               D3DX_DEFAULT : D3DDECLUSAGE_BINORMAL,
                               // provides backward function compatibility
                           BinormIndex,
                           ( TangentIndex == D3DX_DEFAULT ) ?
                               D3DX_DEFAULT : D3DDECLUSAGE_TANGENT,
                           TangentIndex,
                           D3DX_DEFAULT, // do not store normals
                           0,
                           ( Wrap ? D3DXTANGENT_WRAP_UV : 0 )
                               | D3DXTANGENT_GENERATE_IN_PLACE
                               | D3DXTANGENT_ORTHOGONALIZE_FROM_U,
                           pAdjacency,
                           -1.01f,
                           -0.01f,
                           -1.01f,
                           NULL,
                           NULL);
```



## <a name="requirements"></a><span data-ttu-id="e94fd-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e94fd-145">Requirements</span></span>



| <span data-ttu-id="e94fd-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e94fd-146">Requirement</span></span> | <span data-ttu-id="e94fd-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="e94fd-147">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e94fd-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="e94fd-148">Header</span></span><br/>  | <dl> <span data-ttu-id="e94fd-149"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e94fd-149"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e94fd-150">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e94fd-150">Library</span></span><br/> | <dl> <span data-ttu-id="e94fd-151"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e94fd-151"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e94fd-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e94fd-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e94fd-153">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="e94fd-153">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
