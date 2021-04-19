---
description: Pour obtenir des données à partir de WMI, sur l’ordinateur local ou à partir d’un ordinateur distant, vous devez vous connecter au service WMI en vous connectant à un espace de noms spécifique.
ms.assetid: 71ff6b06-af7d-43ee-ae6e-1964ec249472
ms.tgt_platform: multiple
title: 'Tâches WMI : connexion au service WMI'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 751c6c0802c30e113f4a2b7ddc646cdf5646b7dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534195"
---
# <a name="wmi-tasks-connecting-to-the-wmi-service"></a><span data-ttu-id="a44b6-103">Tâches WMI : connexion au service WMI</span><span class="sxs-lookup"><span data-stu-id="a44b6-103">WMI Tasks: Connecting to the WMI Service</span></span>

<span data-ttu-id="a44b6-104">Pour obtenir des données à partir de WMI, sur l’ordinateur local ou à partir d’un ordinateur distant, vous devez vous connecter au service WMI en vous connectant à un [*espace de noms*](gloss-n.md)spécifique.</span><span class="sxs-lookup"><span data-stu-id="a44b6-104">To get data from WMI, either on the local computer or from a remote computer, you must connect to the WMI service by connecting to a specific [*namespace*](gloss-n.md).</span></span> <span data-ttu-id="a44b6-105">Dans la plupart des cas, utilisez soit la connexion sténographique [moniker](creating-a-wmi-script.md) , soit la connexion [**localisateur**](swbemlocator-connectserver.md) .</span><span class="sxs-lookup"><span data-stu-id="a44b6-105">In most cases, use either the shorthand [moniker](creating-a-wmi-script.md) connection or the [**Locator**](swbemlocator-connectserver.md) connection.</span></span> <span data-ttu-id="a44b6-106">Pour obtenir d’autres exemples, consultez le site TechNet ScriptCenter à l’adresse [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a44b6-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="a44b6-107">Les connexions distantes nécessitent des paramètres appropriés pour le pare-feu Windows et DCOM.</span><span class="sxs-lookup"><span data-stu-id="a44b6-107">Remote connections require proper settings for the Windows Firewall and DCOM.</span></span> <span data-ttu-id="a44b6-108">Pour plus d’informations, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md) et [connexion via le pare-feu Windows](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).</span><span class="sxs-lookup"><span data-stu-id="a44b6-108">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md) and [Connecting Through Windows Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).</span></span> <span data-ttu-id="a44b6-109">À compter de Windows Vista, le contrôle de compte d’utilisateur (UAC) peut affecter l’accès WMI.</span><span class="sxs-lookup"><span data-stu-id="a44b6-109">Starting with Windows Vista, User Account Control (UAC) can affect WMI access.</span></span> <span data-ttu-id="a44b6-110">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="a44b6-110">For more information, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

<span data-ttu-id="a44b6-111">Les exemples de scripts présentés dans cette rubrique obtiennent des données uniquement à partir de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="a44b6-111">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="a44b6-112">Pour plus d’informations sur l’utilisation du script pour obtenir des données à partir d’ordinateurs distants, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="a44b6-112">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="a44b6-113">La procédure suivante décrit comment exécuter un script.</span><span class="sxs-lookup"><span data-stu-id="a44b6-113">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="a44b6-114">**Pour exécuter un script**</span><span class="sxs-lookup"><span data-stu-id="a44b6-114">**To run a script**</span></span>

