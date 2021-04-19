---
description: Enregistre les données de l’image clé de l’échelle, de rotation et de translation (SRT) pour une animation.
ms.assetid: 10e5b391-1529-4952-abbb-ef560a35d667
title: 'ID3DXKeyframedAnimationSet :: RegisterAnimationSRTKeys, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.RegisterAnimationSRTKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3098c8e779834daf273d5e85469e3f45b01cb039
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525297"
---
# <a name="id3dxkeyframedanimationsetregisteranimationsrtkeys-method"></a><span data-ttu-id="f083d-103">ID3DXKeyframedAnimationSet :: RegisterAnimationSRTKeys, méthode</span><span class="sxs-lookup"><span data-stu-id="f083d-103">ID3DXKeyframedAnimationSet::RegisterAnimationSRTKeys method</span></span>

<span data-ttu-id="f083d-104">Enregistre les données de l’image clé de l’échelle, de rotation et de translation (SRT) pour une animation.</span><span class="sxs-lookup"><span data-stu-id="f083d-104">Register the scale, rotate, and translate (SRT) key frame data for an animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="f083d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f083d-105">Syntax</span></span>


```C++
HRESULT RegisterAnimationSRTKeys(
  [in]        LPCSTR               pName,
  [in]        UINT                 NumScaleKeys,
  [in]        UINT                 NumRotationKeys,
  [in]        UINT                 NumTranslationKeys,
  [in]  const LPD3DXKEY_VECTOR3    *pScaleKeys,
  [in]  const LPD3DXKEY_QUATERNION *pRotationKeys,
  [in]  const LPD3DXKEY_VECTOR3    *pTranslationKeys,
  [out]       DWORD                *pAnimationIndex
);
```



## <a name="parameters"></a><span data-ttu-id="f083d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f083d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f083d-107">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f083d-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f083d-108">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f083d-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f083d-109">Pointeur vers le nom de l’animation.</span><span class="sxs-lookup"><span data-stu-id="f083d-109">Pointer to the animation name.</span></span>

</dd> <dt>

<span data-ttu-id="f083d-110">*NumScaleKeys* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f083d-110">*NumScaleKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f083d-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f083d-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f083d-112">Nombre de clés de mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="f083d-112">Number of scale keys.</span></span>

</dd> <dt>

<span data-ttu-id="f083d-113">*NumRotationKeys* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f083d-113">*NumRotationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f083d-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f083d-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f083d-115">Nombre de clés de rotation.</span><span class="sxs-lookup"><span data-stu-id="f083d-115">Number of rotation keys.</span></span>

</dd> <dt>

<span data-ttu-id="f083d-116">*NumTranslationKeys* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f083d-116">*NumTranslationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f083d-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f083d-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f083d-118">Nombre de clés de traduction.</span><span class="sxs-lookup"><span data-stu-id="f083d-118">Number of translation keys.</span></span>

</dd> <dt>

<span data-ttu-id="f083d-119">*pScaleKeys* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f083d-119">*pScaleKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f083d-120">Type : **const [**LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f083d-120">Type: **const [**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)\***</span></span>

<span data-ttu-id="f083d-121">Adresse d’un pointeur vers un tableau alloué par l’utilisateur de vecteurs [**\_ VECTOR3 D3DXKEY**](d3dxkey-vector3.md) que la méthode remplit avec les données de mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="f083d-121">Address of a pointer to a user-allocated array of [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md) vectors that the method fills with scale data.</span></span>

</dd> <dt>

<span data-ttu-id="f083d-122">*pRotationKeys* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f083d-122">*pRotationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f083d-123">Type : **const [**LPD3DXKEY \_ Quaternion**](d3dxkey-quaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="f083d-123">Type: **const [**LPD3DXKEY\_QUATERNION**](d3dxkey-quaternion.md)\***</span></span>

<span data-ttu-id="f083d-124">Adresse d’un pointeur vers un tableau alloué par l’utilisateur de quaternions [**D3DXKEY \_ Quaternion**](d3dxkey-quaternion.md) que la méthode remplit avec les données de rotation.</span><span class="sxs-lookup"><span data-stu-id="f083d-124">Address of a pointer to a user-allocated array of [**D3DXKEY\_QUATERNION**](d3dxkey-quaternion.md) quaternions that the method fills with rotation data.</span></span>

</dd> <dt>

<span data-ttu-id="f083d-125">*pTranslationKeys* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f083d-125">*pTranslationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f083d-126">Type : **const [**LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f083d-126">Type: **const [**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)\***</span></span>

<span data-ttu-id="f083d-127">Adresse d’un pointeur vers un tableau alloué par l’utilisateur de vecteurs [**\_ VECTOR3 D3DXKEY**](d3dxkey-vector3.md) que la méthode remplit avec les données de traduction.</span><span class="sxs-lookup"><span data-stu-id="f083d-127">Address of a pointer to a user-allocated array of [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md) vectors that the method fills with translation data.</span></span>

</dd> <dt>

<span data-ttu-id="f083d-128">*pAnimationIndex* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f083d-128">*pAnimationIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f083d-129">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f083d-129">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f083d-130">Retourne l’index d’animation.</span><span class="sxs-lookup"><span data-stu-id="f083d-130">Returns the animation index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f083d-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f083d-131">Return value</span></span>

<span data-ttu-id="f083d-132">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f083d-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f083d-133">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f083d-133">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f083d-134">Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="f083d-134">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="f083d-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f083d-135">Requirements</span></span>



| <span data-ttu-id="f083d-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f083d-136">Requirement</span></span> | <span data-ttu-id="f083d-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="f083d-137">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f083d-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="f083d-138">Header</span></span><br/>  | <dl> <span data-ttu-id="f083d-139"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="f083d-139"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="f083d-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f083d-140">Library</span></span><br/> | <dl> <span data-ttu-id="f083d-141"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f083d-141"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f083d-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f083d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f083d-143">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="f083d-143">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> <dt>

[<span data-ttu-id="f083d-144">**ID3DXKeyframedAnimationSet::GetNumScaleKeys**</span><span class="sxs-lookup"><span data-stu-id="f083d-144">**ID3DXKeyframedAnimationSet::GetNumScaleKeys**</span></span>](id3dxkeyframedanimationset--getnumscalekeys.md)
</dt> <dt>

[<span data-ttu-id="f083d-145">**ID3DXKeyframedAnimationSet::GetNumRotationKeys**</span><span class="sxs-lookup"><span data-stu-id="f083d-145">**ID3DXKeyframedAnimationSet::GetNumRotationKeys**</span></span>](id3dxkeyframedanimationset--getnumrotationkeys.md)
</dt> <dt>

[<span data-ttu-id="f083d-146">**ID3DXKeyframedAnimationSet::GetNumTranslationKeys**</span><span class="sxs-lookup"><span data-stu-id="f083d-146">**ID3DXKeyframedAnimationSet::GetNumTranslationKeys**</span></span>](id3dxkeyframedanimationset--getnumtranslationkeys.md)
</dt> </dl>

 

 
