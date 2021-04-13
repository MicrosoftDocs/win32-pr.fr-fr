---
description: Obtient la matrice de décalage de l’OS.
ms.assetid: 99d47635-ffae-4668-a37c-b15442148fa1
title: 'ID3DXSkinInfo :: GetBoneOffsetMatrix, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneOffsetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fce108dc1d0eb08f198ae9375ac35ed149c5e760
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322614"
---
# <a name="id3dxskininfogetboneoffsetmatrix-method"></a><span data-ttu-id="3e56d-103">ID3DXSkinInfo :: GetBoneOffsetMatrix, méthode</span><span class="sxs-lookup"><span data-stu-id="3e56d-103">ID3DXSkinInfo::GetBoneOffsetMatrix method</span></span>

<span data-ttu-id="3e56d-104">Obtient la matrice de décalage de l’OS.</span><span class="sxs-lookup"><span data-stu-id="3e56d-104">Gets the bone offset matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e56d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3e56d-105">Syntax</span></span>


```C++
LPD3DXMATRIX GetBoneOffsetMatrix(
  [in] DWORD Bone
);
```



## <a name="parameters"></a><span data-ttu-id="3e56d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3e56d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e56d-107">*OS* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3e56d-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e56d-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3e56d-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3e56d-109">Numéro d’os.</span><span class="sxs-lookup"><span data-stu-id="3e56d-109">Bone number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e56d-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3e56d-110">Return value</span></span>

<span data-ttu-id="3e56d-111">Type : **[ **LPD3DXMATRIX**](d3dxmatrix.md)**</span><span class="sxs-lookup"><span data-stu-id="3e56d-111">Type: **[**LPD3DXMATRIX**](d3dxmatrix.md)**</span></span>

<span data-ttu-id="3e56d-112">Retourne un pointeur vers la matrice de décalage de l’OS.</span><span class="sxs-lookup"><span data-stu-id="3e56d-112">Returns a pointer to the bone offset matrix.</span></span> <span data-ttu-id="3e56d-113">Ne libérez pas ce pointeur.</span><span class="sxs-lookup"><span data-stu-id="3e56d-113">Do not free this pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e56d-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e56d-114">Requirements</span></span>



| <span data-ttu-id="3e56d-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3e56d-115">Requirement</span></span> | <span data-ttu-id="3e56d-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e56d-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e56d-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="3e56d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="3e56d-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e56d-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3e56d-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3e56d-119">Library</span></span><br/> | <dl> <span data-ttu-id="3e56d-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3e56d-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3e56d-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e56d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e56d-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="3e56d-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="3e56d-123">**SetBoneOffsetMatrix**</span><span class="sxs-lookup"><span data-stu-id="3e56d-123">**SetBoneOffsetMatrix**</span></span>](id3dxskininfo--setboneoffsetmatrix.md)
</dt> <dt>

[<span data-ttu-id="3e56d-124">**GetNumBones**</span><span class="sxs-lookup"><span data-stu-id="3e56d-124">**GetNumBones**</span></span>](id3dxskininfo--getnumbones.md)
</dt> </dl>

 

 
