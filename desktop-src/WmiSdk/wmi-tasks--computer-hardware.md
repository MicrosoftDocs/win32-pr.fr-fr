---
description: Les tâches WMI pour le matériel informatique obtiennent des informations sur la présence, l’État ou les propriétés de composants matériels.
ms.assetid: eb4c2c38-4853-4486-b889-93a843d88edb
ms.tgt_platform: multiple
title: 'Tâches WMI : matériel de l’ordinateur'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d5589c634a5a7bf11b95bc2d90ebeab038eb8af0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533828"
---
# <a name="wmi-tasks-computer-hardware"></a><span data-ttu-id="9e9c5-103">Tâches WMI : matériel de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="9e9c5-103">WMI Tasks: Computer Hardware</span></span>

<span data-ttu-id="9e9c5-104">Les tâches WMI pour le matériel informatique obtiennent des informations sur la présence, l’État ou les propriétés de composants matériels.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-104">WMI tasks for computer hardware obtain information about the presence, state, or properties of hardware components.</span></span> <span data-ttu-id="9e9c5-105">Par exemple, vous pouvez déterminer si un ordinateur est un ordinateur de bureau ou un ordinateur portable.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-105">For example, you can determine whether a computer is a desktop or laptop.</span></span> <span data-ttu-id="9e9c5-106">Pour obtenir d’autres exemples, consultez le site TechNet ScriptCenter à l’adresse [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="9e9c5-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="9e9c5-107">Les exemples de scripts présentés dans cette rubrique obtiennent des données uniquement à partir de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="9e9c5-108">Pour plus d’informations sur l’utilisation du script pour obtenir des données à partir d’ordinateurs distants, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="9e9c5-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

## <a name="to-run-a-script"></a><span data-ttu-id="9e9c5-109">Pour exécuter un script</span><span class="sxs-lookup"><span data-stu-id="9e9c5-109">To run a script</span></span>

<span data-ttu-id="9e9c5-110">La procédure suivante décrit comment exécuter un script.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-110">The following procedure describes how to run a script.</span></span>

1.  <span data-ttu-id="9e9c5-111">Copiez le code et enregistrez-le dans un fichier avec une extension. vbs, par exemple *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="9e9c5-112">Assurez-vous que votre éditeur de texte n’ajoute pas d’extension. txt au fichier.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="9e9c5-113">Ouvrez une fenêtre d’invite de commandes et accédez au répertoire où vous avez enregistré le fichier.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="9e9c5-114">Tapez **cscript filename.vbs** à l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="9e9c5-115">Si vous ne pouvez pas accéder à un journal des événements, vérifiez si vous exécutez à partir d’une invite de commandes avec élévation de privilèges.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="9e9c5-116">Certains journaux des événements, tels que le journal des événements de sécurité, peuvent être protégés par les contrôles d’accès utilisateur (UAC).</span><span class="sxs-lookup"><span data-stu-id="9e9c5-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="9e9c5-117">Par défaut, cscript affiche la sortie d’un script dans la fenêtre d’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="9e9c5-118">Étant donné que les scripts WMI peuvent générer de grandes quantités de sortie, vous souhaiterez peut-être rediriger la sortie vers un fichier.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="9e9c5-119">Tapez **cscript filename.vbs > outfile.txt** à l’invite de commandes pour rediriger la sortie du script *filename.vbs* vers *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="9e9c5-120">Le tableau suivant répertorie des exemples de scripts qui peuvent être utilisés pour obtenir différents types de données à partir de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9e9c5-121">Comment puis-je...</span><span class="sxs-lookup"><span data-stu-id="9e9c5-121">How do I...</span></span></th>
<th><span data-ttu-id="9e9c5-122">Classes ou méthodes WMI</span><span class="sxs-lookup"><span data-stu-id="9e9c5-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9e9c5-123">... déterminer la quantité de mémoire disponible d’un ordinateur</span><span class="sxs-lookup"><span data-stu-id="9e9c5-123">...determine how much free memory a computer has?</span></span></td>
<td><span data-ttu-id="9e9c5-124">Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> et la propriété <strong>FreePhysicalMemory</strong> .</span><span class="sxs-lookup"><span data-stu-id="9e9c5-124">Use the class <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> and the <strong>FreePhysicalMemory</strong> property.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9e9c5-125">VB</span><span class="sxs-lookup"><span data-stu-id="9e9c5-125">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colSettings = objWMIService.ExecQuery(&quot;Select * from Win32_OperatingSystem&quot;)
For Each objOperatingSystem in colSettings 
    Wscript.Echo &quot;Available Physical Memory: &quot; & objOperatingSystem.FreePhysicalMemory
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
<th><span data-ttu-id="9e9c5-126">PowerShell</span><span class="sxs-lookup"><span data-stu-id="9e9c5-126">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$mem = Get-WmiObject -Class Win32_OperatingSystem
&quot;System : {0}&quot; -f $mem.csname
&quot;Free Memory: {0}&quot; -f $mem.FreePhysicalMemory</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="9e9c5-127">... déterminer si un ordinateur dispose d’un lecteur de DVD ?</span><span class="sxs-lookup"><span data-stu-id="9e9c5-127">...determine whether a computer has a DVD drive?</span></span></td>
<td><p><span data-ttu-id="9e9c5-128">Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-cdromdrive"><strong>Win32_CDROMDrive</strong></a> et recherchez l’acronyme DVD dans la propriété <strong>Name</strong> ou <strong>DeviceID</strong> .</span><span class="sxs-lookup"><span data-stu-id="9e9c5-128">Use the <a href="/windows/desktop/CIMWin32Prov/win32-cdromdrive"><strong>Win32_CDROMDrive</strong></a> class and check for the acronym DVD in the <strong>Name</strong> or <strong>DeviceID</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9e9c5-129">VB</span><span class="sxs-lookup"><span data-stu-id="9e9c5-129">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject( &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_CDROMDrive&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Device ID: &quot; & objItem.DeviceID
    Wscript.Echo &quot;Description: &quot; & objItem.Description
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
<th><span data-ttu-id="9e9c5-130">PowerShell</span><span class="sxs-lookup"><span data-stu-id="9e9c5-130">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$drives = Get-WmiObject -Class Win32_CDROMDrives
$drives | Format-Table DeviceID, Description, Name -autosize</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9e9c5-131">... déterminer la quantité de RAM installée sur un ordinateur</span><span class="sxs-lookup"><span data-stu-id="9e9c5-131">...determine how much RAM is installed in a computer?</span></span></td>
<td><p><span data-ttu-id="9e9c5-132">Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> et vérifiez la valeur de la propriété <strong>TotalPhysicalMemory</strong> .</span><span class="sxs-lookup"><span data-stu-id="9e9c5-132">Use the <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> class and check the value of the <strong>TotalPhysicalMemory</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9e9c5-133">VB</span><span class="sxs-lookup"><span data-stu-id="9e9c5-133">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colSettings = objWMIService.ExecQuery(&quot;Select * from Win32_ComputerSystem&quot;)
For Each objComputer in colSettings 
    Wscript.Echo &quot;System Name: &quot; & objComputer.Name
    Wscript.Echo &quot;Total Physical Memory: &quot; & objComputer.TotalPhysicalMemory
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
<th><span data-ttu-id="9e9c5-134">PowerShell</span><span class="sxs-lookup"><span data-stu-id="9e9c5-134">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$mem = Get-WmiObject -Class Win32_ComputerSystem</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9e9c5-135">... déterminer si un ordinateur a plus d’un processeur ?</span><span class="sxs-lookup"><span data-stu-id="9e9c5-135">...determine if a computer has more than one processor?</span></span></td>
<td><p><span data-ttu-id="9e9c5-136">Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> et la propriété <strong>NumberOfProcessors</strong>.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-136">Use the <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> class and the property <strong>NumberOfProcessors</strong>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9e9c5-137">VB</span><span class="sxs-lookup"><span data-stu-id="9e9c5-137">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colSettings = objWMIService.ExecQuery(&quot;Select * from Win32_ComputerSystem&quot;)
For Each objComputer in colSettings 
    Wscript.Echo &quot;System Name: &quot; & objComputer.Name
    Wscript.Echo &quot;Number of Processors: &quot; & objComputer.NumberOfProcessors
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
<th><span data-ttu-id="9e9c5-138">PowerShell</span><span class="sxs-lookup"><span data-stu-id="9e9c5-138">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>&quot;System Name : {0}&quot; -f $system.Name
&quot;Number of Processors: {0}&quot; -f $system.NumberOfProcessors</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9e9c5-139">... déterminer si un ordinateur dispose d’un emplacement PCMCIA ?</span><span class="sxs-lookup"><span data-stu-id="9e9c5-139">...determine whether a computer has a PCMCIA slot?</span></span></td>
<td><p><span data-ttu-id="9e9c5-140">Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-pcmciacontroller"><strong>Win32_PCMCIAController</strong></a> et vérifiez la valeur de la propriété <strong>Count</strong> .</span><span class="sxs-lookup"><span data-stu-id="9e9c5-140">Use the <a href="/windows/desktop/CIMWin32Prov/win32-pcmciacontroller"><strong>Win32_PCMCIAController</strong></a> class and check the value of the <strong>Count</strong> property.</span></span> <span data-ttu-id="9e9c5-141">Si <strong>Count</strong> a la valeur 0, cela signifie que l’ordinateur n’a pas d’emplacement PCMCIA.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-141">If <strong>Count</strong> is 0, then the computer has no PCMCIA slots.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9e9c5-142">VB</span><span class="sxs-lookup"><span data-stu-id="9e9c5-142">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_PCMCIAController&quot;)
Wscript.Echo &quot;Number of PCMCIA slots: &quot; & colItems.Count</code></pre></td>
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
<th><span data-ttu-id="9e9c5-143">PowerShell</span><span class="sxs-lookup"><span data-stu-id="9e9c5-143">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$Pcmcia = Get-WmiObject -Class Win32_PCMCIAController

if (!$pcmcia.count) {
    &quot;Number of PCMCIA Slots: {0}&quot; -f 1
}else {
    &quot;Number of PCMCIA Slots: {0}&quot; -f $pcmcia.count
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9e9c5-144">... identifier les appareils qui ne fonctionnent pas (ceux marqués d’une icône de point d’exclamation dans <strong>Gestionnaire de périphériques</strong>) ?</span><span class="sxs-lookup"><span data-stu-id="9e9c5-144">...identify devices that are not working (those marked with an exclamation point icon in <strong>Device Manager</strong>)?</span></span></td>
<td><p><span data-ttu-id="9e9c5-145">Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-pnpentity"><strong>Win32_PnPEntity</strong></a> et utilisez la clause suivante dans votre requête <a href="querying-with-wql.md">WQL</a> .</span><span class="sxs-lookup"><span data-stu-id="9e9c5-145">Use the <a href="/windows/desktop/CIMWin32Prov/win32-pnpentity"><strong>Win32_PnPEntity</strong></a> class and use the following clause in your <a href="querying-with-wql.md">WQL</a> query.</span></span> <span data-ttu-id="9e9c5-146"><strong>Où ConfigManagerErrorCode <> 0</strong> Notez que ce code peut ne pas détecter les périphériques USB qui manquent de pilotes.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-146"><strong>WHERE ConfigManagerErrorCode <> 0</strong> Note that this code may not detect USB devices that are missing drivers.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9e9c5-147">VB</span><span class="sxs-lookup"><span data-stu-id="9e9c5-147">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_PnPEntity WHERE ConfigManagerErrorCode <> 0&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Class GUID: &quot; & objItem.ClassGuid
    Wscript.Echo &quot;Description: &quot; & objItem.Description
    Wscript.Echo &quot;Device ID: &quot; & objItem.DeviceID
    Wscript.Echo &quot;Manufacturer: &quot; & objItem.Manufacturer
    Wscript.Echo &quot;Name: &quot; & objItem.Name
    Wscript.Echo &quot;PNP Device ID: &quot; & objItem.PNPDeviceID
    Wscript.Echo &quot;Service: &quot; & objItem.Service
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
<th><span data-ttu-id="9e9c5-148">PowerShell</span><span class="sxs-lookup"><span data-stu-id="9e9c5-148">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$baddevices = Get-WmiObject Win32_PNPEntity | where {$_.ConfigManagerErrorcode -ne 0}
&quot; Total Bad devices: {0}&quot; -f $baddevices.count
foreach ($device in $baddevices) {
    &quot;Name : {0}&quot; -f $device.name
    &quot;Class Guid : {0}&quot; -f $device.Classguid
    &quot;Description : {0}&quot; -f $device.Description
    &quot;Device ID : {0}&quot; -f $device.deviceid
    &quot;Manufacturer : {0}&quot; -f $device.manufactuer
    &quot;PNP Devcice Id : {0}&quot; -f $device.PNPDeviceID
    &quot;Service Name : {0}&quot; -f $device.service
    &quot;&quot;
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9e9c5-149">... déterminer les propriétés de la souris utilisée sur l’ordinateur ?</span><span class="sxs-lookup"><span data-stu-id="9e9c5-149">...determine the properties of the mouse used on computer?</span></span></td>
<td><p><span data-ttu-id="9e9c5-150">Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-pointingdevice"><strong>Win32_PointingDevice</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="9e9c5-150">Use the <a href="/windows/desktop/CIMWin32Prov/win32-pointingdevice"><strong>Win32_PointingDevice</strong></a> class.</span></span> <span data-ttu-id="9e9c5-151">Cela retourne les propriétés de tous les dispositifs de pointage, pas seulement les périphériques souris.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-151">This returns the properties of all pointing devices, not just mouse devices.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9e9c5-152">VB</span><span class="sxs-lookup"><span data-stu-id="9e9c5-152">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_PointingDevice&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Description: &quot; & objItem.Description
    Wscript.Echo &quot;Device ID: &quot; & objItem.DeviceID
    Wscript.Echo &quot;Device Interface: &quot; & objItem.DeviceInterface
    Wscript.Echo &quot;Double Speed Threshold: &quot; & objItem.DoubleSpeedThreshold
    Wscript.Echo &quot;Handedness: &quot; & objItem.Handedness
    Wscript.Echo &quot;Hardware Type: &quot; & objItem.HardwareType
    Wscript.Echo &quot;INF File Name: &quot; & objItem.InfFileName
    Wscript.Echo &quot;INF Section: &quot; & objItem.InfSection
    Wscript.Echo &quot;Manufacturer: &quot; & objItem.Manufacturer
    Wscript.Echo &quot;Name: &quot; & objItem.Name
    Wscript.Echo &quot;Number Of Buttons: &quot; & objItem.NumberOfButtons
    Wscript.Echo &quot;PNP Device ID: &quot; & objItem.PNPDeviceID
    Wscript.Echo &quot;Pointing Type: &quot; & objItem.PointingType
    Wscript.Echo &quot;Quad Speed Threshold: &quot; & objItem.QuadSpeedThreshold
    Wscript.Echo &quot;Resolution: &quot; & objItem.Resolution
    Wscript.Echo &quot;Sample Rate: &quot; & objItem.SampleRate
    Wscript.Echo &quot;Synch: &quot; & objItem.Synch
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
<th><span data-ttu-id="9e9c5-153">PowerShell</span><span class="sxs-lookup"><span data-stu-id="9e9c5-153">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code># Get Mouse information

$mouse = Get-WmiObject -Class Win32_PointingDevice

<# Decode detalis #>

function Deviceinterface {
    param ($value)
    switch ($value) {
        0 {&quot;Other&quot;}
        1 {&quot;Unknown&quot;}
        3 {&quot;Serial&quot;}
        4 {&quot;PS/2&quot;}
        5 {&quot;Infrared&quot;}
        6 {&quot;HP-HIL&quot;}
        7 {&quot;Bus Mouse&quot;}
        8 {&quot;ADP (Apple Desktop Bus)&quot;}
        160 {&quot;Bus Mouse DB-9&quot;}
        161 {&quot;Bus Mouse Micro-DIN&quot;}
        162 {&quot;USB&quot;}
    }
}

function Handedness {
    param ($value)
    switch ($value) {
        0 {&quot;Unknown&quot;}
        1 {&quot;Not Applicable&quot;}
        2 {&quot;Right-Handed Operation&quot;}
        3 {&quot;Left-Handed Operation&quot;}
    }
}

function Pointingtype {

param ($value)
    switch ($value) {
        1 {&quot;Other&quot;}
        2 {&quot;Unknown&quot;}
        3 {&quot;Mouse&quot;}
        4 {&quot;Track Ball&quot;}
        5 {&quot;Track Point&quot;}
        6 {&quot;Glide Point&quot;}
        7 {&quot;Touch Pad&quot;}
        8 {&quot;Touch Screen&quot;}
        9 {&quot;Mouse - Optical Sensor&quot;}
    }
}

<# Display details #>

&quot;Mouse Information on System: {0}&quot; -f $mouse.systemname
&quot;Description : {0}&quot; -f $mouse.Description
&quot;Device ID : {0}&quot; -f $mouse.DeviceID
&quot;Device Interface : {0}&quot; -f (Deviceinterface($mouse.DeviceInterface))
&quot;Double Speed Threshold : {0}&quot; -f $mouse.DoubleSpeedThreshold
&quot;Handedness : {0}&quot; -f (Handedness($mouse.handedness))
&quot;Hardware Type : {0}&quot; -f $mouse.Hardwaretype
&quot;INF FIle Name : {0}&quot; -f $mouse.InfFileName
&quot;Inf Section : {0}&quot; -f $mouse.InfSection
&quot;Manufacturer : {0}&quot; -f $mouse.Manufacturer
&quot;Name : {0}&quot; -f $mouse.Name
&quot;Number of buttons : {0}&quot; -f $mouse.NumberOfButtons
&quot;PNP Device ID : {0}&quot; -f $mouse.PNPDeviceID
&quot;Pointing Type : {0}&quot; -f (Pointingtype ($mouse.PointingType))
&quot;Quad Speed Threshold : {0}&quot; -f $mouse.QuadSpeedThreshold
&quot;Resolution : {0}&quot; -f $mouse.Resolution
&quot;Sample Rate : {0}&quot; -f $mouse.SampleRate
&quot;Synch : {0}&quot; -f $mouse.Synch</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9e9c5-154">... déterminer la vitesse d’un processeur installé sur un ordinateur</span><span class="sxs-lookup"><span data-stu-id="9e9c5-154">...determine the speed of a processor installed in a computer?</span></span></td>
<td><p><span data-ttu-id="9e9c5-155">Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-processor"><strong>Win32_Processor</strong></a> et vérifiez la valeur de la propriété <strong>MaxClockSpeed</strong> .</span><span class="sxs-lookup"><span data-stu-id="9e9c5-155">Use the <a href="/windows/desktop/CIMWin32Prov/win32-processor"><strong>Win32_Processor</strong></a> class and check the value of the <strong>MaxClockSpeed</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9e9c5-156">VB</span><span class="sxs-lookup"><span data-stu-id="9e9c5-156">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_Processor&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Processor Id: &quot; & objItem.ProcessorId
    Wscript.Echo &quot;Maximum Clock Speed: &quot; & objItem.MaxClockSpeed
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9e9c5-157">... déterminer si un ordinateur est une tour, une mini-tour, un ordinateur portable, etc. ?</span><span class="sxs-lookup"><span data-stu-id="9e9c5-157">...determine whether a computer is a tower, a mini-tower, a laptop, and so on?</span></span></td>
<td><p><span data-ttu-id="9e9c5-158">Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-systemenclosure"><strong>Win32_SystemEnclosure</strong></a> et vérifiez la valeur de la propriété <strong>ChassisType</strong> .</span><span class="sxs-lookup"><span data-stu-id="9e9c5-158">Use the <a href="/windows/desktop/CIMWin32Prov/win32-systemenclosure"><strong>Win32_SystemEnclosure</strong></a> class and check the value of the <strong>ChassisType</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9e9c5-159">VB</span><span class="sxs-lookup"><span data-stu-id="9e9c5-159">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colChassis = objWMIService.ExecQuery(&quot;Select * from Win32_SystemEnclosure&quot;)
For Each objChassis in colChassis
    For Each objItem in objChassis.ChassisTypes
        Wscript.Echo &quot;Chassis Type: &quot; & objItem
    Next
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
<th><span data-ttu-id="9e9c5-160">PowerShell</span><span class="sxs-lookup"><span data-stu-id="9e9c5-160">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$processors = Get-WmiObject -Class Win32_Processor
foreach ($proc in $processors)
{
    &quot;Processor ID: &quot; + $proc.ProcessorID
    &quot;Maximum Clock Speed: &quot; + $proc.MaxClockSpeed
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9e9c5-161">... obtenir le numéro de série et l’étiquette d’inventaire d’un ordinateur ?</span><span class="sxs-lookup"><span data-stu-id="9e9c5-161">...get the serial number and asset tag of a computer?</span></span></td>
<td><p><span data-ttu-id="9e9c5-162">Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-systemenclosure"><strong>Win32_SystemEnclosure</strong></a> et les propriétés <strong>SerialNumber</strong> et <strong>SMBIOSAssetTag</strong>.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-162">Use the <a href="/windows/desktop/CIMWin32Prov/win32-systemenclosure"><strong>Win32_SystemEnclosure</strong></a> class, and the properties <strong>SerialNumber</strong> and <strong>SMBIOSAssetTag</strong>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9e9c5-163">VB</span><span class="sxs-lookup"><span data-stu-id="9e9c5-163">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colSMBIOS = objWMIService.ExecQuery(&quot;Select * from Win32_SystemEnclosure&quot;)
For Each objSMBIOS in colSMBIOS
    Wscript.Echo &quot;Part Number: &quot; & objSMBIOS.PartNumber
    Wscript.Echo &quot;Serial Number: &quot; & objSMBIOS.SerialNumber
    Wscript.Echo &quot;Asset Tag: &quot; & objSMBIOS.SMBIOSAssetTag
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
<th><span data-ttu-id="9e9c5-164">PowerShell</span><span class="sxs-lookup"><span data-stu-id="9e9c5-164">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$colSMBIOS = Get-WmiObject -Class Win32_SystemEnclosure

foreach ($objSMBIOS in $colSMBIOS)
{
    &quot;Part Number: &quot; + $objSMBIOS.PartNumber
    &quot;Serial Number: &quot; + $objSMBIOS.SerialNumber
    &quot;Asset Tag: &quot; + $objSMBIOS.SMBIOSAssetTag
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9e9c5-165">... déterminer le type d’appareil branché sur un port USB</span><span class="sxs-lookup"><span data-stu-id="9e9c5-165">...determine what kind of device is plugged into a USB port?</span></span></td>
<td><p><span data-ttu-id="9e9c5-166">Utilisez la classe <a href="/previous-versions/windows/desktop/cimwin32a/win32-usbhub"><strong>Win32_USBHub</strong></a> et vérifiez la propriété <strong>Description</strong> .</span><span class="sxs-lookup"><span data-stu-id="9e9c5-166">Use the <a href="/previous-versions/windows/desktop/cimwin32a/win32-usbhub"><strong>Win32_USBHub</strong></a> class and check the <strong>Description</strong> property.</span></span> <span data-ttu-id="9e9c5-167">Cette propriété peut avoir une valeur telle que &quot; dispositif de stockage de masse &quot; ou &quot; prise en charge de l’impression &quot; .</span><span class="sxs-lookup"><span data-stu-id="9e9c5-167">This property may have a value such as &quot;Mass Storage Device&quot; or &quot;Printing Support&quot;.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9e9c5-168">VB</span><span class="sxs-lookup"><span data-stu-id="9e9c5-168">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_USBHub&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Device ID: &quot; & objItem.DeviceID
    Wscript.Echo &quot;PNP Device ID: &quot; & objItem.PNPDeviceID
    Wscript.Echo &quot;Description: &quot; & objItem.Description
    Wscript.Echo
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
<th><span data-ttu-id="9e9c5-169">PowerShell</span><span class="sxs-lookup"><span data-stu-id="9e9c5-169">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$colItems = Get-WmiObject -Class Win32_USBHub

foreach ($objItem in $colItems)
{
    &quot;Device ID: &quot; + $objItem.DeviceID
    &quot;PNP Device ID: &quot; + $objItem.PNPDeviceID
    &quot;Description: &quot; + $objItem.Description
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9e9c5-170">... déterminer le nombre de lecteurs de bande installés sur un ordinateur</span><span class="sxs-lookup"><span data-stu-id="9e9c5-170">...determine how many tape drives are installed on a computer?</span></span></td>
<td><p><span data-ttu-id="9e9c5-171">Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-tapedrive"><strong>Win32_TapeDrive</strong></a> classe, puis utilisez la méthode <a href="swbemobjectset-count.md"><strong>SWbemObjectSet. Count</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="9e9c5-171">Use the class <a href="/windows/desktop/CIMWin32Prov/win32-tapedrive"><strong>Win32_TapeDrive</strong></a> class and then use the <a href="swbemobjectset-count.md"><strong>SWbemObjectSet.Count</strong></a> method.</span></span> <span data-ttu-id="9e9c5-172">Si Count = 0, aucun lecteur de bande n’est installé sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-172">If Count = 0, then no tape drives are installed on the computer.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9e9c5-173">VB</span><span class="sxs-lookup"><span data-stu-id="9e9c5-173">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_TapeDrive&quot;)
Wscript.Echo &quot;Number of tape drives: &quot; & colItems.Count</code></pre></td>
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
<th><span data-ttu-id="9e9c5-174">PowerShell</span><span class="sxs-lookup"><span data-stu-id="9e9c5-174">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$colItems = Get-WmiObject -Class Win32_TapeDrive

foreach ($objItem in $colItems)
{
    &quot;Number of Drives: &quot; + $colItems.Count
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a><span data-ttu-id="9e9c5-175">Exemples</span><span class="sxs-lookup"><span data-stu-id="9e9c5-175">Examples</span></span>

<span data-ttu-id="9e9c5-176">L' [exemple de code](https://Gallery.TechNet.Microsoft.Com/scriptcenter/List-for-several-machines-1baf6df0) de la Galerie TechNet suivant décrit comment répertorier l’espace libre de tous les lecteurs pour plusieurs ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-176">The following TechNet Gallery [example code](https://Gallery.TechNet.Microsoft.Com/scriptcenter/List-for-several-machines-1baf6df0) describes how to list the free space of all drives for several machines.</span></span>

<span data-ttu-id="9e9c5-177">L’exemple PowerShell- [ComputerInfo-Query Computer Info from local/Remote Computers-(WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sur la Galerie TechNet utilise un certain nombre d’appels au matériel et aux logiciels pour afficher des informations sur un système local ou distant.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-177">The [Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sample on TechNet Gallery uses a number of calls to hardware and software to display information about a local or remote system.</span></span>

<span data-ttu-id="9e9c5-178">L’exemple de [collecte des ressources système multithread avec](https://Gallery.TechNet.Microsoft.Com/Multithreaded-System-Asset-856a8f7c) PowerShell PowerShell sur TechNetGallery rassemble une multitude d’informations utiles sur le système via WMI et le multithread avec PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9e9c5-178">The [Multithreaded System Asset Gathering with Powershell](https://Gallery.TechNet.Microsoft.Com/Multithreaded-System-Asset-856a8f7c) PowerShell sample on TechNetGallery gathers a plethora of useful system information via WMI and multithreading with powershell.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e9c5-179">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9e9c5-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e9c5-180">Tâches WMI pour les scripts et les applications</span><span class="sxs-lookup"><span data-stu-id="9e9c5-180">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="9e9c5-181">Exemples d’applications WMI C++</span><span class="sxs-lookup"><span data-stu-id="9e9c5-181">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="9e9c5-182">ScriptCenter TechNet</span><span class="sxs-lookup"><span data-stu-id="9e9c5-182">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

