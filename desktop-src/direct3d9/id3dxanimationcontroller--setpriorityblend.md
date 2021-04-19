---
description: Définit le poids de fusion des priorités utilisé par le contrôleur d’animation.
ms.assetid: b053024b-f219-48b3-906e-161d9cf47556
title: 'ID3DXAnimationController :: SetPriorityBlend, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a4c820858041c730f971ce2821698f86e6ff2c31
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535833"
---
# <a name="id3dxanimationcontrollersetpriorityblend-method"></a><span data-ttu-id="52adb-103">ID3DXAnimationController :: SetPriorityBlend, méthode</span><span class="sxs-lookup"><span data-stu-id="52adb-103">ID3DXAnimationController::SetPriorityBlend method</span></span>

<span data-ttu-id="52adb-104">Définit le poids de fusion des priorités utilisé par le contrôleur d’animation.</span><span class="sxs-lookup"><span data-stu-id="52adb-104">Sets the priority blending weight used by the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="52adb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="52adb-105">Syntax</span></span>


```C++
HRESULT SetPriorityBlend(
  [in] FLOAT BlendWeight
);
```



## <a name="parameters"></a><span data-ttu-id="52adb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="52adb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52adb-107">*BlendWeight* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="52adb-107">*BlendWeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52adb-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="52adb-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="52adb-109">Poids de fusion des priorités utilisé par le contrôleur d’animation.</span><span class="sxs-lookup"><span data-stu-id="52adb-109">Priority blending weight used by the animation controller.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52adb-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="52adb-110">Return value</span></span>

<span data-ttu-id="52adb-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="52adb-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="52adb-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="52adb-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="52adb-113">Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="52adb-113">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="52adb-114">Notes</span><span class="sxs-lookup"><span data-stu-id="52adb-114">Remarks</span></span>

<span data-ttu-id="52adb-115">Le poids de fusion est utilisé pour fusionner les pistes de priorité haute et basse.</span><span class="sxs-lookup"><span data-stu-id="52adb-115">The blend weight is used to blend high and low priority tracks together.</span></span>

## <a name="requirements"></a><span data-ttu-id="52adb-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="52adb-116">Requirements</span></span>



| <span data-ttu-id="52adb-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="52adb-117">Requirement</span></span> | <span data-ttu-id="52adb-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="52adb-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="52adb-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="52adb-119">Header</span></span><br/>  | <dl> <span data-ttu-id="52adb-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="52adb-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="52adb-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="52adb-121">Library</span></span><br/> | <dl> <span data-ttu-id="52adb-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52adb-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="52adb-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52adb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52adb-124">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="52adb-124">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> <dt>

[<span data-ttu-id="52adb-125">**GetPriorityBlend**</span><span class="sxs-lookup"><span data-stu-id="52adb-125">**GetPriorityBlend**</span></span>](id3dxanimationcontroller--getpriorityblend.md)
</dt> </dl>

 

 
