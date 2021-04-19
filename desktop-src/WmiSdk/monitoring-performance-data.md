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
# <a name="monitoring-performance-data"></a>Analyse des données de performances

À l’aide de WMI, vous pouvez accéder aux données des compteurs système par programmation à partir d’objets dans les bibliothèques de performances. Il s’agit des mêmes données de performances que celles affichées dans le moniteur système de l’utilitaire Perfmon. Utilisez les [classes de compteur de performances](/windows/desktop/CIMWin32Prov/performance-counter-classes) préinstallées pour obtenir des données de performances dans des scripts ou des applications C++.

Les sections suivantes sont présentées dans cette rubrique :

-   [Classes de performance WMI](#wmi-performance-classes)
-   [Fournisseurs de données de performances](#performance-data-providers)
-   [Utilisation des classes de données de performances mises en forme](#using-formatted-performance-data-classes)
-   [Utilisation des classes de données de performances brutes](#using-raw-performance-data-classes)
-   [Rubriques connexes](#related-topics)

## <a name="wmi-performance-classes"></a>Classes de performance WMI

Par exemple, l’objet « l’interface réseau », dans le moniteur système, est représenté dans WMI par la classe [**Win32 \_ PerfRawData \_ tcpip \_ l’interface réseau**](./retrieving-raw-and-formatted-performance-data.md) pour les données brutes et la classe [**Win32 \_ PerfFormattedData \_ tcpip \_ l’interface réseau**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) pour les données précalculées ou mises en forme. Les classes dérivées de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) et de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) doivent être utilisées avec un objet d' [*actualisation*](gloss-r.md) . Sur les classes de données brutes, votre application ou script C++ doit effectuer des calculs pour obtenir la même sortie que Perfmon.exe. Les classes de données mises en forme fournissent des données précalculées. Pour plus d’informations sur l’obtention de données dans les applications C++, consultez [accès aux données de performances en c++](accessing-performance-data-in-c--.md). Pour les scripts, consultez [accès aux données de performances dans le script](accessing-performance-data-in-script.md) et [actualisation des données WMI dans les scripts](refreshing-wmi-data-in-scripts.md).

L’exemple de code VBScript suivant utilise le [**\_ \_ \_ processus Win32 PerfFormattedData perfproc**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) pour obtenir les données de performances du processus inactif. Le script affiche les mêmes données qui apparaissent dans PerfMon pour le compteur% temps processeur de l’objet processus. L’appel à [**SWbemObjectEx. Refresh \_**](swbemobjectex-refresh-.md) effectue l’opération d’actualisation. N’oubliez pas que les données doivent être actualisées, à bail une fois, pour obtenir une ligne de base.


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



Les classes de compteur de performances peuvent également fournir des données statistiques. Pour plus d’informations, consultez [obtention de données de performances statistiques](obtaining-statistical-performance-data.md).

## <a name="performance-data-providers"></a>Fournisseurs de données de performances

WMI a des fournisseurs préinstallés qui surveillent les performances du système sur le système local et à distance. Le fournisseur [WmiPerfClass](wmiperfclass-provider.md) crée les classes dérivées de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) et de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata). Le fournisseur [WmiPerfInst](wmiperfinst-provider.md) fournit des données de manière dynamique aux classes brutes et mises en forme.

## <a name="using-formatted-performance-data-classes"></a>Utilisation des classes de données de performances mises en forme

L’exemple de code VBScript suivant obtient des données de performances sur la mémoire, les partitions de disque et les files d’attente de travail du serveur. Le script détermine ensuite si les valeurs sont comprises dans une plage acceptable.

Le script utilise les objets de fournisseur WMI et les objets de script suivants :

-   Classes de compteur de performances WMI préinstallées.
-   Objet actualisateur, [**SWbemRefresher**](swbemrefresher.md).
-   Éléments à ajouter au conteneur d’actualisation, [ **SWbemRefreshableItem**](swbemrefreshableitem.md)


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



## <a name="using-raw-performance-data-classes"></a>Utilisation des classes de données de performances brutes

L’exemple de code VBScript suivant obtient le pourcentage de temps processeur brut en cours sur l’ordinateur local et le convertit en pourcentage. L’exemple montre comment obtenir des données de performances brutes à partir de la propriété **PercentProcessorTime** de la classe du [**\_ \_ \_ processeur PerfRawData perfos Win32**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) .

Pour calculer la valeur de temps processeur en pourcentage, vous devez rechercher la formule. Recherchez la valeur dans **le qualificateur de l’extension** de nom de la propriété **PercentProcessorTime** dans la table de [**qualificateur**](countertype-qualifier.md) . Recherchez le nom de la constante dans [types de compteurs](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) pour obtenir la formule.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de WMI](using-wmi.md)
</dt> </dl>

 

 
