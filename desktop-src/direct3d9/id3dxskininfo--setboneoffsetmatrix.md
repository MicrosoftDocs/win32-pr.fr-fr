---
description: Définit la matrice de décalage de l’OS.
ms.assetid: f8ac1117-510d-42af-a6bf-422cbaaf6b74
title: 'ID3DXSkinInfo :: SetBoneOffsetMatrix, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetBoneOffsetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 283d36bb68e33cfa0e2349bab304b0cdde7ef77e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761918"
---
# <a name="id3dxskininfosetboneoffsetmatrix-method"></a><span data-ttu-id="4a327-103">ID3DXSkinInfo :: SetBoneOffsetMatrix, méthode</span><span class="sxs-lookup"><span data-stu-id="4a327-103">ID3DXSkinInfo::SetBoneOffsetMatrix method</span></span>

<span data-ttu-id="4a327-104">Définit la matrice de décalage de l’OS.</span><span class="sxs-lookup"><span data-stu-id="4a327-104">Sets the bone offset matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a327-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4a327-105">Syntax</span></span>


```C++
HRESULT SetBoneOffsetMatrix(
  [in]       DWORD      Bone,
  [in] const D3DXMATRIX *pBoneTransform
);
```



## <a name="parameters"></a><span data-ttu-id="4a327-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4a327-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a327-107">*OS* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4a327-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a327-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a327-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4a327-109">Numéro d’os.</span><span class="sxs-lookup"><span data-stu-id="4a327-109">Bone number.</span></span>

</dd> <dt>

<span data-ttu-id="4a327-110">*pBoneTransform* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4a327-110">*pBoneTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a327-111">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="4a327-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4a327-112">Pointeur vers la matrice de décalage de l’OS.</span><span class="sxs-lookup"><span data-stu-id="4a327-112">Pointer to the bone offset matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a327-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4a327-113">Return value</span></span>

<span data-ttu-id="4a327-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4a327-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4a327-115">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4a327-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4a327-116">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="4a327-116">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a327-117">Notes</span><span class="sxs-lookup"><span data-stu-id="4a327-117">Remarks</span></span>

<span data-ttu-id="4a327-118">Les noms osseux sont retournés par [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md).</span><span class="sxs-lookup"><span data-stu-id="4a327-118">Bone names are returned by [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4a327-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4a327-119">Requirements</span></span>



| <span data-ttu-id="4a327-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4a327-120">Requirement</span></span> | <span data-ttu-id="4a327-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a327-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a327-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="4a327-122">Header</span></span><br/>  | <dl> <span data-ttu-id="4a327-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a327-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="4a327-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4a327-124">Library</span></span><br/> | <dl> <span data-ttu-id="4a327-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a327-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4a327-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a327-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a327-127">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="4a327-127">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="4a327-128">**ID3DXSkinInfo::GetBoneOffsetMatrix**</span><span class="sxs-lookup"><span data-stu-id="4a327-128">**ID3DXSkinInfo::GetBoneOffsetMatrix**</span></span>](id3dxskininfo--getboneoffsetmatrix.md)
</dt> </dl>

 

 
