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
# <a name="accessing-performance-data-in-script"></a><span data-ttu-id="c7add-103">Accès aux données de performances dans le script</span><span class="sxs-lookup"><span data-stu-id="c7add-103">Accessing Performance Data in Script</span></span>

<span data-ttu-id="c7add-104">Les scripts WMI peuvent accéder aux [classes de compteur de performances](/windows/desktop/CIMWin32Prov/performance-counter-classes)WMI préinstallées, soit sur l’ordinateur local, soit à distance.</span><span class="sxs-lookup"><span data-stu-id="c7add-104">WMI scripts can access the preinstalled WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes), either on the local computer or remotely.</span></span> <span data-ttu-id="c7add-105">Alors que les scripts peuvent obtenir des données à partir de classes non calculées, telles que la [**\_ \_ \_ mémoire PerfRawData perfos de Win32**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data)ou des classes mises en forme, la [**\_ mémoire Win32 PerfFormattedData \_ perfos \_**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data), les classes de données mises en forme peuvent être plus faciles à utiliser.</span><span class="sxs-lookup"><span data-stu-id="c7add-105">While scripts can obtain data from uncalculated classes, such as [**Win32\_PerfRawData\_PerfOS\_Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data), or formatted classes, [**Win32\_PerfFormattedData\_PerfOS\_Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data), the formatted data classes can be easier to use.</span></span>

<span data-ttu-id="c7add-106">L’analyse des données de performances avec les classes de compteur de performance requiert l’utilisation d’un [*actualisateur*](gloss-r.md).</span><span class="sxs-lookup"><span data-stu-id="c7add-106">Monitoring performance data with the performance counter classes requires the use of a [*refresher*](gloss-r.md).</span></span> <span data-ttu-id="c7add-107">Utilisez l’objet [**SWbemRefresher**](swbemrefresher.md) pour stocker un ou plusieurs objets de performance pour l’actualisation ou pour actualiser un seul objet par l’appel [**SWbemObjectEx. Refresh**](swbemobjectex-refresh-.md) .</span><span class="sxs-lookup"><span data-stu-id="c7add-107">Use the [**SWbemRefresher**](swbemrefresher.md) object to store one or more performance objects for refresh or refresh a single object by the [**SWbemObjectEx.Refresh**](swbemobjectex-refresh-.md) call.</span></span> <span data-ttu-id="c7add-108">Pour plus d’informations, consultez [actualisation des données WMI dans les scripts](refreshing-wmi-data-in-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="c7add-108">For more information, see [Refreshing WMI Data in Scripts](refreshing-wmi-data-in-scripts.md).</span></span>

<span data-ttu-id="c7add-109">En affectant la **valeur true** à la propriété [**SWbemRefresher. reconnexion automatique**](swbemrefresher-autoreconnect.md) , WMI se reconnecte automatiquement à un fournisseur distant si la connexion est interrompue, de sorte que vous n’avez pas besoin de vérifier l’état de la connexion.</span><span class="sxs-lookup"><span data-stu-id="c7add-109">By setting the [**SWbemRefresher.AutoReconnect**](swbemrefresher-autoreconnect.md) property to **TRUE**, WMI automatically reconnects to a remote provider if the connection is broken so that you do not need to check for connection status.</span></span>

<span data-ttu-id="c7add-110">Comme indiqué dans l’exemple de script de code de script suivant, vous devez effectuer un appel d’actualisation initial pour obtenir une valeur de départ pour l’objet que vous actualisez.</span><span class="sxs-lookup"><span data-stu-id="c7add-110">As shown in the following script code example script, you must make an initial refresh call to get a starting value for the object you are refreshing.</span></span> <span data-ttu-id="c7add-111">Les appels d’actualisation suivants contiennent ensuite des données.</span><span class="sxs-lookup"><span data-stu-id="c7add-111">Subsequent refresh calls then contain data.</span></span>

> [!Note]  
> <span data-ttu-id="c7add-112">Lorsqu’un script accède aux données du compteur de performances WMI à partir d’un ordinateur distant, le script ne peut s’exécuter que sous le compte d’utilisateur actuellement connecté.</span><span class="sxs-lookup"><span data-stu-id="c7add-112">When a script is accessing WMI performance counter data from a remote computer, the script can only run under the current logged-on user account.</span></span> <span data-ttu-id="c7add-113">WMI ne prend pas en charge un appel [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) qui transmet des informations d’identification d’utilisateur différentes.</span><span class="sxs-lookup"><span data-stu-id="c7add-113">WMI does not support an [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) call that passes in different user credentials.</span></span> <span data-ttu-id="c7add-114">Par conséquent, le compte qui appelle l’ordinateur distant doit déjà disposer des privilèges appropriés sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c7add-114">Therefore, the account calling the remote computer must already have the appropriate privileges on that computer.</span></span>

 

<span data-ttu-id="c7add-115">L’exemple de code de script suivant montre comment utiliser un objet [**SWbemRefresher**](swbemrefresher.md) pour mettre à jour les données dans des objets de compteur de performance.</span><span class="sxs-lookup"><span data-stu-id="c7add-115">The following script code example shows how to use an [**SWbemRefresher**](swbemrefresher.md) object to update the data in performance counter objects.</span></span> <span data-ttu-id="c7add-116">Pour plus d’informations sur l’utilisation des compteurs de performance dans WMI, consultez [accès aux classes de performances préinstallées par WMI](accessing-wmi-preinstalled-performance-classes.md).</span><span class="sxs-lookup"><span data-stu-id="c7add-116">For more information about using performance counters in WMI, see [Accessing WMI Preinstalled Performance Classes](accessing-wmi-preinstalled-performance-classes.md).</span></span>


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



## <a name="example"></a><span data-ttu-id="c7add-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="c7add-117">Example</span></span>

<span data-ttu-id="c7add-118">L’exemple de code de script suivant montre que vous devez effectuer un appel d’actualisation initial pour obtenir une valeur de départ pour l’objet actualisé.</span><span class="sxs-lookup"><span data-stu-id="c7add-118">The following script code example shows that you must make an initial refresh call to get a starting value for the refreshed object.</span></span> <span data-ttu-id="c7add-119">Les appels d’actualisation suivants contiennent ensuite des données.</span><span class="sxs-lookup"><span data-stu-id="c7add-119">Subsequent refresh calls then contain data.</span></span>

<span data-ttu-id="c7add-120">L’exemple de code de script suivant montre comment utiliser un objet [**SWbemRefresher**](swbemrefresher.md) pour mettre à jour les données dans des objets de compteur de performance.</span><span class="sxs-lookup"><span data-stu-id="c7add-120">The following script code example shows how to use an [**SWbemRefresher**](swbemrefresher.md) object to update the data in performance counter objects.</span></span> <span data-ttu-id="c7add-121">Pour plus d’informations sur l’utilisation des compteurs de performance dans WMI, consultez [accès aux classes de performances préinstallées par WMI](accessing-wmi-preinstalled-performance-classes.md).</span><span class="sxs-lookup"><span data-stu-id="c7add-121">For more information about using performance counters in WMI, see [Accessing WMI Preinstalled Performance Classes](accessing-wmi-preinstalled-performance-classes.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="c7add-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c7add-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7add-123">Classes du compteur de performances</span><span class="sxs-lookup"><span data-stu-id="c7add-123">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="c7add-124">Tâches WMI : analyse des performances</span><span class="sxs-lookup"><span data-stu-id="c7add-124">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="c7add-125">Analyse des données de performances</span><span class="sxs-lookup"><span data-stu-id="c7add-125">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
