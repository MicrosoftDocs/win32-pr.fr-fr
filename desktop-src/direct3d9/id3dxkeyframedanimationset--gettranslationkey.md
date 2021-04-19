---
description: Obtenir des informations de traduction pour une image clé spécifique dans l’ensemble d’animations.
ms.assetid: 757af408-8a9c-4294-9343-91f52d4cc1ab
title: 'ID3DXKeyframedAnimationSet :: GetTranslationKey, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetTranslationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f61d1caecb46477d16be4367588ab5609bfd6224
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106545312"
---
# <a name="id3dxkeyframedanimationsetgettranslationkey-method"></a><span data-ttu-id="8137d-103">ID3DXKeyframedAnimationSet :: GetTranslationKey, méthode</span><span class="sxs-lookup"><span data-stu-id="8137d-103">ID3DXKeyframedAnimationSet::GetTranslationKey method</span></span>

<span data-ttu-id="8137d-104">Obtenir des informations de traduction pour une image clé spécifique dans l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="8137d-104">Get translation information for a specific key frame in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="8137d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8137d-105">Syntax</span></span>


```C++
HRESULT GetTranslationKey(
  [in]  UINT              Animation,
  [in]  UINT              Key,
  [out] LPD3DXKEY_VECTOR3 pTranslationKey
);
```



## <a name="parameters"></a><span data-ttu-id="8137d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8137d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8137d-107">*Animation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8137d-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8137d-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8137d-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8137d-109">Index d’animation.</span><span class="sxs-lookup"><span data-stu-id="8137d-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="8137d-110">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8137d-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8137d-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8137d-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8137d-112">Image clé.</span><span class="sxs-lookup"><span data-stu-id="8137d-112">Key Frame.</span></span>

</dd> <dt>

<span data-ttu-id="8137d-113">*pTranslationKey* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8137d-113">*pTranslationKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8137d-114">Type : **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**</span><span class="sxs-lookup"><span data-stu-id="8137d-114">Type: **[**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)**</span></span>

<span data-ttu-id="8137d-115">Pointeur vers les informations de rotation.</span><span class="sxs-lookup"><span data-stu-id="8137d-115">Pointer to the rotation information.</span></span> <span data-ttu-id="8137d-116">Consultez [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md).</span><span class="sxs-lookup"><span data-stu-id="8137d-116">See [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8137d-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8137d-117">Return value</span></span>

<span data-ttu-id="8137d-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8137d-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8137d-119">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8137d-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="8137d-120">Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="8137d-120">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="8137d-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8137d-121">Requirements</span></span>



| <span data-ttu-id="8137d-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8137d-122">Requirement</span></span> | <span data-ttu-id="8137d-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="8137d-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8137d-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="8137d-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8137d-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="8137d-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="8137d-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8137d-126">Library</span></span><br/> | <dl> <span data-ttu-id="8137d-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8137d-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8137d-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8137d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8137d-129">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="8137d-129">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
