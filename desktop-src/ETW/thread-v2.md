---
description: Classe Thread_V2-cette classe est la classe parente pour les événements de thread. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 63e52cba-42a5-44f0-8eb6-e1bac8414a83
title: Classe Thread_V2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V2
api_type:
- NA
api_location: ''
ms.openlocfilehash: b00067af61a55e61f70b0c799a1512edf284f11c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105617"
---
# <a name="thread_v2-class"></a><span data-ttu-id="3cc08-104">Classe de thread \_ v2</span><span class="sxs-lookup"><span data-stu-id="3cc08-104">Thread\_V2 class</span></span>

<span data-ttu-id="3cc08-105">Cette classe est la classe parente pour les événements de thread.</span><span class="sxs-lookup"><span data-stu-id="3cc08-105">This class is the parent class for thread events.</span></span>

<span data-ttu-id="3cc08-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="3cc08-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cc08-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3cc08-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class Thread_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="3cc08-108">Membres</span><span class="sxs-lookup"><span data-stu-id="3cc08-108">Members</span></span>

<span data-ttu-id="3cc08-109">La classe **thread \_ v2** ne définit aucun membre.</span><span class="sxs-lookup"><span data-stu-id="3cc08-109">The **Thread\_V2** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cc08-110">Notes </span><span class="sxs-lookup"><span data-stu-id="3cc08-110">Remarks</span></span>

<span data-ttu-id="3cc08-111">Pour activer les événements de thread dans une session de journalisation du noyau NT, spécifiez l’indicateur de thread de l' **indicateur de \_ trace \_ \_ d’événements** dans le membre **EnableFlags** d’une structure de [**Propriétés de \_ trace \_ d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) lors de l’appel de la fonction [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="3cc08-111">To enable thread events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_THREAD** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="3cc08-112">Vous pouvez également spécifier les indicateurs suivants :</span><span class="sxs-lookup"><span data-stu-id="3cc08-112">You can also specify the following flags:</span></span>

-   <span data-ttu-id="3cc08-113">**indicateur de suivi d’événement \_ \_ \_ CSWITCH**</span><span class="sxs-lookup"><span data-stu-id="3cc08-113">**EVENT\_TRACE\_FLAG\_CSWITCH**</span></span>
-   <span data-ttu-id="3cc08-114">**\_répartiteur d' \_ indicateurs de trace d’événements \_**</span><span class="sxs-lookup"><span data-stu-id="3cc08-114">**EVENT\_TRACE\_FLAG\_DISPATCHER**</span></span>

<span data-ttu-id="3cc08-115">Les consommateurs de suivi d’événements peuvent implémenter un traitement spécial pour les événements de thread en appelant la fonction [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) et en spécifiant [**ThreadGuid**](nt-kernel-logger-constants.md) comme paramètre *pguid* .</span><span class="sxs-lookup"><span data-stu-id="3cc08-115">Event trace consumers can implement special processing for thread events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ThreadGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="3cc08-116">Utilisez les types d’événements suivants pour identifier l’événement de thread réel lors de la consommation d’événements.</span><span class="sxs-lookup"><span data-stu-id="3cc08-116">Use the following event types to identify the actual thread event when consuming events.</span></span>



