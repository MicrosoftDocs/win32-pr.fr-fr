---
description: Supprime un événement spécifié d’une piste d’animation, empêchant ainsi l’exécution de l’événement.
ms.assetid: 658ffe91-44ba-4bde-b78c-c545dff27ab1
title: 'ID3DXAnimationController :: UnkeyEvent, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.UnkeyEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ac0c9d6a643337c43a5cadd5bcfe0b090cd39a00
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323354"
---
# <a name="id3dxanimationcontrollerunkeyevent-method"></a><span data-ttu-id="67ff5-103">ID3DXAnimationController :: UnkeyEvent, méthode</span><span class="sxs-lookup"><span data-stu-id="67ff5-103">ID3DXAnimationController::UnkeyEvent method</span></span>

<span data-ttu-id="67ff5-104">Supprime un événement spécifié d’une piste d’animation, empêchant ainsi l’exécution de l’événement.</span><span class="sxs-lookup"><span data-stu-id="67ff5-104">Removes a specified event from an animation track, preventing the execution of the event.</span></span>

## <a name="syntax"></a><span data-ttu-id="67ff5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="67ff5-105">Syntax</span></span>


```C++
HRESULT UnkeyEvent(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="67ff5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="67ff5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67ff5-107">*hEvent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="67ff5-107">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67ff5-108">Type : **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="67ff5-108">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="67ff5-109">Handle d’événement de l’événement à supprimer de la piste d’animation.</span><span class="sxs-lookup"><span data-stu-id="67ff5-109">Event handle to the event to be removed from the animation track.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67ff5-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="67ff5-110">Return value</span></span>

<span data-ttu-id="67ff5-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="67ff5-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="67ff5-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="67ff5-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="67ff5-113">Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="67ff5-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="67ff5-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="67ff5-114">Requirements</span></span>



| <span data-ttu-id="67ff5-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="67ff5-115">Requirement</span></span> | <span data-ttu-id="67ff5-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="67ff5-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="67ff5-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="67ff5-117">Header</span></span><br/>  | <dl> <span data-ttu-id="67ff5-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="67ff5-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="67ff5-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="67ff5-119">Library</span></span><br/> | <dl> <span data-ttu-id="67ff5-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="67ff5-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="67ff5-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67ff5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67ff5-122">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="67ff5-122">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




