---
description: Récupère le facteur de fusion et le vertex affectés par une influence osseuse spécifiée.
ms.assetid: bbed4766-e571-4a9e-b7e3-047052470cbe
title: 'ID3DXSkinInfo :: GetBoneVertexInfluence, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneVertexInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6e3cb7c530ed72a65f9a3e8de6b0735b1a7ae5e4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322606"
---
# <a name="id3dxskininfogetbonevertexinfluence-method"></a><span data-ttu-id="59c3f-103">ID3DXSkinInfo :: GetBoneVertexInfluence, méthode</span><span class="sxs-lookup"><span data-stu-id="59c3f-103">ID3DXSkinInfo::GetBoneVertexInfluence method</span></span>

<span data-ttu-id="59c3f-104">Récupère le facteur de fusion et le vertex affectés par une influence osseuse spécifiée.</span><span class="sxs-lookup"><span data-stu-id="59c3f-104">Retrieves the blend factor and vertex affected by a specified bone influence.</span></span>

## <a name="syntax"></a><span data-ttu-id="59c3f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59c3f-105">Syntax</span></span>


```C++
HRESULT GetBoneVertexInfluence(
  [in]      DWORD boneNum,
  [in]      DWORD influenceNum,
  [in, out] FLOAT *pWeight,
  [in, out] DWORD *pVertexNum
);
```



## <a name="parameters"></a><span data-ttu-id="59c3f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59c3f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59c3f-107">*boneNum* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="59c3f-107">*boneNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59c3f-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="59c3f-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="59c3f-109">Index du segment.</span><span class="sxs-lookup"><span data-stu-id="59c3f-109">Index of the bone.</span></span> <span data-ttu-id="59c3f-110">Doit être compris entre 0 et le nombre d’os.</span><span class="sxs-lookup"><span data-stu-id="59c3f-110">Must be between 0 and the number of bones.</span></span>

</dd> <dt>

<span data-ttu-id="59c3f-111">*influenceNum* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="59c3f-111">*influenceNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59c3f-112">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="59c3f-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="59c3f-113">Index du tableau d’influence du segment spécifié.</span><span class="sxs-lookup"><span data-stu-id="59c3f-113">Index of the influence array of the specified bone.</span></span>

</dd> <dt>

<span data-ttu-id="59c3f-114">*pWeight* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="59c3f-114">*pWeight* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="59c3f-115">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="59c3f-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="59c3f-116">Pointeur vers le facteur de fusion influencé par influenceNum.</span><span class="sxs-lookup"><span data-stu-id="59c3f-116">Pointer to the blend factor influenced by influenceNum.</span></span>

</dd> <dt>

<span data-ttu-id="59c3f-117">*pVertexNum* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="59c3f-117">*pVertexNum* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="59c3f-118">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="59c3f-118">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="59c3f-119">Pointeur vers le vertex influencé par influenceNum.</span><span class="sxs-lookup"><span data-stu-id="59c3f-119">Pointer to the vertex influenced by influenceNum.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59c3f-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="59c3f-120">Return value</span></span>

<span data-ttu-id="59c3f-121">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="59c3f-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="59c3f-122">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="59c3f-122">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="59c3f-123">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="59c3f-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="59c3f-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59c3f-124">Requirements</span></span>



| <span data-ttu-id="59c3f-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59c3f-125">Requirement</span></span> | <span data-ttu-id="59c3f-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="59c3f-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="59c3f-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="59c3f-127">Header</span></span><br/>  | <dl> <span data-ttu-id="59c3f-128"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="59c3f-128"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="59c3f-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="59c3f-129">Library</span></span><br/> | <dl> <span data-ttu-id="59c3f-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59c3f-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="59c3f-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59c3f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59c3f-132">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="59c3f-132">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="59c3f-133">**ID3DXSkinInfo::SetBoneVertexInfluence**</span><span class="sxs-lookup"><span data-stu-id="59c3f-133">**ID3DXSkinInfo::SetBoneVertexInfluence**</span></span>](id3dxskininfo--setbonevertexinfluence.md)
</dt> <dt>

[<span data-ttu-id="59c3f-134">**ID3DXSkinInfo::FindBoneVertexInfluenceIndex**</span><span class="sxs-lookup"><span data-stu-id="59c3f-134">**ID3DXSkinInfo::FindBoneVertexInfluenceIndex**</span></span>](id3dxskininfo--findbonevertexinfluenceindex.md)
</dt> <dt>

[<span data-ttu-id="59c3f-135">**ID3DXSkinInfo::GetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="59c3f-135">**ID3DXSkinInfo::GetBoneInfluence**</span></span>](id3dxskininfo--getboneinfluence.md)
</dt> </dl>

 

 
