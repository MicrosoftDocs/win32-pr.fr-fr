---
description: WMI mappe automatiquement les interruptions SNMP aux événements WMI. Le système place les données contenues dans l’interruption dans les propriétés correspondantes d’une instance d’événement WMI pour l’accès par l’ordinateur hôte WMI.
ms.assetid: 549f58a9-9d3b-41b9-a374-ab83877f63a7
ms.tgt_platform: multiple
title: Réception d’interruptions SNMP en tant qu’événements WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da24be8ea9a4882af0b961b1d0f6f0c3d442c70c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528509"
---
# <a name="receiving-snmp-traps-as-wmi-events"></a><span data-ttu-id="0ba78-104">Réception d’interruptions SNMP en tant qu’événements WMI</span><span class="sxs-lookup"><span data-stu-id="0ba78-104">Receiving SNMP Traps as WMI Events</span></span>

<span data-ttu-id="0ba78-105">WMI mappe automatiquement les interruptions SNMP aux événements WMI.</span><span class="sxs-lookup"><span data-stu-id="0ba78-105">WMI automatically maps SNMP traps to WMI events.</span></span> <span data-ttu-id="0ba78-106">Le système place les données contenues dans l’interruption dans les propriétés correspondantes d’une instance d’événement WMI pour l’accès par l’ordinateur hôte WMI.</span><span class="sxs-lookup"><span data-stu-id="0ba78-106">The system places the data contained in the trap in the corresponding properties of a WMI event instance for access by the WMI host machine.</span></span>

> [!Note]  
> <span data-ttu-id="0ba78-107">Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="0ba78-107">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="0ba78-108">La réception d’une interruption SNMP est quasiment identique à la réception d’événements de tout autre fournisseur WMI.</span><span class="sxs-lookup"><span data-stu-id="0ba78-108">Receiving an SNMP trap is nearly identical to receiving events from any other WMI provider.</span></span> <span data-ttu-id="0ba78-109">Toutefois, le filtre d’événement SNMP a plusieurs classes uniques à connaître avant d’inscrire les événements.</span><span class="sxs-lookup"><span data-stu-id="0ba78-109">However, the SNMP event filter has several unique classes to be aware of before registering for events.</span></span> <span data-ttu-id="0ba78-110">En outre, le fournisseur d’événements requiert uniquement l’utilisation de l' \\ espace de noms stockage SMIR.</span><span class="sxs-lookup"><span data-stu-id="0ba78-110">Also, the event provider requires the use of the \\smir namespace exclusively.</span></span>

<span data-ttu-id="0ba78-111">Les classes les plus courantes à inscrire sont [SnmpNotification](snmpnotification.md) et [SnmpExtendedNotification](snmpextendednotification.md).</span><span class="sxs-lookup"><span data-stu-id="0ba78-111">The most common classes to register with are [SnmpNotification](snmpnotification.md) and [SnmpExtendedNotification](snmpextendednotification.md).</span></span> <span data-ttu-id="0ba78-112">Les consommateurs ont l’intention d’utiliser les notifications d’événements pour mettre à jour les valeurs des appareils SNMP surveillés doivent s’inscrire aux événements SnmpExtendedNotification.</span><span class="sxs-lookup"><span data-stu-id="0ba78-112">Consumers intent on using event notifications to update values in monitored SNMP devices must register for SnmpExtendedNotification events.</span></span> <span data-ttu-id="0ba78-113">Les informations des événements SnmpNotification ne sont pas réutilisables.</span><span class="sxs-lookup"><span data-stu-id="0ba78-113">The information from SnmpNotification events is not reusable.</span></span>

<span data-ttu-id="0ba78-114">Le tableau suivant répertorie des informations sur la configuration de votre ordinateur pour recevoir des interruptions SNMP en tant qu’événements WMI.</span><span class="sxs-lookup"><span data-stu-id="0ba78-114">The following table lists information about setting up your computer to receive SNMP traps as WMI events.</span></span>



| <span data-ttu-id="0ba78-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="0ba78-115">Task</span></span>                                                                               | <span data-ttu-id="0ba78-116">Description</span><span class="sxs-lookup"><span data-stu-id="0ba78-116">Description</span></span>                                                                        |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="0ba78-117">Choix entre des fournisseurs d’événements SNMP</span><span class="sxs-lookup"><span data-stu-id="0ba78-117">Choosing Between SNMP Event Providers</span></span>](choosing-between-snmp-event-providers.md) | <span data-ttu-id="0ba78-118">WMI comprend deux fournisseurs d’événements SNMP.</span><span class="sxs-lookup"><span data-stu-id="0ba78-118">WMI includes two SNMP event providers.</span></span>                                             |
| [<span data-ttu-id="0ba78-119">Réception d’événements SNMP</span><span class="sxs-lookup"><span data-stu-id="0ba78-119">Receiving SNMP Events</span></span>](receiving-snmp-events.md)                                 | <span data-ttu-id="0ba78-120">Les fournisseurs d’événements SNMP prennent en charge trois types d’interruptions SNMPv1 et de notifications SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="0ba78-120">SNMP event providers support three types of SNMPv1 traps and SNMPv2 notifications.</span></span> |



 

<span data-ttu-id="0ba78-121">L’exemple suivant configure un ordinateur pour surveiller l’événement **SnmpLinkUpNotification** à partir d’un concentrateur géré.</span><span class="sxs-lookup"><span data-stu-id="0ba78-121">The following example sets up a computer to monitor for the **SnmpLinkUpNotification** event from a managed hub.</span></span>


```VB
Set objLocator = CreateObject("wbemscripting.swbemlocator")
Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")

set objwbemEventsource = _ 
    objServices.ExecNotificationQuery _
   ("SELECT * FROM SnmpLinkUpNotification")

set objWbemObject = objwbemEventsource.NextEvent()

wscript.echo "Received " & objWbemObject.path_.class

for each prop in objWbemObject.properties_
    wscript.echo prop.name & " -- " & prop.value
next
```



 

 



