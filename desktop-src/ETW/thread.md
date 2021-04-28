---
description: 'Thread, classe : cette classe est la classe parente pour les événements de thread. La syntaxe suivante est simplifiée à partir du code MOF.'
ms.assetid: 0bf14240-3b8d-4eb5-b751-7b2e23b55762
title: Thread (classe)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread
api_type:
- NA
api_location: ''
ms.openlocfilehash: 121a8d4aa04017011648d80329ee02396582987a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105527"
---
# <a name="thread-class"></a><span data-ttu-id="70112-104">Thread (classe)</span><span class="sxs-lookup"><span data-stu-id="70112-104">Thread class</span></span>

<span data-ttu-id="70112-105">Cette classe est la classe parente pour les événements de thread.</span><span class="sxs-lookup"><span data-stu-id="70112-105">This class is the parent class for thread events.</span></span>

<span data-ttu-id="70112-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="70112-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="70112-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70112-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(3)]
class Thread : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="70112-108">Membres</span><span class="sxs-lookup"><span data-stu-id="70112-108">Members</span></span>

<span data-ttu-id="70112-109">La classe **thread** ne définit aucun membre.</span><span class="sxs-lookup"><span data-stu-id="70112-109">The **Thread** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="70112-110">Notes </span><span class="sxs-lookup"><span data-stu-id="70112-110">Remarks</span></span>

<span data-ttu-id="70112-111">Pour activer les événements de thread dans une session de journalisation du noyau NT, spécifiez l’indicateur de thread de l' **indicateur de \_ trace \_ \_ d’événements** dans le membre **EnableFlags** d’une structure de [**Propriétés de \_ trace \_ d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) lors de l’appel de la fonction [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="70112-111">To enable thread events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_THREAD** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="70112-112">Les consommateurs de suivi d’événements peuvent implémenter un traitement spécial pour les événements de thread en appelant la fonction [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) et en spécifiant [**ThreadGuid**](nt-kernel-logger-constants.md) comme paramètre *pguid* .</span><span class="sxs-lookup"><span data-stu-id="70112-112">Event trace consumers can implement special processing for thread events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ThreadGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="70112-113">Utilisez les types d’événements suivants pour identifier l’événement de thread réel lors de la consommation d’événements.</span><span class="sxs-lookup"><span data-stu-id="70112-113">Use the following event types to identify the actual thread event when consuming events.</span></span>



