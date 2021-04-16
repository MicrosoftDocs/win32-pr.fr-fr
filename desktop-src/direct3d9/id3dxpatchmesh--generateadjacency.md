---
description: Générez une liste de bords de maillage et les correctifs qui partagent chaque périphérie.
ms.assetid: 024528c0-2c0d-4448-9b38-05cf8d6ffc63
title: 'ID3DXPatchMesh :: GenerateAdjacency, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GenerateAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 68de2a77b9d27391c57ec299ceb87d29166ee248
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394067"
---
# <a name="id3dxpatchmeshgenerateadjacency-method"></a><span data-ttu-id="419ed-103">ID3DXPatchMesh :: GenerateAdjacency, méthode</span><span class="sxs-lookup"><span data-stu-id="419ed-103">ID3DXPatchMesh::GenerateAdjacency method</span></span>

<span data-ttu-id="419ed-104">Générez une liste de bords de maillage et les correctifs qui partagent chaque périphérie.</span><span class="sxs-lookup"><span data-stu-id="419ed-104">Generate a list of mesh edges and the patches that share each edge.</span></span>

## <a name="syntax"></a><span data-ttu-id="419ed-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="419ed-105">Syntax</span></span>


```C++
HRESULT GenerateAdjacency(
  [in] FLOAT fTolerance
);
```



## <a name="parameters"></a><span data-ttu-id="419ed-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="419ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="419ed-107">*fTolerance* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="419ed-107">*fTolerance* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="419ed-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="419ed-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="419ed-109">Spécifie que les vertex qui diffèrent d’une position inférieure à la tolérance doivent être traités comme coïncidents.</span><span class="sxs-lookup"><span data-stu-id="419ed-109">Specifies that vertices that differ in position by less than the tolerance should be treated as coincident.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="419ed-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="419ed-110">Return value</span></span>

<span data-ttu-id="419ed-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="419ed-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="419ed-112">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="419ed-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="419ed-113">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="419ed-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="419ed-114">Notes</span><span class="sxs-lookup"><span data-stu-id="419ed-114">Remarks</span></span>

<span data-ttu-id="419ed-115">Une fois qu’une application a généré des informations d’adjacence pour une maille, les données de maillage peuvent être optimisées pour améliorer les performances de dessin.</span><span class="sxs-lookup"><span data-stu-id="419ed-115">After an application generates adjacency information for a mesh, the mesh data can be optimized for better drawing performance.</span></span> <span data-ttu-id="419ed-116">Cette méthode détermine les correctifs adjacents (dans la tolérance fournie).</span><span class="sxs-lookup"><span data-stu-id="419ed-116">This method determines which patches are adjacent (within the provided tolerance).</span></span> <span data-ttu-id="419ed-117">Ces informations sont utilisées en interne pour optimiser le pavage.</span><span class="sxs-lookup"><span data-stu-id="419ed-117">This information is used internally to optimize tessellation.</span></span>

## <a name="requirements"></a><span data-ttu-id="419ed-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="419ed-118">Requirements</span></span>



| <span data-ttu-id="419ed-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="419ed-119">Requirement</span></span> | <span data-ttu-id="419ed-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="419ed-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="419ed-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="419ed-121">Header</span></span><br/>  | <dl> <span data-ttu-id="419ed-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="419ed-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="419ed-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="419ed-123">Library</span></span><br/> | <dl> <span data-ttu-id="419ed-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="419ed-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="419ed-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="419ed-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="419ed-126">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="419ed-126">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> <dt>

[<span data-ttu-id="419ed-127">**ID3DXPatchMesh :: Optimize**</span><span class="sxs-lookup"><span data-stu-id="419ed-127">**ID3DXPatchMesh::Optimize**</span></span>](id3dxpatchmesh--optimize.md)
</dt> </dl>

 

 
