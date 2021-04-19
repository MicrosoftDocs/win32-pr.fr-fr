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
# <a name="receiving-asynchronous-event-notifications"></a><span data-ttu-id="2598c-103">Réception des notifications d’événements asynchrones</span><span class="sxs-lookup"><span data-stu-id="2598c-103">Receiving Asynchronous Event Notifications</span></span>

<span data-ttu-id="2598c-104">La notification d’événements asynchrone est une technique qui permet à une application de surveiller en permanence les événements sans monopoliser les ressources système.</span><span class="sxs-lookup"><span data-stu-id="2598c-104">Asynchronous event notification is a technique that allows an application to constantly monitor events without monopolizing system resources.</span></span> <span data-ttu-id="2598c-105">Les notifications d’événements asynchrones ont les mêmes restrictions de sécurité que les autres appels asynchrones.</span><span class="sxs-lookup"><span data-stu-id="2598c-105">Asynchronous event notifications have the same security limitations that other asynchronous calls have.</span></span> <span data-ttu-id="2598c-106">Vous pouvez effectuer des appels semi-synchrones à la place.</span><span class="sxs-lookup"><span data-stu-id="2598c-106">You can make semisynchronous calls instead.</span></span> <span data-ttu-id="2598c-107">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="2598c-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="2598c-108">La file d’attente des événements asynchrones routés vers un client a le potentiel de croître de manière exceptionnellement importante.</span><span class="sxs-lookup"><span data-stu-id="2598c-108">The queue of asynchronous events routed to a client has the potential to grow exceptionally large.</span></span> <span data-ttu-id="2598c-109">Par conséquent, WMI implémente une stratégie à l’ensemble du système pour éviter de manquer de mémoire.</span><span class="sxs-lookup"><span data-stu-id="2598c-109">Therefore, WMI implements a system-wide policy to avoid running out of memory.</span></span> <span data-ttu-id="2598c-110">WMI ralentit les événements ou commence à supprimer des événements de la file d’attente lorsque la file d’attente dépasse une certaine taille.</span><span class="sxs-lookup"><span data-stu-id="2598c-110">WMI either slows down events, or starts dropping events from the queue when the queue grows past a certain size.</span></span>

<span data-ttu-id="2598c-111">WMI utilise les propriétés [**LowThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) et [**HighThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) de la classe [**Win32 \_ WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) pour définir des limites en cas d’évitement de mémoire.</span><span class="sxs-lookup"><span data-stu-id="2598c-111">WMI uses the [**LowThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) and [**HighThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) properties of the [**Win32\_WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) class to set limits on out-of-memory avoidance.</span></span> <span data-ttu-id="2598c-112">La valeur minimale indique que WMI doit commencer à ralentir la notification d’événements, et la valeur maximale indique quand commencer à supprimer des événements.</span><span class="sxs-lookup"><span data-stu-id="2598c-112">The minimum value indicates when WMI should start slowing event notification, and the maximum value indicates when to start dropping events.</span></span> <span data-ttu-id="2598c-113">Les valeurs par défaut pour les seuils inférieur et supérieur sont 1 million (10 Mo) et 2 millions (20 Mo).</span><span class="sxs-lookup"><span data-stu-id="2598c-113">The default values for the low and high thresholds are 1000000 (10 MB) and 2000000 (20 MB).</span></span> <span data-ttu-id="2598c-114">En outre, vous pouvez définir la propriété [**MaxWaitOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) pour décrire la durée d’attente de WMI avant de supprimer des événements.</span><span class="sxs-lookup"><span data-stu-id="2598c-114">In addition, you can set the [**MaxWaitOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) property to describe the amount of time WMI should wait before dropping events.</span></span> <span data-ttu-id="2598c-115">La valeur par défaut de **MaxWaitOnEvents** est 2000, ou 2 secondes.</span><span class="sxs-lookup"><span data-stu-id="2598c-115">The default value for **MaxWaitOnEvents** is 2000, or 2 seconds.</span></span>

## <a name="receiving-asynchronous-event-notifications-in-vbscript"></a><span data-ttu-id="2598c-116">Réception de notifications d’événements asynchrones dans VBScript</span><span class="sxs-lookup"><span data-stu-id="2598c-116">Receiving Asynchronous Event Notifications in VBScript</span></span>

