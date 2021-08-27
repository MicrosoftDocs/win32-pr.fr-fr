---
description: Les tâches WMI pour les disques et les systèmes de fichiers obtiennent des informations sur l’état du matériel du lecteur de disque et les volumes logiques. Pour obtenir d’autres exemples, consultez le site TechNet ScriptCenter à l’adresse https://www.microsoft.com/technet .
ms.assetid: d310e5e6-3b67-41bc-b5f2-cea33d0a7a2b
ms.tgt_platform: multiple
title: 'Tâches WMI : Disques et systèmes de fichiers'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9d4bd8b99374cb8e8367470eb6c7e7d750ad077d
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625405"
---
# <a name="wmi-tasks-disks-and-file-systems"></a>Tâches WMI : Disques et systèmes de fichiers

Les tâches WMI pour les disques et les systèmes de fichiers obtiennent des informations sur l’état du matériel du lecteur de disque et les volumes logiques. Pour obtenir d’autres exemples, consultez le site TechNet ScriptCenter à l’adresse [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .

Les exemples de scripts présentés dans cette rubrique obtiennent des données uniquement à partir de l’ordinateur local. Pour plus d’informations sur l’utilisation du script pour obtenir des données à partir d’ordinateurs distants, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md).


La procédure suivante décrit comment exécuter un script.

**Pour exécuter un script**

1.  Copiez le code et enregistrez-le dans un fichier avec une extension. vbs, par exemple *filename.vbs*. Assurez-vous que votre éditeur de texte n’ajoute pas d’extension de .txt au fichier.
2.  Ouvrez une fenêtre d’invite de commandes et accédez au répertoire où vous avez enregistré le fichier.
3.  Tapez **cscript filename.vbs** à l’invite de commandes.
4.  Si vous ne pouvez pas accéder à un journal des événements, vérifiez si vous exécutez à partir d’une invite de commandes avec élévation de privilèges. Certains journaux des événements, tels que le journal des événements de sécurité, peuvent être protégés par les contrôles d’accès utilisateur (UAC).

> [!Note]  
> Par défaut, cscript affiche la sortie d’un script dans la fenêtre d’invite de commandes. Étant donné que les scripts WMI peuvent générer de grandes quantités de sortie, vous souhaiterez peut-être rediriger la sortie vers un fichier. Tapez **cscript filename.vbs > outfile.txt** à l’invite de commandes pour rediriger la sortie du script *filename.vbs* vers *outfile.txt*.

 

Le tableau suivant répertorie des exemples de scripts qui peuvent être utilisés pour obtenir différents types de données à partir de l’ordinateur local.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Comment puis-je...</th>
<th>Classes ou méthodes WMI</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>... Déterminez l’espace disque actuellement utilisé par chaque utilisateur sur un ordinateur.</td>
<td>Si vous utilisez des quotas de disque, utilisez la classe <a href="/previous-versions/windows/desktop/wmipdskq/win32-diskquota"><strong>Win32_DiskQuota</strong></a> et récupérez les valeurs des propriétés <strong>User</strong> et <strong>DiskSpaceUsed</strong> .<br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colQuotas = objWMIService.ExecQuery (&quot;Select * from Win32_DiskQuota&quot;)
For each objQuota in colQuotas
    Wscript.Echo &quot;Volume: &quot;& vbTab &  objQuota.QuotaVolume
    Wscript.Echo &quot;User: &quot;& vbTab &  objQuota.User      
    Wscript.Echo &quot;Disk Space Used: &quot; & vbTab &  objQuota.DiskSpaceUsed
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colItems = Get-WmiObject -Class Win32_DiskQuota -ComputerName $strComputer
foreach ($objQuota in $colItems) 
{ 
    &quot;Volume: &quot; + $objQuota.QuotaVolume
    &quot;User: &quot; + $objQuota.User      
    &quot;Disk Space Used: &quot; + $objQuota.DiskSpaceUsed
}</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>... déterminer quand un lecteur amovible a été ajouté à un ordinateur ou en est supprimé ?</td>
<td><p>Utilisez un script d’analyse qui interroge la classe <a href="/windows/desktop/CIMWin32Prov/win32-volumechangeevent"><strong>Win32_VolumeChangeEvent</strong></a> .</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colMonitoredEvents = objWMIService. ExecNotificationQuery( &quot;Select * from Win32_VolumeChangeEvent&quot;)
Do
    Set objLatestEvent = colMonitoredEvents.NextEvent
    Wscript.Echo objLatestEvent.DriveName
    Wscript.Echo objLatestEvent.EventType
    Wscript.Echo objLatestEvent.Time_Created
