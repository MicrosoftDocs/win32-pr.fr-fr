---
description: D3DXUVAtlasCreate fonction-créer un Atlas UV pour une maille.
ms.assetid: 70256990-b177-451e-b42a-84799fdc2a17
title: D3DXUVAtlasCreate, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasCreate
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5f382e7d59f3a5b5db8ba3cfd65ba6cc1a11e86d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117827"
---
# <a name="d3dxuvatlascreate-function"></a><span data-ttu-id="d13bd-103">D3DXUVAtlasCreate fonction)</span><span class="sxs-lookup"><span data-stu-id="d13bd-103">D3DXUVAtlasCreate function</span></span>

<span data-ttu-id="d13bd-104">Créez un Atlas UV pour une maille.</span><span class="sxs-lookup"><span data-stu-id="d13bd-104">Create a UV atlas for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="d13bd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d13bd-105">Syntax</span></span>


```C++
HRESULT D3DXUVAtlasCreate(
  _In_        LPD3DXMESH      pMesh,
  _In_        UINT            dwMaxChartNumber,
  _In_        FLOAT           fMaxStretch,
  _In_        UINT            dwWidth,
  _In_        UINT            dwHeight,
  _In_        FLOAT           fGutter,
  _In_        DWORD           dwTextureIndex,
  _In_  const DWORD           *pdwAdjacency,
        const DWORD           *pdwFalseEdges,
  _In_        FLOAT           *pfIMTArray,
  _In_        LPD3DXUVATLASCB pCallback,
  _In_        FLOAT           fCallbackFrequency,
  _In_        LPVOID          pUserContext,
  _In_        DWORD           dwOptions,
  _In_        LPD3DXMESH      *ppMeshOut,
  _Out_       LPD3DXBUFFER    *ppFacePartitioning,
  _Out_       LPD3DXBUFFER    *ppVertexRemapArray,
  _Out_       FLOAT           *pfMaxStretchOut,
  _Out_       UINT            *pdwNumChartsOut
);
```



## <a name="parameters"></a><span data-ttu-id="d13bd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d13bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d13bd-107">*pMesh* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d13bd-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d13bd-108">Type : **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="d13bd-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="d13bd-109">Pointeur vers un maillage d’entrée (voir [**ID3DXMesh**](id3dxmesh.md)) qui contient la géométrie de l’objet pour le calcul de l’Atlas.</span><span class="sxs-lookup"><span data-stu-id="d13bd-109">Pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the atlas.</span></span> <span data-ttu-id="d13bd-110">Au minimum, la maille doit contenir des données de position et des coordonnées de texture 2D.</span><span class="sxs-lookup"><span data-stu-id="d13bd-110">At a minimum, the mesh must contain position data and 2D texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="d13bd-111">*dwMaxChartNumber* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d13bd-111">*dwMaxChartNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d13bd-112">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d13bd-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d13bd-113">Nombre maximal de graphiques dans lesquels partitionner le maillage.</span><span class="sxs-lookup"><span data-stu-id="d13bd-113">The maximum number of charts to partition the mesh into.</span></span> <span data-ttu-id="d13bd-114">Consultez les remarques sur les modes de partitionnement.</span><span class="sxs-lookup"><span data-stu-id="d13bd-114">See remarks about the partitioning modes.</span></span> <span data-ttu-id="d13bd-115">Utilisez 0 pour indiquer à D3DX que l’Atlas doit être paramétré en fonction de Stretch.</span><span class="sxs-lookup"><span data-stu-id="d13bd-115">Use 0 to tell D3DX that the atlas should be parameterized based on stretch.</span></span>

</dd> <dt>

<span data-ttu-id="d13bd-116">*fMaxStretch* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d13bd-116">*fMaxStretch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d13bd-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d13bd-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d13bd-118">Quantité d’étirement autorisée.</span><span class="sxs-lookup"><span data-stu-id="d13bd-118">The amount of stretching allowed.</span></span> <span data-ttu-id="d13bd-119">0 signifie qu’aucun étirement n’est autorisé, 1 signifie qu’une quantité d’étirement peut être utilisée.</span><span class="sxs-lookup"><span data-stu-id="d13bd-119">0 means no stretching is allowed, 1 means any amount of stretching can be used.</span></span>