| <span data-ttu-id="70112-114">Type d'événement</span><span class="sxs-lookup"><span data-stu-id="70112-114">Event type</span></span>                                                      | <span data-ttu-id="70112-115">Description</span><span class="sxs-lookup"><span data-stu-id="70112-115">Description</span></span>                                                                                                                                                                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70112-116">**Événement \_ \_ \_ Fin du type de suivi**(la valeur du type d’événement est 2)</span><span class="sxs-lookup"><span data-stu-id="70112-116">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>   | <span data-ttu-id="70112-117">Événement de fin de thread.</span><span class="sxs-lookup"><span data-stu-id="70112-117">End thread event.</span></span> <span data-ttu-id="70112-118">La classe MOF du [**thread \_ TypeGroup1**](thread-typegroup1.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="70112-118">The [**Thread\_TypeGroup1**](thread-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                        |
| <span data-ttu-id="70112-119">**Événement \_ \_ \_ Début du type de suivi**(la valeur du type d’événement est 1)</span><span class="sxs-lookup"><span data-stu-id="70112-119">**EVENT\_TRACE\_TYPE\_START**(Event type value is 1)</span></span><br/> | <span data-ttu-id="70112-120">Événement de démarrage du thread.</span><span class="sxs-lookup"><span data-stu-id="70112-120">Start thread event.</span></span> <span data-ttu-id="70112-121">La classe MOF du [**thread \_ TypeGroup1**](thread-typegroup1.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="70112-121">The [**Thread\_TypeGroup1**](thread-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                      |
| <span data-ttu-id="70112-122">Valeur de type d’événement, 3</span><span class="sxs-lookup"><span data-stu-id="70112-122">Event type value, 3</span></span>                                             | <span data-ttu-id="70112-123">Démarrez l’événement de thread de collecte de données.</span><span class="sxs-lookup"><span data-stu-id="70112-123">Start data collection thread event.</span></span> <span data-ttu-id="70112-124">Énumère les threads en cours d’exécution au moment du démarrage de la session du noyau.</span><span class="sxs-lookup"><span data-stu-id="70112-124">Enumerates threads that are currently running at the time the kernel session starts.</span></span> <span data-ttu-id="70112-125">La classe MOF du [**thread \_ TypeGroup1**](thread-typegroup1.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="70112-125">The [**Thread\_TypeGroup1**](thread-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="70112-126">Valeur de type d’événement, 4</span><span class="sxs-lookup"><span data-stu-id="70112-126">Event type value, 4</span></span>                                             | <span data-ttu-id="70112-127">Événement de thread de collecte de données de fin.</span><span class="sxs-lookup"><span data-stu-id="70112-127">End data collection thread event.</span></span> <span data-ttu-id="70112-128">Énumère les threads en cours d’exécution au moment de la fin de la session du noyau.</span><span class="sxs-lookup"><span data-stu-id="70112-128">Enumerates threads that are currently running at the time the kernel session ends.</span></span> <span data-ttu-id="70112-129">La classe MOF du [**thread \_ TypeGroup1**](thread-typegroup1.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="70112-129">The [**Thread\_TypeGroup1**](thread-typegroup1.md) MOF class defines the event data for this event.</span></span>     |



 

<span data-ttu-id="70112-130">Les événements de démarrage de processus et de thread peuvent être consignés dans le contexte du processus parent ou du thread.</span><span class="sxs-lookup"><span data-stu-id="70112-130">Process and thread start events may be logged in the context of the parent process or thread.</span></span> <span data-ttu-id="70112-131">Par conséquent, les membres **ProcessID** et **ThreadID** de l' [**\_ \_ en-tête de trace d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) peuvent ne pas correspondre au processus et au thread en cours de création.</span><span class="sxs-lookup"><span data-stu-id="70112-131">As a result, the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) may not correspond to the process and thread being created.</span></span> <span data-ttu-id="70112-132">C’est pourquoi ces événements contiennent les identificateurs de processus et de thread dans les données d’événement (en plus de ceux de l’en-tête d’événement).</span><span class="sxs-lookup"><span data-stu-id="70112-132">This is why these events contain the process and thread identifiers in the event data (in addition to those in the event header).</span></span>

## <a name="requirements"></a><span data-ttu-id="70112-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70112-133">Requirements</span></span>



| <span data-ttu-id="70112-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70112-134">Requirement</span></span> | <span data-ttu-id="70112-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="70112-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="70112-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70112-136">Minimum supported client</span></span><br/> | <span data-ttu-id="70112-137">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="70112-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="70112-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70112-138">Minimum supported server</span></span><br/> | <span data-ttu-id="70112-139">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="70112-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="70112-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70112-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70112-141">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="70112-141">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="70112-142">**Thread \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="70112-142">**Thread\_TypeGroup1**</span></span>](thread-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="70112-143">**Thread \_ v0**</span><span class="sxs-lookup"><span data-stu-id="70112-143">**Thread\_V0**</span></span>](thread-v0.md)
</dt> <dt>

[<span data-ttu-id="70112-144">**Thread \_ v1**</span><span class="sxs-lookup"><span data-stu-id="70112-144">**Thread\_V1**</span></span>](thread-v1.md)
</dt> <dt>

[<span data-ttu-id="70112-145">**Thread \_ v2**</span><span class="sxs-lookup"><span data-stu-id="70112-145">**Thread\_V2**</span></span>](thread-v2.md)
</dt> </dl>

 

 
