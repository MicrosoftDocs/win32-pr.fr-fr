---
description: Obtient des informations sur un rappel spécifique dans l’ensemble d’animations.
ms.assetid: a1d3ca96-2852-420a-aa5c-a434970e5523
title: 'ID3DXKeyframedAnimationSet :: GetCallbackKey, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetCallbackKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 95a3f5a97b84862a66d18b60a3776e183df36444
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106542194"
---
# <a name="id3dxkeyframedanimationsetgetcallbackkey-method"></a><span data-ttu-id="c228f-103">ID3DXKeyframedAnimationSet :: GetCallbackKey, méthode</span><span class="sxs-lookup"><span data-stu-id="c228f-103">ID3DXKeyframedAnimationSet::GetCallbackKey method</span></span>

<span data-ttu-id="c228f-104">Obtient des informations sur un rappel spécifique dans l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="c228f-104">Gets information about a specific callback in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="c228f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c228f-105">Syntax</span></span>


```C++
HRESULT GetCallbackKey(
  [in]  UINT               Animation,
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a><span data-ttu-id="c228f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c228f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c228f-107">*Animation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c228f-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c228f-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c228f-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c228f-109">Index d’animation.</span><span class="sxs-lookup"><span data-stu-id="c228f-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="c228f-110">*pCallbackKeys* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c228f-110">*pCallbackKeys* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c228f-111">Type : **[ **\_ rappel LPD3DXKEY**](d3dxkey-callback.md)**</span><span class="sxs-lookup"><span data-stu-id="c228f-111">Type: **[**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)**</span></span>

<span data-ttu-id="c228f-112">Pointeur vers la [**fonction de rappel**](d3dxkey-callback.md).</span><span class="sxs-lookup"><span data-stu-id="c228f-112">Pointer to the [**callback function**](d3dxkey-callback.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c228f-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c228f-113">Return value</span></span>

<span data-ttu-id="c228f-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c228f-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c228f-115">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c228f-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c228f-116">Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="c228f-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="c228f-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c228f-117">Requirements</span></span>



| <span data-ttu-id="c228f-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c228f-118">Requirement</span></span> | <span data-ttu-id="c228f-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="c228f-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c228f-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="c228f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c228f-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="c228f-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="c228f-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c228f-122">Library</span></span><br/> | <dl> <span data-ttu-id="c228f-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c228f-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c228f-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c228f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c228f-125">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="c228f-125">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
