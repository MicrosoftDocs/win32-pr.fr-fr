---
description: Cette classe est la classe parente des événements de processus. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: a505c693-2169-499b-bd32-42fa9bd69d2f
title: Process, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process
api_type:
- NA
api_location: ''
ms.openlocfilehash: b014262044db9e227bec5af2b351d1392c243c23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973567"
---
# <a name="process-class"></a><span data-ttu-id="a76f2-104">Process, classe</span><span class="sxs-lookup"><span data-stu-id="a76f2-104">Process class</span></span>

<span data-ttu-id="a76f2-105">Cette classe est la classe parente des événements de processus.</span><span class="sxs-lookup"><span data-stu-id="a76f2-105">This class is the parent class for process events.</span></span>

<span data-ttu-id="a76f2-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="a76f2-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a76f2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a76f2-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d0-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(3)]
class Process : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="a76f2-108">Membres</span><span class="sxs-lookup"><span data-stu-id="a76f2-108">Members</span></span>

<span data-ttu-id="a76f2-109">La classe **Process** ne définit aucun membre.</span><span class="sxs-lookup"><span data-stu-id="a76f2-109">The **Process** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="a76f2-110">Notes</span><span class="sxs-lookup"><span data-stu-id="a76f2-110">Remarks</span></span>

<span data-ttu-id="a76f2-111">Pour activer les événements de processus dans une session de journalisation du noyau NT, spécifiez l’indicateur de **\_ \_ \_ processus indicateur de suivi d’événement** dans le membre **EnableFlags** d’une structure de [**\_ \_ Propriétés de trace d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) lors de l’appel de la fonction [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="a76f2-111">To enable process events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_PROCESS** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="a76f2-112">Vous pouvez également spécifier l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="a76f2-112">You can also specify the following flag:</span></span>

-   <span data-ttu-id="a76f2-113">**compteurs de processus de l' \_ indicateur de trace d’événements \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a76f2-113">**EVENT\_TRACE\_FLAG\_PROCESS\_COUNTERS**</span></span>

<span data-ttu-id="a76f2-114">Les consommateurs de suivi d’événements peuvent implémenter un traitement spécial pour les événements de processus en appelant la fonction [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) et en spécifiant [**ProcessGuid**](nt-kernel-logger-constants.md) comme paramètre *pguid* .</span><span class="sxs-lookup"><span data-stu-id="a76f2-114">Event trace consumers can implement special processing for process events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ProcessGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="a76f2-115">Utilisez les types d’événements suivants pour identifier l’événement de processus réel lors de la consommation d’événements.</span><span class="sxs-lookup"><span data-stu-id="a76f2-115">Use the following event types to identify the actual process event when consuming events.</span></span>



| <span data-ttu-id="a76f2-116">Type d'événement</span><span class="sxs-lookup"><span data-stu-id="a76f2-116">Event type</span></span>                                                      | <span data-ttu-id="a76f2-117">Description</span><span class="sxs-lookup"><span data-stu-id="a76f2-117">Description</span></span>                                                                                                                                                                                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a76f2-118">**Événement \_ \_ \_ Fin du type de suivi**(la valeur du type d’événement est 2)</span><span class="sxs-lookup"><span data-stu-id="a76f2-118">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>   | <span data-ttu-id="a76f2-119">Événement de fin de processus.</span><span class="sxs-lookup"><span data-stu-id="a76f2-119">End process event.</span></span> <span data-ttu-id="a76f2-120">La classe MOF [**process \_ TypeGroup1**](process-typegroup1.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="a76f2-120">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                          |
| <span data-ttu-id="a76f2-121">**Événement \_ \_ \_ Début du type de suivi**(la valeur du type d’événement est 1)</span><span class="sxs-lookup"><span data-stu-id="a76f2-121">**EVENT\_TRACE\_TYPE\_START**(Event type value is 1)</span></span><br/> | <span data-ttu-id="a76f2-122">Événement de démarrage du processus.</span><span class="sxs-lookup"><span data-stu-id="a76f2-122">Start process event.</span></span> <span data-ttu-id="a76f2-123">La classe MOF [**process \_ TypeGroup1**](process-typegroup1.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="a76f2-123">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                        |
| <span data-ttu-id="a76f2-124">Valeur de type d’événement, 3</span><span class="sxs-lookup"><span data-stu-id="a76f2-124">Event type value, 3</span></span>                                             | <span data-ttu-id="a76f2-125">Démarrez l’événement processus de collecte de données.</span><span class="sxs-lookup"><span data-stu-id="a76f2-125">Start data collection process event.</span></span> <span data-ttu-id="a76f2-126">Énumère les processus en cours d’exécution au moment du démarrage de la session du noyau.</span><span class="sxs-lookup"><span data-stu-id="a76f2-126">Enumerates processes that are currently running at the time the kernel session starts.</span></span> <span data-ttu-id="a76f2-127">La classe MOF [**process \_ TypeGroup1**](process-typegroup1.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="a76f2-127">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="a76f2-128">Valeur de type d’événement, 4</span><span class="sxs-lookup"><span data-stu-id="a76f2-128">Event type value, 4</span></span>                                             | <span data-ttu-id="a76f2-129">Événement de fin de processus de collecte de données.</span><span class="sxs-lookup"><span data-stu-id="a76f2-129">End data collection process event.</span></span> <span data-ttu-id="a76f2-130">Énumère les processus en cours d’exécution au moment de la fin de la session du noyau.</span><span class="sxs-lookup"><span data-stu-id="a76f2-130">Enumerates processes that are currently running at the time the kernel session ends.</span></span> <span data-ttu-id="a76f2-131">La classe MOF [**process \_ TypeGroup1**](process-typegroup1.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="a76f2-131">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>     |



 

<span data-ttu-id="a76f2-132">Les événements de démarrage de processus et de thread peuvent être consignés dans le contexte du processus parent ou du thread.</span><span class="sxs-lookup"><span data-stu-id="a76f2-132">Process and thread start events may be logged in the context of the parent process or thread.</span></span> <span data-ttu-id="a76f2-133">Par conséquent, les membres **ProcessID** et **ThreadID** de l' [**\_ \_ en-tête de trace d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) peuvent ne pas correspondre au processus et au thread en cours de création.</span><span class="sxs-lookup"><span data-stu-id="a76f2-133">As a result, the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) may not correspond to the process and thread being created.</span></span> <span data-ttu-id="a76f2-134">C’est pourquoi ces événements contiennent les identificateurs de processus et de thread dans les données d’événement (en plus de ceux de l’en-tête d’événement).</span><span class="sxs-lookup"><span data-stu-id="a76f2-134">This is why these events contain the process and thread identifiers in the event data (in addition to those in the event header).</span></span>

## <a name="requirements"></a><span data-ttu-id="a76f2-135">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a76f2-135">Requirements</span></span>



| <span data-ttu-id="a76f2-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a76f2-136">Requirement</span></span> | <span data-ttu-id="a76f2-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="a76f2-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="a76f2-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a76f2-138">Minimum supported client</span></span><br/> | <span data-ttu-id="a76f2-139">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="a76f2-139">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>       |
| <span data-ttu-id="a76f2-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a76f2-140">Minimum supported server</span></span><br/> | <span data-ttu-id="a76f2-141">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="a76f2-141">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a76f2-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a76f2-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a76f2-143">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="a76f2-143">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="a76f2-144">**Traiter \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="a76f2-144">**Process\_TypeGroup1**</span></span>](process-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="a76f2-145">**Processus \_ v0**</span><span class="sxs-lookup"><span data-stu-id="a76f2-145">**Process\_V0**</span></span>](process-v0.md)
</dt> <dt>

[<span data-ttu-id="a76f2-146">**Traiter \_ v1**</span><span class="sxs-lookup"><span data-stu-id="a76f2-146">**Process\_V1**</span></span>](process-v1.md)
</dt> <dt>

[<span data-ttu-id="a76f2-147">**Traitement \_ v2**</span><span class="sxs-lookup"><span data-stu-id="a76f2-147">**Process\_V2**</span></span>](process-v2.md)
</dt> </dl>

 

 
