---
description: D3DXUVAtlasPartition fonction-créer un Atlas UV pour une maille.
ms.assetid: c46f3e47-8e72-435c-875d-cccfa4b893a2
title: D3DXUVAtlasPartition, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasPartition
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 63df6bbcc1b811b9617796bc6e7e51af2dfdca56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117797"
---
# <a name="d3dxuvatlaspartition-function"></a><span data-ttu-id="1eb70-103">D3DXUVAtlasPartition fonction)</span><span class="sxs-lookup"><span data-stu-id="1eb70-103">D3DXUVAtlasPartition function</span></span>

<span data-ttu-id="1eb70-104">Créez un Atlas UV pour une maille.</span><span class="sxs-lookup"><span data-stu-id="1eb70-104">Create a UV atlas for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="1eb70-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1eb70-105">Syntax</span></span>


```C++
HRESULT D3DXUVAtlasPartition(
  _In_        LPD3DXMESH      pMesh,
  _In_        UINT            dwMaxChartNumber,
  _In_        FLOAT           fMaxStretch,
  _In_        DWORD           dwTextureIndex,
  _In_  const DWORD           *pdwAdjacency,
        const DWORD           *pdwFalseEdges,
  _In_        FLOAT           *pfIMTArray,
  _In_        LPD3DXUVATLASCB pCallback,
  _In_        FLOAT           fCallbackFrequency,
  _In_        LPVOID          pUserContent,
  _In_        DWORD           dwOptions,
  _In_        LPD3DXMESH      *ppMeshOut,
  _Out_       LPD3DXBUFFER    pFacePartitioning,
  _Out_       LPD3DXBUFFER    *ppVertexRemapArray,
              LPD3DXBUFFER    *ppPartitionResultAdjacency,
  _Out_       FLOAT           *pfMaxStretchOut,
  _Out_       UINT            *pdwNumChartsOut
);
```



## <a name="parameters"></a><span data-ttu-id="1eb70-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1eb70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1eb70-107">*pMesh* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1eb70-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eb70-108">Type : **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="1eb70-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="1eb70-109">Pointeur vers un maillage d’entrée (voir [**ID3DXMesh**](id3dxmesh.md)) qui contient la géométrie de l’objet pour le calcul de l’Atlas.</span><span class="sxs-lookup"><span data-stu-id="1eb70-109">Pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) that contains the object geometry for calculating the atlas.</span></span> <span data-ttu-id="1eb70-110">Au minimum, la maille doit contenir des données de position et des coordonnées de texture 2D.</span><span class="sxs-lookup"><span data-stu-id="1eb70-110">At a minimum, the mesh must contain position data and 2D texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="1eb70-111">*dwMaxChartNumber* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1eb70-111">*dwMaxChartNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eb70-112">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1eb70-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1eb70-113">Nombre maximal de graphiques dans lesquels partitionner le maillage.</span><span class="sxs-lookup"><span data-stu-id="1eb70-113">The maximum number of charts to partition the mesh into.</span></span> <span data-ttu-id="1eb70-114">Consultez les remarques sur les modes de partitionnement.</span><span class="sxs-lookup"><span data-stu-id="1eb70-114">See remarks about the partitioning modes.</span></span> <span data-ttu-id="1eb70-115">Utilisez 0 pour indiquer à D3DX que l’Atlas doit être paramétré en fonction de Stretch.</span><span class="sxs-lookup"><span data-stu-id="1eb70-115">Use 0 to tell D3DX that the atlas should be parameterized based on stretch.</span></span>

</dd> <dt>

<span data-ttu-id="1eb70-116">*fMaxStretch* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1eb70-116">*fMaxStretch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eb70-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1eb70-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1eb70-118">Quantité d’étirement autorisée.</span><span class="sxs-lookup"><span data-stu-id="1eb70-118">The amount of stretching allowed.</span></span> <span data-ttu-id="1eb70-119">0 signifie qu’aucun étirement n’est autorisé, 1 signifie qu’une quantité d’étirement peut être utilisée.</span><span class="sxs-lookup"><span data-stu-id="1eb70-119">0 means no stretching is allowed, 1 means any amount of stretching can be used.</span></span>

</dd> <dt>

<span data-ttu-id="1eb70-120">*dwTextureIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1eb70-120">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eb70-121">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1eb70-121">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1eb70-122">Index de coordonnées de texture de base zéro qui identifie le jeu de coordonnées de texture à utiliser.</span><span class="sxs-lookup"><span data-stu-id="1eb70-122">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="1eb70-123">*pdwAdjacency* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1eb70-123">*pdwAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eb70-124">Type : **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="1eb70-124">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1eb70-125">Pointeur vers un tableau de données d’contiguïté avec 3 DWORDs par face, indiquant quels triangles sont adjacents les uns aux autres (voir [**ID3DXBaseMesh :: GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).</span><span class="sxs-lookup"><span data-stu-id="1eb70-125">A pointer to an array of adjacency data with 3 DWORDs per face, indicating which triangles are adjacent to each other (see [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).</span></span>

