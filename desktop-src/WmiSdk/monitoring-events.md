---
description: Les administrateurs système peuvent utiliser WMI pour surveiller les événements sur un réseau.
ms.assetid: 871d4add-a7b1-4ec9-a202-3821fdf09e9f
ms.tgt_platform: multiple
title: Surveillance des événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea5d9fc6f9a12f4aa1fb7bc0ff6f66fc4dd4a7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114278"
---
# <a name="monitoring-events"></a><span data-ttu-id="68159-103">Surveillance des événements</span><span class="sxs-lookup"><span data-stu-id="68159-103">Monitoring Events</span></span>

<span data-ttu-id="68159-104">Les administrateurs système peuvent utiliser WMI pour surveiller les événements sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="68159-104">System administrators can use WMI to monitor events on a network.</span></span> <span data-ttu-id="68159-105">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="68159-105">For example:</span></span>

-   <span data-ttu-id="68159-106">Un service s’arrête de manière inattendue.</span><span class="sxs-lookup"><span data-stu-id="68159-106">A service stops unexpectedly.</span></span>
-   <span data-ttu-id="68159-107">Un serveur devient indisponible.</span><span class="sxs-lookup"><span data-stu-id="68159-107">A server becomes unavailable.</span></span>
-   <span data-ttu-id="68159-108">Un lecteur de disque remplit la capacité de 80%.</span><span class="sxs-lookup"><span data-stu-id="68159-108">A disk drive fills to 80% capacity.</span></span>
-   <span data-ttu-id="68159-109">Les événements de sécurité sont signalés dans un journal des événements NT.</span><span class="sxs-lookup"><span data-stu-id="68159-109">Security events are reported to an NT Event Log.</span></span>

