---
description: Définit la valeur d’influence d’un segment.
ms.assetid: c6dc8a33-8f5c-47d0-8637-a2492b1e3089
title: 'ID3DXSkinInfo :: SetBoneInfluence, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetBoneInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 16ed3514c986dee89f964074d18a646bcf3a1249
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539421"
---
# <a name="id3dxskininfosetboneinfluence-method"></a><span data-ttu-id="c1aeb-103">ID3DXSkinInfo :: SetBoneInfluence, méthode</span><span class="sxs-lookup"><span data-stu-id="c1aeb-103">ID3DXSkinInfo::SetBoneInfluence method</span></span>

<span data-ttu-id="c1aeb-104">Définit la valeur d’influence d’un segment.</span><span class="sxs-lookup"><span data-stu-id="c1aeb-104">Sets the influence value for a bone.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1aeb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c1aeb-105">Syntax</span></span>


```C++
HRESULT SetBoneInfluence(
  [in]       DWORD Bone,
  [in]       DWORD numInfluences,
  [in] const DWORD *vertices,
  [in] const FLOAT *weights
);
```



## <a name="parameters"></a><span data-ttu-id="c1aeb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c1aeb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1aeb-107">*OS* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c1aeb-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1aeb-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c1aeb-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c1aeb-109">Numéro d’os.</span><span class="sxs-lookup"><span data-stu-id="c1aeb-109">Bone number.</span></span>

</dd> <dt>

<span data-ttu-id="c1aeb-110">*numInfluences* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c1aeb-110">*numInfluences* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1aeb-111">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c1aeb-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c1aeb-112">Nombre d’influences.</span><span class="sxs-lookup"><span data-stu-id="c1aeb-112">Number of influences.</span></span>

</dd> <dt>

<span data-ttu-id="c1aeb-113">*vertex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c1aeb-113">*vertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1aeb-114">Type : **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="c1aeb-114">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c1aeb-115">Tableau de vertex influencé par un segment.</span><span class="sxs-lookup"><span data-stu-id="c1aeb-115">The array of vertices influenced by a bone.</span></span>

</dd> <dt>

<span data-ttu-id="c1aeb-116">*poids* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c1aeb-116">*weights* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1aeb-117">Type : **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="c1aeb-117">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c1aeb-118">Tableau de poids influencé par un segment.</span><span class="sxs-lookup"><span data-stu-id="c1aeb-118">The array of weights influenced by a bone.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1aeb-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c1aeb-119">Return value</span></span>

<span data-ttu-id="c1aeb-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c1aeb-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c1aeb-121">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c1aeb-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c1aeb-122">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="c1aeb-122">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1aeb-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c1aeb-123">Requirements</span></span>



| <span data-ttu-id="c1aeb-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c1aeb-124">Requirement</span></span> | <span data-ttu-id="c1aeb-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1aeb-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1aeb-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="c1aeb-126">Header</span></span><br/>  | <dl> <span data-ttu-id="c1aeb-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1aeb-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c1aeb-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c1aeb-128">Library</span></span><br/> | <dl> <span data-ttu-id="c1aeb-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1aeb-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c1aeb-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1aeb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1aeb-131">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="c1aeb-131">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="c1aeb-132">**ID3DXSkinInfo::GetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="c1aeb-132">**ID3DXSkinInfo::GetBoneInfluence**</span></span>](id3dxskininfo--getboneinfluence.md)
</dt> <dt>

[<span data-ttu-id="c1aeb-133">**ID3DXSkinInfo::GetNumBoneInfluences**</span><span class="sxs-lookup"><span data-stu-id="c1aeb-133">**ID3DXSkinInfo::GetNumBoneInfluences**</span></span>](id3dxskininfo--getnumboneinfluences.md)
</dt> </dl>

 

 
