---
description: Remplit un tableau avec les données de la clé de mise à l’échelle utilisées pour l’animation d’image clé.
ms.assetid: 0d595510-6d8c-4bc9-b5ca-0d6f73be3439
title: 'ID3DXKeyframedAnimationSet :: GetScaleKeys, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetScaleKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 88c907bc9b45b1203917b092f565096be3ed1fb6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525298"
---
# <a name="id3dxkeyframedanimationsetgetscalekeys-method"></a><span data-ttu-id="56371-103">ID3DXKeyframedAnimationSet :: GetScaleKeys, méthode</span><span class="sxs-lookup"><span data-stu-id="56371-103">ID3DXKeyframedAnimationSet::GetScaleKeys method</span></span>

<span data-ttu-id="56371-104">Remplit un tableau avec les données de la clé de mise à l’échelle utilisées pour l’animation d’image clé.</span><span class="sxs-lookup"><span data-stu-id="56371-104">Fills an array with scale key data used for key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="56371-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56371-105">Syntax</span></span>


```C++
HRESULT GetScaleKeys(
  [in] UINT              Animation,
  [in] LPD3DXKEY_VECTOR3 pScaleKeys
);
```



## <a name="parameters"></a><span data-ttu-id="56371-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56371-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56371-107">*Animation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="56371-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56371-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="56371-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="56371-109">Index d’animation.</span><span class="sxs-lookup"><span data-stu-id="56371-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="56371-110">*pScaleKeys* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="56371-110">*pScaleKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56371-111">Type : **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**</span><span class="sxs-lookup"><span data-stu-id="56371-111">Type: **[**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)**</span></span>

<span data-ttu-id="56371-112">Pointeur vers un tableau alloué par l’utilisateur de vecteurs [**\_ VECTOR3 D3DXKEY**](d3dxkey-vector3.md) que la méthode doit remplir avec les données de mise à l’échelle de l’animation.</span><span class="sxs-lookup"><span data-stu-id="56371-112">Pointer to a user-allocated array of [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md) vectors that the method is to fill with animation scale data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56371-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="56371-113">Return value</span></span>

<span data-ttu-id="56371-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="56371-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="56371-115">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="56371-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="56371-116">Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="56371-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="56371-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56371-117">Requirements</span></span>



| <span data-ttu-id="56371-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56371-118">Requirement</span></span> | <span data-ttu-id="56371-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="56371-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="56371-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="56371-120">Header</span></span><br/>  | <dl> <span data-ttu-id="56371-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="56371-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="56371-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="56371-122">Library</span></span><br/> | <dl> <span data-ttu-id="56371-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="56371-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="56371-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56371-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56371-125">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="56371-125">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> <dt>

[<span data-ttu-id="56371-126">**ID3DXKeyframedAnimationSet::GetNumScaleKeys**</span><span class="sxs-lookup"><span data-stu-id="56371-126">**ID3DXKeyframedAnimationSet::GetNumScaleKeys**</span></span>](id3dxkeyframedanimationset--getnumscalekeys.md)
</dt> </dl>

 

 
