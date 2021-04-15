---
description: Les tâches WMI pour les processus obtiennent des informations telles que le compte sous lequel un processus est en cours d’exécution. Vous pouvez effectuer des actions telles que la création de processus. Pour obtenir d’autres exemples, consultez le site TechNet ScriptCenter à l’adresse https://www.microsoft.com/technet .
ms.assetid: 2ae7c302-ab8b-4150-8ece-ffb66374b3f7
ms.tgt_platform: multiple
title: 'Tâches WMI : Processus'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a720046d8f5cd25c55f2d5f367d2c23d5e4fc882
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104485936"
---
# <a name="wmi-tasks-processes"></a><span data-ttu-id="11c1c-105">Tâches WMI : Processus</span><span class="sxs-lookup"><span data-stu-id="11c1c-105">WMI Tasks: Processes</span></span>

<span data-ttu-id="11c1c-106">Les tâches WMI pour les processus obtiennent des informations telles que le compte sous lequel un processus est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="11c1c-106">WMI tasks for processes obtain information such as the account under which a process is running.</span></span> <span data-ttu-id="11c1c-107">Vous pouvez effectuer des actions telles que la création de processus.</span><span class="sxs-lookup"><span data-stu-id="11c1c-107">You can perform actions like creating processes.</span></span> <span data-ttu-id="11c1c-108">Pour obtenir d’autres exemples, consultez le site TechNet ScriptCenter à l’adresse [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="11c1c-108">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="11c1c-109">Les exemples de scripts présentés dans cette rubrique obtiennent des données uniquement à partir de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="11c1c-109">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="11c1c-110">Pour plus d’informations sur l’utilisation du script pour obtenir des données à partir d’ordinateurs distants, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="11c1c-110">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="11c1c-111">La procédure suivante décrit comment exécuter un script.</span><span class="sxs-lookup"><span data-stu-id="11c1c-111">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="11c1c-112">**Pour exécuter un script**</span><span class="sxs-lookup"><span data-stu-id="11c1c-112">**To run a script**</span></span>

1.  <span data-ttu-id="11c1c-113">Copiez le code et enregistrez-le dans un fichier avec une extension. vbs, par exemple *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="11c1c-113">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="11c1c-114">Assurez-vous que votre éditeur de texte n’ajoute pas d’extension. txt au fichier.</span><span class="sxs-lookup"><span data-stu-id="11c1c-114">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="11c1c-115">Ouvrez une fenêtre d’invite de commandes et accédez au répertoire où vous avez enregistré le fichier.</span><span class="sxs-lookup"><span data-stu-id="11c1c-115">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="11c1c-116">Tapez **cscript filename.vbs** à l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="11c1c-116">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="11c1c-117">Si vous ne pouvez pas accéder à un journal des événements, vérifiez si vous exécutez à partir d’une invite de commandes avec élévation de privilèges.</span><span class="sxs-lookup"><span data-stu-id="11c1c-117">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="11c1c-118">Certains journaux des événements, tels que le journal des événements de sécurité, peuvent être protégés par les contrôles d’accès utilisateur (UAC).</span><span class="sxs-lookup"><span data-stu-id="11c1c-118">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="11c1c-119">Par défaut, cscript affiche la sortie d’un script dans la fenêtre d’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="11c1c-119">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="11c1c-120">Étant donné que les scripts WMI peuvent générer de grandes quantités de sortie, vous souhaiterez peut-être rediriger la sortie vers un fichier.</span><span class="sxs-lookup"><span data-stu-id="11c1c-120">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="11c1c-121">Tapez **cscript filename.vbs > outfile.txt** à l’invite de commandes pour rediriger la sortie du script *filename.vbs* vers *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="11c1c-121">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="11c1c-122">Le tableau suivant répertorie des exemples de scripts qui peuvent être utilisés pour obtenir différents types de données à partir de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="11c1c-122">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11c1c-123">Comment puis-je...</span><span class="sxs-lookup"><span data-stu-id="11c1c-123">How do I...</span></span></th>
<th><span data-ttu-id="11c1c-124">Classes ou méthodes WMI</span><span class="sxs-lookup"><span data-stu-id="11c1c-124">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="11c1c-125">... exécuter une application dans une fenêtre masquée ?</span><span class="sxs-lookup"><span data-stu-id="11c1c-125">...run an application in a hidden window?</span></span></td>
<td><span data-ttu-id="11c1c-126">Appelez l’application à partir d’un script qui utilise les classes <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> et <a href="/windows/desktop/CIMWin32Prov/win32-processstartup"><strong>Win32_ProcessStartup</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="11c1c-126">Call the application from a script that uses the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> and <a href="/windows/desktop/CIMWin32Prov/win32-processstartup"><strong>Win32_ProcessStartup</strong></a> classes.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11c1c-127">VB</span><span class="sxs-lookup"><span data-stu-id="11c1c-127">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Const HIDDEN_WINDOW = 0
strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set objStartup = objWMIService.Get(&quot;Win32_ProcessStartup&quot;)
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = HIDDEN_WINDOW
Set objProcess = GetObject(&quot;winmgmts:root\cimv2:Win32_Process&quot;)
errReturn = objProcess.Create( &quot;Notepad.exe&quot;, null, objConfig, intProcessID)</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11c1c-128">PowerShell</span><span class="sxs-lookup"><span data-stu-id="11c1c-128">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$startup=[wmiclass]&quot;Win32_ProcessStartup&quot;
$startup.Properties[&#39;ShowWindow&#39;].value=$False
([wmiclass]&quot;win32_Process&quot;).create(&#39;notepad.exe&#39;,&#39;C:\&#39;,$Startup)</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="11c1c-129">... déterminer les scripts qui s’exécutent sur l’ordinateur local ?</span><span class="sxs-lookup"><span data-stu-id="11c1c-129">...determine which scripts are running on the local computer?</span></span></td>
<td><p><span data-ttu-id="11c1c-130">Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> et retournez tous les processus portant le nom Cscript.exe ou Wscript.exe.</span><span class="sxs-lookup"><span data-stu-id="11c1c-130">Use the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class and return all processes with the name Cscript.exe or Wscript.exe.</span></span> <span data-ttu-id="11c1c-131">Pour déterminer les scripts individuels qui s’exécutent dans ces processus, vérifiez la valeur de la propriété <strong>CommandLine</strong> .</span><span class="sxs-lookup"><span data-stu-id="11c1c-131">To determine the individual scripts running in these processes, check the value of the <strong>CommandLine</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11c1c-132">VB</span><span class="sxs-lookup"><span data-stu-id="11c1c-132">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot; 
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\CIMV2&quot;) 
Set colItems = objWMIService.ExecQuery(&quot;SELECT * FROM Win32_Process&quot; & _
           &quot; WHERE Name = &#39;cscript.exe&#39;&quot; & &quot; OR Name = &#39;wscript.exe&#39;&quot;,,48) 
For Each objItem in colItems 
    Wscript.Echo &quot;-------------------------------------------&quot;
    Wscript.Echo &quot;CommandLine: &quot; & objItem.CommandLine
    Wscript.Echo &quot;Name: &quot; & objItem.Name
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11c1c-133">PowerShell</span><span class="sxs-lookup"><span data-stu-id="11c1c-133">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
Get-WmiObject -Class &quot;Win32_Process&quot; -ComputerName &quot;.&quot; | `
     where {($_.name -eq &#39;cscript.exe&#39;) -or ($_.name -eq &#39;wscript.exe&#39;) } | `
     Format-List -Property CommandLine, Name</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11c1c-134">... déterminer le nom du compte sous lequel un processus est en cours d’exécution ?</span><span class="sxs-lookup"><span data-stu-id="11c1c-134">...find out the account name under which a process is running?</span></span></td>
<td><p><span data-ttu-id="11c1c-135">Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> et la méthode <a href="/windows/desktop/CIMWin32Prov/getowner-method-in-class-win32-process"><strong>GetOwner</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="11c1c-135">Use the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/getowner-method-in-class-win32-process"><strong>GetOwner</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11c1c-136">VB</span><span class="sxs-lookup"><span data-stu-id="11c1c-136">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colProcessList = objWMIService.ExecQuery (&quot;Select * from Win32_Process&quot;)
For Each objProcess in colProcessList
    colProperties = objProcess.GetOwner( strNameOfUser,strUserDomain)
    Wscript.Echo &quot;Process &quot; & objProcess.Name & &quot; is owned by &quot; & strUserDomain & &quot;\&quot; & strNameOfUser & &quot;.&quot;
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11c1c-137">PowerShell</span><span class="sxs-lookup"><span data-stu-id="11c1c-137">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -class win32_process -ComputerName &quot;.&quot; | ForEach-Object { $_.GetOwner() | Select -Property domain, user }</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11c1c-138">... modifier la priorité d’un processus en cours d’exécution ?</span><span class="sxs-lookup"><span data-stu-id="11c1c-138">...change the priority of a running process?</span></span></td>
<td><p><span data-ttu-id="11c1c-139">Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> et la méthode <a href="/windows/desktop/CIMWin32Prov/setpriority-method-in-class-win32-process"><strong>SetPriority</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="11c1c-139">Use the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/setpriority-method-in-class-win32-process"><strong>SetPriority</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11c1c-140">VB</span><span class="sxs-lookup"><span data-stu-id="11c1c-140">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Const ABOVE_NORMAL = 32768
strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colProcesses = objWMIService.ExecQuery (&quot;Select * from Win32_Process Where Name = &#39;Notepad.exe&#39;&quot;)
For Each objProcess in colProcesses
    objProcess.SetPriority(ABOVE_NORMAL) 
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11c1c-141">PowerShell</span><span class="sxs-lookup"><span data-stu-id="11c1c-141">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$ABOVE_NORMAL = 32768
$strComputer = &quot;.&quot;
$colProcesses = Get-WmiObject -Class Win32_Process -ComputerName $strComputer | Where-Object { $_.name -eq &#39;Notepad.exe&#39; }
foreach ($objProcess in $colProcesses) { $objProcess.SetPriority($ABOVE_NORMAL) }</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11c1c-142">... mettre fin à un processus à l’aide d’un script ?</span><span class="sxs-lookup"><span data-stu-id="11c1c-142">...terminate a process using a script?</span></span></td>
<td><p><span data-ttu-id="11c1c-143">Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> et la méthode <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="11c1c-143">Use the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11c1c-144">VB</span><span class="sxs-lookup"><span data-stu-id="11c1c-144">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colProcessList = objWMIService.ExecQuery (&quot;Select * from Win32_Process Where Name = &#39;Notepad.exe&#39;&quot;)
For Each objProcess in colProcessList
    objProcess.Terminate()
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11c1c-145">PowerShell</span><span class="sxs-lookup"><span data-stu-id="11c1c-145">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colProcesses = Get-WmiObject -Class Win32_Process -ComputerName $strComputer | Where-Object { $_.name -eq &#39;Notepad.exe&#39; }
foreach ($objProcess in $colProcesses) { $objProcess.Terminate() }</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11c1c-146">... déterminer la quantité de temps processeur et de mémoire que chaque processus utilise ?</span><span class="sxs-lookup"><span data-stu-id="11c1c-146">...determine how much processor time and memory each process is using?</span></span></td>
<td><p><span data-ttu-id="11c1c-147">Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> et les propriétés telles <strong>que KernelModeTime</strong>, <strong>WorkingSetSize</strong>, <strong>PageFileUsage</strong>et <strong>PageFaults</strong>.</span><span class="sxs-lookup"><span data-stu-id="11c1c-147">Use the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class and properties such as <strong>KernelModeTime</strong>, <strong>WorkingSetSize</strong>, <strong>PageFileUsage</strong>, and <strong>PageFaults</strong>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11c1c-148">VB</span><span class="sxs-lookup"><span data-stu-id="11c1c-148">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colProcesses = objWMIService.ExecQuery(&quot;Select * from Win32_Process&quot;)
For Each objProcess in colProcesses
    Wscript.Echo &quot;Process: &quot; & objProcess.Name
    sngProcessTime = (CSng(objProcess.KernelModeTime) + CSng(objProcess.UserModeTime)) / 10000000
    Wscript.Echo &quot;Processor Time: &quot; & sngProcessTime
    Wscript.Echo &quot;Process ID: &quot; & objProcess.ProcessID
    Wscript.Echo &quot;Working Set Size: &quot; & objProcess.WorkingSetSize
    Wscript.Echo &quot;Page File Size: &quot; & objProcess.PageFileUsage
    Wscript.Echo &quot;Page Faults: &quot; & objProcess.PageFaults
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11c1c-149">PowerShell</span><span class="sxs-lookup"><span data-stu-id="11c1c-149">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
Get-WmiObject -Class &quot;Win32s_Process&quot; -ComputerName $strComputer | `
     Format-List -Property Name, KernelModeTime, UserModeTime, ProcessID, WorkingSetSize, PageFileUsage, PageFaults</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11c1c-150">... indiquer quelles applications s’exécutent sur un ordinateur distant ?</span><span class="sxs-lookup"><span data-stu-id="11c1c-150">...tell what applications are running on a remote computer?</span></span></td>
<td><p><span data-ttu-id="11c1c-151">Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="11c1c-151">Use the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11c1c-152">VB</span><span class="sxs-lookup"><span data-stu-id="11c1c-152">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colProcessList = objWMIService.ExecQuery (&quot;Select * from Win32_Process&quot;)
For Each objProcess in colProcessList
    Wscript.Echo &quot;Process: &quot; & objProcess.Name 
    Wscript.Echo &quot;Process ID: &quot; & objProcess.ProcessID 
    Wscript.Echo &quot;Thread Count: &quot; & objProcess.ThreadCount 
    Wscript.Echo &quot;Page File Size: &quot; & objProcess.PageFileUsage 
    Wscript.Echo &quot;Page Faults: &quot; & objProcess.PageFaults 
    Wscript.Echo &quot;Working Set Size: &quot; & objProcess.WorkingSetSize 
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11c1c-153">PowerShell</span><span class="sxs-lookup"><span data-stu-id="11c1c-153">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
get-wmiObject -class Win32_Process -Namespace &quot;root\cimv2&quot; -ComputerName $strComputer | `
   Format-list Name, ProcessID, ThreadCount, PageFileUsage, PageFaults, WorkingSetSize</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="11c1c-154">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="11c1c-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11c1c-155">Tâches WMI pour les scripts et les applications</span><span class="sxs-lookup"><span data-stu-id="11c1c-155">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="11c1c-156">Exemples d’applications WMI C++</span><span class="sxs-lookup"><span data-stu-id="11c1c-156">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="11c1c-157">ScriptCenter TechNet</span><span class="sxs-lookup"><span data-stu-id="11c1c-157">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

