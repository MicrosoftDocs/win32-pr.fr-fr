---
description: Le système diffuse l' \_ événement de l’appareil DBT DEVICEREMOVECOMPLETE lorsqu’un appareil ou un élément multimédia a été physiquement supprimé.
ms.assetid: e25d35b9-f8f1-4850-996c-e1cb393cca66
title: Événement DBT_DEVICEREMOVECOMPLETE (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16c899d8cee4a0be34829ba0a8edbaf27be71f6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519214"
---
# <a name="dbt_deviceremovecomplete-event"></a><span data-ttu-id="30f8f-103">\_Événement DBT DEVICEREMOVECOMPLETE</span><span class="sxs-lookup"><span data-stu-id="30f8f-103">DBT\_DEVICEREMOVECOMPLETE event</span></span>

<span data-ttu-id="30f8f-104">Le système diffuse l' \_ événement de l’appareil DBT DEVICEREMOVECOMPLETE lorsqu’un appareil ou un élément multimédia a été physiquement supprimé.</span><span class="sxs-lookup"><span data-stu-id="30f8f-104">The system broadcasts the DBT\_DEVICEREMOVECOMPLETE device event when a device or piece of media has been physically removed.</span></span>

<span data-ttu-id="30f8f-105">Pour diffuser cet événement d’appareil, le système utilise le message [**WM \_ DEVICECHANGE**](wm-devicechange.md) avec *wParam* défini sur DBT \_ DEVICEREMOVECOMPLETE et *lParam* défini comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="30f8f-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICEREMOVECOMPLETE and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="30f8f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30f8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30f8f-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="30f8f-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="30f8f-108">Handle d'une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="30f8f-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="30f8f-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="30f8f-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="30f8f-110">Identificateur du message [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="30f8f-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="30f8f-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="30f8f-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30f8f-112">Défini sur DBT \_ DEVICEREMOVECOMPLETE</span><span class="sxs-lookup"><span data-stu-id="30f8f-112">Set to DBT\_DEVICEREMOVECOMPLETE</span></span>

</dd> <dt>

<span data-ttu-id="30f8f-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="30f8f-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30f8f-114">Pointeur vers une structure identifiant l’appareil supprimé.</span><span class="sxs-lookup"><span data-stu-id="30f8f-114">A pointer to a structure identifying the device removed.</span></span> <span data-ttu-id="30f8f-115">La structure se compose d’un en-tête indépendant des événements, suivi de membres dépendants de l’événement qui décrivent l’appareil.</span><span class="sxs-lookup"><span data-stu-id="30f8f-115">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="30f8f-116">Pour utiliser cette structure, traitez la structure comme une structure [**\_ \_ HDR de diffusion dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) , puis vérifiez son membre **dbch \_ DeviceType** pour déterminer le type d’appareil.</span><span class="sxs-lookup"><span data-stu-id="30f8f-116">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30f8f-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="30f8f-117">Return value</span></span>

<span data-ttu-id="30f8f-118">Retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="30f8f-118">Return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="30f8f-119">Notes</span><span class="sxs-lookup"><span data-stu-id="30f8f-119">Remarks</span></span>

<span data-ttu-id="30f8f-120">Le système peut diffuser un \_ message DBT DEVICEREMOVECOMPLETE sans envoyer les messages [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) et [DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) correspondants.</span><span class="sxs-lookup"><span data-stu-id="30f8f-120">The system may broadcast a DBT\_DEVICEREMOVECOMPLETE message without sending corresponding [DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md) and [DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md) messages.</span></span> <span data-ttu-id="30f8f-121">Dans ce cas, les applications et les pilotes doivent récupérer à partir de la perte de l’appareil le mieux possible.</span><span class="sxs-lookup"><span data-stu-id="30f8f-121">In such cases, the applications and drivers must recover from the loss of the device as best they can.</span></span>

<span data-ttu-id="30f8f-122">Si le support est en cours de suppression, le type d’appareil arrivant est un volume (le membre **dbch \_ DEVICETYPE** est DBT \_ DEVTYP \_ ) et la modification affecte le support (le membre **\_ indicateurs DBCV** est un \_ support DBTF).</span><span class="sxs-lookup"><span data-stu-id="30f8f-122">If media is being removed, the type of device arriving is a volume (the **dbch\_devicetype** member is DBT\_DEVTYP\_VOLUME) and the change effects the media (the **dbcv\_flags** member is DBTF\_MEDIA).</span></span>

## <a name="examples"></a><span data-ttu-id="30f8f-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="30f8f-123">Examples</span></span>

<span data-ttu-id="30f8f-124">Pour obtenir un exemple, consultez détection de l' [insertion ou suppression d’un média](detecting-media-insertion-or-removal.md) ou [traitement d’une demande de suppression d’un appareil](processing-a-request-to-remove-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="30f8f-124">For an example, see [Detecting Media Insertion or Removal](detecting-media-insertion-or-removal.md) or [Processing a Request to Remove a Device](processing-a-request-to-remove-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="30f8f-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30f8f-125">Requirements</span></span>



| <span data-ttu-id="30f8f-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30f8f-126">Requirement</span></span> | <span data-ttu-id="30f8f-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="30f8f-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="30f8f-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30f8f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="30f8f-129">Windows XP</span><span class="sxs-lookup"><span data-stu-id="30f8f-129">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="30f8f-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30f8f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="30f8f-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="30f8f-131">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="30f8f-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="30f8f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="30f8f-133"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="30f8f-133"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30f8f-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30f8f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30f8f-135">Événements de l’appareil</span><span class="sxs-lookup"><span data-stu-id="30f8f-135">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="30f8f-136">Événements de gestion des appareils</span><span class="sxs-lookup"><span data-stu-id="30f8f-136">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="30f8f-137">**\_HDR de diffusion dev \_**</span><span class="sxs-lookup"><span data-stu-id="30f8f-137">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="30f8f-138">**\_DEVICECHANGE WM**</span><span class="sxs-lookup"><span data-stu-id="30f8f-138">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




