---
description: Les tâches WMI pour les logiciels informatiques obtiennent des informations telles que le logiciel installé par le Microsoft Windows Installer (MSI) et les versions logicielles. Pour obtenir d’autres exemples, consultez le site TechNet ScriptCenter à l’adresse https://www.microsoft.com/technet .
ms.assetid: 65a61be3-7870-4178-9e96-78b82898271f
ms.tgt_platform: multiple
title: 'Tâches WMI : logiciel informatique'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 800a42764cbb1b9552a8ecc87debc04685d28850
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530075"
---
# <a name="wmi-tasks-computer-software"></a><span data-ttu-id="22ff3-104">Tâches WMI : logiciel informatique</span><span class="sxs-lookup"><span data-stu-id="22ff3-104">WMI Tasks: Computer Software</span></span>

<span data-ttu-id="22ff3-105">Les tâches WMI pour les logiciels informatiques obtiennent des informations telles que le logiciel installé par le Microsoft Windows Installer (MSI) et les versions logicielles.</span><span class="sxs-lookup"><span data-stu-id="22ff3-105">WMI tasks for computer software obtain information such as which software is installed by the Microsoft Windows Installer (MSI) and software versions.</span></span> <span data-ttu-id="22ff3-106">Pour obtenir d’autres exemples, consultez le site TechNet ScriptCenter à l’adresse [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="22ff3-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="22ff3-107">Les exemples de scripts présentés dans cette rubrique obtiennent des données uniquement à partir de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="22ff3-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="22ff3-108">Pour plus d’informations sur l’utilisation du script pour obtenir des données à partir d’ordinateurs distants, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="22ff3-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="22ff3-109">La procédure suivante décrit comment exécuter un script.</span><span class="sxs-lookup"><span data-stu-id="22ff3-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="22ff3-110">**Pour exécuter un script**</span><span class="sxs-lookup"><span data-stu-id="22ff3-110">**To run a script**</span></span>

1.  <span data-ttu-id="22ff3-111">Copiez le code et enregistrez-le dans un fichier avec une extension. vbs, par exemple *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="22ff3-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="22ff3-112">Assurez-vous que votre éditeur de texte n’ajoute pas d’extension. txt au fichier.</span><span class="sxs-lookup"><span data-stu-id="22ff3-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="22ff3-113">Ouvrez une fenêtre d’invite de commandes et accédez au répertoire où vous avez enregistré le fichier.</span><span class="sxs-lookup"><span data-stu-id="22ff3-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="22ff3-114">Tapez **cscript filename.vbs** à l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="22ff3-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="22ff3-115">Si vous ne pouvez pas accéder à un journal des événements, vérifiez si vous exécutez à partir d’une invite de commandes avec élévation de privilèges.</span><span class="sxs-lookup"><span data-stu-id="22ff3-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="22ff3-116">Certains journaux des événements, tels que le journal des événements de sécurité, peuvent être protégés par les contrôles d’accès utilisateur (UAC).</span><span class="sxs-lookup"><span data-stu-id="22ff3-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="22ff3-117">Par défaut, cscript affiche la sortie d’un script dans la fenêtre d’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="22ff3-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="22ff3-118">Étant donné que les scripts WMI peuvent générer de grandes quantités de sortie, vous souhaiterez peut-être rediriger la sortie vers un fichier.</span><span class="sxs-lookup"><span data-stu-id="22ff3-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="22ff3-119">Tapez **cscript filename.vbs > outfile.txt** à l’invite de commandes pour rediriger la sortie du script *filename.vbs* vers *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="22ff3-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

> [!Note]  
> <span data-ttu-id="22ff3-120">L’exécution d’une \* requête « Select from Win32 \_ Product » peut entraîner un comportement inattendu.</span><span class="sxs-lookup"><span data-stu-id="22ff3-120">Running a "Select \* from Win32\_Product" query may result in unexpected behavior.</span></span> <span data-ttu-id="22ff3-121">Cela est dû au fait que le fournisseur qui prend en charge le \_ produit Win32 n’est pas optimisé pour les requêtes.</span><span class="sxs-lookup"><span data-stu-id="22ff3-121">This is because the provider that supports Win32\_Product is not query optimized.</span></span> <span data-ttu-id="22ff3-122">Pour plus d’informations, consultez [l’Article 974524](https://support.microsoft.com/kb/974524)de la base de connaissances.</span><span class="sxs-lookup"><span data-stu-id="22ff3-122">For more information, see [KB Article 974524](https://support.microsoft.com/kb/974524).</span></span>

 

<span data-ttu-id="22ff3-123">Le tableau suivant répertorie des exemples de scripts qui peuvent être utilisés pour obtenir différents types de données à partir de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="22ff3-123">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="22ff3-124">Comment puis-je...</span><span class="sxs-lookup"><span data-stu-id="22ff3-124">How do I...</span></span></th>
<th><span data-ttu-id="22ff3-125">Classes ou méthodes WMI</span><span class="sxs-lookup"><span data-stu-id="22ff3-125">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="22ff3-126">... désinstaller le logiciel à l’aide d’un script ?</span><span class="sxs-lookup"><span data-stu-id="22ff3-126">...uninstall software using a script?</span></span></td>
<td><span data-ttu-id="22ff3-127">Si le logiciel a été installé à l’aide de Microsoft Windows Installer (MSI), utilisez la classe WMI <a href="/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)"><strong>Win32_Product</strong></a> et la méthode <a href="/previous-versions/windows/desktop/msiprov/uninstall-method-in-class-win32-product"><strong>Uninstall</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="22ff3-127">If the software was installed using Microsoft Windows Installer (MSI), use the WMI class <a href="/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)"><strong>Win32_Product</strong></a> and the <a href="/previous-versions/windows/desktop/msiprov/uninstall-method-in-class-win32-product"><strong>Uninstall</strong></a> method.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="22ff3-128">VB</span><span class="sxs-lookup"><span data-stu-id="22ff3-128">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
Set colSoftware = objWMIService.ExecQuery _
    (&quot;Select * from Win32_Product &quot; _
        & &quot;Where Name = &#39;Personnel database&#39;&quot;)
For Each objSoftware in colSoftware
    objSoftware.Uninstall()
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
<th><span data-ttu-id="22ff3-129">PowerShell</span><span class="sxs-lookup"><span data-stu-id="22ff3-129">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$colSoftware = Get-WmiObject -Class Win32_Product | Where-Object {$_.name -eq &quot;Personnel database&quot;}

foreach ($colItem in $colSoftware)
{
    $colItem.Uninstall()
}</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="22ff3-130">... Inventoriez-vous tous les logiciels installés sur un ordinateur à l’aide d’un script ?</span><span class="sxs-lookup"><span data-stu-id="22ff3-130">...inventory all the software installed on a computer with a script?</span></span></td>
<td><p><span data-ttu-id="22ff3-131">Si le logiciel a été installé à l’aide de Microsoft Windows Installer (MSI), utilisez la <a href="/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)"><strong>Win32_Product</strong></a>de classe WMI.</span><span class="sxs-lookup"><span data-stu-id="22ff3-131">If the software was installed using Microsoft Windows Installer (MSI) use the WMI class <a href="/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)"><strong>Win32_Product</strong></a>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="22ff3-132">VB</span><span class="sxs-lookup"><span data-stu-id="22ff3-132">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
Set colSoftware = objWMIService.ExecQuery _
    (&quot;Select * from Win32_Product&quot;)

For Each objSoftware in colSoftware
    Wscript.Echo &quot;Name: &quot; & objSoftware.Name
    Wscript.Echo &quot;Version: &quot; & objSoftware.Version
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
<th><span data-ttu-id="22ff3-133">PowerShell</span><span class="sxs-lookup"><span data-stu-id="22ff3-133">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$colSoftware = Get-WmiObject -Class Win32_Product

foreach ($colItem in $colSoftware)
{
    &quot;Name: &quot; + $colItem.Name
    &quot;Version: &quot;+ $colItem.Version
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22ff3-134">... déterminer quelle version de Microsoft Office est installée ?</span><span class="sxs-lookup"><span data-stu-id="22ff3-134">...determine what version of Microsoft Office is installed?</span></span></td>
<td><p><span data-ttu-id="22ff3-135">Utilisez la classe <a href="/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)"><strong>Win32_Product</strong></a> et vérifiez la valeur de la propriété <strong>version</strong> .</span><span class="sxs-lookup"><span data-stu-id="22ff3-135">Use the <a href="/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)"><strong>Win32_Product</strong></a> class and check the value of the <strong>Version</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="22ff3-136">VB</span><span class="sxs-lookup"><span data-stu-id="22ff3-136">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
Set colSoftware = objWMIService.ExecQuery(_
    &quot;Select * from Win32_Product &quot; & _
    &quot;Where IdentifyingNumber =&quot; _
        & &quot; &#39;{90280409-6000-11D3-8CFE-0050048383C9}&#39;&quot;)
For Each objItem in colSoftware
    Wscript.Echo &quot;Name: &quot; & objItem.Name
    Wscript.Echo &quot;Version: &quot; & objItem.Version
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
<th><span data-ttu-id="22ff3-137">PowerShell</span><span class="sxs-lookup"><span data-stu-id="22ff3-137">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$colSoftware = Get-WmiObject -Class Win32_Product | Where-Object {$_.IdentifyingNumber -eq &quot;{90280409-6000-11D3-8CFE-0050048383C9}&quot;}

foreach ($colItem in $colSoftware)
{
    &quot;Name: &quot; + $colItem.Name
    &quot;Version: &quot; + $colItem.Version
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a><span data-ttu-id="22ff3-138">Exemples</span><span class="sxs-lookup"><span data-stu-id="22ff3-138">Examples</span></span>

<span data-ttu-id="22ff3-139">L’exemple de code PowerShell PowerShell [Remote PC info](https://Gallery.TechNet.Microsoft.Com/2a8a008c-ee30-4b50-a81a-1b7545ef3436) utilise un certain nombre de classes matérielles et logicielles, notamment Win32Product, pour rechercher diverses informations sur un PC distant à l’aide de WMI et du Registre distant.</span><span class="sxs-lookup"><span data-stu-id="22ff3-139">The [Powershell Remote PC Info Script](https://Gallery.TechNet.Microsoft.Com/2a8a008c-ee30-4b50-a81a-1b7545ef3436) PowerShell code sample uses a number of hardware and software classes, including Win32Product, to find various information about a remote PC using WMI and the remote registry.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22ff3-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="22ff3-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22ff3-141">Tâches WMI pour les scripts et les applications</span><span class="sxs-lookup"><span data-stu-id="22ff3-141">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="22ff3-142">Exemples d’applications WMI C++</span><span class="sxs-lookup"><span data-stu-id="22ff3-142">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="22ff3-143">ScriptCenter TechNet</span><span class="sxs-lookup"><span data-stu-id="22ff3-143">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

