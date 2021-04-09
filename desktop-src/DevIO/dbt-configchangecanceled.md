---
description: Le système diffuse l’événement de l' \_ appareil DBT CONFIGCHANGECANCELED lorsqu’une demande de modification de la configuration actuelle (ancrer ou détacher) a été annulée.
ms.assetid: b4b1455c-9a04-4fa0-a3fa-ed991f278c0c
title: Événement DBT_CONFIGCHANGECANCELED (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97944daa698808c55f88bc377c9bf1c59c1217fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861114"
---
# <a name="dbt_configchangecanceled-event"></a><span data-ttu-id="d0230-103">\_Événement DBT CONFIGCHANGECANCELED</span><span class="sxs-lookup"><span data-stu-id="d0230-103">DBT\_CONFIGCHANGECANCELED event</span></span>

<span data-ttu-id="d0230-104">Le système diffuse l’événement de l' \_ appareil DBT CONFIGCHANGECANCELED lorsqu’une demande de modification de la configuration actuelle (ancrer ou détacher) a été annulée.</span><span class="sxs-lookup"><span data-stu-id="d0230-104">The system broadcasts the DBT\_CONFIGCHANGECANCELED device event when a request to change the current configuration (dock or undock) has been canceled.</span></span>

<span data-ttu-id="d0230-105">Pour diffuser cet événement d’appareil, le système utilise le message [**WM \_ DEVICECHANGE**](wm-devicechange.md) avec *wParam* défini sur DBT \_ CONFIGCHANGECANCELED et *lParam* défini sur zéro.</span><span class="sxs-lookup"><span data-stu-id="d0230-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_CONFIGCHANGECANCELED and *lParam* set to zero.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="d0230-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0230-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0230-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="d0230-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="d0230-108">Handle d'une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d0230-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="d0230-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="d0230-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="d0230-110">Identificateur du message [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="d0230-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="d0230-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d0230-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0230-112">Définissez sur DBT \_ CONFIGCHANGECANCELED.</span><span class="sxs-lookup"><span data-stu-id="d0230-112">Set to DBT\_CONFIGCHANGECANCELED.</span></span>

</dd> <dt>

<span data-ttu-id="d0230-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d0230-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0230-114">Définit la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="d0230-114">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0230-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d0230-115">Return value</span></span>

<span data-ttu-id="d0230-116">Retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="d0230-116">Return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0230-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0230-117">Requirements</span></span>



| <span data-ttu-id="d0230-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d0230-118">Requirement</span></span> | <span data-ttu-id="d0230-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0230-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d0230-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0230-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d0230-121">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d0230-121">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="d0230-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0230-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d0230-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d0230-123">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="d0230-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="d0230-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0230-125"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0230-125"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0230-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0230-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0230-127">Événements de l’appareil</span><span class="sxs-lookup"><span data-stu-id="d0230-127">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="d0230-128">Événements de gestion des appareils</span><span class="sxs-lookup"><span data-stu-id="d0230-128">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="d0230-129">**\_DEVICECHANGE WM**</span><span class="sxs-lookup"><span data-stu-id="d0230-129">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




