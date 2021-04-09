---
description: Le système diffuse l’événement de l' \_ appareil DBT DEVNODES \_ Changed lorsqu’un appareil a été ajouté ou supprimé du système. Les applications qui maintiennent des listes d’appareils dans le système doivent actualiser leurs listes.
ms.assetid: 62acc633-7dad-4792-a5a2-1f95356479d1
title: Événement DBT_DEVNODES_CHANGED (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1450e9a87d541e5df3d9a9286e48601697e6aaae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110694"
---
# <a name="dbt_devnodes_changed-event"></a><span data-ttu-id="c9497-104">\_Événement DBT DEVNODES \_ Changed</span><span class="sxs-lookup"><span data-stu-id="c9497-104">DBT\_DEVNODES\_CHANGED event</span></span>

<span data-ttu-id="c9497-105">Le système diffuse l’événement de l' \_ appareil DBT DEVNODES \_ Changed lorsqu’un appareil a été ajouté ou supprimé du système.</span><span class="sxs-lookup"><span data-stu-id="c9497-105">The system broadcasts the DBT\_DEVNODES\_CHANGED device event when a device has been added to or removed from the system.</span></span> <span data-ttu-id="c9497-106">Les applications qui maintiennent des listes d’appareils dans le système doivent actualiser leurs listes.</span><span class="sxs-lookup"><span data-stu-id="c9497-106">Applications that maintain lists of devices in the system should refresh their lists.</span></span>

<span data-ttu-id="c9497-107">Pour diffuser cet événement d’appareil, le système utilise le message [**WM \_ DEVICECHANGE**](wm-devicechange.md) avec *wParam* défini sur DBT \_ DEVNODES \_ Changed et *lParam* défini sur zéro.</span><span class="sxs-lookup"><span data-stu-id="c9497-107">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVNODES\_CHANGED and *lParam* set to zero.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="c9497-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9497-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9497-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="c9497-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="c9497-110">Handle d'une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c9497-110">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="c9497-111">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="c9497-111">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="c9497-112">Identificateur du message [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="c9497-112">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="c9497-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c9497-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c9497-114">Défini sur DBT \_ DEVNODES \_ Changed.</span><span class="sxs-lookup"><span data-stu-id="c9497-114">Set to DBT\_DEVNODES\_CHANGED.</span></span>

</dd> <dt>

<span data-ttu-id="c9497-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c9497-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c9497-116">Définit la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="c9497-116">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9497-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c9497-117">Return value</span></span>

<span data-ttu-id="c9497-118">Retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="c9497-118">Return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9497-119">Notes</span><span class="sxs-lookup"><span data-stu-id="c9497-119">Remarks</span></span>

<span data-ttu-id="c9497-120">Il n’y a pas d’informations supplémentaires sur l’appareil qui a été ajouté ou supprimé du système.</span><span class="sxs-lookup"><span data-stu-id="c9497-120">There is no additional information about which device has been added to or removed from the system.</span></span> <span data-ttu-id="c9497-121">Les applications qui requièrent plus d’informations doivent s’inscrire à la notification de l’appareil à l’aide de la fonction [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) .</span><span class="sxs-lookup"><span data-stu-id="c9497-121">Applications that require more information should register for device notification using the [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9497-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9497-122">Requirements</span></span>



| <span data-ttu-id="c9497-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9497-123">Requirement</span></span> | <span data-ttu-id="c9497-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9497-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c9497-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9497-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c9497-126">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c9497-126">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="c9497-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9497-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c9497-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c9497-128">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="c9497-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="c9497-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9497-130"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9497-130"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9497-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9497-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9497-132">Événements de l’appareil</span><span class="sxs-lookup"><span data-stu-id="c9497-132">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="c9497-133">Événements de gestion des appareils</span><span class="sxs-lookup"><span data-stu-id="c9497-133">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="c9497-134">**\_HDR de diffusion dev \_**</span><span class="sxs-lookup"><span data-stu-id="c9497-134">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="c9497-135">**\_DEVICECHANGE WM**</span><span class="sxs-lookup"><span data-stu-id="c9497-135">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




