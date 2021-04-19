---
description: Événement au niveau système généré sur un paramètre de contrôle parental modifié.
ms.assetid: 2540c3cc-96d0-4e01-a525-4da4a857cb58
title: Événement WPCEVENT_SYS_SETTINGCHANGE (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ea0efb4d68fabcb5f9216c4ccf3bb923ee0ff54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545856"
---
# <a name="wpcevent_sys_settingchange-event"></a><span data-ttu-id="189eb-103">\_Événement Sys \_ SETTINGCHANGE WPCEVENT</span><span class="sxs-lookup"><span data-stu-id="189eb-103">WPCEVENT\_SYS\_SETTINGCHANGE event</span></span>

<span data-ttu-id="189eb-104">Événement au niveau système généré sur un paramètre de contrôle parental modifié.</span><span class="sxs-lookup"><span data-stu-id="189eb-104">System-level event generated on a Parental Controls setting change.</span></span>


```C++
const EVENT_DESCRIPTOR WPCEVENT_SYS_SETTINGCHANGE = {0x1, 0x0, 0x10, 0x4, 0x15, 0x1, 0x8000000000000010};
```



## <a name="parameters"></a><span data-ttu-id="189eb-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="189eb-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="189eb-106">*Classe*</span><span class="sxs-lookup"><span data-stu-id="189eb-106">*Class*</span></span> 
</dt> <dd>

<span data-ttu-id="189eb-107">Classe qui génère l’événement.</span><span class="sxs-lookup"><span data-stu-id="189eb-107">The class that is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="189eb-108">*Paramètre*</span><span class="sxs-lookup"><span data-stu-id="189eb-108">*Setting*</span></span> 
</dt> <dd>

<span data-ttu-id="189eb-109">Valeur de l’énumération des **\_ paramètres WPC** .</span><span class="sxs-lookup"><span data-stu-id="189eb-109">A value of the **WPC\_SETTINGS** enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="189eb-110">*Propriétaire*</span><span class="sxs-lookup"><span data-stu-id="189eb-110">*Owner*</span></span> 
</dt> <dd>

<span data-ttu-id="189eb-111">Identificateur de sécurité de l’utilisateur qui génère l’événement.</span><span class="sxs-lookup"><span data-stu-id="189eb-111">The security identifier of the user who is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="189eb-112">*OldVal*</span><span class="sxs-lookup"><span data-stu-id="189eb-112">*OldVal*</span></span> 
</dt> <dd>

<span data-ttu-id="189eb-113">Valeur précédente de ce paramètre, en cas de suppression ou de modification.</span><span class="sxs-lookup"><span data-stu-id="189eb-113">The previous value of this setting, if deleted or changed.</span></span>

</dd> <dt>

<span data-ttu-id="189eb-114">*NewVal*</span><span class="sxs-lookup"><span data-stu-id="189eb-114">*NewVal*</span></span> 
</dt> <dd>

<span data-ttu-id="189eb-115">Nouvelle valeur de ce paramètre, si elle est ajoutée ou modifiée.</span><span class="sxs-lookup"><span data-stu-id="189eb-115">The new value of this setting, if added or changed.</span></span>

</dd> <dt>

<span data-ttu-id="189eb-116">*Motif*</span><span class="sxs-lookup"><span data-stu-id="189eb-116">*Reason*</span></span> 
</dt> <dd>

<span data-ttu-id="189eb-117">Valeur de l’énumération [**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) qui indique des informations sur les événements dont l’utilisation est bloquée et sur les contrôles en place.</span><span class="sxs-lookup"><span data-stu-id="189eb-117">A value of the [**WPCFLAG\_ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) enumeration that indicates information about what events are blocked from use and what controls are in place.</span></span>

</dd> <dt>

<span data-ttu-id="189eb-118">*Facultatif*</span><span class="sxs-lookup"><span data-stu-id="189eb-118">*Optional*</span></span> 
</dt> <dd>

<span data-ttu-id="189eb-119">Champ facultatif.</span><span class="sxs-lookup"><span data-stu-id="189eb-119">An optional field.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="189eb-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="189eb-120">Requirements</span></span>



| <span data-ttu-id="189eb-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="189eb-121">Requirement</span></span> | <span data-ttu-id="189eb-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="189eb-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="189eb-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="189eb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="189eb-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="189eb-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="189eb-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="189eb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="189eb-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="189eb-126">None supported</span></span><br/>                                                             |
| <span data-ttu-id="189eb-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="189eb-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="189eb-128"><dt>Wpcevent. h</dt></span><span class="sxs-lookup"><span data-stu-id="189eb-128"><dt>Wpcevent.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="189eb-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="189eb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="189eb-130">Utilisation des API de journalisation pour les contrôles parentaux</span><span class="sxs-lookup"><span data-stu-id="189eb-130">Using Logging APIs for Parental Controls</span></span>](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[<span data-ttu-id="189eb-131">**WPC \_ args \_ CONVERSATIONINITEVENT**</span><span class="sxs-lookup"><span data-stu-id="189eb-131">**WPC\_ARGS\_CONVERSATIONINITEVENT**</span></span>](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