| <span data-ttu-id="3cc08-117">Type d'événement</span><span class="sxs-lookup"><span data-stu-id="3cc08-117">Event type</span></span>                                                      | <span data-ttu-id="3cc08-118">Description</span><span class="sxs-lookup"><span data-stu-id="3cc08-118">Description</span></span>                                                                                                                                                                                                                          |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cc08-119">**Événement \_ \_ \_ Fin du type de suivi**(la valeur du type d’événement est 2)</span><span class="sxs-lookup"><span data-stu-id="3cc08-119">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>   | <span data-ttu-id="3cc08-120">Événement de fin de thread.</span><span class="sxs-lookup"><span data-stu-id="3cc08-120">End thread event.</span></span> <span data-ttu-id="3cc08-121">La classe MOF [**\_ \_ TypeGroup1 du thread v2**](thread-v2-typegroup1.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="3cc08-121">The [**Thread\_V2\_TypeGroup1**](thread-v2-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                        |
| <span data-ttu-id="3cc08-122">**Événement \_ \_ \_ Début du type de suivi**(la valeur du type d’événement est 1)</span><span class="sxs-lookup"><span data-stu-id="3cc08-122">**EVENT\_TRACE\_TYPE\_START**(Event type value is 1)</span></span><br/> | <span data-ttu-id="3cc08-123">Événement de démarrage du thread.</span><span class="sxs-lookup"><span data-stu-id="3cc08-123">Start thread event.</span></span> <span data-ttu-id="3cc08-124">La classe MOF [**\_ \_ TypeGroup1 du thread v2**](thread-v2-typegroup1.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="3cc08-124">The [**Thread\_V2\_TypeGroup1**](thread-v2-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                      |
| <span data-ttu-id="3cc08-125">Valeur de type d’événement, 3</span><span class="sxs-lookup"><span data-stu-id="3cc08-125">Event type value, 3</span></span>                                             | <span data-ttu-id="3cc08-126">Démarrez l’événement de thread de collecte de données.</span><span class="sxs-lookup"><span data-stu-id="3cc08-126">Start data collection thread event.</span></span> <span data-ttu-id="3cc08-127">Énumère les threads en cours d’exécution au moment du démarrage de la session du noyau.</span><span class="sxs-lookup"><span data-stu-id="3cc08-127">Enumerates threads that are currently running at the time the kernel session starts.</span></span> <span data-ttu-id="3cc08-128">La classe MOF [**\_ \_ TypeGroup1 du thread v2**](thread-v2-typegroup1.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="3cc08-128">The [**Thread\_V2\_TypeGroup1**](thread-v2-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="3cc08-129">Valeur de type d’événement, 4</span><span class="sxs-lookup"><span data-stu-id="3cc08-129">Event type value, 4</span></span>                                             | <span data-ttu-id="3cc08-130">Événement de thread de collecte de données de fin.</span><span class="sxs-lookup"><span data-stu-id="3cc08-130">End data collection thread event.</span></span> <span data-ttu-id="3cc08-131">Énumère les threads en cours d’exécution au moment de la fin de la session du noyau.</span><span class="sxs-lookup"><span data-stu-id="3cc08-131">Enumerates threads that are currently running at the time the kernel session ends.</span></span> <span data-ttu-id="3cc08-132">La classe MOF [**\_ \_ TypeGroup1 du thread v2**](thread-v2-typegroup1.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="3cc08-132">The [**Thread\_V2\_TypeGroup1**](thread-v2-typegroup1.md) MOF class defines the event data for this event.</span></span>     |
| <span data-ttu-id="3cc08-133">Valeur de type d’événement, 36</span><span class="sxs-lookup"><span data-stu-id="3cc08-133">Event type value, 36</span></span>                                            | <span data-ttu-id="3cc08-134">Événement de changement de contexte.</span><span class="sxs-lookup"><span data-stu-id="3cc08-134">Context switch event.</span></span> <span data-ttu-id="3cc08-135">La classe MOF [**CSwitch**](cswitch.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="3cc08-135">The [**CSwitch**](cswitch.md) MOF class defines the event data for this event.</span></span>                                                                                                                                |
| <span data-ttu-id="3cc08-136">Valeur de type d’événement, 50</span><span class="sxs-lookup"><span data-stu-id="3cc08-136">Event type value, 50</span></span>                                            | <span data-ttu-id="3cc08-137">Événement de thread Ready.</span><span class="sxs-lookup"><span data-stu-id="3cc08-137">Ready thread event.</span></span> <span data-ttu-id="3cc08-138">La classe MOF [**ReadyThread**](readythread.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="3cc08-138">The [**ReadyThread**](readythread.md) MOF class defines the event data for this event.</span></span>                                                                                                                          |



 

<span data-ttu-id="3cc08-139">Les événements de démarrage de processus et de thread peuvent être consignés dans le contexte du processus parent ou du thread.</span><span class="sxs-lookup"><span data-stu-id="3cc08-139">Process and thread start events may be logged in the context of the parent process or thread.</span></span> <span data-ttu-id="3cc08-140">Par conséquent, les membres **ProcessID** et **ThreadID** de l' [**\_ \_ en-tête de trace d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) peuvent ne pas correspondre au processus et au thread en cours de création.</span><span class="sxs-lookup"><span data-stu-id="3cc08-140">As a result, the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) may not correspond to the process and thread being created.</span></span> <span data-ttu-id="3cc08-141">C’est pourquoi ces événements contiennent les identificateurs de processus et de thread dans les données d’événement (en plus de ceux de l’en-tête d’événement).</span><span class="sxs-lookup"><span data-stu-id="3cc08-141">This is why these events contain the process and thread identifiers in the event data (in addition to those in the event header).</span></span>

## <a name="requirements"></a><span data-ttu-id="3cc08-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3cc08-142">Requirements</span></span>



| <span data-ttu-id="3cc08-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3cc08-143">Requirement</span></span> | <span data-ttu-id="3cc08-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="3cc08-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3cc08-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3cc08-145">Minimum supported client</span></span><br/> | <span data-ttu-id="3cc08-146">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3cc08-146">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3cc08-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3cc08-147">Minimum supported server</span></span><br/> | <span data-ttu-id="3cc08-148">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3cc08-148">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3cc08-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3cc08-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cc08-150">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="3cc08-150">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="3cc08-151">**CSwitch**</span><span class="sxs-lookup"><span data-stu-id="3cc08-151">**CSwitch**</span></span>](cswitch.md)
</dt> <dt>

[<span data-ttu-id="3cc08-152">**Thread**</span><span class="sxs-lookup"><span data-stu-id="3cc08-152">**Thread**</span></span>](thread.md)
</dt> <dt>

[<span data-ttu-id="3cc08-153">**Thread \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="3cc08-153">**Thread\_TypeGroup1**</span></span>](thread-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="3cc08-154">**Thread \_ v0**</span><span class="sxs-lookup"><span data-stu-id="3cc08-154">**Thread\_V0**</span></span>](thread-v0.md)
</dt> <dt>

[<span data-ttu-id="3cc08-155">**Thread \_ v1**</span><span class="sxs-lookup"><span data-stu-id="3cc08-155">**Thread\_V1**</span></span>](thread-v1.md)
</dt> </dl>

 

 
