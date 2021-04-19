---
description: WMI fournit une infrastructure de gestion de système standardisée qui peut être exploitée par un certain nombre de clients différents.
ms.assetid: 7aa0ead7-010c-4ad2-b6ba-0ef84263d5c6
ms.tgt_platform: multiple
title: Création de clients WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd6d89c63218ffd20ef66b2115e581bdb9c4373
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524994"
---
# <a name="creating-wmi-clients"></a><span data-ttu-id="ab9d3-103">Création de clients WMI</span><span class="sxs-lookup"><span data-stu-id="ab9d3-103">Creating WMI Clients</span></span>

<span data-ttu-id="ab9d3-104">WMI fournit une infrastructure de gestion de système standardisée qui peut être exploitée par un certain nombre de clients différents.</span><span class="sxs-lookup"><span data-stu-id="ab9d3-104">WMI provides a standardized system management infrastructure that can be leveraged by a number of different clients.</span></span> <span data-ttu-id="ab9d3-105">Ces clients vont de l’outil en ligne de commande wmic.exe à System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="ab9d3-105">These clients range from the wmic.exe command line tool to System Center Operations Manager.</span></span> <span data-ttu-id="ab9d3-106">Vous pouvez écrire vos propres clients WMI en utilisant l’API de script WMI, l’API C++ native ou en utilisant les types de l’espace de noms de la bibliothèque de classes System. Management .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="ab9d3-106">You can write your own WMI clients by using either the WMI Scripting API, the native C++ API or by using the types in the System.Management .NET Framework class library namespace.</span></span>

## <a name="how-to-create-a-wmi-client"></a><span data-ttu-id="ab9d3-107">Comment créer un client WMI</span><span class="sxs-lookup"><span data-stu-id="ab9d3-107">How to create a WMI client</span></span>

<span data-ttu-id="ab9d3-108">Les fonctionnalités principales de WMI consistent à récupérer des objets de l’espace de stockage WMI et à examiner les propriétés de ces objets.</span><span class="sxs-lookup"><span data-stu-id="ab9d3-108">The core functionality of WMI consists of retrieving objects from the WMI repository and examining the properties of those objects.</span></span> <span data-ttu-id="ab9d3-109">Vous pouvez également choisir de mettre à jour ces propriétés ou d’appeler des méthodes sur ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="ab9d3-109">You can also choose to update those properties, or call methods on those properties.</span></span> <span data-ttu-id="ab9d3-110">Les exemples suivants montrent comment effectuer une tâche d’administration WMI de base : récupération du nom de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="ab9d3-110">The following examples show how to perform a basic WMI administration task: retrieving the name of the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ab9d3-111">Terme</span><span class="sxs-lookup"><span data-stu-id="ab9d3-111">Term</span></span></th>
<th><span data-ttu-id="ab9d3-112">Description</span><span class="sxs-lookup"><span data-stu-id="ab9d3-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ab9d3-113"><span id="Creating_a_client_with_PowerShell"></span><span id="creating_a_client_with_powershell"></span><span id="CREATING_A_CLIENT_WITH_POWERSHELL"></span>Création d’un client avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="ab9d3-113"><span id="Creating_a_client_with_PowerShell"></span><span id="creating_a_client_with_powershell"></span><span id="CREATING_A_CLIENT_WITH_POWERSHELL"></span>Creating a client with PowerShell</span></span><br/></td>
<td><span data-ttu-id="ab9d3-114">WMI et PowerShell sont étroitement intégrés. par conséquent, la récupération d’objets WMI avec PowerShell consiste simplement à appeler l’applet de commande Get-WmiObject.</span><span class="sxs-lookup"><span data-stu-id="ab9d3-114">WMI and PowerShell are tightly integrated; as such, retrieving WMI objects with PowerShell is simply a matter of calling the Get-WmiObject cmdlet.</span></span> <span data-ttu-id="ab9d3-115">Notez que, pour des fins de cohérence, le premier extrait de code indique explicitement la plupart des valeurs par défaut ; le deuxième suppose que les valeurs par défaut sont correctes.</span><span class="sxs-lookup"><span data-stu-id="ab9d3-115">Note that for consistency, the first code snippet explicitly states many of the default values; the second assumes that the default values are correct.</span></span><br/> <span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ab9d3-116">PowerShell</span><span class="sxs-lookup"><span data-stu-id="ab9d3-116">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#explicitly states many of the default parameters
$myComputer = Get-WmiObject -ComputerName &quot;.&quot; -Namespace &quot;root\cimv2&quot; -Query &quot;SELECT * FROM Win32_ComputerSystem&quot;
foreach ($computer in $myComputer)
{ &quot;System Name: &quot; + $computer.name }

