---
description: Pour recevoir des notifications du fournisseur de Registre système, une application de gestion doit s’inscrire en tant que consommateur d’événements temporaires.
ms.assetid: 4cac5fdd-c842-4d7e-a56e-2e1312df68b4
ms.tgt_platform: multiple
title: Inscription pour les événements du Registre système
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 886046f5ffef366cdba2efb86629019f2ee0b5e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106542011"
---
# <a name="registering-for-system-registry-events"></a><span data-ttu-id="f01eb-103">Inscription pour les événements du Registre système</span><span class="sxs-lookup"><span data-stu-id="f01eb-103">Registering for System Registry Events</span></span>

<span data-ttu-id="f01eb-104">Pour recevoir des notifications du fournisseur de [Registre système](/previous-versions/windows/desktop/regprov/system-registry-provider) , une application de gestion doit s’inscrire en tant que consommateur d’événements temporaires.</span><span class="sxs-lookup"><span data-stu-id="f01eb-104">To receive notifications from the [System Registry](/previous-versions/windows/desktop/regprov/system-registry-provider) provider, a management application must register as a temporary event consumer.</span></span> <span data-ttu-id="f01eb-105">La plupart des conditions requises pour s’inscrire pour le fournisseur de Registre système sont les mêmes que pour toute autre inscription d’événement, sauf que vous devez également effectuer la procédure suivante.</span><span class="sxs-lookup"><span data-stu-id="f01eb-105">Most of the requirements to register for the System Registry provider are the same as any other event registration, except you must also perform the following procedure.</span></span>

