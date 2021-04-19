---
description: À l’aide de WMI, vous pouvez accéder aux données des compteurs système par programmation à partir d’objets dans les bibliothèques de performances.
ms.assetid: a0ed14e9-d2ec-43eb-8c8e-eac3c134ea1d
ms.tgt_platform: multiple
title: Analyse des données de performances
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95cee18ba88a8aff920c2d14b5709a0fd913e2ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534121"
---
# <a name="monitoring-performance-data"></a><span data-ttu-id="c8208-103">Analyse des données de performances</span><span class="sxs-lookup"><span data-stu-id="c8208-103">Monitoring Performance Data</span></span>

<span data-ttu-id="c8208-104">À l’aide de WMI, vous pouvez accéder aux données des compteurs système par programmation à partir d’objets dans les bibliothèques de performances.</span><span class="sxs-lookup"><span data-stu-id="c8208-104">Using WMI, you can access system counter data programmatically from objects in the performance libraries.</span></span> <span data-ttu-id="c8208-105">Il s’agit des mêmes données de performances que celles affichées dans le moniteur système de l’utilitaire Perfmon.</span><span class="sxs-lookup"><span data-stu-id="c8208-105">This is the same performance data that appears in the System Monitor in the Perfmon utility.</span></span> <span data-ttu-id="c8208-106">Utilisez les [classes de compteur de performances](/windows/desktop/CIMWin32Prov/performance-counter-classes) préinstallées pour obtenir des données de performances dans des scripts ou des applications C++.</span><span class="sxs-lookup"><span data-stu-id="c8208-106">Use the preinstalled [performance counter classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) to obtain performance data in scripts or C++ applications.</span></span>

