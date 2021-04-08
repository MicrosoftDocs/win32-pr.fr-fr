---
description: Remplit un tableau avec les données de clé de rotation utilisées pour l’animation d’image clé.
ms.assetid: 9ae8bc28-d231-4d50-98f0-762b2d2c04e8
title: 'ID3DXKeyframedAnimationSet :: GetRotationKeys, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetRotationKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: af9242ccf75bc1e5443f040399ffbd8a939ed92e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762308"
---
# <a name="id3dxkeyframedanimationsetgetrotationkeys-method"></a><span data-ttu-id="c65ad-103">ID3DXKeyframedAnimationSet :: GetRotationKeys, méthode</span><span class="sxs-lookup"><span data-stu-id="c65ad-103">ID3DXKeyframedAnimationSet::GetRotationKeys method</span></span>

<span data-ttu-id="c65ad-104">Remplit un tableau avec les données de clé de rotation utilisées pour l’animation d’image clé.</span><span class="sxs-lookup"><span data-stu-id="c65ad-104">Fills an array with rotational key data used for key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="c65ad-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c65ad-105">Syntax</span></span>


```C++
HRESULT GetRotationKeys(
  [in] UINT                 Animation,
  [in] LPD3DXKEY_QUATERNION pRotationKeys
);
```



## <a name="parameters"></a><span data-ttu-id="c65ad-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c65ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c65ad-107">*Animation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c65ad-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c65ad-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c65ad-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c65ad-109">Index d’animation.</span><span class="sxs-lookup"><span data-stu-id="c65ad-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="c65ad-110">*pRotationKeys* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c65ad-110">*pRotationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c65ad-111">Type : **[ **LPD3DXKEY \_ Quaternion**](d3dxkey-quaternion.md)**</span><span class="sxs-lookup"><span data-stu-id="c65ad-111">Type: **[**LPD3DXKEY\_QUATERNION**](d3dxkey-quaternion.md)**</span></span>

<span data-ttu-id="c65ad-112">Pointeur vers un tableau alloué par l’utilisateur de quaternions [**D3DXKEY \_ Quaternion**](d3dxkey-quaternion.md) que la méthode doit remplir avec les données de rotation d’animation.</span><span class="sxs-lookup"><span data-stu-id="c65ad-112">Pointer to a user-allocated array of [**D3DXKEY\_QUATERNION**](d3dxkey-quaternion.md) quaternions that the method is to fill with animation rotation data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c65ad-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c65ad-113">Return value</span></span>

<span data-ttu-id="c65ad-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c65ad-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c65ad-115">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c65ad-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c65ad-116">Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="c65ad-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="c65ad-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c65ad-117">Requirements</span></span>



| <span data-ttu-id="c65ad-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c65ad-118">Requirement</span></span> | <span data-ttu-id="c65ad-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="c65ad-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c65ad-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="c65ad-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c65ad-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="c65ad-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="c65ad-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c65ad-122">Library</span></span><br/> | <dl> <span data-ttu-id="c65ad-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c65ad-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c65ad-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c65ad-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c65ad-125">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="c65ad-125">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> <dt>

[<span data-ttu-id="c65ad-126">**ID3DXKeyframedAnimationSet::GetNumRotationKeys**</span><span class="sxs-lookup"><span data-stu-id="c65ad-126">**ID3DXKeyframedAnimationSet::GetNumRotationKeys**</span></span>](id3dxkeyframedanimationset--getnumrotationkeys.md)
</dt> </dl>

 

 
