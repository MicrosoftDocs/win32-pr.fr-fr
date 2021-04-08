---
description: Définissez les informations de rotation pour une image clé spécifique dans l’ensemble d’animations.
ms.assetid: b31edc88-0d77-49f3-b4c4-39cd866e1379
title: 'ID3DXKeyframedAnimationSet :: SetRotationKey, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.SetRotationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b03a6818a6a59904c3db5b4819775d9e58d4f8ec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043172"
---
# <a name="id3dxkeyframedanimationsetsetrotationkey-method"></a><span data-ttu-id="f3723-103">ID3DXKeyframedAnimationSet :: SetRotationKey, méthode</span><span class="sxs-lookup"><span data-stu-id="f3723-103">ID3DXKeyframedAnimationSet::SetRotationKey method</span></span>

<span data-ttu-id="f3723-104">Définissez les informations de rotation pour une image clé spécifique dans l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="f3723-104">Set rotation information for a specific key frame in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3723-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f3723-105">Syntax</span></span>


```C++
HRESULT SetRotationKey(
  [in] UINT                 Animation,
  [in] UINT                 Key,
  [in] LPD3DXKEY_QUATERNION pRotationKeys
);
```



## <a name="parameters"></a><span data-ttu-id="f3723-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f3723-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3723-107">*Animation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f3723-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3723-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f3723-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f3723-109">Index d’animation.</span><span class="sxs-lookup"><span data-stu-id="f3723-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="f3723-110">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f3723-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3723-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f3723-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f3723-112">Image clé.</span><span class="sxs-lookup"><span data-stu-id="f3723-112">Key frame.</span></span>

</dd> <dt>

<span data-ttu-id="f3723-113">*pRotationKeys* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f3723-113">*pRotationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3723-114">Type : **[ **LPD3DXKEY \_ Quaternion**](d3dxkey-quaternion.md)**</span><span class="sxs-lookup"><span data-stu-id="f3723-114">Type: **[**LPD3DXKEY\_QUATERNION**](d3dxkey-quaternion.md)**</span></span>

<span data-ttu-id="f3723-115">Pointeur vers les données de rotation.</span><span class="sxs-lookup"><span data-stu-id="f3723-115">Pointer to the rotation data.</span></span> <span data-ttu-id="f3723-116">Consultez [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md).</span><span class="sxs-lookup"><span data-stu-id="f3723-116">See [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3723-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f3723-117">Return value</span></span>

<span data-ttu-id="f3723-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f3723-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f3723-119">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f3723-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f3723-120">Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="f3723-120">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3723-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f3723-121">Requirements</span></span>



| <span data-ttu-id="f3723-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f3723-122">Requirement</span></span> | <span data-ttu-id="f3723-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3723-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3723-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="f3723-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f3723-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3723-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="f3723-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f3723-126">Library</span></span><br/> | <dl> <span data-ttu-id="f3723-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3723-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f3723-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3723-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3723-129">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="f3723-129">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
