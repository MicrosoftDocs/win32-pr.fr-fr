---
description: Obtient des informations de rotation pour une image clé spécifique dans l’ensemble d’animations.
ms.assetid: d62b8d5e-328e-4227-b2e8-cb6e5ccc4b3f
title: 'ID3DXKeyframedAnimationSet :: GetRotationKey, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetRotationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8f5bf30eaf261e4baa032ed1411b3d70bddc706c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762313"
---
# <a name="id3dxkeyframedanimationsetgetrotationkey-method"></a><span data-ttu-id="689b4-103">ID3DXKeyframedAnimationSet :: GetRotationKey, méthode</span><span class="sxs-lookup"><span data-stu-id="689b4-103">ID3DXKeyframedAnimationSet::GetRotationKey method</span></span>

<span data-ttu-id="689b4-104">Obtient des informations de rotation pour une image clé spécifique dans l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="689b4-104">Get rotation information for a specific key frame in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="689b4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="689b4-105">Syntax</span></span>


```C++
HRESULT GetRotationKey(
  [in] UINT                 Animation,
  [in] UINT                 Key,
  [in] LPD3DXKEY_QUATERNION pRotationKeys
);
```



## <a name="parameters"></a><span data-ttu-id="689b4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="689b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="689b4-107">*Animation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="689b4-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="689b4-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="689b4-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="689b4-109">Index d’animation.</span><span class="sxs-lookup"><span data-stu-id="689b4-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="689b4-110">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="689b4-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="689b4-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="689b4-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="689b4-112">Image clé.</span><span class="sxs-lookup"><span data-stu-id="689b4-112">Key frame.</span></span>

</dd> <dt>

<span data-ttu-id="689b4-113">*pRotationKeys* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="689b4-113">*pRotationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="689b4-114">Type : **[ **LPD3DXKEY \_ Quaternion**](d3dxkey-quaternion.md)**</span><span class="sxs-lookup"><span data-stu-id="689b4-114">Type: **[**LPD3DXKEY\_QUATERNION**](d3dxkey-quaternion.md)**</span></span>

<span data-ttu-id="689b4-115">Pointeur vers les données de rotation.</span><span class="sxs-lookup"><span data-stu-id="689b4-115">Pointer to the rotation data.</span></span> <span data-ttu-id="689b4-116">Consultez [**D3DXKEY \_ Quaternion**](d3dxkey-quaternion.md).</span><span class="sxs-lookup"><span data-stu-id="689b4-116">See [**D3DXKEY\_QUATERNION**](d3dxkey-quaternion.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="689b4-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="689b4-117">Return value</span></span>

<span data-ttu-id="689b4-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="689b4-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="689b4-119">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="689b4-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="689b4-120">Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="689b4-120">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="689b4-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="689b4-121">Requirements</span></span>



| <span data-ttu-id="689b4-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="689b4-122">Requirement</span></span> | <span data-ttu-id="689b4-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="689b4-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="689b4-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="689b4-124">Header</span></span><br/>  | <dl> <span data-ttu-id="689b4-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="689b4-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="689b4-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="689b4-126">Library</span></span><br/> | <dl> <span data-ttu-id="689b4-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="689b4-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="689b4-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="689b4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="689b4-129">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="689b4-129">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
