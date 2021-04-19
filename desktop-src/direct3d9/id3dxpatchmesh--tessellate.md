---
description: Effectue un pavage uniforme basé sur le niveau de pavage.
ms.assetid: 0fc701b4-0636-450e-b8e0-e7a490871316
title: 'ID3DXPatchMesh :: paver, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.Tessellate
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b94b79a9decd2f44fa1675e257a2401e2ae8f7a6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522397"
---
# <a name="id3dxpatchmeshtessellate-method"></a><span data-ttu-id="8b8df-103">ID3DXPatchMesh :: paver, méthode</span><span class="sxs-lookup"><span data-stu-id="8b8df-103">ID3DXPatchMesh::Tessellate method</span></span>

<span data-ttu-id="8b8df-104">Effectue un pavage uniforme basé sur le niveau de pavage.</span><span class="sxs-lookup"><span data-stu-id="8b8df-104">Performs uniform tessellation based on the tessellation level.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b8df-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b8df-105">Syntax</span></span>


```C++
HRESULT Tessellate(
  [in] FLOAT      fTessLevel,
  [in] LPD3DXMESH pMesh
);
```



## <a name="parameters"></a><span data-ttu-id="8b8df-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b8df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b8df-107">*fTessLevel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8b8df-107">*fTessLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b8df-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8b8df-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8b8df-109">Niveau de pavage.</span><span class="sxs-lookup"><span data-stu-id="8b8df-109">Tessellation level.</span></span> <span data-ttu-id="8b8df-110">Il s’agit du nombre de vertex introduits entre les vertex existants.</span><span class="sxs-lookup"><span data-stu-id="8b8df-110">This is the number of vertices introduced between existing vertices.</span></span> <span data-ttu-id="8b8df-111">La plage de ce paramètre float est 0 < fTessLevel <= 32.</span><span class="sxs-lookup"><span data-stu-id="8b8df-111">The range of this float parameter is 0 < fTessLevel <= 32.</span></span>

</dd> <dt>

<span data-ttu-id="8b8df-112">*pMesh* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8b8df-112">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b8df-113">Type : **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="8b8df-113">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="8b8df-114">Maillage fractionné résultant.</span><span class="sxs-lookup"><span data-stu-id="8b8df-114">Resulting tessellated mesh.</span></span> <span data-ttu-id="8b8df-115">Consultez [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="8b8df-115">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b8df-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8b8df-116">Return value</span></span>

<span data-ttu-id="8b8df-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8b8df-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8b8df-118">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8b8df-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8b8df-119">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="8b8df-119">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b8df-120">Notes</span><span class="sxs-lookup"><span data-stu-id="8b8df-120">Remarks</span></span>

<span data-ttu-id="8b8df-121">Cette fonction s’exécute plus efficacement si la maille de correctifs a été optimisée à l’aide de [**ID3DXPatchMesh :: Optimize**](id3dxpatchmesh--optimize.md).</span><span class="sxs-lookup"><span data-stu-id="8b8df-121">This function will perform more efficiently if the patch mesh has been optimized using [**ID3DXPatchMesh::Optimize**](id3dxpatchmesh--optimize.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8b8df-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b8df-122">Requirements</span></span>



| <span data-ttu-id="8b8df-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8b8df-123">Requirement</span></span> | <span data-ttu-id="8b8df-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b8df-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b8df-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="8b8df-125">Header</span></span><br/>  | <dl> <span data-ttu-id="8b8df-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b8df-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8b8df-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8b8df-127">Library</span></span><br/> | <dl> <span data-ttu-id="8b8df-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b8df-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8b8df-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b8df-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b8df-130">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="8b8df-130">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
