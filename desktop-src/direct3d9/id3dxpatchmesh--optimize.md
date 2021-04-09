---
description: Optimise le maillage des correctifs pour une polygonalisation efficace.
ms.assetid: 0049e649-5fe5-45b4-9b09-14b7f99b4988
title: 'ID3DXPatchMesh :: Optimize, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.Optimize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6fa66aadd0ef1f9f9f65747694fc311f80172449
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103954014"
---
# <a name="id3dxpatchmeshoptimize-method"></a><span data-ttu-id="b584b-103">ID3DXPatchMesh :: Optimize, méthode</span><span class="sxs-lookup"><span data-stu-id="b584b-103">ID3DXPatchMesh::Optimize method</span></span>

<span data-ttu-id="b584b-104">Optimise le maillage des correctifs pour une polygonalisation efficace.</span><span class="sxs-lookup"><span data-stu-id="b584b-104">Optimizes the patch mesh for efficient tessellation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b584b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b584b-105">Syntax</span></span>


```C++
HRESULT Optimize(
  [in] DWORD Flags
);
```



## <a name="parameters"></a><span data-ttu-id="b584b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b584b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b584b-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="b584b-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b584b-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b584b-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b584b-109">Actuellement inutilisé.</span><span class="sxs-lookup"><span data-stu-id="b584b-109">Currently unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b584b-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b584b-110">Return value</span></span>

<span data-ttu-id="b584b-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b584b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b584b-112">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b584b-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b584b-113">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ CANNOTATTRSORT.</span><span class="sxs-lookup"><span data-stu-id="b584b-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_CANNOTATTRSORT.</span></span>

## <a name="remarks"></a><span data-ttu-id="b584b-114">Notes</span><span class="sxs-lookup"><span data-stu-id="b584b-114">Remarks</span></span>

<span data-ttu-id="b584b-115">Une fois qu’une application a généré des informations d’adjacence pour une maille, les données de maillage peuvent être optimisées (réorganisées) pour améliorer les performances de dessin.</span><span class="sxs-lookup"><span data-stu-id="b584b-115">After an application generates adjacency information for a mesh, the mesh data can be optimized (reordered) for better drawing performance.</span></span> <span data-ttu-id="b584b-116">Cette méthode détermine les correctifs adjacents (dans la tolérance fournie).</span><span class="sxs-lookup"><span data-stu-id="b584b-116">This method determines which patches are adjacent (within the provided tolerance).</span></span>

<span data-ttu-id="b584b-117">Les informations d’contiguïté sont également utilisées pour optimiser la pavage.</span><span class="sxs-lookup"><span data-stu-id="b584b-117">Adjacency information is also used to optimize tessellation.</span></span> <span data-ttu-id="b584b-118">Générez des informations d’adjacence une fois et paver à plusieurs reprises en appelant [**ID3DXPatchMesh :: paver**](id3dxpatchmesh--tessellate.md).</span><span class="sxs-lookup"><span data-stu-id="b584b-118">Generate adjacency information once and tessellate repeatedly by calling [**ID3DXPatchMesh::Tessellate**](id3dxpatchmesh--tessellate.md).</span></span> <span data-ttu-id="b584b-119">L’optimisation effectuée est indépendante du niveau de pavage réel utilisé.</span><span class="sxs-lookup"><span data-stu-id="b584b-119">The optimization performed is independent of the actual tessellation level used.</span></span> <span data-ttu-id="b584b-120">Toutefois, si les vertex de maillage sont modifiés, vous devez régénérer les informations d’adjacence.</span><span class="sxs-lookup"><span data-stu-id="b584b-120">However, if the mesh vertices are changed, you must regenerate the adjacency information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b584b-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b584b-121">Requirements</span></span>



| <span data-ttu-id="b584b-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b584b-122">Requirement</span></span> | <span data-ttu-id="b584b-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="b584b-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b584b-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="b584b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b584b-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b584b-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b584b-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b584b-126">Library</span></span><br/> | <dl> <span data-ttu-id="b584b-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b584b-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b584b-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b584b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b584b-129">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="b584b-129">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> <dt>

[<span data-ttu-id="b584b-130">**ID3DXPatchMesh::GenerateAdjacency**</span><span class="sxs-lookup"><span data-stu-id="b584b-130">**ID3DXPatchMesh::GenerateAdjacency**</span></span>](id3dxpatchmesh--generateadjacency.md)
</dt> </dl>

 

 
