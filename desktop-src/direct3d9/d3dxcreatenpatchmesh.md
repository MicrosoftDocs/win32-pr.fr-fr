---
description: Crée un maillage N-patch à partir d’un maillage de triangles.
ms.assetid: f565ed0b-72fc-4184-b423-f68b0acfafb0
title: D3DXCreateNPatchMesh, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateNPatchMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ab73d1254700808bbd56b7b46f7781b27b188b7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527955"
---
# <a name="d3dxcreatenpatchmesh-function"></a><span data-ttu-id="7c2e0-103">D3DXCreateNPatchMesh fonction)</span><span class="sxs-lookup"><span data-stu-id="7c2e0-103">D3DXCreateNPatchMesh function</span></span>

<span data-ttu-id="7c2e0-104">Crée un maillage N-patch à partir d’un maillage de triangles.</span><span class="sxs-lookup"><span data-stu-id="7c2e0-104">Creates an N-patch mesh from a triangle mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c2e0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7c2e0-105">Syntax</span></span>


```C++
HRESULT D3DXCreateNPatchMesh(
  _In_    LPD3DXMESH      pMeshSysMem,
  _Inout_ LPD3DXPATCHMESH *pPatchMesh
);
```



## <a name="parameters"></a><span data-ttu-id="7c2e0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c2e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c2e0-107">*pMeshSysMem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7c2e0-107">*pMeshSysMem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c2e0-108">Type : **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="7c2e0-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="7c2e0-109">Adresse d’un pointeur vers une interface [**ID3DXMesh**](id3dxmesh.md) qui représente l’objet de maillage de triangle.</span><span class="sxs-lookup"><span data-stu-id="7c2e0-109">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface that represents the triangle mesh object.</span></span>

</dd> <dt>

<span data-ttu-id="7c2e0-110">*pPatchMesh* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7c2e0-110">*pPatchMesh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c2e0-111">Type : **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="7c2e0-111">Type: **[**LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span></span>

<span data-ttu-id="7c2e0-112">Adresse d’un pointeur vers une interface [**ID3DXPatchMesh**](id3dxpatchmesh.md) qui représente l’objet de maillage de correctif créé.</span><span class="sxs-lookup"><span data-stu-id="7c2e0-112">Address of a pointer to an [**ID3DXPatchMesh**](id3dxpatchmesh.md) interface that represents the created patch mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c2e0-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7c2e0-113">Return value</span></span>

<span data-ttu-id="7c2e0-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7c2e0-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7c2e0-115">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7c2e0-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7c2e0-116">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="7c2e0-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c2e0-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c2e0-117">Requirements</span></span>



| <span data-ttu-id="7c2e0-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c2e0-118">Requirement</span></span> | <span data-ttu-id="7c2e0-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c2e0-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c2e0-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="7c2e0-120">Header</span></span><br/>  | <dl> <span data-ttu-id="7c2e0-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c2e0-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="7c2e0-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7c2e0-122">Library</span></span><br/> | <dl> <span data-ttu-id="7c2e0-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c2e0-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7c2e0-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c2e0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c2e0-125">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="7c2e0-125">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




