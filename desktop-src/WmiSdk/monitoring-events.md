---
description: Les administrateurs système peuvent utiliser WMI pour surveiller les événements sur un réseau.
ms.assetid: 871d4add-a7b1-4ec9-a202-3821fdf09e9f
ms.tgt_platform: multiple
title: Surveillance des événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb90a0a6eef87f88543e8f2414bc38bdea4f7d89c577471d79d23393f331b053
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317113"
---
# <a name="monitoring-events"></a>Surveillance des événements

Les administrateurs système peuvent utiliser WMI pour surveiller les événements sur un réseau. Par exemple :

-   Un service s’arrête de manière inattendue.
-   Un serveur devient indisponible.
-   Un lecteur de disque remplit la capacité de 80%.
-   Les événements de sécurité sont signalés dans un journal des événements NT.

WMI prend en charge la détection et la remise d’événements aux consommateurs d’événements, car certains fournisseurs WMI sont des fournisseurs d’événements. Pour plus d’informations, consultez [réception d’un événement WMI](receiving-a-wmi-event.md).

Les [*consommateurs d’événements*](gloss-e.md) sont des applications ou des scripts qui demandent une notification d’événements, puis exécutent des tâches lorsque des événements spécifiques se produisent. Vous pouvez créer des scripts ou des applications de surveillance des événements qui surveillent temporairement le moment où les événements se produisent. WMI fournit également un ensemble de fournisseurs d’événements permanents préinstallés et les classes de consommateurs permanentes qui vous permettent de surveiller de façon permanente les événements. Pour plus d’informations, consultez [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).

Les sections suivantes sont présentées dans cette rubrique :

-   [Utilisation des consommateurs d’événements temporaires](#using-temporary-event-consumers)
-   [Utilisation des consommateurs d’événements permanents](#using-permanent-event-consumers)

## <a name="using-temporary-event-consumers"></a>Utilisation des consommateurs d’événements temporaires

Les consommateurs d’événements temporaires sont des scripts ou des applications qui retournent les événements qui correspondent à une requête d’événement ou à un filtre. Les requêtes d’événements temporaires utilisent généralement [**IWbemServices :: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) dans les applications C++ ou [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) dans des scripts et des Visual Basic.

Une requête d’événement demande des instances d’une classe d’événements qui spécifient un certain type d’événement, tel que [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) ou [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).

L’exemple de code VBScript suivant demande une notification lorsqu’une instance de [**\_ ProcessTrace Win32**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) est créée. Une instance de cette classe est générée lorsqu’un processus est démarré ou arrêté.

Pour exécuter le script, copiez-le dans un fichier nommé event.vbs et utilisez la ligne de commande suivante : **cscript event.vbs**. Vous pouvez voir la sortie du script en démarrant Notepad.exe ou tout autre processus. Le script s’arrête après le démarrage ou l’arrêt de cinq processus.

Ce script appelle [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md), qui est la version [*semi-synchrone*](gloss-s.md) de la méthode. Consultez le script suivant pour obtenir un exemple de configuration d’un abonnement d’événement temporaire asynchrone en appelant [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md). Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md). Le script appelle [**SWbemEventSource. NextEvent**](swbemeventsource-nextevent.md) pour obtenir et traiter chaque événement au fur et à mesure de son arrivée. Enregistrez le script dans un fichier avec une extension. vbs et exécutez le script sur une ligne de commande à l’aide de CScript : **cscript file.vbs**.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" _
    & strComputer & "\root\CIMV2") 
Set objEvents = objWMIService.ExecNotificationQuery _
    ("SELECT * FROM Win32_ProcessTrace")

Wscript.Echo "Waiting for events ..."
i = 0
Do Until i=5
    Set objReceivedEvent = objEvents.NextEvent
    'report an event
    Wscript.Echo "Win32_ProcessTrace event occurred" & VBNewLine _
        & "Process Name = " _
            & objReceivedEvent.ProcessName & VBNewLine _
        & "Process ID = " _
            & objReceivedEvent.Processid & VBNewLine _
        & "Session ID = " & objReceivedEvent.SessionID 
