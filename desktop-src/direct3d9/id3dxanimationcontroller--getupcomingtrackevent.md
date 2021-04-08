---
description: Retourne un handle d’événement pour l’événement suivant planifié pour se produire après un événement spécifié sur une piste d’animation.
ms.assetid: 616b2de1-6107-4d18-ad2e-de2ef4560aee
title: 'ID3DXAnimationController :: GetUpcomingTrackEvent, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetUpcomingTrackEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f863ce918f25c6b0975010f71a63f067c01f7345
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953806"
---
# <a name="id3dxanimationcontrollergetupcomingtrackevent-method"></a><span data-ttu-id="3c551-103">ID3DXAnimationController :: GetUpcomingTrackEvent, méthode</span><span class="sxs-lookup"><span data-stu-id="3c551-103">ID3DXAnimationController::GetUpcomingTrackEvent method</span></span>

<span data-ttu-id="3c551-104">Retourne un handle d’événement pour l’événement suivant planifié pour se produire après un événement spécifié sur une piste d’animation.</span><span class="sxs-lookup"><span data-stu-id="3c551-104">Returns an event handle to the next event scheduled to occur after a specified event on an animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c551-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c551-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE GetUpcomingTrackEvent(
  [in] UINT            Track,
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="3c551-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c551-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c551-107">*Suivre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c551-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c551-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3c551-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3c551-109">Identificateur de suivi.</span><span class="sxs-lookup"><span data-stu-id="3c551-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="3c551-110">*hEvent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c551-110">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c551-111">Type : **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="3c551-111">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="3c551-112">Handle d’événement vers un événement spécifié après lequel Rechercher un événement suivant.</span><span class="sxs-lookup"><span data-stu-id="3c551-112">Event handle to a specified event after which to search for a following event.</span></span> <span data-ttu-id="3c551-113">Si la valeur est **null**, la méthode retourne l’événement planifié suivant.</span><span class="sxs-lookup"><span data-stu-id="3c551-113">If set to **NULL**, then the method will return the next scheduled event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c551-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3c551-114">Return value</span></span>

<span data-ttu-id="3c551-115">Type : **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="3c551-115">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="3c551-116">Handle d’événement vers l’événement suivant planifié pour s’exécuter sur la piste spécifiée. La **valeur null** est retournée si aucun nouvel événement n’est planifié.</span><span class="sxs-lookup"><span data-stu-id="3c551-116">Event handle to the next event scheduled to run on the specified track. **NULL** is returned if no new event is scheduled.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c551-117">Notes</span><span class="sxs-lookup"><span data-stu-id="3c551-117">Remarks</span></span>

<span data-ttu-id="3c551-118">Cette méthode peut être utilisée de façon itérative pour localiser un événement souhaité en passant à plusieurs reprises la **valeur null** pour hEvent.</span><span class="sxs-lookup"><span data-stu-id="3c551-118">This method can be used iteratively to locate a desired event by repeatedly passing in **NULL** for hEvent.</span></span>

> [!Note]  
> <span data-ttu-id="3c551-119">N’effectuez pas d’itération après que la méthode a retourné la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="3c551-119">Do not iterate further after the method has returned **NULL**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3c551-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c551-120">Requirements</span></span>



| <span data-ttu-id="3c551-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c551-121">Requirement</span></span> | <span data-ttu-id="3c551-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c551-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c551-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="3c551-123">Header</span></span><br/>  | <dl> <span data-ttu-id="3c551-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c551-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="3c551-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3c551-125">Library</span></span><br/> | <dl> <span data-ttu-id="3c551-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c551-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3c551-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c551-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c551-128">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="3c551-128">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
