---
description: Génère un maillage avec des faces et des sommets réorganisés pour optimiser les performances du dessin. Cette méthode réorganise la maille existante.
ms.assetid: 2cdaf627-d1d3-44f0-a5ae-9023d4b0de45
title: 'ID3DXMesh :: OptimizeInplace, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.OptimizeInplace
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f889e0d3754cc1321ffa59eba294038b87991489
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762302"
---
# <a name="id3dxmeshoptimizeinplace-method"></a><span data-ttu-id="ad2c9-104">ID3DXMesh :: OptimizeInplace, méthode</span><span class="sxs-lookup"><span data-stu-id="ad2c9-104">ID3DXMesh::OptimizeInplace method</span></span>

<span data-ttu-id="ad2c9-105">Génère un maillage avec des faces et des sommets réorganisés pour optimiser les performances du dessin.</span><span class="sxs-lookup"><span data-stu-id="ad2c9-105">Generates a mesh with reordered faces and vertices to optimize drawing performance.</span></span> <span data-ttu-id="ad2c9-106">Cette méthode réorganise la maille existante.</span><span class="sxs-lookup"><span data-stu-id="ad2c9-106">This method reorders the existing mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad2c9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad2c9-107">Syntax</span></span>


```C++
HRESULT OptimizeInplace(
  [in]        DWORD        Flags,
  [in]  const DWORD        *pAdjacencyIn,
  [out]       DWORD        *pAdjacencyOut,
  [out]       DWORD        *pFaceRemap,
  [out]       LPD3DXBUFFER *ppVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="ad2c9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ad2c9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad2c9-109">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="ad2c9-109">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad2c9-110">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ad2c9-110">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ad2c9-111">Combinaison d’un ou plusieurs indicateurs [**D3DXMESHOPT**](./d3dxmeshopt.md) , en spécifiant le type d’optimisation à effectuer.</span><span class="sxs-lookup"><span data-stu-id="ad2c9-111">Combination of one or more [**D3DXMESHOPT**](./d3dxmeshopt.md) flags, specifying the type of optimization to perform.</span></span>

</dd> <dt>

<span data-ttu-id="ad2c9-112">*pAdjacencyIn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ad2c9-112">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad2c9-113">Type : **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="ad2c9-113">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ad2c9-114">Pointeur vers un tableau de trois DWORD par visage qui spécifie les trois voisins pour chaque visage dans le maillage source.</span><span class="sxs-lookup"><span data-stu-id="ad2c9-114">Pointer to an array of three DWORDs per face that specifies the three neighbors for each face in the source mesh.</span></span> <span data-ttu-id="ad2c9-115">Si le bord n’a pas de faces adjacentes, la valeur est 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="ad2c9-115">If the edge has no adjacent faces, the value is 0xffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="ad2c9-116">*pAdjacencyOut* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ad2c9-116">*pAdjacencyOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad2c9-117">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ad2c9-117">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ad2c9-118">Pointeur vers un tableau de trois DWORD par visage qui spécifie les trois voisins pour chaque visage dans le maillage optimisé.</span><span class="sxs-lookup"><span data-stu-id="ad2c9-118">Pointer to an array of three DWORDs per face that specifies the three neighbors for each face in the optimized mesh.</span></span> <span data-ttu-id="ad2c9-119">Si le bord n’a pas de faces adjacentes, la valeur est 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="ad2c9-119">If the edge has no adjacent faces, the value is 0xffffffff.</span></span> <span data-ttu-id="ad2c9-120">Si la valeur fournie pour cet argument est **null**, les données d’contiguïté ne sont pas retournées.</span><span class="sxs-lookup"><span data-stu-id="ad2c9-120">If the value supplied for this argument is **NULL**, adjacency data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="ad2c9-121">*pFaceRemap* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ad2c9-121">*pFaceRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad2c9-122">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ad2c9-122">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ad2c9-123">Tableau de DWORDs, un par visage, qui identifie la face d’origine du maillage qui correspond à chaque visage dans le maillage optimisé.</span><span class="sxs-lookup"><span data-stu-id="ad2c9-123">An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the optimized mesh.</span></span> <span data-ttu-id="ad2c9-124">Si la valeur fournie pour cet argument est **null**, les données de remappage de visage ne sont pas retournées.</span><span class="sxs-lookup"><span data-stu-id="ad2c9-124">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="ad2c9-125">*ppVertexRemap* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ad2c9-125">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad2c9-126">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="ad2c9-126">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="ad2c9-127">Adresse d’un pointeur vers une interface [**ID3DXBuffer**](id3dxbuffer.md) , qui contient une valeur DWORD pour chaque vertex qui spécifie la façon dont les nouveaux vertex sont mappés aux anciens vertex.</span><span class="sxs-lookup"><span data-stu-id="ad2c9-127">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="ad2c9-128">Ce remappage est utile si vous devez modifier des données externes en fonction du nouveau mappage de vertex.</span><span class="sxs-lookup"><span data-stu-id="ad2c9-128">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span> <span data-ttu-id="ad2c9-129">Si la valeur fournie pour cet argument est **null**, les données de remappage de vertex ne sont pas retournées.</span><span class="sxs-lookup"><span data-stu-id="ad2c9-129">If the value supplied for this argument is **NULL**, vertex remap data is not returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad2c9-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ad2c9-130">Return value</span></span>

<span data-ttu-id="ad2c9-131">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ad2c9-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ad2c9-132">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ad2c9-132">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ad2c9-133">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ CANNOTATTRSORT, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ad2c9-133">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_CANNOTATTRSORT, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad2c9-134">Notes</span><span class="sxs-lookup"><span data-stu-id="ad2c9-134">Remarks</span></span>

<span data-ttu-id="ad2c9-135">Avant d’exécuter **ID3DXMesh :: OptimizeInplace**, une application doit générer une mémoire tampon de contiguïté en appelant [**ID3DXBaseMesh :: GenerateAdjacency**](id3dxbasemesh--generateadjacency.md).</span><span class="sxs-lookup"><span data-stu-id="ad2c9-135">Before running **ID3DXMesh::OptimizeInplace**, an application must generate an adjacency buffer by calling [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md).</span></span> <span data-ttu-id="ad2c9-136">La mémoire tampon d’adjacence contient des données d’contiguïté, telles qu’une liste de bords et les faces adjacentes les unes aux autres.</span><span class="sxs-lookup"><span data-stu-id="ad2c9-136">The adjacency buffer contains adjacency data, such as a list of edges and the faces that are adjacent to each other.</span></span>

> [!Note]  
> <span data-ttu-id="ad2c9-137">Cette méthode échoue si le maillage partage sa mémoire tampon de vertex avec un autre maillage, sauf si le \_ IGNOREVERTS D3DXMESHOPT est défini dans Flags.</span><span class="sxs-lookup"><span data-stu-id="ad2c9-137">This method will fail if the mesh is sharing its vertex buffer with another mesh, unless the D3DXMESHOPT\_IGNOREVERTS is set in Flags.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ad2c9-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad2c9-138">Requirements</span></span>



| <span data-ttu-id="ad2c9-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad2c9-139">Requirement</span></span> | <span data-ttu-id="ad2c9-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad2c9-140">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad2c9-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="ad2c9-141">Header</span></span><br/>  | <dl> <span data-ttu-id="ad2c9-142"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad2c9-142"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ad2c9-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ad2c9-143">Library</span></span><br/> | <dl> <span data-ttu-id="ad2c9-144"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad2c9-144"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ad2c9-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad2c9-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad2c9-146">ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="ad2c9-146">ID3DXMesh</span></span>](id3dxmesh.md)
</dt> <dt>

[<span data-ttu-id="ad2c9-147">**ID3DXMesh :: Optimize**</span><span class="sxs-lookup"><span data-stu-id="ad2c9-147">**ID3DXMesh::Optimize**</span></span>](id3dxmesh--optimize.md)
</dt> </dl>

 

 
