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
ms.openlocfilehash: 8dcbf9437cf7f3ede54f8d1e72ae678fdc5cb3de
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624565"
---
# <a name="wmi-tasks-computer-hardware"></a>Tâches WMI : matériel de l’ordinateur

Les tâches WMI pour le matériel informatique obtiennent des informations sur la présence, l’État ou les propriétés de composants matériels. Par exemple, vous pouvez déterminer si un ordinateur est un ordinateur de bureau ou un ordinateur portable. Pour obtenir d’autres exemples, consultez le site TechNet ScriptCenter à l’adresse [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .

Les exemples de scripts présentés dans cette rubrique obtiennent des données uniquement à partir de l’ordinateur local. Pour plus d’informations sur l’utilisation du script pour obtenir des données à partir d’ordinateurs distants, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md).

## <a name="to-run-a-script"></a>Pour exécuter un script

La procédure suivante décrit comment exécuter un script.

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
<td>... déterminer la quantité de mémoire disponible d’un ordinateur</td>
<td>Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> et la propriété <strong>FreePhysicalMemory</strong> .<br/> <span data-codelanguage="VisualBasic"></span>
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
<col  />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
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
<td>... déterminer si un ordinateur dispose d’un lecteur de DVD ?</td>
<td><p>Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-cdromdrive"><strong>Win32_CDROMDrive</strong></a> et recherchez l’acronyme DVD dans la propriété <strong>Name</strong> ou <strong>DeviceID</strong> .</p>
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
<col  />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
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
<td>... déterminer la quantité de RAM installée sur un ordinateur</td>
<td><p>Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> et vérifiez la valeur de la propriété <strong>TotalPhysicalMemory</strong> .</p>
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
<col  />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
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
<td>... déterminer si un ordinateur a plus d’un processeur ?</td>
<td><p>Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> et la propriété <strong>NumberOfProcessors</strong>.</p>
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
<col  />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
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
<td>... déterminer si un ordinateur dispose d’un emplacement PCMCIA ?</td>
<td><p>Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-pcmciacontroller"><strong>Win32_PCMCIAController</strong></a> et vérifiez la valeur de la propriété <strong>Count</strong> . Si <strong>Count</strong> a la valeur 0, cela signifie que l’ordinateur n’a pas d’emplacement PCMCIA.</p>
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
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_PCMCIAController&quot;)
Wscript.Echo &quot;Number of PCMCIA slots: &quot; & colItems.Count</code></pre></td>
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
<td>... identifier les appareils qui ne fonctionnent pas (ceux marqués d’une icône de point d’exclamation dans <strong>Gestionnaire de périphériques</strong>) ?</td>
<td><p>Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-pnpentity"><strong>Win32_PnPEntity</strong></a> et utilisez la clause suivante dans votre requête <a href="querying-with-wql.md">WQL</a> . <strong>Où ConfigManagerErrorCode <> 0</strong> Notez que ce code peut ne pas détecter les périphériques USB qui manquent de pilotes.</p>
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
<col  />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
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
<td>... déterminer les propriétés de la souris utilisée sur l’ordinateur ?</td>
<td><p>Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-pointingdevice"><strong>Win32_PointingDevice</strong></a> . Cela retourne les propriétés de tous les dispositifs de pointage, pas seulement les périphériques souris.</p>
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
<col  />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
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
<td>... déterminer la vitesse d’un processeur installé sur un ordinateur</td>
<td><p>Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-processor"><strong>Win32_Processor</strong></a> et vérifiez la valeur de la propriété <strong>MaxClockSpeed</strong> .</p>
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
<td>... déterminer si un ordinateur est une tour, une mini-tour, un ordinateur portable, etc. ?</td>
<td><p>Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-systemenclosure"><strong>Win32_SystemEnclosure</strong></a> et vérifiez la valeur de la propriété <strong>ChassisType</strong> .</p>
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
<col  />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
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
<td>... obtenir le numéro de série et l’étiquette d’inventaire d’un ordinateur ?</td>
<td><p>Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-systemenclosure"><strong>Win32_SystemEnclosure</strong></a> et les propriétés <strong>SerialNumber</strong> et <strong>SMBIOSAssetTag</strong>.</p>
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
<col  />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
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
<td>... déterminer le type d’appareil branché sur un port USB</td>
<td><p>Utilisez la classe <a href="/previous-versions/windows/desktop/cimwin32a/win32-usbhub"><strong>Win32_USBHub</strong></a> et vérifiez la propriété <strong>Description</strong> . cette propriété peut avoir une valeur telle que la &quot; masse Stockage périphérique &quot; ou la &quot; prise en charge de l’impression &quot; .</p>
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
<col  />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
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
<td>... déterminer le nombre de lecteurs de bande installés sur un ordinateur</td>
<td><p>Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-tapedrive"><strong>Win32_TapeDrive</strong></a> classe, puis utilisez la méthode <a href="swbemobjectset-count.md"><strong>SWbemObjectSet. Count</strong></a> . Si Count = 0, aucun lecteur de bande n’est installé sur l’ordinateur.</p>
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
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_TapeDrive&quot;)
Wscript.Echo &quot;Number of tape drives: &quot; & colItems.Count</code></pre></td>
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



 

## <a name="examples"></a>Exemples

L' [exemple de code](https://Gallery.TechNet.Microsoft.Com/scriptcenter/List-for-several-machines-1baf6df0) de la Galerie TechNet suivant décrit comment répertorier l’espace libre de tous les lecteurs pour plusieurs ordinateurs.

L’exemple PowerShell- [ComputerInfo-Query Computer Info from local/Remote Computers-(WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sur la Galerie TechNet utilise un certain nombre d’appels au matériel et aux logiciels pour afficher des informations sur un système local ou distant.

L’exemple de [collecte des ressources système multithread avec](https://Gallery.TechNet.Microsoft.Com/Multithreaded-System-Asset-856a8f7c) PowerShell PowerShell sur TechNetGallery rassemble une multitude d’informations utiles sur le système via WMI et le multithread avec PowerShell.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Tâches WMI pour les scripts et les applications](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[Exemples d’applications WMI C++](wmi-c---application-examples.md)
</dt> <dt>

[ScriptCenter TechNet](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

