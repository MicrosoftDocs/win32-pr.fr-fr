---
description: Obtenir le degré d’influence d’un segment donné sur un vertex donné.
ms.assetid: 0586fdfd-e5b1-4699-b489-c54a0f305ee4
title: 'ID3DX10SkinInfo :: GetBoneInfluence, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.GetBoneInfluence
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b2f7e6b75e9c0f9f08463b6dacf9d7c9d72f4f28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523844"
---
# <a name="id3dx10skininfogetboneinfluence-method"></a><span data-ttu-id="da92d-103">ID3DX10SkinInfo :: GetBoneInfluence, méthode</span><span class="sxs-lookup"><span data-stu-id="da92d-103">ID3DX10SkinInfo::GetBoneInfluence method</span></span>

<span data-ttu-id="da92d-104">Obtenir le degré d’influence d’un segment donné sur un vertex donné.</span><span class="sxs-lookup"><span data-stu-id="da92d-104">Get the amount of influence a given bone has over a given vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="da92d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da92d-105">Syntax</span></span>


```C++
HRESULT GetBoneInfluence(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceIndex,
  [in] float *pWeight
);
```



## <a name="parameters"></a><span data-ttu-id="da92d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="da92d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da92d-107">*BoneIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="da92d-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da92d-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="da92d-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="da92d-109">Index qui spécifie un segment existant.</span><span class="sxs-lookup"><span data-stu-id="da92d-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="da92d-110">Doit être compris entre 0 et la valeur retournée par [**ID3DX10SkinInfo :: GetNumBones**](id3dx10skininfo-getnumbones.md).</span><span class="sxs-lookup"><span data-stu-id="da92d-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> <dt>

<span data-ttu-id="da92d-111">*InfluenceIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="da92d-111">*InfluenceIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da92d-112">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="da92d-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="da92d-113">Index dans la liste des vertex du segment qu’il influence.</span><span class="sxs-lookup"><span data-stu-id="da92d-113">An index into the bone's list of vertices that it influences.</span></span>

</dd> <dt>

<span data-ttu-id="da92d-114">*pWeight* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="da92d-114">*pWeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da92d-115">Type : **float \***</span><span class="sxs-lookup"><span data-stu-id="da92d-115">Type: **float\***</span></span>

<span data-ttu-id="da92d-116">La quantité d’influence, comprise entre 0 et 1, que le segment a sur le vertex.</span><span class="sxs-lookup"><span data-stu-id="da92d-116">The amount of influence, between 0 and 1, that the bone has over the vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da92d-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="da92d-117">Return value</span></span>

<span data-ttu-id="da92d-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="da92d-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="da92d-119">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="da92d-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="da92d-120">Si la méthode échoue, la valeur de retour peut être E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="da92d-120">If the method fails, the return value can be E\_INVALIDARG.</span></span>

## <a name="remarks"></a><span data-ttu-id="da92d-121">Notes</span><span class="sxs-lookup"><span data-stu-id="da92d-121">Remarks</span></span>

<span data-ttu-id="da92d-122">Utilisez ID3DX10SkinInfo :: GetBoneInfluenceCount pour connaître le nombre de vertex que le segment influence.</span><span class="sxs-lookup"><span data-stu-id="da92d-122">Use ID3DX10SkinInfo::GetBoneInfluenceCount to find out how many vertices the bone influences.</span></span>

## <a name="requirements"></a><span data-ttu-id="da92d-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da92d-123">Requirements</span></span>



| <span data-ttu-id="da92d-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da92d-124">Requirement</span></span> | <span data-ttu-id="da92d-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="da92d-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="da92d-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="da92d-126">Header</span></span><br/>  | <dl> <span data-ttu-id="da92d-127"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="da92d-127"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="da92d-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="da92d-128">Library</span></span><br/> | <dl> <span data-ttu-id="da92d-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="da92d-129"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da92d-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da92d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da92d-131">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="da92d-131">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="da92d-132">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="da92d-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
