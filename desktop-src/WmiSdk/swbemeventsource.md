---
description: L’objet SWbemEventSource récupère les événements d’une requête d’événement conjointement avec SWbemServices.ExecNotificationQuery.
ms.assetid: 7efd5e6a-4311-4d20-8b05-e9208eec098a
ms.tgt_platform: multiple
title: Objet SWbemEventSource (wbemdisp. h)
ms.topic: reference
ms.date: 09/25/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemEventSource
- ISWbemEventSource
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8da55a7b6722c263fe9a3fb0af7a8db07d672e12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527625"
---
# <a name="swbemeventsource-object"></a><span data-ttu-id="0f68c-103">Objet SWbemEventSource</span><span class="sxs-lookup"><span data-stu-id="0f68c-103">SWbemEventSource object</span></span>

<span data-ttu-id="0f68c-104">L’objet **SWbemEventSource** récupère les événements d’une requête d’événement conjointement avec [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).</span><span class="sxs-lookup"><span data-stu-id="0f68c-104">The **SWbemEventSource** object retrieves events from an event query in conjunction with [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).</span></span> <span data-ttu-id="0f68c-105">Vous recevez un objet **SWbemEventSource** si vous effectuez un appel à **SWbemServices.ExecNotificationQuery** pour effectuer une requête d’événement.</span><span class="sxs-lookup"><span data-stu-id="0f68c-105">You get an **SWbemEventSource** object if you make a call to **SWbemServices.ExecNotificationQuery** to make an event query.</span></span> <span data-ttu-id="0f68c-106">Vous pouvez ensuite utiliser la méthode [**NextEvent**](swbemeventsource-nextevent.md) pour récupérer les événements à mesure qu’ils arrivent.</span><span class="sxs-lookup"><span data-stu-id="0f68c-106">You can then use the [**NextEvent**](swbemeventsource-nextevent.md) method to retrieve events as they arrive.</span></span> <span data-ttu-id="0f68c-107">Cet objet ne peut pas être créé par l’appel VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="0f68c-107">This object cannot be created by the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call.</span></span>

## <a name="members"></a><span data-ttu-id="0f68c-108">Membres</span><span class="sxs-lookup"><span data-stu-id="0f68c-108">Members</span></span>

<span data-ttu-id="0f68c-109">L’objet **SWbemEventSource** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0f68c-109">The **SWbemEventSource** object has these types of members:</span></span>

