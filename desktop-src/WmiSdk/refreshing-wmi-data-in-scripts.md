---
description: Dans les scripts d’analyse, vous pouvez éviter les appels successifs à GetObject à l’aide d’un objet SWbemRefresher. L’objet SWbemRefresher est un conteneur qui peut contenir plusieurs objets WMI dont les données peuvent être actualisées en un seul appel.
ms.assetid: b34567f5-9349-4580-97d5-723759805d88
ms.tgt_platform: multiple
title: Actualisation des données WMI dans les scripts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae0f17ce718fcf5b57e4f3204337634af4129d24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203732"
---
# <a name="refreshing-wmi-data-in-scripts"></a><span data-ttu-id="e177e-104">Actualisation des données WMI dans les scripts</span><span class="sxs-lookup"><span data-stu-id="e177e-104">Refreshing WMI Data in Scripts</span></span>

<span data-ttu-id="e177e-105">Dans les scripts d’analyse, vous pouvez éviter les appels successifs à **GetObject** à l’aide d’un objet [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="e177e-105">In monitoring scripts, you can avoid successive calls to **GetObject** by using an [**SWbemRefresher**](swbemrefresher.md) object.</span></span> <span data-ttu-id="e177e-106">L’objet **SWbemRefresher** est un conteneur qui peut contenir plusieurs objets WMI dont les données peuvent être actualisées en un seul appel.</span><span class="sxs-lookup"><span data-stu-id="e177e-106">The **SWbemRefresher** object is a container that can hold several WMI objects whose data can be refreshed in one call.</span></span>

<span data-ttu-id="e177e-107">L’utilisation d’un objet [**SWbemRefresher**](swbemrefresher.md) est nécessaire pour récupérer des données précises à partir des classes de performance WMI, telles que le [**\_ \_ \_ disque logique Win32 PerfFormattedData Perfdisk**](./retrieving-raw-and-formatted-performance-data.md) ou d’autres classes préinstallées dérivées de la [**\_ performance Win32**](/windows/desktop/CIMWin32Prov/win32-perf).</span><span class="sxs-lookup"><span data-stu-id="e177e-107">Using an [**SWbemRefresher**](swbemrefresher.md) object is required to get accurate data from WMI performance classes, such as [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) or other preinstalled classes derived from [**Win32\_Perf**](/windows/desktop/CIMWin32Prov/win32-perf).</span></span>

<span data-ttu-id="e177e-108">La procédure suivante décrit comment actualiser des données dans des scripts.</span><span class="sxs-lookup"><span data-stu-id="e177e-108">The following procedure describes how to refresh data in scripts.</span></span>

<span data-ttu-id="e177e-109">**Pour actualiser des données dans des scripts**</span><span class="sxs-lookup"><span data-stu-id="e177e-109">**To refresh data in scripts**</span></span>

1.  <span data-ttu-id="e177e-110">Appelez **CreateObject** pour créer un objet actualisateur [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="e177e-110">Call **CreateObject** to create an [**SWbemRefresher**](swbemrefresher.md) refresher object.</span></span>

    ```VB
    Set objRefresher = CreateObject("WbemScripting.SWbemRefresher")
    ```

    

2.  <span data-ttu-id="e177e-111">Connectez-vous à l’espace de noms WMI.</span><span class="sxs-lookup"><span data-stu-id="e177e-111">Connect to the WMI namespace.</span></span> <span data-ttu-id="e177e-112">Pour utiliser les classes de performances de [**\_ performances Win32**](/windows/desktop/CIMWin32Prov/win32-perf) préinstallées, connectez-vous à la **racine \\ cimv2**.</span><span class="sxs-lookup"><span data-stu-id="e177e-112">To use preinstalled [**Win32\_Perf**](/windows/desktop/CIMWin32Prov/win32-perf) performances classes, connect to **root\\cimv2**.</span></span>

    ```VB
    Set objServicesCimv2 = GetObject("winmgmts:\\" _
        & strComputer & "\root\cimv2")
    ```

    

3.  <span data-ttu-id="e177e-113">Ajoutez un objet unique (appelez [**SWbemRefresher. Add**](swbemrefresher-add.md)) ou une collection (appelez [**SWbemRefresher. AddEnum**](swbemrefresher-addenum.md)) à l’actualisateur.</span><span class="sxs-lookup"><span data-stu-id="e177e-113">Add a single object (call [**SWbemRefresher.Add**](swbemrefresher-add.md)) or a collection (call [**SWbemRefresher.AddEnum**](swbemrefresher-addenum.md)) to the refresher.</span></span>

    <span data-ttu-id="e177e-114">Utilisez les classes de données précalculées dérivées de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), par exemple, [**\_ \_ \_ disque logique Win32 PerfFormattedData Perfdisk**](./retrieving-raw-and-formatted-performance-data.md) au lieu du [**\_ \_ \_ disque logique Win32 PerfRawData Perfdisk**](./retrieving-raw-and-formatted-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="e177e-114">Use the precalculated data classes derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), for example, [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) instead of [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md).</span></span> <span data-ttu-id="e177e-115">Dans le cas contraire, vous devez calculer les valeurs de toutes les propriétés autres que des compteurs simples.</span><span class="sxs-lookup"><span data-stu-id="e177e-115">Otherwise, you must calculate the values for all of the properties other than simple counters.</span></span>

    ```VB
    Set objRefreshableItem = _
        objRefresher.AddEnum(objServicesCimv2 , _
        "Win32_PerfFormattedData_PerfProc_Process")
    ```

    

4.  <span data-ttu-id="e177e-116">Actualisez les données une fois pour récupérer les données de performances initiales.</span><span class="sxs-lookup"><span data-stu-id="e177e-116">Refresh the data one time to get the initial performance data.</span></span>

    <span data-ttu-id="e177e-117">Appelez la méthode [**SWbemRefresher. Refresh**](swbemrefresher-refresh.md) ou la méthode [**SWbemObjectEx. Refresh \_**](swbemobjectex-refresh-.md) générique.</span><span class="sxs-lookup"><span data-stu-id="e177e-117">Call either the [**SWbemRefresher.Refresh**](swbemrefresher-refresh.md) method or the generic [**SWbemObjectEx.Refresh\_**](swbemobjectex-refresh-.md) method.</span></span>

    ```VB
    objRefresher.Refresh
    ```

    

5.  <span data-ttu-id="e177e-118">Si vous surveillez les performances et que vous avez une collection dans l’objet actualisateur, parcourez les objets de la collection.</span><span class="sxs-lookup"><span data-stu-id="e177e-118">If you are monitoring performance and have a collection in the refresher object, loop through the collection objects.</span></span>

    ```VB
    For Each Process in objRefreshableItem.ObjectSet
        If Process.PercentProcessorTime > 1 then
            WScript.Echo Process.Name & vbnewLine _
                & Process.PercentProcessorTime & "%"
        End If
    Next
    ```

    

6.  <span data-ttu-id="e177e-119">Effacez les éléments de l’actualisateur en appelant [**SWbemRefresher. DeleteAll**](swbemrefresher-deleteall.md) ou supprimez des éléments spécifiques en appelant [**SWbemRefresher. Remove**](swbemrefresher-remove.md).</span><span class="sxs-lookup"><span data-stu-id="e177e-119">Clear the items from the refresher by calling [**SWbemRefresher.DeleteAll**](swbemrefresher-deleteall.md) or remove specific items by calling [**SwbemRefresher.Remove**](swbemrefresher-remove.md).</span></span>

<span data-ttu-id="e177e-120">L’exemple de code VBScript suivant montre comment actualiser un seul objet sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="e177e-120">The following VBScript code example shows how to refresh a single object on the local computer.</span></span> <span data-ttu-id="e177e-121">Le script crée un conteneur d’actualisation et ajoute une instance d’un énumérateur pour les instances de [**\_ \_ \_ processus Win32 PerfFormattedData perfproc**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) .</span><span class="sxs-lookup"><span data-stu-id="e177e-121">The script creates a refresher container and adds an instance of an enumerator for [**Win32\_PerfFormattedData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) instances.</span></span> <span data-ttu-id="e177e-122">L’appel d' [**actualisation**](swbemrefresher-refresh.md) est effectué trois fois pour illustrer les modifications apportées à la propriété **PercentProcessorTime** pour les processus utilisant plus d’un pour cent du temps processeur.</span><span class="sxs-lookup"><span data-stu-id="e177e-122">The [**Refresh**](swbemrefresher-refresh.md) call is made three times to demonstrate the changes in the **PercentProcessorTime** property for processes using more than one percent of the processor time.</span></span>


```VB
On Error Resume Next
strComputer = "."
Set objRefresher = CreateObject("WbemScripting.SWbemRefresher")
Set objServicesCimv2 = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
If Err = 0 Then 
Set objRefreshableItem = _
    objRefresher.AddEnum(objServicesCimv2 ,"Win32_PerfFormattedData_PerfProc_Process")
objRefresher.Refresh
' Loop through the processes three times to locate  
'    and display all the process currently using 
'    more than 1 % of the process time. Refresh on each pass.
For i = 1 to 3
    Wscript.Echo "Refresh number " & i 
    objRefresher.Refresh 
    For Each Process in objRefreshableItem.ObjectSet
        If Process.PercentProcessorTime > 1 then
            WScript.Echo Process.Name & vbnewLine & Process.PercentProcessorTime & "%"
        End If
    Next
Next
Else
    WScript.Echo Err.Description
End If
```



<span data-ttu-id="e177e-123">La propriété d' [**index**](swbemrefreshableitem-index.md) de la [**SWbemRefreshableItem**](swbemrefreshableitem.md) retournée représente l’index de l’objet dans la collection d’actualisations.</span><span class="sxs-lookup"><span data-stu-id="e177e-123">The [**Index**](swbemrefreshableitem-index.md) property of the returned [**SWbemRefreshableItem**](swbemrefreshableitem.md) represents the index of the object in the refresher collection.</span></span> <span data-ttu-id="e177e-124">Vous pouvez appeler la propriété [**SWbemRefreshableItem. isset**](swbemrefreshableitem-isset.md) pour déterminer si un élément d’un actualisateur est un élément unique ou une collection.</span><span class="sxs-lookup"><span data-stu-id="e177e-124">You can call [**SWbemRefreshableItem.IsSet**](swbemrefreshableitem-isset.md) property to determine whether or not an item in a refresher is a single item or a collection.</span></span> <span data-ttu-id="e177e-125">Pour accéder à un seul élément, utilisez la propriété [**SWbemRefreshableItem. Object**](swbemrefreshableitem-object.md) .</span><span class="sxs-lookup"><span data-stu-id="e177e-125">To access a single item, use the [**SWbemRefreshableItem.Object**](swbemrefreshableitem-object.md) property.</span></span> <span data-ttu-id="e177e-126">Si vous n’effectuez pas l’appel à **SWbemRefreshableItem. Object**, le script échoue lorsque vous essayez d’accéder à l’objet.</span><span class="sxs-lookup"><span data-stu-id="e177e-126">If you do not make the call to **SWbemRefreshableItem.Object**, then the script fails when you try to access the object.</span></span> <span data-ttu-id="e177e-127">Pour accéder à une collection, utilisez la propriété [**SWbemRefreshableItem. ObjectSet**](swbemrefreshableitem-objectset.md) .</span><span class="sxs-lookup"><span data-stu-id="e177e-127">To access a collection, use the [**SWbemRefreshableItem.ObjectSet**](swbemrefreshableitem-objectset.md) property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e177e-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e177e-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e177e-129">Classes du compteur de performances</span><span class="sxs-lookup"><span data-stu-id="e177e-129">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="e177e-130">Accès aux données de performances dans le script</span><span class="sxs-lookup"><span data-stu-id="e177e-130">Accessing Performance Data in Script</span></span>](accessing-performance-data-in-script.md)
</dt> <dt>

[<span data-ttu-id="e177e-131">Tâches WMI : analyse des performances</span><span class="sxs-lookup"><span data-stu-id="e177e-131">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="e177e-132">Analyse des données de performances</span><span class="sxs-lookup"><span data-stu-id="e177e-132">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
