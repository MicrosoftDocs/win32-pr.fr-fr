---
description: Définit le nom du segment.
ms.assetid: 2eecddb8-4efa-41a3-be83-7404047a9857
title: 'ID3DXSkinInfo :: SetBoneName, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetBoneName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0c9190c12eac21963d116f60d5a7aa09f97db796
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211675"
---
# <a name="id3dxskininfosetbonename-method"></a><span data-ttu-id="28dab-103">ID3DXSkinInfo :: SetBoneName, méthode</span><span class="sxs-lookup"><span data-stu-id="28dab-103">ID3DXSkinInfo::SetBoneName method</span></span>

<span data-ttu-id="28dab-104">Définit le nom du segment.</span><span class="sxs-lookup"><span data-stu-id="28dab-104">Sets the bone name.</span></span>

## <a name="syntax"></a><span data-ttu-id="28dab-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28dab-105">Syntax</span></span>


```C++
HRESULT SetBoneName(
  [in] DWORD  Bone,
  [in] LPCSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="28dab-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="28dab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28dab-107">*OS* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="28dab-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28dab-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="28dab-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="28dab-109">Numéro d’OS</span><span class="sxs-lookup"><span data-stu-id="28dab-109">Bone number</span></span>

</dd> <dt>

<span data-ttu-id="28dab-110">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="28dab-110">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28dab-111">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="28dab-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="28dab-112">Nom de l’OS</span><span class="sxs-lookup"><span data-stu-id="28dab-112">Bone name</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28dab-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="28dab-113">Return value</span></span>

<span data-ttu-id="28dab-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="28dab-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="28dab-115">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="28dab-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="28dab-116">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="28dab-116">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="28dab-117">Notes</span><span class="sxs-lookup"><span data-stu-id="28dab-117">Remarks</span></span>

<span data-ttu-id="28dab-118">Les noms osseux sont retournés par [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md).</span><span class="sxs-lookup"><span data-stu-id="28dab-118">Bone names are returned by [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="28dab-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="28dab-119">Requirements</span></span>



| <span data-ttu-id="28dab-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="28dab-120">Requirement</span></span> | <span data-ttu-id="28dab-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="28dab-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="28dab-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="28dab-122">Header</span></span><br/>  | <dl> <span data-ttu-id="28dab-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="28dab-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="28dab-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="28dab-124">Library</span></span><br/> | <dl> <span data-ttu-id="28dab-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="28dab-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="28dab-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28dab-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28dab-127">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="28dab-127">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="28dab-128">**ID3DXSkinInfo::GetBoneName**</span><span class="sxs-lookup"><span data-stu-id="28dab-128">**ID3DXSkinInfo::GetBoneName**</span></span>](id3dxskininfo--getbonename.md)
</dt> </dl>

 

 
