---
description: Obtient les vertex et les poids influencés par un segment.
ms.assetid: 84cb064b-b6b2-402d-81cc-8c02de6f8b52
title: 'ID3DXSkinInfo :: GetBoneInfluence, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8b4b31ab08aca476ced1cb28dfc5ed5bfe61d044
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531308"
---
# <a name="id3dxskininfogetboneinfluence-method"></a><span data-ttu-id="cad52-103">ID3DXSkinInfo :: GetBoneInfluence, méthode</span><span class="sxs-lookup"><span data-stu-id="cad52-103">ID3DXSkinInfo::GetBoneInfluence method</span></span>

<span data-ttu-id="cad52-104">Obtient les vertex et les poids influencés par un segment.</span><span class="sxs-lookup"><span data-stu-id="cad52-104">Gets the vertices and weights that a bone influences.</span></span>

## <a name="syntax"></a><span data-ttu-id="cad52-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cad52-105">Syntax</span></span>


```C++
HRESULT GetBoneInfluence(
  [in]      DWORD Bone,
  [in, out] DWORD *vertices,
  [in, out] FLOAT *weights
);
```



## <a name="parameters"></a><span data-ttu-id="cad52-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cad52-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cad52-107">*OS* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cad52-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cad52-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cad52-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cad52-109">Numéro d’os.</span><span class="sxs-lookup"><span data-stu-id="cad52-109">Bone number.</span></span>

</dd> <dt>

<span data-ttu-id="cad52-110">*vertex* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="cad52-110">*vertices* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cad52-111">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="cad52-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cad52-112">Obtient le tableau de vertex influencé par un segment.</span><span class="sxs-lookup"><span data-stu-id="cad52-112">Get the array of vertices influenced by a bone.</span></span>

</dd> <dt>

<span data-ttu-id="cad52-113">*poids* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="cad52-113">*weights* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cad52-114">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="cad52-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cad52-115">Obtenir le tableau de poids influencé par un segment.</span><span class="sxs-lookup"><span data-stu-id="cad52-115">Get the array of weights influenced by a bone.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cad52-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cad52-116">Return value</span></span>

<span data-ttu-id="cad52-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cad52-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cad52-118">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cad52-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cad52-119">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="cad52-119">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="cad52-120">Notes</span><span class="sxs-lookup"><span data-stu-id="cad52-120">Remarks</span></span>

<span data-ttu-id="cad52-121">Utilisez [**ID3DXSkinInfo :: GetNumBoneInfluences**](id3dxskininfo--getnumboneinfluences.md) pour connaître le nombre de vertex que le segment influence.</span><span class="sxs-lookup"><span data-stu-id="cad52-121">Use [**ID3DXSkinInfo::GetNumBoneInfluences**](id3dxskininfo--getnumboneinfluences.md) to find out how many vertices the bone influences.</span></span>

## <a name="requirements"></a><span data-ttu-id="cad52-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cad52-122">Requirements</span></span>



| <span data-ttu-id="cad52-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cad52-123">Requirement</span></span> | <span data-ttu-id="cad52-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="cad52-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cad52-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="cad52-125">Header</span></span><br/>  | <dl> <span data-ttu-id="cad52-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="cad52-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="cad52-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cad52-127">Library</span></span><br/> | <dl> <span data-ttu-id="cad52-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cad52-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cad52-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cad52-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cad52-130">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="cad52-130">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="cad52-131">**ID3DXSkinInfo::SetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="cad52-131">**ID3DXSkinInfo::SetBoneInfluence**</span></span>](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 
