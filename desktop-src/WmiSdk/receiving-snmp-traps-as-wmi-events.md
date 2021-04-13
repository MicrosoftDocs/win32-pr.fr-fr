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
# <a name="receiving-snmp-traps-as-wmi-events"></a>Réception d’interruptions SNMP en tant qu’événements WMI

WMI mappe automatiquement les interruptions SNMP aux événements WMI. Le système place les données contenues dans l’interruption dans les propriétés correspondantes d’une instance d’événement WMI pour l’accès par l’ordinateur hôte WMI.

> [!Note]  
> Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

La réception d’une interruption SNMP est quasiment identique à la réception d’événements de tout autre fournisseur WMI. Toutefois, le filtre d’événement SNMP a plusieurs classes uniques à connaître avant d’inscrire les événements. En outre, le fournisseur d’événements requiert uniquement l’utilisation de l' \\ espace de noms stockage SMIR.

Les classes les plus courantes à inscrire sont [SnmpNotification](snmpnotification.md) et [SnmpExtendedNotification](snmpextendednotification.md). Les consommateurs ont l’intention d’utiliser les notifications d’événements pour mettre à jour les valeurs des appareils SNMP surveillés doivent s’inscrire aux événements SnmpExtendedNotification. Les informations des événements SnmpNotification ne sont pas réutilisables.

Le tableau suivant répertorie des informations sur la configuration de votre ordinateur pour recevoir des interruptions SNMP en tant qu’événements WMI.



| Tâche                                                                               | Description                                                                        |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Choix entre des fournisseurs d’événements SNMP](choosing-between-snmp-event-providers.md) | WMI comprend deux fournisseurs d’événements SNMP.                                             |
| [Réception d’événements SNMP](receiving-snmp-events.md)                                 | Les fournisseurs d’événements SNMP prennent en charge trois types d’interruptions SNMPv1 et de notifications SNMPv2. |



 

L’exemple suivant configure un ordinateur pour surveiller l’événement **SnmpLinkUpNotification** à partir d’un concentrateur géré.


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



 

 



