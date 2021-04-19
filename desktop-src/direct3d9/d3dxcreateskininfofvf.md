---
description: Crée un objet de maillage d’apparence vide à l’aide d’un code de format de vertex flexible.
ms.assetid: 72e27850-0102-4121-a397-16f2e0220b93
title: D3DXCreateSkinInfoFVF, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSkinInfoFVF
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 907ab874b8cd8b766e6f9413212ba8771df9b25c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106529613"
---
# <a name="d3dxcreateskininfofvf-function"></a><span data-ttu-id="d95ef-103">D3DXCreateSkinInfoFVF fonction)</span><span class="sxs-lookup"><span data-stu-id="d95ef-103">D3DXCreateSkinInfoFVF function</span></span>

<span data-ttu-id="d95ef-104">Crée un objet de maillage d’apparence vide à l’aide d’un code de format de vertex flexible.</span><span class="sxs-lookup"><span data-stu-id="d95ef-104">Creates an empty skin mesh object using a flexible vertex format (FVF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d95ef-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d95ef-105">Syntax</span></span>


```C++
HRESULT D3DXCreateSkinInfoFVF(
  _In_  DWORD          NumVertices,
  _In_  DWORD          FVF,
  _In_  DWORD          NumBones,
  _Out_ LPD3DXSKININFO *ppSkinInfo
);
```



## <a name="parameters"></a><span data-ttu-id="d95ef-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d95ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d95ef-107">*NumVertices* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d95ef-107">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d95ef-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d95ef-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d95ef-109">Nombre de vertex pour le maillage de l’apparence.</span><span class="sxs-lookup"><span data-stu-id="d95ef-109">Number of vertices for the skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="d95ef-110">*Commission* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d95ef-110">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d95ef-111">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d95ef-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d95ef-112">Combinaison de [D3DFVF](d3dfvf.md) qui décrit le format de vertex pour le maillage d’apparence retourné.</span><span class="sxs-lookup"><span data-stu-id="d95ef-112">Combination of [D3DFVF](d3dfvf.md) that describes the vertex format for the returned skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="d95ef-113">*NumBones* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d95ef-113">*NumBones* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d95ef-114">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d95ef-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d95ef-115">Nombre d’OS pour le maillage de l’apparence.</span><span class="sxs-lookup"><span data-stu-id="d95ef-115">Number of bones for the skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="d95ef-116">*ppSkinInfo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d95ef-116">*ppSkinInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d95ef-117">Type : **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="d95ef-117">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)\***</span></span>

<span data-ttu-id="d95ef-118">Adresse d’un pointeur vers une interface [**ID3DXSkinInfo**](id3dxskininfo.md) , représentant l’objet d’informations d’apparence créé.</span><span class="sxs-lookup"><span data-stu-id="d95ef-118">Address of a pointer to an [**ID3DXSkinInfo**](id3dxskininfo.md) interface, representing the created skin information object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d95ef-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d95ef-119">Return value</span></span>

<span data-ttu-id="d95ef-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d95ef-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d95ef-121">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d95ef-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d95ef-122">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="d95ef-122">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="d95ef-123">Notes</span><span class="sxs-lookup"><span data-stu-id="d95ef-123">Remarks</span></span>

<span data-ttu-id="d95ef-124">Utilisez [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md) pour remplir l’objet de maillage d’apparence vide retourné par cette méthode.</span><span class="sxs-lookup"><span data-stu-id="d95ef-124">Use [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md) to populate the empty skin mesh object returned by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d95ef-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d95ef-125">Requirements</span></span>



| <span data-ttu-id="d95ef-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d95ef-126">Requirement</span></span> | <span data-ttu-id="d95ef-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="d95ef-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d95ef-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="d95ef-128">Header</span></span><br/>  | <dl> <span data-ttu-id="d95ef-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d95ef-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d95ef-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d95ef-130">Library</span></span><br/> | <dl> <span data-ttu-id="d95ef-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d95ef-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d95ef-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d95ef-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d95ef-133">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="d95ef-133">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="d95ef-134">**SetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="d95ef-134">**SetBoneInfluence**</span></span>](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 
