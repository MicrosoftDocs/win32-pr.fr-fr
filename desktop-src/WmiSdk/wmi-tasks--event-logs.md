---
description: Les tâches WMI pour les journaux des événements obtiennent des données d’événement à partir de fichiers journaux d’événements et effectuent des opérations telles que la sauvegarde ou l’effacement des fichiers journaux. Pour obtenir d’autres exemples, consultez le site TechNet ScriptCenter à l’adresse https://www.microsoft.com/technet .
ms.assetid: f6d4e68e-d757-44aa-be74-3b26168626b8
ms.tgt_platform: multiple
title: 'Tâches WMI : Journaux des événements'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8fdcfe3f547e58fa60e552abad9867f8556fc8b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524992"
---
# <a name="wmi-tasks-event-logs"></a><span data-ttu-id="8f1a8-104">Tâches WMI : Journaux des événements</span><span class="sxs-lookup"><span data-stu-id="8f1a8-104">WMI Tasks: Event Logs</span></span>

<span data-ttu-id="8f1a8-105">Les tâches WMI pour les journaux des événements obtiennent des données d’événement à partir de fichiers journaux d’événements et effectuent des opérations telles que la sauvegarde ou l’effacement des fichiers journaux.</span><span class="sxs-lookup"><span data-stu-id="8f1a8-105">WMI tasks for event logs obtain event data from event log files and perform operations like backing up or clearing log files.</span></span> <span data-ttu-id="8f1a8-106">Pour obtenir d’autres exemples, consultez le site TechNet ScriptCenter à l’adresse [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="8f1a8-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="8f1a8-107">Les exemples de scripts présentés dans cette rubrique obtiennent des données uniquement à partir de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="8f1a8-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="8f1a8-108">Pour plus d’informations sur l’utilisation du script pour obtenir des données à partir d’ordinateurs distants, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="8f1a8-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="8f1a8-109">La procédure suivante décrit comment exécuter un script.</span><span class="sxs-lookup"><span data-stu-id="8f1a8-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="8f1a8-110">**Pour exécuter un script**</span><span class="sxs-lookup"><span data-stu-id="8f1a8-110">**To run a script**</span></span>

1.  <span data-ttu-id="8f1a8-111">Copiez le code et enregistrez-le dans un fichier avec une extension. vbs, par exemple *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="8f1a8-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="8f1a8-112">Assurez-vous que votre éditeur de texte n’ajoute pas d’extension. txt au fichier.</span><span class="sxs-lookup"><span data-stu-id="8f1a8-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="8f1a8-113">Ouvrez une fenêtre d’invite de commandes et accédez au répertoire où vous avez enregistré le fichier.</span><span class="sxs-lookup"><span data-stu-id="8f1a8-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="8f1a8-114">Tapez **cscript filename.vbs** à l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="8f1a8-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="8f1a8-115">Si vous ne pouvez pas accéder à un journal des événements, vérifiez si vous exécutez à partir d’une invite de commandes avec élévation de privilèges.</span><span class="sxs-lookup"><span data-stu-id="8f1a8-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="8f1a8-116">Certains journaux des événements, tels que le journal des événements de sécurité, peuvent être protégés par les contrôles d’accès utilisateur (UAC).</span><span class="sxs-lookup"><span data-stu-id="8f1a8-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="8f1a8-117">Par défaut, cscript affiche la sortie d’un script dans la fenêtre d’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="8f1a8-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="8f1a8-118">Étant donné que les scripts WMI peuvent générer de grandes quantités de sortie, vous souhaiterez peut-être rediriger la sortie vers un fichier.</span><span class="sxs-lookup"><span data-stu-id="8f1a8-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="8f1a8-119">Tapez **cscript filename.vbs > outfile.txt** à l’invite de commandes pour rediriger la sortie du script *filename.vbs* vers *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="8f1a8-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="8f1a8-120">Le tableau suivant répertorie des exemples de scripts qui peuvent être utilisés pour obtenir différents types de données à partir de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="8f1a8-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8f1a8-121">Comment puis-je...</span><span class="sxs-lookup"><span data-stu-id="8f1a8-121">How do I...</span></span></th>
<th><span data-ttu-id="8f1a8-122">Classes ou méthodes WMI</span><span class="sxs-lookup"><span data-stu-id="8f1a8-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8f1a8-123">... récupérer les informations sur le journal des événements de sécurité ?</span><span class="sxs-lookup"><span data-stu-id="8f1a8-123">...retrieve information about the Security event log?</span></span></td>
<td><span data-ttu-id="8f1a8-124">Incluez le privilège de <a href="privilege-constants.md">sécurité</a> lors de la connexion à la classe <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventLogFile</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8f1a8-124">Include the <a href="privilege-constants.md">Security</a> privilege when connecting to the <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> class.</span></span> <span data-ttu-id="8f1a8-125">Pour plus d’informations, consultez <a href="executing-privileged-operations-using-vbscript.md">exécution d’opérations privilégiées à l’aide de VBScript</a>.</span><span class="sxs-lookup"><span data-stu-id="8f1a8-125">For more information, see <a href="executing-privileged-operations-using-vbscript.md">Executing Privileged Operations Using VBScript</a>.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8f1a8-126">VB</span><span class="sxs-lookup"><span data-stu-id="8f1a8-126">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate,(Security)}!\\&quot; & _
        strComputer & &quot;\root\cimv2&quot;)
