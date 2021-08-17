---
description: L’objet de script SWbemObject est l’objet WMI générique, qui définit des propriétés et des méthodes qui peuvent être utilisées indépendamment de l’objet WMI spécifique auquel l’objet SWbemObject est lié.
ms.assetid: 33252b49-00d4-4c43-8abe-9368ed82f34b
ms.tgt_platform: multiple
title: Écriture de scripts avec SWbemObject
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d6ba0cccca8fcd62af490aa91ab1cc965fdad4d3682d99a8fda52151135500ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739695"
---
# <a name="scripting-with-swbemobject"></a>Écriture de scripts avec SWbemObject

L’objet de script [**SWbemObject**](swbemobject.md) est l’objet WMI générique, qui définit des propriétés et des méthodes qui peuvent être utilisées indépendamment de l’objet WMI spécifique auquel l’objet **SWbemObject** est lié. Tous les objets WMI, tels qu’une instance [**de \_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process) ou toute autre classe de données WMI, sont représentés par [**SWbemObject**](swbemobject.md) et peuvent utiliser les propriétés et méthodes communes **SWbemObject** en plus de leurs propres propriétés et méthodes.

Par exemple, utilisez le script suivant pour obtenir toutes les instances d’un [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process) en appelant la méthode [**SWbemObject. instances \_**](swbemobject-instances-.md) . ClsobjProcess représente à la fois la définition de classe de **\_ processus Win32** et un [**SWbemObject**](swbemobject.md).


```VB
strComputer = "."
Set objWMIServices = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set clsobjProcess = objWMIServices.Get("Win32_Process")
Set colProcesses = clsobjProcess.Instances_()
For Each Process in colProcesses
    WScript.Echo Process.Name
Next
```



L’exemple suivant obtient une instance spécifique du [**\_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service) qui représente le service d’alerte et le stocke dans objAlerter. Vous pouvez ensuite appeler les méthodes [**SWbemObject**](swbemobject.md) , telles que WScript. Echo ObjAlerter. Path \_ , ou les méthodes définies par la classe de données, telles que WScript. Echo objAlerter. State. objAlerter qui représente une instance de service Win32 \_ et un **SWbemObject**.


```VB
strComputer = "." 
Set objWMIServices = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set objAlerter = objWMIServices.Get("Win32_Service.Name='Alerter'")
WScript.Echo objAlerter.Path_
objAlerter.StopService()
WScript.Echo objAlerter.State
```




```VB
For each Prop in myObject.Properties_
    Wscript.Echo Prop.Name
Next
```



L’appel à [**SWbemObject. instances \_**](swbemobject-instances-.md) obtient un autre objet de script WMI générique, [**SWbemObjectSet**](swbemobjectset.md). Comme indiqué, l’objet **SWbemObjectSet** peut être traité comme une [collection](accessing-a-collection.md).


```VB
Set clsobjProcess = objWMIServices.Get("Win32_Process")
```



Vous pouvez identifier les méthodes [**SWbemObject**](swbemobject.md) , car elles se terminent toutes par un trait de soulignement ( \_ ), par exemple [**SWbemObject. instances \_**](swbemobject-instances-.md).

[**SWbemObjectEx**](swbemobjectex.md) étend les propriétés de [**SWbemObject**](swbemobject.md). Par exemple, vous pouvez maintenant mettre à jour les données de n’importe quel objet WMI, par exemple une instance de [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process), par un appel à [**\_ SWbemObjectEx. Refresh**](swbemobjectex-refresh-.md).

L’exemple suivant montre comment les données de défaillance de page de processus système peuvent être actualisées toutes les cinq secondes.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'System'",,48) 
For Each Process in colProcesses
        i = 0
        Do Until i = 5
            i = i + 1
            Wscript.Echo "PageFaults = " & Process.PageFaults 
            Wscript.Sleep 10000
            Process.Refresh_
        Loop
Next
```



Pour plus d’informations sur l’actualisation des données à l’aide d’un objet [**SWbemRefresher**](swbemrefresher.md) , consultez [actualisation des données WMI dans des scripts](refreshing-wmi-data-in-scripts.md).

Les objets [**SWbemObject. \_ put**](swbemobject-put-.md) et [**\_ PutAsync**](swbemobject-putasync-.md) vous permettent d’écrire des modifications dans n’importe quel objet WMI. Ces méthodes valident uniquement les modifications apportées à un objet dans l’espace de noms dans lequel l’objet a été créé. Vous pouvez écrire l’objet dans un autre espace de noms à l’aide de [**SWbemServicesEx. put**](swbemservicesex-put.md) ou [**SWbemServicesEx. PutAsync**](swbemservicesex-putasync.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[API de script pour WMI](scripting-api-for-wmi.md)
</dt> <dt>

[Création d’un script WMI](creating-a-wmi-script.md)
</dt> <dt>

[Mise à jour d’une instance entière](updating-an-entire-instance.md)
</dt> <dt>

[Appel d’une méthode](calling-a-method.md)
</dt> </dl>

 

 
