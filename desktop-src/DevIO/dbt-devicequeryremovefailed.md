---
description: Le système diffuse l' \_ événement de l’appareil DBT DEVICEQUERYREMOVEFAILED lorsqu’une demande de suppression d’un périphérique ou d’un élément multimédia a été annulée.
ms.assetid: a24916a9-b67a-4622-b9f3-4b4f26bf4d6b
title: Événement DBT_DEVICEQUERYREMOVEFAILED (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 848c7378cdbac95729eee70c70a1e323373b8e85
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861110"
---
# <a name="dbt_devicequeryremovefailed-event"></a><span data-ttu-id="e42e1-103">\_Événement DBT DEVICEQUERYREMOVEFAILED</span><span class="sxs-lookup"><span data-stu-id="e42e1-103">DBT\_DEVICEQUERYREMOVEFAILED event</span></span>

<span data-ttu-id="e42e1-104">Le système diffuse l' \_ événement de l’appareil DBT DEVICEQUERYREMOVEFAILED lorsqu’une demande de suppression d’un périphérique ou d’un élément multimédia a été annulée.</span><span class="sxs-lookup"><span data-stu-id="e42e1-104">The system broadcasts the DBT\_DEVICEQUERYREMOVEFAILED device event when a request to remove a device or piece of media has been canceled.</span></span>

<span data-ttu-id="e42e1-105">Pour diffuser cet événement d’appareil, le système utilise le message [**WM \_ DEVICECHANGE**](wm-devicechange.md) avec *wParam* défini sur DBT \_ DEVICEQUERYREMOVEFAILED et *lParam* défini comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="e42e1-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICEQUERYREMOVEFAILED and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="e42e1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e42e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e42e1-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="e42e1-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="e42e1-108">Handle d'une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e42e1-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="e42e1-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="e42e1-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="e42e1-110">Identificateur du message [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="e42e1-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="e42e1-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e42e1-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e42e1-112">Définissez sur DBT \_ DEVICEQUERYREMOVEFAILED.</span><span class="sxs-lookup"><span data-stu-id="e42e1-112">Set to DBT\_DEVICEQUERYREMOVEFAILED.</span></span>

</dd> <dt>

<span data-ttu-id="e42e1-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e42e1-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e42e1-114">Pointeur vers une structure identifiant l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e42e1-114">A pointer to a structure identifying the device.</span></span> <span data-ttu-id="e42e1-115">La structure se compose d’un en-tête indépendant des événements, suivi de membres dépendants de l’événement qui décrivent l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e42e1-115">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="e42e1-116">Pour utiliser cette structure, traitez la structure comme une structure [**\_ \_ HDR de diffusion dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) , puis vérifiez son membre **dbch \_ DeviceType** pour déterminer le type d’appareil.</span><span class="sxs-lookup"><span data-stu-id="e42e1-116">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e42e1-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e42e1-117">Return value</span></span>

<span data-ttu-id="e42e1-118">Retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="e42e1-118">Return **TRUE**.</span></span>

## <a name="examples"></a><span data-ttu-id="e42e1-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="e42e1-119">Examples</span></span>

<span data-ttu-id="e42e1-120">Pour obtenir un exemple, consultez [traitement d’une demande de suppression d’un appareil](processing-a-request-to-remove-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="e42e1-120">For an example, see [Processing a Request to Remove a Device](processing-a-request-to-remove-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e42e1-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e42e1-121">Requirements</span></span>



| <span data-ttu-id="e42e1-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e42e1-122">Requirement</span></span> | <span data-ttu-id="e42e1-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="e42e1-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e42e1-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e42e1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e42e1-125">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e42e1-125">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="e42e1-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e42e1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e42e1-127">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e42e1-127">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="e42e1-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="e42e1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e42e1-129"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="e42e1-129"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e42e1-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e42e1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e42e1-131">Événements de l’appareil</span><span class="sxs-lookup"><span data-stu-id="e42e1-131">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="e42e1-132">Événements de gestion des appareils</span><span class="sxs-lookup"><span data-stu-id="e42e1-132">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="e42e1-133">**\_HDR de diffusion dev \_**</span><span class="sxs-lookup"><span data-stu-id="e42e1-133">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="e42e1-134">**\_DEVICECHANGE WM**</span><span class="sxs-lookup"><span data-stu-id="e42e1-134">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




