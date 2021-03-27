---
description: Cette classe est la classe parente des événements d’appel de procédure locale avancés. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 5380fada-50e7-4eb2-8549-6d738a56d2cd
title: Classe ALPC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2a4b09a8bab9280de8fb4c91368f5d6d93f7944a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972235"
---
# <a name="alpc-class"></a><span data-ttu-id="3f8fb-104">Classe ALPC</span><span class="sxs-lookup"><span data-stu-id="3f8fb-104">ALPC class</span></span>

<span data-ttu-id="3f8fb-105">Cette classe est la classe parente des événements d’appel de procédure locale avancés.</span><span class="sxs-lookup"><span data-stu-id="3f8fb-105">This class is the parent class for advanced local procedure call events.</span></span>

<span data-ttu-id="3f8fb-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="3f8fb-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f8fb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f8fb-107">Syntax</span></span>

``` syntax
[Guid("{45d8cccd-539f-4b72-a8b7-5c683142609a}")]
class ALPC : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="3f8fb-108">Membres</span><span class="sxs-lookup"><span data-stu-id="3f8fb-108">Members</span></span>

<span data-ttu-id="3f8fb-109">La classe **ALPC** ne définit aucun membre.</span><span class="sxs-lookup"><span data-stu-id="3f8fb-109">The **ALPC** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f8fb-110">Notes</span><span class="sxs-lookup"><span data-stu-id="3f8fb-110">Remarks</span></span>

<span data-ttu-id="3f8fb-111">Pour activer les événements d’appel de procédure locale avancée dans une session de journalisation du noyau NT, spécifiez l’indicateur de **suivi d’événement \_ \_ \_ ALPC** dans le membre **EnableFlags** d’une structure de [**Propriétés de \_ trace \_ d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) lors de l’appel de la fonction [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="3f8fb-111">To enable advanced local procedure call events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_ALPC** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="3f8fb-112">Les consommateurs de suivi d’événements peuvent implémenter un traitement spécial pour les événements ALPC en appelant la fonction [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) et en spécifiant [**ALPCGuid**](nt-kernel-logger-constants.md) comme paramètre *pguid* .</span><span class="sxs-lookup"><span data-stu-id="3f8fb-112">Event trace consumers can implement special processing for ALPC events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ALPCGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="3f8fb-113">Utilisez les types d’événements suivants pour identifier l’événement ALPC réel lors de la consommation d’événements.</span><span class="sxs-lookup"><span data-stu-id="3f8fb-113">Use the following event types to identify the actual ALPC event when consuming events.</span></span>



| <span data-ttu-id="3f8fb-114">Type d'événement</span><span class="sxs-lookup"><span data-stu-id="3f8fb-114">Event type</span></span>           | <span data-ttu-id="3f8fb-115">Description</span><span class="sxs-lookup"><span data-stu-id="3f8fb-115">Description</span></span>                                                                                                                                         |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f8fb-116">Valeur de type d’événement, 33</span><span class="sxs-lookup"><span data-stu-id="3f8fb-116">Event type value, 33</span></span> | <span data-ttu-id="3f8fb-117">Événement d’envoi de message.</span><span class="sxs-lookup"><span data-stu-id="3f8fb-117">Send message event.</span></span> <span data-ttu-id="3f8fb-118">La classe MOF de [**\_ \_ message d’envoi ALPC**](alpc-send-message.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="3f8fb-118">The [**ALPC\_Send\_Message**](alpc-send-message.md) MOF class defines the event data for this event.</span></span>                           |
| <span data-ttu-id="3f8fb-119">Valeur de type d’événement, 34</span><span class="sxs-lookup"><span data-stu-id="3f8fb-119">Event type value, 34</span></span> | <span data-ttu-id="3f8fb-120">Recevoir un événement de message.</span><span class="sxs-lookup"><span data-stu-id="3f8fb-120">Receive message event.</span></span> <span data-ttu-id="3f8fb-121">La classe MOF de [**\_ \_ message de réception ALPC**](alpc-receive-message.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="3f8fb-121">The [**ALPC\_Receive\_Message**](alpc-receive-message.md) MOF class defines the event data for this event.</span></span>                  |
| <span data-ttu-id="3f8fb-122">Valeur de type d’événement, 35</span><span class="sxs-lookup"><span data-stu-id="3f8fb-122">Event type value, 35</span></span> | <span data-ttu-id="3f8fb-123">Attente d’un événement de réponse.</span><span class="sxs-lookup"><span data-stu-id="3f8fb-123">Wait for reply event.</span></span> <span data-ttu-id="3f8fb-124">La classe MOF [**\_ \_ d’attente de \_ réponse ALPC**](alpc-wait-for-reply.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="3f8fb-124">The [**ALPC\_Wait\_For\_Reply**](alpc-wait-for-reply.md) MOF class defines the event data for this event.</span></span>                    |
| <span data-ttu-id="3f8fb-125">Valeur de type d’événement, 36</span><span class="sxs-lookup"><span data-stu-id="3f8fb-125">Event type value, 36</span></span> | <span data-ttu-id="3f8fb-126">Attendez l’événement du nouveau message.</span><span class="sxs-lookup"><span data-stu-id="3f8fb-126">Wait for new message event.</span></span> <span data-ttu-id="3f8fb-127">La classe MOF [**\_ wait \_ for \_ New \_ message**](alpc-wait-for-new-message.md) MOF définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="3f8fb-127">The [**ALPC\_Wait\_For\_New\_Message**](alpc-wait-for-new-message.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="3f8fb-128">Valeur de type d’événement, 37</span><span class="sxs-lookup"><span data-stu-id="3f8fb-128">Event type value, 37</span></span> | <span data-ttu-id="3f8fb-129">Arrêter l’événement en attente.</span><span class="sxs-lookup"><span data-stu-id="3f8fb-129">Stop waiting event.</span></span> <span data-ttu-id="3f8fb-130">La classe MOF d' [**\_ inattente ALPC**](alpc-unwait.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="3f8fb-130">The [**ALPC\_Unwait**](alpc-unwait.md) MOF class defines the event data for this event.</span></span>                                        |



 

## <a name="requirements"></a><span data-ttu-id="3f8fb-131">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3f8fb-131">Requirements</span></span>



| <span data-ttu-id="3f8fb-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3f8fb-132">Requirement</span></span> | <span data-ttu-id="3f8fb-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f8fb-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3f8fb-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f8fb-134">Minimum supported client</span></span><br/> | <span data-ttu-id="3f8fb-135">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3f8fb-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3f8fb-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f8fb-136">Minimum supported server</span></span><br/> | <span data-ttu-id="3f8fb-137">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3f8fb-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

