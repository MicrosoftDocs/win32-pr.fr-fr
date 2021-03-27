---
description: Cette classe est la classe parente pour les événements de compteur de performance. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 2606fea3-0651-4f7f-83a6-63021039eb95
title: PerfInfo, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PerfInfo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 93f12242fef86e5eab81bb702b783eb1f4c1915c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972226"
---
# <a name="perfinfo-class"></a><span data-ttu-id="111fb-104">PerfInfo, classe</span><span class="sxs-lookup"><span data-stu-id="111fb-104">PerfInfo class</span></span>

<span data-ttu-id="111fb-105">Cette classe est la classe parente pour les événements de compteur de performance.</span><span class="sxs-lookup"><span data-stu-id="111fb-105">This class is the parent class for performance counter events.</span></span>

<span data-ttu-id="111fb-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="111fb-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="111fb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="111fb-107">Syntax</span></span>

``` syntax
[Guid("{ce1dbfb4-137e-4da6-87b0-3f59aa102cbc}"), EventVersion(2)]
class PerfInfo : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="111fb-108">Membres</span><span class="sxs-lookup"><span data-stu-id="111fb-108">Members</span></span>

<span data-ttu-id="111fb-109">La classe **PerfInfo** ne définit aucun membre.</span><span class="sxs-lookup"><span data-stu-id="111fb-109">The **PerfInfo** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="111fb-110">Notes</span><span class="sxs-lookup"><span data-stu-id="111fb-110">Remarks</span></span>

<span data-ttu-id="111fb-111">Pour activer les événements DPC (appels de procédure différés) dans une session de journalisation du noyau NT, spécifiez l’indicateur  DPC de l’indicateur de suivi d' **événement \_ \_ \_** dans le membre EnableFlags d’une structure de [**Propriétés de \_ trace \_ d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) lors de l’appel de la fonction [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="111fb-111">To enable deferred procedure call (DPC) events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_DPC** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="111fb-112">Vous pouvez également spécifier un ou plusieurs des indicateurs suivants :</span><span class="sxs-lookup"><span data-stu-id="111fb-112">You can also specify one or more of the following flags:</span></span>

-   <span data-ttu-id="111fb-113">**indicateur de suivi d’événement, \_ \_ \_ interruption**</span><span class="sxs-lookup"><span data-stu-id="111fb-113">**EVENT\_TRACE\_FLAG\_INTERRUPT**</span></span>
-   <span data-ttu-id="111fb-114">**\_profil d' \_ indicateur de trace d’événements \_**</span><span class="sxs-lookup"><span data-stu-id="111fb-114">**EVENT\_TRACE\_FLAG\_PROFILE**</span></span>
-   <span data-ttu-id="111fb-115">**indicateur de suivi d’événement \_ \_ \_ SYSTEMCALL**</span><span class="sxs-lookup"><span data-stu-id="111fb-115">**EVENT\_TRACE\_FLAG\_SYSTEMCALL**</span></span>

<span data-ttu-id="111fb-116">Les consommateurs de suivi d’événements peuvent implémenter un traitement spécial pour les événements DPC en appelant la fonction [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) et en spécifiant [**PerfInfoGuid**](nt-kernel-logger-constants.md) comme paramètre *pguid* .</span><span class="sxs-lookup"><span data-stu-id="111fb-116">Event trace consumers can implement special processing for DPC events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**PerfInfoGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="111fb-117">Utilisez les types d’événements suivants pour identifier l’événement réel lors de la consommation d’événements.</span><span class="sxs-lookup"><span data-stu-id="111fb-117">Use the following event types to identify the actual event when consuming events.</span></span>



| <span data-ttu-id="111fb-118">Type d'événement</span><span class="sxs-lookup"><span data-stu-id="111fb-118">Event type</span></span>           | <span data-ttu-id="111fb-119">Description</span><span class="sxs-lookup"><span data-stu-id="111fb-119">Description</span></span>                                                                                                          |
|----------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="111fb-120">Valeur de type d’événement, 46</span><span class="sxs-lookup"><span data-stu-id="111fb-120">Event type value, 46</span></span> | <span data-ttu-id="111fb-121">Événement de profil échantillonné.</span><span class="sxs-lookup"><span data-stu-id="111fb-121">Sampled profile event.</span></span> <span data-ttu-id="111fb-122">La classe MOF [**SampledProfile**](sampledprofile.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="111fb-122">The [**SampledProfile**](sampledprofile.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="111fb-123">Valeur de type d’événement, 51</span><span class="sxs-lookup"><span data-stu-id="111fb-123">Event type value, 51</span></span> | <span data-ttu-id="111fb-124">Événement d’entrée d’appel système.</span><span class="sxs-lookup"><span data-stu-id="111fb-124">System call enter event.</span></span> <span data-ttu-id="111fb-125">La classe MOF [**SysCallEnter**](syscallenter.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="111fb-125">The [**SysCallEnter**](syscallenter.md) MOF class defines the event data for this event.</span></span>   |
| <span data-ttu-id="111fb-126">Valeur de type d’événement, 52</span><span class="sxs-lookup"><span data-stu-id="111fb-126">Event type value, 52</span></span> | <span data-ttu-id="111fb-127">Événement de sortie de l’appel système.</span><span class="sxs-lookup"><span data-stu-id="111fb-127">System call exit event.</span></span> <span data-ttu-id="111fb-128">La classe MOF [**SysCallExit**](syscallexit.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="111fb-128">The [**SysCallExit**](syscallexit.md) MOF class defines the event data for this event.</span></span>      |
| <span data-ttu-id="111fb-129">Valeur de type d’événement, 66</span><span class="sxs-lookup"><span data-stu-id="111fb-129">Event type value, 66</span></span> | <span data-ttu-id="111fb-130">Événement DPC lié à un thread.</span><span class="sxs-lookup"><span data-stu-id="111fb-130">Threaded DPC event.</span></span> <span data-ttu-id="111fb-131">La classe MOF [**DPC**](dpc.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="111fb-131">The [**DPC**](dpc.md) MOF class defines the event data for this event.</span></span>                          |
| <span data-ttu-id="111fb-132">Valeur de type d’événement, 67</span><span class="sxs-lookup"><span data-stu-id="111fb-132">Event type value, 67</span></span> | <span data-ttu-id="111fb-133">Événement de routine de service d’interruption (ISR).</span><span class="sxs-lookup"><span data-stu-id="111fb-133">Interrupt service routine (ISR) event.</span></span> <span data-ttu-id="111fb-134">La classe MOF [**ISR**](isr.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="111fb-134">The [**ISR**](isr.md) MOF class defines the event data for this event.</span></span>       |
| <span data-ttu-id="111fb-135">Valeur de type d’événement, 68</span><span class="sxs-lookup"><span data-stu-id="111fb-135">Event type value, 68</span></span> | <span data-ttu-id="111fb-136">Événement DPC.</span><span class="sxs-lookup"><span data-stu-id="111fb-136">DPC event.</span></span> <span data-ttu-id="111fb-137">La classe MOF [**DPC**](dpc.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="111fb-137">The [**DPC**](dpc.md) MOF class defines the event data for this event.</span></span>                                   |
| <span data-ttu-id="111fb-138">Valeur de type d’événement, 69</span><span class="sxs-lookup"><span data-stu-id="111fb-138">Event type value, 69</span></span> | <span data-ttu-id="111fb-139">Événement du minuteur DPC.</span><span class="sxs-lookup"><span data-stu-id="111fb-139">DPC timer event.</span></span> <span data-ttu-id="111fb-140">La classe MOF [**DPC**](dpc.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="111fb-140">The [**DPC**](dpc.md) MOF class defines the event data for this event.</span></span>                             |



 

## <a name="requirements"></a><span data-ttu-id="111fb-141">Spécifications</span><span class="sxs-lookup"><span data-stu-id="111fb-141">Requirements</span></span>



| <span data-ttu-id="111fb-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="111fb-142">Requirement</span></span> | <span data-ttu-id="111fb-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="111fb-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="111fb-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="111fb-144">Minimum supported client</span></span><br/> | <span data-ttu-id="111fb-145">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="111fb-145">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="111fb-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="111fb-146">Minimum supported server</span></span><br/> | <span data-ttu-id="111fb-147">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="111fb-147">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 
