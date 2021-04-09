---
description: Génère un nouveau maillage avec des faces et des sommets réorganisés pour optimiser les performances du dessin.
ms.assetid: 6a9bf7b9-2cb9-4b42-92d9-2a121ff79284
title: 'ID3DXMesh :: Optimize, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.Optimize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7752e08236094d7038a5e77ac1a679f787305022
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103954018"
---
# <a name="id3dxmeshoptimize-method"></a><span data-ttu-id="46b1a-103">ID3DXMesh :: Optimize, méthode</span><span class="sxs-lookup"><span data-stu-id="46b1a-103">ID3DXMesh::Optimize method</span></span>

<span data-ttu-id="46b1a-104">Génère un nouveau maillage avec des faces et des sommets réorganisés pour optimiser les performances du dessin.</span><span class="sxs-lookup"><span data-stu-id="46b1a-104">Generates a new mesh with reordered faces and vertices to optimize drawing performance.</span></span>

## <a name="syntax"></a><span data-ttu-id="46b1a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46b1a-105">Syntax</span></span>


```C++
HRESULT Optimize(
  [in]            DWORD        Flags,
  [in]      const DWORD        *pAdjacencyIn,
  [in, out]       DWORD        *pAdjacencyOut,
  [in, out]       DWORD        *pFaceRemap,
  [out]           LPD3DXBUFFER *ppVertexRemap,
  [out]           LPD3DXMESH   *ppOptMesh
);
```



## <a name="parameters"></a><span data-ttu-id="46b1a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="46b1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46b1a-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="46b1a-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46b1a-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46b1a-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46b1a-109">Spécifie le type d’optimisation à effectuer.</span><span class="sxs-lookup"><span data-stu-id="46b1a-109">Specifies the type of optimization to perform.</span></span> <span data-ttu-id="46b1a-110">Ce paramètre peut être défini sur une combinaison d’un ou plusieurs indicateurs de [**D3DXMESHOPT**](./d3dxmeshopt.md) et [**D3DXMESH**](./d3dxmesh.md) (à l’exception de D3DXMESH \_ 32 bits, D3DXMESH \_ IB \_ WriteOnly et D3DXMESH \_ WRITEONLY).</span><span class="sxs-lookup"><span data-stu-id="46b1a-110">This parameter can be set to a combination of one or more flags from [**D3DXMESHOPT**](./d3dxmeshopt.md) and [**D3DXMESH**](./d3dxmesh.md) (except D3DXMESH\_32BIT, D3DXMESH\_IB\_WRITEONLY, and D3DXMESH\_WRITEONLY).</span></span>

</dd> <dt>

<span data-ttu-id="46b1a-111">*pAdjacencyIn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="46b1a-111">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46b1a-112">Type : **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="46b1a-112">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="46b1a-113">Pointeur vers un tableau de trois DWORD par visage qui spécifie les trois voisins pour chaque visage dans le maillage source.</span><span class="sxs-lookup"><span data-stu-id="46b1a-113">Pointer to an array of three DWORDs per face that specifies the three neighbors for each face in the source mesh.</span></span> <span data-ttu-id="46b1a-114">Si le bord n’a pas de faces adjacentes, la valeur est 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="46b1a-114">If the edge has no adjacent faces, the value is 0xffffffff.</span></span> <span data-ttu-id="46b1a-115">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="46b1a-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="46b1a-116">*pAdjacencyOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="46b1a-116">*pAdjacencyOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="46b1a-117">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="46b1a-117">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="46b1a-118">Pointeur vers un tableau de trois DWORD par visage qui spécifie les trois voisins pour chaque visage dans le maillage optimisé.</span><span class="sxs-lookup"><span data-stu-id="46b1a-118">Pointer to an array of three DWORDs per face that specifies the three neighbors for each face in the optimized mesh.</span></span> <span data-ttu-id="46b1a-119">Si le bord n’a pas de faces adjacentes, la valeur est 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="46b1a-119">If the edge has no adjacent faces, the value is 0xffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="46b1a-120">*pFaceRemap* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="46b1a-120">*pFaceRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="46b1a-121">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="46b1a-121">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="46b1a-122">Tableau de DWORDs, un par visage, qui identifie la face d’origine du maillage qui correspond à chaque visage dans le maillage optimisé.</span><span class="sxs-lookup"><span data-stu-id="46b1a-122">An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the optimized mesh.</span></span> <span data-ttu-id="46b1a-123">Si la valeur fournie pour cet argument est **null**, les données de remappage de visage ne sont pas retournées.</span><span class="sxs-lookup"><span data-stu-id="46b1a-123">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="46b1a-124">*ppVertexRemap* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="46b1a-124">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46b1a-125">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="46b1a-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="46b1a-126">Adresse d’un pointeur vers une interface [**ID3DXBuffer**](id3dxbuffer.md) , qui contient une valeur DWORD pour chaque vertex qui spécifie la façon dont les nouveaux vertex sont mappés aux anciens vertex.</span><span class="sxs-lookup"><span data-stu-id="46b1a-126">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="46b1a-127">Ce remappage est utile si vous devez modifier des données externes en fonction du nouveau mappage de vertex.</span><span class="sxs-lookup"><span data-stu-id="46b1a-127">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span>

