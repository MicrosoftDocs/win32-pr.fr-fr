---
description: L’objet SWbemSink est implémenté par les applications clientes pour recevoir les résultats des opérations asynchrones et des notifications d’événements.
ms.assetid: a90777ef-fa26-4bfb-b196-c083a0c92a29
ms.tgt_platform: multiple
title: Objet SWbemSink (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink
- ISWbemSinkEvents
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3f7b2c499716bb8da3d2cc9a7db5dd06a2341c5d75876468f5e81853a8120944
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071459"
---
# <a name="swbemsink-object"></a>Objet SWbemSink

L’objet **SWbemSink** est implémenté par les applications clientes pour recevoir les résultats des opérations asynchrones et des notifications d’événements. Pour effectuer un appel asynchrone, vous devez créer une instance d’un objet **SWbemSink** et la passer en tant que paramètre *ObjWbemSink* . Les événements de votre implémentation de **SWbemSink** sont déclenchés lorsque l’État ou les résultats sont retournés, ou lorsque l’appel est terminé. L’appel de VBScript **CreateObject** crée cet objet.

## <a name="members"></a>Membres

L’objet **SWbemSink** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’objet **SWbemSink** a ces méthodes.



| Méthode                             | Description                                                                        |
|:-----------------------------------|:-----------------------------------------------------------------------------------|
| [**Annuler**](swbemsink-cancel.md) | Annule toutes les opérations asynchrones associées à ce récepteur.<br/> |



 

## <a name="remarks"></a>Remarques

Un rappel asynchrone permet à un utilisateur non authentifié de fournir des données au récepteur. Cela pose des risques de sécurité pour vos scripts et vos applications. Pour éliminer les risques, utilisez une communication semi-synchrone ou une communication synchrone. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

### <a name="events"></a>Événements

Vous pouvez implémenter des sous-routines à appeler lorsque des événements sont déclenchés. Par exemple, si vous souhaitez traiter chaque objet retourné par un appel de requête asynchrone comme [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md), créez une sous-routine à l’aide du récepteur qui est spécifié dans l’appel asynchrone, comme indiqué dans l’exemple suivant.


```VB
Sub SinkName_OnObjectReady(objObject, objAsyncContext)
```



Utilisez le tableau suivant comme référence pour identifier les événements et les descriptions des déclencheurs.



| Événement                                            | Description                                                             |
|--------------------------------------------------|-------------------------------------------------------------------------|
| [**OnCompleted**](swbemsink-oncompleted.md)     | Déclenché lorsqu’une opération asynchrone est terminée.                   |
| [**OnObjectPut**](swbemsink-onobjectput.md)     | Déclenché lorsqu’une opération put asynchrone est terminée.               |
| [**OnObjectReady**](swbemsink-onobjectready.md) | Déclenché lorsqu’un objet fourni par un appel asynchrone est disponible. |
| [**OnProgress**](swbemsink-onprogress.md)       | Déclenché pour fournir l’état d’une opération asynchrone.            |



 

**Récupération asynchrone des statistiques des journaux des événements**

WMI prend en charge les scripts asynchrones et semi-synchrones. Lors de la récupération d’événements à partir des journaux des événements, les scripts asynchrones récupèrent souvent ces données beaucoup plus rapidement.

Dans un script asynchrone, une requête est émise et le contrôle est immédiatement retourné au script. La requête continue à traiter sur un thread distinct, tandis que le script commence immédiatement à agir sur les informations retournées. Les scripts asynchrones sont pilotés par les événements : chaque fois qu’un enregistrement d’événement est récupéré, l’événement OnObjectReady est déclenché. Une fois la requête terminée, l’événement OnCompleted se déclenche et le script peut continuer en fonction du fait que tous les enregistrements disponibles ont été retournés.

En revanche, dans un script semi-synchrone, une requête est émise et le script met en file d’attente une grande quantité d’informations extraites avant d’agir dessus. Pour de nombreux objets, le traitement semi-synchrone est approprié ; par exemple, lors de l’interrogation d’un lecteur de disque pour ses propriétés, il peut y avoir uniquement une seconde fractionnée entre le moment où la requête est émise et le moment où les informations sont retournées et exploitées. Cela est dû en grande partie au fait que la quantité d’informations renvoyées est relativement faible.

Toutefois, lors de l’interrogation d’un journal des événements, l’intervalle entre le moment où la requête est émise et le moment où un script semi-synchrone peut se terminer et le retour des informations peut prendre des heures. En plus de cela, le script peut manquer de mémoire et échouer de manière autonome avant de terminer.

Pour les journaux des événements avec un grand nombre d’enregistrements, la différence de temps de traitement peut être considérable. sur un ordinateur de test Windows 2000 avec 2 000 enregistrements dans le journal des événements, une requête semi-synchrone qui a récupéré tous les événements et les a affichés dans une fenêtre de commande a duré 10 minutes 45 secondes. Une requête asynchrone qui a effectué la même opération a duré une minute de 54 secondes.

## <a name="examples"></a>Exemples

Le code VBScript suivant interroge de manière asynchrone les journaux des événements pour tous les enregistrements.


```VB
Const POPUP_DURATION = 10
Const OK_BUTTON = 0
Set objWSHShell = Wscript.CreateObject("Wscript.Shell")
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objSink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
objWMIService.InstancesOfAsync objSink, "Win32_NTLogEvent"
errReturn = objWshShell.Popup("Retrieving events", POPUP_DURATION, _
"Event Retrieval", OK_BUTTON)
Sub SINK_OnCompleted(iHResult, objErrorObject, objAsyncContext)
 WScript.Echo "Asynchronous operation is done."
End Sub
Sub SINK_OnObjectReady(objEvent, objAsyncContext)
 Wscript.Echo "Category: " & objEvent.Category
 Wscript.Echo "Computer Name: " & objEvent.ComputerName
 Wscript.Echo "Event Code: " & objEvent.EventCode
 Wscript.Echo "Message: " & objEvent.Message
 Wscript.Echo "Record Number: " & objEvent.RecordNumber
 Wscript.Echo "Source Name: " & objEvent.SourceName
 Wscript.Echo "Time Written: " & objEvent.TimeWritten
 Wscript.Echo "Event Type: " & objEvent.Type
 Wscript.Echo "User: " & objEvent.User
End Sub
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Wbemdisp. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemSink<br/> CLSID \_ SWbemSinkEvents<br/>                           |
| IID<br/>                      | IID \_ ISWbemSink<br/> IID \_ ISWbemSinkEvents<br/>                             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Scripts d’objets d’API](scripting-api-objects.md)
</dt> </dl>

 

 