<span data-ttu-id="2598c-117">Les appels de script pour recevoir des notifications d’événements sont essentiellement les mêmes que tous les appels asynchrones ayant les mêmes problèmes de sécurité.</span><span class="sxs-lookup"><span data-stu-id="2598c-117">The scripting calls to receive event notifications are essentially the same as all asynchronous calls with the same security issues.</span></span> <span data-ttu-id="2598c-118">Pour plus d’informations, consultez [création d’un appel asynchrone avec VBScript](making-an-asynchronous-call-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="2598c-118">For more information, see [Making an Asynchronous Call with VBScript](making-an-asynchronous-call-with-vbscript.md).</span></span>

<span data-ttu-id="2598c-119">**Pour recevoir des notifications d’événements asynchrones dans VBScript**</span><span class="sxs-lookup"><span data-stu-id="2598c-119">**To receive asynchronous event notifications in VBScript**</span></span>

1.  <span data-ttu-id="2598c-120">Créez un objet récepteur en appelant [Wscript. CreateObject](/previous-versions//xzysf6hc(v=vs.85)) et en spécifiant le ProgID de « WbemScripting » et le type d’objet [**SWbemSink**](swbemsink.md).</span><span class="sxs-lookup"><span data-stu-id="2598c-120">Create a sink object by calling [WScript.CreateObject](/previous-versions//xzysf6hc(v=vs.85)) and specifying the progid of "WbemScripting" and the object type of [**SWbemSink**](swbemsink.md).</span></span> <span data-ttu-id="2598c-121">L’objet récepteur reçoit les notifications.</span><span class="sxs-lookup"><span data-stu-id="2598c-121">The sink object receives the notifications.</span></span>
2.  <span data-ttu-id="2598c-122">Écrivez une sous-routine pour chaque événement que vous souhaitez gérer.</span><span class="sxs-lookup"><span data-stu-id="2598c-122">Write a subroutine for each event you want to handle.</span></span> <span data-ttu-id="2598c-123">Le tableau suivant répertorie les événements [**SWbemSink**](swbemsink.md) .</span><span class="sxs-lookup"><span data-stu-id="2598c-123">The following table lists the [**SWbemSink**](swbemsink.md) events.</span></span>

    

    | <span data-ttu-id="2598c-124">Événement</span><span class="sxs-lookup"><span data-stu-id="2598c-124">Event</span></span>                                            | <span data-ttu-id="2598c-125">Signification</span><span class="sxs-lookup"><span data-stu-id="2598c-125">Meaning</span></span>                                                                                                                         |
    |--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
    | [<span data-ttu-id="2598c-126">**OnObjectReady**</span><span class="sxs-lookup"><span data-stu-id="2598c-126">**OnObjectReady**</span></span>](swbemsink-onobjectready.md) | <span data-ttu-id="2598c-127">Signale le retour d’un objet au récepteur.</span><span class="sxs-lookup"><span data-stu-id="2598c-127">Reports the returns of an object to the sink.</span></span> <span data-ttu-id="2598c-128">L’utilisation de cet appel retourne un objet chaque fois que l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="2598c-128">Using this call returns one object each time until the operation is complete.</span></span>     |
    | [<span data-ttu-id="2598c-129">**OnCompleted**</span><span class="sxs-lookup"><span data-stu-id="2598c-129">**OnCompleted**</span></span>](swbemsink-oncompleted.md)     | <span data-ttu-id="2598c-130">Signale quand un appel asynchrone est terminé.</span><span class="sxs-lookup"><span data-stu-id="2598c-130">Reports when an asynchronous call is complete.</span></span> <span data-ttu-id="2598c-131">Cet événement ne se produit jamais si l’opération est indéfinie.</span><span class="sxs-lookup"><span data-stu-id="2598c-131">This event never occurs if the operation is indefinite.</span></span>                          |
    | [<span data-ttu-id="2598c-132">**OnObjectPut**</span><span class="sxs-lookup"><span data-stu-id="2598c-132">**OnObjectPut**</span></span>](swbemsink-onobjectput.md)     | <span data-ttu-id="2598c-133">Signale l’achèvement d’une opération put asynchrone.</span><span class="sxs-lookup"><span data-stu-id="2598c-133">Reports the completion of an asynchronous put operation.</span></span> <span data-ttu-id="2598c-134">Cet événement retourne le chemin d’accès de l’objet de l’instance ou de la classe enregistrée.</span><span class="sxs-lookup"><span data-stu-id="2598c-134">This event returns the object path of the instance or the saved class.</span></span> |
    | [<span data-ttu-id="2598c-135">**OnProgress**</span><span class="sxs-lookup"><span data-stu-id="2598c-135">**OnProgress**</span></span>](swbemsink-onprogress.md)       | <span data-ttu-id="2598c-136">Signale l’état d’un appel asynchrone en cours.</span><span class="sxs-lookup"><span data-stu-id="2598c-136">Reports the status of an asynchronous call that is in progress.</span></span> <span data-ttu-id="2598c-137">Tous les fournisseurs ne prennent pas en charge les rapports de progression temporaires.</span><span class="sxs-lookup"><span data-stu-id="2598c-137">Not all providers support interim progress reports.</span></span>             |
    | [<span data-ttu-id="2598c-138">**Annuler**</span><span class="sxs-lookup"><span data-stu-id="2598c-138">**Cancel**</span></span>](swbemsink-cancel.md)               | <span data-ttu-id="2598c-139">Annule toutes les opérations asynchrones en suspens associées à ce récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="2598c-139">Cancels all of the outstanding asynchronous operations associated with this object sink.</span></span>                                        |

    

     

<span data-ttu-id="2598c-140">L’exemple de code VBScript suivant indique la suppression des processus avec un intervalle d’interrogation de 10 secondes.</span><span class="sxs-lookup"><span data-stu-id="2598c-140">The following VBScript code example notifies the deletion of processes with a 10 second polling interval.</span></span> <span data-ttu-id="2598c-141">Dans ce script, le récepteur de sous-routine \_ OnObjectReady gère l’occurrence de l’événement.</span><span class="sxs-lookup"><span data-stu-id="2598c-141">In this script, the subroutine SINK\_OnObjectReady handles the event occurrence.</span></span> <span data-ttu-id="2598c-142">Dans l’exemple, l’objet récepteur est nommé « sink », mais vous pouvez nommer cet objet comme vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="2598c-142">In the example, the sink object is named "Sink", however you can name this object as you choose.</span></span>


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



## <a name="receiving-asynchronous-event-notifications-in-c"></a><span data-ttu-id="2598c-143">Réception de notifications d’événements asynchrones en C++</span><span class="sxs-lookup"><span data-stu-id="2598c-143">Receiving Asynchronous Event Notifications in C++</span></span>

<span data-ttu-id="2598c-144">Pour exécuter une notification asynchrone, vous créez un thread distinct uniquement pour surveiller et recevoir des événements à partir d’Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="2598c-144">To perform asynchronous notification, you create a separate thread solely to monitor and receive events from Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="2598c-145">Lorsque ce thread reçoit un message, le thread notifie votre application principale.</span><span class="sxs-lookup"><span data-stu-id="2598c-145">When that thread receives a message, the thread notifies your main application.</span></span>

<span data-ttu-id="2598c-146">En dédiant un thread distinct, vous autorisez votre processus principal à exécuter d’autres activités en attendant l’arrivée d’un événement.</span><span class="sxs-lookup"><span data-stu-id="2598c-146">By dedicating a separate thread, you permit your main process to perform other activities while waiting for an event to arrive.</span></span> <span data-ttu-id="2598c-147">La remise asynchrone des notifications améliore les performances, mais peut fournir moins de sécurité que vous ne le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="2598c-147">Asynchronous delivery of notifications improves performance but may provide less security than you want.</span></span> <span data-ttu-id="2598c-148">En C++, vous avez la possibilité d’utiliser l’interface [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) ou d’effectuer des vérifications d’accès sur les descripteurs de sécurité.</span><span class="sxs-lookup"><span data-stu-id="2598c-148">In C++, you have the option of using the [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) interface or performing access checks on security descriptors.</span></span> <span data-ttu-id="2598c-149">Pour plus d’informations, consultez [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="2598c-149">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="2598c-150">**Pour configurer des notifications d’événements asynchrones**</span><span class="sxs-lookup"><span data-stu-id="2598c-150">**To set up asynchronous event notifications**</span></span>

1.  <span data-ttu-id="2598c-151">Avant d’initialiser des notifications asynchrones, assurez-vous que vos paramètres d’évitement de mémoire sont correctement définis dans [**Win32 \_ WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting).</span><span class="sxs-lookup"><span data-stu-id="2598c-151">Before initializing any asynchronous notifications, ensure your out-of-memory avoidance parameters are set correctly in [**Win32\_WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting).</span></span>

2.  <span data-ttu-id="2598c-152">Déterminez le type d’événement que vous souhaitez recevoir.</span><span class="sxs-lookup"><span data-stu-id="2598c-152">Determine what kind of events you want to receive.</span></span>

    <span data-ttu-id="2598c-153">WMI prend en charge les événements intrinsèques et extrinsèques.</span><span class="sxs-lookup"><span data-stu-id="2598c-153">WMI supports intrinsic and extrinsic events.</span></span> <span data-ttu-id="2598c-154">Un événement intrinsèque est un événement prédéfini par WMI, alors qu’un événement extrinsèque est un événement défini par un fournisseur tiers.</span><span class="sxs-lookup"><span data-stu-id="2598c-154">An intrinsic event is an event predefined by WMI, whereas an extrinsic event is an event defined by a third party provider.</span></span> <span data-ttu-id="2598c-155">Pour plus d’informations, consultez [détermination du type d’événement à recevoir](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="2598c-155">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="2598c-156">La procédure suivante décrit comment recevoir des notifications d’événements asynchrones en C++.</span><span class="sxs-lookup"><span data-stu-id="2598c-156">The following procedure describes how to receive asynchronous event notifications in C++.</span></span>

<span data-ttu-id="2598c-157">**Pour recevoir des notifications d’événements asynchrones en C++**</span><span class="sxs-lookup"><span data-stu-id="2598c-157">**To receive asynchronous event notifications in C++**</span></span>

1.  <span data-ttu-id="2598c-158">Configurez votre application avec des appels aux fonctions [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) et [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .</span><span class="sxs-lookup"><span data-stu-id="2598c-158">Set up your application with calls to the [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) functions.</span></span>

    <span data-ttu-id="2598c-159">L’appel de [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) Initialise com, tandis que [**COINITIALIZESECURITY**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) accorde à WMI l’autorisation d’appeler le processus du consommateur.</span><span class="sxs-lookup"><span data-stu-id="2598c-159">Calling [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) initializes COM, while [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) grants WMI the permission to call into the process of the consumer.</span></span> <span data-ttu-id="2598c-160">La fonction **CoInitializeEx** vous donne également la possibilité de programmer une application multithread, ce qui est nécessaire pour la notification asynchrone.</span><span class="sxs-lookup"><span data-stu-id="2598c-160">The **CoInitializeEx** function also grants you the ability to program a multithreaded application, which is necessary for asynchronous notification.</span></span> <span data-ttu-id="2598c-161">Pour plus d’informations, consultez [maintenance de la sécurité WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="2598c-161">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

    <span data-ttu-id="2598c-162">Le code de cette rubrique requiert les références suivantes et les \# instructions include pour être compilées correctement.</span><span class="sxs-lookup"><span data-stu-id="2598c-162">The code in this topic requires the following references and \#include statements to compile correctly.</span></span>

    ```C++
    #define _WIN32_DCOM
    #include <iostream>
    using namespace std;
    #include <wbemidl.h>
    ```

    

    <span data-ttu-id="2598c-163">L’exemple de code suivant décrit comment configurer le consommateur d’événements temporaires avec des appels à [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) et [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="2598c-163">The following code example describes how to set up the temporary event consumer with calls to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

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

    

2.  <span data-ttu-id="2598c-164">Créez un objet récepteur par le biais de l’interface [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="2598c-164">Create a sink object through the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

    <span data-ttu-id="2598c-165">WMI utilise [**IWbemObjectSink**](iwbemobjectsink.md) pour envoyer des notifications d’événements et signaler l’état d’une opération asynchrone ou d’une notification d’événement.</span><span class="sxs-lookup"><span data-stu-id="2598c-165">WMI uses [**IWbemObjectSink**](iwbemobjectsink.md) to send event notifications and to report status on an asynchronous operation or event notification.</span></span>

3.  <span data-ttu-id="2598c-166">Inscrivez votre consommateur d’événements à l’aide d’un appel à la méthode [**IWbemServices :: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) .</span><span class="sxs-lookup"><span data-stu-id="2598c-166">Register your event consumer with a call to the [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) method.</span></span>

    <span data-ttu-id="2598c-167">Assurez-vous que le paramètre *pResponseHandler* pointe vers l’objet récepteur créé à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="2598c-167">Make sure that the *pResponseHandler* parameter points to the sink object created in the preceding step.</span></span>

    <span data-ttu-id="2598c-168">L’objectif de l’inscription est de recevoir uniquement les notifications requises.</span><span class="sxs-lookup"><span data-stu-id="2598c-168">The purpose of registration is to receive only the required notifications.</span></span> <span data-ttu-id="2598c-169">La réception de notifications superflues gaspille le traitement et la remise du temps ; et n’utilise pas la fonctionnalité de filtrage de WMI pour obtenir le potentiel le plus complet possible.</span><span class="sxs-lookup"><span data-stu-id="2598c-169">Receiving superfluous notifications wastes processing and delivery time; and does not use the filtering ability of WMI to the fullest potential.</span></span>

    <span data-ttu-id="2598c-170">Toutefois, un consommateur temporaire peut recevoir plus d’un type d’événement.</span><span class="sxs-lookup"><span data-stu-id="2598c-170">However, a temporary consumer can receive more than one type of event.</span></span> <span data-ttu-id="2598c-171">Dans ce cas, un consommateur temporaire doit effectuer des appels distincts à [**IWbemServices :: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) pour chaque type d’événement.</span><span class="sxs-lookup"><span data-stu-id="2598c-171">In this case, a temporary consumer must make separate calls to [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) for each event type.</span></span> <span data-ttu-id="2598c-172">Par exemple, un consommateur peut nécessiter une notification lorsque de nouveaux processus sont créés (un événement de création d’instance ou [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)) et des modifications à certaines clés de Registre (un événement de registre tel que [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)).</span><span class="sxs-lookup"><span data-stu-id="2598c-172">For example, a consumer might require notification when new processes are created (an instance creation event or [**\_\_InstanceCreationEvent**](--instancecreationevent.md)) and for changes to certain registry keys (a registry event such as [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)).</span></span> <span data-ttu-id="2598c-173">Par conséquent, le consommateur effectue un appel à [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) pour s’inscrire aux événements de création d’instance et un autre appel à **ExecNotificationQueryAsync** pour s’inscrire aux événements de registre.</span><span class="sxs-lookup"><span data-stu-id="2598c-173">Therefore, the consumer makes one call to [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) to register for instance creation events and another call to **ExecNotificationQueryAsync** to register for registry events.</span></span>

    <span data-ttu-id="2598c-174">Si vous choisissez de créer un consommateur d’événements qui s’inscrit pour plusieurs événements, vous devez éviter d’inscrire plusieurs classes avec le même récepteur.</span><span class="sxs-lookup"><span data-stu-id="2598c-174">If you choose to create an event consumer that registers for multiple events, you should avoid registering multiple classes with the same sink.</span></span> <span data-ttu-id="2598c-175">Utilisez plutôt un récepteur distinct pour chaque classe d’événements inscrits.</span><span class="sxs-lookup"><span data-stu-id="2598c-175">Instead, use a separate sink for each class of registered event.</span></span> <span data-ttu-id="2598c-176">Le fait de disposer d’un récepteur dédié simplifie le traitement et les aides en maintenance, ce qui vous permet d’annuler une inscription sans affecter les autres.</span><span class="sxs-lookup"><span data-stu-id="2598c-176">Having a dedicated sink simplifies processing and aids in maintenance, allowing you to cancel one registration without affecting the others.</span></span>

4.  <span data-ttu-id="2598c-177">Effectuez les activités nécessaires dans votre consommateur d’événements.</span><span class="sxs-lookup"><span data-stu-id="2598c-177">Perform any necessary activities in your event consumer.</span></span>

    <span data-ttu-id="2598c-178">Cette étape doit contenir la majeure partie de votre code et inclure des activités telles que l’affichage des événements dans une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2598c-178">This step should contain most of your code and include such activities as displaying events to a user interface.</span></span>

5.  <span data-ttu-id="2598c-179">Lorsque vous avez terminé, annulez l’inscription du consommateur d’événements temporaires avec un appel à l’événement [**IWbemServices :: CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) .</span><span class="sxs-lookup"><span data-stu-id="2598c-179">When finished, unregister the temporary event consumer with a call to the [**IWbemServices::CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) event.</span></span>

    <span data-ttu-id="2598c-180">Que l’appel à [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) réussisse ou échoue, ne supprimez pas l’objet récepteur tant que le nombre de références d’objet n’atteint pas zéro.</span><span class="sxs-lookup"><span data-stu-id="2598c-180">Regardless of whether the call to [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) succeeds or fails, do not delete the sink object until the object reference count reaches zero.</span></span> <span data-ttu-id="2598c-181">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="2598c-181">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

 
