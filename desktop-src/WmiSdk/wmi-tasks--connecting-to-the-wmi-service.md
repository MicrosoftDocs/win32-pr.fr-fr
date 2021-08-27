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
ms.openlocfilehash: 4da816b45709f6140efb7e6e0460e27d9f9ed00f
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627715"
---
# <a name="wmi-tasks-connecting-to-the-wmi-service"></a>Tâches WMI : connexion au service WMI

Pour obtenir des données à partir de WMI, sur l’ordinateur local ou à partir d’un ordinateur distant, vous devez vous connecter au service WMI en vous connectant à un [*espace de noms*](gloss-n.md)spécifique. Dans la plupart des cas, utilisez soit la connexion sténographique [moniker](creating-a-wmi-script.md) , soit la connexion [**localisateur**](swbemlocator-connectserver.md) . Pour obtenir d’autres exemples, consultez le site TechNet ScriptCenter à l’adresse [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .

les connexions distantes nécessitent des paramètres appropriés pour le pare-feu Windows et DCOM. pour plus d’informations, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md) et [connexion via Windows pare-feu](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista). à compter de Windows Vista, le contrôle de compte d’utilisateur (UAC) peut affecter l’accès WMI. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](user-account-control-and-wmi.md).

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
<td>... se connecter à un ordinateur distant à l’aide de WMI ?</td>
<td>Spécifiez l’un des éléments suivants dans le cadre de votre chaîne de connexion <a href="constructing-a-moniker-string.md">moniker</a> :<br/>
<ul>
<li>Un nom d’ordinateur NetBIOS, tel que &quot; ATL-DC-01&quot;</li>
<li>Un nom de domaine complet, tel que &quot; ATL-DC-01.fabrikam.com&quot;</li>
<li>Une adresse IPv4, telle que &quot; 192.168.1.1&quot;</li>
<li>à partir de Windows Vista, vous pouvez spécifier une adresse ipv6 si l’ordinateur cible et l’ordinateur à partir desquels vous établissez la connexion exécutent ipv6.<br/></li>
</ul>
Pour plus d’informations, consultez <a href="connecting-to-wmi-on-a-remote-computer.md">connexion à WMI sur un ordinateur distant</a> et <a href="ipv6-and-ipv4-support-in-wmi.md">prise en charge d’IPv6 et IPv4 dans WMI</a>.<br/> <span data-codelanguage="VisualBasic"></span>
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
<col  />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
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
<td>... exécuter un script WMI sous autres informations d’identification ?</td>
<td><p>Utilisez la méthode <a href="swbemlocator-connectserver.md"><strong>SWbemLocator. ConnectServer</strong></a> , ou <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver"><strong>IWbemLocator :: ConnectServer</strong></a> en C++, et incluez le nom d’utilisateur et le mot de passe appropriés. Vous ne pouvez pas modifier les informations d’identification lors de la connexion à l’ordinateur local. Pour plus d’informations, consultez <a href="creating-a-wmi-script.md">création d’un script WMI</a> et <a href="connecting-to-wmi-on-a-remote-computer.md">connexion à WMI sur un ordinateur distant</a>.</p>
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
<col  />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
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



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Tâches WMI pour les scripts et les applications](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[Exemples d’applications WMI C++](wmi-c---application-examples.md)
</dt> <dt>

[ScriptCenter TechNet](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

 



`