</dd> <dt>

<span data-ttu-id="1eb70-126">*pdwFalseEdges*</span><span class="sxs-lookup"><span data-stu-id="1eb70-126">*pdwFalseEdges*</span></span> 
</dt> <dd>

<span data-ttu-id="1eb70-127">Type : **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="1eb70-127">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1eb70-128">Tableau avec 3 DWORDs par face.</span><span class="sxs-lookup"><span data-stu-id="1eb70-128">An array with 3 DWORDS per face.</span></span> <span data-ttu-id="1eb70-129">Chaque visage indique si une arête est false ou non.</span><span class="sxs-lookup"><span data-stu-id="1eb70-129">Each face indicates if an edge is false or not.</span></span> <span data-ttu-id="1eb70-130">Un bord non-faux est indiqué par-1, un faux bord est indiqué par une autre valeur.</span><span class="sxs-lookup"><span data-stu-id="1eb70-130">A non-false edge is indicated by -1, a false edge is indicated by any other value.</span></span> <span data-ttu-id="1eb70-131">Cela permet le paramétrage d’une maille de quatre cœurs où les bords du milieu de chaque quadruple ne sont pas coupés.</span><span class="sxs-lookup"><span data-stu-id="1eb70-131">This enables the parameterization of a mesh of quads where the edges down the middle of each quad will not be cut.</span></span>

</dd> <dt>

<span data-ttu-id="1eb70-132">*pfIMTArray* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1eb70-132">*pfIMTArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eb70-133">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1eb70-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1eb70-134">Pointeur vers un tableau de dizaines de métriques intégrés qui décrit comment étirer un triangle (voir [IntegratedMetricTensor](using-uvatlas.md)).</span><span class="sxs-lookup"><span data-stu-id="1eb70-134">A pointer to an array of integrated metric tensors that describes how to stretch a triangle (see [IntegratedMetricTensor](using-uvatlas.md)).</span></span>

</dd> <dt>

