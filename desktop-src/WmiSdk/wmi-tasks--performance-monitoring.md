---
description: Utilisez les classes WMI qui obtiennent des données à partir des compteurs de performances pour accéder et actualiser les données sur les performances de l’ordinateur.
ms.assetid: 4c88de96-992e-4d34-ba93-35d2b6e73c1d
ms.tgt_platform: multiple
title: 'Tâches WMI : analyse des performances'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bbb254e14280bec5a928bdc32aaa9a3e03c7a4f4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "106543575"
---
# <a name="wmi-tasks-performance-monitoring"></a><span data-ttu-id="b3a93-103">Tâches WMI : analyse des performances</span><span class="sxs-lookup"><span data-stu-id="b3a93-103">WMI Tasks: Performance Monitoring</span></span>

<span data-ttu-id="b3a93-104">Utilisez les classes WMI qui obtiennent des données à partir des compteurs de performances pour accéder et actualiser les données sur les performances de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b3a93-104">Use the WMI classes that obtain data from performance counters to access and refresh data about computer performance.</span></span> <span data-ttu-id="b3a93-105">Pour obtenir d’autres exemples, consultez le site TechNet ScriptCenter à l’adresse [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b3a93-105">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span> <span data-ttu-id="b3a93-106">Pour plus d’informations, consultez [bibliothèques de performances et WMI](performance-libraries-and-wmi.md) et [surveillance des données de performances](monitoring-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="b3a93-106">For more information, see [Performance Libraries and WMI](performance-libraries-and-wmi.md) and [Monitoring Performance Data](monitoring-performance-data.md).</span></span>

<span data-ttu-id="b3a93-107">Les exemples de scripts présentés dans cette rubrique obtiennent des données uniquement à partir de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="b3a93-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="b3a93-108">Pour plus d’informations sur l’utilisation du script pour obtenir des données à partir d’ordinateurs distants, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="b3a93-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="b3a93-109">La procédure suivante décrit comment exécuter un script.</span><span class="sxs-lookup"><span data-stu-id="b3a93-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="b3a93-110">**Pour exécuter un script**</span><span class="sxs-lookup"><span data-stu-id="b3a93-110">**To run a script**</span></span>

1.  <span data-ttu-id="b3a93-111">Copiez le code et enregistrez-le dans un fichier avec une extension. vbs, par exemple *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="b3a93-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="b3a93-112">Assurez-vous que votre éditeur de texte n’ajoute pas d’extension. txt au fichier.</span><span class="sxs-lookup"><span data-stu-id="b3a93-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="b3a93-113">Ouvrez une fenêtre d’invite de commandes et accédez au répertoire où vous avez enregistré le fichier.</span><span class="sxs-lookup"><span data-stu-id="b3a93-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="b3a93-114">Tapez **cscript filename.vbs** à l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="b3a93-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="b3a93-115">Si vous ne pouvez pas accéder à un journal des événements, vérifiez si vous exécutez à partir d’une invite de commandes avec élévation de privilèges.</span><span class="sxs-lookup"><span data-stu-id="b3a93-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="b3a93-116">Certains journaux des événements, tels que le journal des événements de sécurité, peuvent être protégés par les contrôles d’accès utilisateur (UAC).</span><span class="sxs-lookup"><span data-stu-id="b3a93-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="b3a93-117">Par défaut, cscript affiche la sortie d’un script dans la fenêtre d’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="b3a93-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="b3a93-118">Étant donné que les scripts WMI peuvent générer de grandes quantités de sortie, vous souhaiterez peut-être rediriger la sortie vers un fichier.</span><span class="sxs-lookup"><span data-stu-id="b3a93-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="b3a93-119">Tapez **cscript filename.vbs > outfile.txt** à l’invite de commandes pour rediriger la sortie du script *filename.vbs* vers *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="b3a93-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="b3a93-120">Le tableau suivant répertorie des exemples de scripts qui peuvent être utilisés pour obtenir différents types de données à partir de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="b3a93-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b3a93-121">Comment puis-je...</span><span class="sxs-lookup"><span data-stu-id="b3a93-121">How do I...</span></span></th>
<th><span data-ttu-id="b3a93-122">Classes ou méthodes WMI</span><span class="sxs-lookup"><span data-stu-id="b3a93-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b3a93-123">... obtenir les données du compteur de performance que je peux voir dans l’utilitaire Perfmon dans un script ?</span><span class="sxs-lookup"><span data-stu-id="b3a93-123">...obtain the performance counter data that I can see in the Perfmon utility in a script?</span></span></td>
<td><span data-ttu-id="b3a93-124">Utilisez les classes dont les noms commencent par &quot; <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">Win32_PerfFormattedData</a> &quot; , par exemple <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b3a93-124">Use classes that have names that begin with &quot;<a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">Win32_PerfFormattedData</a>&quot;, for example <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a>.</span></span> <span data-ttu-id="b3a93-125">Les propriétés avec des noms tels que <strong>PageFileBytes</strong> correspondent aux compteurs de performances que vous voyez dans Perfmon.</span><span class="sxs-lookup"><span data-stu-id="b3a93-125">Properties with names like <strong>PageFileBytes</strong> correspond to performance counters you see in Perfmon.</span></span> <span data-ttu-id="b3a93-126">Les &quot; &quot; classes Win32_PerfFormattedData calculent les valeurs finales des compteurs pour vous.</span><span class="sxs-lookup"><span data-stu-id="b3a93-126">The &quot;Win32_PerfFormattedData&quot; classes calculate the final values of counters for you.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3a93-127">... obtenir des données de performances continues pour un processus unique, un lecteur de disque et d’autres données ?</span><span class="sxs-lookup"><span data-stu-id="b3a93-127">...get on-going performance data for a single process, disk drive, and other data?</span></span></td>
<td><span data-ttu-id="b3a93-128">Utilisez la <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a> ou la classe de <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">compteur de performance</a> mise en forme appropriée et la méthode <a href="swbemobjectex-refresh-.md"><strong>SWbemObjectEx.Refresh_</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b3a93-128">Use the <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a> or the appropriate formatted <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">Performance Counter Class</a> and the <a href="swbemobjectex-refresh-.md"><strong>SWbemObjectEx.Refresh_</strong></a> method.</span></span> <span data-ttu-id="b3a93-129">Pour plus d’informations, consultez <a href="scripting-with-swbemobject.md">Scripting with SWbemObject</a>.</span><span class="sxs-lookup"><span data-stu-id="b3a93-129">For more information, see <a href="scripting-with-swbemobject.md">Scripting with SWbemObject</a>.</span></span><br/> <span data-ttu-id="b3a93-130">En C++, utilisez <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath"><strong>IWbemConfigureRefresher :: AddObjectByPath</strong></a> et <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh"><strong>IWbemRefresher :: Refresh</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b3a93-130">In C++, use <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath"><strong>IWbemConfigureRefresher::AddObjectByPath</strong></a> and <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh"><strong>IWbemRefresher::Refresh</strong></a>.</span></span> <span data-ttu-id="b3a93-131">Pour plus d’informations, consultez <a href="monitoring-performance-data.md">analyse des données de performances</a>.</span><span class="sxs-lookup"><span data-stu-id="b3a93-131">For more information, see <a href="monitoring-performance-data.md">Monitoring Performance Data</a>.</span></span><br/> <span data-ttu-id="b3a93-132">Le script suivant s’exécute jusqu’à ce que l’ordinateur soit redémarré, que WMI soit arrêté ou que le script soit arrêté.</span><span class="sxs-lookup"><span data-stu-id="b3a93-132">The following script runs until the computer is restarted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="b3a93-133">Pour arrêter le script manuellement, utilisez le gestionnaire des tâches pour arrêter le processus.</span><span class="sxs-lookup"><span data-stu-id="b3a93-133">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="b3a93-134">Pour l’arrêter par programmation, utilisez la méthode <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> dans la classe <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b3a93-134">To stop it programmatically, use the <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> method in the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b3a93-135">VB</span><span class="sxs-lookup"><span data-stu-id="b3a93-135">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
set PerfProcess = objWMIService.Get(_
    &quot;Win32_PerfFormattedData_PerfProc_Process.Name=&#39;Idle&#39;&quot;)

While (True)
    PerfProcess.Refresh_     
    Wscript.Echo PerfProcess.PercentProcessorTime
    Wscript.Sleep 1000
Wend</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3a93-136">... obtenir des données de performances continues pour tous les processus sans interrogation répétée ?</span><span class="sxs-lookup"><span data-stu-id="b3a93-136">...get on-going performance data for all processes without repeated polling?</span></span></td>
<td><p><span data-ttu-id="b3a93-137">Utilisez les classes dont les noms commencent par &quot; Win32_PerfFormattedData &quot; et un objet <a href="swbemrefresher.md"><strong>SWbemRefresher</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b3a93-137">Use classes that have names that begin with &quot;Win32_PerfFormattedData&quot; and an <a href="swbemrefresher.md"><strong>SWbemRefresher</strong></a> object.</span></span> <span data-ttu-id="b3a93-138">L’actualisateur contient les objets, ce qui vous permet de ne pas avoir à faire plusieurs fois la collection.</span><span class="sxs-lookup"><span data-stu-id="b3a93-138">The refresher holds the objects so you do not need to get the collection repeatedly.</span></span> <span data-ttu-id="b3a93-139">Au moins deux valeurs sont nécessaires pour calculer les données de performances, car la plupart des compteurs sont des compteurs de taux.</span><span class="sxs-lookup"><span data-stu-id="b3a93-139">A minimum of two values are needed to calculate performance data because most counters are rate counters.</span></span> <span data-ttu-id="b3a93-140">La première fois que vous affichez les données de l’actualisateur, elles sont vides.</span><span class="sxs-lookup"><span data-stu-id="b3a93-140">The first time you display the refresher data it is empty.</span></span></p>
<p><span data-ttu-id="b3a93-141">Le script suivant s’exécute indéfiniment jusqu’à ce que l’ordinateur soit redémarré, que WMI soit arrêté ou que le script soit arrêté.</span><span class="sxs-lookup"><span data-stu-id="b3a93-141">The following script runs indefinitely until the computer is rebooted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="b3a93-142">Pour arrêter le script manuellement, utilisez le gestionnaire des tâches pour arrêter le processus.</span><span class="sxs-lookup"><span data-stu-id="b3a93-142">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="b3a93-143">Pour l’arrêter par programmation, utilisez la méthode <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> dans la classe <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b3a93-143">To stop it programmatically, use the <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> method in the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b3a93-144">VB</span><span class="sxs-lookup"><span data-stu-id="b3a93-144">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
set objRefresher = CreateObject(&quot;WbemScripting.Swbemrefresher&quot;)
Set objProcessor = objRefresher.AddEnum _
    (objWMIService, _
    &quot;Win32_PerfFormattedData_PerfOS_Processor&quot;).ObjectSet

While (True)
    objRefresher.Refresh
        For each RefreshItem in objRefresher
            For each objProcess in RefreshItem.ObjectSet
                Wscript.Echo objProcess.GetObjectText_
            Next
        Next
     Wscript.Sleep 5000
Wend</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3a93-145">... obtenir et calculer les données de performances des processus sur Windows 2000 ?</span><span class="sxs-lookup"><span data-stu-id="b3a93-145">...get and calculate performance data for processes on Windows 2000?</span></span></td>
<td><p><span data-ttu-id="b3a93-146">Utilisez les &quot; &quot; classes Win32_PerfRawData, telles que <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfRawData_PerfProc_Process</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b3a93-146">Use the &quot;Win32_PerfRawData&quot; classes, such as <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfRawData_PerfProc_Process</strong></a>.</span></span> <span data-ttu-id="b3a93-147">Obtenir les données de propriété, telles que <strong>PercentProcessorTime</strong>, deux fois pour un processus spécifique.</span><span class="sxs-lookup"><span data-stu-id="b3a93-147">Get the property data, such as <strong>PercentProcessorTime</strong>, twice for a specific process.</span></span> <span data-ttu-id="b3a93-148">Recherchez la formule spécifiée dans <a href="countertype-qualifier.md"><strong>le qualificateur de l’identificateur</strong></a> de la propriété et calculez.</span><span class="sxs-lookup"><span data-stu-id="b3a93-148">Look up the formula specified in the <a href="countertype-qualifier.md"><strong>CounterType</strong></a> qualifier for the property and calculate.</span></span> <span data-ttu-id="b3a93-149">L’exemple est <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)">PERF_100NSEC_TIMER_INV</a>.</span><span class="sxs-lookup"><span data-stu-id="b3a93-149">The CounterType in the example is <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)">PERF_100NSEC_TIMER_INV</a>.</span></span> <span data-ttu-id="b3a93-150">Pour plus d’informations, consultez <a href="monitoring-performance-data.md">analyse des données de performances</a>.</span><span class="sxs-lookup"><span data-stu-id="b3a93-150">For more information, see <a href="monitoring-performance-data.md">Monitoring Performance Data</a>.</span></span></p>
<p><span data-ttu-id="b3a93-151">Le script suivant s’exécute indéfiniment jusqu’à ce que l’ordinateur soit redémarré, que WMI soit arrêté ou que le script soit arrêté.</span><span class="sxs-lookup"><span data-stu-id="b3a93-151">The following script runs indefinitely until the computer is rebooted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="b3a93-152">Pour arrêter le script manuellement, utilisez le gestionnaire des tâches pour arrêter le processus.</span><span class="sxs-lookup"><span data-stu-id="b3a93-152">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="b3a93-153">Pour l’arrêter par programmation, utilisez la méthode <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> dans la classe <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b3a93-153">To stop it programmatically, use the <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> method in the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b3a93-154">VB</span><span class="sxs-lookup"><span data-stu-id="b3a93-154">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)