</dd> <dt>

<span data-ttu-id="46b1a-128">*ppOptMesh* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="46b1a-128">*ppOptMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46b1a-129">Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="46b1a-129">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="46b1a-130">Adresse d’un pointeur vers une interface [**ID3DXMesh**](id3dxmesh.md) , représentant la maille optimisée.</span><span class="sxs-lookup"><span data-stu-id="46b1a-130">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the optimized mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46b1a-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="46b1a-131">Return value</span></span>

<span data-ttu-id="46b1a-132">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="46b1a-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="46b1a-133">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="46b1a-133">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="46b1a-134">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="46b1a-134">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="46b1a-135">Notes</span><span class="sxs-lookup"><span data-stu-id="46b1a-135">Remarks</span></span>

<span data-ttu-id="46b1a-136">Cette méthode génère un nouveau maillage.</span><span class="sxs-lookup"><span data-stu-id="46b1a-136">This method generates a new mesh.</span></span> <span data-ttu-id="46b1a-137">Avant d’exécuter Optimize, une application doit générer une mémoire tampon de contiguïté en appelant [**ID3DXBaseMesh :: GenerateAdjacency**](id3dxbasemesh--generateadjacency.md).</span><span class="sxs-lookup"><span data-stu-id="46b1a-137">Before running Optimize, an application must generate an adjacency buffer by calling [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md).</span></span> <span data-ttu-id="46b1a-138">La mémoire tampon d’adjacence contient des données d’contiguïté, telles qu’une liste de bords et les faces adjacentes les unes aux autres.</span><span class="sxs-lookup"><span data-stu-id="46b1a-138">The adjacency buffer contains adjacency data, such as a list of edges and the faces that are adjacent to each other.</span></span>

<span data-ttu-id="46b1a-139">Cette méthode est très similaire à la méthode [**ID3DXBaseMesh :: CloneMesh**](id3dxbasemesh--clonemesh.md) , à ceci près qu’elle peut effectuer une optimisation lors de la génération du nouveau clone de la maille.</span><span class="sxs-lookup"><span data-stu-id="46b1a-139">This method is very similar to the [**ID3DXBaseMesh::CloneMesh**](id3dxbasemesh--clonemesh.md) method, except that it can perform optimization while generating the new clone of the mesh.</span></span> <span data-ttu-id="46b1a-140">Le maillage de sortie hérite de tous les paramètres de création du maillage d’entrée.</span><span class="sxs-lookup"><span data-stu-id="46b1a-140">The output mesh inherits all of the creation parameters of the input mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="46b1a-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46b1a-141">Requirements</span></span>



| <span data-ttu-id="46b1a-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46b1a-142">Requirement</span></span> | <span data-ttu-id="46b1a-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="46b1a-143">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="46b1a-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="46b1a-144">Header</span></span><br/>  | <dl> <span data-ttu-id="46b1a-145"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="46b1a-145"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="46b1a-146">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="46b1a-146">Library</span></span><br/> | <dl> <span data-ttu-id="46b1a-147"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46b1a-147"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="46b1a-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46b1a-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46b1a-149">ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="46b1a-149">ID3DXMesh</span></span>](id3dxmesh.md)
</dt> <dt>

[<span data-ttu-id="46b1a-150">**ID3DXMesh::OptimizeInplace**</span><span class="sxs-lookup"><span data-stu-id="46b1a-150">**ID3DXMesh::OptimizeInplace**</span></span>](id3dxmesh--optimizeinplace.md)
</dt> </dl>

 

 
