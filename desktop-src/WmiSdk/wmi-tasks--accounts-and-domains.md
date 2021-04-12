---
description: Les tâches d’administration du compte et du domaine obtiennent des informations telles que le domaine de l’ordinateur ou l’utilisateur actuellement connecté.
ms.assetid: 1a9cc44b-c366-465d-a0d0-536d5dc818b5
ms.tgt_platform: multiple
title: 'Tâches WMI : comptes et domaines'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3bcda33677ada6c4a08e2d9bdc1676c9662a5cd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210410"
---
# <a name="wmi-tasks-accounts-and-domains"></a><span data-ttu-id="0aa4d-103">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="0aa4d-103">WMI Tasks: Accounts and Domains</span></span>

<span data-ttu-id="0aa4d-104">Les tâches d’administration du compte et du domaine obtiennent des informations telles que le domaine de l’ordinateur ou l’utilisateur actuellement connecté.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-104">Account and domain administrative tasks obtain information such as the computer domain or the currently logged-on user.</span></span> <span data-ttu-id="0aa4d-105">La plupart de ces tâches sont exécutées de manière optimale avec les scripts [ADSI](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) .</span><span class="sxs-lookup"><span data-stu-id="0aa4d-105">Many of these tasks are best performed with [ADSI](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) scripts.</span></span> <span data-ttu-id="0aa4d-106">Pour plus d’informations et pour obtenir d’autres exemples, consultez le référentiel de scripts TechNet [scriptcenter](https://www.microsoft.com/technet/scriptcenter) .</span><span class="sxs-lookup"><span data-stu-id="0aa4d-106">For more information and other examples, see the TechNet [ScriptCenter](https://www.microsoft.com/technet/scriptcenter) Script Repository.</span></span>

<span data-ttu-id="0aa4d-107">Les exemples de scripts présentés dans cette rubrique obtiennent des données uniquement à partir de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="0aa4d-108">Pour plus d’informations sur l’utilisation du script pour obtenir des données à partir d’ordinateurs distants, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="0aa4d-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="0aa4d-109">La procédure suivante décrit comment exécuter un script.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="0aa4d-110">**Pour exécuter un script**</span><span class="sxs-lookup"><span data-stu-id="0aa4d-110">**To run a script**</span></span>

1.  <span data-ttu-id="0aa4d-111">Copiez le code et enregistrez-le dans un fichier avec une extension. vbs, par exemple *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="0aa4d-112">Assurez-vous que votre éditeur de texte n’ajoute pas d’extension. txt au fichier.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="0aa4d-113">Ouvrez une fenêtre d’invite de commandes et accédez au répertoire où vous avez enregistré le fichier.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="0aa4d-114">Tapez **cscript filename.vbs** à l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="0aa4d-115">Si vous ne pouvez pas accéder à un journal des événements, vérifiez si vous exécutez à partir d’une invite de commandes avec élévation de privilèges.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="0aa4d-116">Certains journaux des événements, tels que le journal des événements de sécurité, peuvent être protégés par les contrôles d’accès utilisateur (UAC).</span><span class="sxs-lookup"><span data-stu-id="0aa4d-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="0aa4d-117">Par défaut, cscript affiche la sortie d’un script dans la fenêtre d’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="0aa4d-118">Étant donné que les scripts WMI peuvent générer de grandes quantités de sortie, vous souhaiterez peut-être rediriger la sortie vers un fichier.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="0aa4d-119">Tapez **cscript filename.vbs > outfile.txt** à l’invite de commandes pour rediriger la sortie du script *filename.vbs* vers *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="0aa4d-120">Le tableau suivant répertorie des exemples de scripts qui peuvent être utilisés pour obtenir différents types de données à partir de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0aa4d-121">Comment puis-je...</span><span class="sxs-lookup"><span data-stu-id="0aa4d-121">How do I...</span></span></th>
<th><span data-ttu-id="0aa4d-122">Classes ou méthodes WMI</span><span class="sxs-lookup"><span data-stu-id="0aa4d-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0aa4d-123">... déterminer le domaine auquel appartient un ordinateur ?</span><span class="sxs-lookup"><span data-stu-id="0aa4d-123">...determine the domain in which a computer belongs?</span></span></td>
<td><span data-ttu-id="0aa4d-124">Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> et vérifiez la valeur de la propriété de <strong>domaine</strong> .</span><span class="sxs-lookup"><span data-stu-id="0aa4d-124">Use the <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> class and check the value of the <strong>Domain</strong> property.</span></span> <span data-ttu-id="0aa4d-125">Vous pouvez également utiliser la propriété <strong>dnsdomain</strong> dans <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-125">You can also use the <strong>DNSDomain</strong> property in <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a>.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0aa4d-126">VB</span><span class="sxs-lookup"><span data-stu-id="0aa4d-126">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colSettings = objWMIService.ExecQuery(&quot;Select * from Win32_ComputerSystem&quot;)

