---
description: Le système diffuse l’événement de l' \_ appareil DBT DEVICEQUERYREMOVE pour demander l’autorisation de supprimer un appareil ou un élément multimédia.
ms.assetid: a0e9aa57-da0e-4e9c-99d0-5502040d2664
title: Événement DBT_DEVICEQUERYREMOVE (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8c9dbdee13318f9a664582fdba8f9e3f9bfc5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513139"
---
# <a name="dbt_devicequeryremove-event"></a><span data-ttu-id="6f9c0-103">\_Événement DBT DEVICEQUERYREMOVE</span><span class="sxs-lookup"><span data-stu-id="6f9c0-103">DBT\_DEVICEQUERYREMOVE event</span></span>

<span data-ttu-id="6f9c0-104">Le système diffuse l’événement de l' \_ appareil DBT DEVICEQUERYREMOVE pour demander l’autorisation de supprimer un appareil ou un élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="6f9c0-104">The system broadcasts the DBT\_DEVICEQUERYREMOVE device event to request permission to remove a device or piece of media.</span></span> <span data-ttu-id="6f9c0-105">Ce message est la dernière chance pour les applications et les pilotes de se préparer pour cette suppression.</span><span class="sxs-lookup"><span data-stu-id="6f9c0-105">This message is the last chance for applications and drivers to prepare for this removal.</span></span> <span data-ttu-id="6f9c0-106">Toutefois, toute application peut refuser cette demande et annuler l’opération.</span><span class="sxs-lookup"><span data-stu-id="6f9c0-106">However, any application can deny this request and cancel the operation.</span></span>

<span data-ttu-id="6f9c0-107">Pour diffuser cet événement d’appareil, le système utilise le message [**WM \_ DEVICECHANGE**](wm-devicechange.md) avec *wParam* défini sur DBT \_ DEVICEQUERYREMOVE et *lParam* défini comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="6f9c0-107">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICEQUERYREMOVE and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="6f9c0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6f9c0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f9c0-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="6f9c0-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="6f9c0-110">Handle d'une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6f9c0-110">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="6f9c0-111">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="6f9c0-111">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="6f9c0-112">Identificateur du message [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="6f9c0-112">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="6f9c0-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6f9c0-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6f9c0-114">Définissez sur DBT \_ DEVICEQUERYREMOVE.</span><span class="sxs-lookup"><span data-stu-id="6f9c0-114">Set to DBT\_DEVICEQUERYREMOVE.</span></span>

</dd> <dt>

<span data-ttu-id="6f9c0-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6f9c0-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6f9c0-116">Pointeur vers une structure identifiant l’appareil à supprimer.</span><span class="sxs-lookup"><span data-stu-id="6f9c0-116">A pointer to a structure identifying the device to remove.</span></span> <span data-ttu-id="6f9c0-117">La structure se compose d’un en-tête indépendant des événements, suivi de membres dépendants de l’événement qui décrivent l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6f9c0-117">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="6f9c0-118">Pour utiliser cette structure, traitez la structure comme une structure [**\_ \_ HDR de diffusion dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) , puis vérifiez son membre **dbch \_ DeviceType** pour déterminer le type d’appareil.</span><span class="sxs-lookup"><span data-stu-id="6f9c0-118">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f9c0-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6f9c0-119">Return value</span></span>

<span data-ttu-id="6f9c0-120">Retourne la **valeur true** pour accorder l’autorisation de supprimer un appareil.</span><span class="sxs-lookup"><span data-stu-id="6f9c0-120">Return **TRUE** to grant permission to remove a device.</span></span>

<span data-ttu-id="6f9c0-121">Retournez \_ la requête de diffusion \_ Deny pour refuser l’autorisation de supprimer un appareil.</span><span class="sxs-lookup"><span data-stu-id="6f9c0-121">Return BROADCAST\_QUERY\_DENY to deny permission to remove a device.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f9c0-122">Notes</span><span class="sxs-lookup"><span data-stu-id="6f9c0-122">Remarks</span></span>

<span data-ttu-id="6f9c0-123">Vous devez fermer tous les descripteurs de l’appareil, sinon la suppression de l’appareil échouera.</span><span class="sxs-lookup"><span data-stu-id="6f9c0-123">You must close all handles to the device or the device removal will fail.</span></span>

## <a name="examples"></a><span data-ttu-id="6f9c0-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="6f9c0-124">Examples</span></span>

<span data-ttu-id="6f9c0-125">Pour obtenir un exemple, consultez [traitement d’une demande de suppression d’un appareil](processing-a-request-to-remove-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="6f9c0-125">For an example, see [Processing a Request to Remove a Device](processing-a-request-to-remove-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f9c0-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6f9c0-126">Requirements</span></span>



| <span data-ttu-id="6f9c0-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6f9c0-127">Requirement</span></span> | <span data-ttu-id="6f9c0-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f9c0-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6f9c0-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f9c0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6f9c0-130">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6f9c0-130">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="6f9c0-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f9c0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6f9c0-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6f9c0-132">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="6f9c0-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="6f9c0-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f9c0-134"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f9c0-134"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f9c0-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f9c0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f9c0-136">Événements de l’appareil</span><span class="sxs-lookup"><span data-stu-id="6f9c0-136">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="6f9c0-137">Événements de gestion des appareils</span><span class="sxs-lookup"><span data-stu-id="6f9c0-137">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="6f9c0-138">**\_HDR de diffusion dev \_**</span><span class="sxs-lookup"><span data-stu-id="6f9c0-138">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="6f9c0-139">**\_DEVICECHANGE WM**</span><span class="sxs-lookup"><span data-stu-id="6f9c0-139">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