</dd> <dt>

<span data-ttu-id="d13bd-120">*dwWidth* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d13bd-120">*dwWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d13bd-121">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d13bd-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d13bd-122">Largeur de la texture.</span><span class="sxs-lookup"><span data-stu-id="d13bd-122">Texture width.</span></span>

</dd> <dt>

<span data-ttu-id="d13bd-123">*dwHeight* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d13bd-123">*dwHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d13bd-124">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d13bd-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d13bd-125">Hauteur de la texture.</span><span class="sxs-lookup"><span data-stu-id="d13bd-125">Texture height.</span></span>

</dd> <dt>

<span data-ttu-id="d13bd-126">*fGutter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d13bd-126">*fGutter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d13bd-127">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d13bd-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d13bd-128">Distance minimale, dans les texels, entre deux graphiques sur l’Atlas.</span><span class="sxs-lookup"><span data-stu-id="d13bd-128">The minimum distance, in texels, between two charts on the atlas.</span></span> <span data-ttu-id="d13bd-129">La reliure est toujours mise à l’échelle en largeur ; ainsi, si une marge de 2,5 est utilisée sur une texture 512 x 512, la distance minimale entre deux graphiques 2,5 est de/512,0.</span><span class="sxs-lookup"><span data-stu-id="d13bd-129">The gutter is always scaled by the width; so, if a gutter of 2.5 is used on a 512x512 texture, then the minimum distance between two charts is 2.5 / 512.0 texels.</span></span>

</dd> <dt>

