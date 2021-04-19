---
description: Utilisez SWbemServices.ExecQuery pour demander tous les événements existants.
ms.assetid: bc99719a-7e33-4e2d-8355-f8fc97c66f71
ms.tgt_platform: multiple
title: Réception des notifications d’événements synchrones et semi-synchrones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15327c66f7ba3e59824c94d54a206ec348c85952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520609"
---
# <a name="receiving-synchronous-and-semisynchronous-event-notifications"></a><span data-ttu-id="5aac7-103">Réception des notifications d’événements synchrones et semi-synchrones</span><span class="sxs-lookup"><span data-stu-id="5aac7-103">Receiving Synchronous and Semisynchronous Event Notifications</span></span>

<span data-ttu-id="5aac7-104">Utilisez [**SWbemServices.ExecQuery**](swbemservices-execquery.md) pour demander tous les événements existants.</span><span class="sxs-lookup"><span data-stu-id="5aac7-104">Use [**SWbemServices.ExecQuery**](swbemservices-execquery.md) to request all existing events.</span></span>

<span data-ttu-id="5aac7-105">L’exemple de code suivant montre comment interroger les événements d’un journal.</span><span class="sxs-lookup"><span data-stu-id="5aac7-105">The following code example shows how to query for the events in a log.</span></span>

`Select * from Win32_NTLogEvent`

<span data-ttu-id="5aac7-106">Pour plus d’informations, consultez [déterminer le type d’événement à recevoir](determining-the-type-of-event-to-receive.md), recevoir [des notifications d’événements](receiving-event-notifications.md)et [WQL (SQL pour WMI)](wql-sql-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="5aac7-106">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md), [Receiving Event Notifications](receiving-event-notifications.md), and [WQL (SQL for WMI)](wql-sql-for-wmi.md).</span></span>

<span data-ttu-id="5aac7-107">L’appel par défaut à [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) utilise la communication semi-synchrone.</span><span class="sxs-lookup"><span data-stu-id="5aac7-107">The default call to [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) uses semisynchronous communication.</span></span> <span data-ttu-id="5aac7-108">Les indicateurs **wbemFlagForwardOnly** et **wbemFlagReturnImmediately** sont définis par défaut pour le paramètre *IFlags* .</span><span class="sxs-lookup"><span data-stu-id="5aac7-108">The *iflags* parameter has the **wbemFlagForwardOnly** and **wbemFlagReturnImmediately** flags set by default.</span></span> <span data-ttu-id="5aac7-109">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="5aac7-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="5aac7-110">La procédure suivante décrit comment recevoir une notification d’événements semi-synchrone à l’aide de VBScript.</span><span class="sxs-lookup"><span data-stu-id="5aac7-110">The following procedure describes how to receive semisynchronous event notification using VBScript.</span></span>

<span data-ttu-id="5aac7-111">**Pour recevoir une notification d’événements semi-synchrone dans VBScript**</span><span class="sxs-lookup"><span data-stu-id="5aac7-111">**To receive semisynchronous event notification in VBScript**</span></span>

