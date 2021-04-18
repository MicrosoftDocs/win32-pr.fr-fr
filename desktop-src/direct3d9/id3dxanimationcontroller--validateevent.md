---
description: Vérifie si un handle d’événement spécifié est valide et que l’événement d’animation n’est pas encore terminé.
ms.assetid: 242ad1e2-4b04-4ce1-9cdf-f66da9f83f06
title: 'ID3DXAnimationController :: ValidateEvent, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.ValidateEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e1a632fa867269f04e8f5f66e6bc352ef1701cd9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522996"
---
# <a name="id3dxanimationcontrollervalidateevent-method"></a><span data-ttu-id="d8e0c-103">ID3DXAnimationController :: ValidateEvent, méthode</span><span class="sxs-lookup"><span data-stu-id="d8e0c-103">ID3DXAnimationController::ValidateEvent method</span></span>

<span data-ttu-id="d8e0c-104">Vérifie si un handle d’événement spécifié est valide et que l’événement d’animation n’est pas encore terminé.</span><span class="sxs-lookup"><span data-stu-id="d8e0c-104">Checks whether a specified event handle is valid and the animation event has not yet completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8e0c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8e0c-105">Syntax</span></span>


```C++
HRESULT ValidateEvent(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="d8e0c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d8e0c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8e0c-107">*hEvent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d8e0c-107">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8e0c-108">Type : **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="d8e0c-108">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="d8e0c-109">Handle d’événement vers un événement d’animation.</span><span class="sxs-lookup"><span data-stu-id="d8e0c-109">Event handle to an animation event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8e0c-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d8e0c-110">Return value</span></span>

<span data-ttu-id="d8e0c-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d8e0c-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d8e0c-112">Retourne S \_ OK si le handle d’événement est valide et que l’événement n’est pas encore terminé.</span><span class="sxs-lookup"><span data-stu-id="d8e0c-112">Returns S\_OK if the event handle is valid and the event has not yet completed.</span></span>

<span data-ttu-id="d8e0c-113">Retourne E \_ Fail si le descripteur d’événement n’est pas valide et/ou si l’événement est terminé.</span><span class="sxs-lookup"><span data-stu-id="d8e0c-113">Returns E\_FAIL if the event handle is invalid and/or the event has completed.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8e0c-114">Notes</span><span class="sxs-lookup"><span data-stu-id="d8e0c-114">Remarks</span></span>

<span data-ttu-id="d8e0c-115">La méthode indique qu’un handle d’événement est valide même si l’événement est en cours d’exécution, mais n’est pas encore terminé.</span><span class="sxs-lookup"><span data-stu-id="d8e0c-115">The method will indicate that an event handle is valid even if the event is running but has not yet completed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8e0c-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8e0c-116">Requirements</span></span>



| <span data-ttu-id="d8e0c-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8e0c-117">Requirement</span></span> | <span data-ttu-id="d8e0c-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8e0c-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8e0c-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="d8e0c-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d8e0c-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8e0c-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="d8e0c-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d8e0c-121">Library</span></span><br/> | <dl> <span data-ttu-id="d8e0c-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8e0c-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d8e0c-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8e0c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8e0c-124">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="d8e0c-124">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




