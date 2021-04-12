---
description: Définit des informations sur un rappel spécifique dans l’ensemble d’animations.
ms.assetid: 899f3a85-c878-4eeb-8bda-fc4e9083bd1f
title: 'ID3DXKeyframedAnimationSet :: SetCallbackKey, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.SetCallbackKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 49d3373e0ab0fa221e707ca6eda9ac9bb468a5a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211927"
---
# <a name="id3dxkeyframedanimationsetsetcallbackkey-method"></a><span data-ttu-id="90c51-103">ID3DXKeyframedAnimationSet :: SetCallbackKey, méthode</span><span class="sxs-lookup"><span data-stu-id="90c51-103">ID3DXKeyframedAnimationSet::SetCallbackKey method</span></span>

<span data-ttu-id="90c51-104">Définit des informations sur un rappel spécifique dans l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="90c51-104">Sets information about a specific callback in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="90c51-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="90c51-105">Syntax</span></span>


```C++
HRESULT SetCallbackKey(
  [in]  UINT               Animation,
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a><span data-ttu-id="90c51-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="90c51-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90c51-107">*Animation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="90c51-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90c51-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="90c51-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="90c51-109">Index d’animation.</span><span class="sxs-lookup"><span data-stu-id="90c51-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="90c51-110">*pCallbackKeys* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="90c51-110">*pCallbackKeys* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90c51-111">Type : **[ **\_ rappel LPD3DXKEY**](d3dxkey-callback.md)**</span><span class="sxs-lookup"><span data-stu-id="90c51-111">Type: **[**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)**</span></span>

<span data-ttu-id="90c51-112">Pointeur vers la [**fonction de rappel**](d3dxkey-callback.md).</span><span class="sxs-lookup"><span data-stu-id="90c51-112">Pointer to the [**callback function**](d3dxkey-callback.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90c51-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="90c51-113">Return value</span></span>

<span data-ttu-id="90c51-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="90c51-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="90c51-115">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="90c51-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="90c51-116">Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="90c51-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="90c51-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="90c51-117">Requirements</span></span>



| <span data-ttu-id="90c51-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="90c51-118">Requirement</span></span> | <span data-ttu-id="90c51-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="90c51-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="90c51-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="90c51-120">Header</span></span><br/>  | <dl> <span data-ttu-id="90c51-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="90c51-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="90c51-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="90c51-122">Library</span></span><br/> | <dl> <span data-ttu-id="90c51-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="90c51-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="90c51-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90c51-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90c51-125">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="90c51-125">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