i = i+ 1
Loop
```



Les consommateurs d’événements temporaires doivent être démarrés manuellement et ne doivent pas être conservés à travers les redémarrages WMI ou les redémarrages du système d’exploitation. Un consommateur d’événements temporaire peut traiter les événements uniquement lorsqu’il est en cours d’exécution.

La procédure suivante décrit comment créer un consommateur d’événements temporaire.

**Pour créer un consommateur d’événements temporaire**

1.  Choisissez le langage de programmation à utiliser.

    Le langage de programmation détermine l’API à utiliser.

    -   Pour le langage de programmation C++, utilisez l' [API com pour WMI](com-api-for-wmi.md).
    -   pour les Visual Basic ou les langages de script, utilisez l' [API de script pour WMI](scripting-api-for-wmi.md).

2.  Commencez le codage d’une application de consommateur d’événements temporaire de la même façon que vous démarrez une application WMI.

    Les premières étapes du codage dépendent du langage de programmation. En règle générale, vous vous connectez à WMI et configurez les paramètres de sécurité. Pour plus d’informations, consultez [création d’une application ou d’un script WMI](creating-a-wmi-application-or-script.md).

3.  Définissez la requête d’événement que vous souhaitez utiliser.

    Pour obtenir des types de données de performances, vous devrez peut-être utiliser des classes fournies par des fournisseurs hautement performants. Pour plus d’informations, consultez [analyse des données de performances](monitoring-performance-data.md), [détermination du type d’événement à recevoir](determining-the-type-of-event-to-receive.md)et [interrogation avec WQL](querying-with-wql.md).

4.  Décidez d’effectuer un appel asynchrone ou un appel semi-synchrone, puis de choisir la méthode de l’API.

    Les appels asynchrones vous permettent d’éviter la surcharge liée à l’interrogation des données. Toutefois, les appels semi-synchrones offrent des performances similaires avec une sécurité accrue. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

5.  Effectuez l’appel de la méthode asynchrone ou semi-synchrone et incluez une requête d’événement en tant que paramètre *strQuery* .

    Pour les applications C++, appelez les méthodes suivantes :

    -   [**IWbemServices :: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery)
    -   [**IWbemServices :: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)

    Pour les scripts, appelez les méthodes suivantes :

    -   [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)
    -   [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md)

6.  Écrivez le code pour traiter l’objet d’événement retourné.

    Pour les requêtes d’événements asynchrones, placez le code dans les diverses méthodes ou événements du récepteur d’objets. Pour les requêtes d’événements semi-synchrones, chaque objet est retourné au fur et à mesure que WMI l’obtient. le code doit donc être dans la boucle qui gère chaque objet.

L’exemple de code de script suivant est une version asynchrone du script [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) . Étant donné que les opérations asynchrones sont retournées immédiatement, une boîte de dialogue garde le script actif pendant qu’il attend des événements.

Au lieu d’appeler [**SWbemEventSource. NextEvent**](swbemeventsource-nextevent.md) pour recevoir chaque événement, le script a un gestionnaire d’événements pour l’événement [**OnObjectReady SWbemSink**](swbemsink-onobjectready.md) .


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\CIMV2") 
Set EventSink = WScript.CreateObject( _
    "WbemScripting.SWbemSink","SINK_")

objWMIservice.ExecNotificationQueryAsync EventSink, _
    "SELECT * FROM Win32_ProcessTrace WITHIN 10"
WScript.Echo "Waiting for events..."

i = 0
While (True)
    Wscript.Sleep(1000)
Wend

Sub SINK_OnObjectReady(objObject, objAsyncContext)
    Wscript.Echo "Win32_ProcessTrace event has occurred."
    i = i+1
    If i = 3 Then WScript.Quit 0 
End Sub

```



> [!Note]
>
> Un rappel asynchrone, tel qu’un rappel géré par la `SINK_OnObjectReady` sous-routine, permet à un utilisateur non authentifié de fournir des données au récepteur. Pour une meilleure sécurité, utilisez une communication semi-synchrone ou une communication synchrone. Pour plus d'informations, voir les rubriques suivantes :
>
> -   [Appel semi-synchrone avec C++](making-a-semisynchronous-call-with-c--.md)
> -   [Exécution d’un appel semi-synchrone avec VBScript](making-a-semisynchronous-call-with-vbscript.md)
> -   [Exécution d’un appel asynchrone avec C++](making-an-asynchronous-call-with-c--.md)
> -   [Exécution d’un appel asynchrone avec VBScript](making-an-asynchronous-call-with-vbscript.md)
> -   [Définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md)
> -   [Sécurisation des clients de script](securing-scripting-clients.md)

 