For Each objComputer in colSettings 
    Wscript.Echo &quot;System Name: &quot; & objComputer.Name
    Wscript.Echo &quot;Domain: &quot; & objComputer.Domain
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
<th><span data-ttu-id="0aa4d-127">PowerShell</span><span class="sxs-lookup"><span data-stu-id="0aa4d-127">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$computer = Get-WmiObject -Class Win32_ComputerSystem
&quot;System Name: {0}&quot; -f $computer.name
&quot;Domain : {0}&quot; -f $computer.domain</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0aa4d-128">C#</span><span class="sxs-lookup"><span data-stu-id="0aa4d-128">C#</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>using Microsoft.Management.Infrastructure;
...
CimSession session = CimSession.Create(&quot;localHost&quot;);
IEnumerable<CimInstance> queryInstance = session.QueryInstances(@&quot;root\cimv2&quot;, &quot;WQL&quot;, &quot;SELECT * FROM Win32_ComputerSystem&quot;);

foreach (CimInstance cimObj in queryInstance)
{
   Console.WriteLine(cimObj.CimInstanceProperties[&quot;Name&quot;].ToString());
   Console.WriteLine(cimObj.CimInstanceProperties[&quot;Domain&quot;].ToString());
}</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aa4d-129">... déterminer si un ordinateur est un serveur ou un poste de travail ?</span><span class="sxs-lookup"><span data-stu-id="0aa4d-129">...determine whether a computer is a server or a workstation?</span></span></td>
<td><p><span data-ttu-id="0aa4d-130">Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> et la propriété <strong>DomainRole</strong> .</span><span class="sxs-lookup"><span data-stu-id="0aa4d-130">Use the <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> class and the <strong>DomainRole</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0aa4d-131">VB</span><span class="sxs-lookup"><span data-stu-id="0aa4d-131">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colComputers = objWMIService.ExecQuery(&quot;Select DomainRole from Win32_ComputerSystem&quot;)
For Each objComputer in colComputers
    Select Case objComputer.DomainRole 
        Case 0 
            strComputerRole = &quot;Standalone Workstation&quot;
        Case 1        
            strComputerRole = &quot;Member Workstation&quot;
        Case 2
            strComputerRole = &quot;Standalone Server&quot;
        Case 3
            strComputerRole = &quot;Member Server&quot;
        Case 4
            strComputerRole = &quot;Backup Domain Controller&quot;
        Case 5
            strComputerRole = &quot;Primary Domain Controller&quot;
    End Select
    Wscript.Echo strComputerRole
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
<th><span data-ttu-id="0aa4d-132">PowerShell</span><span class="sxs-lookup"><span data-stu-id="0aa4d-132">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$Computer = Get-WmiObject -Class Win32_ComputerSystem 

&quot;Computer `&quot;{0}.{1}`&quot; is a: &quot;-f $Computer.Name,$computer.domain

