---
description: Le système diffuse l' \_ événement de l’appareil DBT DEVICEARRIVAL lorsqu’un périphérique ou un élément multimédia est inséré et devient disponible.
ms.assetid: 8e44cb02-cf79-4b19-807e-20cea07362af
title: Événement DBT_DEVICEARRIVAL (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f69c2feec996b4306c271454767ca4e75d1ff855
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483280"
---
# <a name="dbt_devicearrival-event"></a><span data-ttu-id="13606-103">\_Événement DBT DEVICEARRIVAL</span><span class="sxs-lookup"><span data-stu-id="13606-103">DBT\_DEVICEARRIVAL event</span></span>

<span data-ttu-id="13606-104">Le système diffuse l' \_ événement de l’appareil DBT DEVICEARRIVAL lorsqu’un périphérique ou un élément multimédia est inséré et devient disponible.</span><span class="sxs-lookup"><span data-stu-id="13606-104">The system broadcasts the DBT\_DEVICEARRIVAL device event when a device or piece of media has been inserted and becomes available.</span></span>

<span data-ttu-id="13606-105">Pour diffuser cet événement d’appareil, le système utilise le message [**WM \_ DEVICECHANGE**](wm-devicechange.md) avec *wParam* défini sur DBT \_ DEVICEARRIVAL et *lParam* défini comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="13606-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICEARRIVAL and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="13606-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="13606-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13606-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="13606-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="13606-108">Handle d'une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="13606-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="13606-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="13606-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="13606-110">Identificateur du message [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="13606-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="13606-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="13606-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="13606-112">Définissez sur DBT \_ DEVICEARRIVAL.</span><span class="sxs-lookup"><span data-stu-id="13606-112">Set to DBT\_DEVICEARRIVAL.</span></span>

</dd> <dt>

<span data-ttu-id="13606-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="13606-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="13606-114">Pointeur vers une structure identifiant l’appareil inséré.</span><span class="sxs-lookup"><span data-stu-id="13606-114">A pointer to a structure identifying the device inserted.</span></span> <span data-ttu-id="13606-115">La structure se compose d’un en-tête indépendant des événements, suivi de membres dépendants de l’événement qui décrivent l’appareil.</span><span class="sxs-lookup"><span data-stu-id="13606-115">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="13606-116">Pour utiliser cette structure, traitez la structure comme une structure [**\_ \_ HDR de diffusion dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) , puis vérifiez son membre **dbch \_ DeviceType** pour déterminer le type d’appareil.</span><span class="sxs-lookup"><span data-stu-id="13606-116">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13606-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="13606-117">Return value</span></span>

<span data-ttu-id="13606-118">Retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="13606-118">Return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="13606-119">Notes</span><span class="sxs-lookup"><span data-stu-id="13606-119">Remarks</span></span>

<span data-ttu-id="13606-120">Si le média est inséré, le type d’appareil arrivant est un volume (le membre **dbch \_ DEVICETYPE** est DBT \_ DEVTYP \_ ) et la modification affecte le support (le membre des **\_ indicateurs DBCV** est un \_ support DBTF).</span><span class="sxs-lookup"><span data-stu-id="13606-120">If media is being inserted, the type of device arriving is a volume (the **dbch\_devicetype** member is DBT\_DEVTYP\_VOLUME) and the change effects the media (the **dbcv\_flags** member is DBTF\_MEDIA).</span></span>

## <a name="examples"></a><span data-ttu-id="13606-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="13606-121">Examples</span></span>

<span data-ttu-id="13606-122">Pour obtenir un exemple, consultez détection de l' [insertion ou de la suppression d’un média](detecting-media-insertion-or-removal.md).</span><span class="sxs-lookup"><span data-stu-id="13606-122">For an example, see [Detecting Media Insertion or Removal](detecting-media-insertion-or-removal.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="13606-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="13606-123">Requirements</span></span>



| <span data-ttu-id="13606-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="13606-124">Requirement</span></span> | <span data-ttu-id="13606-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="13606-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="13606-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13606-126">Minimum supported client</span></span><br/> | <span data-ttu-id="13606-127">Windows XP</span><span class="sxs-lookup"><span data-stu-id="13606-127">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="13606-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13606-128">Minimum supported server</span></span><br/> | <span data-ttu-id="13606-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="13606-129">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="13606-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="13606-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="13606-131"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="13606-131"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13606-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13606-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13606-133">Événements de l’appareil</span><span class="sxs-lookup"><span data-stu-id="13606-133">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="13606-134">Événements de gestion des appareils</span><span class="sxs-lookup"><span data-stu-id="13606-134">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="13606-135">**\_HDR de diffusion dev \_**</span><span class="sxs-lookup"><span data-stu-id="13606-135">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="13606-136">**\_DEVICECHANGE WM**</span><span class="sxs-lookup"><span data-stu-id="13606-136">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




