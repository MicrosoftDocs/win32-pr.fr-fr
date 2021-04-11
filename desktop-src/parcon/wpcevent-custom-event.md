---
description: Événement par utilisateur qui prend en charge jusqu’à trois champs.
ms.assetid: e6cf8008-b896-453b-9946-a6b3d94a991a
title: Événement WPCEVENT_CUSTOM (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d20cb2450cd18bb0c77993622d226cfc06dff6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202707"
---
# <a name="wpcevent_custom-event"></a><span data-ttu-id="db6dc-103">\_Événement personnalisé WPCEVENT</span><span class="sxs-lookup"><span data-stu-id="db6dc-103">WPCEVENT\_CUSTOM event</span></span>

<span data-ttu-id="db6dc-104">Événement par utilisateur qui prend en charge jusqu’à trois champs.</span><span class="sxs-lookup"><span data-stu-id="db6dc-104">Per-user event that supports up to three fields.</span></span>

<span data-ttu-id="db6dc-105">Les événements sont affichés dans l' **Observateur d’activité** dans l' **autre** section avec la hiérarchie suivante :</span><span class="sxs-lookup"><span data-stu-id="db6dc-105">Events are displayed in the **Activity Viewer** in the **Other** section with the following hierarchy:</span></span>

1.  <span data-ttu-id="db6dc-106">Publisher</span><span class="sxs-lookup"><span data-stu-id="db6dc-106">Publisher</span></span>

2.  <span data-ttu-id="db6dc-107">Application</span><span class="sxs-lookup"><span data-stu-id="db6dc-107">Application</span></span>

3.  <span data-ttu-id="db6dc-108">Événement</span><span class="sxs-lookup"><span data-stu-id="db6dc-108">Event</span></span>


```C++
const EVENT_DESCRIPTOR WPCEVENT_CUSTOM = {0xd, 0x0, 0x10, 0x4, 0x17, 0xd, 0x8000000000000030};
```



## <a name="parameters"></a><span data-ttu-id="db6dc-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="db6dc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db6dc-110">*Publisher*</span><span class="sxs-lookup"><span data-stu-id="db6dc-110">*Publisher*</span></span> 
</dt> <dd>

<span data-ttu-id="db6dc-111">Éditeur de l’événement (par exemple, un nom de société).</span><span class="sxs-lookup"><span data-stu-id="db6dc-111">The publisher of the event (for example, a company name).</span></span>

</dd> <dt>

<span data-ttu-id="db6dc-112">*AppName*</span><span class="sxs-lookup"><span data-stu-id="db6dc-112">*AppName*</span></span> 
</dt> <dd>

<span data-ttu-id="db6dc-113">Nom de l’application qui génère l’événement.</span><span class="sxs-lookup"><span data-stu-id="db6dc-113">The name of the application that is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="db6dc-114">*AppVersion*</span><span class="sxs-lookup"><span data-stu-id="db6dc-114">*AppVersion*</span></span> 
</dt> <dd>

<span data-ttu-id="db6dc-115">Version de l’application qui génère l’événement.</span><span class="sxs-lookup"><span data-stu-id="db6dc-115">The version of the application that is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="db6dc-116">*Event*</span><span class="sxs-lookup"><span data-stu-id="db6dc-116">*Event*</span></span> 
</dt> <dd>

<span data-ttu-id="db6dc-117">Nom de l’événement.</span><span class="sxs-lookup"><span data-stu-id="db6dc-117">The name for the event.</span></span>

</dd> <dt>

<span data-ttu-id="db6dc-118">*Value*</span><span class="sxs-lookup"><span data-stu-id="db6dc-118">*Value1*</span></span> 
</dt> <dd>

<span data-ttu-id="db6dc-119">Champ personnalisé 1.</span><span class="sxs-lookup"><span data-stu-id="db6dc-119">Custom field 1.</span></span>

</dd> <dt>

<span data-ttu-id="db6dc-120">*Value2*</span><span class="sxs-lookup"><span data-stu-id="db6dc-120">*Value2*</span></span> 
</dt> <dd>

<span data-ttu-id="db6dc-121">Champ personnalisé 2.</span><span class="sxs-lookup"><span data-stu-id="db6dc-121">Custom field 2.</span></span>

</dd> <dt>

<span data-ttu-id="db6dc-122">*Valeur3*</span><span class="sxs-lookup"><span data-stu-id="db6dc-122">*Value3*</span></span> 
</dt> <dd>

<span data-ttu-id="db6dc-123">Champ personnalisé 3.</span><span class="sxs-lookup"><span data-stu-id="db6dc-123">Custom field 3.</span></span>

</dd> <dt>

<span data-ttu-id="db6dc-124">*Bloqué*</span><span class="sxs-lookup"><span data-stu-id="db6dc-124">*Blocked*</span></span> 
</dt> <dd>

<span data-ttu-id="db6dc-125">Valeur de l’énumération [**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) qui indique des informations sur les événements dont l’utilisation est bloquée et sur les contrôles en place.</span><span class="sxs-lookup"><span data-stu-id="db6dc-125">A value of the [**WPCFLAG\_ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) enumeration that indicates information about what events are blocked from use and what controls are in place.</span></span>

</dd> <dt>

<span data-ttu-id="db6dc-126">*Motif*</span><span class="sxs-lookup"><span data-stu-id="db6dc-126">*Reason*</span></span> 
</dt> <dd>

<span data-ttu-id="db6dc-127">Chaîne personnalisée qui fournit des informations supplémentaires sur la raison du blocage ou non du blocage.</span><span class="sxs-lookup"><span data-stu-id="db6dc-127">A custom string that provides extra information about the reason for blocking or not blocking.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="db6dc-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="db6dc-128">Requirements</span></span>



| <span data-ttu-id="db6dc-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="db6dc-129">Requirement</span></span> | <span data-ttu-id="db6dc-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="db6dc-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="db6dc-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db6dc-131">Minimum supported client</span></span><br/> | <span data-ttu-id="db6dc-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db6dc-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="db6dc-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db6dc-133">Minimum supported server</span></span><br/> | <span data-ttu-id="db6dc-134">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="db6dc-134">None supported</span></span><br/>                                                             |
| <span data-ttu-id="db6dc-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="db6dc-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="db6dc-136"><dt>Wpcevent. h</dt></span><span class="sxs-lookup"><span data-stu-id="db6dc-136"><dt>Wpcevent.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db6dc-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db6dc-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db6dc-138">Utilisation des API de journalisation pour les contrôles parentaux</span><span class="sxs-lookup"><span data-stu-id="db6dc-138">Using Logging APIs for Parental Controls</span></span>](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[<span data-ttu-id="db6dc-139">**WPC \_ args \_ CONVERSATIONINITEVENT**</span><span class="sxs-lookup"><span data-stu-id="db6dc-139">**WPC\_ARGS\_CONVERSATIONINITEVENT**</span></span>](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




