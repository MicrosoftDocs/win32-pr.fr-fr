---
description: Les tâches WMI pour les fichiers et les dossiers modifient les propriétés des fichiers ou des dossiers par le biais de WMI, y compris la création d’un partage ou le changement de nom d’un fichier.
ms.assetid: 91281fe1-0461-48da-ac5c-cab7e8e1b285
ms.tgt_platform: multiple
title: 'Tâches WMI : fichiers et dossiers'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4b7ac3b02e0268d9357e00d91e21d878f78bf966
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122629461"
---
# <a name="wmi-tasks-files-and-folders"></a>Tâches WMI : fichiers et dossiers

Les tâches WMI pour les fichiers et les dossiers modifient les propriétés des fichiers ou des dossiers par le biais de WMI, y compris la création d’un partage ou le changement de nom d’un fichier. si vous souhaitez copier un fichier ou lire et écrire un fichier, le moyen le plus simple consiste à utiliser le Windows générer un Script de [l’hôte de](/previous-versions/visualstudio/visual-basic-6/aa242706(v=vs.60)) Script plutôt que WMI. Pour obtenir d’autres exemples, consultez la section [fichiers et dossiers](/previous-versions/tn-archive/ee176985(v=technet.10)) de [technet scriptcenter](https://www.microsoft.com/technet/scriptcenter).

[**CIM \_ DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile) est l’une des rares [classes CIM](cimclas.md) de WMI qui est implémentée. Évitez l’énumération ou l’interrogation de toutes les instances du **\_ fichier** de données CIM sur un ordinateur, car le volume de données risque d’affecter les performances ou de provoquer le blocage de l’ordinateur.

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
<td>... renommer un fichier sans recevoir de message d’erreur ?</td>
<td>Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/cim-datafile"><strong>CIM_Datafile</strong></a> . Veillez à passer le nom de chemin d’accès complet lors de l’appel de la méthode <a href="/windows/desktop/CIMWin32Prov/rename-method-in-class-cim-datafile"><strong>Rename</strong></a> , par exemple, &quot;C:\Scripts\Test.txt&quot; au lieu de &quot;Text.txt&quot; . Pour PowerShell, l’utilisation de <strong>CIM_Datafile</strong> peut être inefficace. Par conséquent, vous pouvez simplement utiliser l’applet de commande Rename-Item.<br/> <span data-codelanguage="VisualBasic"></span>
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
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colFiles = objWMIService.ExecQuery (&quot;Select * from CIM_DataFile where Name = &quot; & &quot;&#39;c:\\scripts\\toggle_service.vbs&#39;&quot;)
For Each objFile in colFiles
    errResult = objFile.Rename(&quot;c:\scripts\toggle_service.old&quot;)
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
<td><pre><code>rename-item c:\scripts\toggle_service.vbs toggle_service.old</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>... déterminer si les utilisateurs ont .MP3 fichiers stockés sur leur ordinateur ?</td>
<td><p>Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/cim-datafile"><strong>CIM_Datafile</strong></a> et sélectionnez fichiers à l’aide de la clause <strong>Where</strong> <a href="querying-with-wql.md">WQL</a> suivante : Where extension = &quot; mp3 &quot; .</p>
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
Set colFiles = objWMIService.ExecQuery(&quot;Select * from CIM_DataFile where Extension = &#39;mp3&#39;&quot;)
For Each objFile in colFiles
    Wscript.Echo &quot;File Name: &quot; & objFile.Name & &quot;.&quot; & objFile.Extension
    Wscript.Echo &quot;Path: &quot; & objFile.Path
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
<td><pre><code>Get-WmiObject -Class CIM_DataFile -namespace &quot;root\cimv2&quot; -Filter &quot;Extension = &#39;mp3&#39;&quot; | `
   format-list Name, Extension, Path</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>... créer des dossiers partagés sur un ordinateur ?</td>
<td><p>Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-share"><strong>Win32_Share</strong></a> et la méthode <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-share"><strong>Create</strong></a> .</p>
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
<td><pre><code>Const FILE_SHARE = 0
Const MAXIMUM_CONNECTIONS = 25
strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set objNewShare = objWMIService.Get(&quot;Win32_Share&quot;)
errReturn = objNewShare.Create(&quot;C:\Finance&quot;, &quot;FinanceShare&quot;, FILE_SHARE, MAXIMUM_CONNECTIONS, &quot;Public share for the Finance group.&quot;)</code></pre></td>
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
<td><pre><code>$FILE_SHARE = 0
$MAXIMUM_CONNECTIONS = 25

$NewDir = new-item C:\Finance -type directory 
$Shares= [WMICLASS]&quot;Win32_Share&quot;
[void]$Shares.Create(&quot;C:\Finance&quot;,&quot;FinanceShare&quot;, $FILE_SHARE, $MAXIMUM_CONNECTIONS, &quot;Public share for the Finance group.&quot;) </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>... copier un dossier ?</td>
<td><p>Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-directory"><strong>Win32_Directory</strong></a> et la méthode <a href="/windows/desktop/CIMWin32Prov/copy-method-in-class-win32-directory"><strong>Copy</strong></a> . Pour PowerShell, vous pouvez simplement utiliser l’applet de commande Copy-Item.</p>
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
 
Set colFolders = objWMIService.ExecQuery(&quot;Select * from Win32_Directory where Name = &#39;c:\\Scripts&#39;&quot;) 
 
For Each objFolder in colFolders 
    errResults  = objFolder.Copy(&quot;D:\Archive&quot;) 
Next </code></pre></td>
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
<td><pre><code>Copy-Item C:\Scripts -Destination D:\Archive -Recurse</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>... déplacer un dossier ?</td>
<td><p>Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-directory"><strong>Win32_Directory</strong></a> et la méthode <a href="/windows/desktop/CIMWin32Prov/rename-method-in-class-win32-directory"><strong>Rename</strong></a> . Pour PowerShell, vous pouvez simplement utiliser l’applet de commande Move-Item.</p>
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
    & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;) 
 
Set colFolders = objWMIService.ExecQuery _ 
    (&quot;Select * from Win32_Directory where name = &#39;c:\\Scripts&#39;&quot;) 
 
For Each objFolder in colFolders 
    errResults = objFolder.Rename(&quot;C:\Admins\Documents\Archive\VBScript&quot;) 
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
<td><pre><code>move-item -path C:\Scripts -destination C:\Admins\Documents\Archive\PowerShell</code></pre></td>
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
