---
description: Effectue un pavage adaptatif basé sur le critère de pavage adaptative basé sur z.
ms.assetid: 9f8f5c18-e866-4893-ba07-2a3c0d26c028
title: 'ID3DXPatchMesh :: TessellateAdaptive, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.TessellateAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e4cc6c6b7ff7b0cdb99e56386df49529f26c9166
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539899"
---
# <a name="id3dxpatchmeshtessellateadaptive-method"></a><span data-ttu-id="217c3-103">ID3DXPatchMesh :: TessellateAdaptive, méthode</span><span class="sxs-lookup"><span data-stu-id="217c3-103">ID3DXPatchMesh::TessellateAdaptive method</span></span>

<span data-ttu-id="217c3-104">Effectue un pavage adaptatif basé sur le critère de pavage adaptative basé sur z.</span><span class="sxs-lookup"><span data-stu-id="217c3-104">Performs adaptive tessellation based on the z-based adaptive tessellation criterion.</span></span>

## <a name="syntax"></a><span data-ttu-id="217c3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="217c3-105">Syntax</span></span>


```C++
HRESULT TessellateAdaptive(
  [in] const D3DXVECTOR4 *pTrans,
  [in]       DWORD       dwMaxTessLevel,
  [in]       DWORD       dwMinTessLevel,
  [in]       LPD3DXMESH  pMesh
);
```



## <a name="parameters"></a><span data-ttu-id="217c3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="217c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="217c3-107">*pTrans* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="217c3-107">*pTrans* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="217c3-108">Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="217c3-108">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="217c3-109">Spécifie un vecteur 4D avec points avec les sommets pour obtenir la quantité de pavage adaptative par vertex.</span><span class="sxs-lookup"><span data-stu-id="217c3-109">Specifies a 4D vector that is dotted with the vertices to get the per-vertex adaptive tessellation amount.</span></span> <span data-ttu-id="217c3-110">Chaque bord est fractionné sur la valeur moyenne des niveaux de pavage pour les deux vertex qu’il connecte.</span><span class="sxs-lookup"><span data-stu-id="217c3-110">Each edge is tessellated to the average value of the tessellation levels for the two vertices it connects.</span></span>

</dd> <dt>

<span data-ttu-id="217c3-111">*dwMaxTessLevel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="217c3-111">*dwMaxTessLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="217c3-112">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="217c3-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="217c3-113">Limite maximale pour le pavage adaptatif.</span><span class="sxs-lookup"><span data-stu-id="217c3-113">Maximum limit for adaptive tessellation.</span></span> <span data-ttu-id="217c3-114">Il s’agit du nombre de vertex introduits entre les vertex existants.</span><span class="sxs-lookup"><span data-stu-id="217c3-114">This is the number of vertices introduced between existing vertices.</span></span> <span data-ttu-id="217c3-115">Cette valeur entière peut être comprise entre 1 et 32 inclus.</span><span class="sxs-lookup"><span data-stu-id="217c3-115">This integer value can range from 1 to 32, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="217c3-116">*dwMinTessLevel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="217c3-116">*dwMinTessLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="217c3-117">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="217c3-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="217c3-118">Limite minimale pour le pavage adaptatif.</span><span class="sxs-lookup"><span data-stu-id="217c3-118">Minimum limit for adaptive tessellation.</span></span> <span data-ttu-id="217c3-119">Il s’agit du nombre de vertex introduits entre les vertex existants.</span><span class="sxs-lookup"><span data-stu-id="217c3-119">This is the number of vertices introduced between existing vertices.</span></span> <span data-ttu-id="217c3-120">Cette valeur entière peut être comprise entre 1 et 32 inclus.</span><span class="sxs-lookup"><span data-stu-id="217c3-120">This integer value can range from 1 to 32, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="217c3-121">*pMesh* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="217c3-121">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="217c3-122">Type : **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="217c3-122">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="217c3-123">Maillage fractionné résultant.</span><span class="sxs-lookup"><span data-stu-id="217c3-123">Resulting tessellated mesh.</span></span> <span data-ttu-id="217c3-124">Consultez [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="217c3-124">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="217c3-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="217c3-125">Return value</span></span>

<span data-ttu-id="217c3-126">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="217c3-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="217c3-127">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="217c3-127">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="217c3-128">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="217c3-128">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="217c3-129">Notes</span><span class="sxs-lookup"><span data-stu-id="217c3-129">Remarks</span></span>

<span data-ttu-id="217c3-130">Cette fonction s’exécute plus efficacement si la maille de correctifs a été optimisée à l’aide de [**ID3DXPatchMesh :: Optimize**](id3dxpatchmesh--optimize.md).</span><span class="sxs-lookup"><span data-stu-id="217c3-130">This function will perform more efficiently if the patch mesh has been optimized using [**ID3DXPatchMesh::Optimize**](id3dxpatchmesh--optimize.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="217c3-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="217c3-131">Requirements</span></span>



| <span data-ttu-id="217c3-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="217c3-132">Requirement</span></span> | <span data-ttu-id="217c3-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="217c3-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="217c3-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="217c3-134">Header</span></span><br/>  | <dl> <span data-ttu-id="217c3-135"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="217c3-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="217c3-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="217c3-136">Library</span></span><br/> | <dl> <span data-ttu-id="217c3-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="217c3-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="217c3-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="217c3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="217c3-139">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="217c3-139">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