<span data-ttu-id="68159-110">WMI prend en charge la détection et la remise d’événements aux consommateurs d’événements, car certains fournisseurs WMI sont des fournisseurs d’événements.</span><span class="sxs-lookup"><span data-stu-id="68159-110">WMI supports event detection and delivery to event consumers because some WMI providers are event providers.</span></span> <span data-ttu-id="68159-111">Pour plus d’informations, consultez [réception d’un événement WMI](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="68159-111">For more information, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

<span data-ttu-id="68159-112">Les [*consommateurs d’événements*](gloss-e.md) sont des applications ou des scripts qui demandent une notification d’événements, puis exécutent des tâches lorsque des événements spécifiques se produisent.</span><span class="sxs-lookup"><span data-stu-id="68159-112">[*Event consumers*](gloss-e.md) are applications or scripts that request notification of events, and then perform tasks when specific events occur.</span></span> <span data-ttu-id="68159-113">Vous pouvez créer des scripts ou des applications de surveillance des événements qui surveillent temporairement le moment où les événements se produisent.</span><span class="sxs-lookup"><span data-stu-id="68159-113">You can create event monitoring scripts or applications that temporarily monitor when events occur.</span></span> <span data-ttu-id="68159-114">WMI fournit également un ensemble de fournisseurs d’événements permanents préinstallés et les classes de consommateurs permanentes qui vous permettent de surveiller de façon permanente les événements.</span><span class="sxs-lookup"><span data-stu-id="68159-114">WMI also supplies a set of preinstalled permanent event providers and the permanent consumer classes that enable you to permanently monitor events.</span></span> <span data-ttu-id="68159-115">Pour plus d’informations, consultez [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="68159-115">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="68159-116">Les sections suivantes sont présentées dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="68159-116">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="68159-117">Utilisation des consommateurs d’événements temporaires</span><span class="sxs-lookup"><span data-stu-id="68159-117">Using Temporary Event Consumers</span></span>](#using-temporary-event-consumers)
-   [<span data-ttu-id="68159-118">Utilisation des consommateurs d’événements permanents</span><span class="sxs-lookup"><span data-stu-id="68159-118">Using Permanent Event Consumers</span></span>](#using-permanent-event-consumers)

## <a name="using-temporary-event-consumers"></a><span data-ttu-id="68159-119">Utilisation des consommateurs d’événements temporaires</span><span class="sxs-lookup"><span data-stu-id="68159-119">Using Temporary Event Consumers</span></span>

<span data-ttu-id="68159-120">Les consommateurs d’événements temporaires sont des scripts ou des applications qui retournent les événements qui correspondent à une requête d’événement ou à un filtre.</span><span class="sxs-lookup"><span data-stu-id="68159-120">Temporary event consumers are scripts or applications that return the events that match an event query or filter.</span></span> <span data-ttu-id="68159-121">Les requêtes d’événements temporaires utilisent généralement [**IWbemServices :: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) dans les applications C++ ou [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) dans des scripts et des Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="68159-121">Temporary event queries usually use either [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) in C++ applications or [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) in scripts and Visual Basic.</span></span>

<span data-ttu-id="68159-122">Une requête d’événement demande des instances d’une classe d’événements qui spécifient un certain type d’événement, tel que [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) ou [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span><span class="sxs-lookup"><span data-stu-id="68159-122">An event query requests instances of an event class that specifies a certain type of event, such as [**Win32\_ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) or [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span></span>

<span data-ttu-id="68159-123">L’exemple de code VBScript suivant demande une notification lorsqu’une instance de [**\_ ProcessTrace Win32**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) est créée.</span><span class="sxs-lookup"><span data-stu-id="68159-123">The following VBScript code example requests notification when an instance of [**Win32\_ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) is created.</span></span> <span data-ttu-id="68159-124">Une instance de cette classe est générée lorsqu’un processus est démarré ou arrêté.</span><span class="sxs-lookup"><span data-stu-id="68159-124">An instance of this class is generated when a process is started or stopped.</span></span>

<span data-ttu-id="68159-125">Pour exécuter le script, copiez-le dans un fichier nommé event.vbs et utilisez la ligne de commande suivante : **cscript event.vbs**.</span><span class="sxs-lookup"><span data-stu-id="68159-125">To execute the script, copy it to a file named event.vbs and use the following command line: **cscript event.vbs**.</span></span> <span data-ttu-id="68159-126">Vous pouvez voir la sortie du script en démarrant Notepad.exe ou tout autre processus.</span><span class="sxs-lookup"><span data-stu-id="68159-126">You can see output from the script by starting Notepad.exe or any other process.</span></span> <span data-ttu-id="68159-127">Le script s’arrête après le démarrage ou l’arrêt de cinq processus.</span><span class="sxs-lookup"><span data-stu-id="68159-127">The script stops after five processes have started or stopped.</span></span>

<span data-ttu-id="68159-128">Ce script appelle [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md), qui est la version [*semi-synchrone*](gloss-s.md) de la méthode.</span><span class="sxs-lookup"><span data-stu-id="68159-128">This script calls [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md), which is the [*semisynchronous*](gloss-s.md) version of the method.</span></span> <span data-ttu-id="68159-129">Consultez le script suivant pour obtenir un exemple de configuration d’un abonnement d’événement temporaire asynchrone en appelant [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md).</span><span class="sxs-lookup"><span data-stu-id="68159-129">See the next script for an example of setting up an asynchronous temporary event subscription by calling [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md).</span></span> <span data-ttu-id="68159-130">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="68159-130">For more information, see [Calling a Method](calling-a-method.md).</span></span> <span data-ttu-id="68159-131">Le script appelle [**SWbemEventSource. NextEvent**](swbemeventsource-nextevent.md) pour obtenir et traiter chaque événement au fur et à mesure de son arrivée.</span><span class="sxs-lookup"><span data-stu-id="68159-131">The script calls [**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md) to obtain and process each event as it arrives.</span></span> <span data-ttu-id="68159-132">Enregistrez le script dans un fichier avec une extension. vbs et exécutez le script sur une ligne de commande à l’aide de CScript : **cscript file.vbs**.</span><span class="sxs-lookup"><span data-stu-id="68159-132">Save the script in a file with a .vbs extension and run the script on a command line using CScript: **cscript file.vbs**.</span></span>


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



Les consommateurs d’événements temporaires doivent être démarrés manuellement et ne doivent pas être conservés à travers les redémarrages WMI ou les redémarrages du système d’exploitation. <span data-ttu-id="68159-134">Un consommateur d’événements temporaire peut traiter les événements uniquement lorsqu’il est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="68159-134">A temporary event consumer can process events only while it is running.</span></span>

<span data-ttu-id="68159-135">La procédure suivante décrit comment créer un consommateur d’événements temporaire.</span><span class="sxs-lookup"><span data-stu-id="68159-135">The following procedure describes how to create a temporary event consumer.</span></span>

<span data-ttu-id="68159-136">**Pour créer un consommateur d’événements temporaire**</span><span class="sxs-lookup"><span data-stu-id="68159-136">**To create a temporary event consumer**</span></span>

1.  <span data-ttu-id="68159-137">Choisissez le langage de programmation à utiliser.</span><span class="sxs-lookup"><span data-stu-id="68159-137">Decide which programming language to use.</span></span>

    <span data-ttu-id="68159-138">Le langage de programmation détermine l’API à utiliser.</span><span class="sxs-lookup"><span data-stu-id="68159-138">The programming language determines the API to use.</span></span>

    -   <span data-ttu-id="68159-139">Pour le langage de programmation C++, utilisez l' [API com pour WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="68159-139">For the C++ programming language, use the [COM API for WMI](com-api-for-wmi.md).</span></span>
    -   <span data-ttu-id="68159-140">Pour les Visual Basic ou les langages de script, utilisez l' [API de script pour WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="68159-140">For Visual Basic or scripting languages, use the [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

2.  <span data-ttu-id="68159-141">Commencez le codage d’une application de consommateur d’événements temporaire de la même façon que vous démarrez une application WMI.</span><span class="sxs-lookup"><span data-stu-id="68159-141">Start coding a temporary event consumer application the same way that you start a WMI application.</span></span>

    <span data-ttu-id="68159-142">Les premières étapes du codage dépendent du langage de programmation.</span><span class="sxs-lookup"><span data-stu-id="68159-142">The first steps of coding depend on the programming language.</span></span> <span data-ttu-id="68159-143">En règle générale, vous vous connectez à WMI et configurez les paramètres de sécurité.</span><span class="sxs-lookup"><span data-stu-id="68159-143">Typically, you log onto WMI and set up the security settings.</span></span> <span data-ttu-id="68159-144">Pour plus d’informations, consultez [création d’une application ou d’un script WMI](creating-a-wmi-application-or-script.md).</span><span class="sxs-lookup"><span data-stu-id="68159-144">For more information, see [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span>

3.  <span data-ttu-id="68159-145">Définissez la requête d’événement que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="68159-145">Define the event query that you want to use.</span></span>

    <span data-ttu-id="68159-146">Pour obtenir des types de données de performances, vous devrez peut-être utiliser des classes fournies par des fournisseurs hautement performants.</span><span class="sxs-lookup"><span data-stu-id="68159-146">To obtain some types of performance data, you may need to use classes provided by high-performance providers.</span></span> <span data-ttu-id="68159-147">Pour plus d’informations, consultez [analyse des données de performances](monitoring-performance-data.md), [détermination du type d’événement à recevoir](determining-the-type-of-event-to-receive.md)et [interrogation avec WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="68159-147">For more information, see [Monitoring Performance Data](monitoring-performance-data.md), [Determining the Type of Event To Receive](determining-the-type-of-event-to-receive.md), and [Querying with WQL](querying-with-wql.md).</span></span>

4.  <span data-ttu-id="68159-148">Décidez d’effectuer un appel asynchrone ou un appel semi-synchrone, puis de choisir la méthode de l’API.</span><span class="sxs-lookup"><span data-stu-id="68159-148">Decide to make either an asynchronous call or an semisynchronous call, and choose the API method.</span></span>

    <span data-ttu-id="68159-149">Les appels asynchrones vous permettent d’éviter la surcharge liée à l’interrogation des données.</span><span class="sxs-lookup"><span data-stu-id="68159-149">Asynchronous calls allow you to avoid the overhead of polling for data.</span></span> <span data-ttu-id="68159-150">Toutefois, les appels semi-synchrones offrent des performances similaires avec une sécurité accrue.</span><span class="sxs-lookup"><span data-stu-id="68159-150">However, semisynchronous calls provide similar performance with greater security.</span></span> <span data-ttu-id="68159-151">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="68159-151">For more information, see [Calling a Method](calling-a-method.md).</span></span>

5.  <span data-ttu-id="68159-152">Effectuez l’appel de la méthode asynchrone ou semi-synchrone et incluez une requête d’événement en tant que paramètre *strQuery* .</span><span class="sxs-lookup"><span data-stu-id="68159-152">Make the asynchronous or semisynchronous method call and include an event query as the *strQuery* parameter.</span></span>

    <span data-ttu-id="68159-153">Pour les applications C++, appelez les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="68159-153">For C++ applications, call the following methods:</span></span>

    -   [<span data-ttu-id="68159-154">**IWbemServices :: ExecNotificationQuery**</span><span class="sxs-lookup"><span data-stu-id="68159-154">**IWbemServices::ExecNotificationQuery**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery)
    -   [<span data-ttu-id="68159-155">**IWbemServices :: ExecNotificationQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="68159-155">**IWbemServices::ExecNotificationQueryAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)

    <span data-ttu-id="68159-156">Pour les scripts, appelez les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="68159-156">For scripts, call the following methods:</span></span>

    -   [<span data-ttu-id="68159-157">**SWbemServices.ExecNotificationQuery**</span><span class="sxs-lookup"><span data-stu-id="68159-157">**SWbemServices.ExecNotificationQuery**</span></span>](swbemservices-execnotificationquery.md)
    -   [<span data-ttu-id="68159-158">**SWbemServices.ExecNotificationQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="68159-158">**SWbemServices.ExecNotificationQueryAsync**</span></span>](swbemservices-execnotificationqueryasync.md)

6.  <span data-ttu-id="68159-159">Écrivez le code pour traiter l’objet d’événement retourné.</span><span class="sxs-lookup"><span data-stu-id="68159-159">Write the code to process the returned event object.</span></span>

    <span data-ttu-id="68159-160">Pour les requêtes d’événements asynchrones, placez le code dans les diverses méthodes ou événements du récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="68159-160">For asynchronous event queries, put the code in the various methods or events of the object sink.</span></span> <span data-ttu-id="68159-161">Pour les requêtes d’événements semi-synchrones, chaque objet est retourné au fur et à mesure que WMI l’obtient. le code doit donc être dans la boucle qui gère chaque objet.</span><span class="sxs-lookup"><span data-stu-id="68159-161">For semisynchronous event queries, each object is returned as WMI obtains it, so the code should be in the loop that handles each object.</span></span>

<span data-ttu-id="68159-162">L’exemple de code de script suivant est une version asynchrone du script [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) .</span><span class="sxs-lookup"><span data-stu-id="68159-162">The following script code example is an asynchronous version of the [**Win32\_ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) script.</span></span> <span data-ttu-id="68159-163">Étant donné que les opérations asynchrones sont retournées immédiatement, une boîte de dialogue garde le script actif pendant qu’il attend des événements.</span><span class="sxs-lookup"><span data-stu-id="68159-163">Because asynchronous operations return immediately, a dialog box keeps the script active while it is waiting for events.</span></span>

<span data-ttu-id="68159-164">Au lieu d’appeler [**SWbemEventSource. NextEvent**](swbemeventsource-nextevent.md) pour recevoir chaque événement, le script a un gestionnaire d’événements pour l’événement [**OnObjectReady SWbemSink**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="68159-164">Rather than call [**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md) to receive each event, the script has an event handler for the [**SWbemSink OnObjectReady**](swbemsink-onobjectready.md) event.</span></span>


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
> <span data-ttu-id="68159-165">Un rappel asynchrone, tel qu’un rappel géré par la `SINK_OnObjectReady` sous-routine, permet à un utilisateur non authentifié de fournir des données au récepteur.</span><span class="sxs-lookup"><span data-stu-id="68159-165">An asynchronous callback such as a callback handled by the `SINK_OnObjectReady` subroutine, allows a nonauthenticated user to provide data to the sink.</span></span> <span data-ttu-id="68159-166">Pour une meilleure sécurité, utilisez une communication semi-synchrone ou une communication synchrone.</span><span class="sxs-lookup"><span data-stu-id="68159-166">For better security, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="68159-167">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="68159-167">For more information, see the following topics:</span></span>
>
> -   [<span data-ttu-id="68159-168">Appel semi-synchrone avec C++</span><span class="sxs-lookup"><span data-stu-id="68159-168">Making a Semisynchronous Call with C++</span></span>](making-a-semisynchronous-call-with-c--.md)
> -   [<span data-ttu-id="68159-169">Exécution d’un appel semi-synchrone avec VBScript</span><span class="sxs-lookup"><span data-stu-id="68159-169">Making a Semisynchronous Call with VBScript</span></span>](making-a-semisynchronous-call-with-vbscript.md)
> -   [<span data-ttu-id="68159-170">Exécution d’un appel asynchrone avec C++</span><span class="sxs-lookup"><span data-stu-id="68159-170">Making an Asynchronous Call with C++</span></span>](making-an-asynchronous-call-with-c--.md)
> -   [<span data-ttu-id="68159-171">Exécution d’un appel asynchrone avec VBScript</span><span class="sxs-lookup"><span data-stu-id="68159-171">Making an Asynchronous Call with VBScript</span></span>](making-an-asynchronous-call-with-vbscript.md)
> -   [<span data-ttu-id="68159-172">Définition de la sécurité sur un appel asynchrone</span><span class="sxs-lookup"><span data-stu-id="68159-172">Setting Security on an Asynchronous Call</span></span>](setting-security-on-an-asynchronous-call.md)
> -   [<span data-ttu-id="68159-173">Sécurisation des clients de script</span><span class="sxs-lookup"><span data-stu-id="68159-173">Securing Scripting Clients</span></span>](securing-scripting-clients.md)

 

## <a name="using-permanent-event-consumers"></a><span data-ttu-id="68159-174">Utilisation des consommateurs d’événements permanents</span><span class="sxs-lookup"><span data-stu-id="68159-174">Using Permanent Event Consumers</span></span>

<span data-ttu-id="68159-175">Un consommateur d’événements permanent s’exécute jusqu’à ce que son inscription soit annulée explicitement, puis démarre lors du redémarrage de WMI ou du système.</span><span class="sxs-lookup"><span data-stu-id="68159-175">A permanent event consumer runs until its registration is explicitly canceled, and then starts up when WMI or the system restarts.</span></span>

<span data-ttu-id="68159-176">Un consommateur d’événements permanent est une combinaison de classes WMI, de filtres et d’objets COM sur un système.</span><span class="sxs-lookup"><span data-stu-id="68159-176">A permanent event consumer is a combination of WMI classes, filters, and COM objects on a system.</span></span>

<span data-ttu-id="68159-177">La liste suivante identifie les parties nécessaires à la création d’un consommateur d’événements permanent :</span><span class="sxs-lookup"><span data-stu-id="68159-177">The following list identifies the parts required to create a permanent event consumer:</span></span>

-   <span data-ttu-id="68159-178">Objet COM contenant le code qui implémente le consommateur permanent.</span><span class="sxs-lookup"><span data-stu-id="68159-178">A COM object containing the code that implements the permanent consumer.</span></span>
-   <span data-ttu-id="68159-179">Nouvelle classe de consommateur permanente.</span><span class="sxs-lookup"><span data-stu-id="68159-179">A new permanent consumer class.</span></span>
-   <span data-ttu-id="68159-180">Instance de la classe de consommateur permanente.</span><span class="sxs-lookup"><span data-stu-id="68159-180">An instance of the permanent consumer class.</span></span>
-   <span data-ttu-id="68159-181">Filtre qui contient la requête pour les événements.</span><span class="sxs-lookup"><span data-stu-id="68159-181">A filter that contains the query for events.</span></span>
-   <span data-ttu-id="68159-182">Lien entre le consommateur et le filtre.</span><span class="sxs-lookup"><span data-stu-id="68159-182">A link between the consumer and the filter.</span></span>

<span data-ttu-id="68159-183">Pour plus d’informations, consultez [réception d’événements à tout moment](--filtertoconsumerbinding.md).</span><span class="sxs-lookup"><span data-stu-id="68159-183">For more information, see [Receiving Events At All Times](--filtertoconsumerbinding.md).</span></span>

<span data-ttu-id="68159-184">WMI fournit plusieurs consommateurs permanents.</span><span class="sxs-lookup"><span data-stu-id="68159-184">WMI supplies several permanent consumers.</span></span> <span data-ttu-id="68159-185">Les classes de consommateur et l’objet COM contenant le code sont préinstallés.</span><span class="sxs-lookup"><span data-stu-id="68159-185">The consumer classes and COM object containing the code are preinstalled.</span></span> <span data-ttu-id="68159-186">Par exemple, vous pouvez créer et configurer une instance de la classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) pour exécuter un script lorsqu’un événement se produit.</span><span class="sxs-lookup"><span data-stu-id="68159-186">For example, you can create and configure an instance of the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class to run a script when an event occurs.</span></span> <span data-ttu-id="68159-187">Pour plus d’informations, consultez [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="68159-187">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span> <span data-ttu-id="68159-188">Pour obtenir un exemple d’utilisation de **ActiveScriptEventConsumer**, consultez [exécution d’un script basé sur un événement](running-a-script-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="68159-188">For an example of using **ActiveScriptEventConsumer**, see [Running a Script Based on an Event](running-a-script-based-on-an-event.md).</span></span>

<span data-ttu-id="68159-189">La procédure suivante décrit comment créer un consommateur d’événements permanent.</span><span class="sxs-lookup"><span data-stu-id="68159-189">The following procedure describes how to create a permanent event consumer.</span></span>

<span data-ttu-id="68159-190">**Pour créer un consommateur d’événements permanent**</span><span class="sxs-lookup"><span data-stu-id="68159-190">**To create a permanent event consumer**</span></span>

1.  <span data-ttu-id="68159-191">[Inscrivez le fournisseur d’événements](registering-a-provider.md) avec l’espace de noms que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="68159-191">[Register the event provider](registering-a-provider.md) with the namespace that you are using.</span></span>

    <span data-ttu-id="68159-192">Certains fournisseurs d’événements peuvent uniquement utiliser un espace de noms spécifique.</span><span class="sxs-lookup"><span data-stu-id="68159-192">Some event providers can only use a specific namespace.</span></span> <span data-ttu-id="68159-193">Par exemple, [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) est un événement intrinsèque qui est pris en charge par le [fournisseur Win32](/windows/desktop/CIMWin32Prov/win32-provider) et qui est inscrit par défaut avec l' \\ espace de \\ noms CIMV2 racine.</span><span class="sxs-lookup"><span data-stu-id="68159-193">For example, [**\_\_InstanceCreationEvent**](--instancecreationevent.md) is an intrinsic event that is supported by the [Win32 provider](/windows/desktop/CIMWin32Prov/win32-provider) and is registered by default with the \\root\\cimv2 namespace.</span></span>

    > [!Note]  
    > <span data-ttu-id="68159-194">Vous pouvez utiliser la propriété **EventNamespace** du [**\_ \_ EventFilter**](--eventfilter.md) utilisé dans l’inscription pour créer un abonnement entre espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="68159-194">You can use the **EventNamespace** property of the [**\_\_EventFilter**](--eventfilter.md) used in the registration to create a cross-namespace subscription.</span></span> <span data-ttu-id="68159-195">Pour plus d’informations, consultez [Implementing Cross-namespace permanent Event subscriptions](implementing-cross-namespace-permanent-event-subscriptions.md).</span><span class="sxs-lookup"><span data-stu-id="68159-195">For more information, see [Implementing Cross-Namespace Permanent Event Subscriptions](implementing-cross-namespace-permanent-event-subscriptions.md).</span></span>

     

2.  <span data-ttu-id="68159-196">[Inscrivez le fournisseur de consommateur d’événements](registering-an-event-consumer-provider.md) avec l’espace de noms où se trouvent les classes d’événements.</span><span class="sxs-lookup"><span data-stu-id="68159-196">[Register the event consumer provider](registering-an-event-consumer-provider.md) with the namespace where event classes are located.</span></span>

    <span data-ttu-id="68159-197">WMI utilise un fournisseur de consommateur d’événements pour rechercher un consommateur d’événements permanent.</span><span class="sxs-lookup"><span data-stu-id="68159-197">WMI uses an event consumer provider to find an event consumer that is permanent.</span></span> <span data-ttu-id="68159-198">Le consommateur d’événements permanent est l’application lancée par WMI lorsqu’un événement est reçu.</span><span class="sxs-lookup"><span data-stu-id="68159-198">The permanent event consumer is the application that WMI starts when an event is received.</span></span> <span data-ttu-id="68159-199">Pour inscrire un consommateur d’événements, les fournisseurs créent des instances de [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="68159-199">To register event consumer, providers create instances of [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md).</span></span>

3.  <span data-ttu-id="68159-200">Créez une instance de la classe qui représente le consommateur d’événements permanent que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="68159-200">Create an instance of the class that represents the permanent event consumer you want to use.</span></span>

    <span data-ttu-id="68159-201">Les classes de consommateur d’événements sont dérivées de la classe [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="68159-201">Event consumer classes are derived from the class [**\_\_EventConsumer**](--eventconsumer.md).</span></span> <span data-ttu-id="68159-202">Définissez les propriétés requises par l’instance du consommateur d’événements.</span><span class="sxs-lookup"><span data-stu-id="68159-202">Set the properties that the event consumer instance requires.</span></span>

4.  <span data-ttu-id="68159-203">Inscrivez le consommateur auprès de COM à l’aide de l’utilitaire **regsvr32** .</span><span class="sxs-lookup"><span data-stu-id="68159-203">Register the consumer with COM by using the **regsvr32** utility.</span></span>
5.  <span data-ttu-id="68159-204">Créez une instance de la classe de filtre d’événement [**\_ \_ EventFilter**](--eventfilter.md).</span><span class="sxs-lookup"><span data-stu-id="68159-204">Create an instance of the event filter class [**\_\_EventFilter**](--eventfilter.md).</span></span>

    <span data-ttu-id="68159-205">Définissez les champs requis pour l’instance de filtre d’événement.</span><span class="sxs-lookup"><span data-stu-id="68159-205">Set the required fields for the event filter instance.</span></span> <span data-ttu-id="68159-206">Les champs requis pour [**\_ \_ EventFilter**](--eventfilter.md) sont **Name**, **QueryLanguage** et **query**.</span><span class="sxs-lookup"><span data-stu-id="68159-206">The required fields for [**\_\_EventFilter**](--eventfilter.md) are **Name**, **QueryLanguage**, and **Query**.</span></span> <span data-ttu-id="68159-207">La propriété **Name** peut être n’importe quel nom unique pour une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="68159-207">The **Name** property can be any unique name for an instance of this class.</span></span> <span data-ttu-id="68159-208">La propriété **QueryLanguage** a toujours la valeur « WQL ».</span><span class="sxs-lookup"><span data-stu-id="68159-208">The **QueryLanguage** property is always set to "WQL".</span></span> <span data-ttu-id="68159-209">La propriété de **requête** est une chaîne qui contient une requête d’événement.</span><span class="sxs-lookup"><span data-stu-id="68159-209">The **Query** property is a string that contains an event query.</span></span> <span data-ttu-id="68159-210">Un événement est généré en cas d’échec de la requête d’un consommateur d’événements permanent.</span><span class="sxs-lookup"><span data-stu-id="68159-210">An event is generated when a permanent event consumer's query fails.</span></span> <span data-ttu-id="68159-211">La source de l’événement est WinMgmt, l’ID d’événement est 10 et le type d’événement est Error.</span><span class="sxs-lookup"><span data-stu-id="68159-211">The event's source is WinMgmt, the event ID is 10, and the event type is Error.</span></span>

6.  <span data-ttu-id="68159-212">Créez une instance de la classe [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) pour associer un consommateur d’événements logiques à un filtre d’événement.</span><span class="sxs-lookup"><span data-stu-id="68159-212">Create an instance of the [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) class to associate a logical event consumer with an event filter.</span></span>

    <span data-ttu-id="68159-213">WMI utilise une association pour rechercher le consommateur d’événements associé à l’événement qui correspond aux critères spécifiés dans le filtre d’événement.</span><span class="sxs-lookup"><span data-stu-id="68159-213">WMI uses an association to find the event consumer associated with the event that matches the criteria specified in the event filter.</span></span> <span data-ttu-id="68159-214">WMI utilise le fournisseur de consommateur d’événements pour Rechercher l’application de consommateur d’événements permanente à démarrer.</span><span class="sxs-lookup"><span data-stu-id="68159-214">WMI uses the event consumer provider to find the permanent event consumer application to start.</span></span>

 

 