## <a name="using-permanent-event-consumers"></a>Utilisation des consommateurs d’événements permanents

Un consommateur d’événements permanent s’exécute jusqu’à ce que son inscription soit annulée explicitement, puis démarre lors du redémarrage de WMI ou du système.

Un consommateur d’événements permanent est une combinaison de classes WMI, de filtres et d’objets COM sur un système.

La liste suivante identifie les parties nécessaires à la création d’un consommateur d’événements permanent :

-   Objet COM contenant le code qui implémente le consommateur permanent.
-   Nouvelle classe de consommateur permanente.
-   Instance de la classe de consommateur permanente.
-   Filtre qui contient la requête pour les événements.
-   Lien entre le consommateur et le filtre.

Pour plus d’informations, consultez [réception d’événements à tout moment](--filtertoconsumerbinding.md).

WMI fournit plusieurs consommateurs permanents. Les classes de consommateur et l’objet COM contenant le code sont préinstallés. Par exemple, vous pouvez créer et configurer une instance de la classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) pour exécuter un script lorsqu’un événement se produit. Pour plus d’informations, consultez [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md). Pour obtenir un exemple d’utilisation de **ActiveScriptEventConsumer**, consultez [exécution d’un script basé sur un événement](running-a-script-based-on-an-event.md).

La procédure suivante décrit comment créer un consommateur d’événements permanent.

**Pour créer un consommateur d’événements permanent**

1.  [Inscrivez le fournisseur d’événements](registering-a-provider.md) avec l’espace de noms que vous utilisez.

    Certains fournisseurs d’événements peuvent uniquement utiliser un espace de noms spécifique. Par exemple, [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) est un événement intrinsèque qui est pris en charge par le [fournisseur Win32](/windows/desktop/CIMWin32Prov/win32-provider) et qui est inscrit par défaut avec l' \\ espace de \\ noms CIMV2 racine.

    > [!Note]  
    > Vous pouvez utiliser la propriété **EventNamespace** du [**\_ \_ EventFilter**](--eventfilter.md) utilisé dans l’inscription pour créer un abonnement entre espaces de noms. Pour plus d’informations, consultez [Implementing Cross-namespace permanent Event subscriptions](implementing-cross-namespace-permanent-event-subscriptions.md).

     

2.  [Inscrivez le fournisseur de consommateur d’événements](registering-an-event-consumer-provider.md) avec l’espace de noms où se trouvent les classes d’événements.

    WMI utilise un fournisseur de consommateur d’événements pour rechercher un consommateur d’événements permanent. Le consommateur d’événements permanent est l’application lancée par WMI lorsqu’un événement est reçu. Pour inscrire un consommateur d’événements, les fournisseurs créent des instances de [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md).

3.  Créez une instance de la classe qui représente le consommateur d’événements permanent que vous souhaitez utiliser.

    Les classes de consommateur d’événements sont dérivées de la classe [**\_ \_ EventConsumer**](--eventconsumer.md). Définissez les propriétés requises par l’instance du consommateur d’événements.

4.  Inscrivez le consommateur auprès de COM à l’aide de l’utilitaire **regsvr32** .
5.  Créez une instance de la classe de filtre d’événement [**\_ \_ EventFilter**](--eventfilter.md).

    Définissez les champs requis pour l’instance de filtre d’événement. Les champs requis pour [**\_ \_ EventFilter**](--eventfilter.md) sont **Name**, **QueryLanguage** et **query**. La propriété **Name** peut être n’importe quel nom unique pour une instance de cette classe. La propriété **QueryLanguage** a toujours la valeur « WQL ». La propriété de **requête** est une chaîne qui contient une requête d’événement. Un événement est généré en cas d’échec de la requête d’un consommateur d’événements permanent. La source de l’événement est WinMgmt, l’ID d’événement est 10 et le type d’événement est Error.

6.  Créez une instance de la classe [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) pour associer un consommateur d’événements logiques à un filtre d’événement.

    WMI utilise une association pour rechercher le consommateur d’événements associé à l’événement qui correspond aux critères spécifiés dans le filtre d’événement. WMI utilise le fournisseur de consommateur d’événements pour Rechercher l’application de consommateur d’événements permanente à démarrer.

 

 
