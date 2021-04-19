---
description: La notification d’événements asynchrone est une technique qui permet à une application de surveiller en permanence les événements sans monopoliser les ressources système.
ms.assetid: 69ec8ead-9073-4689-bc66-5134728ab147
ms.tgt_platform: multiple
title: Réception des notifications d’événements asynchrones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d883908475c796a6bcf31895f2928345541c940
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522086"
---
# <a name="receiving-asynchronous-event-notifications"></a>Réception des notifications d’événements asynchrones

La notification d’événements asynchrone est une technique qui permet à une application de surveiller en permanence les événements sans monopoliser les ressources système. Les notifications d’événements asynchrones ont les mêmes restrictions de sécurité que les autres appels asynchrones. Vous pouvez effectuer des appels semi-synchrones à la place. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

La file d’attente des événements asynchrones routés vers un client a le potentiel de croître de manière exceptionnellement importante. Par conséquent, WMI implémente une stratégie à l’ensemble du système pour éviter de manquer de mémoire. WMI ralentit les événements ou commence à supprimer des événements de la file d’attente lorsque la file d’attente dépasse une certaine taille.

WMI utilise les propriétés [**LowThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) et [**HighThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) de la classe [**Win32 \_ WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) pour définir des limites en cas d’évitement de mémoire. La valeur minimale indique que WMI doit commencer à ralentir la notification d’événements, et la valeur maximale indique quand commencer à supprimer des événements. Les valeurs par défaut pour les seuils inférieur et supérieur sont 1 million (10 Mo) et 2 millions (20 Mo). En outre, vous pouvez définir la propriété [**MaxWaitOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) pour décrire la durée d’attente de WMI avant de supprimer des événements. La valeur par défaut de **MaxWaitOnEvents** est 2000, ou 2 secondes.

## <a name="receiving-asynchronous-event-notifications-in-vbscript"></a>Réception de notifications d’événements asynchrones dans VBScript

Les appels de script pour recevoir des notifications d’événements sont essentiellement les mêmes que tous les appels asynchrones ayant les mêmes problèmes de sécurité. Pour plus d’informations, consultez [création d’un appel asynchrone avec VBScript](making-an-asynchronous-call-with-vbscript.md).

**Pour recevoir des notifications d’événements asynchrones dans VBScript**

