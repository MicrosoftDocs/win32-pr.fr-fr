---
description: Obtient le nom du segment à partir de l’index de l’OS.
ms.assetid: f56faf41-c119-4cdd-bb8a-86fc99ff5893
title: 'ID3DXSkinInfo :: GetBoneName, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0566d423d277dc3f39f36f8c1fda297ec917eb7f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106524838"
---
# <a name="id3dxskininfogetbonename-method"></a><span data-ttu-id="2f761-103">ID3DXSkinInfo :: GetBoneName, méthode</span><span class="sxs-lookup"><span data-stu-id="2f761-103">ID3DXSkinInfo::GetBoneName method</span></span>

<span data-ttu-id="2f761-104">Obtient le nom du segment à partir de l’index de l’OS.</span><span class="sxs-lookup"><span data-stu-id="2f761-104">Gets the bone name, from the bone index.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f761-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2f761-105">Syntax</span></span>


```C++
LPCSTR GetBoneName(
  [in] DWORD Bone
);
```



## <a name="parameters"></a><span data-ttu-id="2f761-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2f761-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f761-107">*OS* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2f761-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f761-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f761-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f761-109">Numéro d’os.</span><span class="sxs-lookup"><span data-stu-id="2f761-109">Bone number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f761-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2f761-110">Return value</span></span>

<span data-ttu-id="2f761-111">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f761-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f761-112">Retourne le nom du segment.</span><span class="sxs-lookup"><span data-stu-id="2f761-112">Returns the bone name.</span></span> <span data-ttu-id="2f761-113">Ne libérez pas cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="2f761-113">Do not free this string.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f761-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f761-114">Requirements</span></span>



| <span data-ttu-id="2f761-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f761-115">Requirement</span></span> | <span data-ttu-id="2f761-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f761-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f761-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="2f761-117">Header</span></span><br/>  | <dl> <span data-ttu-id="2f761-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f761-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="2f761-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2f761-119">Library</span></span><br/> | <dl> <span data-ttu-id="2f761-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f761-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2f761-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f761-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f761-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="2f761-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="2f761-123">**ID3DXSkinInfo::SetBoneName**</span><span class="sxs-lookup"><span data-stu-id="2f761-123">**ID3DXSkinInfo::SetBoneName**</span></span>](id3dxskininfo--setbonename.md)
</dt> <dt>

[<span data-ttu-id="2f761-124">**ID3DXSkinInfo::GetNumBones**</span><span class="sxs-lookup"><span data-stu-id="2f761-124">**ID3DXSkinInfo::GetNumBones**</span></span>](id3dxskininfo--getnumbones.md)
</dt> </dl>

 

 