<span data-ttu-id="1eb70-135">*pCallback* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1eb70-135">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eb70-136">Type : **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="1eb70-136">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="1eb70-137">Pointeur vers une fonction de rappel (voir [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) qui est utile pour surveiller la progression.</span><span class="sxs-lookup"><span data-stu-id="1eb70-137">A pointer to a callback function (see [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) that is useful for monitoring progress.</span></span>

</dd> <dt>

<span data-ttu-id="1eb70-138">*fCallbackFrequency* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1eb70-138">*fCallbackFrequency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eb70-139">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1eb70-139">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1eb70-140">Spécifiez la fréquence à laquelle D3DX appellera le rappel. une valeur par défaut raisonnable est 0,0001 f.</span><span class="sxs-lookup"><span data-stu-id="1eb70-140">Specify how often D3DX will call the callback; a reasonable default value is 0.0001f.</span></span>

</dd> <dt>

<span data-ttu-id="1eb70-141">*pUserContent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1eb70-141">*pUserContent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eb70-142">Type : **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1eb70-142">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1eb70-143">Pointeur vers une valeur définie par l’utilisateur qui est passée à la fonction de rappel ; généralement utilisé par une application pour passer un pointeur vers une structure de données qui fournit des informations de contexte pour la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="1eb70-143">Pointer to a user-defined value that is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="1eb70-144">*dwOptions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1eb70-144">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eb70-145">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1eb70-145">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1eb70-146">Spécifiez la qualité des graphiques générés en combinant un ou plusieurs indicateurs [**D3DXUVATLAS**](./d3dxuvatlas.md) .</span><span class="sxs-lookup"><span data-stu-id="1eb70-146">Specify the quality of the charts generated by combining one or more [**D3DXUVATLAS**](./d3dxuvatlas.md) flags.</span></span>

</dd> <dt>

<span data-ttu-id="1eb70-147">*ppMeshOut* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1eb70-147">*ppMeshOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eb70-148">Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="1eb70-148">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="1eb70-149">Pointeur vers la maille créée avec l’Atlas (voir [**ID3DXMesh**](id3dxmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="1eb70-149">Pointer to the created mesh with the atlas (see [**ID3DXMesh**](id3dxmesh.md)).</span></span>

</dd> <dt>

<span data-ttu-id="1eb70-150">*pFacePartitioning* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1eb70-150">*pFacePartitioning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1eb70-151">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="1eb70-151">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)**</span></span>

<span data-ttu-id="1eb70-152">Pointeur vers un tableau des données de partitionnement de type final.</span><span class="sxs-lookup"><span data-stu-id="1eb70-152">A pointer to an array of the final face-partitioning data.</span></span> <span data-ttu-id="1eb70-153">Chaque élément contient un DWORD par face (voir [**ID3DXBuffer**](id3dxbuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="1eb70-153">Each element contains one DWORD per face (see [**ID3DXBuffer**](id3dxbuffer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="1eb70-154">*ppVertexRemapArray* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1eb70-154">*ppVertexRemapArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1eb70-155">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="1eb70-155">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="1eb70-156">Pointeur vers un tableau de vertex remappés.</span><span class="sxs-lookup"><span data-stu-id="1eb70-156">A pointer to an array of remapped vertices.</span></span> <span data-ttu-id="1eb70-157">Chaque élément de tableau identifie le sommet d’origine à partir duquel provient chaque sommet final (si le Vertex a été fractionné pendant le remappage).</span><span class="sxs-lookup"><span data-stu-id="1eb70-157">Each array element identifies the original vertex each final vertex came from (if the vertex was split during remapping).</span></span> <span data-ttu-id="1eb70-158">Chaque élément de tableau contient une valeur DWORD par vertex.</span><span class="sxs-lookup"><span data-stu-id="1eb70-158">Each array element contains one DWORD per vertex.</span></span>

</dd> <dt>

<span data-ttu-id="1eb70-159">*ppPartitionResultAdjacency*</span><span class="sxs-lookup"><span data-stu-id="1eb70-159">*ppPartitionResultAdjacency*</span></span> 
</dt> <dd>

<span data-ttu-id="1eb70-160">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="1eb70-160">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="1eb70-161">Adresse d’un pointeur vers une interface [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="1eb70-161">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="1eb70-162">Cette mémoire tampon contient un tableau de trois DWORD par visage qui spécifient les trois voisins pour chaque visage dans le maillage de sortie.</span><span class="sxs-lookup"><span data-stu-id="1eb70-162">This buffer will contain an array of three DWORDs per face that specify the three neighbors for each face in the output mesh.</span></span> <span data-ttu-id="1eb70-163">Ce paramètre ne doit pas avoir la **valeur null**, car l’appel suivant à D3DXUVAtlasPack () en a besoin.</span><span class="sxs-lookup"><span data-stu-id="1eb70-163">This parameter must not be **NULL**, because the subsequent call to D3DXUVAtlasPack() requires it.</span></span>

</dd> <dt>

<span data-ttu-id="1eb70-164">*pfMaxStretchOut* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1eb70-164">*pfMaxStretchOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1eb70-165">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1eb70-165">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1eb70-166">Pointeur vers la valeur d’étirement maximale générée par l’algorithme Atlas.</span><span class="sxs-lookup"><span data-stu-id="1eb70-166">A pointer to the maximum stretch value generated by the atlas algorithm.</span></span> <span data-ttu-id="1eb70-167">La plage est comprise entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="1eb70-167">The range is between 0.0 and 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="1eb70-168">*pdwNumChartsOut* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1eb70-168">*pdwNumChartsOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1eb70-169">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1eb70-169">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1eb70-170">Pointeur vers le nombre de graphiques créés par l’algorithme Atlas.</span><span class="sxs-lookup"><span data-stu-id="1eb70-170">A pointer to the number of charts created by the atlas algorithm.</span></span> <span data-ttu-id="1eb70-171">Si dwMaxChartNumber est trop faible, ce paramètre retourne le nombre minimal de graphiques requis pour créer un Atlas.</span><span class="sxs-lookup"><span data-stu-id="1eb70-171">If dwMaxChartNumber is too low, this parameter will return the minimum number of charts required to create an atlas.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1eb70-172">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1eb70-172">Return value</span></span>

<span data-ttu-id="1eb70-173">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1eb70-173">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1eb70-174">Si la fonction est réussie, la valeur de retour est D3D \_ OK ; sinon, la valeur est D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="1eb70-174">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="1eb70-175">Notes </span><span class="sxs-lookup"><span data-stu-id="1eb70-175">Remarks</span></span>

<span data-ttu-id="1eb70-176">D3DXUVAtlasPartition est similaire à [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md), à ceci près que D3DXUVAtlasPartition n’effectue pas l’étape de compression finale.</span><span class="sxs-lookup"><span data-stu-id="1eb70-176">D3DXUVAtlasPartition is similar to [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md), except that D3DXUVAtlasPartition does not performing the final packing step.</span></span>

## <a name="requirements"></a><span data-ttu-id="1eb70-177">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1eb70-177">Requirements</span></span>



| <span data-ttu-id="1eb70-178">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1eb70-178">Requirement</span></span> | <span data-ttu-id="1eb70-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="1eb70-179">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1eb70-180">En-tête</span><span class="sxs-lookup"><span data-stu-id="1eb70-180">Header</span></span><br/>  | <dl> <span data-ttu-id="1eb70-181"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1eb70-181"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1eb70-182">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1eb70-182">Library</span></span><br/> | <dl> <span data-ttu-id="1eb70-183"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1eb70-183"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1eb70-184">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1eb70-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1eb70-185">UVAtlas, fonctions</span><span class="sxs-lookup"><span data-stu-id="1eb70-185">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

<span data-ttu-id="1eb70-186">[Outil Command-Line d’Atlas UV (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="1eb70-186">[UV Atlas Command-Line Tool (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 