1.  Créez un objet récepteur en appelant [Wscript. CreateObject](/previous-versions//xzysf6hc(v=vs.85)) et en spécifiant le ProgID de « WbemScripting » et le type d’objet [**SWbemSink**](swbemsink.md). L’objet récepteur reçoit les notifications.
2.  Écrivez une sous-routine pour chaque événement que vous souhaitez gérer. Le tableau suivant répertorie les événements [**SWbemSink**](swbemsink.md) .

    

    | Événement                                            | Signification                                                                                                                         |
    |--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
    | [**OnObjectReady**](swbemsink-onobjectready.md) | Signale le retour d’un objet au récepteur. L’utilisation de cet appel retourne un objet chaque fois que l’opération est terminée.     |
    | [**OnCompleted**](swbemsink-oncompleted.md)     | Signale quand un appel asynchrone est terminé. Cet événement ne se produit jamais si l’opération est indéfinie.                          |
    | [**OnObjectPut**](swbemsink-onobjectput.md)     | Signale l’achèvement d’une opération put asynchrone. Cet événement retourne le chemin d’accès de l’objet de l’instance ou de la classe enregistrée. |
    | [**OnProgress**](swbemsink-onprogress.md)       | Signale l’état d’un appel asynchrone en cours. Tous les fournisseurs ne prennent pas en charge les rapports de progression temporaires.             |
    | [**Annuler**](swbemsink-cancel.md)               | Annule toutes les opérations asynchrones en suspens associées à ce récepteur d’objets.                                        |

    

     

L’exemple de code VBScript suivant indique la suppression des processus avec un intervalle d’interrogation de 10 secondes. Dans ce script, le récepteur de sous-routine \_ OnObjectReady gère l’occurrence de l’événement. Dans l’exemple, l’objet récepteur est nommé « sink », mais vous pouvez nommer cet objet comme vous le souhaitez.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set MySink = WScript.CreateObject( _
    "WbemScripting.SWbemSink","SINK_")

objWMIservice.ExecNotificationQueryAsync MySink, _
    "SELECT * FROM __InstanceDeletionEvent" _
    & " WITHIN 10 WHERE TargetInstance ISA 'Win32_Process'"


WScript.Echo "Waiting for events..."

While (True)
    Wscript.Sleep(1000)
Wend

Sub SINK_OnObjectReady(objObject, objAsyncContext)
    Wscript.Echo "__InstanceDeletionEvent event has occurred."
End Sub

Sub SINK_OnCompleted(objObject, objAsyncContext)
    WScript.Echo "Event call complete."
End Sub
```



## <a name="receiving-asynchronous-event-notifications-in-c"></a>Réception de notifications d’événements asynchrones en C++

Pour exécuter une notification asynchrone, vous créez un thread distinct uniquement pour surveiller et recevoir des événements à partir d’Windows Management Instrumentation (WMI). Lorsque ce thread reçoit un message, le thread notifie votre application principale.

En dédiant un thread distinct, vous autorisez votre processus principal à exécuter d’autres activités en attendant l’arrivée d’un événement. La remise asynchrone des notifications améliore les performances, mais peut fournir moins de sécurité que vous ne le souhaitez. En C++, vous avez la possibilité d’utiliser l’interface [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) ou d’effectuer des vérifications d’accès sur les descripteurs de sécurité. Pour plus d’informations, consultez [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md).

**Pour configurer des notifications d’événements asynchrones**

1.  Avant d’initialiser des notifications asynchrones, assurez-vous que vos paramètres d’évitement de mémoire sont correctement définis dans [**Win32 \_ WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting).

2.  Déterminez le type d’événement que vous souhaitez recevoir.

    WMI prend en charge les événements intrinsèques et extrinsèques. Un événement intrinsèque est un événement prédéfini par WMI, alors qu’un événement extrinsèque est un événement défini par un fournisseur tiers. Pour plus d’informations, consultez [détermination du type d’événement à recevoir](determining-the-type-of-event-to-receive.md).

La procédure suivante décrit comment recevoir des notifications d’événements asynchrones en C++.

**Pour recevoir des notifications d’événements asynchrones en C++**

1.  Configurez votre application avec des appels aux fonctions [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) et [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .

    L’appel de [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) Initialise com, tandis que [**COINITIALIZESECURITY**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) accorde à WMI l’autorisation d’appeler le processus du consommateur. La fonction **CoInitializeEx** vous donne également la possibilité de programmer une application multithread, ce qui est nécessaire pour la notification asynchrone. Pour plus d’informations, consultez [maintenance de la sécurité WMI](maintaining-wmi-security.md).

    Le code de cette rubrique requiert les références suivantes et les \# instructions include pour être compilées correctement.

    ```C++
    #define _WIN32_DCOM
    #include <iostream>
    using namespace std;
    #include <wbemidl.h>
    ```

    

    L’exemple de code suivant décrit comment configurer le consommateur d’événements temporaires avec des appels à [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) et [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).

    ```C++
    void main(int argc, char **argv)
    {
        HRESULT hr = 0;
        hr = CoInitializeEx (0, COINIT_MULTITHREADED);
        hr = CoInitializeSecurity (NULL, 
           -1, 
           NULL, 
           NULL,   
           RPC_C_AUTHN_LEVEL_NONE, 
           RPC_C_IMP_LEVEL_IMPERSONATE, 
           NULL,
           EOAC_NONE,
           NULL); 

        if (FAILED(hr))
        {
           CoUninitialize();
           cout << "Failed to initialize security. Error code = 0x"
               << hex << hr << endl;
           return;
        }

    // ...
    }
    ```

    

2.  Créez un objet récepteur par le biais de l’interface [**IWbemObjectSink**](iwbemobjectsink.md) .

    WMI utilise [**IWbemObjectSink**](iwbemobjectsink.md) pour envoyer des notifications d’événements et signaler l’état d’une opération asynchrone ou d’une notification d’événement.

3.  Inscrivez votre consommateur d’événements à l’aide d’un appel à la méthode [**IWbemServices :: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) .

    Assurez-vous que le paramètre *pResponseHandler* pointe vers l’objet récepteur créé à l’étape précédente.

    L’objectif de l’inscription est de recevoir uniquement les notifications requises. La réception de notifications superflues gaspille le traitement et la remise du temps ; et n’utilise pas la fonctionnalité de filtrage de WMI pour obtenir le potentiel le plus complet possible.

    Toutefois, un consommateur temporaire peut recevoir plus d’un type d’événement. Dans ce cas, un consommateur temporaire doit effectuer des appels distincts à [**IWbemServices :: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) pour chaque type d’événement. Par exemple, un consommateur peut nécessiter une notification lorsque de nouveaux processus sont créés (un événement de création d’instance ou [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)) et des modifications à certaines clés de Registre (un événement de registre tel que [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)). Par conséquent, le consommateur effectue un appel à [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) pour s’inscrire aux événements de création d’instance et un autre appel à **ExecNotificationQueryAsync** pour s’inscrire aux événements de registre.

    Si vous choisissez de créer un consommateur d’événements qui s’inscrit pour plusieurs événements, vous devez éviter d’inscrire plusieurs classes avec le même récepteur. Utilisez plutôt un récepteur distinct pour chaque classe d’événements inscrits. Le fait de disposer d’un récepteur dédié simplifie le traitement et les aides en maintenance, ce qui vous permet d’annuler une inscription sans affecter les autres.

4.  Effectuez les activités nécessaires dans votre consommateur d’événements.

    Cette étape doit contenir la majeure partie de votre code et inclure des activités telles que l’affichage des événements dans une interface utilisateur.

5.  Lorsque vous avez terminé, annulez l’inscription du consommateur d’événements temporaires avec un appel à l’événement [**IWbemServices :: CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) .

    Que l’appel à [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) réussisse ou échoue, ne supprimez pas l’objet récepteur tant que le nombre de références d’objet n’atteint pas zéro. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

 

 