1.  <span data-ttu-id="a44b6-115">Copiez le code et enregistrez-le dans un fichier avec une extension. vbs, par exemple *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="a44b6-115">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="a44b6-116">Assurez-vous que votre éditeur de texte n’ajoute pas d’extension. txt au fichier.</span><span class="sxs-lookup"><span data-stu-id="a44b6-116">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="a44b6-117">Ouvrez une fenêtre d’invite de commandes et accédez au répertoire où vous avez enregistré le fichier.</span><span class="sxs-lookup"><span data-stu-id="a44b6-117">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="a44b6-118">Tapez **cscript filename.vbs** à l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="a44b6-118">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="a44b6-119">Si vous ne pouvez pas accéder à un journal des événements, vérifiez si vous exécutez à partir d’une invite de commandes avec élévation de privilèges.</span><span class="sxs-lookup"><span data-stu-id="a44b6-119">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="a44b6-120">Certains journaux des événements, tels que le journal des événements de sécurité, peuvent être protégés par les contrôles d’accès utilisateur (UAC).</span><span class="sxs-lookup"><span data-stu-id="a44b6-120">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="a44b6-121">Par défaut, cscript affiche la sortie d’un script dans la fenêtre d’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="a44b6-121">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="a44b6-122">Étant donné que les scripts WMI peuvent générer de grandes quantités de sortie, vous souhaiterez peut-être rediriger la sortie vers un fichier.</span><span class="sxs-lookup"><span data-stu-id="a44b6-122">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="a44b6-123">Tapez **cscript filename.vbs > outfile.txt** à l’invite de commandes pour rediriger la sortie du script *filename.vbs* vers *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="a44b6-123">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="a44b6-124">Le tableau suivant répertorie des exemples de scripts qui peuvent être utilisés pour obtenir différents types de données à partir de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="a44b6-124">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a44b6-125">Comment puis-je...</span><span class="sxs-lookup"><span data-stu-id="a44b6-125">How do I...</span></span></th>
<th><span data-ttu-id="a44b6-126">Classes ou méthodes WMI</span><span class="sxs-lookup"><span data-stu-id="a44b6-126">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a44b6-127">... se connecter à un ordinateur distant à l’aide de WMI ?</span><span class="sxs-lookup"><span data-stu-id="a44b6-127">...connect to a remote computer using WMI?</span></span></td>
<td><span data-ttu-id="a44b6-128">Spécifiez l’un des éléments suivants dans le cadre de votre chaîne de connexion <a href="constructing-a-moniker-string.md">moniker</a> :</span><span class="sxs-lookup"><span data-stu-id="a44b6-128">Specify one of the following as part of your <a href="constructing-a-moniker-string.md">moniker</a> connection string:</span></span><br/>
<ul>
<li><span data-ttu-id="a44b6-129">Un nom d’ordinateur NetBIOS, tel que &quot; ATL-DC-01&quot;</span><span class="sxs-lookup"><span data-stu-id="a44b6-129">A NetBIOS computer name, such as &quot;atl-dc-01&quot;</span></span></li>
<li><span data-ttu-id="a44b6-130">Un nom de domaine complet, tel que &quot; ATL-DC-01.fabrikam.com&quot;</span><span class="sxs-lookup"><span data-stu-id="a44b6-130">A fully qualified domain name, such as &quot;atl-dc-01.fabrikam.com&quot;</span></span></li>
<li><span data-ttu-id="a44b6-131">Une adresse IPv4, telle que &quot; 192.168.1.1&quot;</span><span class="sxs-lookup"><span data-stu-id="a44b6-131">An IPv4 address, such as &quot;192.168.1.1&quot;</span></span></li>
<li><span data-ttu-id="a44b6-132">À compter de Windows Vista, vous pouvez spécifier une adresse IPv6 si l’ordinateur cible et l’ordinateur à partir desquels vous établissez la connexion exécutent IPv6.</span><span class="sxs-lookup"><span data-stu-id="a44b6-132">Starting with Windows Vista, you can specify an IPv6 address if the target computer and the computer from which you are making the connection both run IPv6.</span></span><br/></li>
</ul>
<span data-ttu-id="a44b6-133">Pour plus d’informations, consultez <a href="connecting-to-wmi-on-a-remote-computer.md">connexion à WMI sur un ordinateur distant</a> et <a href="ipv6-and-ipv4-support-in-wmi.md">prise en charge d’IPv6 et IPv4 dans WMI</a>.</span><span class="sxs-lookup"><span data-stu-id="a44b6-133">For more information, see <a href="connecting-to-wmi-on-a-remote-computer.md">Connecting to WMI on a Remote Computer</a> and <a href="ipv6-and-ipv4-support-in-wmi.md">IPv6 and IPv4 Support in WMI</a>.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a44b6-134">VB</span><span class="sxs-lookup"><span data-stu-id="a44b6-134">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colProcessList = objWMIService.ExecQuery (&quot;Select * from Win32_Process&quot;)
For Each objProcess in colProcessList
    Wscript.Echo &quot;Process Name: &quot; & objProcess.Name 
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
<th><span data-ttu-id="a44b6-135">PowerShell</span><span class="sxs-lookup"><span data-stu-id="a44b6-135">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Get-WmiObject -Class Win32_Process -ComputerName $strComputer -Namespace &quot;root\cimv2&quot; | format-list -Property Name</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="a44b6-136">... exécuter un script WMI sous autres informations d’identification ?</span><span class="sxs-lookup"><span data-stu-id="a44b6-136">...run a WMI script under alternate credentials?</span></span></td>
<td><p><span data-ttu-id="a44b6-137">Utilisez la méthode <a href="swbemlocator-connectserver.md"><strong>SWbemLocator. ConnectServer</strong></a> , ou <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver"><strong>IWbemLocator :: ConnectServer</strong></a> en C++, et incluez le nom d’utilisateur et le mot de passe appropriés.</span><span class="sxs-lookup"><span data-stu-id="a44b6-137">Use the <a href="swbemlocator-connectserver.md"><strong>SWbemLocator.ConnectServer</strong></a> method, or <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver"><strong>IWbemLocator::ConnectServer</strong></a> in C++, and include the appropriate user name and password.</span></span> <span data-ttu-id="a44b6-138">Vous ne pouvez pas modifier les informations d’identification lors de la connexion à l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="a44b6-138">You cannot change credentials when connecting to the local computer.</span></span> <span data-ttu-id="a44b6-139">Pour plus d’informations, consultez <a href="creating-a-wmi-script.md">création d’un script WMI</a> et <a href="connecting-to-wmi-on-a-remote-computer.md">connexion à WMI sur un ordinateur distant</a>.</span><span class="sxs-lookup"><span data-stu-id="a44b6-139">For more information, see <a href="creating-a-wmi-script.md">Creating a WMI Script</a> and <a href="connecting-to-wmi-on-a-remote-computer.md">Connecting to WMI on a Remote Computer</a>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a44b6-140">VB</span><span class="sxs-lookup"><span data-stu-id="a44b6-140">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Set objSWbemLocator = CreateObject(&quot;WbemScripting.SWbemLocator&quot;)
Set objSWbemServices = objSWbemLocator.ConnectServer (strComputer, &quot;root\cimv2&quot;, &quot;fabrikam\administrator&quot;, &quot;password&quot;)
Set colProcessList = objSWbemServices.ExecQuery(&quot;Select * From Win32_Process&quot;)
For Each objProcess in colProcessList
    Wscript.Echo &quot;Process Name: &quot; & objProcess.Name 
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
<th><span data-ttu-id="a44b6-141">PowerShell</span><span class="sxs-lookup"><span data-stu-id="a44b6-141">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$StrComputer = &quot;atl-dc-01&quot;
$strCredentials = &quot;FABRIKAM\administrator&quot;
Get-WmiObject -Class Win32_Process -ComputerName $strComputer -Namespace &quot;root\cimv2&quot; -credential $strCredentials `
   -Impersonation Impersonate | format-list -Property Name</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="a44b6-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a44b6-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a44b6-143">Tâches WMI pour les scripts et les applications</span><span class="sxs-lookup"><span data-stu-id="a44b6-143">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="a44b6-144">Exemples d’applications WMI C++</span><span class="sxs-lookup"><span data-stu-id="a44b6-144">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="a44b6-145">ScriptCenter TechNet</span><span class="sxs-lookup"><span data-stu-id="a44b6-145">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

 



`