-   [<span data-ttu-id="0f68c-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0f68c-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="0f68c-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0f68c-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0f68c-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0f68c-112">Methods</span></span>

<span data-ttu-id="0f68c-113">L’objet **SWbemEventSource** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="0f68c-113">The **SWbemEventSource** object has these methods.</span></span>



| <span data-ttu-id="0f68c-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="0f68c-114">Method</span></span>                                          | <span data-ttu-id="0f68c-115">Description</span><span class="sxs-lookup"><span data-stu-id="0f68c-115">Description</span></span>                                                                                                                                  |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0f68c-116">**NextEvent**</span><span class="sxs-lookup"><span data-stu-id="0f68c-116">**NextEvent**</span></span>](swbemeventsource-nextevent.md) | <span data-ttu-id="0f68c-117">Utilisé pour récupérer un événement conjointement à [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).</span><span class="sxs-lookup"><span data-stu-id="0f68c-117">Used to retrieve an event in conjunction with [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0f68c-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0f68c-118">Properties</span></span>

<span data-ttu-id="0f68c-119">L’objet **SWbemEventSource** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="0f68c-119">The **SWbemEventSource** object has these properties.</span></span>



| <span data-ttu-id="0f68c-120">Propriété</span><span class="sxs-lookup"><span data-stu-id="0f68c-120">Property</span></span>                                                    | <span data-ttu-id="0f68c-121">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="0f68c-121">Access type</span></span>          | <span data-ttu-id="0f68c-122">Description</span><span class="sxs-lookup"><span data-stu-id="0f68c-122">Description</span></span>                                              |
|:------------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [<span data-ttu-id="0f68c-123">**Sécurité\_**</span><span class="sxs-lookup"><span data-stu-id="0f68c-123">**Security\_**</span></span>](swbemeventsource-security-.md)<br/> | <span data-ttu-id="0f68c-124">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0f68c-124">Read-only</span></span><br/> | <span data-ttu-id="0f68c-125">Utilisé pour lire ou modifier les paramètres de sécurité.</span><span class="sxs-lookup"><span data-stu-id="0f68c-125">Used to read or change the security settings.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="0f68c-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="0f68c-126">Examples</span></span>

<span data-ttu-id="0f68c-127">Ce script utilise les méthodes de la classe **SWbemEventSource** et de la classe [**SWbemServices**](swbemservices.md) conjointement avec une requête WQL pour les événements d’application.</span><span class="sxs-lookup"><span data-stu-id="0f68c-127">This script uses the methods of the **SWbemEventSource** class and the [**SWbemServices**](swbemservices.md) class in conjunction with a WQL query for application events.</span></span> <span data-ttu-id="0f68c-128">Pour plus d’informations sur les requêtes et notifications d’événements WMI, consultez [surveillance des événements](monitoring-events.md), [exécution d’un script basé sur un événement](running-a-script-based-on-an-event.md)et [réception de notifications d’événements asynchrones](receiving-asynchronous-event-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="0f68c-128">For more information about WMI event notification and queries see [Monitoring Events](monitoring-events.md), [Running a Script Based on an Event](running-a-script-based-on-an-event.md), and [Receiving Asynchronous Event Notifications](receiving-asynchronous-event-notifications.md).</span></span>


```VB
' Connect to WMI, obtaining an SWbemServices object
set svc = _
CreateObject("Wbemscripting.SWbemLocator")._
   ConnectServer(,"root\cimv2")

' Obtain an SWbemEventSource object from the 
' SWbemServices.ExecNotificationQuery method to specify the 
' event source as "Application" events in a Win32_NTLogEvent
set evtsrc = svc.ExecNotificationQuery("SELECT * " _
   & "FROM __InstanceCreationEvent " _
   & "WHERE TargetInstance ISA 'Win32_NTLogEvent'" _
   & "AND TargetInstance.Logfile ='Application'")

' Wait for an event by executing the NextEvent method on the 
' SWbemEventSource object.
while (num < 5)
    set inst = evtsrc.NextEvent(-1)
    Wscript.echo inst.TargetInstance.Logfile
    num = num + 1
wend
```



## <a name="requirements"></a><span data-ttu-id="0f68c-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f68c-129">Requirements</span></span>



| <span data-ttu-id="0f68c-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f68c-130">Requirement</span></span> | <span data-ttu-id="0f68c-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f68c-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f68c-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f68c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="0f68c-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0f68c-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0f68c-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f68c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="0f68c-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0f68c-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0f68c-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="0f68c-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f68c-137"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f68c-137"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0f68c-138">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="0f68c-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="0f68c-139"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0f68c-139"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0f68c-140">DLL</span><span class="sxs-lookup"><span data-stu-id="0f68c-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f68c-141"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f68c-141"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0f68c-142">CLSID</span><span class="sxs-lookup"><span data-stu-id="0f68c-142">CLSID</span></span><br/>                    | <span data-ttu-id="0f68c-143">CLSID \_ SWbemEventSource</span><span class="sxs-lookup"><span data-stu-id="0f68c-143">CLSID\_SWbemEventSource</span></span><br/>                                                      |
| <span data-ttu-id="0f68c-144">IID</span><span class="sxs-lookup"><span data-stu-id="0f68c-144">IID</span></span><br/>                      | <span data-ttu-id="0f68c-145">IID \_ ISWbemEventSource</span><span class="sxs-lookup"><span data-stu-id="0f68c-145">IID\_ISWbemEventSource</span></span><br/>                                                       |



## <a name="see-also"></a><span data-ttu-id="0f68c-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f68c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f68c-147">Scripts d’objets d’API</span><span class="sxs-lookup"><span data-stu-id="0f68c-147">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

