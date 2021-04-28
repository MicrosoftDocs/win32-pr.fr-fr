---
description: 'Classe UdpIp : cette classe est la classe parente pour les événements UDP/IP. La syntaxe suivante est simplifiée à partir du code MOF.'
ms.assetid: 0fbecad2-0221-408e-9f43-859547efa803
title: UdpIp, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp
api_type:
- NA
api_location: ''
ms.openlocfilehash: d76aeb00ece18b026d9e5515a74ce830eb14af32
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105387"
---
# <a name="udpip-class"></a><span data-ttu-id="c6e46-104">UdpIp, classe</span><span class="sxs-lookup"><span data-stu-id="c6e46-104">UdpIp class</span></span>

<span data-ttu-id="c6e46-105">Cette classe est la classe parente pour les événements UDP/IP.</span><span class="sxs-lookup"><span data-stu-id="c6e46-105">This class is the parent class for UDP/IP events.</span></span>

<span data-ttu-id="c6e46-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="c6e46-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6e46-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c6e46-107">Syntax</span></span>

``` syntax
[Guid("{bf3a50c5-a9c9-4988-a005-2df0b7c80f80}"), EventVersion(2)]
class UdpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="c6e46-108">Membres</span><span class="sxs-lookup"><span data-stu-id="c6e46-108">Members</span></span>

<span data-ttu-id="c6e46-109">La classe **UdpIp** ne définit aucun membre.</span><span class="sxs-lookup"><span data-stu-id="c6e46-109">The **UdpIp** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6e46-110">Notes </span><span class="sxs-lookup"><span data-stu-id="c6e46-110">Remarks</span></span>

<span data-ttu-id="c6e46-111">Pour activer les événements UDP/IP dans une session de journalisation du noyau NT, spécifiez l’indicateur de **trace d’événements indicateur \_ \_ \_ réseau \_ tcpip** dans le membre **EnableFlags** d’une structure de propriétés de [**\_ trace \_ d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) lors de l’appel de la fonction [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="c6e46-111">To enable UDP/IP events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_NETWORK\_TCPIP** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="c6e46-112">Les consommateurs de suivi d’événements peuvent implémenter un traitement spécial pour les événements UDP/IP en appelant la fonction [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) et en spécifiant [**UdpIpGuid**](nt-kernel-logger-constants.md) comme paramètre *pguid* .</span><span class="sxs-lookup"><span data-stu-id="c6e46-112">Event trace consumers can implement special processing for UDP/IP events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**UdpIpGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="c6e46-113">Utilisez les types d’événements suivants pour identifier l’événement réseau (UDP/IP) réel lors de la consommation d’événements.</span><span class="sxs-lookup"><span data-stu-id="c6e46-113">Use the following event types to identify the actual network (UDP/IP) event when consuming events.</span></span>



| <span data-ttu-id="c6e46-114">Type d'événement</span><span class="sxs-lookup"><span data-stu-id="c6e46-114">Event type</span></span>                                                         | <span data-ttu-id="c6e46-115">Description</span><span class="sxs-lookup"><span data-stu-id="c6e46-115">Description</span></span>                                                                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6e46-116">**Événement \_ \_ \_ Réception du type de suivi**(la valeur du type d’événement est 11)</span><span class="sxs-lookup"><span data-stu-id="c6e46-116">**EVENT\_TRACE\_TYPE\_RECEIVE**(Event type value is 11)</span></span><br/> | <span data-ttu-id="c6e46-117">Événement de réception pour le protocole IPv4.</span><span class="sxs-lookup"><span data-stu-id="c6e46-117">Receive event for IPv4 protocol.</span></span> <span data-ttu-id="c6e46-118">La classe [**UdpIp \_ TypeGroup1**](udpip-typegroup1.md) MOF définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="c6e46-118">The [**UdpIp\_TypeGroup1**](udpip-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="c6e46-119">**Événement \_ Type de TRACE \_ \_ Send**(la valeur du type d’événement est 10)</span><span class="sxs-lookup"><span data-stu-id="c6e46-119">**EVENT\_TRACE\_TYPE\_SEND**(Event type value is 10)</span></span><br/>    | <span data-ttu-id="c6e46-120">Envoi d’un événement pour le protocole IPv4.</span><span class="sxs-lookup"><span data-stu-id="c6e46-120">Send event for IPv4 protocol.</span></span> <span data-ttu-id="c6e46-121">La classe [**UdpIp \_ TypeGroup1**](udpip-typegroup1.md) MOF définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="c6e46-121">The [**UdpIp\_TypeGroup1**](udpip-typegroup1.md) MOF class defines the event data for this event.</span></span>    |
| <span data-ttu-id="c6e46-122">Valeur de type d’événement, 17</span><span class="sxs-lookup"><span data-stu-id="c6e46-122">Event type value, 17</span></span>                                               | <span data-ttu-id="c6e46-123">Événement d’échec.</span><span class="sxs-lookup"><span data-stu-id="c6e46-123">Fail event.</span></span> <span data-ttu-id="c6e46-124">La classe MOF [**\_ Fail UdpIp**](udpip-fail.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="c6e46-124">The [**UdpIp\_Fail**](udpip-fail.md) MOF class defines the event data for this event.</span></span>                                  |
| <span data-ttu-id="c6e46-125">Valeur de type d’événement, 26</span><span class="sxs-lookup"><span data-stu-id="c6e46-125">Event type value, 26</span></span>                                               | <span data-ttu-id="c6e46-126">Envoi d’un événement pour le protocole IPv6.</span><span class="sxs-lookup"><span data-stu-id="c6e46-126">Send event for IPv6 protocol.</span></span> <span data-ttu-id="c6e46-127">La classe [**UdpIp \_ TypeGroup2**](udpip-typegroup2.md) MOF définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="c6e46-127">The [**UdpIp\_TypeGroup2**](udpip-typegroup2.md) MOF class defines the event data for this event.</span></span>    |
| <span data-ttu-id="c6e46-128">Valeur de type d’événement, 27</span><span class="sxs-lookup"><span data-stu-id="c6e46-128">Event type value, 27</span></span>                                               | <span data-ttu-id="c6e46-129">Événement Receive pour le protocole IPv6.</span><span class="sxs-lookup"><span data-stu-id="c6e46-129">Receive event for IPv6 protocol.</span></span> <span data-ttu-id="c6e46-130">La classe [**UdpIp \_ TypeGroup2**](udpip-typegroup2.md) MOF définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="c6e46-130">The [**UdpIp\_TypeGroup2**](udpip-typegroup2.md) MOF class defines the event data for this event.</span></span> |



 

<span data-ttu-id="c6e46-131">Vous pouvez suivre les événements réseau dans un processus source et de destination à l’aide de la propriété **ProcessID** .</span><span class="sxs-lookup"><span data-stu-id="c6e46-131">You can trace network events to a source and destination process using the **ProcessId** property.</span></span> <span data-ttu-id="c6e46-132">Étant donné que certains événements réseau sont journalisés par des threads distincts, vous ne pourrez peut-être pas utiliser les membres **ProcessID** et **ThreadID** de l' [**\_ \_ en-tête Event Trace**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) pour identifier le processus ou le thread à l’origine des activités réseau.</span><span class="sxs-lookup"><span data-stu-id="c6e46-132">Because some network events are logged by separate threads, you may not be able to use the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) to identify the process or thread that originated the network activities.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6e46-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c6e46-133">Requirements</span></span>



| <span data-ttu-id="c6e46-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c6e46-134">Requirement</span></span> | <span data-ttu-id="c6e46-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="c6e46-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c6e46-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6e46-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c6e46-137">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c6e46-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c6e46-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6e46-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c6e46-139">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c6e46-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c6e46-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6e46-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6e46-141">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="c6e46-141">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="c6e46-142">**Échec de UdpIp \_**</span><span class="sxs-lookup"><span data-stu-id="c6e46-142">**UdpIp\_Fail**</span></span>](udpip-fail.md)
</dt> <dt>

[<span data-ttu-id="c6e46-143">**UdpIp \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="c6e46-143">**UdpIp\_TypeGroup1**</span></span>](udpip-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="c6e46-144">**UdpIp \_ TypeGroup2**</span><span class="sxs-lookup"><span data-stu-id="c6e46-144">**UdpIp\_TypeGroup2**</span></span>](udpip-typegroup2.md)
</dt> <dt>

[<span data-ttu-id="c6e46-145">**UdpIp \_ v0**</span><span class="sxs-lookup"><span data-stu-id="c6e46-145">**UdpIp\_V0**</span></span>](udpip-v0.md)
</dt> <dt>

[<span data-ttu-id="c6e46-146">**UdpIp \_ v1**</span><span class="sxs-lookup"><span data-stu-id="c6e46-146">**UdpIp\_V1**</span></span>](udpip-v1.md)
</dt> </dl>

 

 
