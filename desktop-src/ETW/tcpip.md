---
description: 'TcpIp, classe : cette classe est la classe parente pour les événements TCP/IP. La syntaxe suivante est simplifiée à partir du code MOF.'
ms.assetid: f9d6ea8f-c777-4747-89f4-f389c6eeac35
title: TcpIp (classe)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp
api_type:
- NA
api_location: ''
ms.openlocfilehash: abcd805b417451adf2122e7baf3310be101a35ff
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105727"
---
# <a name="tcpip-class"></a><span data-ttu-id="3c79f-104">TcpIp (classe)</span><span class="sxs-lookup"><span data-stu-id="3c79f-104">TcpIp class</span></span>

<span data-ttu-id="3c79f-105">Cette classe est la classe parente pour les événements TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="3c79f-105">This class is the parent class for TCP/IP events.</span></span>

<span data-ttu-id="3c79f-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="3c79f-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c79f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c79f-107">Syntax</span></span>

``` syntax
[Guid("{9a280ac0-c8e0-11d1-84e2-00c04fb998a2}"), EventVersion(2)]
class TcpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="3c79f-108">Membres</span><span class="sxs-lookup"><span data-stu-id="3c79f-108">Members</span></span>

<span data-ttu-id="3c79f-109">La classe **TcpIp** ne définit aucun membre.</span><span class="sxs-lookup"><span data-stu-id="3c79f-109">The **TcpIp** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c79f-110">Notes </span><span class="sxs-lookup"><span data-stu-id="3c79f-110">Remarks</span></span>

<span data-ttu-id="3c79f-111">Pour activer les événements TCP/IP dans une session de journalisation du noyau NT, spécifiez l’indicateur de **trace d’événement indicateur \_ \_ \_ réseau \_ tcpip** dans le membre **EnableFlags** d’une structure de propriétés de [**\_ trace \_ d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) lors de l’appel de la fonction [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="3c79f-111">To enable TCP/IP events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_NETWORK\_TCPIP** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="3c79f-112">Les consommateurs de suivi d’événements peuvent implémenter un traitement spécial pour les événements TCP/IP en appelant la fonction [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) et en spécifiant [**TcpIpGuid**](nt-kernel-logger-constants.md) comme paramètre *pguid* .</span><span class="sxs-lookup"><span data-stu-id="3c79f-112">Event trace consumers can implement special processing for TCP/IP events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**TcpIpGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="3c79f-113">Utilisez les types d’événements suivants pour identifier l’événement réseau (TCP/IP) réel lors de la consommation d’événements.</span><span class="sxs-lookup"><span data-stu-id="3c79f-113">Use the following event types to identify the actual network (TCP/IP) event when consuming events.</span></span>



| <span data-ttu-id="3c79f-114">Type d'événement</span><span class="sxs-lookup"><span data-stu-id="3c79f-114">Event type</span></span>                                                            | <span data-ttu-id="3c79f-115">Description</span><span class="sxs-lookup"><span data-stu-id="3c79f-115">Description</span></span>                                                                                                                                                                                   |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c79f-116">**Événement \_ Type de suivi \_ \_ Accept**(la valeur de type d’événement est 15)</span><span class="sxs-lookup"><span data-stu-id="3c79f-116">**EVENT\_TRACE\_TYPE\_ACCEPT**(Event type value is 15)</span></span><br/>     | <span data-ttu-id="3c79f-117">Accepter un événement pour le protocole IPv4.</span><span class="sxs-lookup"><span data-stu-id="3c79f-117">Accept event for IPv4 protocol.</span></span> <span data-ttu-id="3c79f-118">La classe MOF [**\_ TypeGroup2**](tcpip-typegroup2.md) MOF définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="3c79f-118">The [**TcpIp\_TypeGroup2**](tcpip-typegroup2.md) MOF class defines the event data for this event.</span></span>                                                            |
| <span data-ttu-id="3c79f-119">**Événement \_ Type de suivi \_ \_ Connect**(la valeur de type d’événement est 12)</span><span class="sxs-lookup"><span data-stu-id="3c79f-119">**EVENT\_TRACE\_TYPE\_CONNECT**(Event type value is 12)</span></span><br/>    | <span data-ttu-id="3c79f-120">Événement Connect pour le protocole IPv4.</span><span class="sxs-lookup"><span data-stu-id="3c79f-120">Connect event for IPv4 protocol.</span></span> <span data-ttu-id="3c79f-121">La classe MOF [**\_ TypeGroup2**](tcpip-typegroup2.md) MOF définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="3c79f-121">The [**TcpIp\_TypeGroup2**](tcpip-typegroup2.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="3c79f-122">**Événement \_ Type de TRACE \_ \_ Disconnect**(la valeur du type d’événement est 13)</span><span class="sxs-lookup"><span data-stu-id="3c79f-122">**EVENT\_TRACE\_TYPE\_DISCONNECT**(Event type value is 13)</span></span><br/> | <span data-ttu-id="3c79f-123">Événement de déconnexion pour le protocole IPv4.</span><span class="sxs-lookup"><span data-stu-id="3c79f-123">Disconnect event for IPv4 protocol.</span></span> <span data-ttu-id="3c79f-124">La classe MOF [**\_ TypeGroup1**](tcpip-typegroup1.md) MOF définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="3c79f-124">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="3c79f-125">**Événement \_ \_ \_ Réception du type de suivi**(la valeur du type d’événement est 11)</span><span class="sxs-lookup"><span data-stu-id="3c79f-125">**EVENT\_TRACE\_TYPE\_RECEIVE**(Event type value is 11)</span></span><br/>    | <span data-ttu-id="3c79f-126">Événement de réception pour le protocole IPv4.</span><span class="sxs-lookup"><span data-stu-id="3c79f-126">Receive event for IPv4 protocol.</span></span> <span data-ttu-id="3c79f-127">La classe MOF [**\_ TypeGroup1**](tcpip-typegroup1.md) MOF définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="3c79f-127">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="3c79f-128">**Événement \_ \_REconnexion \_ du type de suivi**(la valeur du type d’événement est 16)</span><span class="sxs-lookup"><span data-stu-id="3c79f-128">**EVENT\_TRACE\_TYPE\_RECONNECT**(Event type value is 16)</span></span><br/>  | <span data-ttu-id="3c79f-129">Événement de reconnexion pour le protocole IPv4.</span><span class="sxs-lookup"><span data-stu-id="3c79f-129">Reconnect event for IPv4 protocol.</span></span> <span data-ttu-id="3c79f-130">(Une tentative de connexion a échoué et une autre tentative est effectuée.) La classe MOF [**\_ TypeGroup1**](tcpip-typegroup1.md) MOF définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="3c79f-130">(A connect attempt failed and another attempt is made.) The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="3c79f-131">**Événement \_ \_REtransmission \_ du type de suivi**(la valeur du type d’événement est 14)</span><span class="sxs-lookup"><span data-stu-id="3c79f-131">**EVENT\_TRACE\_TYPE\_RETRANSMIT**(Event type value is 14)</span></span><br/> | <span data-ttu-id="3c79f-132">Événement de retransmission pour le protocole IPv4.</span><span class="sxs-lookup"><span data-stu-id="3c79f-132">Retransmit event for IPv4 protocol.</span></span> <span data-ttu-id="3c79f-133">La classe MOF [**\_ TypeGroup1**](tcpip-typegroup1.md) MOF définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="3c79f-133">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="3c79f-134">**Événement \_ Type de TRACE \_ \_ Send**(la valeur du type d’événement est 10)</span><span class="sxs-lookup"><span data-stu-id="3c79f-134">**EVENT\_TRACE\_TYPE\_SEND**(Event type value is 10)</span></span><br/>       | <span data-ttu-id="3c79f-135">Envoi d’un événement pour le protocole IPv4.</span><span class="sxs-lookup"><span data-stu-id="3c79f-135">Send event for IPv4 protocol.</span></span> <span data-ttu-id="3c79f-136">La classe MOF [**\_ SendIPV4**](tcpip-sendipv4.md) MOF définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="3c79f-136">The [**TcpIp\_SendIPV4**](tcpip-sendipv4.md) MOF class defines the event data for this event.</span></span>                                                                  |
| <span data-ttu-id="3c79f-137">Valeur de type d’événement, 17</span><span class="sxs-lookup"><span data-stu-id="3c79f-137">Event type value, 17</span></span>                                                  | <span data-ttu-id="3c79f-138">Événement d’échec.</span><span class="sxs-lookup"><span data-stu-id="3c79f-138">Fail event.</span></span> <span data-ttu-id="3c79f-139">La classe MOF d' [**\_ échec TcpIp**](tcpip-fail.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="3c79f-139">The [**TcpIp\_Fail**](tcpip-fail.md) MOF class defines the event data for this event.</span></span>                                                                                            |
| <span data-ttu-id="3c79f-140">Valeur de type d’événement, 18</span><span class="sxs-lookup"><span data-stu-id="3c79f-140">Event type value, 18</span></span>                                                  | <span data-ttu-id="3c79f-141">Événement TCP Copy pour le protocole IPv4.</span><span class="sxs-lookup"><span data-stu-id="3c79f-141">TCP copy event for IPv4 protocol.</span></span> <span data-ttu-id="3c79f-142">La classe MOF [**\_ TypeGroup1**](tcpip-typegroup1.md) MOF définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="3c79f-142">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                          |
| <span data-ttu-id="3c79f-143">Valeur de type d’événement, 26</span><span class="sxs-lookup"><span data-stu-id="3c79f-143">Event type value, 26</span></span>                                                  | <span data-ttu-id="3c79f-144">Envoi d’un événement pour le protocole IPv6.</span><span class="sxs-lookup"><span data-stu-id="3c79f-144">Send event for IPv6 protocol.</span></span> <span data-ttu-id="3c79f-145">La classe MOF [**\_ SendIPV6**](tcpip-sendipv6.md) MOF définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="3c79f-145">The [**TcpIp\_SendIPV6**](tcpip-sendipv6.md) MOF class defines the event data for this event.</span></span>                                                                  |
| <span data-ttu-id="3c79f-146">Valeur de type d’événement, 27</span><span class="sxs-lookup"><span data-stu-id="3c79f-146">Event type value, 27</span></span>                                                  | <span data-ttu-id="3c79f-147">Événement Receive pour le protocole IPv6.</span><span class="sxs-lookup"><span data-stu-id="3c79f-147">Receive event for IPv6 protocol.</span></span> <span data-ttu-id="3c79f-148">La classe MOF [**\_ TypeGroup3**](tcpip-typegroup3.md) MOF définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="3c79f-148">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="3c79f-149">Valeur du type d’événement, 28</span><span class="sxs-lookup"><span data-stu-id="3c79f-149">Event type value, 28</span></span>                                                  | <span data-ttu-id="3c79f-150">Événement Connect pour le protocole IPv6.</span><span class="sxs-lookup"><span data-stu-id="3c79f-150">Connect event for IPv6 protocol.</span></span> <span data-ttu-id="3c79f-151">La classe MOF [**\_ TypeGroup4**](tcpip-typegroup4.md) MOF définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="3c79f-151">The [**TcpIp\_TypeGroup4**](tcpip-typegroup4.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="3c79f-152">Valeur de type d’événement, 29</span><span class="sxs-lookup"><span data-stu-id="3c79f-152">Event type value, 29</span></span>                                                  | <span data-ttu-id="3c79f-153">Événement de déconnexion pour le protocole IPv6.</span><span class="sxs-lookup"><span data-stu-id="3c79f-153">Disconnect event for IPv6 protocol.</span></span> <span data-ttu-id="3c79f-154">La classe MOF [**\_ TypeGroup3**](tcpip-typegroup3.md) MOF définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="3c79f-154">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="3c79f-155">Valeur de type d’événement, 30</span><span class="sxs-lookup"><span data-stu-id="3c79f-155">Event type value, 30</span></span>                                                  | <span data-ttu-id="3c79f-156">Événement de retransmission pour le protocole IPv6.</span><span class="sxs-lookup"><span data-stu-id="3c79f-156">Retransmit event for IPv6 protocol.</span></span> <span data-ttu-id="3c79f-157">La classe MOF [**\_ TypeGroup3**](tcpip-typegroup3.md) MOF définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="3c79f-157">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="3c79f-158">Valeur de type d’événement 31</span><span class="sxs-lookup"><span data-stu-id="3c79f-158">Event type value, 31</span></span>                                                  | <span data-ttu-id="3c79f-159">Accepter un événement pour le protocole IPv6.</span><span class="sxs-lookup"><span data-stu-id="3c79f-159">Accept event for IPv6 protocol.</span></span> <span data-ttu-id="3c79f-160">La classe MOF [**\_ TypeGroup4**](tcpip-typegroup4.md) MOF définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="3c79f-160">The [**TcpIp\_TypeGroup4**](tcpip-typegroup4.md) MOF class defines the event data for this event.</span></span>                                                            |
| <span data-ttu-id="3c79f-161">Valeur de type d’événement, 32</span><span class="sxs-lookup"><span data-stu-id="3c79f-161">Event type value, 32</span></span>                                                  | <span data-ttu-id="3c79f-162">Événement de reconnexion pour le protocole IPv6.</span><span class="sxs-lookup"><span data-stu-id="3c79f-162">Reconnect event for IPv6 protocol.</span></span> <span data-ttu-id="3c79f-163">(Une tentative de connexion a échoué et une autre tentative est effectuée.) La classe MOF [**\_ TypeGroup3**](tcpip-typegroup3.md) MOF définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="3c79f-163">(A connect attempt failed and another attempt is made.) The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="3c79f-164">Valeur de type d’événement, 34</span><span class="sxs-lookup"><span data-stu-id="3c79f-164">Event type value, 34</span></span>                                                  | <span data-ttu-id="3c79f-165">Événement TCP Copy pour le protocole IPv6.</span><span class="sxs-lookup"><span data-stu-id="3c79f-165">TCP copy event for IPv6 protocol.</span></span> <span data-ttu-id="3c79f-166">La classe MOF [**\_ TypeGroup3**](tcpip-typegroup3.md) MOF définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="3c79f-166">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                          |



 

<span data-ttu-id="3c79f-167">Vous pouvez suivre les événements réseau dans un processus source et de destination à l’aide de la propriété **ProcessID** .</span><span class="sxs-lookup"><span data-stu-id="3c79f-167">You can trace network events to a source and destination process using the **ProcessId** property.</span></span> <span data-ttu-id="3c79f-168">Étant donné que certains événements réseau sont journalisés par des threads distincts, vous ne pourrez peut-être pas utiliser les membres **ProcessID** et **ThreadID** de l' [**\_ \_ en-tête Event Trace**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) pour identifier le processus ou le thread à l’origine des activités réseau.</span><span class="sxs-lookup"><span data-stu-id="3c79f-168">Because some network events are logged by separate threads, you may not be able to use the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) to identify the process or thread that originated the network activities.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c79f-169">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c79f-169">Requirements</span></span>



| <span data-ttu-id="3c79f-170">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c79f-170">Requirement</span></span> | <span data-ttu-id="3c79f-171">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c79f-171">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3c79f-172">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c79f-172">Minimum supported client</span></span><br/> | <span data-ttu-id="3c79f-173">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3c79f-173">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3c79f-174">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c79f-174">Minimum supported server</span></span><br/> | <span data-ttu-id="3c79f-175">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3c79f-175">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3c79f-176">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c79f-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c79f-177">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="3c79f-177">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="3c79f-178">**Échec de TcpIp \_**</span><span class="sxs-lookup"><span data-stu-id="3c79f-178">**TcpIp\_Fail**</span></span>](tcpip-fail.md)
</dt> <dt>

[<span data-ttu-id="3c79f-179">**TcpIp \_ SendIPV4**</span><span class="sxs-lookup"><span data-stu-id="3c79f-179">**TcpIp\_SendIPV4**</span></span>](tcpip-sendipv4.md)
</dt> <dt>

[<span data-ttu-id="3c79f-180">**TcpIp \_ SendIPV6**</span><span class="sxs-lookup"><span data-stu-id="3c79f-180">**TcpIp\_SendIPV6**</span></span>](tcpip-sendipv6.md)
</dt> <dt>

[<span data-ttu-id="3c79f-181">**TcpIp \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="3c79f-181">**TcpIp\_TypeGroup1**</span></span>](tcpip-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="3c79f-182">**TcpIp \_ TypeGroup2**</span><span class="sxs-lookup"><span data-stu-id="3c79f-182">**TcpIp\_TypeGroup2**</span></span>](tcpip-typegroup2.md)
</dt> <dt>

[<span data-ttu-id="3c79f-183">**TcpIp \_ TypeGroup3**</span><span class="sxs-lookup"><span data-stu-id="3c79f-183">**TcpIp\_TypeGroup3**</span></span>](tcpip-typegroup3.md)
</dt> <dt>

[<span data-ttu-id="3c79f-184">**TcpIp \_ TypeGroup4**</span><span class="sxs-lookup"><span data-stu-id="3c79f-184">**TcpIp\_TypeGroup4**</span></span>](tcpip-typegroup4.md)
</dt> <dt>

[<span data-ttu-id="3c79f-185">**TcpIp \_ v0**</span><span class="sxs-lookup"><span data-stu-id="3c79f-185">**TcpIp\_V0**</span></span>](tcpip-v0.md)
</dt> <dt>

[<span data-ttu-id="3c79f-186">**TcpIp \_ v1**</span><span class="sxs-lookup"><span data-stu-id="3c79f-186">**TcpIp\_V1**</span></span>](tcpip-v1.md)
</dt> </dl>

 

 
