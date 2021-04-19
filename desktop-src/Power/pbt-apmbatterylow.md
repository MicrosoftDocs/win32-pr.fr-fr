---
description: Avertit les applications que la puissance de la batterie est faible.
ms.assetid: ef24b8cf-d801-4452-a03c-3f2bdbdd7e5d
title: Événement PBT_APMBATTERYLOW (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64884f9bb01e37883e1be61b2de88862e8b119fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531940"
---
# <a name="pbt_apmbatterylow-event"></a><span data-ttu-id="a3072-103">\_Événement PBT APMBATTERYLOW</span><span class="sxs-lookup"><span data-stu-id="a3072-103">PBT\_APMBATTERYLOW event</span></span>

<span data-ttu-id="a3072-104">\[PBT \_ APMBATTERYLOW peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="a3072-104">\[PBT\_APMBATTERYLOW is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a3072-105">La prise en charge de cet événement a été supprimée dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a3072-105">Support for this event was removed in Windows Vista.</span></span> <span data-ttu-id="a3072-106">Utilisez [PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) à la place.\]</span><span class="sxs-lookup"><span data-stu-id="a3072-106">Use [PBT\_APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) instead.\]</span></span>

<span data-ttu-id="a3072-107">Avertit les applications que la puissance de la batterie est faible.</span><span class="sxs-lookup"><span data-stu-id="a3072-107">Notifies applications that the battery power is low.</span></span>

<span data-ttu-id="a3072-108">Une fenêtre reçoit cet événement par le biais du message [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="a3072-108">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="a3072-109">Les paramètres *wParam* et *lParam* sont définis comme suit.</span><span class="sxs-lookup"><span data-stu-id="a3072-109">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMBATTERYLOW
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="a3072-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a3072-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3072-111">*HWND*</span><span class="sxs-lookup"><span data-stu-id="a3072-111">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="a3072-112">Handle de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="a3072-112">A handle to the window.</span></span>

<span data-ttu-id="a3072-113"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="a3072-113"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="a3072-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3072-114">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="a3072-115">Signification</span><span class="sxs-lookup"><span data-stu-id="a3072-115">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="a3072-116"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="a3072-116"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="a3072-117">Identificateur du message.</span><span class="sxs-lookup"><span data-stu-id="a3072-117">Message identifier.</span></span><br/> |



 

<span data-ttu-id="a3072-118"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="a3072-118"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="a3072-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3072-119">Value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="a3072-120">Signification</span><span class="sxs-lookup"><span data-stu-id="a3072-120">Meaning</span></span>                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMBATTERYLOW"></span><span id="pbt_apmbatterylow"></span><dl> <span data-ttu-id="a3072-121"><dt>**PBT \_ APMBATTERYLOW**</dt> <dt>9 (0x9)</dt></span><span class="sxs-lookup"><span data-stu-id="a3072-121"><dt>**PBT\_APMBATTERYLOW**</dt> <dt>9 (0x9)</dt></span></span> </dl> | <span data-ttu-id="a3072-122">Identificateur d’événement.</span><span class="sxs-lookup"><span data-stu-id="a3072-122">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a3072-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a3072-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a3072-124">Réservé, doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="a3072-124">Reserved, must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3072-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a3072-125">Return value</span></span>

<span data-ttu-id="a3072-126">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="a3072-126">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3072-127">Notes</span><span class="sxs-lookup"><span data-stu-id="a3072-127">Remarks</span></span>

<span data-ttu-id="a3072-128">Cet événement est diffusé quand le BIOS APM d’un système signale une notification Low de batterie APM faible.</span><span class="sxs-lookup"><span data-stu-id="a3072-128">This event is broadcast when a system's APM BIOS signals an APM battery low notification.</span></span> <span data-ttu-id="a3072-129">Étant donné que certaines implémentations du BIOS APM ne fournissent pas de notifications lorsque les batteries sont faibles, cet événement peut ne jamais être diffusé sur certains ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="a3072-129">Because some APM BIOS implementations do not provide notifications when batteries are low, this event may never be broadcast on some computers.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3072-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a3072-130">Requirements</span></span>



| <span data-ttu-id="a3072-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a3072-131">Requirement</span></span> | <span data-ttu-id="a3072-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3072-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3072-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3072-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a3072-134">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a3072-134">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a3072-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3072-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a3072-136">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a3072-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a3072-137">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="a3072-137">End of client support</span></span><br/>    | <span data-ttu-id="a3072-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a3072-138">Windows XP</span></span><br/>                                                                                    |
| <span data-ttu-id="a3072-139">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="a3072-139">End of server support</span></span><br/>    | <span data-ttu-id="a3072-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a3072-140">Windows Server 2003</span></span><br/>                                                                           |
| <span data-ttu-id="a3072-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="a3072-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3072-142"><dt>WinUser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a3072-142"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3072-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3072-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3072-144">Événements de gestion de l’alimentation</span><span class="sxs-lookup"><span data-stu-id="a3072-144">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="a3072-145">**\_POWERBROADCAST WM**</span><span class="sxs-lookup"><span data-stu-id="a3072-145">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




