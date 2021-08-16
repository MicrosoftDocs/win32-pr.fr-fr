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
ms.openlocfilehash: e38dab258ebccacb24cf92b7445752102b297ab1207b99e40355c30fde99113d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992139"
---
# <a name="swbemeventsource-object"></a>Objet SWbemEventSource

L’objet **SWbemEventSource** récupère les événements d’une requête d’événement conjointement avec [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md). Vous recevez un objet **SWbemEventSource** si vous effectuez un appel à **SWbemServices.ExecNotificationQuery** pour effectuer une requête d’événement. Vous pouvez ensuite utiliser la méthode [**NextEvent**](swbemeventsource-nextevent.md) pour récupérer les événements à mesure qu’ils arrivent. Cet objet ne peut pas être créé par l’appel VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) .

## <a name="members"></a>Membres

L’objet **SWbemEventSource** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **SWbemEventSource** a ces méthodes.



| Méthode                                          | Description                                                                                                                                  |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**NextEvent**](swbemeventsource-nextevent.md) | Utilisé pour récupérer un événement conjointement à [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **SWbemEventSource** a ces propriétés.



| Propriété                                                    | Type d’accès          | Description                                              |
|:------------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [**Sécurité\_**](swbemeventsource-security-.md)<br/> | Lecture seule<br/> | Utilisé pour lire ou modifier les paramètres de sécurité.<br/> |



 

## <a name="examples"></a>Exemples

Ce script utilise les méthodes de la classe **SWbemEventSource** et de la classe [**SWbemServices**](swbemservices.md) conjointement avec une requête WQL pour les événements d’application. Pour plus d’informations sur les requêtes et notifications d’événements WMI, consultez [surveillance des événements](monitoring-events.md), [exécution d’un script basé sur un événement](running-a-script-based-on-an-event.md)et [réception de notifications d’événements asynchrones](receiving-asynchronous-event-notifications.md).


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



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemEventSource<br/>                                                      |
| IID<br/>                      | IID \_ ISWbemEventSource<br/>                                                       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Scripts d’objets d’API](scripting-api-objects.md)
</dt> </dl>

 

