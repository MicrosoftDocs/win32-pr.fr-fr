---
description: D3DXCreateSkinInfo fonction-crée un objet de maillage d’apparence vide à l’aide d’un déclarateur.
ms.assetid: c98da2e5-a9eb-4070-8846-b346b5c57fb3
title: D3DXCreateSkinInfo, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSkinInfo
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da582d791b27d30c78583972e6f598af8af3eb9e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102737"
---
# <a name="d3dxcreateskininfo-function"></a><span data-ttu-id="7676b-103">D3DXCreateSkinInfo fonction)</span><span class="sxs-lookup"><span data-stu-id="7676b-103">D3DXCreateSkinInfo function</span></span>

<span data-ttu-id="7676b-104">Crée un objet de maillage d’apparence vide à l’aide d’un déclarateur.</span><span class="sxs-lookup"><span data-stu-id="7676b-104">Creates an empty skin mesh object using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="7676b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7676b-105">Syntax</span></span>


```C++
HRESULT D3DXCreateSkinInfo(
  _In_        DWORD             NumVertices,
  _In_  const D3DVERTEXELEMENT9 *pDeclaration,
  _In_        DWORD             NumBones,
  _Out_       LPD3DXSKININFO    *ppSkinInfo
);
```



## <a name="parameters"></a><span data-ttu-id="7676b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7676b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7676b-107">*NumVertices* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7676b-107">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7676b-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7676b-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7676b-109">Nombre de vertex pour le maillage de l’apparence.</span><span class="sxs-lookup"><span data-stu-id="7676b-109">Number of vertices for the skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="7676b-110">*pDeclaration* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7676b-110">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7676b-111">Type : **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="7676b-111">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="7676b-112">Tableau d’éléments [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , décrivant le format de vertex pour le maillage retourné.</span><span class="sxs-lookup"><span data-stu-id="7676b-112">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, describing the vertex format for the returned mesh.</span></span>

</dd> <dt>

<span data-ttu-id="7676b-113">*NumBones* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7676b-113">*NumBones* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7676b-114">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7676b-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7676b-115">Nombre d’OS pour le maillage de l’apparence.</span><span class="sxs-lookup"><span data-stu-id="7676b-115">Number of bones for the skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="7676b-116">*ppSkinInfo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7676b-116">*ppSkinInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7676b-117">Type : **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="7676b-117">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)\***</span></span>

<span data-ttu-id="7676b-118">Adresse d’un pointeur vers une interface [**ID3DXSkinInfo**](id3dxskininfo.md) représentant l’objet de maillage d’apparence créé.</span><span class="sxs-lookup"><span data-stu-id="7676b-118">Address of a pointer to an [**ID3DXSkinInfo**](id3dxskininfo.md) interface, representing the created skin mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7676b-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7676b-119">Return value</span></span>

<span data-ttu-id="7676b-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7676b-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7676b-121">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7676b-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7676b-122">Si la fonction échoue, la valeur de retour peut être : E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="7676b-122">If the function fails, the return value can be: E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="7676b-123">Notes </span><span class="sxs-lookup"><span data-stu-id="7676b-123">Remarks</span></span>

<span data-ttu-id="7676b-124">Utilisez [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md) pour remplir l’objet de maillage d’apparence vide retourné par cette méthode.</span><span class="sxs-lookup"><span data-stu-id="7676b-124">Use [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md) to populate the empty skin mesh object returned by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7676b-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7676b-125">Requirements</span></span>



| <span data-ttu-id="7676b-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7676b-126">Requirement</span></span> | <span data-ttu-id="7676b-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="7676b-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7676b-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="7676b-128">Header</span></span><br/>  | <dl> <span data-ttu-id="7676b-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="7676b-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="7676b-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7676b-130">Library</span></span><br/> | <dl> <span data-ttu-id="7676b-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7676b-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7676b-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7676b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7676b-133">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="7676b-133">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="7676b-134">**SetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="7676b-134">**SetBoneInfluence**</span></span>](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 
