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
ms.openlocfilehash: b24d5f7708b88507cd08b73c0b08a83c94f6bb28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528347"
---
# <a name="wmi-tasks-files-and-folders"></a><span data-ttu-id="98f4d-103">Tâches WMI : fichiers et dossiers</span><span class="sxs-lookup"><span data-stu-id="98f4d-103">WMI Tasks: Files and Folders</span></span>

<span data-ttu-id="98f4d-104">Les tâches WMI pour les fichiers et les dossiers modifient les propriétés des fichiers ou des dossiers par le biais de WMI, y compris la création d’un partage ou le changement de nom d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="98f4d-104">WMI tasks for files and folders change file or folder properties through WMI, including creating a share or renaming a file.</span></span> <span data-ttu-id="98f4d-105">Si vous souhaitez copier un fichier ou lire et écrire un fichier, le moyen le plus simple consiste à utiliser l’environnement d’exécution de scripts Windows ( [FileSystemObject](/previous-versions/visualstudio/visual-basic-6/aa242706(v=vs.60)) ) au lieu de WMI.</span><span class="sxs-lookup"><span data-stu-id="98f4d-105">If you want to copy a file or read and write a file, the easiest way is to use the Windows Script Host [FileSystemObject](/previous-versions/visualstudio/visual-basic-6/aa242706(v=vs.60)) rather than WMI.</span></span> <span data-ttu-id="98f4d-106">Pour obtenir d’autres exemples, consultez la section [fichiers et dossiers](/previous-versions/tn-archive/ee176985(v=technet.10)) de [technet scriptcenter](https://www.microsoft.com/technet/scriptcenter).</span><span class="sxs-lookup"><span data-stu-id="98f4d-106">For other examples, see the [Files and Folders](/previous-versions/tn-archive/ee176985(v=technet.10)) section of the [TechNet ScriptCenter](https://www.microsoft.com/technet/scriptcenter).</span></span>

<span data-ttu-id="98f4d-107">[**CIM \_ DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile) est l’une des rares [classes CIM](cimclas.md) de WMI qui est implémentée.</span><span class="sxs-lookup"><span data-stu-id="98f4d-107">[**CIM\_DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile) is one of the few [CIM classes](cimclas.md) in WMI that is implemented.</span></span> <span data-ttu-id="98f4d-108">Évitez l’énumération ou l’interrogation de toutes les instances du **\_ fichier** de données CIM sur un ordinateur, car le volume de données risque d’affecter les performances ou de provoquer le blocage de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="98f4d-108">Avoid enumerating or querying for all instances of **CIM\_DataFile** on a computer because the volume of data is likely to either affect performance or cause the computer to stop responding.</span></span>

<span data-ttu-id="98f4d-109">Les exemples de scripts présentés dans cette rubrique obtiennent des données uniquement à partir de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="98f4d-109">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="98f4d-110">Pour plus d’informations sur l’utilisation du script pour obtenir des données à partir d’ordinateurs distants, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="98f4d-110">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="98f4d-111">La procédure suivante décrit comment exécuter un script.</span><span class="sxs-lookup"><span data-stu-id="98f4d-111">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="98f4d-112">**Pour exécuter un script**</span><span class="sxs-lookup"><span data-stu-id="98f4d-112">**To run a script**</span></span>

1.  <span data-ttu-id="98f4d-113">Copiez le code et enregistrez-le dans un fichier avec une extension. vbs, par exemple *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="98f4d-113">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="98f4d-114">Assurez-vous que votre éditeur de texte n’ajoute pas d’extension. txt au fichier.</span><span class="sxs-lookup"><span data-stu-id="98f4d-114">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="98f4d-115">Ouvrez une fenêtre d’invite de commandes et accédez au répertoire où vous avez enregistré le fichier.</span><span class="sxs-lookup"><span data-stu-id="98f4d-115">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="98f4d-116">Tapez **cscript filename.vbs** à l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="98f4d-116">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="98f4d-117">Si vous ne pouvez pas accéder à un journal des événements, vérifiez si vous exécutez à partir d’une invite de commandes avec élévation de privilèges.</span><span class="sxs-lookup"><span data-stu-id="98f4d-117">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="98f4d-118">Certains journaux des événements, tels que le journal des événements de sécurité, peuvent être protégés par les contrôles d’accès utilisateur (UAC).</span><span class="sxs-lookup"><span data-stu-id="98f4d-118">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="98f4d-119">Par défaut, cscript affiche la sortie d’un script dans la fenêtre d’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="98f4d-119">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="98f4d-120">Étant donné que les scripts WMI peuvent générer de grandes quantités de sortie, vous souhaiterez peut-être rediriger la sortie vers un fichier.</span><span class="sxs-lookup"><span data-stu-id="98f4d-120">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="98f4d-121">Tapez **cscript filename.vbs > outfile.txt** à l’invite de commandes pour rediriger la sortie du script *filename.vbs* vers *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="98f4d-121">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="98f4d-122">Le tableau suivant répertorie des exemples de scripts qui peuvent être utilisés pour obtenir différents types de données à partir de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="98f4d-122">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="98f4d-123">Comment puis-je...</span><span class="sxs-lookup"><span data-stu-id="98f4d-123">How do I...</span></span></th>
<th><span data-ttu-id="98f4d-124">Classes ou méthodes WMI</span><span class="sxs-lookup"><span data-stu-id="98f4d-124">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="98f4d-125">... renommer un fichier sans recevoir de message d’erreur ?</span><span class="sxs-lookup"><span data-stu-id="98f4d-125">...rename a file without getting an error message?</span></span></td>
<td><span data-ttu-id="98f4d-126">Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/cim-datafile"><strong>CIM_Datafile</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="98f4d-126">Use the <a href="/windows/desktop/CIMWin32Prov/cim-datafile"><strong>CIM_DataFile</strong></a> class.</span></span> <span data-ttu-id="98f4d-127">Veillez à passer le nom de chemin d’accès complet lors de l’appel de la méthode <a href="/windows/desktop/CIMWin32Prov/rename-method-in-class-cim-datafile"><strong>Rename</strong></a> , par exemple, &quot;C:\Scripts\Test.txt&quot; au lieu de &quot;Text.txt&quot; .</span><span class="sxs-lookup"><span data-stu-id="98f4d-127">Ensure that you pass the entire path name when calling the <a href="/windows/desktop/CIMWin32Prov/rename-method-in-class-cim-datafile"><strong>Rename</strong></a> method, for example, &quot;C:\Scripts\Test.txt&quot; instead of &quot;Text.txt&quot;.</span></span> <span data-ttu-id="98f4d-128">Pour PowerShell, l’utilisation de <strong>CIM_Datafile</strong> peut être inefficace.</span><span class="sxs-lookup"><span data-stu-id="98f4d-128">For PowerShell, using <strong>CIM_DataFile</strong> may be inefficient.</span></span> <span data-ttu-id="98f4d-129">Par conséquent, vous pouvez simplement utiliser l’applet de commande Rename-Item.</span><span class="sxs-lookup"><span data-stu-id="98f4d-129">As such, you may simply use the Rename-Item cmdlet.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="98f4d-130">VB</span><span class="sxs-lookup"><span data-stu-id="98f4d-130">VB</span></span></th>
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
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="98f4d-131">PowerShell</span><span class="sxs-lookup"><span data-stu-id="98f4d-131">PowerShell</span></span></th>
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
<td><span data-ttu-id="98f4d-132">... Déterminez si les utilisateurs ont. Fichiers MP3 stockés sur leur ordinateur</span><span class="sxs-lookup"><span data-stu-id="98f4d-132">...determine whether users have .MP3 files stored on their computer?</span></span></td>
<td><p><span data-ttu-id="98f4d-133">Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/cim-datafile"><strong>CIM_Datafile</strong></a> et sélectionnez fichiers à l’aide de la clause <strong>Where</strong> <a href="querying-with-wql.md">WQL</a> suivante : Where extension = &quot; mp3 &quot; .</span><span class="sxs-lookup"><span data-stu-id="98f4d-133">Use the <a href="/windows/desktop/CIMWin32Prov/cim-datafile"><strong>CIM_DataFile</strong></a> class and select files using the following <a href="querying-with-wql.md">WQL</a> <strong>WHERE</strong> clause: Where Extension = &quot;MP3&quot;.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="98f4d-134">VB</span><span class="sxs-lookup"><span data-stu-id="98f4d-134">VB</span></span></th>
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
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="98f4d-135">PowerShell</span><span class="sxs-lookup"><span data-stu-id="98f4d-135">PowerShell</span></span></th>
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
<td><span data-ttu-id="98f4d-136">... créer des dossiers partagés sur un ordinateur ?</span><span class="sxs-lookup"><span data-stu-id="98f4d-136">...create shared folders on a computer?</span></span></td>
<td><p><span data-ttu-id="98f4d-137">Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-share"><strong>Win32_Share</strong></a> et la méthode <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-share"><strong>Create</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="98f4d-137">Use the <a href="/windows/desktop/CIMWin32Prov/win32-share"><strong>Win32_Share</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-share"><strong>Create</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="98f4d-138">VB</span><span class="sxs-lookup"><span data-stu-id="98f4d-138">VB</span></span></th>
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
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="98f4d-139">PowerShell</span><span class="sxs-lookup"><span data-stu-id="98f4d-139">PowerShell</span></span></th>
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
<td><span data-ttu-id="98f4d-140">... copier un dossier ?</span><span class="sxs-lookup"><span data-stu-id="98f4d-140">...copy a folder?</span></span></td>
<td><p><span data-ttu-id="98f4d-141">Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-directory"><strong>Win32_Directory</strong></a> et la méthode <a href="/windows/desktop/CIMWin32Prov/copy-method-in-class-win32-directory"><strong>Copy</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="98f4d-141">Use the <a href="/windows/desktop/CIMWin32Prov/win32-directory"><strong>Win32_Directory</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/copy-method-in-class-win32-directory"><strong>Copy</strong></a> method.</span></span> <span data-ttu-id="98f4d-142">Pour PowerShell, vous pouvez simplement utiliser l’applet de commande Copy-Item.</span><span class="sxs-lookup"><span data-stu-id="98f4d-142">For PowerShell, you can simply use the Copy-Item cmdlet.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="98f4d-143">VB</span><span class="sxs-lookup"><span data-stu-id="98f4d-143">VB</span></span></th>
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
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="98f4d-144">PowerShell</span><span class="sxs-lookup"><span data-stu-id="98f4d-144">PowerShell</span></span></th>
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
<td><span data-ttu-id="98f4d-145">... déplacer un dossier ?</span><span class="sxs-lookup"><span data-stu-id="98f4d-145">...move a folder?</span></span></td>
<td><p><span data-ttu-id="98f4d-146">Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-directory"><strong>Win32_Directory</strong></a> et la méthode <a href="/windows/desktop/CIMWin32Prov/rename-method-in-class-win32-directory"><strong>Rename</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="98f4d-146">Use the <a href="/windows/desktop/CIMWin32Prov/win32-directory"><strong>Win32_Directory</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/rename-method-in-class-win32-directory"><strong>Rename</strong></a> method.</span></span> <span data-ttu-id="98f4d-147">Pour PowerShell, vous pouvez simplement utiliser l’applet de commande Move-Item.</span><span class="sxs-lookup"><span data-stu-id="98f4d-147">For PowerShell, you can simply use the Move-Item cmdlet.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="98f4d-148">VB</span><span class="sxs-lookup"><span data-stu-id="98f4d-148">VB</span></span></th>
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
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="98f4d-149">PowerShell</span><span class="sxs-lookup"><span data-stu-id="98f4d-149">PowerShell</span></span></th>
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



 

## <a name="related-topics"></a><span data-ttu-id="98f4d-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="98f4d-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98f4d-151">Tâches WMI pour les scripts et les applications</span><span class="sxs-lookup"><span data-stu-id="98f4d-151">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="98f4d-152">Exemples d’applications WMI C++</span><span class="sxs-lookup"><span data-stu-id="98f4d-152">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="98f4d-153">ScriptCenter TechNet</span><span class="sxs-lookup"><span data-stu-id="98f4d-153">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

 



`
