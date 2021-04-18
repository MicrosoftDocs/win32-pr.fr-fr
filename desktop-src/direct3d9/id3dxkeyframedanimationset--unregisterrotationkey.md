---
description: Supprime les données de rotation au niveau de l’image clé spécifiée.
ms.assetid: 8e95d684-fa22-4eba-a721-e7551e8f393b
title: 'ID3DXKeyframedAnimationSet :: UnregisterRotationKey, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.UnregisterRotationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 420a15d0086f94def7db8c7d558640d03b69562f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106533718"
---
# <a name="id3dxkeyframedanimationsetunregisterrotationkey-method"></a><span data-ttu-id="5b0d2-103">ID3DXKeyframedAnimationSet :: UnregisterRotationKey, méthode</span><span class="sxs-lookup"><span data-stu-id="5b0d2-103">ID3DXKeyframedAnimationSet::UnregisterRotationKey method</span></span>

<span data-ttu-id="5b0d2-104">Supprime les données de rotation au niveau de l’image clé spécifiée.</span><span class="sxs-lookup"><span data-stu-id="5b0d2-104">Removes the rotation data at the specified key frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b0d2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5b0d2-105">Syntax</span></span>


```C++
HRESULT UnregisterRotationKey(
  [in] UINT Animation,
  [in] UINT Key
);
```



## <a name="parameters"></a><span data-ttu-id="5b0d2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5b0d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b0d2-107">*Animation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5b0d2-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b0d2-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5b0d2-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5b0d2-109">Identificateur d’animation.</span><span class="sxs-lookup"><span data-stu-id="5b0d2-109">Animation identifier.</span></span>

</dd> <dt>

<span data-ttu-id="5b0d2-110">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5b0d2-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b0d2-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5b0d2-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5b0d2-112">Image clé.</span><span class="sxs-lookup"><span data-stu-id="5b0d2-112">Key frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b0d2-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5b0d2-113">Return value</span></span>

<span data-ttu-id="5b0d2-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5b0d2-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5b0d2-115">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5b0d2-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5b0d2-116">Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="5b0d2-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b0d2-117">Notes</span><span class="sxs-lookup"><span data-stu-id="5b0d2-117">Remarks</span></span>

<span data-ttu-id="5b0d2-118">Cette méthode est lente et ne doit pas être utilisée une fois que l’animation a commencé à jouer.</span><span class="sxs-lookup"><span data-stu-id="5b0d2-118">This method is slow and should not be used after an animation has begun to play.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b0d2-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5b0d2-119">Requirements</span></span>



| <span data-ttu-id="5b0d2-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5b0d2-120">Requirement</span></span> | <span data-ttu-id="5b0d2-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b0d2-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b0d2-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="5b0d2-122">Header</span></span><br/>  | <dl> <span data-ttu-id="5b0d2-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b0d2-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="5b0d2-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5b0d2-124">Library</span></span><br/> | <dl> <span data-ttu-id="5b0d2-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5b0d2-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5b0d2-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5b0d2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b0d2-127">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="5b0d2-127">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