switch  ($computer.DomainRole) {
    0 {&quot;Standalone Workstation&quot;}
    1 {&quot;Member Workstation&quot;}
    2 {&quot;Standalone Server&quot;}
    3 {&quot;Member Server&quot;}
    4 {&quot;Backup Domain Controller&quot;}
    5 {&quot;Primary Domain Controller&quot;}
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0aa4d-133">... déterminer le nom de l’ordinateur ?</span><span class="sxs-lookup"><span data-stu-id="0aa4d-133">...determine the computer name?</span></span></td>
<td><p><span data-ttu-id="0aa4d-134">Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> et la propriété <strong>Name</strong> .</span><span class="sxs-lookup"><span data-stu-id="0aa4d-134">Use the <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> class and the <strong>Name</strong> property.</span></span> <span data-ttu-id="0aa4d-135">Vous pouvez également utiliser la propriété <strong>dNSHostName</strong> dans <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-135">You can also use the <strong>DNSHostName</strong> property in <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0aa4d-136">VB</span><span class="sxs-lookup"><span data-stu-id="0aa4d-136">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_ComputerSystem&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Computer Name: &quot; & objItem.Name
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
<th><span data-ttu-id="0aa4d-137">PowerShell</span><span class="sxs-lookup"><span data-stu-id="0aa4d-137">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$Computer = Get-WmiObject -Class Win32_ComputerSystem
&quot;Computer Name is: {0}&quot; -f $Computer.Name</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0aa4d-138">C#</span><span class="sxs-lookup"><span data-stu-id="0aa4d-138">C#</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>using Microsoft.Management.Infrastructure;
...
CimSession session = CimSession.Create(&quot;localHost&quot;);
IEnumerable<CimInstance> queryInstance = session.QueryInstances(@&quot;root\cimv2&quot;, &quot;WQL&quot;, &quot;SELECT * FROM Win32_ComputerSystem&quot;);

foreach (CimInstance cimObj in queryInstance)
{
   Console.WriteLine(cimObj.CimInstanceProperties[&quot;Name&quot;].ToString());
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aa4d-139">... Rechercher le nom de la personne actuellement connectée à un ordinateur ?</span><span class="sxs-lookup"><span data-stu-id="0aa4d-139">...find the name of the person currently logged on to a computer?</span></span></td>
<td><p><span data-ttu-id="0aa4d-140">Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> et la propriété <strong>username</strong> .</span><span class="sxs-lookup"><span data-stu-id="0aa4d-140">Use the <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> class and the <strong>UserName</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0aa4d-141">VB</span><span class="sxs-lookup"><span data-stu-id="0aa4d-141">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;) 
Set colComputer = objWMIService.ExecQuery(&quot;Select * from Win32_ComputerSystem&quot;)
 
For Each objComputer in colComputer
    Wscript.Echo &quot;User Name = &quot; & objComputer.UserName & VBNewLine & &quot;Computer Name = &quot; & objComputer.Name
WScript.Echo objComputer.UserName
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
<th><span data-ttu-id="0aa4d-142">PowerShell</span><span class="sxs-lookup"><span data-stu-id="0aa4d-142">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$computers = Get-WmiObject -Class Win32_ComputerSystem 
&quot;Logged on user(s):&quot;
foreach($computer in $computers) {
   &quot;User: {0}&quot; -f $computer.UserName
}</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0aa4d-143">C#</span><span class="sxs-lookup"><span data-stu-id="0aa4d-143">C#</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>using Microsoft.Management.Infrastructure;
...
CimSession session = CimSession.Create(&quot;localHost&quot;);
IEnumerable<CimInstance> queryInstance = session.QueryInstances(@&quot;root\cimv2&quot;, &quot;WQL&quot;, &quot;SELECT * FROM Win32_ComputerSystem&quot;);

foreach (CimInstance cimObj in queryInstance)
{
   Console.WriteLine(&quot;User Name: &quot; + cimObj.CimInstanceProperties[&quot;UserName&quot;].ToString());
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0aa4d-144">... renommer un ordinateur ?</span><span class="sxs-lookup"><span data-stu-id="0aa4d-144">...rename a computer?</span></span></td>
<td><p><span data-ttu-id="0aa4d-145">Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> et la méthode <strong>Rename</strong> .</span><span class="sxs-lookup"><span data-stu-id="0aa4d-145">Use the <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> class, and the <strong>Rename</strong> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0aa4d-146">VB</span><span class="sxs-lookup"><span data-stu-id="0aa4d-146">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colComputers = objWMIService.ExecQuery(&quot;Select * from Win32_ComputerSystem&quot;)
For Each objComputer in colComputers
    errReturn = ObjComputer.Rename(&quot;NewName&quot;)
    WScript.Echo &quot;Computer name is now &quot; & objComputer.Name
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
<th><span data-ttu-id="0aa4d-147">PowerShell</span><span class="sxs-lookup"><span data-stu-id="0aa4d-147">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>param (
[$String] $NewName = &#39;NewName&#39;,
[$string] $Comp = &quot;.&quot;
}

<# Get computer object #>
$Computer = Get-WmiObject -Class Win32_ComputerSystem -ComputerName $comp

<# Rename the Computer #>
$Return  = $Computer.Rename($NewName)

if ($return.ReturnValue -eq 0) {
   &quot;Computer name is now: $NewName&quot;
   &quot; but you need to reboot first&quot;
} else {
&quot;  RenameFailed, return code: {0}&quot; -f $return.ReturnValue
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aa4d-148">... récupérer uniquement les groupes locaux à l’aide de WMI ?</span><span class="sxs-lookup"><span data-stu-id="0aa4d-148">...retrieve only local groups using WMI?</span></span></td>
<td><p><span data-ttu-id="0aa4d-149">Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-group"><strong>Win32_Group</strong></a> et incluez la clause <strong>Where</strong> suivante dans votre requête <a href="querying-with-wql.md">WQL</a> .</span><span class="sxs-lookup"><span data-stu-id="0aa4d-149">Use the <a href="/windows/desktop/CIMWin32Prov/win32-group"><strong>Win32_Group</strong></a> class and include the following <strong>WHERE</strong> clause in your <a href="querying-with-wql.md">WQL</a> query.</span></span></p>
<p><code>Where LocalAccount = True</code></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0aa4d-150">VB</span><span class="sxs-lookup"><span data-stu-id="0aa4d-150">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject( _
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery _
    (&quot;Select * from Win32_Group  Where LocalAccount = True&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Local Account: &quot; & objItem.LocalAccount & VBNewLine _
        & &quot;Name: &quot; & objItem.Name & VBNewLine _
        & &quot;SID: &quot; & objItem.SID & VBNewLine _
        & &quot;SID Type: &quot; & objItem.SIDType & VBNewLine _
        & &quot;Status: &quot; & objItem.Status & VBNewLine
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
<th><span data-ttu-id="0aa4d-151">PowerShell</span><span class="sxs-lookup"><span data-stu-id="0aa4d-151">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$Accts=Get-WMIObjectWin32_Group|where {$_.LocalAccount}
$accts |ftName, Sid, SidType, Status-autosize</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="0aa4d-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0aa4d-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0aa4d-153">Tâches WMI pour les scripts et les applications</span><span class="sxs-lookup"><span data-stu-id="0aa4d-153">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="0aa4d-154">Exemples d’applications WMI C++</span><span class="sxs-lookup"><span data-stu-id="0aa4d-154">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="0aa4d-155">ScriptCenter TechNet</span><span class="sxs-lookup"><span data-stu-id="0aa4d-155">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>
