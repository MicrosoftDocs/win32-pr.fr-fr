---
description: Les scripts WMI peuvent accéder aux classes de compteur de performances WMI préinstallées, soit sur l’ordinateur local, soit à distance.
ms.assetid: 79e47173-c8b6-452d-9400-93e2bd6e9da5
ms.tgt_platform: multiple
title: Accès aux données de performances dans le script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e203acfc7fc23fe0dab466eee383223aad0bf889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529226"
---
# <a name="accessing-performance-data-in-script"></a>Accès aux données de performances dans le script

Les scripts WMI peuvent accéder aux [classes de compteur de performances](/windows/desktop/CIMWin32Prov/performance-counter-classes)WMI préinstallées, soit sur l’ordinateur local, soit à distance. Alors que les scripts peuvent obtenir des données à partir de classes non calculées, telles que la [**\_ \_ \_ mémoire PerfRawData perfos de Win32**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data)ou des classes mises en forme, la [**\_ mémoire Win32 PerfFormattedData \_ perfos \_**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data), les classes de données mises en forme peuvent être plus faciles à utiliser.

L’analyse des données de performances avec les classes de compteur de performance requiert l’utilisation d’un [*actualisateur*](gloss-r.md). Utilisez l’objet [**SWbemRefresher**](swbemrefresher.md) pour stocker un ou plusieurs objets de performance pour l’actualisation ou pour actualiser un seul objet par l’appel [**SWbemObjectEx. Refresh**](swbemobjectex-refresh-.md) . Pour plus d’informations, consultez [actualisation des données WMI dans les scripts](refreshing-wmi-data-in-scripts.md).

En affectant la **valeur true** à la propriété [**SWbemRefresher. reconnexion automatique**](swbemrefresher-autoreconnect.md) , WMI se reconnecte automatiquement à un fournisseur distant si la connexion est interrompue, de sorte que vous n’avez pas besoin de vérifier l’état de la connexion.

Comme indiqué dans l’exemple de script de code de script suivant, vous devez effectuer un appel d’actualisation initial pour obtenir une valeur de départ pour l’objet que vous actualisez. Les appels d’actualisation suivants contiennent ensuite des données.

> [!Note]  
> Lorsqu’un script accède aux données du compteur de performances WMI à partir d’un ordinateur distant, le script ne peut s’exécuter que sous le compte d’utilisateur actuellement connecté. WMI ne prend pas en charge un appel [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) qui transmet des informations d’identification d’utilisateur différentes. Par conséquent, le compte qui appelle l’ordinateur distant doit déjà disposer des privilèges appropriés sur cet ordinateur.

 

L’exemple de code de script suivant montre comment utiliser un objet [**SWbemRefresher**](swbemrefresher.md) pour mettre à jour les données dans des objets de compteur de performance. Pour plus d’informations sur l’utilisation des compteurs de performance dans WMI, consultez [accès aux classes de performances préinstallées par WMI](accessing-wmi-preinstalled-performance-classes.md).


```VB
' Get raw and cooked data performance counter instances for the
" wscript process running this script

set RawProc = GetObject("winmgmts:Win32_PerfRawdata_Perfproc_process.name='wscript'")
set CookedProc = GetObject("winmgmts:Win32_Perfformatteddata_Perfproc_process.name='wscript'")

' Display the same property in raw and cooked form in a loop
for I = 1 to 6
    Wscript.Echo "wscript process raw PageFaultsPerSec = & RawProc.PageFaultsPerSec _
                 & " cooked PageFaultsPerSec= " & CookedProc.PageFaultsPerSec 

' Wait 2 seconds
    Wscript.Sleep 2000
    
    ' Refresh the object
    RawProc.Refresh_
    CookedProc.Refresh_
next
```



## <a name="example"></a>Exemple

L’exemple de code de script suivant montre que vous devez effectuer un appel d’actualisation initial pour obtenir une valeur de départ pour l’objet actualisé. Les appels d’actualisation suivants contiennent ensuite des données.

L’exemple de code de script suivant montre comment utiliser un objet [**SWbemRefresher**](swbemrefresher.md) pour mettre à jour les données dans des objets de compteur de performance. Pour plus d’informations sur l’utilisation des compteurs de performance dans WMI, consultez [accès aux classes de performances préinstallées par WMI](accessing-wmi-preinstalled-performance-classes.md).


```VB
' Get raw and cooked data performance counter instances for the
" wscript process running this script

set RawProc = GetObject("winmgmts:" _
                        & "Win32_PerfRawdata_Perfproc_process." _
                        & "name='wscript'")
set CookedProc = GetObject("winmgmts:" _ 
                & "Win32_Perfformatteddata_Perfproc_process." _
                & "name='wscript'")

' Display the same property in raw and cooked form in a loop
for I = 1 to 6
    Wscript.Echo "wscript process raw PageFaultsPerSec = " _
                 & RawProc.PageFaultsPerSec _
                 & " cooked PageFaultsPerSec= " _
                 & CookedProc.PageFaultsPerSec 

' Wait 2 seconds
    Wscript.Sleep 2000
    
    ' Refresh the object
    RawProc.Refresh_
    CookedProc.Refresh_
next
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Classes du compteur de performances](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Tâches WMI : analyse des performances](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Analyse des données de performances](monitoring-performance-data.md)
</dt> </dl>

 

 
