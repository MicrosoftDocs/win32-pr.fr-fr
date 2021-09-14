---
description: Dans les scripts d’analyse, vous pouvez éviter les appels successifs à GetObject à l’aide d’un objet SWbemRefresher. L’objet SWbemRefresher est un conteneur qui peut contenir plusieurs objets WMI dont les données peuvent être actualisées en un seul appel.
ms.assetid: b34567f5-9349-4580-97d5-723759805d88
ms.tgt_platform: multiple
title: Actualisation des données WMI dans les scripts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae0f17ce718fcf5b57e4f3204337634af4129d24
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008226"
---
# <a name="refreshing-wmi-data-in-scripts"></a>Actualisation des données WMI dans les scripts

Dans les scripts d’analyse, vous pouvez éviter les appels successifs à **GetObject** à l’aide d’un objet [**SWbemRefresher**](swbemrefresher.md) . L’objet **SWbemRefresher** est un conteneur qui peut contenir plusieurs objets WMI dont les données peuvent être actualisées en un seul appel.

L’utilisation d’un objet [**SWbemRefresher**](swbemrefresher.md) est nécessaire pour récupérer des données précises à partir des classes de performance WMI, telles que le [**\_ \_ \_ disque logique Win32 PerfFormattedData Perfdisk**](./retrieving-raw-and-formatted-performance-data.md) ou d’autres classes préinstallées dérivées de la [**\_ performance Win32**](/windows/desktop/CIMWin32Prov/win32-perf).

La procédure suivante décrit comment actualiser des données dans des scripts.

**Pour actualiser des données dans des scripts**

1.  Appelez **CreateObject** pour créer un objet actualisateur [**SWbemRefresher**](swbemrefresher.md) .

    ```VB
    Set objRefresher = CreateObject("WbemScripting.SWbemRefresher")
    ```

    

2.  Connecter à l’espace de noms WMI. Pour utiliser les classes de performances de [**\_ performances Win32**](/windows/desktop/CIMWin32Prov/win32-perf) préinstallées, connectez-vous à la **racine \\ cimv2**.

    ```VB
    Set objServicesCimv2 = GetObject("winmgmts:\\" _
        & strComputer & "\root\cimv2")
    ```

    

3.  Ajoutez un objet unique (appelez [**SWbemRefresher. Add**](swbemrefresher-add.md)) ou une collection (appelez [**SWbemRefresher. AddEnum**](swbemrefresher-addenum.md)) à l’actualisateur.

    Utilisez les classes de données précalculées dérivées de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), par exemple, [**\_ \_ \_ disque logique Win32 PerfFormattedData Perfdisk**](./retrieving-raw-and-formatted-performance-data.md) au lieu du [**\_ \_ \_ disque logique Win32 PerfRawData Perfdisk**](./retrieving-raw-and-formatted-performance-data.md). Dans le cas contraire, vous devez calculer les valeurs de toutes les propriétés autres que des compteurs simples.

    ```VB
    Set objRefreshableItem = _
        objRefresher.AddEnum(objServicesCimv2 , _
        "Win32_PerfFormattedData_PerfProc_Process")
    ```

    

4.  Actualisez les données une fois pour récupérer les données de performances initiales.

    Appelez la méthode [**SWbemRefresher. Refresh**](swbemrefresher-refresh.md) ou la méthode [**SWbemObjectEx. Refresh \_**](swbemobjectex-refresh-.md) générique.

    ```VB
    objRefresher.Refresh
    ```

    

5.  Si vous surveillez les performances et que vous avez une collection dans l’objet actualisateur, parcourez les objets de la collection.

    ```VB
    For Each Process in objRefreshableItem.ObjectSet
        If Process.PercentProcessorTime > 1 then
            WScript.Echo Process.Name & vbnewLine _
                & Process.PercentProcessorTime & "%"
        End If
    Next
    ```

    

6.  Effacez les éléments de l’actualisateur en appelant [**SWbemRefresher. DeleteAll**](swbemrefresher-deleteall.md) ou supprimez des éléments spécifiques en appelant [**SWbemRefresher. Remove**](swbemrefresher-remove.md).

L’exemple de code VBScript suivant montre comment actualiser un seul objet sur l’ordinateur local. Le script crée un conteneur d’actualisation et ajoute une instance d’un énumérateur pour les instances de [**\_ \_ \_ processus Win32 PerfFormattedData perfproc**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) . L’appel d' [**actualisation**](swbemrefresher-refresh.md) est effectué trois fois pour illustrer les modifications apportées à la propriété **PercentProcessorTime** pour les processus utilisant plus d’un pour cent du temps processeur.


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



La propriété d' [**index**](swbemrefreshableitem-index.md) de la [**SWbemRefreshableItem**](swbemrefreshableitem.md) retournée représente l’index de l’objet dans la collection d’actualisations. Vous pouvez appeler la propriété [**SWbemRefreshableItem. isset**](swbemrefreshableitem-isset.md) pour déterminer si un élément d’un actualisateur est un élément unique ou une collection. Pour accéder à un seul élément, utilisez la propriété [**SWbemRefreshableItem. Object**](swbemrefreshableitem-object.md) . Si vous n’effectuez pas l’appel à **SWbemRefreshableItem. Object**, le script échoue lorsque vous essayez d’accéder à l’objet. Pour accéder à une collection, utilisez la propriété [**SWbemRefreshableItem. ObjectSet**](swbemrefreshableitem-objectset.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Classes du compteur de performances](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Accès aux données de performances dans le script](accessing-performance-data-in-script.md)
</dt> <dt>

[Tâches WMI : analyse des performances](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Analyse des données de performances](monitoring-performance-data.md)
</dt> </dl>

 

 