1.  <span data-ttu-id="5aac7-112">Créez une requête pour le type d’événement que vous souhaitez recevoir.</span><span class="sxs-lookup"><span data-stu-id="5aac7-112">Create a query for the type of event that you want to receive.</span></span> <span data-ttu-id="5aac7-113">Pour plus d’informations, consultez [détermination du type d’événement à recevoir](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="5aac7-113">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

2.  <span data-ttu-id="5aac7-114">Si vous demandez un type d’instance d’événement tel que [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md), indiquez dans la requête un type d’instance cible, par exemple [**, \_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span><span class="sxs-lookup"><span data-stu-id="5aac7-114">If you request an instance type of event such as [**\_\_InstanceCreationEvent**](--instancecreationevent.md), indicate in the query a type of target instance, for example, [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span></span>

3.  <span data-ttu-id="5aac7-115">Si nécessaire, spécifiez une instance, par exemple, le nom d’un espace de noms lors de la demande de futures instances [**\_ \_ NamespaceModificationEvent**](--namespacemodificationevent.md) pour un espace de noms spécifique.</span><span class="sxs-lookup"><span data-stu-id="5aac7-115">If necessary, specify an instance, for example, the name of a namespace when requesting future [**\_\_NamespaceModificationEvent**](--namespacemodificationevent.md) instances for a specific namespace.</span></span>

4.  <span data-ttu-id="5aac7-116">Spécifiez une fréquence d’interrogation de Windows Management Instrumentation (WMI) dans une requête, telle que « dans les 10 », pour interroger toutes les 10 secondes.</span><span class="sxs-lookup"><span data-stu-id="5aac7-116">Specify a polling interval for Windows Management Instrumentation (WMI) in a query, such as "WITHIN 10"—to poll every 10 seconds.</span></span> <span data-ttu-id="5aac7-117">Pour plus d’informations, consultez [dans la clause in](within-clause.md).</span><span class="sxs-lookup"><span data-stu-id="5aac7-117">For more information, see [WITHIN Clause](within-clause.md).</span></span>

5.  <span data-ttu-id="5aac7-118">Appelez [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) à l’aide de la requête.</span><span class="sxs-lookup"><span data-stu-id="5aac7-118">Call [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) using the query.</span></span>

6.  <span data-ttu-id="5aac7-119">Parcourez la collection que vous recevez.</span><span class="sxs-lookup"><span data-stu-id="5aac7-119">Loop through the collection you receive.</span></span>

<span data-ttu-id="5aac7-120">L’exemple suivant montre comment surveiller l’insertion et la suppression de disques à partir d’un lecteur de disquette sur un ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="5aac7-120">The following example shows how to monitor insertion and removal of disks from a floppy disk drive on a local machine.</span></span> <span data-ttu-id="5aac7-121">Le script demande \_ des instances [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md) pour l’instance [**disque \_ logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) du lecteur de disquette et interroge toutes les 10 secondes les nouvelles instances.</span><span class="sxs-lookup"><span data-stu-id="5aac7-121">The script requests \_[**\_\_InstanceModificationEvent**](--instancemodificationevent.md) instances for the floppy drive [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) instance and polls every 10 seconds for new instances.</span></span> <span data-ttu-id="5aac7-122">Ce script est un exemple de consommateur d’événements temporaire et continue de s’exécuter jusqu’à ce qu’il soit arrêté dans le gestionnaire des tâches ou que le système soit redémarré.</span><span class="sxs-lookup"><span data-stu-id="5aac7-122">This script is an example of a temporary event consumer, and continues running until it is stopped in Task Manager or the system is rebooted.</span></span> <span data-ttu-id="5aac7-123">Pour plus d’informations, consultez [réception d’événements pendant la durée de votre application](receiving-events-for-the-duration-of-your-application.md).</span><span class="sxs-lookup"><span data-stu-id="5aac7-123">For more information, see [Receiving Events for the Duration of your Application](receiving-events-for-the-duration-of-your-application.md).</span></span>


```VB
Const FLOPPY_DISK = 2
Set colMonitoredDisks = GetObject("Winmgmts:").ExecNotificationQuery _
    ("Select * from __InstanceModificationEvent within 10 WHERE " _
        & "TargetInstance ISA 'Win32_LogicalDisk'")
i = 0
Do While i = 0
    Set strDiskChange = colMonitoredDisks.NextEvent
    If strDiskChange.TargetInstance.DriveType = FLOPPY_DISK Then
        If strDiskChange.TargetInstance.Size > 0 Then
            Wscript.Echo "A disk has been inserted" & _
                " into the floppy drive."
    Else
            Wscript.Echo "A disk has been removed" & _
                " from the floppy drive."
        End If
    End If
Loop
```



<span data-ttu-id="5aac7-124">La procédure suivante décrit comment recevoir une notification d’événements semi-synchrone à l’aide de C++.</span><span class="sxs-lookup"><span data-stu-id="5aac7-124">The following procedure describes how to receive semisynchronous event notification using C++.</span></span>

<span data-ttu-id="5aac7-125">**Pour recevoir une notification d’événements semi-synchrone en C++**</span><span class="sxs-lookup"><span data-stu-id="5aac7-125">**To receive semisynchronous event notification in C++**</span></span>

1.  <span data-ttu-id="5aac7-126">Configurez l’application avec des appels aux fonctions [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) et [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .</span><span class="sxs-lookup"><span data-stu-id="5aac7-126">Set up the application with calls to the [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) functions.</span></span>

    <span data-ttu-id="5aac7-127">Étant donné que WMI est basé sur COM, l’appel de [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) et de [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) est une étape obligatoire pour une application WMI.</span><span class="sxs-lookup"><span data-stu-id="5aac7-127">Because WMI is COM based, calling [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) is a required step for a WMI application.</span></span> <span data-ttu-id="5aac7-128">Pour plus d’informations, consultez [création d’une application ou d’un script WMI](creating-a-wmi-application-or-script.md).</span><span class="sxs-lookup"><span data-stu-id="5aac7-128">For more information, see [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span>

2.  <span data-ttu-id="5aac7-129">Déterminez le type d’événement que vous souhaitez recevoir.</span><span class="sxs-lookup"><span data-stu-id="5aac7-129">Determine the kind of events that you want to receive.</span></span>

    <span data-ttu-id="5aac7-130">WMI prend en charge les événements intrinsèques et extrinsèques.</span><span class="sxs-lookup"><span data-stu-id="5aac7-130">WMI supports intrinsic and extrinsic events.</span></span> <span data-ttu-id="5aac7-131">Un événement intrinsèque est un événement prédéfini par WMI.</span><span class="sxs-lookup"><span data-stu-id="5aac7-131">An intrinsic event is an event predefined by WMI.</span></span> <span data-ttu-id="5aac7-132">Un événement extrinsèque est un événement défini par un fournisseur tiers.</span><span class="sxs-lookup"><span data-stu-id="5aac7-132">An extrinsic event is an event defined by a third party provider.</span></span> <span data-ttu-id="5aac7-133">Pour plus d’informations, consultez [détermination du type d’événement à recevoir](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="5aac7-133">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

3.  <span data-ttu-id="5aac7-134">Inscrivez-vous pour recevoir une classe spécifique d’événements avec un appel à la méthode [**IWbemServices :: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) .</span><span class="sxs-lookup"><span data-stu-id="5aac7-134">Register to receive a specific class of events with a call to the [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) method.</span></span>

    <span data-ttu-id="5aac7-135">Rendez chaque requête très spécifique.</span><span class="sxs-lookup"><span data-stu-id="5aac7-135">Make each query very specific.</span></span> <span data-ttu-id="5aac7-136">L’objectif de l’inscription est de s’inscrire pour recevoir uniquement les notifications requises.</span><span class="sxs-lookup"><span data-stu-id="5aac7-136">The goal of registration is to register to receive only the required notifications.</span></span> <span data-ttu-id="5aac7-137">Notifications qui ne sont pas requises pour le traitement et le temps de remise des déchets.</span><span class="sxs-lookup"><span data-stu-id="5aac7-137">Notifications that are not required waste processing and delivery time.</span></span>

    <span data-ttu-id="5aac7-138">Vous pouvez concevoir un consommateur d’événements pour recevoir plusieurs événements.</span><span class="sxs-lookup"><span data-stu-id="5aac7-138">You can design an event consumer to receive multiple events.</span></span> <span data-ttu-id="5aac7-139">Par exemple, un consommateur peut exiger la notification des événements de modification d’instance pour une classe spécifique d’événements d’appareil et de violation de sécurité.</span><span class="sxs-lookup"><span data-stu-id="5aac7-139">For example, a consumer might require notification of instance modification events for a specific class of device and security violation events.</span></span> <span data-ttu-id="5aac7-140">Dans ce cas, les tâches qu’un consommateur effectue lors de la réception d’un événement de modification d’instance sont différentes pour les deux événements.</span><span class="sxs-lookup"><span data-stu-id="5aac7-140">In this case, the tasks a consumer performs when receiving an instance modification event are different for the two events.</span></span> <span data-ttu-id="5aac7-141">Par conséquent, le consommateur doit effectuer un appel à [**IWbemServices :: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) pour s’inscrire aux événements de modification d’instance, et un autre appel à **ExecNotificationQuery** pour s’inscrire aux événements de violation de sécurité.</span><span class="sxs-lookup"><span data-stu-id="5aac7-141">Thus, the consumer should make one call to [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) to register for instance modification events, and another call to **ExecNotificationQuery** to register for security violation events.</span></span>

    <span data-ttu-id="5aac7-142">Dans l’appel à [**ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery), définissez le paramètre *lFlags* sur **l' \_ indicateur WBEM \_ Return \_ immédiatement** et l' **\_ indicateur WBEM \_ Forward \_ uniquement**.</span><span class="sxs-lookup"><span data-stu-id="5aac7-142">In the call to [**ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery), set the *lFlags* parameter to **WBEM\_FLAG\_RETURN\_IMMEDIATELY** and **WBEM\_FLAG\_FORWARD\_ONLY**.</span></span> <span data-ttu-id="5aac7-143">L' **\_ indicateur WBEM \_ retourne \_ immédiatement** les demandes d’indicateur de traitement semi-synchrone, et l’indicateur **WBEM en \_ \_ avant \_ uniquement** demande un énumérateur avant uniquement.</span><span class="sxs-lookup"><span data-stu-id="5aac7-143">The **WBEM\_FLAG\_RETURN\_IMMEDIATELY** flag requests semisynchronous processing, and the **WBEM\_FLAG\_FORWARD\_ONLY** flag requests a forward-only enumerator.</span></span> <span data-ttu-id="5aac7-144">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="5aac7-144">For more information, see [Calling a Method](calling-a-method.md).</span></span> <span data-ttu-id="5aac7-145">La fonction **ExecNotificationQuery** retourne un pointeur vers une interface [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) .</span><span class="sxs-lookup"><span data-stu-id="5aac7-145">The **ExecNotificationQuery** function returns a pointer to an [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) interface.</span></span>

4.  <span data-ttu-id="5aac7-146">Interrogez les notifications d’événements enregistrées en effectuant des appels répétés à la méthode [**IEnumWbemClassObject :: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) .</span><span class="sxs-lookup"><span data-stu-id="5aac7-146">Poll for registered event notifications by making repeated calls to the [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) method.</span></span>
5.  <span data-ttu-id="5aac7-147">Lorsque vous avez terminé, Libérez l’énumérateur qui pointe vers l’objet [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) .</span><span class="sxs-lookup"><span data-stu-id="5aac7-147">When finished, release the enumerator that points to the [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) object.</span></span>

    <span data-ttu-id="5aac7-148">Vous pouvez libérer le pointeur [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) associé à l’inscription.</span><span class="sxs-lookup"><span data-stu-id="5aac7-148">You can release the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer associated with the registration.</span></span> <span data-ttu-id="5aac7-149">Le fait de libérer le pointeur **IWbemServices** entraîne l’arrêt de la remise des événements par WMI à tous les consommateurs temporaires associés.</span><span class="sxs-lookup"><span data-stu-id="5aac7-149">Releasing the **IWbemServices** pointer causes WMI to stop delivering events to all associated temporary consumers.</span></span>

 

 
