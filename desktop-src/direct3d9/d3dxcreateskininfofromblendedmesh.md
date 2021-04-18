---
description: Crée un maillage d’apparence à partir d’un autre maillage.
ms.assetid: 4c69377e-61ef-42b8-8864-c116164d4b22
title: D3DXCreateSkinInfoFromBlendedMesh, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSkinInfoFromBlendedMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d81de43dde2b4f0df5913831ddfcefbab1a41855
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530927"
---
# <a name="d3dxcreateskininfofromblendedmesh-function"></a><span data-ttu-id="57d3e-103">D3DXCreateSkinInfoFromBlendedMesh fonction)</span><span class="sxs-lookup"><span data-stu-id="57d3e-103">D3DXCreateSkinInfoFromBlendedMesh function</span></span>

<span data-ttu-id="57d3e-104">Crée un maillage d’apparence à partir d’un autre maillage.</span><span class="sxs-lookup"><span data-stu-id="57d3e-104">Creates a skin mesh from another mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="57d3e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="57d3e-105">Syntax</span></span>


```C++
HRESULT D3DXCreateSkinInfoFromBlendedMesh(
  _In_        LPD3DXBASEMESH      pMesh,
  _In_        DWORD               NumBones,
  _In_  const D3DXBONECOMBINATION *pBoneCombinationTable,
  _Out_       LPD3DXSKININFO      *ppSkinInfo
);
```



## <a name="parameters"></a><span data-ttu-id="57d3e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57d3e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57d3e-107">*pMesh* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="57d3e-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57d3e-108">Type : **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="57d3e-108">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="57d3e-109">Pointeur vers un objet [**ID3DXBaseMesh**](id3dxbasemesh.md) , le maillage à partir duquel créer le maillage d’apparence.</span><span class="sxs-lookup"><span data-stu-id="57d3e-109">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) object, the mesh from which to create the skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="57d3e-110">*NumBones* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="57d3e-110">*NumBones* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57d3e-111">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="57d3e-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="57d3e-112">Longueur du tableau attaché à BoneId.</span><span class="sxs-lookup"><span data-stu-id="57d3e-112">The length of the array attached to the BoneId.</span></span> <span data-ttu-id="57d3e-113">Consultez [**D3DXBONECOMBINATION**](d3dxbonecombination.md).</span><span class="sxs-lookup"><span data-stu-id="57d3e-113">See [**D3DXBONECOMBINATION**](d3dxbonecombination.md).</span></span>

</dd> <dt>

<span data-ttu-id="57d3e-114">*pBoneCombinationTable* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="57d3e-114">*pBoneCombinationTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57d3e-115">Type : **const [**D3DXBONECOMBINATION**](d3dxbonecombination.md) \***</span><span class="sxs-lookup"><span data-stu-id="57d3e-115">Type: **const [**D3DXBONECOMBINATION**](d3dxbonecombination.md)\***</span></span>

<span data-ttu-id="57d3e-116">Pointeur vers un tableau de combinaisons osseuses.</span><span class="sxs-lookup"><span data-stu-id="57d3e-116">Pointer to an array of bone combinations.</span></span> <span data-ttu-id="57d3e-117">Consultez [**D3DXBONECOMBINATION**](d3dxbonecombination.md).</span><span class="sxs-lookup"><span data-stu-id="57d3e-117">See [**D3DXBONECOMBINATION**](d3dxbonecombination.md).</span></span>

</dd> <dt>

<span data-ttu-id="57d3e-118">*ppSkinInfo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="57d3e-118">*ppSkinInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57d3e-119">Type : **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="57d3e-119">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)\***</span></span>

<span data-ttu-id="57d3e-120">Adresse d’un pointeur vers une interface [**ID3DXSkinInfo**](id3dxskininfo.md) représentant l’objet de maillage d’apparence créé.</span><span class="sxs-lookup"><span data-stu-id="57d3e-120">Address of a pointer to an [**ID3DXSkinInfo**](id3dxskininfo.md) interface representing the created skin mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57d3e-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="57d3e-121">Return value</span></span>

<span data-ttu-id="57d3e-122">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="57d3e-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="57d3e-123">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="57d3e-123">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="57d3e-124">Si la fonction échoue, la valeur de retour peut être la suivante : E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="57d3e-124">If the function fails, the return value can be the following: E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="57d3e-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57d3e-125">Requirements</span></span>



| <span data-ttu-id="57d3e-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="57d3e-126">Requirement</span></span> | <span data-ttu-id="57d3e-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="57d3e-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="57d3e-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="57d3e-128">Header</span></span><br/>  | <dl> <span data-ttu-id="57d3e-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="57d3e-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="57d3e-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="57d3e-130">Library</span></span><br/> | <dl> <span data-ttu-id="57d3e-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="57d3e-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="57d3e-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57d3e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57d3e-133">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="57d3e-133">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
