---
description: Définit une valeur d’influence d’un segment sur un seul vertex.
ms.assetid: 9283866f-3dfe-467d-a74f-77e89c2778c4
title: 'ID3DXSkinInfo :: SetBoneVertexInfluence, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetBoneVertexInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: db84cdf9a1647bc5302c421e52d50f812e74596e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106536239"
---
# <a name="id3dxskininfosetbonevertexinfluence-method"></a><span data-ttu-id="e9650-103">ID3DXSkinInfo :: SetBoneVertexInfluence, méthode</span><span class="sxs-lookup"><span data-stu-id="e9650-103">ID3DXSkinInfo::SetBoneVertexInfluence method</span></span>

<span data-ttu-id="e9650-104">Définit une valeur d’influence d’un segment sur un seul vertex.</span><span class="sxs-lookup"><span data-stu-id="e9650-104">Sets an influence value of a bone on a single vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9650-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9650-105">Syntax</span></span>


```C++
HRESULT SetBoneVertexInfluence(
  [in] DWORD boneNum,
  [in] DWORD influenceNum,
  [in] FLOAT weight
);
```



## <a name="parameters"></a><span data-ttu-id="e9650-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e9650-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9650-107">*boneNum* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e9650-107">*boneNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9650-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e9650-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e9650-109">Index du segment.</span><span class="sxs-lookup"><span data-stu-id="e9650-109">Index of the bone.</span></span> <span data-ttu-id="e9650-110">Doit être compris entre 0 et le nombre d’os.</span><span class="sxs-lookup"><span data-stu-id="e9650-110">Must be between 0 and the number of bones.</span></span>

</dd> <dt>

<span data-ttu-id="e9650-111">*influenceNum* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e9650-111">*influenceNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9650-112">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e9650-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e9650-113">Index du tableau d’influence du segment spécifié.</span><span class="sxs-lookup"><span data-stu-id="e9650-113">Index of the influence array of the specified bone.</span></span>

</dd> <dt>

<span data-ttu-id="e9650-114">*poids* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e9650-114">*weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9650-115">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e9650-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e9650-116">Facteur de fusion de l’influence osseuse spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e9650-116">Blend factor of the specified bone influence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9650-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e9650-117">Return value</span></span>

<span data-ttu-id="e9650-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e9650-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e9650-119">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e9650-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e9650-120">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="e9650-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9650-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9650-121">Requirements</span></span>



| <span data-ttu-id="e9650-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9650-122">Requirement</span></span> | <span data-ttu-id="e9650-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9650-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9650-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="e9650-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e9650-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9650-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e9650-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e9650-126">Library</span></span><br/> | <dl> <span data-ttu-id="e9650-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9650-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e9650-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9650-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9650-129">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="e9650-129">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="e9650-130">**ID3DXSkinInfo::GetBoneVertexInfluence**</span><span class="sxs-lookup"><span data-stu-id="e9650-130">**ID3DXSkinInfo::GetBoneVertexInfluence**</span></span>](id3dxskininfo--getbonevertexinfluence.md)
</dt> <dt>

[<span data-ttu-id="e9650-131">**ID3DXSkinInfo::FindBoneVertexInfluenceIndex**</span><span class="sxs-lookup"><span data-stu-id="e9650-131">**ID3DXSkinInfo::FindBoneVertexInfluenceIndex**</span></span>](id3dxskininfo--findbonevertexinfluenceindex.md)
</dt> <dt>

[<span data-ttu-id="e9650-132">**ID3DXSkinInfo::GetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="e9650-132">**ID3DXSkinInfo::GetBoneInfluence**</span></span>](id3dxskininfo--getboneinfluence.md)
</dt> </dl>

 

 
