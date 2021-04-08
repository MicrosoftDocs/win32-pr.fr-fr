---
description: Événement de modification du paramètre d’alimentation envoyé avec un \_ message de fenêtre WM POWERBROADCAST ou dans un rappel de notification HandlerEx pour les services.
ms.assetid: 0bcadb85-47c5-48a9-b3f9-f0a1ca60b503
title: Événement PBT_POWERSETTINGCHANGE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f38486d2e5cce1cfe541468e548e92353c9837
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865069"
---
# <a name="pbt_powersettingchange-event"></a><span data-ttu-id="6e7fc-103">\_Événement PBT POWERSETTINGCHANGE</span><span class="sxs-lookup"><span data-stu-id="6e7fc-103">PBT\_POWERSETTINGCHANGE event</span></span>

<span data-ttu-id="6e7fc-104">Événement de modification du paramètre d’alimentation envoyé avec un message de fenêtre [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) ou dans un rappel de notification [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) pour les services.</span><span class="sxs-lookup"><span data-stu-id="6e7fc-104">Power setting change event sent with a [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) window message or in a [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) notification callback for services.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_POWERSETTINGCHANGE
            LPARAM lParam); // Pointer to POWERBROADCAST_SETTING
```



## <a name="parameters"></a><span data-ttu-id="6e7fc-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6e7fc-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e7fc-106">*HWND*</span><span class="sxs-lookup"><span data-stu-id="6e7fc-106">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="6e7fc-107">Handle de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6e7fc-107">A handle to window.</span></span>

<span data-ttu-id="6e7fc-108"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="6e7fc-108"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="6e7fc-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="6e7fc-109">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="6e7fc-110">Signification</span><span class="sxs-lookup"><span data-stu-id="6e7fc-110">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="6e7fc-111"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="6e7fc-111"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="6e7fc-112">Identificateur du message.</span><span class="sxs-lookup"><span data-stu-id="6e7fc-112">Message identifier.</span></span><br/> |



 

<span data-ttu-id="6e7fc-113"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="6e7fc-113"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="6e7fc-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="6e7fc-114">Value</span></span>                                                                                                                                                                                                                                                        | <span data-ttu-id="6e7fc-115">Signification</span><span class="sxs-lookup"><span data-stu-id="6e7fc-115">Meaning</span></span>                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_POWERSETTINGCHANGE"></span><span id="pbt_powersettingchange"></span><dl> <span data-ttu-id="6e7fc-116"><dt>**PBT \_ POWERSETTINGCHANGE**</dt> <dt>32787 (0x8013)</dt></span><span class="sxs-lookup"><span data-stu-id="6e7fc-116"><dt>**PBT\_POWERSETTINGCHANGE**</dt> <dt>32787 (0x8013)</dt></span></span> </dl> | <span data-ttu-id="6e7fc-117">Identificateur d’événement.</span><span class="sxs-lookup"><span data-stu-id="6e7fc-117">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6e7fc-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6e7fc-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6e7fc-119">Pointeur vers une structure de [**\_ paramètre POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) .</span><span class="sxs-lookup"><span data-stu-id="6e7fc-119">Pointer to a [**POWERBROADCAST\_SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e7fc-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6e7fc-120">Return value</span></span>

<span data-ttu-id="6e7fc-121">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="6e7fc-121">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e7fc-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6e7fc-122">Requirements</span></span>



| <span data-ttu-id="6e7fc-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6e7fc-123">Requirement</span></span> | <span data-ttu-id="6e7fc-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="6e7fc-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e7fc-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e7fc-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6e7fc-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e7fc-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6e7fc-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e7fc-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6e7fc-128">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e7fc-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6e7fc-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="6e7fc-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e7fc-130"><dt>WinUser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6e7fc-130"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e7fc-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e7fc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e7fc-132">Événements de gestion de l’alimentation</span><span class="sxs-lookup"><span data-stu-id="6e7fc-132">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="6e7fc-133">**HandlerEx**</span><span class="sxs-lookup"><span data-stu-id="6e7fc-133">**HandlerEx**</span></span>](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex)
</dt> <dt>

[<span data-ttu-id="6e7fc-134">**\_POWERBROADCAST WM**</span><span class="sxs-lookup"><span data-stu-id="6e7fc-134">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> <dt>

[<span data-ttu-id="6e7fc-135">**\_paramètre POWERBROADCAST**</span><span class="sxs-lookup"><span data-stu-id="6e7fc-135">**POWERBROADCAST\_SETTING**</span></span>](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting)
</dt> </dl>

 

