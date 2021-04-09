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
# <a name="receiving-a-wmi-event"></a><span data-ttu-id="6a589-104">Réception d’un événement WMI</span><span class="sxs-lookup"><span data-stu-id="6a589-104">Receiving a WMI Event</span></span>

<span data-ttu-id="6a589-105">WMI contient une infrastructure d’événements qui produit des notifications sur les modifications apportées aux données et services WMI.</span><span class="sxs-lookup"><span data-stu-id="6a589-105">WMI contains an event infrastructure that produces notifications about changes in WMI data and services.</span></span> <span data-ttu-id="6a589-106">Les [*classes d’événements*](gloss-e.md) WMI fournissent une notification lorsque des événements spécifiques se produisent.</span><span class="sxs-lookup"><span data-stu-id="6a589-106">WMI [*event classes*](gloss-e.md) provide notification when specific events occur.</span></span>

<span data-ttu-id="6a589-107">Les sections suivantes sont présentées dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="6a589-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="6a589-108">Requêtes d’événements</span><span class="sxs-lookup"><span data-stu-id="6a589-108">Event Queries</span></span>](#event-queries)
-   [<span data-ttu-id="6a589-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="6a589-109">Example</span></span>](#example)
-   [<span data-ttu-id="6a589-110">Consommateurs d’événements</span><span class="sxs-lookup"><span data-stu-id="6a589-110">Event Consumers</span></span>](#event-consumers)
-   [<span data-ttu-id="6a589-111">Fournir des événements</span><span class="sxs-lookup"><span data-stu-id="6a589-111">Providing Events</span></span>](#providing-events)
-   [<span data-ttu-id="6a589-112">Quotas d’abonnement</span><span class="sxs-lookup"><span data-stu-id="6a589-112">Subscription Quotas</span></span>](#subscription-quotas)
-   [<span data-ttu-id="6a589-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6a589-113">Related topics</span></span>](#related-topics)

## <a name="event-queries"></a><span data-ttu-id="6a589-114">Requêtes d’événements</span><span class="sxs-lookup"><span data-stu-id="6a589-114">Event Queries</span></span>

<span data-ttu-id="6a589-115">Vous pouvez créer une requête [semi-synchrone](receiving-synchronous-and-semisynchronous-event-notifications.md) ou [**asynchrone**](receiving-asynchronous-event-notifications.md) pour surveiller les modifications apportées aux journaux des événements, à la création du processus, à l’état du service, à la disponibilité de l’ordinateur ou à l’espace disque disponible, ainsi qu’à d’autres entités ou événements</span><span class="sxs-lookup"><span data-stu-id="6a589-115">You can create a [semisynchronous](receiving-synchronous-and-semisynchronous-event-notifications.md) or [**asynchronous**](receiving-asynchronous-event-notifications.md) query to monitor changes to event logs, process creation, service status, computer availability or disk drive free space, and other entities or events.</span></span> <span data-ttu-id="6a589-116">Dans les scripts, la méthode [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) est utilisée pour s’abonner à des événements.</span><span class="sxs-lookup"><span data-stu-id="6a589-116">In scripting, the [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) method is used to subscribe to events.</span></span> <span data-ttu-id="6a589-117">En C++, [**IWbemServices :: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="6a589-117">In C++, [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) is used.</span></span> <span data-ttu-id="6a589-118">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="6a589-118">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="6a589-119">La notification d’une modification dans le modèle de données WMI standard est appelée [*événement intrinsèque*](gloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="6a589-119">Notification of a change in the standard WMI data model is called an [*intrinsic event*](gloss-i.md).</span></span> <span data-ttu-id="6a589-120">[**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) ou [**\_ \_ NamespaceDeletionEvent**](--namespacedeletionevent.md) sont des exemples d’événements intrinsèques.</span><span class="sxs-lookup"><span data-stu-id="6a589-120">[**\_\_InstanceCreationEvent**](--instancecreationevent.md) or [**\_\_NamespaceDeletionEvent**](--namespacedeletionevent.md) are examples of intrinsic events.</span></span> <span data-ttu-id="6a589-121">La notification d’une modification apportée par un fournisseur pour définir un événement de fournisseur est appelée [*événement extrinsèque*](gloss-e.md).</span><span class="sxs-lookup"><span data-stu-id="6a589-121">Notification of a change that a provider makes to define a provider event is called an [*extrinsic event*](gloss-e.md).</span></span> <span data-ttu-id="6a589-122">Par exemple, le fournisseur de [Registre système](/previous-versions/windows/desktop/regprov/system-registry-provider), le fournisseur [d’événements de gestion](/windows/desktop/CIMWin32Prov/power-management-event-provider)de l’alimentation et le [fournisseur Win32](/windows/desktop/CIMWin32Prov/win32-provider) définissent leurs propres événements.</span><span class="sxs-lookup"><span data-stu-id="6a589-122">For example, the [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider), [Power Management Event Provider](/windows/desktop/CIMWin32Prov/power-management-event-provider), and [Win32 Provider](/windows/desktop/CIMWin32Prov/win32-provider) define their own events.</span></span> <span data-ttu-id="6a589-123">Pour plus d’informations, consultez [détermination du type d’événement à recevoir](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="6a589-123">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

## <a name="example"></a><span data-ttu-id="6a589-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="6a589-124">Example</span></span>

<span data-ttu-id="6a589-125">L’exemple de code de script suivant est une requête pour le [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) intrinsèque de la classe d’événements [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span><span class="sxs-lookup"><span data-stu-id="6a589-125">The following script code example is a query for the intrinsic [**\_\_InstanceCreationEvent**](--instancecreationevent.md) of the event class [**Win32\_NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span></span> <span data-ttu-id="6a589-126">Vous pouvez exécuter ce programme en arrière-plan et, lorsqu’un événement survient, un message s’affiche.</span><span class="sxs-lookup"><span data-stu-id="6a589-126">You can run this program in the background and when there is an event, a message appears.</span></span> <span data-ttu-id="6a589-127">Si vous fermez la boîte de dialogue en **attente d’événements** , le programme cesse d’attendre les événements.</span><span class="sxs-lookup"><span data-stu-id="6a589-127">If you close the **Waiting for events** dialog box, the program stops waiting for events.</span></span> <span data-ttu-id="6a589-128">N’oubliez pas que le **droit SeSecurityPrivilege** doit être activé.</span><span class="sxs-lookup"><span data-stu-id="6a589-128">Be aware that the **SeSecurityPrivilege** must be enabled.</span></span>


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





<span data-ttu-id="6a589-129">L’exemple de code VBScript suivant montre l’événement extrinsèque défini par le [ \_ \_ fournisseur de Registre](registering-for-system-registry-events.md) .</span><span class="sxs-lookup"><span data-stu-id="6a589-129">The following VBScript code example shows the extrinsic event [\_\_RegistryValueChangeEvent](registering-for-system-registry-events.md) that the registry provider defines.</span></span> <span data-ttu-id="6a589-130">Le script crée un consommateur temporaire en utilisant l’appel à [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md)et reçoit uniquement les événements lorsque le script est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="6a589-130">The script creates a temporary consumer by using the call to [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md), and only receives events when the script is running.</span></span> <span data-ttu-id="6a589-131">Le script suivant s’exécute indéfiniment jusqu’à ce que l’ordinateur soit redémarré, que WMI soit arrêté ou que le script soit arrêté.</span><span class="sxs-lookup"><span data-stu-id="6a589-131">The following script runs indefinitely until the computer is rebooted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="6a589-132">Pour arrêter le script manuellement, utilisez le gestionnaire des tâches pour arrêter le processus.</span><span class="sxs-lookup"><span data-stu-id="6a589-132">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="6a589-133">Pour l’arrêter par programmation, utilisez la méthode [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) dans la classe de \_ processus Win32.</span><span class="sxs-lookup"><span data-stu-id="6a589-133">To stop it programmatically, use the [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) method in the Win32\_Process class.</span></span> <span data-ttu-id="6a589-134">Pour plus d’informations, consultez [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="6a589-134">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>


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



## <a name="event-consumers"></a><span data-ttu-id="6a589-135">Consommateurs d'événements</span><span class="sxs-lookup"><span data-stu-id="6a589-135">Event Consumers</span></span>

<span data-ttu-id="6a589-136">Vous pouvez surveiller ou consommer des événements à l’aide des consommateurs suivants lorsqu’un script ou une application est en cours d’exécution :</span><span class="sxs-lookup"><span data-stu-id="6a589-136">You can monitor or consume events using the following consumers while a script or application is running:</span></span>

-   <span data-ttu-id="6a589-137">Consommateurs d’événements temporaires</span><span class="sxs-lookup"><span data-stu-id="6a589-137">Temporary event consumers</span></span>

    <span data-ttu-id="6a589-138">Un [*consommateur temporaire*](gloss-t.md) est une application cliente WMI qui reçoit un événement WMI.</span><span class="sxs-lookup"><span data-stu-id="6a589-138">A [*temporary consumer*](gloss-t.md) is a WMI client application that receives a WMI event.</span></span> <span data-ttu-id="6a589-139">WMI comprend une interface unique qui permet de spécifier les événements que WMI doit envoyer à une application cliente.</span><span class="sxs-lookup"><span data-stu-id="6a589-139">WMI includes a unique interface that use to specify the events for WMI to send to a client application.</span></span> <span data-ttu-id="6a589-140">Un consommateur d’événements temporaire est considéré comme temporaire, car il fonctionne uniquement lorsqu’il est spécifiquement chargé par un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6a589-140">A temporary event consumer is considered temporary because it only works when specifically loaded by a user.</span></span> <span data-ttu-id="6a589-141">Pour plus d’informations, consultez [réception d’événements pendant la durée de votre application](receiving-events-for-the-duration-of-your-application.md).</span><span class="sxs-lookup"><span data-stu-id="6a589-141">For more information, see [Receiving Events for the Duration of Your Application](receiving-events-for-the-duration-of-your-application.md).</span></span>

-   <span data-ttu-id="6a589-142">Consommateurs d’événements permanents</span><span class="sxs-lookup"><span data-stu-id="6a589-142">Permanent event consumers</span></span>

    <span data-ttu-id="6a589-143">Un [*consommateur permanent*](gloss-p.md) est un objet com qui peut recevoir à tout moment un événement WMI.</span><span class="sxs-lookup"><span data-stu-id="6a589-143">A [*permanent consumer*](gloss-p.md) is a COM object that can receive a WMI event at all times.</span></span> <span data-ttu-id="6a589-144">Un consommateur d’événements permanent utilise un ensemble d’objets et de filtres persistants pour capturer un événement WMI.</span><span class="sxs-lookup"><span data-stu-id="6a589-144">A permanent event consumer uses a set of persistent objects and filters to capture a WMI event.</span></span> <span data-ttu-id="6a589-145">À l’instar d’un consommateur d’événements temporaire, vous configurez une série d’objets WMI et de filtres qui capturent un événement WMI.</span><span class="sxs-lookup"><span data-stu-id="6a589-145">Like a temporary event consumer, you set up a series of WMI objects and filters that capture a WMI event.</span></span> <span data-ttu-id="6a589-146">Lorsqu’un événement qui correspond à un filtre est exécuté, WMI charge le consommateur d’événements permanent et le notifie à l’événement.</span><span class="sxs-lookup"><span data-stu-id="6a589-146">When an event occurs that matches a filter, WMI loads the permanent event consumer and notifies it about the event.</span></span> <span data-ttu-id="6a589-147">Étant donné qu’un consommateur permanent est implémenté dans l’espace de stockage WMI et qu’il s’agit d’un fichier exécutable enregistré dans WMI, le consommateur d’événements permanent opère et reçoit des événements après sa création et même après un redémarrage du système d’exploitation tant que WMI est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="6a589-147">Because a permanent consumer is implemented in the WMI repository and is an executable file that is registered in WMI, the permanent event consumer operates and receives events after it is created and even after a reboot of the operating system as long as WMI is running.</span></span> <span data-ttu-id="6a589-148">Pour plus d’informations, consultez [réception d’événements à tout moment](receiving-events-at-all-times.md).</span><span class="sxs-lookup"><span data-stu-id="6a589-148">For more information, see [Receiving Events at All Times](receiving-events-at-all-times.md).</span></span>

<span data-ttu-id="6a589-149">Les scripts ou les applications qui reçoivent des événements ont des considérations spéciales en matière de sécurité.</span><span class="sxs-lookup"><span data-stu-id="6a589-149">Scripts or applications that receive events have special security considerations.</span></span> <span data-ttu-id="6a589-150">Pour plus d’informations, consultez [sécurisation des événements WMI](securing-wmi-events.md).</span><span class="sxs-lookup"><span data-stu-id="6a589-150">For more information, see [Securing WMI Events](securing-wmi-events.md).</span></span>

<span data-ttu-id="6a589-151">Une application ou un script peut utiliser un fournisseur d’événements WMI intégré qui fournit des [classes de consommateur standard](standard-consumer-classes.md).</span><span class="sxs-lookup"><span data-stu-id="6a589-151">An application or script can use a built-in WMI event provider that supplies [standard consumer classes](standard-consumer-classes.md).</span></span> <span data-ttu-id="6a589-152">Chaque classe de consommateur standard répond à un événement avec une action différente en envoyant un message électronique ou en exécutant un script.</span><span class="sxs-lookup"><span data-stu-id="6a589-152">Each standard consumer class responds to an event with a different action by sending an email message or executing a script.</span></span> <span data-ttu-id="6a589-153">Vous n’avez pas besoin d’écrire du code fournisseur pour utiliser une classe de consommateur standard pour créer un consommateur d’événements permanent.</span><span class="sxs-lookup"><span data-stu-id="6a589-153">You do not have to write provider code to use a standard consumer class to create a permanent event consumer.</span></span> <span data-ttu-id="6a589-154">Pour plus d’informations, consultez [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="6a589-154">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

## <a name="providing-events"></a><span data-ttu-id="6a589-155">Fournir des événements</span><span class="sxs-lookup"><span data-stu-id="6a589-155">Providing Events</span></span>

<span data-ttu-id="6a589-156">Un fournisseur d’événements est un composant COM qui envoie un événement à WMI.</span><span class="sxs-lookup"><span data-stu-id="6a589-156">An event provider is a COM component that sends an event to WMI.</span></span> <span data-ttu-id="6a589-157">Vous pouvez créer un fournisseur d’événements pour envoyer un événement dans une application C++ ou C#.</span><span class="sxs-lookup"><span data-stu-id="6a589-157">You can create an event provider to send an event in a C++ or C# application.</span></span> <span data-ttu-id="6a589-158">La plupart des fournisseurs d’événements gèrent un objet pour WMI, par exemple, une application ou un élément matériel.</span><span class="sxs-lookup"><span data-stu-id="6a589-158">Most event providers manage an object for WMI, for example, an application or hardware item.</span></span> <span data-ttu-id="6a589-159">Pour plus d’informations, consultez [écriture d’un fournisseur d’événements](writing-an-event-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6a589-159">For more information, see [Writing an Event Provider](writing-an-event-provider.md).</span></span>

<span data-ttu-id="6a589-160">Un événement chronométré ou répété est un événement qui se produit à une heure prédéterminée.</span><span class="sxs-lookup"><span data-stu-id="6a589-160">A timed or repeating event is an event that occurs at a predetermined time.</span></span>

<span data-ttu-id="6a589-161">WMI offre les moyens suivants de créer des événements chronométrés ou répétitifs pour vos applications :</span><span class="sxs-lookup"><span data-stu-id="6a589-161">WMI provides the following ways to create timed or repeating events for your applications:</span></span>

-   <span data-ttu-id="6a589-162">L’infrastructure d’événements Microsoft standard.</span><span class="sxs-lookup"><span data-stu-id="6a589-162">The standard Microsoft event infrastructure.</span></span>
-   <span data-ttu-id="6a589-163">Classe de minuteur spécialisée.</span><span class="sxs-lookup"><span data-stu-id="6a589-163">A specialized timer class.</span></span>

<span data-ttu-id="6a589-164">Pour plus d’informations, consultez [réception d’un événement chronométré ou répétitif](receiving-a-timed-or-repeating-event.md).</span><span class="sxs-lookup"><span data-stu-id="6a589-164">For more information, see [Receiving a Timed or Repeating Event](receiving-a-timed-or-repeating-event.md).</span></span> <span data-ttu-id="6a589-165">Lorsque vous écrivez un fournisseur d’événements, tenez compte des informations de sécurité identifiées dans [fourniture sécurisée des événements](providing-events-securely.md).</span><span class="sxs-lookup"><span data-stu-id="6a589-165">When you write an event provider, consider the security information identified in [Providing Events Securely](providing-events-securely.md).</span></span>

<span data-ttu-id="6a589-166">Il est recommandé de compiler les abonnements d’événements permanents dans l’espace de noms de l' \\ \\ abonnement racine.</span><span class="sxs-lookup"><span data-stu-id="6a589-166">It is recommended that permanent event subscriptions be compiled into the \\root\\subscription namespace.</span></span> <span data-ttu-id="6a589-167">Pour plus d’informations, consultez [Implementing Cross-namespace permanent Event subscriptions](implementing-cross-namespace-permanent-event-subscriptions.md).</span><span class="sxs-lookup"><span data-stu-id="6a589-167">For more information, see [Implementing Cross-Namespace Permanent Event Subscriptions](implementing-cross-namespace-permanent-event-subscriptions.md).</span></span>

## <a name="subscription-quotas"></a><span data-ttu-id="6a589-168">Quotas d’abonnement</span><span class="sxs-lookup"><span data-stu-id="6a589-168">Subscription Quotas</span></span>

<span data-ttu-id="6a589-169">L’interrogation des événements peut nuire aux performances des fournisseurs qui prennent en charge les requêtes sur des jeux de données volumineux.</span><span class="sxs-lookup"><span data-stu-id="6a589-169">Polling for events can degrade performance for providers that support queries over huge data sets.</span></span> <span data-ttu-id="6a589-170">En outre, tout utilisateur disposant d’un accès en lecture à un espace de noms avec des fournisseurs dynamiques peut effectuer une attaque par déni de service (DoS).</span><span class="sxs-lookup"><span data-stu-id="6a589-170">Additionally, any user that has read access to a namespace with dynamic providers can perform a denial of service (DoS) attack.</span></span> <span data-ttu-id="6a589-171">WMI gère les quotas pour tous les utilisateurs combinés et pour chaque consommateur d’événements dans l’instance unique de [**\_ \_ ArbitratorConfiguration**](--arbitratorconfiguration.md) située dans l' \\ espace de noms racine.</span><span class="sxs-lookup"><span data-stu-id="6a589-171">WMI maintains quotas for all of the users combined and for each event consumer in the single instance of [**\_\_ArbitratorConfiguration**](--arbitratorconfiguration.md) located in the \\root namespace.</span></span> <span data-ttu-id="6a589-172">Ces quotas sont globaux plutôt que pour chaque espace de noms.</span><span class="sxs-lookup"><span data-stu-id="6a589-172">These quotas are global rather than for each namespace.</span></span> <span data-ttu-id="6a589-173">Vous ne pouvez pas modifier les quotas.</span><span class="sxs-lookup"><span data-stu-id="6a589-173">You cannot change the quotas.</span></span>

<span data-ttu-id="6a589-174">WMI applique actuellement des quotas à l’aide des propriétés de [**\_ \_ ArbitratorConfiguration**](--arbitratorconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="6a589-174">WMI currently enforces quotas using the properties of [**\_\_ArbitratorConfiguration**](--arbitratorconfiguration.md).</span></span> <span data-ttu-id="6a589-175">Chaque quota a un par utilisateur et une version totale qui inclut tous les utilisateurs combinés, et non par espace de noms.</span><span class="sxs-lookup"><span data-stu-id="6a589-175">Each quota has a per user and a total version that includes all users combined, not per namespace.</span></span> <span data-ttu-id="6a589-176">Le tableau suivant répertorie les quotas qui s’appliquent aux propriétés **\_ \_ ArbitratorConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="6a589-176">The following table lists the quotas that apply to the **\_\_ArbitratorConfiguration** properties.</span></span>



| <span data-ttu-id="6a589-177">Total/PerUser</span><span class="sxs-lookup"><span data-stu-id="6a589-177">Total/PerUser</span></span>                                                                   | <span data-ttu-id="6a589-178">Quota</span><span class="sxs-lookup"><span data-stu-id="6a589-178">Quota</span></span>                                                                       |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="6a589-179">TemporarySubscriptionsTotal</span><span class="sxs-lookup"><span data-stu-id="6a589-179">TemporarySubscriptionsTotal</span></span><br/> <span data-ttu-id="6a589-180">TemporarySubscriptionsPerUser</span><span class="sxs-lookup"><span data-stu-id="6a589-180">TemporarySubscriptionsPerUser</span></span><br/> | <span data-ttu-id="6a589-181">10 000</span><span class="sxs-lookup"><span data-stu-id="6a589-181">10,000</span></span><br/> <span data-ttu-id="6a589-182">1 000</span><span class="sxs-lookup"><span data-stu-id="6a589-182">1,000</span></span><br/>                                          |
| <span data-ttu-id="6a589-183">PermanentSubscriptionsTotal</span><span class="sxs-lookup"><span data-stu-id="6a589-183">PermanentSubscriptionsTotal</span></span><br/> <span data-ttu-id="6a589-184">PermanentSubscriptionsPerUser</span><span class="sxs-lookup"><span data-stu-id="6a589-184">PermanentSubscriptionsPerUser</span></span><br/> | <span data-ttu-id="6a589-185">10 000</span><span class="sxs-lookup"><span data-stu-id="6a589-185">10,000</span></span><br/> <span data-ttu-id="6a589-186">1 000</span><span class="sxs-lookup"><span data-stu-id="6a589-186">1,000</span></span><br/>                                          |
| <span data-ttu-id="6a589-187">PollingInstructionsTotal</span><span class="sxs-lookup"><span data-stu-id="6a589-187">PollingInstructionsTotal</span></span><br/> <span data-ttu-id="6a589-188">PollingInstructionsPerUser</span><span class="sxs-lookup"><span data-stu-id="6a589-188">PollingInstructionsPerUser</span></span><br/>       | <span data-ttu-id="6a589-189">10 000</span><span class="sxs-lookup"><span data-stu-id="6a589-189">10,000</span></span><br/> <span data-ttu-id="6a589-190">1 000</span><span class="sxs-lookup"><span data-stu-id="6a589-190">1,000</span></span><br/>                                          |
| <span data-ttu-id="6a589-191">PollingMemoryTotal</span><span class="sxs-lookup"><span data-stu-id="6a589-191">PollingMemoryTotal</span></span><br/> <span data-ttu-id="6a589-192">PollingMemoryPerUser</span><span class="sxs-lookup"><span data-stu-id="6a589-192">PollingMemoryPerUser</span></span><br/>                   | <span data-ttu-id="6a589-193">10 millions (0x989680) octets</span><span class="sxs-lookup"><span data-stu-id="6a589-193">10,000,000 (0x989680) bytes</span></span><br/> <span data-ttu-id="6a589-194">5 millions (0x4CB40) octets</span><span class="sxs-lookup"><span data-stu-id="6a589-194">5,000,000 (0x4CB40) bytes</span></span><br/> |



 

<span data-ttu-id="6a589-195">Un administrateur ou un utilisateur disposant d’une autorisation en **\_ écriture totale** dans l’espace de noms peut modifier l’instance singleton de [**\_ \_ ArbitratorConfiguration**](--arbitratorconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="6a589-195">An administrator or a user with **FULL\_WRITE** permission in the namespace can modify the singleton instance of [**\_\_ArbitratorConfiguration**](--arbitratorconfiguration.md).</span></span> <span data-ttu-id="6a589-196">WMI effectue le suivi du quota par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6a589-196">WMI tracks the per-user quota.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a589-197">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6a589-197">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a589-198">Utilisation de WMI</span><span class="sxs-lookup"><span data-stu-id="6a589-198">Using WMI</span></span>](using-wmi.md)
</dt> </dl>

 

