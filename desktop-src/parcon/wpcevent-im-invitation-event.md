---
description: Événement par utilisateur fourni pour l’initiation de la journalisation des conversations par les clients de messagerie instantanée.
ms.assetid: b2cd1d37-9993-4990-83b7-b147a109e4af
title: Événement WPCEVENT_IM_INVITATION (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87c9d7e90eaa901b5e18a072e03e3112ee8c2934
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522724"
---
# <a name="wpcevent_im_invitation-event"></a><span data-ttu-id="a05e1-103">\_Événement d' \_ invitation im WPCEVENT</span><span class="sxs-lookup"><span data-stu-id="a05e1-103">WPCEVENT\_IM\_INVITATION event</span></span>

<span data-ttu-id="a05e1-104">Événement par utilisateur fourni pour l’initiation de la journalisation des conversations par les clients de messagerie instantanée.</span><span class="sxs-lookup"><span data-stu-id="a05e1-104">Per-user event provided for logging initiation of conversations by Instant Messaging clients.</span></span>


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_INVITATION = {0x7, 0x0, 0x10, 0x4, 0x16, 0x7, 0x8000000000000030};
```



## <a name="parameters"></a><span data-ttu-id="a05e1-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a05e1-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a05e1-106">*AppName*</span><span class="sxs-lookup"><span data-stu-id="a05e1-106">*AppName*</span></span> 
</dt> <dd>

<span data-ttu-id="a05e1-107">Nom de l’application qui génère l’événement.</span><span class="sxs-lookup"><span data-stu-id="a05e1-107">The name of the application that is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="a05e1-108">*AppVersion*</span><span class="sxs-lookup"><span data-stu-id="a05e1-108">*AppVersion*</span></span> 
</dt> <dd>

<span data-ttu-id="a05e1-109">Chaîne de version de l’application qui génère l’événement.</span><span class="sxs-lookup"><span data-stu-id="a05e1-109">The version string for the application that is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="a05e1-110">*AccountName*</span><span class="sxs-lookup"><span data-stu-id="a05e1-110">*AccountName*</span></span> 
</dt> <dd>

<span data-ttu-id="a05e1-111">Chaîne d’identité du compte de messagerie instantanée.</span><span class="sxs-lookup"><span data-stu-id="a05e1-111">The instant messaging account identity string.</span></span>

</dd> <dt>

<span data-ttu-id="a05e1-112">*ConvID*</span><span class="sxs-lookup"><span data-stu-id="a05e1-112">*ConvID*</span></span> 
</dt> <dd>

<span data-ttu-id="a05e1-113">Identificateur de la conversation.</span><span class="sxs-lookup"><span data-stu-id="a05e1-113">The identifier for the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="a05e1-114">*RequestingIP*</span><span class="sxs-lookup"><span data-stu-id="a05e1-114">*RequestingIP*</span></span> 
</dt> <dd>

<span data-ttu-id="a05e1-115">Chaîne qui contient l’adresse IP de l’ordinateur qui envoie l’invitation.</span><span class="sxs-lookup"><span data-stu-id="a05e1-115">A string that contains the IP address of the computer that is sending the invitation.</span></span>

</dd> <dt>

<span data-ttu-id="a05e1-116">*Expéditeur*</span><span class="sxs-lookup"><span data-stu-id="a05e1-116">*Sender*</span></span> 
</dt> <dd>

<span data-ttu-id="a05e1-117">Chaîne d’identité du compte de messagerie instantanée pour le compte qui émet l’invitation.</span><span class="sxs-lookup"><span data-stu-id="a05e1-117">The instant messaging account identity string for the account that is issuing the invitation.</span></span>

</dd> <dt>

<span data-ttu-id="a05e1-118">*Motif*</span><span class="sxs-lookup"><span data-stu-id="a05e1-118">*Reason*</span></span> 
</dt> <dd>

<span data-ttu-id="a05e1-119">Valeur de l’énumération [**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) qui indique des informations sur les événements dont l’utilisation est bloquée et sur les contrôles en place.</span><span class="sxs-lookup"><span data-stu-id="a05e1-119">A value of the [**WPCFLAG\_ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) enumeration that indicates information about what events are blocked from use and what controls are in place.</span></span>

</dd> <dt>

<span data-ttu-id="a05e1-120">*RecipCount*</span><span class="sxs-lookup"><span data-stu-id="a05e1-120">*RecipCount*</span></span> 
</dt> <dd>

<span data-ttu-id="a05e1-121">Nombre de destinataires qui reçoivent l’invitation et dont les identités sont définies dans le champ destinataire.</span><span class="sxs-lookup"><span data-stu-id="a05e1-121">The count of recipients who are receiving the invitation and who have identities defined in the recipient field.</span></span>

</dd> <dt>

<span data-ttu-id="a05e1-122">*Recipient*</span><span class="sxs-lookup"><span data-stu-id="a05e1-122">*Recipient*</span></span> 
</dt> <dd>

<span data-ttu-id="a05e1-123">Chaîne délimitée qui contient les chaînes d’identité du compte de messagerie instantanée pour les destinataires de l’invitation.</span><span class="sxs-lookup"><span data-stu-id="a05e1-123">A delimited string that contains instant messaging account identity strings for the recipients of the invitation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a05e1-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a05e1-124">Requirements</span></span>



| <span data-ttu-id="a05e1-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a05e1-125">Requirement</span></span> | <span data-ttu-id="a05e1-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="a05e1-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a05e1-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a05e1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a05e1-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a05e1-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a05e1-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a05e1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a05e1-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a05e1-130">None supported</span></span><br/>                                                             |
| <span data-ttu-id="a05e1-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="a05e1-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a05e1-132"><dt>Wpcevent. h</dt></span><span class="sxs-lookup"><span data-stu-id="a05e1-132"><dt>Wpcevent.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a05e1-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a05e1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a05e1-134">Utilisation des API de journalisation pour les contrôles parentaux</span><span class="sxs-lookup"><span data-stu-id="a05e1-134">Using Logging APIs for Parental Controls</span></span>](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[<span data-ttu-id="a05e1-135">**WPC \_ args \_ CONVERSATIONINITEVENT**</span><span class="sxs-lookup"><span data-stu-id="a05e1-135">**WPC\_ARGS\_CONVERSATIONINITEVENT**</span></span>](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