#assumes the default values are correct
Get-WmiObject Win32_ComputerSystem | Format-Table &quot;Name&quot;</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab9d3-117"><span id="Creating_a_client_with_VBScript"></span><span id="creating_a_client_with_vbscript"></span><span id="CREATING_A_CLIENT_WITH_VBSCRIPT"></span>Création d’un client à l’aide de VBScript</span><span class="sxs-lookup"><span data-stu-id="ab9d3-117"><span id="Creating_a_client_with_VBScript"></span><span id="creating_a_client_with_vbscript"></span><span id="CREATING_A_CLIENT_WITH_VBSCRIPT"></span>Creating a client with VBScript</span></span></p></td>
<td><p><span data-ttu-id="ab9d3-118">VBScript était le langage de script d’origine qui avait été couramment utilisé avec WMI.</span><span class="sxs-lookup"><span data-stu-id="ab9d3-118">VBScript was the original scripting language that had common use with WMI.</span></span> <span data-ttu-id="ab9d3-119">Alors que PowerShell est devenu plus populaire, un grand nombre des exemples de code existants dans cette documentation sont écrits en VBScript.</span><span class="sxs-lookup"><span data-stu-id="ab9d3-119">While PowerShell has become more popular, many of the existing code samples in this documentation are written in VBScript.</span></span> <span data-ttu-id="ab9d3-120">Notez que cet exemple VBScript particulier indique explicitement le chemin d’accès à l’ordinateur local, ainsi que le niveau d’emprunt d’identité. ce n’est pas obligatoire, mais il s’agit souvent d’une bonne pratique.</span><span class="sxs-lookup"><span data-stu-id="ab9d3-120">Note that this particular VBScript sample explicitly states both the local machine path as well as the impersonation level; this is not required, but is often a best practice.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ab9d3-121">VB</span><span class="sxs-lookup"><span data-stu-id="ab9d3-121">VB</span></span></th>
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

</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ab9d3-122"><span id="Creating_a_client_with_C___Microsoft.Management.Infrastructure_"></span><span id="creating_a_client_with_c___microsoft.management.infrastructure_"></span><span id="CREATING_A_CLIENT_WITH_C___MICROSOFT.MANAGEMENT.INFRASTRUCTURE_"></span>Création d’un client avec C# (<a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft. Management. infrastructure</a>)</span><span class="sxs-lookup"><span data-stu-id="ab9d3-122"><span id="Creating_a_client_with_C___Microsoft.Management.Infrastructure_"></span><span id="creating_a_client_with_c___microsoft.management.infrastructure_"></span><span id="CREATING_A_CLIENT_WITH_C___MICROSOFT.MANAGEMENT.INFRASTRUCTURE_"></span>Creating a client with C# (<a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft.Management.Infrastructure</a>)</span></span></p></td>
<td><p><span data-ttu-id="ab9d3-123">Cet espace de noms contient la solution actuelle pour accéder à WMI avec du code managé, et est connu sous le nom d’infrastructure de gestion Windows (MI ou WMIv2).</span><span class="sxs-lookup"><span data-stu-id="ab9d3-123">This namespace contains the current solution for accessing WMI with managed code, and is known as the Windows Management Infrastructure (MI, or WMIv2).</span></span> <span data-ttu-id="ab9d3-124">À l’heure actuelle, MI est la technologie prise en charge pour la création de clients de gestion gérés.</span><span class="sxs-lookup"><span data-stu-id="ab9d3-124">Currently, MI is the supported technology for creating managed management clients.</span></span> <span data-ttu-id="ab9d3-125">Pour plus d’informations, consultez <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client">comment implémenter un client mi géré</a> et <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-native-mi-client">comment implémenter un client mi natif</a>.</span><span class="sxs-lookup"><span data-stu-id="ab9d3-125">For more information, see <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client">How to Implement a Managed MI Client</a> and <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-native-mi-client">How to Implement a Native MI Client</a>.</span></span></p>
<div class="code">
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ab9d3-126">C#</span><span class="sxs-lookup"><span data-stu-id="ab9d3-126">C#</span></span></th>
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
<td><p><span data-ttu-id="ab9d3-127"><span id="Creating_a_client_with_C___System.Management_"></span><span id="creating_a_client_with_c___system.management_"></span><span id="CREATING_A_CLIENT_WITH_C___SYSTEM.MANAGEMENT_"></span>Création d’un client avec C# (<a href="/dotnet/api/system.management">System. Management</a>)</span><span class="sxs-lookup"><span data-stu-id="ab9d3-127"><span id="Creating_a_client_with_C___System.Management_"></span><span id="creating_a_client_with_c___system.management_"></span><span id="CREATING_A_CLIENT_WITH_C___SYSTEM.MANAGEMENT_"></span>Creating a client with C# (<a href="/dotnet/api/system.management">System.Management</a>)</span></span></p></td>
<td><p><span data-ttu-id="ab9d3-128">Cet espace de noms contient la solution d’origine pour accéder à WMI avec du code managé.</span><span class="sxs-lookup"><span data-stu-id="ab9d3-128">This namespace contains the original solution for accessing WMI with managed code.</span></span> <span data-ttu-id="ab9d3-129">Alors que les classes <a href="/dotnet/api/system.management">System. Management</a> sont toujours disponibles, les classes <a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft. Management. infrastructure</a> sont généralement plus efficaces et plus évolutives.</span><span class="sxs-lookup"><span data-stu-id="ab9d3-129">While the <a href="/dotnet/api/system.management">System.Management</a> classes are still available, the <a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft.Management.Infrastructure</a> classes are generally more efficient and scale better.</span></span> <span data-ttu-id="ab9d3-130">Par conséquent, il est recommandé d’utiliser les classes MI, plutôt que les classes WMI d’origine.</span><span class="sxs-lookup"><span data-stu-id="ab9d3-130">As such, it is recommended that you use the MI classes, rather than the original WMI classes.</span></span></p>
<div class="code">
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ab9d3-131">C#</span><span class="sxs-lookup"><span data-stu-id="ab9d3-131">C#</span></span></th>
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
</tbody>
</table>



 