While (True)
    Set object1 = objWMIService.Get( _
    &quot;Win32_PerfRawData_PerfOS_Processor.Name=&#39;_Total&#39;&quot;)
    N1 = object1.PercentProcessorTime
    D1 = object1.TimeStamp_Sys100NS
    Wscript.Sleep(1000)
    set object2 = objWMIService.Get( _
    &quot;Win32_PerfRawData_PerfOS_Processor.Name=&#39;_Total&#39;&quot;)
    N2 = object2.PercentProcessorTime
    D2 = object2.TimeStamp_Sys100NS
    &#39; CounterType - PERF_100NSEC_TIMER_INV
    &#39; Formula - (1- ((N2 - N1) / (D2 - D1))) x 100
    PercentProcessorTime = (1 - ((N2 - N1)/(D2-D1)))*100
    Wscript.Echo &quot;% Processor Time=&quot; , PercentProcessorTime
Wend</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="b3a93-155">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b3a93-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3a93-156">Tâches WMI pour les scripts et les applications</span><span class="sxs-lookup"><span data-stu-id="b3a93-156">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="b3a93-157">Exemples d’applications WMI C++</span><span class="sxs-lookup"><span data-stu-id="b3a93-157">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="b3a93-158">ScriptCenter TechNet</span><span class="sxs-lookup"><span data-stu-id="b3a93-158">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>
