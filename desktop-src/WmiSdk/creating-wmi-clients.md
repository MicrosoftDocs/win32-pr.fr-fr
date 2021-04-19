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
# <a name="creating-wmi-clients"></a>Création de clients WMI

WMI fournit une infrastructure de gestion de système standardisée qui peut être exploitée par un certain nombre de clients différents. Ces clients vont de l’outil en ligne de commande wmic.exe à System Center Operations Manager. Vous pouvez écrire vos propres clients WMI en utilisant l’API de script WMI, l’API C++ native ou en utilisant les types de l’espace de noms de la bibliothèque de classes System. Management .NET Framework.

## <a name="how-to-create-a-wmi-client"></a>Comment créer un client WMI

Les fonctionnalités principales de WMI consistent à récupérer des objets de l’espace de stockage WMI et à examiner les propriétés de ces objets. Vous pouvez également choisir de mettre à jour ces propriétés ou d’appeler des méthodes sur ces propriétés. Les exemples suivants montrent comment effectuer une tâche d’administration WMI de base : récupération du nom de l’ordinateur local.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Terme</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Creating_a_client_with_PowerShell"></span><span id="creating_a_client_with_powershell"></span><span id="CREATING_A_CLIENT_WITH_POWERSHELL"></span>Création d’un client avec PowerShell<br/></td>
<td>WMI et PowerShell sont étroitement intégrés. par conséquent, la récupération d’objets WMI avec PowerShell consiste simplement à appeler l’applet de commande Get-WmiObject. Notez que, pour des fins de cohérence, le premier extrait de code indique explicitement la plupart des valeurs par défaut ; le deuxième suppose que les valeurs par défaut sont correctes.<br/> <span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
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
<td><p><span id="Creating_a_client_with_VBScript"></span><span id="creating_a_client_with_vbscript"></span><span id="CREATING_A_CLIENT_WITH_VBSCRIPT"></span>Création d’un client à l’aide de VBScript</p></td>
<td><p>VBScript était le langage de script d’origine qui avait été couramment utilisé avec WMI. Alors que PowerShell est devenu plus populaire, un grand nombre des exemples de code existants dans cette documentation sont écrits en VBScript. Notez que cet exemple VBScript particulier indique explicitement le chemin d’accès à l’ordinateur local, ainsi que le niveau d’emprunt d’identité. ce n’est pas obligatoire, mais il s’agit souvent d’une bonne pratique.</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
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
<td><p><span id="Creating_a_client_with_C___Microsoft.Management.Infrastructure_"></span><span id="creating_a_client_with_c___microsoft.management.infrastructure_"></span><span id="CREATING_A_CLIENT_WITH_C___MICROSOFT.MANAGEMENT.INFRASTRUCTURE_"></span>Création d’un client avec C# (<a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft. Management. infrastructure</a>)</p></td>
<td><p>Cet espace de noms contient la solution actuelle pour accéder à WMI avec du code managé, et est connu sous le nom d’infrastructure de gestion Windows (MI ou WMIv2). À l’heure actuelle, MI est la technologie prise en charge pour la création de clients de gestion gérés. Pour plus d’informations, consultez <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client">comment implémenter un client mi géré</a> et <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-native-mi-client">comment implémenter un client mi natif</a>.</p>
<div class="code">
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C#</th>
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
<td><p><span id="Creating_a_client_with_C___System.Management_"></span><span id="creating_a_client_with_c___system.management_"></span><span id="CREATING_A_CLIENT_WITH_C___SYSTEM.MANAGEMENT_"></span>Création d’un client avec C# (<a href="/dotnet/api/system.management">System. Management</a>)</p></td>
<td><p>Cet espace de noms contient la solution d’origine pour accéder à WMI avec du code managé. Alors que les classes <a href="/dotnet/api/system.management">System. Management</a> sont toujours disponibles, les classes <a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft. Management. infrastructure</a> sont généralement plus efficaces et plus évolutives. Par conséquent, il est recommandé d’utiliser les classes MI, plutôt que les classes WMI d’origine.</p>
<div class="code">
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C#</th>
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



 

Le tableau ci-dessous répertorie les rubriques traitées dans cette section.



| Rubrique                                                                                                        | Description                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md)                         | Décrit un certain nombre de problèmes qui surviennent lorsque des clients utilisent l’infrastructure WMI sur un ordinateur distant.                                                                                          |
| [Tâches WMI pour les scripts et les applications](wmi-tasks-for-scripts-and-applications.md)                         | Montre un exemple de code de client WMI.                                                                                                                                                                 |
| [Création d’une application ou d’un script WMI](creating-a-wmi-application-or-script.md)                             | Fournit des informations sur la création de différents clients WMI.                                                                                                                                       |
| [Analyse des données de performances](monitoring-performance-data.md)                                               | Décrit comment utiliser WMI pour analyser les données de performances.                                                                                                                                          |
| [Réception d’un événement WMI](receiving-a-wmi-event.md)                                                           | Décrit comment afficher les événements WMI.                                                                                                                                                              |
| [Événements d’analyse](monitoring-events.md)                                                                   | Décrit comment surveiller les événements WMI.                                                                                                                                                           |
| [Interrogation avec WQL](querying-with-wql.md)                                                                   | Présente le Langage de requêtes WMI (WQL) (WQL).                                                                                                                                                       |
| [Interrogation de l’état des fonctionnalités facultatives](querying-the-status-of-optional-features.md)                     | Dans Windows 7, WMI implémentait la classe [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) . Cette classe récupère l’état des fonctionnalités facultatives présentes sur un ordinateur. |
| [Description de l’emplacement d’un objet WMI](describing-the-location-of-a-wmi-object.md)                       | Se concentre sur la syntaxe pour décrire l’emplacement d’une entité gérée par WMI.                                                                                                                     |
| [Accès à d’autres fonctionnalités du système d’exploitation avec WMI](accessing-other-operating-system-features-with-wmi.md) | Décrit comment écrire des clients WMI qui accèdent à des pilotes de périphériques, des Active Directory et des périphériques SNMP.                                                                                             |
| [Accès aux données dans l’espace de noms Interop](accessing-data-in-the-interop-namespace.md)                       | Les fournisseurs d’associations permettent aux clients Windows Management Instrumentation (WMI) de traverser et de récupérer des profils et des instances de classe associées à partir d’espaces de noms différents.                      |
| [Manipulation des informations relatives aux classes et aux instances](manipulating-class-and-instance-information.md)               | Décrit les tâches courantes que les clients WMI doivent effectuer.                                                                                                                                      |
| [Liaison de classes](linking-classes-together.md)                                                     | Décrit le fournisseur d’affichage et comment il peut être utilisé pour réunir des informations à partir de plusieurs classes WMI.                                                                                    |
| [Modification du Registre système](modifying-the-system-registry.md)                                           | Décrit comment les clients WMI peuvent utiliser WMI pour gérer les informations du Registre système.                                                                                                                   |



 

