---
description: WMI contient une infrastructure d’événements qui produit des notifications sur les modifications apportées aux données et services WMI. Les classes d’événements WMI fournissent une notification lorsque des événements spécifiques se produisent.
ms.assetid: 347808a7-0f7b-4687-93f4-bea55c96795a
ms.tgt_platform: multiple
title: Réception d’un événement WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 255f54f78bb64659d1cd07eddb72eae55b0263c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114899"
---
# <a name="receiving-a-wmi-event"></a>Réception d’un événement WMI

WMI contient une infrastructure d’événements qui produit des notifications sur les modifications apportées aux données et services WMI. Les [*classes d’événements*](gloss-e.md) WMI fournissent une notification lorsque des événements spécifiques se produisent.

Les sections suivantes sont présentées dans cette rubrique :

-   [Requêtes d’événements](#event-queries)
-   [Exemple](#example)
-   [Consommateurs d’événements](#event-consumers)
-   [Fournir des événements](#providing-events)
-   [Quotas d’abonnement](#subscription-quotas)
-   [Rubriques connexes](#related-topics)

## <a name="event-queries"></a>Requêtes d’événements

Vous pouvez créer une requête [semi-synchrone](receiving-synchronous-and-semisynchronous-event-notifications.md) ou [**asynchrone**](receiving-asynchronous-event-notifications.md) pour surveiller les modifications apportées aux journaux des événements, à la création du processus, à l’état du service, à la disponibilité de l’ordinateur ou à l’espace disque disponible, ainsi qu’à d’autres entités ou événements Dans les scripts, la méthode [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) est utilisée pour s’abonner à des événements. En C++, [**IWbemServices :: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) est utilisé. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

La notification d’une modification dans le modèle de données WMI standard est appelée [*événement intrinsèque*](gloss-i.md). [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) ou [**\_ \_ NamespaceDeletionEvent**](--namespacedeletionevent.md) sont des exemples d’événements intrinsèques. La notification d’une modification apportée par un fournisseur pour définir un événement de fournisseur est appelée [*événement extrinsèque*](gloss-e.md). Par exemple, le fournisseur de [Registre système](/previous-versions/windows/desktop/regprov/system-registry-provider), le fournisseur [d’événements de gestion](/windows/desktop/CIMWin32Prov/power-management-event-provider)de l’alimentation et le [fournisseur Win32](/windows/desktop/CIMWin32Prov/win32-provider) définissent leurs propres événements. Pour plus d’informations, consultez [détermination du type d’événement à recevoir](determining-the-type-of-event-to-receive.md).

## <a name="example"></a>Exemple

L’exemple de code de script suivant est une requête pour le [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) intrinsèque de la classe d’événements [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent). Vous pouvez exécuter ce programme en arrière-plan et, lorsqu’un événement survient, un message s’affiche. Si vous fermez la boîte de dialogue en **attente d’événements** , le programme cesse d’attendre les événements. N’oubliez pas que le **droit SeSecurityPrivilege** doit être activé.


```VB
Sub SINK_OnObjectReady(objObject, objAsyncContext)
    WScript.Echo (objObject.TargetInstance.Message)
End Sub

Set objWMIServices = GetObject( _
    "WinMgmts:{impersonationLevel=impersonate, (security)}") 

' Create the event sink object that receives the events
Set sink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
 
' Set up the event selection. SINK_OnObjectReady is called when
' a Win32_NTLogEvent event occurs
objWMIServices.ExecNotificationQueryAsync sink,"SELECT * FROM __InstanceCreationEvent " & "WHERE TargetInstance ISA 'Win32_NTLogEvent' "

WScript.Echo "Waiting for events"
```


```PowerShell

# Define event Query
$query = "SELECT * FROM __InstanceCreationEvent 
          WHERE TargetInstance ISA 'Win32_NTLogEvent' "

<# Register for event - also specify an action that
displays the log event when the event fires.#>

Register-WmiEvent -Source Demo1 -Query $query -Action {
                Write-Host "Log Event occured"
                $global:myevent = $event
                Write-Host "EVENT MESSAGE"
                Write-Host $event.SourceEventArgs.NewEvent.TargetInstance.Message}
<# So wait #>
"Waiting for events"
```





L’exemple de code VBScript suivant montre l’événement extrinsèque défini par le [ \_ \_ fournisseur de Registre](registering-for-system-registry-events.md) . Le script crée un consommateur temporaire en utilisant l’appel à [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md)et reçoit uniquement les événements lorsque le script est en cours d’exécution. Le script suivant s’exécute indéfiniment jusqu’à ce que l’ordinateur soit redémarré, que WMI soit arrêté ou que le script soit arrêté. Pour arrêter le script manuellement, utilisez le gestionnaire des tâches pour arrêter le processus. Pour l’arrêter par programmation, utilisez la méthode [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) dans la classe de \_ processus Win32. Pour plus d’informations, consultez [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md).


```VB
strComputer = "."

Set objWMIServices=GetObject( _
    "winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\default")

set objSink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")


objWMIServices.ExecNotificationQueryAsync objSink, _
    "Select * from RegistryValueChangeEvent Where Hive = 'HKEY_LOCAL_MACHINE' and KeyPath = 'SYSTEM\\ControlSet001\\Control' and ValueName = 'CurrentUser'"

WScript.Echo "Waiting for events..."

While (True) 
     WScript.Sleep (1000)
Wend

 
WScript.Echo "Listening for Registry Change Events..." & vbCrLf 

While(True) 
    WScript.Sleep 1000 
Wend 

Sub SINK_OnObjectReady(wmiObject, wmiAsyncContext) 
    WScript.Echo "Received Registry Value Change Event" & vbCrLf & wmiObject.GetObjectText_() 
End Sub
```



## <a name="event-consumers"></a>Consommateurs d'événements

Vous pouvez surveiller ou consommer des événements à l’aide des consommateurs suivants lorsqu’un script ou une application est en cours d’exécution :

-   Consommateurs d’événements temporaires

    Un [*consommateur temporaire*](gloss-t.md) est une application cliente WMI qui reçoit un événement WMI. WMI comprend une interface unique qui permet de spécifier les événements que WMI doit envoyer à une application cliente. Un consommateur d’événements temporaire est considéré comme temporaire, car il fonctionne uniquement lorsqu’il est spécifiquement chargé par un utilisateur. Pour plus d’informations, consultez [réception d’événements pendant la durée de votre application](receiving-events-for-the-duration-of-your-application.md).

-   Consommateurs d’événements permanents

    Un [*consommateur permanent*](gloss-p.md) est un objet com qui peut recevoir à tout moment un événement WMI. Un consommateur d’événements permanent utilise un ensemble d’objets et de filtres persistants pour capturer un événement WMI. À l’instar d’un consommateur d’événements temporaire, vous configurez une série d’objets WMI et de filtres qui capturent un événement WMI. Lorsqu’un événement qui correspond à un filtre est exécuté, WMI charge le consommateur d’événements permanent et le notifie à l’événement. Étant donné qu’un consommateur permanent est implémenté dans l’espace de stockage WMI et qu’il s’agit d’un fichier exécutable enregistré dans WMI, le consommateur d’événements permanent opère et reçoit des événements après sa création et même après un redémarrage du système d’exploitation tant que WMI est en cours d’exécution. Pour plus d’informations, consultez [réception d’événements à tout moment](receiving-events-at-all-times.md).

Les scripts ou les applications qui reçoivent des événements ont des considérations spéciales en matière de sécurité. Pour plus d’informations, consultez [sécurisation des événements WMI](securing-wmi-events.md).

Une application ou un script peut utiliser un fournisseur d’événements WMI intégré qui fournit des [classes de consommateur standard](standard-consumer-classes.md). Chaque classe de consommateur standard répond à un événement avec une action différente en envoyant un message électronique ou en exécutant un script. Vous n’avez pas besoin d’écrire du code fournisseur pour utiliser une classe de consommateur standard pour créer un consommateur d’événements permanent. Pour plus d’informations, consultez [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).

## <a name="providing-events"></a>Fournir des événements

Un fournisseur d’événements est un composant COM qui envoie un événement à WMI. Vous pouvez créer un fournisseur d’événements pour envoyer un événement dans une application C++ ou C#. La plupart des fournisseurs d’événements gèrent un objet pour WMI, par exemple, une application ou un élément matériel. Pour plus d’informations, consultez [écriture d’un fournisseur d’événements](writing-an-event-provider.md).

Un événement chronométré ou répété est un événement qui se produit à une heure prédéterminée.

WMI offre les moyens suivants de créer des événements chronométrés ou répétitifs pour vos applications :

-   L’infrastructure d’événements Microsoft standard.
-   Classe de minuteur spécialisée.

Pour plus d’informations, consultez [réception d’un événement chronométré ou répétitif](receiving-a-timed-or-repeating-event.md). Lorsque vous écrivez un fournisseur d’événements, tenez compte des informations de sécurité identifiées dans [fourniture sécurisée des événements](providing-events-securely.md).

Il est recommandé de compiler les abonnements d’événements permanents dans l’espace de noms de l' \\ \\ abonnement racine. Pour plus d’informations, consultez [Implementing Cross-namespace permanent Event subscriptions](implementing-cross-namespace-permanent-event-subscriptions.md).

## <a name="subscription-quotas"></a>Quotas d’abonnement

L’interrogation des événements peut nuire aux performances des fournisseurs qui prennent en charge les requêtes sur des jeux de données volumineux. En outre, tout utilisateur disposant d’un accès en lecture à un espace de noms avec des fournisseurs dynamiques peut effectuer une attaque par déni de service (DoS). WMI gère les quotas pour tous les utilisateurs combinés et pour chaque consommateur d’événements dans l’instance unique de [**\_ \_ ArbitratorConfiguration**](--arbitratorconfiguration.md) située dans l' \\ espace de noms racine. Ces quotas sont globaux plutôt que pour chaque espace de noms. Vous ne pouvez pas modifier les quotas.

WMI applique actuellement des quotas à l’aide des propriétés de [**\_ \_ ArbitratorConfiguration**](--arbitratorconfiguration.md). Chaque quota a un par utilisateur et une version totale qui inclut tous les utilisateurs combinés, et non par espace de noms. Le tableau suivant répertorie les quotas qui s’appliquent aux propriétés **\_ \_ ArbitratorConfiguration** .



| Total/PerUser                                                                   | Quota                                                                       |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| TemporarySubscriptionsTotal<br/> TemporarySubscriptionsPerUser<br/> | 10 000<br/> 1 000<br/>                                          |
| PermanentSubscriptionsTotal<br/> PermanentSubscriptionsPerUser<br/> | 10 000<br/> 1 000<br/>                                          |
| PollingInstructionsTotal<br/> PollingInstructionsPerUser<br/>       | 10 000<br/> 1 000<br/>                                          |
| PollingMemoryTotal<br/> PollingMemoryPerUser<br/>                   | 10 millions (0x989680) octets<br/> 5 millions (0x4CB40) octets<br/> |



 

Un administrateur ou un utilisateur disposant d’une autorisation en **\_ écriture totale** dans l’espace de noms peut modifier l’instance singleton de [**\_ \_ ArbitratorConfiguration**](--arbitratorconfiguration.md). WMI effectue le suivi du quota par utilisateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de WMI](using-wmi.md)
</dt> </dl>

 

