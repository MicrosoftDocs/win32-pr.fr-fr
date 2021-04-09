---
description: L' \_ événement d’appareil DBT USERDEFINED identifie un événement défini par l’utilisateur.
ms.assetid: b42feda9-5fe7-4e54-aad9-28c61d2f29b6
title: Événement DBT_USERDEFINED (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d57ed3ebb801da4ae1ed7a7964cb7aac4f411a35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033683"
---
# <a name="dbt_userdefined-event"></a><span data-ttu-id="31b51-103">\_Événement USERDEFINED DBT</span><span class="sxs-lookup"><span data-stu-id="31b51-103">DBT\_USERDEFINED event</span></span>

<span data-ttu-id="31b51-104">L' \_ événement d’appareil DBT USERDEFINED identifie un événement défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="31b51-104">The DBT\_USERDEFINED device event identifies a user-defined event.</span></span>

<span data-ttu-id="31b51-105">Pour diffuser cet événement d’appareil, appelez la fonction [**BroadcastSystemMessage**](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage) avec le message [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="31b51-105">To broadcast this device event, call the [**BroadcastSystemMessage**](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage) function with the [**WM\_DEVICECHANGE**](wm-devicechange.md) message.</span></span> <span data-ttu-id="31b51-106">Affectez à *wParam* la valeur DBT \_ USERDEFINED et définissez *lParam* comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="31b51-106">Set *wParam* to DBT\_USERDEFINED and set *lParam* as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc( HWND   hwnd,     // handle to window
                             UINT   uMsg,     // WM_DEVICECHANGE
                             WPARAM wParam,   // DBT_USERDEFINED
                             LPARAM lParam ); // event-specific data
```



## <a name="parameters"></a><span data-ttu-id="31b51-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="31b51-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31b51-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="31b51-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="31b51-109">Handle d'une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="31b51-109">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="31b51-110">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="31b51-110">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="31b51-111">Identificateur du message [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="31b51-111">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="31b51-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="31b51-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="31b51-113">Défini sur DBT \_ USERDEFINED.</span><span class="sxs-lookup"><span data-stu-id="31b51-113">Set to DBT\_USERDEFINED.</span></span>

</dd> <dt>

<span data-ttu-id="31b51-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="31b51-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="31b51-115">Pointeur vers une structure [**\_ \_ \_ USERDEFINED de diffusion de développement**](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined) qui décrit la diffusion définie par l’utilisateur en cours.</span><span class="sxs-lookup"><span data-stu-id="31b51-115">A pointer to a [**\_DEV\_BROADCAST\_USERDEFINED**](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined) structure which describes the user-defined broadcast in progress.</span></span> <span data-ttu-id="31b51-116">Le membre **dbud \_ szName** contient le nom du message défini par l’utilisateur, suivi de toutes les données définies par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="31b51-116">The **dbud\_szName** member contains the name of the user-defined message, followed by any user-defined data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31b51-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="31b51-117">Return value</span></span>

<span data-ttu-id="31b51-118">Retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="31b51-118">Return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="31b51-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31b51-119">Requirements</span></span>



| <span data-ttu-id="31b51-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="31b51-120">Requirement</span></span> | <span data-ttu-id="31b51-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="31b51-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="31b51-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31b51-122">Minimum supported client</span></span><br/> | <span data-ttu-id="31b51-123">Windows XP</span><span class="sxs-lookup"><span data-stu-id="31b51-123">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="31b51-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31b51-124">Minimum supported server</span></span><br/> | <span data-ttu-id="31b51-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="31b51-125">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="31b51-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="31b51-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="31b51-127"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="31b51-127"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31b51-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31b51-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31b51-129">Événements de l’appareil</span><span class="sxs-lookup"><span data-stu-id="31b51-129">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="31b51-130">Événements de gestion des appareils</span><span class="sxs-lookup"><span data-stu-id="31b51-130">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="31b51-131">**\_\_USERDEFINED de diffusion dev \_**</span><span class="sxs-lookup"><span data-stu-id="31b51-131">**\_DEV\_BROADCAST\_USERDEFINED**</span></span>](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined)
</dt> <dt>

[<span data-ttu-id="31b51-132">**\_DEVICECHANGE WM**</span><span class="sxs-lookup"><span data-stu-id="31b51-132">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> <dt>

[<span data-ttu-id="31b51-133">**BroadcastSystemMessage**</span><span class="sxs-lookup"><span data-stu-id="31b51-133">**BroadcastSystemMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage)
</dt> </dl>

 