<span data-ttu-id="ab9d3-132">Le tableau ci-dessous répertorie les rubriques traitées dans cette section.</span><span class="sxs-lookup"><span data-stu-id="ab9d3-132">The following table lists the topics covered in this section.</span></span>



| <span data-ttu-id="ab9d3-133">Rubrique</span><span class="sxs-lookup"><span data-stu-id="ab9d3-133">Topic</span></span>                                                                                                        | <span data-ttu-id="ab9d3-134">Description</span><span class="sxs-lookup"><span data-stu-id="ab9d3-134">Description</span></span>                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ab9d3-135">Connexion à WMI sur un ordinateur distant</span><span class="sxs-lookup"><span data-stu-id="ab9d3-135">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)                         | <span data-ttu-id="ab9d3-136">Décrit un certain nombre de problèmes qui surviennent lorsque des clients utilisent l’infrastructure WMI sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="ab9d3-136">Describes a number of issues that arise when clients use the WMI infrastructure on a remote computer.</span></span>                                                                                          |
| [<span data-ttu-id="ab9d3-137">Tâches WMI pour les scripts et les applications</span><span class="sxs-lookup"><span data-stu-id="ab9d3-137">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)                         | <span data-ttu-id="ab9d3-138">Montre un exemple de code de client WMI.</span><span class="sxs-lookup"><span data-stu-id="ab9d3-138">Shows example WMI client code.</span></span>                                                                                                                                                                 |
| [<span data-ttu-id="ab9d3-139">Création d’une application ou d’un script WMI</span><span class="sxs-lookup"><span data-stu-id="ab9d3-139">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)                             | <span data-ttu-id="ab9d3-140">Fournit des informations sur la création de différents clients WMI.</span><span class="sxs-lookup"><span data-stu-id="ab9d3-140">Provides information about creating various WMI clients.</span></span>                                                                                                                                       |
| [<span data-ttu-id="ab9d3-141">Analyse des données de performances</span><span class="sxs-lookup"><span data-stu-id="ab9d3-141">Monitoring Performance Data</span></span>](monitoring-performance-data.md)                                               | <span data-ttu-id="ab9d3-142">Décrit comment utiliser WMI pour analyser les données de performances.</span><span class="sxs-lookup"><span data-stu-id="ab9d3-142">Describes how to use WMI to monitor performance data.</span></span>                                                                                                                                          |
| [<span data-ttu-id="ab9d3-143">Réception d’un événement WMI</span><span class="sxs-lookup"><span data-stu-id="ab9d3-143">Receiving a WMI Event</span></span>](receiving-a-wmi-event.md)                                                           | <span data-ttu-id="ab9d3-144">Décrit comment afficher les événements WMI.</span><span class="sxs-lookup"><span data-stu-id="ab9d3-144">Describes how to view WMI events.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="ab9d3-145">Événements d’analyse</span><span class="sxs-lookup"><span data-stu-id="ab9d3-145">Monitoring Events</span></span>](monitoring-events.md)                                                                   | <span data-ttu-id="ab9d3-146">Décrit comment surveiller les événements WMI.</span><span class="sxs-lookup"><span data-stu-id="ab9d3-146">Describes how to monitor WMI events.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="ab9d3-147">Interrogation avec WQL</span><span class="sxs-lookup"><span data-stu-id="ab9d3-147">Querying with WQL</span></span>](querying-with-wql.md)                                                                   | <span data-ttu-id="ab9d3-148">Présente le Langage de requêtes WMI (WQL) (WQL).</span><span class="sxs-lookup"><span data-stu-id="ab9d3-148">Introduces the WMI Query Language (WQL).</span></span>                                                                                                                                                       |
| [<span data-ttu-id="ab9d3-149">Interrogation de l’état des fonctionnalités facultatives</span><span class="sxs-lookup"><span data-stu-id="ab9d3-149">Querying the Status of Optional Features</span></span>](querying-the-status-of-optional-features.md)                     | <span data-ttu-id="ab9d3-150">Dans Windows 7, WMI implémentait la classe [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) .</span><span class="sxs-lookup"><span data-stu-id="ab9d3-150">In Windows 7, WMI implemented the [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) class.</span></span> <span data-ttu-id="ab9d3-151">Cette classe récupère l’état des fonctionnalités facultatives présentes sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ab9d3-151">This class retrieves the status of the optional features that are present on a computer.</span></span> |
| [<span data-ttu-id="ab9d3-152">Description de l’emplacement d’un objet WMI</span><span class="sxs-lookup"><span data-stu-id="ab9d3-152">Describing the Location of a WMI Object</span></span>](describing-the-location-of-a-wmi-object.md)                       | <span data-ttu-id="ab9d3-153">Se concentre sur la syntaxe pour décrire l’emplacement d’une entité gérée par WMI.</span><span class="sxs-lookup"><span data-stu-id="ab9d3-153">Focuses on the syntax for describing the location of a WMI managed entity.</span></span>                                                                                                                     |
| [<span data-ttu-id="ab9d3-154">Accès à d’autres fonctionnalités du système d’exploitation avec WMI</span><span class="sxs-lookup"><span data-stu-id="ab9d3-154">Accessing Other Operating System Features with WMI</span></span>](accessing-other-operating-system-features-with-wmi.md) | <span data-ttu-id="ab9d3-155">Décrit comment écrire des clients WMI qui accèdent à des pilotes de périphériques, des Active Directory et des périphériques SNMP.</span><span class="sxs-lookup"><span data-stu-id="ab9d3-155">Describes how to write WMI clients that access device drivers, Active Directory, and SNMP devices.</span></span>                                                                                             |
| [<span data-ttu-id="ab9d3-156">Accès aux données dans l’espace de noms Interop</span><span class="sxs-lookup"><span data-stu-id="ab9d3-156">Accessing Data in the Interop Namespace</span></span>](accessing-data-in-the-interop-namespace.md)                       | <span data-ttu-id="ab9d3-157">Les fournisseurs d’associations permettent aux clients Windows Management Instrumentation (WMI) de traverser et de récupérer des profils et des instances de classe associées à partir d’espaces de noms différents.</span><span class="sxs-lookup"><span data-stu-id="ab9d3-157">Association providers enable Windows Management Instrumentation (WMI) clients to traverse and retrieve profiles and associated class instances from different namespaces.</span></span>                      |
| [<span data-ttu-id="ab9d3-158">Manipulation des informations relatives aux classes et aux instances</span><span class="sxs-lookup"><span data-stu-id="ab9d3-158">Manipulating Class and Instance Information</span></span>](manipulating-class-and-instance-information.md)               | <span data-ttu-id="ab9d3-159">Décrit les tâches courantes que les clients WMI doivent effectuer.</span><span class="sxs-lookup"><span data-stu-id="ab9d3-159">Describes the common tasks that WMI clients must perform.</span></span>                                                                                                                                      |
| [<span data-ttu-id="ab9d3-160">Liaison de classes</span><span class="sxs-lookup"><span data-stu-id="ab9d3-160">Linking Classes Together</span></span>](linking-classes-together.md)                                                     | <span data-ttu-id="ab9d3-161">Décrit le fournisseur d’affichage et comment il peut être utilisé pour réunir des informations à partir de plusieurs classes WMI.</span><span class="sxs-lookup"><span data-stu-id="ab9d3-161">Discusses the view provider and how it can be used to bring together information from multiple WMI classes.</span></span>                                                                                    |
| [<span data-ttu-id="ab9d3-162">Modification du Registre système</span><span class="sxs-lookup"><span data-stu-id="ab9d3-162">Modifying the System Registry</span></span>](modifying-the-system-registry.md)                                           | <span data-ttu-id="ab9d3-163">Décrit comment les clients WMI peuvent utiliser WMI pour gérer les informations du Registre système.</span><span class="sxs-lookup"><span data-stu-id="ab9d3-163">Describes how WMI clients can use WMI to manage system registry information.</span></span>                                                                                                                   |



 

