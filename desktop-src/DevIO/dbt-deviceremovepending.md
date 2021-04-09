---
description: Le système diffuse l' \_ événement de l’appareil DBT DEVICEREMOVEPENDING lorsqu’un périphérique ou un élément multimédia est en cours de suppression et n’est plus disponible.
ms.assetid: 28cb4481-8961-4896-9608-afccba9a2bfe
title: Événement DBT_DEVICEREMOVEPENDING (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 421851dc46d905ae85941b92df6649ccb504ee50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110695"
---
# <a name="dbt_deviceremovepending-event"></a><span data-ttu-id="d4937-103">\_Événement DBT DEVICEREMOVEPENDING</span><span class="sxs-lookup"><span data-stu-id="d4937-103">DBT\_DEVICEREMOVEPENDING event</span></span>

<span data-ttu-id="d4937-104">Le système diffuse l' \_ événement de l’appareil DBT DEVICEREMOVEPENDING lorsqu’un périphérique ou un élément multimédia est en cours de suppression et n’est plus disponible.</span><span class="sxs-lookup"><span data-stu-id="d4937-104">The system broadcasts the DBT\_DEVICEREMOVEPENDING device event when a device or piece of media is being removed and is no longer available for use.</span></span>

<span data-ttu-id="d4937-105">Pour diffuser cet événement d’appareil, le système utilise le message [**WM \_ DEVICECHANGE**](wm-devicechange.md) avec *wParam* défini sur DBT \_ DEVICEREMOVEPENDING et *lParam* défini comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="d4937-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICEREMOVEPENDING and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="d4937-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d4937-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4937-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="d4937-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="d4937-108">Handle d'une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d4937-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="d4937-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="d4937-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="d4937-110">Identificateur du message [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="d4937-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="d4937-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d4937-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d4937-112">Définissez sur DBT \_ DEVICEREMOVEPENDING.</span><span class="sxs-lookup"><span data-stu-id="d4937-112">Set to DBT\_DEVICEREMOVEPENDING.</span></span>

</dd> <dt>

<span data-ttu-id="d4937-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d4937-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d4937-114">Pointeur vers une structure identifiant l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d4937-114">A pointer to a structure identifying the device.</span></span> <span data-ttu-id="d4937-115">La structure se compose d’un en-tête indépendant des événements, suivi de membres dépendants de l’événement qui décrivent l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d4937-115">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="d4937-116">Pour utiliser cette structure, traitez la structure comme une structure [**\_ \_ HDR de diffusion dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) , puis vérifiez son membre **dbch \_ DeviceType** pour déterminer le type d’appareil.</span><span class="sxs-lookup"><span data-stu-id="d4937-116">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4937-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d4937-117">Return value</span></span>

<span data-ttu-id="d4937-118">Retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="d4937-118">Return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4937-119">Notes</span><span class="sxs-lookup"><span data-stu-id="d4937-119">Remarks</span></span>

<span data-ttu-id="d4937-120">Le système peut diffuser un \_ message DBT DEVICEREMOVEPENDING sans envoyer de message [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) correspondant.</span><span class="sxs-lookup"><span data-stu-id="d4937-120">The system may broadcast a DBT\_DEVICEREMOVEPENDING message without sending a corresponding [DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md) message.</span></span> <span data-ttu-id="d4937-121">Dans ce cas, les applications et les pilotes doivent récupérer à partir de la perte de l’appareil le mieux possible.</span><span class="sxs-lookup"><span data-stu-id="d4937-121">In such cases, the applications and drivers must recover from the loss of the device as best they can.</span></span>

## <a name="examples"></a><span data-ttu-id="d4937-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="d4937-122">Examples</span></span>

<span data-ttu-id="d4937-123">Pour obtenir un exemple, consultez [traitement d’une demande de suppression d’un appareil](processing-a-request-to-remove-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="d4937-123">For an example, see [Processing a Request to Remove a Device](processing-a-request-to-remove-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d4937-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4937-124">Requirements</span></span>



| <span data-ttu-id="d4937-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4937-125">Requirement</span></span> | <span data-ttu-id="d4937-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4937-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d4937-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4937-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d4937-128">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d4937-128">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="d4937-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4937-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d4937-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d4937-130">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="d4937-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="d4937-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4937-132"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4937-132"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4937-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4937-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4937-134">Événements de l’appareil</span><span class="sxs-lookup"><span data-stu-id="d4937-134">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="d4937-135">Événements de gestion des appareils</span><span class="sxs-lookup"><span data-stu-id="d4937-135">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="d4937-136">**\_HDR de diffusion dev \_**</span><span class="sxs-lookup"><span data-stu-id="d4937-136">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="d4937-137">**\_DEVICECHANGE WM**</span><span class="sxs-lookup"><span data-stu-id="d4937-137">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




