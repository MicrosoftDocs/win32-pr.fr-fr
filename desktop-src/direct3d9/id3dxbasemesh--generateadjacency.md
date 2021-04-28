---
description: 'ID3DXBaseMesh :: GenerateAdjacency, méthode-générer une liste de bords de maillage, ainsi qu’une liste des visages qui partagent chaque bord.'
ms.assetid: 9d52290f-1c9e-43a7-b239-35cd54e36466
title: 'ID3DXBaseMesh :: GenerateAdjacency, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GenerateAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 783ed7ad61337e606793b9b467e4b17fddd7ecd2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115457"
---
# <a name="id3dxbasemeshgenerateadjacency-method"></a><span data-ttu-id="7927c-103">ID3DXBaseMesh :: GenerateAdjacency, méthode</span><span class="sxs-lookup"><span data-stu-id="7927c-103">ID3DXBaseMesh::GenerateAdjacency method</span></span>

<span data-ttu-id="7927c-104">Générez une liste de contours de maillage, ainsi qu’une liste des visages qui partagent chaque arête.</span><span class="sxs-lookup"><span data-stu-id="7927c-104">Generate a list of mesh edges, as well as a list of faces that share each edge.</span></span>

## <a name="syntax"></a><span data-ttu-id="7927c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7927c-105">Syntax</span></span>


```C++
HRESULT GenerateAdjacency(
  [in] FLOAT Epsilon,
  [in] DWORD *pAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="7927c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7927c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7927c-107">*Epsilon* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7927c-107">*Epsilon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7927c-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7927c-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7927c-109">Spécifie que les vertex qui diffèrent de la position par moins de Epsilon doivent être traités comme coïncidents.</span><span class="sxs-lookup"><span data-stu-id="7927c-109">Specifies that vertices that differ in position by less than epsilon should be treated as coincident.</span></span>

</dd> <dt>

<span data-ttu-id="7927c-110">*pAdjacency* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7927c-110">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7927c-111">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7927c-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7927c-112">Pointeur vers un tableau de trois DWORDs par visage à remplir avec les index des visages adjacents.</span><span class="sxs-lookup"><span data-stu-id="7927c-112">Pointer to an array of three DWORDs per face to be filled with the indices of adjacent faces.</span></span> <span data-ttu-id="7927c-113">Le nombre d’octets dans ce tableau doit être au moins égal à 3 \* [**ID3DXBaseMesh :: GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD).</span><span class="sxs-lookup"><span data-stu-id="7927c-113">The number of bytes in this array must be at least 3 \* [**ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7927c-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7927c-114">Return value</span></span>

<span data-ttu-id="7927c-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7927c-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7927c-116">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7927c-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7927c-117">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="7927c-117">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="7927c-118">Notes </span><span class="sxs-lookup"><span data-stu-id="7927c-118">Remarks</span></span>

<span data-ttu-id="7927c-119">Une fois qu’une application a généré des informations d’adjacence pour une maille, les données de maillage peuvent être optimisées pour améliorer les performances de dessin.</span><span class="sxs-lookup"><span data-stu-id="7927c-119">After an application generates adjacency information for a mesh, the mesh data can be optimized for better drawing performance.</span></span>

<span data-ttu-id="7927c-120">L’ordre des entrées dans la mémoire tampon d’adjacence est déterminé par l’ordre des index de vertex dans le tampon d’index.</span><span class="sxs-lookup"><span data-stu-id="7927c-120">The order of the entries in the adjacency buffer is determined by the order of the vertex indices in the index buffer.</span></span> <span data-ttu-id="7927c-121">Le triangle adjacent 0 correspond toujours au bord entre les index des angles 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="7927c-121">The adjacent triangle 0 always corresponds to the edge between the indices of the corners 0 and 1.</span></span> <span data-ttu-id="7927c-122">Le triangle 1 adjacent correspond toujours au bord entre les index des angles 1 et 2, tandis que le triangle 2 adjacent correspond au bord entre les index des angles 2 et 0.</span><span class="sxs-lookup"><span data-stu-id="7927c-122">The adjacent triangle 1 always corresponds to the edge between the indices of the corners 1 and 2 while the adjacent triangle 2 corresponds to the edge between the indices of the corners 2 and 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="7927c-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7927c-123">Requirements</span></span>



| <span data-ttu-id="7927c-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7927c-124">Requirement</span></span> | <span data-ttu-id="7927c-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="7927c-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7927c-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="7927c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="7927c-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="7927c-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="7927c-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7927c-128">Library</span></span><br/> | <dl> <span data-ttu-id="7927c-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7927c-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7927c-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7927c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7927c-131">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="7927c-131">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="7927c-132">**ID3DXMesh :: Optimize**</span><span class="sxs-lookup"><span data-stu-id="7927c-132">**ID3DXMesh::Optimize**</span></span>](id3dxmesh--optimize.md)
</dt> <dt>

[<span data-ttu-id="7927c-133">**ID3DXMesh::OptimizeInplace**</span><span class="sxs-lookup"><span data-stu-id="7927c-133">**ID3DXMesh::OptimizeInplace**</span></span>](id3dxmesh--optimizeinplace.md)
</dt> </dl>

 

 