<span data-ttu-id="c8208-107">Les sections suivantes sont présentées dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="c8208-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="c8208-108">Classes de performance WMI</span><span class="sxs-lookup"><span data-stu-id="c8208-108">WMI Performance Classes</span></span>](#wmi-performance-classes)
-   [<span data-ttu-id="c8208-109">Fournisseurs de données de performances</span><span class="sxs-lookup"><span data-stu-id="c8208-109">Performance Data Providers</span></span>](#performance-data-providers)
-   [<span data-ttu-id="c8208-110">Utilisation des classes de données de performances mises en forme</span><span class="sxs-lookup"><span data-stu-id="c8208-110">Using Formatted Performance Data Classes</span></span>](#using-formatted-performance-data-classes)
-   [<span data-ttu-id="c8208-111">Utilisation des classes de données de performances brutes</span><span class="sxs-lookup"><span data-stu-id="c8208-111">Using Raw Performance Data Classes</span></span>](#using-raw-performance-data-classes)
-   [<span data-ttu-id="c8208-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c8208-112">Related topics</span></span>](#related-topics)

## <a name="wmi-performance-classes"></a><span data-ttu-id="c8208-113">Classes de performance WMI</span><span class="sxs-lookup"><span data-stu-id="c8208-113">WMI Performance Classes</span></span>

<span data-ttu-id="c8208-114">Par exemple, l’objet « l’interface réseau », dans le moniteur système, est représenté dans WMI par la classe [**Win32 \_ PerfRawData \_ tcpip \_ l’interface réseau**](./retrieving-raw-and-formatted-performance-data.md) pour les données brutes et la classe [**Win32 \_ PerfFormattedData \_ tcpip \_ l’interface réseau**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) pour les données précalculées ou mises en forme.</span><span class="sxs-lookup"><span data-stu-id="c8208-114">As an example, the "NetworkInterface" object, in System Monitor, is represented in WMI by the [**Win32\_PerfRawData\_Tcpip\_NetworkInterface**](./retrieving-raw-and-formatted-performance-data.md) class for raw data and the [**Win32\_PerfFormattedData\_Tcpip\_NetworkInterface**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) class for precalculated, or formatted data.</span></span> <span data-ttu-id="c8208-115">Les classes dérivées de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) et de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) doivent être utilisées avec un objet d' [*actualisation*](gloss-r.md) .</span><span class="sxs-lookup"><span data-stu-id="c8208-115">Classes derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) must be used with a [*refresher*](gloss-r.md) object.</span></span> <span data-ttu-id="c8208-116">Sur les classes de données brutes, votre application ou script C++ doit effectuer des calculs pour obtenir la même sortie que Perfmon.exe.</span><span class="sxs-lookup"><span data-stu-id="c8208-116">On raw data classes, your C++ application or script must perform calculations to obtain the same output as Perfmon.exe.</span></span> <span data-ttu-id="c8208-117">Les classes de données mises en forme fournissent des données précalculées.</span><span class="sxs-lookup"><span data-stu-id="c8208-117">Formatted data classes supply precalculated data.</span></span> <span data-ttu-id="c8208-118">Pour plus d’informations sur l’obtention de données dans les applications C++, consultez [accès aux données de performances en c++](accessing-performance-data-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="c8208-118">For more information about obtaining data in C++ applications, see [Accessing Performance Data in C++](accessing-performance-data-in-c--.md).</span></span> <span data-ttu-id="c8208-119">Pour les scripts, consultez [accès aux données de performances dans le script](accessing-performance-data-in-script.md) et [actualisation des données WMI dans les scripts](refreshing-wmi-data-in-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="c8208-119">For scripting, see [Accessing Performance Data in Script](accessing-performance-data-in-script.md) and [Refreshing WMI Data in Scripts](refreshing-wmi-data-in-scripts.md).</span></span>

<span data-ttu-id="c8208-120">L’exemple de code VBScript suivant utilise le [**\_ \_ \_ processus Win32 PerfFormattedData perfproc**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) pour obtenir les données de performances du processus inactif.</span><span class="sxs-lookup"><span data-stu-id="c8208-120">The following VBScript code example uses [**Win32\_PerfFormattedData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) to obtain performance data for the Idle process.</span></span> <span data-ttu-id="c8208-121">Le script affiche les mêmes données qui apparaissent dans PerfMon pour le compteur% temps processeur de l’objet processus.</span><span class="sxs-lookup"><span data-stu-id="c8208-121">The script displays the same data that appears in Perfmon for the % Processor Time counter of the Process object.</span></span> <span data-ttu-id="c8208-122">L’appel à [**SWbemObjectEx. Refresh \_**](swbemobjectex-refresh-.md) effectue l’opération d’actualisation.</span><span class="sxs-lookup"><span data-stu-id="c8208-122">The call to [**SWbemObjectEx.Refresh\_**](swbemobjectex-refresh-.md) performs the refresh operation.</span></span> <span data-ttu-id="c8208-123">N’oubliez pas que les données doivent être actualisées, à bail une fois, pour obtenir une ligne de base.</span><span class="sxs-lookup"><span data-stu-id="c8208-123">Be aware that the data must be refreshed, at lease once, to obtain a baseline.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" _
    & strComputer & "\root\cimv2")
set PerfProcess = objWMIService.Get(_
    "Win32_PerfFormattedData_PerfProc_Process.Name='Idle'")

While (True)
    PerfProcess.Refresh_     
    Wscript.Echo PerfProcess.PercentProcessorTime
    Wscript.Sleep 1000
Wend
```



<span data-ttu-id="c8208-124">Les classes de compteur de performances peuvent également fournir des données statistiques.</span><span class="sxs-lookup"><span data-stu-id="c8208-124">Performance counter classes can also provide statistical data.</span></span> <span data-ttu-id="c8208-125">Pour plus d’informations, consultez [obtention de données de performances statistiques](obtaining-statistical-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="c8208-125">For more information, see [Obtaining Statistical Performance Data](obtaining-statistical-performance-data.md).</span></span>

## <a name="performance-data-providers"></a><span data-ttu-id="c8208-126">Fournisseurs de données de performances</span><span class="sxs-lookup"><span data-stu-id="c8208-126">Performance Data Providers</span></span>

<span data-ttu-id="c8208-127">WMI a des fournisseurs préinstallés qui surveillent les performances du système sur le système local et à distance.</span><span class="sxs-lookup"><span data-stu-id="c8208-127">WMI has preinstalled providers that monitor system performance on both the local system and remotely.</span></span> <span data-ttu-id="c8208-128">Le fournisseur [WmiPerfClass](wmiperfclass-provider.md) crée les classes dérivées de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) et de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="c8208-128">The [WmiPerfClass](wmiperfclass-provider.md) provider creates the classes derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span> <span data-ttu-id="c8208-129">Le fournisseur [WmiPerfInst](wmiperfinst-provider.md) fournit des données de manière dynamique aux classes brutes et mises en forme.</span><span class="sxs-lookup"><span data-stu-id="c8208-129">The [WmiPerfInst](wmiperfinst-provider.md) provider supplies data dynamically to both raw and formatted classes.</span></span>

## <a name="using-formatted-performance-data-classes"></a><span data-ttu-id="c8208-130">Utilisation des classes de données de performances mises en forme</span><span class="sxs-lookup"><span data-stu-id="c8208-130">Using Formatted Performance Data Classes</span></span>

<span data-ttu-id="c8208-131">L’exemple de code VBScript suivant obtient des données de performances sur la mémoire, les partitions de disque et les files d’attente de travail du serveur.</span><span class="sxs-lookup"><span data-stu-id="c8208-131">The following VBScript code example obtains performance data about memory, disk partitions, and server work queues.</span></span> <span data-ttu-id="c8208-132">Le script détermine ensuite si les valeurs sont comprises dans une plage acceptable.</span><span class="sxs-lookup"><span data-stu-id="c8208-132">The script then determines if the values are within an acceptable range.</span></span>

<span data-ttu-id="c8208-133">Le script utilise les objets de fournisseur WMI et les objets de script suivants :</span><span class="sxs-lookup"><span data-stu-id="c8208-133">The script uses the following WMI provider objects and scripting objects:</span></span>

-   <span data-ttu-id="c8208-134">Classes de compteur de performances WMI préinstallées.</span><span class="sxs-lookup"><span data-stu-id="c8208-134">Preinstalled WMI performance counter classes.</span></span>
-   <span data-ttu-id="c8208-135">Objet actualisateur, [**SWbemRefresher**](swbemrefresher.md).</span><span class="sxs-lookup"><span data-stu-id="c8208-135">The refresher object, [**SWbemRefresher**](swbemrefresher.md).</span></span>
-   <span data-ttu-id="c8208-136">Éléments à ajouter au conteneur d’actualisation, [ **SWbemRefreshableItem**](swbemrefreshableitem.md)</span><span class="sxs-lookup"><span data-stu-id="c8208-136">Items to add to the refresher container, [**SWbemRefreshableItem**](swbemrefreshableitem.md)</span></span>


```VB
Set objCimv2 = GetObject("winmgmts:root\cimv2")
Set objRefresher = CreateObject("WbemScripting.SWbemRefresher")

' Add items to the SWbemRefresher
' Without the SWbemRefreshableItem.ObjectSet call,
' the script will fail
Set objMemory = objRefresher.AddEnum _
    (objCimv2, _ 
    "Win32_PerfFormattedData_PerfOS_Memory").ObjectSet
Set objDiskQueue = objRefresher.AddEnum _
    (objCimv2, _
    "Win32_PerfFormattedData_PerfDisk_LogicalDisk").ObjectSet
Set objQueueLength = objRefresher.AddEnum _
    (objCimv2, _
    "Win32_PerfFormattedData_PerfNet_ServerWorkQueues").ObjectSet

' Initial refresh needed to get baseline values
objRefresher.Refresh
intTotalHealth = 0
' Do three refreshes to get data
For i = 1 to 3
    WScript.Echo "Refresh " & i
    For each intAvailableBytes in objMemory
        WScript.Echo "Available megabytes of memory: " _
            & intAvailableBytes.AvailableMBytes
        If intAvailableBytes.AvailableMBytes < 4 Then
            intTotalHealth = intTotalHealth + 1
        End If
    Next
    For each intDiskQueue in objDiskQueue
        WScript.Echo "Current disk queue length " & "Name: " _
            & intDiskQueue.Name & ":" _
            & intDiskQueue.CurrentDiskQueueLength
        If intDiskQueue.CurrentDiskQueueLength > 2 Then
            intTotalHealth = intTotalHealth + 1
        End If
    Next
    For each intServerQueueLength in objQueueLength
        WScript.Echo "Server work queue length: " _
            & intServerQueueLength.QueueLength
        If intServerQueueLength.QueueLength > 4 Then
            intTotalHealth = intTotalHealth + 1                       
        End If
    Wscript.Echo "  "
    Next
    If intTotalHealth > 0 Then
        Wscript.Echo "Unhealthy."
    Else
        Wscript.Echo "Healthy."
    End If
    intTotalHealth = 0
    Wscript.Sleep 5000
' Refresh data for all objects in the collection
    objRefresher.Refresh
Next
```



## <a name="using-raw-performance-data-classes"></a><span data-ttu-id="c8208-137">Utilisation des classes de données de performances brutes</span><span class="sxs-lookup"><span data-stu-id="c8208-137">Using Raw Performance Data Classes</span></span>

<span data-ttu-id="c8208-138">L’exemple de code VBScript suivant obtient le pourcentage de temps processeur brut en cours sur l’ordinateur local et le convertit en pourcentage.</span><span class="sxs-lookup"><span data-stu-id="c8208-138">The following VBScript code example obtains raw, current percent processor time on the local computer and converts it to a percentage.</span></span> <span data-ttu-id="c8208-139">L’exemple montre comment obtenir des données de performances brutes à partir de la propriété **PercentProcessorTime** de la classe du [**\_ \_ \_ processeur PerfRawData perfos Win32**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) .</span><span class="sxs-lookup"><span data-stu-id="c8208-139">The example shows you how to obtain raw performance data from the **PercentProcessorTime** property of the [**Win32\_PerfRawData\_PerfOS\_Processor**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) class.</span></span>

<span data-ttu-id="c8208-140">Pour calculer la valeur de temps processeur en pourcentage, vous devez rechercher la formule.</span><span class="sxs-lookup"><span data-stu-id="c8208-140">To calculate the percent processor time value, you must locate the formula.</span></span> <span data-ttu-id="c8208-141">Recherchez la valeur dans **le qualificateur de l’extension** de nom de la propriété **PercentProcessorTime** dans la table de [**qualificateur**](countertype-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="c8208-141">Look up the value in the **CounterType** qualifier for the **PercentProcessorTime** property in the [**CounterType Qualifier**](countertype-qualifier.md) table to get the constant name.</span></span> <span data-ttu-id="c8208-142">Recherchez le nom de la constante dans [types de compteurs](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) pour obtenir la formule.</span><span class="sxs-lookup"><span data-stu-id="c8208-142">Locate the constant name in [Counter Types](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) to obtain the formula.</span></span>


```VB
Set objService = GetObject( _
    "Winmgmts:{impersonationlevel=impersonate}!\Root\Cimv2")

For i = 1 to 8
    Set objInstance1 = objService.Get( _
        "Win32_PerfRawData_PerfOS_Processor.Name='_Total'")
    N1 = objInstance1.PercentProcessorTime
    D1 = objInstance1.TimeStamp_Sys100NS

'Sleep for two seconds = 2000 ms
    WScript.Sleep(2000)

    Set perf_instance2 = objService.Get( _
        "Win32_PerfRawData_PerfOS_Processor.Name='_Total'")
    N2 = perf_instance2.PercentProcessorTime
    D2 = perf_instance2.TimeStamp_Sys100NS
' Look up the CounterType qualifier for the PercentProcessorTime 
' and obtain the formula to calculate the meaningful data. 
' CounterType - PERF_100NSEC_TIMER_INV
' Formula - (1- ((N2 - N1) / (D2 - D1))) x 100

    PercentProcessorTime = (1 - ((N2 - N1)/(D2-D1)))*100
    WScript.Echo "% Processor Time=" , Round(PercentProcessorTime,2)
Next
```



## <a name="related-topics"></a><span data-ttu-id="c8208-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c8208-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8208-144">Utilisation de WMI</span><span class="sxs-lookup"><span data-stu-id="c8208-144">Using WMI</span></span>](using-wmi.md)
</dt> </dl>

 

 
