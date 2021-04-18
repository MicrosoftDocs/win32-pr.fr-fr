---
description: Récupère l’index de l’influence osseuse affectant un seul vertex.
ms.assetid: vs|directx_sdk|~\id3dxskininfo__findbonevertexinfluenceindex.htm
title: 'ID3DXSkinInfo :: FindBoneVertexInfluenceIndex, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.FindBoneVertexInfluenceIndex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 05a86e98e5001092700fdec12f2a7afc33ddf082
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106543020"
---
# <a name="id3dxskininfofindbonevertexinfluenceindex-method"></a><span data-ttu-id="bae63-103">ID3DXSkinInfo :: FindBoneVertexInfluenceIndex, méthode</span><span class="sxs-lookup"><span data-stu-id="bae63-103">ID3DXSkinInfo::FindBoneVertexInfluenceIndex method</span></span>

<span data-ttu-id="bae63-104">Récupère l’index de l’influence osseuse affectant un seul vertex.</span><span class="sxs-lookup"><span data-stu-id="bae63-104">Retrieves the index of the bone influence affecting a single vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="bae63-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bae63-105">Syntax</span></span>


```C++
HRESULT FindBoneVertexInfluenceIndex(
  [in]      DWORD boneNum,
  [in]      DWORD vertexNum,
  [in, out] DWORD *pInfluenceIndex
);
```



## <a name="parameters"></a><span data-ttu-id="bae63-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bae63-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bae63-107">*boneNum* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bae63-107">*boneNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bae63-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bae63-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bae63-109">Index du segment.</span><span class="sxs-lookup"><span data-stu-id="bae63-109">Index of the bone.</span></span> <span data-ttu-id="bae63-110">Doit être compris entre 0 et le nombre d’os.</span><span class="sxs-lookup"><span data-stu-id="bae63-110">Must be between 0 and the number of bones.</span></span>

</dd> <dt>

<span data-ttu-id="bae63-111">*vertexNum* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bae63-111">*vertexNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bae63-112">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bae63-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bae63-113">Index du vertex pour lequel l’influence du segment est recherchée.</span><span class="sxs-lookup"><span data-stu-id="bae63-113">Index of the vertex for which the bone influence is to be found.</span></span> <span data-ttu-id="bae63-114">Doit être compris entre 0 et le nombre de vertex dans le maillage.</span><span class="sxs-lookup"><span data-stu-id="bae63-114">Must be between 0 and the number of vertices in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="bae63-115">*pInfluenceIndex* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bae63-115">*pInfluenceIndex* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bae63-116">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="bae63-116">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="bae63-117">Pointeur vers l’index de l’influence du segment qui affecte vertexNum.</span><span class="sxs-lookup"><span data-stu-id="bae63-117">Pointer to the index of the bone influence that affects vertexNum.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bae63-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bae63-118">Return value</span></span>

<span data-ttu-id="bae63-119">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bae63-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bae63-120">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bae63-120">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="bae63-121">Si le segment spécifié n’influence pas le vertex donné, S \_ false est retourné.</span><span class="sxs-lookup"><span data-stu-id="bae63-121">If the specified bone does not influence the given vertex, S\_FALSE is returned.</span></span> <span data-ttu-id="bae63-122">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="bae63-122">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="bae63-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bae63-123">Requirements</span></span>



| <span data-ttu-id="bae63-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bae63-124">Requirement</span></span> | <span data-ttu-id="bae63-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="bae63-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bae63-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="bae63-126">Header</span></span><br/>  | <dl> <span data-ttu-id="bae63-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="bae63-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="bae63-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bae63-128">Library</span></span><br/> | <dl> <span data-ttu-id="bae63-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bae63-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bae63-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bae63-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bae63-131">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="bae63-131">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="bae63-132">**ID3DXSkinInfo::GetBoneVertexInfluence**</span><span class="sxs-lookup"><span data-stu-id="bae63-132">**ID3DXSkinInfo::GetBoneVertexInfluence**</span></span>](id3dxskininfo--getbonevertexinfluence.md)
</dt> <dt>

[<span data-ttu-id="bae63-133">**ID3DXSkinInfo::SetBoneVertexInfluence**</span><span class="sxs-lookup"><span data-stu-id="bae63-133">**ID3DXSkinInfo::SetBoneVertexInfluence**</span></span>](id3dxskininfo--setbonevertexinfluence.md)
</dt> <dt>

[<span data-ttu-id="bae63-134">**ID3DXSkinInfo::GetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="bae63-134">**ID3DXSkinInfo::GetBoneInfluence**</span></span>](id3dxskininfo--getboneinfluence.md)
</dt> </dl>

 

 