<span data-ttu-id="f01eb-106">Le fournisseur Registry fournit des classes d’événements pour les événements dans le registre système.</span><span class="sxs-lookup"><span data-stu-id="f01eb-106">The registry provider supplies event classes for events in the system registry.</span></span> <span data-ttu-id="f01eb-107">Pour plus d’informations sur l’inscription générale des événements, consultez [réception d’un événement WMI](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="f01eb-107">For more information about general event registration, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

<span data-ttu-id="f01eb-108">La procédure suivante décrit comment s’inscrire pour les événements du Registre système.</span><span class="sxs-lookup"><span data-stu-id="f01eb-108">The following procedure describes how to register for system registry events.</span></span>

<span data-ttu-id="f01eb-109">**Pour s’inscrire aux événements du Registre système**</span><span class="sxs-lookup"><span data-stu-id="f01eb-109">**To register for system registry events**</span></span>

1.  <span data-ttu-id="f01eb-110">Appeler une méthode de requête de notification.</span><span class="sxs-lookup"><span data-stu-id="f01eb-110">Call a notification query method.</span></span>

    <span data-ttu-id="f01eb-111">Dans script ou C++, utilisez une requête de notification comme [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) ou [**IWbemServices :: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync).</span><span class="sxs-lookup"><span data-stu-id="f01eb-111">In either script or C++, use a notification query such as [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) or [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync).</span></span> <span data-ttu-id="f01eb-112">Créez une chaîne de requête pour le paramètre *bstrQuery* de **IWbemServices :: ExecNotificationQueryAsync** ou *strQuery* dans le script.</span><span class="sxs-lookup"><span data-stu-id="f01eb-112">Create a query string for the *bstrQuery* parameter of **IWbemServices::ExecNotificationQueryAsync** or the *strQuery* in script.</span></span>

2.  <span data-ttu-id="f01eb-113">Déterminez le type d’événement que vous souhaitez recevoir et créez la requête.</span><span class="sxs-lookup"><span data-stu-id="f01eb-113">Determine which type of event you want to receive and create the query.</span></span>

    <span data-ttu-id="f01eb-114">Le tableau suivant répertorie les classes d’événements de registre que vous pouvez utiliser.</span><span class="sxs-lookup"><span data-stu-id="f01eb-114">The following table lists the registry event classes that you can use.</span></span>

    

    | <span data-ttu-id="f01eb-115">Classe d'événements</span><span class="sxs-lookup"><span data-stu-id="f01eb-115">Event class</span></span>                                                      | <span data-ttu-id="f01eb-116">Emplacement Hive</span><span class="sxs-lookup"><span data-stu-id="f01eb-116">Hive location</span></span>        | <span data-ttu-id="f01eb-117">Description</span><span class="sxs-lookup"><span data-stu-id="f01eb-117">Description</span></span>                                                 |
    |------------------------------------------------------------------|----------------------|-------------------------------------------------------------|
    | [<span data-ttu-id="f01eb-118">**RegistryEvent**</span><span class="sxs-lookup"><span data-stu-id="f01eb-118">**RegistryEvent**</span></span>](/previous-versions/windows/desktop/regprov/registryevent)                       | <span data-ttu-id="f01eb-119">N/A</span><span class="sxs-lookup"><span data-stu-id="f01eb-119">N/A</span></span><br/>       | <span data-ttu-id="f01eb-120">Classe de base abstraite pour les modifications dans le registre.</span><span class="sxs-lookup"><span data-stu-id="f01eb-120">Abstract base class for changes in the registry.</span></span><br/> |
    | [<span data-ttu-id="f01eb-121">**RegistryTreeChangeEvent**</span><span class="sxs-lookup"><span data-stu-id="f01eb-121">**RegistryTreeChangeEvent**</span></span>](/previous-versions/windows/desktop/regprov/registrytreechangeevent)   | <span data-ttu-id="f01eb-122">RootPath</span><span class="sxs-lookup"><span data-stu-id="f01eb-122">RootPath</span></span><br/>  | <span data-ttu-id="f01eb-123">Surveille les modifications apportées à une hiérarchie de clés.</span><span class="sxs-lookup"><span data-stu-id="f01eb-123">Monitors changes to a hierarchy of keys.</span></span><br/>         |
    | [<span data-ttu-id="f01eb-124">**RegistryKeyChangeEvent**</span><span class="sxs-lookup"><span data-stu-id="f01eb-124">**RegistryKeyChangeEvent**</span></span>](/previous-versions/windows/desktop/regprov/registrykeychangeevent)     | <span data-ttu-id="f01eb-125">KeyPath</span><span class="sxs-lookup"><span data-stu-id="f01eb-125">KeyPath</span></span><br/>   | <span data-ttu-id="f01eb-126">Analyse les modifications apportées à une clé unique.</span><span class="sxs-lookup"><span data-stu-id="f01eb-126">Monitors changes to a single key.</span></span><br/>                |
    | [<span data-ttu-id="f01eb-127">**RegistryValueChangeEvent**</span><span class="sxs-lookup"><span data-stu-id="f01eb-127">**RegistryValueChangeEvent**</span></span>](/previous-versions/windows/desktop/regprov/registryvaluechangeevent) | <span data-ttu-id="f01eb-128">ValueName</span><span class="sxs-lookup"><span data-stu-id="f01eb-128">ValueName</span></span><br/> | <span data-ttu-id="f01eb-129">Analyse les modifications apportées à une valeur unique.</span><span class="sxs-lookup"><span data-stu-id="f01eb-129">Monitors changes to a single value.</span></span><br/>              |

    

     

    <span data-ttu-id="f01eb-130">Ces classes ont une propriété appelée **Hive** qui identifie la hiérarchie des clés dont la modification doit être surveillée, telle que **HKEY \_ local \_ machine**.</span><span class="sxs-lookup"><span data-stu-id="f01eb-130">These classes have a property called **Hive** that identifies the hierarchy of keys to be monitored for change, such as **HKEY\_LOCAL\_MACHINE**.</span></span>

    <span data-ttu-id="f01eb-131">Les modifications apportées aux ruches **\_ \_ racine** et **HKEY \_ Current \_ User** ne sont pas prises en charge par les [**RegistryEvent**](/previous-versions/windows/desktop/regprov/registryevent) ou les classes qui en sont dérivées, par exemple [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent).</span><span class="sxs-lookup"><span data-stu-id="f01eb-131">Changes to the **HKEY\_CLASSES\_ROOT** and **HKEY\_CURRENT\_USER** hives are not supported by [**RegistryEvent**](/previous-versions/windows/desktop/regprov/registryevent) or classes derived from it, such as [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent).</span></span>

3.  <span data-ttu-id="f01eb-132">Créez la clause WHERE pour votre inscription d’événement.</span><span class="sxs-lookup"><span data-stu-id="f01eb-132">Create the WHERE clause for your event registration.</span></span>

    <span data-ttu-id="f01eb-133">Le fournisseur de Registre système a des règles spécifiques pour les clauses WHERE.</span><span class="sxs-lookup"><span data-stu-id="f01eb-133">The System Registry provider has specific rules for WHERE clauses.</span></span> <span data-ttu-id="f01eb-134">Pour plus d’informations, consultez [création d’une clause WHERE appropriée pour le fournisseur de Registre](creating-a-proper-where-clause-for-the-registry-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f01eb-134">For more information, see [Creating a Proper WHERE Clause for the Registry Provider](creating-a-proper-where-clause-for-the-registry-provider.md).</span></span> <span data-ttu-id="f01eb-135">Pour plus d’informations générales sur la création d’une clause WHERE, consultez [interrogation avec WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="f01eb-135">For more general information about creating a WHERE clause, see [Querying with WQL](querying-with-wql.md).</span></span>

4.  <span data-ttu-id="f01eb-136">Déterminez si votre consommateur reçoit des événements.</span><span class="sxs-lookup"><span data-stu-id="f01eb-136">Determine whether your consumer is receiving events.</span></span>

    <span data-ttu-id="f01eb-137">Le fournisseur de Registre système ne garantit pas que tous les événements envoyés sont remis.</span><span class="sxs-lookup"><span data-stu-id="f01eb-137">The System Registry provider does not guarantee that all sent events are delivered.</span></span> <span data-ttu-id="f01eb-138">Pour plus d’informations, consultez [réception d’événements de Registre](receiving-registry-events.md).</span><span class="sxs-lookup"><span data-stu-id="f01eb-138">For more information, see [Receiving Registry Events](receiving-registry-events.md).</span></span>

<span data-ttu-id="f01eb-139">L’exemple de code VBScript suivant montre comment détecter une modification du Registre dans la ruche ou la sous-arborescence Microsoft **HKEY \_ local \_ machine** \\ **Software** \\  .</span><span class="sxs-lookup"><span data-stu-id="f01eb-139">The following VBScript code example shows how to detect a registry change in the **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft** hive or subtree.</span></span> <span data-ttu-id="f01eb-140">Il s’agit d’un script d’analyse qui, à des fins de démonstration, s’exécute dans un processus nommé Wscript.exe jusqu’à ce qu’il soit terminé dans le **Gestionnaire des tâches**, que WMI soit arrêté ou que le système d’exploitation soit redémarré.</span><span class="sxs-lookup"><span data-stu-id="f01eb-140">This is a monitoring script that, for demonstration purposes, runs in a process named Wscript.exe until it is terminated in **Task Manager**, WMI is stopped, or the operating system is rebooted.</span></span> <span data-ttu-id="f01eb-141">Le script utilise un appel [*semi-synchrone*](gloss-s.md) pour [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).</span><span class="sxs-lookup"><span data-stu-id="f01eb-141">The script uses a [*semisynchronous*](gloss-s.md) call to [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).</span></span> <span data-ttu-id="f01eb-142">Pour plus d’informations sur les appels semi-synchrones, consultez [création d’un appel semi-synchrone avec VBScript](making-a-semisynchronous-call-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="f01eb-142">For more information about semisynchronous calls, see [Making a Semisynchronous Call with VBScript](making-a-semisynchronous-call-with-vbscript.md).</span></span>


```VB
Set wmiServices = GetObject("winmgmts:root/default") 
Set colTreeChanges = wmiServices.ExecNotificationQuery _
    ("SELECT * FROM RegistryTreeChangeEvent " _
    & "WHERE Hive='HKEY_LOCAL_MACHINE' " _
    & "AND RootPath='SOFTWARE\\Microsoft'")

While (True)
   Set TreeChange = colTreeChanges.NextEvent
   TreeChange.GetObjectText_()
   Wscript.Echo  "Hive = " & TreeChange.Hive & VBNewLine _
      & "RootPath = "& TreeChange.RootPath _
      & TreeChange.GetObjectText_()      
Wend
```



L’exemple de code VBScript suivant montre comment surveiller la modification des valeurs d’une clé en vous inscrivant pour le type d’événement du fournisseur de Registre [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent). Le script appelle une méthode asynchrone, [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md). <span data-ttu-id="f01eb-145">Pour plus d’informations sur les appels asynchrones et la sécurité, consultez [création d’un appel asynchrone avec VBScript](making-an-asynchronous-call-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="f01eb-145">For more information about asynchronous calls and security, see [Making an Asynchronous Call with VBScript](making-an-asynchronous-call-with-vbscript.md).</span></span>

<span data-ttu-id="f01eb-146">Le script suivant s’exécute indéfiniment jusqu’à ce que l’ordinateur soit redémarré, que WMI soit arrêté ou que le script soit arrêté.</span><span class="sxs-lookup"><span data-stu-id="f01eb-146">The following script runs indefinitely until the computer is rebooted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="f01eb-147">Pour arrêter le script manuellement, utilisez le gestionnaire des tâches pour arrêter le processus.</span><span class="sxs-lookup"><span data-stu-id="f01eb-147">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="f01eb-148">Pour l’arrêter par programmation, utilisez la méthode [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) dans la classe de \_ processus Win32.</span><span class="sxs-lookup"><span data-stu-id="f01eb-148">To stop it programmatically, use the [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) method in the Win32\_Process class.</span></span>


```VB
strComputer = "."
Set objWMIServices = GetObject("winmgmts:root/default") 
Set wmiSink = WScript.CreateObject( _
    "WbemScripting.SWbemSink", "SINK_") 
Set ObjRegistry = GetObject("winmgmts:_
    {impersonationLevel = impersonate}!\\" _
    & strComputer & "\root\default:StdRegProv")

' Create a new key
strPath = "SOFTWARE\MyKey\MySubKey\"
Return = objRegistry.CreateKey(HKEY_LOCAL_MACHINE, strPath)

' Start listening for change in key
objWMIServices.ExecNotificationQueryAsync wmiSink, _ 
    "SELECT * FROM RegistryKeyChangeEvent " _ 
    & "WHERE Hive='HKEY_LOCAL_MACHINE' AND " _ 
    & "KeyPath='SOFTWARE\\MyKey\\MySubKey\\'" 
WScript.Echo "Listening for Registry Change Events..." 

While(True) 
    WScript.Sleep 1000
' You can use Regedit to make a change in the key 
' HKEY_LOCAL_MACHINE\SOFTWARE\MyKey\MySubKey\ 
'    to see an event generated.
Wend 

Sub SINK_OnObjectReady(EventObject, wmiAsyncContext) 
    WScript.Echo "Received Registry Change Event" & vbCrLf & _
      EventObject.GetObjectText_() 
End Sub
```



 

