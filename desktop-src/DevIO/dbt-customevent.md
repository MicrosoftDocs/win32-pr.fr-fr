---
description: Le système envoie l' \_ événement d’appareil DBT CUSTOMEVENT lorsqu’un événement personnalisé défini par le pilote s’est produit.
ms.assetid: 6e66fa93-0cd7-4202-83eb-cddc668525ae
title: Événement DBT_CUSTOMEVENT (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 777049a0a94b16450ed9ee8567f3fc6506e47174
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748364"
---
# <a name="dbt_customevent-event"></a><span data-ttu-id="eddf6-103">\_Événement DBT CUSTOMEVENT</span><span class="sxs-lookup"><span data-stu-id="eddf6-103">DBT\_CUSTOMEVENT event</span></span>

<span data-ttu-id="eddf6-104">Le système envoie l' \_ événement d’appareil DBT CUSTOMEVENT lorsqu’un événement personnalisé défini par le pilote s’est produit.</span><span class="sxs-lookup"><span data-stu-id="eddf6-104">The system sends the DBT\_CUSTOMEVENT device event when a driver-defined custom event has occurred.</span></span>

<span data-ttu-id="eddf6-105">Pour diffuser cet événement d’appareil, le système utilise le message [**WM \_ DEVICECHANGE**](wm-devicechange.md) avec *wParam* défini sur DBT \_ CUSTOMEVENT et *lParam* défini comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="eddf6-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_CUSTOMEVENT and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="eddf6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eddf6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eddf6-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="eddf6-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="eddf6-108">Handle d'une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="eddf6-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="eddf6-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="eddf6-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="eddf6-110">Identificateur du message [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="eddf6-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="eddf6-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eddf6-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eddf6-112">Définissez sur DBT \_ CUSTOMEVENT.</span><span class="sxs-lookup"><span data-stu-id="eddf6-112">Set to DBT\_CUSTOMEVENT.</span></span>

</dd> <dt>

<span data-ttu-id="eddf6-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eddf6-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eddf6-114">Pointeur vers une structure identifiant l’appareil.</span><span class="sxs-lookup"><span data-stu-id="eddf6-114">A pointer to a structure identifying the device.</span></span> <span data-ttu-id="eddf6-115">La structure se compose d’un en-tête indépendant des événements, suivi de membres dépendants de l’événement qui décrivent l’appareil.</span><span class="sxs-lookup"><span data-stu-id="eddf6-115">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="eddf6-116">Pour utiliser cette structure, traitez la structure comme une structure [**\_ \_ HDR de diffusion dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) , puis vérifiez son membre **dbch \_ DeviceType** pour déterminer le type d’appareil.</span><span class="sxs-lookup"><span data-stu-id="eddf6-116">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eddf6-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eddf6-117">Return value</span></span>

<span data-ttu-id="eddf6-118">Retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="eddf6-118">Return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="eddf6-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eddf6-119">Requirements</span></span>



| <span data-ttu-id="eddf6-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eddf6-120">Requirement</span></span> | <span data-ttu-id="eddf6-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="eddf6-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="eddf6-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eddf6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="eddf6-123">Windows XP</span><span class="sxs-lookup"><span data-stu-id="eddf6-123">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="eddf6-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eddf6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="eddf6-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="eddf6-125">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="eddf6-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="eddf6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="eddf6-127"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="eddf6-127"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eddf6-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eddf6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eddf6-129">Événements de l’appareil</span><span class="sxs-lookup"><span data-stu-id="eddf6-129">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="eddf6-130">Événements de gestion des appareils</span><span class="sxs-lookup"><span data-stu-id="eddf6-130">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="eddf6-131">**\_HDR de diffusion dev \_**</span><span class="sxs-lookup"><span data-stu-id="eddf6-131">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="eddf6-132">**\_DEVICECHANGE WM**</span><span class="sxs-lookup"><span data-stu-id="eddf6-132">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




