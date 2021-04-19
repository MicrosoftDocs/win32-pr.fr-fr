---
description: Définir les informations de mise à l’échelle d’une image clé spécifique dans l’ensemble d’animations.
ms.assetid: b606e5d3-11c9-4997-ad3c-d3ae21c32e10
title: 'ID3DXKeyframedAnimationSet :: SetScaleKey, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.SetScaleKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 12ac4d46a2719e452d44d2da67f178e6146b799b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539917"
---
# <a name="id3dxkeyframedanimationsetsetscalekey-method"></a><span data-ttu-id="5d132-103">ID3DXKeyframedAnimationSet :: SetScaleKey, méthode</span><span class="sxs-lookup"><span data-stu-id="5d132-103">ID3DXKeyframedAnimationSet::SetScaleKey method</span></span>

<span data-ttu-id="5d132-104">Définir les informations de mise à l’échelle d’une image clé spécifique dans l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="5d132-104">Set scale information for a specific key frame in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d132-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d132-105">Syntax</span></span>


```C++
HRESULT SetScaleKey(
  [in] UINT              Animation,
  [in] UINT              Key,
  [in] LPD3DXKEY_VECTOR3 pScaleKeys
);
```



## <a name="parameters"></a><span data-ttu-id="5d132-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d132-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d132-107">*Animation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5d132-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d132-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5d132-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5d132-109">Index d’animation.</span><span class="sxs-lookup"><span data-stu-id="5d132-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="5d132-110">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5d132-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d132-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5d132-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5d132-112">Image clé.</span><span class="sxs-lookup"><span data-stu-id="5d132-112">Key frame.</span></span>

</dd> <dt>

<span data-ttu-id="5d132-113">*pScaleKeys* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5d132-113">*pScaleKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d132-114">Type : **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**</span><span class="sxs-lookup"><span data-stu-id="5d132-114">Type: **[**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)**</span></span>

<span data-ttu-id="5d132-115">Pointeur vers les données de mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="5d132-115">Pointer to the scale data.</span></span> <span data-ttu-id="5d132-116">Consultez [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md).</span><span class="sxs-lookup"><span data-stu-id="5d132-116">See [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d132-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5d132-117">Return value</span></span>

<span data-ttu-id="5d132-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5d132-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5d132-119">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5d132-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5d132-120">Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="5d132-120">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d132-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d132-121">Requirements</span></span>



| <span data-ttu-id="5d132-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d132-122">Requirement</span></span> | <span data-ttu-id="5d132-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d132-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d132-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="5d132-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5d132-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d132-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="5d132-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5d132-126">Library</span></span><br/> | <dl> <span data-ttu-id="5d132-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d132-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5d132-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d132-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d132-129">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="5d132-129">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
