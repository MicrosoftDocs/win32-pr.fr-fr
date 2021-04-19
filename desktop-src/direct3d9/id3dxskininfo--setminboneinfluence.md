---
description: Définit l’influence minimale du segment. Les valeurs d’influence inférieures à cette valeur sont ignorées.
ms.assetid: 9af19c9e-bb6e-4f93-973f-5c38f88eea3d
title: 'ID3DXSkinInfo :: SetMinBoneInfluence, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetMinBoneInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 03e3aeeed31a58231644784ba5070bc9422f7820
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525849"
---
# <a name="id3dxskininfosetminboneinfluence-method"></a><span data-ttu-id="e90b7-104">ID3DXSkinInfo :: SetMinBoneInfluence, méthode</span><span class="sxs-lookup"><span data-stu-id="e90b7-104">ID3DXSkinInfo::SetMinBoneInfluence method</span></span>

<span data-ttu-id="e90b7-105">Définit l’influence minimale du segment.</span><span class="sxs-lookup"><span data-stu-id="e90b7-105">Sets the minimum bone influence.</span></span> <span data-ttu-id="e90b7-106">Les valeurs d’influence inférieures à cette valeur sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="e90b7-106">Influence values smaller than this are ignored.</span></span>

## <a name="syntax"></a><span data-ttu-id="e90b7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e90b7-107">Syntax</span></span>


```C++
HRESULT SetMinBoneInfluence(
  [in] FLOAT MinInfl
);
```



## <a name="parameters"></a><span data-ttu-id="e90b7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e90b7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e90b7-109">*MinInfl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e90b7-109">*MinInfl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e90b7-110">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e90b7-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e90b7-111">Valeur d’influence minimale.</span><span class="sxs-lookup"><span data-stu-id="e90b7-111">Minimum influence value.</span></span> <span data-ttu-id="e90b7-112">Les valeurs d’influence inférieures à cette valeur sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="e90b7-112">Influence values smaller than this are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e90b7-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e90b7-113">Return value</span></span>

<span data-ttu-id="e90b7-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e90b7-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e90b7-115">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e90b7-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e90b7-116">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="e90b7-116">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e90b7-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e90b7-117">Requirements</span></span>



| <span data-ttu-id="e90b7-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e90b7-118">Requirement</span></span> | <span data-ttu-id="e90b7-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="e90b7-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e90b7-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="e90b7-120">Header</span></span><br/>  | <dl> <span data-ttu-id="e90b7-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e90b7-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e90b7-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e90b7-122">Library</span></span><br/> | <dl> <span data-ttu-id="e90b7-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e90b7-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e90b7-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e90b7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e90b7-125">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="e90b7-125">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="e90b7-126">**ID3DXSkinInfo::GetMinBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="e90b7-126">**ID3DXSkinInfo::GetMinBoneInfluence**</span></span>](id3dxskininfo--getminboneinfluence.md)
</dt> </dl>

 

 
