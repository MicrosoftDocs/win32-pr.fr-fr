---
description: Modifiez les segments qui influencent les vertex.
ms.assetid: 0955e0ba-ffc5-408b-ab38-2abd39e1c429
title: 'ID3DX10SkinInfo :: RemapBones, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.RemapBones
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 238e4628740fa74e055312c82de2635316f5bde5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539446"
---
# <a name="id3dx10skininforemapbones-method"></a><span data-ttu-id="8968f-103">ID3DX10SkinInfo :: RemapBones, méthode</span><span class="sxs-lookup"><span data-stu-id="8968f-103">ID3DX10SkinInfo::RemapBones method</span></span>

<span data-ttu-id="8968f-104">Modifiez les segments qui influencent les vertex.</span><span class="sxs-lookup"><span data-stu-id="8968f-104">Change which bones influence which vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="8968f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8968f-105">Syntax</span></span>


```C++
HRESULT RemapBones(
  [in] UINT NewBoneCount,
  [in] UINT *pBoneRemap
);
```



## <a name="parameters"></a><span data-ttu-id="8968f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8968f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8968f-107">*NewBoneCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8968f-107">*NewBoneCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8968f-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8968f-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8968f-109">Nouveau nombre d’os.</span><span class="sxs-lookup"><span data-stu-id="8968f-109">The new number of bones.</span></span>

</dd> <dt>

<span data-ttu-id="8968f-110">*pBoneRemap* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8968f-110">*pBoneRemap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8968f-111">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8968f-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8968f-112">Pointeur vers un tableau d’index osseux qui décrivent le remappage.</span><span class="sxs-lookup"><span data-stu-id="8968f-112">A pointer to an array of bone indices, which describe the remapping.</span></span> <span data-ttu-id="8968f-113">Par exemple, disons SkinInfo contient des segments tels que bone0 est mappé à v0, bone1 à v1 et bone2 à v2, et Array avec 2, 1, 0 est spécifié pour pBoneRemap.</span><span class="sxs-lookup"><span data-stu-id="8968f-113">For example, say SkinInfo contains some bones such that bone0 is mapped to v0, bone1 to v1, and bone2 to v2, and array with 2,1,0 is specified for pBoneRemap.</span></span> <span data-ttu-id="8968f-114">Bone0 sera alors mappé à v2, bone1 à v1 et bone2 à v0.</span><span class="sxs-lookup"><span data-stu-id="8968f-114">This will cause bone0 to be mapped to v2, bone1 to v1, and bone2 to v0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8968f-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8968f-115">Return value</span></span>

<span data-ttu-id="8968f-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8968f-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8968f-117">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8968f-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="8968f-118">Si la méthode échoue, la valeur de retour peut être : E \_ OUTOFMEMORY ou e \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="8968f-118">If the method fails, the return value can be: E\_OUTOFMEMORY or E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="8968f-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8968f-119">Requirements</span></span>



| <span data-ttu-id="8968f-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8968f-120">Requirement</span></span> | <span data-ttu-id="8968f-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="8968f-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8968f-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="8968f-122">Header</span></span><br/>  | <dl> <span data-ttu-id="8968f-123"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="8968f-123"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="8968f-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8968f-124">Library</span></span><br/> | <dl> <span data-ttu-id="8968f-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8968f-125"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8968f-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8968f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8968f-127">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="8968f-127">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="8968f-128">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="8968f-128">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