Loop</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>... déterminer si un CD se trouve dans un lecteur de CD-ROM ?</td>
<td><p>Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-cdromdrive"><strong>Win32_CDROMDrive</strong></a> et la propriété <strong>MediaLoaded</strong> .</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery( &quot;Select * from Win32_CDROMDrive&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Device ID: &quot; & objItem.DeviceID
    Wscript.Echo &quot;Media Loaded: &quot; & objItem.MediaLoaded
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colItems = Get-WmiObject -Class Win32_CDROMDrive -ComputerName $strComputer
foreach ($objItem in $colItems)
{
    &quot;Device ID: &quot; + $objItem.DeviceID
    &quot;MediaLoaded: &quot; + $objItem.MediaLoaded
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>... déterminer si un disque se trouve dans le lecteur de disquette ?</td>
<td><p>Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> et vérifiez la propriété <strong>FreeSpace</strong> . Si la valeur est null, aucun disque n’est présent dans le lecteur.</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject( &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery (&quot;Select * From Win32_LogicalDisk Where DeviceID = &#39;A:&#39;&quot;)

For Each objItem in colItems
    intFreeSpace = objItem.FreeSpace
    If IsNull(intFreeSpace) Then
        Wscript.Echo &quot;There is no disk in the floppy drive.&quot;
    Else
        Wscript.Echo &quot;There is a disk in the floppy drive.&quot;
    End If
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colItems = Get-WmiObject -Class Win32_LogicalDisk -Namespace &quot;root\cimv2&quot; -ComputerName $strComputer | `
    Where-Object { $_.DeviceID -eq &quot;A:&quot; }

foreach ($objItem in $colItems)
{
    $intFreeSpace = $objItem.FreeSpace
    if ($intFreeSpace -eq $null) { &quot;There is no disk in the floppy drive.&quot; }
    else { &quot;There is a disk in the floppy drive.&quot; }
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>... faire la distinction entre un disque dur fixe et un disque dur amovible ?</td>
<td><p>Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> et vérifiez la valeur de la propriété <strong>DriveType</strong> .</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
Set colDisks = objWMIService.ExecQuery _
    (&quot;Select * from Win32_LogicalDisk&quot;)
For Each objDisk in colDisks
    Wscript.Echo &quot;DeviceID: &quot;& vbTab _
        &  objDisk.DeviceID       
    Select Case objDisk.DriveType
        Case 1
            Wscript.Echo &quot;No root directory. &quot; & &quot;Drive type could not be &quot; & &quot;determined.&quot;
        Case 2
            Wscript.Echo &quot;DriveType: &quot;& vbTab &  &quot;Removable drive.&quot;
        Case 3
            Wscript.Echo &quot;DriveType: &quot;& vbTab &  &quot;Local hard disk.&quot;
        Case 4
            Wscript.Echo &quot;DriveType: &quot;& vbTab &  &quot;Network disk.&quot;      
        Case 5
            Wscript.Echo &quot;DriveType: &quot;& vbTab &  &quot;Compact disk.&quot;      
        Case 6
            Wscript.Echo &quot;DriveType: &quot;& vbTab &  &quot;RAM disk.&quot;   
        Case Else
            Wscript.Echo &quot;Drive type could not be&quot; & &quot; determined.&quot;
    End Select
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colDisks = Get-WmiObject -Class Win32_LogicalDisk -ComputerName $strComputer 

foreach ($objDisk in $colDisks)
{
    &quot;DeviceID: &quot; + $objDisk.deviceID
    switch ($objDisk.DriveType)
    {
        &#39;1&#39; { &quot;No root directory. Drive type could not be determined.&quot; }
        &#39;2&#39; { &quot;DriveType: Removable drive.&quot; }
        &#39;3&#39; { &quot;DriveType: Local hard disk.&quot; }
        &#39;4&#39; { &quot;DriveType: Network disk.&quot; }
        &#39;5&#39; { &quot;DriveType: Compact disk.&quot; }
        &#39;6&#39; { &quot;DriveType: RAM disk.&quot; }
        default: { &quot;Drive type could not be determined.&quot; }
    }
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>... déterminer quel système de fichiers est en cours d’utilisation sur un lecteur ?</td>
<td><p>Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> et la propriété <strong>FileSystem</strong> .</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colDisks = objWMIService.ExecQuery (&quot;Select * from Win32_LogicalDisk&quot;)
For Each objDisk in colDisks
    Wscript.Echo &quot;DeviceID: &quot; & objDisk.DeviceID       
    Wscript.Echo &quot;File System: &quot; & objDisk.FileSystem
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>... déterminer la quantité d’espace libre disponible sur un lecteur ?</td>
<td><p>Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> et la propriété <strong>FreeSpace</strong> .</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colDisks = objWMIService.ExecQuery (&quot;Select * from Win32_LogicalDisk&quot;)
For Each objDisk in colDisks
    Wscript.Echo &quot;DeviceID: &quot; & objDisk.DeviceID       
    Wscript.Echo &quot;Free Disk Space: &quot; & objDisk.FreeSpace
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>... déterminer la taille d’un lecteur ?</td>
<td><p>Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> et la propriété <strong>Size</strong> .</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colDisks = objWMIService.ExecQuery (&quot;Select * from Win32_LogicalDisk&quot;)
For Each objDisk in colDisks
    Wscript.Echo &quot;DeviceID: &quot; & objDisk.DeviceID       
    Wscript.Echo &quot;Disk Size: &quot; & objDisk.Size
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>... Quels sont les lecteurs mappés sur un ordinateur ?</td>
<td><p>Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-mappedlogicaldisk"><strong>Win32_MappedLogicalDisk</strong></a> .</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colDisks = objWMIService. ExecQuery(&quot;Select * from Win32_MappedLogicalDisk&quot;)
For Each objDisk in colDisks
    Wscript.Echo &quot;Device ID: &quot; & objDisk.DeviceID
    Wscript.Echo &quot;Name: &quot; & objDisk.Name
    Wscript.Echo &quot;Free Space: &quot; & objDisk.FreeSpace
    Wscript.Echo &quot;Size: &quot; & objDisk.Size
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>... défragmenter un disque dur ?</td>
<td><p>Utilisez la classe <a href="/previous-versions/windows/desktop/legacy/aa394515(v=vs.85)"><strong>Win32_Volume</strong></a> et la méthode <a href="/previous-versions/windows/desktop/vdswmi/defrag-method-in-class-win32-volume"><strong>Defrag</strong></a> .</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colVolumes = objWMIService.ExecQuery (&quot;Select * from Win32_Volume Where Name = &#39;K:\\&#39;&quot;)
For Each objVolume in colVolumes
     errResult = objVolume.Defrag()
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>... Comment détecter la lettre de lecteur associée à une partition de disque logique ?</td>
<td><ol>
<li>Commencez par la classe <a href="/windows/desktop/CIMWin32Prov/win32-diskdrive"><strong>Win32_DiskDrive</strong></a> et interrogez les instances de <a href="/windows/desktop/CIMWin32Prov/win32-diskpartition"><strong>Win32_DiskPartition</strong></a> à l’aide de la propriété <strong>DeviceID</strong> et de la classe Association <a href="/windows/desktop/CIMWin32Prov/win32-diskdrivetodiskpartition"><strong>Win32_DiskDriveToDiskPartition</strong></a> . Vous disposez maintenant d’une collection de partitions sur le lecteur physique.</li>
<li>Recherchez la <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> qui représente la partition à l’aide de la propriété <a href="/windows/desktop/CIMWin32Prov/win32-diskpartition"><strong>Win32_DiskPartition. DeviceID</strong></a> et <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisktopartition"><strong>Win32_LogicalDiskToPartition</strong></a> classe Association.</li>
<li>Récupérez la lettre de lecteur à partir du <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk. DeviceID</strong></a>.</li>
</ol>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>ComputerName = &quot;.&quot;
Set wmiServices  = GetObject ( _
    &quot;winmgmts:{impersonationLevel=Impersonate}!//&quot; & ComputerName)
&#39; Get physical disk drive
Set wmiDiskDrives =  wmiServices.ExecQuery ( &quot;SELECT Caption, DeviceID FROM Win32_DiskDrive&quot;)

For Each wmiDiskDrive In wmiDiskDrives
    WScript.Echo &quot;Disk drive Caption: &quot; & wmiDiskDrive.Caption & VbNewLine & &quot;DeviceID: &quot; & &quot; (&quot; & wmiDiskDrive.DeviceID & &quot;)&quot;

&#39;Use the disk drive device id to
&#39; find associated partition
query = &quot;ASSOCIATORS OF {Win32_DiskDrive.DeviceID=&#39;&quot; _
        & wmiDiskDrive.DeviceID & &quot;&#39;} WHERE AssocClass = Win32_DiskDriveToDiskPartition&quot;    
Set wmiDiskPartitions = wmiServices.ExecQuery(query)

For Each wmiDiskPartition In wmiDiskPartitions
    &#39;Use partition device id to find logical disk
    Set wmiLogicalDisks = wmiServices.ExecQuery _
        (&quot;ASSOCIATORS OF {Win32_DiskPartition.DeviceID=&#39;&quot; _
             & wmiDiskPartition.DeviceID & &quot;&#39;} WHERE AssocClass = Win32_LogicalDiskToPartition&quot;)

For Each wmiLogicalDisk In wmiLogicalDisks
    WScript.Echo &quot;Drive letter associated&quot; _
        & &quot; with disk drive = &quot; _ 
        & wmiDiskDrive.Caption _
        & wmiDiskDrive.DeviceID _
        & VbNewLine & &quot; Partition = &quot; _
        & wmiDiskPartition.DeviceID _
        & VbNewLine & &quot; is &quot; _
        & wmiLogicalDisk.DeviceID
    Next
    Next
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Tâches WMI pour les scripts et les applications](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[Exemples d’applications WMI C++](wmi-c---application-examples.md)
</dt> <dt>

[ScriptCenter TechNet](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

 



`
