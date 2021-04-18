---
description: Définit le degré d’influence d’un segment donné sur un sommet donné.
ms.assetid: adbdc784-c6b4-4e10-85c8-5e0b794d946f
title: 'ID3DX10SkinInfo :: SetBoneInfluence, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.SetBoneInfluence
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d136ddf4491a2a00c029422512c671a5439ba47c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106536248"
---
# <a name="id3dx10skininfosetboneinfluence-method"></a><span data-ttu-id="d8f94-103">ID3DX10SkinInfo :: SetBoneInfluence, méthode</span><span class="sxs-lookup"><span data-stu-id="d8f94-103">ID3DX10SkinInfo::SetBoneInfluence method</span></span>

<span data-ttu-id="d8f94-104">Définit le degré d’influence d’un segment donné sur un sommet donné.</span><span class="sxs-lookup"><span data-stu-id="d8f94-104">Set the amount of influence a given bone has over a given vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8f94-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8f94-105">Syntax</span></span>


```C++
HRESULT SetBoneInfluence(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceIndex,
  [in] float Weight
);
```



## <a name="parameters"></a><span data-ttu-id="d8f94-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d8f94-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8f94-107">*BoneIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d8f94-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8f94-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d8f94-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d8f94-109">Index qui spécifie un segment existant.</span><span class="sxs-lookup"><span data-stu-id="d8f94-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="d8f94-110">Doit être compris entre 0 et la valeur retournée par [**ID3DX10SkinInfo :: GetNumBones**](id3dx10skininfo-getnumbones.md).</span><span class="sxs-lookup"><span data-stu-id="d8f94-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8f94-111">*InfluenceIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d8f94-111">*InfluenceIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8f94-112">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d8f94-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d8f94-113">Index dans la liste des vertex du segment qu’il influence.</span><span class="sxs-lookup"><span data-stu-id="d8f94-113">An index into the bone's list of vertices that it influences.</span></span>

</dd> <dt>

<span data-ttu-id="d8f94-114">*Poids* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d8f94-114">*Weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8f94-115">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="d8f94-115">Type: **float**</span></span>

<span data-ttu-id="d8f94-116">La quantité d’influence, comprise entre 0 et 1, que le segment a sur le vertex.</span><span class="sxs-lookup"><span data-stu-id="d8f94-116">The amount of influence, between 0 and 1, that the bone has over the vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8f94-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d8f94-117">Return value</span></span>

<span data-ttu-id="d8f94-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d8f94-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d8f94-119">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d8f94-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d8f94-120">Si la méthode échoue, la valeur de retour peut être E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="d8f94-120">If the method fails, the return value can be E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8f94-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8f94-121">Requirements</span></span>



| <span data-ttu-id="d8f94-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8f94-122">Requirement</span></span> | <span data-ttu-id="d8f94-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8f94-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d8f94-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="d8f94-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d8f94-125"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8f94-125"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="d8f94-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d8f94-126">Library</span></span><br/> | <dl> <span data-ttu-id="d8f94-127"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8f94-127"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8f94-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8f94-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8f94-129">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="d8f94-129">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="d8f94-130">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="d8f94-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