Set colLogFiles = objWMIService.ExecQuery _
    (&quot;Select * from Win32_NTEventLogFile &quot; _
        & &quot;Where LogFileName=&#39;Security&#39;&quot;)
For Each objLogFile in colLogFiles
    Wscript.Echo objLogFile.NumberOfRecords
    Wscript.Echo &quot;Maximum Size: &quot; _
    &  objLogfile.MaxFileSize 
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
<th><span data-ttu-id="8f1a8-127">PowerShell</span><span class="sxs-lookup"><span data-stu-id="8f1a8-127">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colLogFiles = Get-WmiObject -Class Win32_NTEventLogFile -ComputerName $strComputer | Where-Object {$_.LogFileName -eq &#39;security&#39;}
foreach ($objLogFile in $colLogFiles) 
{ 
    &quot;Record Number: &quot; + $objLogFile.NumberOfRecords
    &quot;Maximum Size: &quot; + $objLogFile.MaxFileSize
}</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="8f1a8-128">... sauvegarder un journal des événements ?</span><span class="sxs-lookup"><span data-stu-id="8f1a8-128">...back up an event log?</span></span></td>
<td><p><span data-ttu-id="8f1a8-129">Utilisez la classe <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventLogFile</strong></a> et la méthode <a href="/previous-versions/windows/desktop/eventlogprov/backupeventlog-method-in-class-win32-nteventlogfile"><strong>BackupEventLog</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8f1a8-129">Use the <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> class and the <a href="/previous-versions/windows/desktop/eventlogprov/backupeventlog-method-in-class-win32-nteventlogfile"><strong>BackupEventLog</strong></a> method.</span></span> <span data-ttu-id="8f1a8-130">Vous devrez peut-être inclure le privilège de <a href="privilege-constants.md">sauvegarde</a> lors de la connexion à WMI.</span><span class="sxs-lookup"><span data-stu-id="8f1a8-130">You may need to include the <a href="privilege-constants.md">Backup</a> privilege when connecting to WMI.</span></span> <span data-ttu-id="8f1a8-131">Pour plus d’informations, consultez <a href="executing-privileged-operations-using-vbscript.md">exécution d’opérations privilégiées à l’aide de VBScript</a>.</span><span class="sxs-lookup"><span data-stu-id="8f1a8-131">For more information, see <a href="executing-privileged-operations-using-vbscript.md">Executing Privileged Operations Using VBScript</a>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8f1a8-132">VB</span><span class="sxs-lookup"><span data-stu-id="8f1a8-132">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate,(Backup)}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colLogFiles = objWMIService.ExecQuery (&quot;Select * from Win32_NTEventLogFile &quot; & &quot;Where LogFileName=&#39;Application&#39;&quot;)
For Each objLogfile in colLogFiles
    errBackupLog = objLogFile.BackupEventLog(&quot;c:\scripts\application.evt&quot;)
    WScript.Echo &quot;File saved as c:\scripts\applications.evt&quot;
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
<th><span data-ttu-id="8f1a8-133">PowerShell</span><span class="sxs-lookup"><span data-stu-id="8f1a8-133">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colLogFiles = Get-WmiObject -Class Win32_NTEventLogFile -ComputerName $strComputer | Where-Object {$_.LogFileName -eq &#39;Application&#39;}

foreach ($objLogFile in $colLogFiles) 
{ 
    [void]$objLogFile.BackupEventlog(&quot;c:\scripts\applications.evt&quot;)
    &quot;File saved as c:\scripts\applications.evt&quot;
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8f1a8-134">... sauvegarder un journal des événements plusieurs fois ?</span><span class="sxs-lookup"><span data-stu-id="8f1a8-134">...back up an event log more than once?</span></span></td>
<td><p><span data-ttu-id="8f1a8-135">Assurez-vous que le fichier de sauvegarde a un nom unique avant d’utiliser les <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventLogFile</strong></a> et la méthode <a href="/previous-versions/windows/desktop/eventlogprov/backupeventlog-method-in-class-win32-nteventlogfile"><strong>BackupEventLog</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8f1a8-135">Ensure that the backup file has a unique name before using the <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> and the <a href="/previous-versions/windows/desktop/eventlogprov/backupeventlog-method-in-class-win32-nteventlogfile"><strong>BackupEventLog</strong></a> method.</span></span> <span data-ttu-id="8f1a8-136">Le système d’exploitation ne vous permet pas de remplacer un fichier de sauvegarde existant ; vous devez soit déplacer le fichier de sauvegarde, soit le renommer avant de pouvoir réexécuter le script.</span><span class="sxs-lookup"><span data-stu-id="8f1a8-136">The operating system does not allow you to overwrite an existing backup file; you must either move the backup file or rename it before you can run the script again.</span></span> <span data-ttu-id="8f1a8-137">Vous devrez peut-être inclure le privilège de <a href="privilege-constants.md">sauvegarde</a> lors de la connexion à WMI.</span><span class="sxs-lookup"><span data-stu-id="8f1a8-137">You may need to include the <a href="privilege-constants.md">Backup</a> privilege when connecting to WMI.</span></span> <span data-ttu-id="8f1a8-138">Pour plus d’informations, consultez <a href="executing-privileged-operations-using-vbscript.md">exécution d’opérations privilégiées à l’aide de VBScript</a>.</span><span class="sxs-lookup"><span data-stu-id="8f1a8-138">For more information, see <a href="executing-privileged-operations-using-vbscript.md">Executing Privileged Operations Using VBScript</a>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8f1a8-139">VB</span><span class="sxs-lookup"><span data-stu-id="8f1a8-139">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>dtmThisDay = Day(Date)
dtmThisMonth = Month(Date)
dtmThisYear = Year(Date)
strBackupName = dtmThisYear & &quot;_&quot; & dtmThisMonth & &quot;_&quot; & dtmThisDay
strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate,(Backup)}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colLogFiles = objWMIService.ExecQuery (&quot;Select * from Win32_NTEventLogFile &quot; & &quot;Where LogFileName=&#39;Application&#39;&quot;)
For Each objLogfile in colLogFiles
    objLogFile.BackupEventLog(&quot;c:\scripts\&quot; & strBackupName & &quot;_application.evt&quot;)
    objLogFile.ClearEventLog()
    WScript.Echo &quot;File saved: &quot; & strBackupName & &quot;_application.evt&quot;
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
<th><span data-ttu-id="8f1a8-140">PowerShell</span><span class="sxs-lookup"><span data-stu-id="8f1a8-140">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$CurDate = Get-Date
$strBackupName = $curDate.Year.ToString() + &quot;_&quot; + $curDate.Month.ToString() + &quot;_&quot; + $CurDate.Day.ToString()

$strComputer = &quot;.&quot;
$colLogFiles = Get-WmiObject -Class Win32_NTEventLogFile -ComputerName $strComputer | Where-Object {$_.LogFileName -eq &#39;Application&#39;}
foreach ($objLogFile in $colLogFiles) 
{ 
    $BackupFile = $objLogFile.BackupEventlog(&quot;c:\scripts\&quot; + $strBackupName + &quot;_application.evt&quot;)
    &quot;File saved: c:\scripts\&quot; + $strBackupName + &quot;_application.evt&quot;
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8f1a8-141">... déterminer le nombre d’enregistrements dans un journal des événements ?</span><span class="sxs-lookup"><span data-stu-id="8f1a8-141">...determine the number of records in an event log?</span></span></td>
<td><p><span data-ttu-id="8f1a8-142">Utilisez la classe <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventLogFile</strong></a> et vérifiez la valeur de la propriété <strong>NumberOfRecords</strong> .</span><span class="sxs-lookup"><span data-stu-id="8f1a8-142">Use the <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> class and check the value of the <strong>NumberOfRecords</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8f1a8-143">VB</span><span class="sxs-lookup"><span data-stu-id="8f1a8-143">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colLogFiles = objWMIService.ExecQuery (&quot;Select * from Win32_NTEventLogFile &quot; & &quot;Where LogFileName=&#39;System&#39;&quot;)
For Each objLogFile in colLogFiles
    Wscript.Echo objLogFile.NumberOfRecords
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
<th><span data-ttu-id="8f1a8-144">PowerShell</span><span class="sxs-lookup"><span data-stu-id="8f1a8-144">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colLogFiles = Get-WmiObject -Class Win32_NTEventLogFile -ComputerName $strComputer | Where-Object {$_.LogFileName -eq &#39;System&#39;}

foreach ($objLogFile in $colLogFiles) 
{ 
    $objLogFile.NumberOfRecords
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8f1a8-145">... Effacer mes journaux des événements ?</span><span class="sxs-lookup"><span data-stu-id="8f1a8-145">...clear my event logs?</span></span></td>
<td><p><span data-ttu-id="8f1a8-146">Utilisez la classe <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventLogFile</strong></a> et la méthode <a href="/previous-versions/windows/desktop/eventlogprov/cleareventlog-method-in-class-win32-nteventlogfile"><strong>ClearEventLog</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8f1a8-146">Use the <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> class and the <a href="/previous-versions/windows/desktop/eventlogprov/cleareventlog-method-in-class-win32-nteventlogfile"><strong>ClearEventLog</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8f1a8-147">VB</span><span class="sxs-lookup"><span data-stu-id="8f1a8-147">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate,(Backup, Security)}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colLogFiles = objWMIService.ExecQuery (&quot;Select * from Win32_NTEventLogFile &quot; & &quot;Where LogFileName=&#39;Application&#39;&quot;)
For Each objLogfile in colLogFiles
    objLogFile.ClearEventLog()
    WScript.Echo &quot;Cleared application event log file&quot;
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
<th><span data-ttu-id="8f1a8-148">PowerShell</span><span class="sxs-lookup"><span data-stu-id="8f1a8-148">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colLogFiles = Get-WmiObject -Class Win32_NTEventLogFile -ComputerName $strComputer | Where-Object {$_.LogFileName -eq &#39;System&#39;}

foreach ($objLogFile in $colLogFiles) 
{ 
    [void]$objLogFile.ClearEventlog()
    &quot;Cleared application event log file&quot;
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8f1a8-149">... lire les événements à partir des journaux des événements ?</span><span class="sxs-lookup"><span data-stu-id="8f1a8-149">...read events from the event logs?</span></span></td>
<td><p><span data-ttu-id="8f1a8-150">Utilisez la classe <a href="/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent"><strong>Win32_NTLogEvent</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8f1a8-150">Use the <a href="/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent"><strong>Win32_NTLogEvent</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8f1a8-151">VB</span><span class="sxs-lookup"><span data-stu-id="8f1a8-151">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
Set colLoggedEvents = objWMIService.ExecQuery _
    (&quot;Select * from Win32_NTLogEvent &quot; _
        & &quot;Where Logfile = &#39;System&#39;&quot;)
For Each objEvent in colLoggedEvents
    Wscript.Echo &quot;Category: &quot; & objEvent.Category & VBNewLine _
    & &quot;Computer Name: &quot; & objEvent.ComputerName & VBNewLine _
    & &quot;Event Code: &quot; & objEvent.EventCode & VBNewLine _
    & &quot;Message: &quot; & objEvent.Message & VBNewLine _
    & &quot;Record Number: &quot; & objEvent.RecordNumber & VBNewLine _
    & &quot;Source Name: &quot; & objEvent.SourceName & VBNewLine _
    & &quot;Time Written: &quot; & objEvent.TimeWritten & VBNewLine _
    & &quot;Event Type: &quot; & objEvent.Type & VBNewLine _
    & &quot;User: &quot; & objEvent.User
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
<th><span data-ttu-id="8f1a8-152">PowerShell</span><span class="sxs-lookup"><span data-stu-id="8f1a8-152">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colLogFiles = Get-WmiObject -Class Win32_NTLogEvent -ComputerName $strComputer | Where-Object {$_.LogFile -eq &#39;System&#39;}

foreach ($objEvent in $colLoggedEvents) 
{ 
    &quot;Category: &quot; + $objEvent.Category
    &quot;Computer Name: &quot; + $objEvent.ComputerName
    &quot;Event Code: &quot; + $objEvent.EventCode
    &quot;Message: &quot; + $objEvent.Message
    &quot;Record Number: &quot; + $objEvent.RecordNumber
    &quot;Source Name: &quot; + $objEvent.SourceName
    &quot;Time Written: &quot; + $objEvent.TimeWritten
    &quot;Event Type: &quot; + $objEvent.Type
    &quot;User: &quot; + $objEvent.Use
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="8f1a8-153">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8f1a8-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f1a8-154">Tâches WMI pour les scripts et les applications</span><span class="sxs-lookup"><span data-stu-id="8f1a8-154">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="8f1a8-155">Exemples d’applications WMI C++</span><span class="sxs-lookup"><span data-stu-id="8f1a8-155">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="8f1a8-156">ScriptCenter TechNet</span><span class="sxs-lookup"><span data-stu-id="8f1a8-156">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