<span data-ttu-id="d13bd-130">*dwTextureIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d13bd-130">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d13bd-131">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d13bd-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d13bd-132">Index de coordonnées de texture de base zéro qui identifie le jeu de coordonnées de texture à utiliser.</span><span class="sxs-lookup"><span data-stu-id="d13bd-132">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="d13bd-133">*pdwAdjacency* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d13bd-133">*pdwAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d13bd-134">Type : **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="d13bd-134">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d13bd-135">Pointeur vers un tableau de données d’adjacence.</span><span class="sxs-lookup"><span data-stu-id="d13bd-135">A pointer to an array of adjacency data.</span></span> <span data-ttu-id="d13bd-136">avec 3 DWORDs par face, indiquant quels triangles sont adjacents les uns aux autres (voir [**ID3DXBaseMesh :: GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).</span><span class="sxs-lookup"><span data-stu-id="d13bd-136">with 3 DWORDs per face, indicating which triangles are adjacent to each other (see [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).</span></span>

</dd> <dt>

<span data-ttu-id="d13bd-137">*pdwFalseEdges*</span><span class="sxs-lookup"><span data-stu-id="d13bd-137">*pdwFalseEdges*</span></span> 
</dt> <dd>

<span data-ttu-id="d13bd-138">Type : **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="d13bd-138">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d13bd-139">Tableau avec 3 DWORDs par face.</span><span class="sxs-lookup"><span data-stu-id="d13bd-139">An array with 3 DWORDS per face.</span></span> <span data-ttu-id="d13bd-140">Chaque visage indique si une arête est false ou non.</span><span class="sxs-lookup"><span data-stu-id="d13bd-140">Each face indicates if an edge is false or not.</span></span> <span data-ttu-id="d13bd-141">Un bord non-faux est indiqué par-1, un faux bord est indiqué par une autre valeur.</span><span class="sxs-lookup"><span data-stu-id="d13bd-141">A non-false edge is indicated by -1, a false edge is indicated by any other value.</span></span> <span data-ttu-id="d13bd-142">Cela permet le paramétrage d’une maille de quatre cœurs où les bords du milieu de chaque quadruple ne sont pas coupés.</span><span class="sxs-lookup"><span data-stu-id="d13bd-142">This enables the parameterization of a mesh of quads where the edges down the middle of each quad will not be cut.</span></span>

</dd> <dt>

<span data-ttu-id="d13bd-143">*pfIMTArray* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d13bd-143">*pfIMTArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d13bd-144">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d13bd-144">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d13bd-145">Pointeur vers un tableau de dizaines de métriques intégrés qui décrit comment étirer un triangle (voir [IntegratedMetricTensor](using-uvatlas.md)).</span><span class="sxs-lookup"><span data-stu-id="d13bd-145">A pointer to an array of integrated metric tensors that describes how to stretch a triangle (see [IntegratedMetricTensor](using-uvatlas.md)).</span></span>

</dd> <dt>

<span data-ttu-id="d13bd-146">*pCallback* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d13bd-146">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d13bd-147">Type : **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="d13bd-147">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="d13bd-148">Pointeur vers une fonction de rappel (voir [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) qui est utile pour surveiller la progression.</span><span class="sxs-lookup"><span data-stu-id="d13bd-148">A pointer to a callback function (see [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) that is useful for monitoring progress.</span></span>

</dd> <dt>

<span data-ttu-id="d13bd-149">*fCallbackFrequency* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d13bd-149">*fCallbackFrequency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d13bd-150">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d13bd-150">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d13bd-151">Spécifiez la fréquence à laquelle D3DX appellera le rappel. une valeur par défaut raisonnable est 0,0001 f.</span><span class="sxs-lookup"><span data-stu-id="d13bd-151">Specify how often D3DX will call the callback; a reasonable default value is 0.0001f.</span></span>

</dd> <dt>

<span data-ttu-id="d13bd-152">*pUserContent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d13bd-152">*pUserContent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d13bd-153">Type : **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d13bd-153">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d13bd-154">Pointeur vers une valeur définie par l’utilisateur qui est passée à la fonction de rappel ; généralement utilisé par une application pour passer un pointeur vers une structure de données qui fournit des informations de contexte pour la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="d13bd-154">Pointer to a user-defined value which is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="d13bd-155">*dwOptions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d13bd-155">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d13bd-156">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d13bd-156">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d13bd-157">Spécifiez la qualité des graphiques générés.</span><span class="sxs-lookup"><span data-stu-id="d13bd-157">Specify the quality of the charts generated.</span></span> <span data-ttu-id="d13bd-158">Consultez [**D3DXUVATLAS**](./d3dxuvatlas.md).</span><span class="sxs-lookup"><span data-stu-id="d13bd-158">See [**D3DXUVATLAS**](./d3dxuvatlas.md).</span></span>

</dd> <dt>

<span data-ttu-id="d13bd-159">*ppMeshOut* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d13bd-159">*ppMeshOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d13bd-160">Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="d13bd-160">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="d13bd-161">Pointeur vers la maille créée avec l’Atlas (voir [**ID3DXMesh**](id3dxmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="d13bd-161">Pointer to the created mesh with the atlas (see [**ID3DXMesh**](id3dxmesh.md)).</span></span>

</dd> <dt>

<span data-ttu-id="d13bd-162">*ppFacePartitioning* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d13bd-162">*ppFacePartitioning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d13bd-163">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="d13bd-163">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="d13bd-164">Pointeur vers un tableau des données de partitionnement de type final.</span><span class="sxs-lookup"><span data-stu-id="d13bd-164">A pointer to an array of the final face-partitioning data.</span></span> <span data-ttu-id="d13bd-165">Chaque élément contient un DWORD par face (voir [**ID3DXBuffer**](id3dxbuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="d13bd-165">Each element contains one DWORD per face (see [**ID3DXBuffer**](id3dxbuffer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="d13bd-166">*ppVertexRemapArray* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d13bd-166">*ppVertexRemapArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d13bd-167">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="d13bd-167">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="d13bd-168">Pointeur vers un tableau de vertex remappés.</span><span class="sxs-lookup"><span data-stu-id="d13bd-168">A pointer to an array of remapped vertices.</span></span> <span data-ttu-id="d13bd-169">Chaque élément de tableau identifie le vertex d’origine à partir duquel provient chaque vertex final (si le Vertex a été fractionné pendant le remappage).</span><span class="sxs-lookup"><span data-stu-id="d13bd-169">Each array element identifies the original vertex that each final vertex came from (if the vertex was split during remapping).</span></span> <span data-ttu-id="d13bd-170">Chaque élément de tableau contient une valeur DWORD par vertex.</span><span class="sxs-lookup"><span data-stu-id="d13bd-170">Each array element contains one DWORD per vertex.</span></span>

</dd> <dt>

<span data-ttu-id="d13bd-171">*pfMaxStretchOut* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d13bd-171">*pfMaxStretchOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d13bd-172">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d13bd-172">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d13bd-173">Pointeur vers la valeur d’étirement maximale générée par l’algorithme Atlas.</span><span class="sxs-lookup"><span data-stu-id="d13bd-173">A pointer to the maximum stretch value generated by the atlas algorithm.</span></span> <span data-ttu-id="d13bd-174">La plage est comprise entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="d13bd-174">The range is between 0.0 and 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="d13bd-175">*pdwNumChartsOut* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d13bd-175">*pdwNumChartsOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d13bd-176">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d13bd-176">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d13bd-177">Pointeur vers le nombre de graphiques créés par l’algorithme Atlas.</span><span class="sxs-lookup"><span data-stu-id="d13bd-177">A pointer to the number of charts created by the atlas algorithm.</span></span> <span data-ttu-id="d13bd-178">Si dwMaxChartNumber est trop faible, ce paramètre retourne le nombre minimal de graphiques requis pour créer un Atlas.</span><span class="sxs-lookup"><span data-stu-id="d13bd-178">If dwMaxChartNumber is too low, this parameter will return the minimum number of charts required to create an atlas.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d13bd-179">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d13bd-179">Return value</span></span>

<span data-ttu-id="d13bd-180">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d13bd-180">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d13bd-181">Si la fonction est réussie, la valeur de retour est D3D \_ OK ; sinon, la valeur est D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d13bd-181">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d13bd-182">Notes </span><span class="sxs-lookup"><span data-stu-id="d13bd-182">Remarks</span></span>

<span data-ttu-id="d13bd-183">D3DXUVAtlasCreate peut partitionner la géométrie de maille de deux manières :</span><span class="sxs-lookup"><span data-stu-id="d13bd-183">D3DXUVAtlasCreate can partition mesh geometry two ways:</span></span>

-   <span data-ttu-id="d13bd-184">En fonction du nombre de graphiques</span><span class="sxs-lookup"><span data-stu-id="d13bd-184">Based on the number of charts</span></span>
-   <span data-ttu-id="d13bd-185">Sur la base de l’étirement maximal autorisé.</span><span class="sxs-lookup"><span data-stu-id="d13bd-185">Based on the maximum allowed stretch.</span></span> <span data-ttu-id="d13bd-186">Si l’étirement maximal autorisé est 0, chaque triangle sera probablement dans son propre graphique.</span><span class="sxs-lookup"><span data-stu-id="d13bd-186">If the maximum allowed stretch is 0, each triangle will likely be in its own chart.</span></span>

## <a name="requirements"></a><span data-ttu-id="d13bd-187">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d13bd-187">Requirements</span></span>



| <span data-ttu-id="d13bd-188">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d13bd-188">Requirement</span></span> | <span data-ttu-id="d13bd-189">Valeur</span><span class="sxs-lookup"><span data-stu-id="d13bd-189">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d13bd-190">En-tête</span><span class="sxs-lookup"><span data-stu-id="d13bd-190">Header</span></span><br/>  | <dl> <span data-ttu-id="d13bd-191"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d13bd-191"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d13bd-192">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d13bd-192">Library</span></span><br/> | <dl> <span data-ttu-id="d13bd-193"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d13bd-193"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d13bd-194">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d13bd-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d13bd-195">UVAtlas, fonctions</span><span class="sxs-lookup"><span data-stu-id="d13bd-195">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

<span data-ttu-id="d13bd-196">[Outil Command-Line d’Atlas UV (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="d13bd-196">[UV Atlas Command-Line Tool (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 
