---
description: D’un point de vue conceptuel similaire à un Uniform Resource Locator (URL), un chemin d’accès d’objet WMI est une chaîne qui identifie de façon unique l’espace de noms sur un serveur, une classe dans un espace de noms ou des instances d’une classe.
ms.assetid: 7a390541-609d-4b97-b91c-1a41d21ec17d
ms.tgt_platform: multiple
title: Description de l’emplacement d’un objet WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b58b58a6b668955d6eba1e4c51f6f8dccdac890
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521507"
---
# <a name="describing-the-location-of-a-wmi-object"></a>Description de l’emplacement d’un objet WMI

D’un point de vue conceptuel similaire à un Uniform Resource Locator (URL), un chemin d’accès d’objet WMI est une chaîne qui identifie de façon unique l’espace de noms sur un serveur, une classe dans un espace de noms ou des instances d’une classe. Un chemin d’accès d’objet est hiérarchique et contient plusieurs éléments qui décrivent l’emplacement de l’objet en question. Comme les chemins d’accès aux fichiers, les chemins d’accès d’objet WMI peuvent être décrits dans l’intégralité ou spécifiés en tant que chemin d’accès relatif.

L’espace de noms d’un objet WMI est indiqué sur la page de référence WMI. Par exemple, l’emplacement de la plupart des classes prises en charge par les [fournisseurs WMI cimwin32](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers) se trouvent dans l' \\ espace de \\ noms CIMV2 racine. Le code PowerShell suivant décrit un appel pour récupérer l' [**objet \_ ComputerSystem Win32**](/windows/desktop/CIMWin32Prov/win32-computersystem) sur votre ordinateur local :

`Get-WmiObject -Class Win32_ComputerSystem -Namespace "root\cimv2" -ComputerName "."`

Une instance spécifique du [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) peut également avoir le chemin d’accès suivant à partir de la propriété [**SWbemObject. Path \_**](swbemobject-path-.md) .

`\\Machine1\root\cimv2:Win32_LogicalDisk.DeviceID="C:"`

L’exemple suivant montre le chemin d’accès relatif à cette instance, comme indiqué par l’affichage de la propriété [**RelPath**](swbemobjectpath-relpath.md) de l’objet [**SWbemObjectPath**](swbemobjectpath.md) retourné par l’appel à [**SWbemObject. \_ path**](swbemobject-path-.md).

`Win32_LogicalDisk.DeviceID="A:"`

Notez que **DeviceID** est la propriété de clé de la classe [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .

## <a name="c"></a>C++

Le tableau suivant répertorie les types de chemin d’accès d’objet et les méthodes associées qui requièrent des chemins d’accès aux objets.



<table>
<thead>
<tr class="header">
<th>Type de chemin d’accès de l’objet</th>
<th>Méthode</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="describing-a-wmi-namespace-object-path.md">Espace de noms</a></td>
<td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-opennamespace"><strong>IWbemServices :: OpenNamespace,</strong></a><br />
</dl></td>
</tr>
<tr class="even">
<td><a href="describing-a-class-object-path.md">Classe</a></td>
<td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod"><strong>IWbemServices :: ExecMethod</strong></a><br />
[<strong>IWbemServices :: ExecMethodAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="describing-a-class-object-path.md">Classe</a> ou <a href="describing-an-instance-object-path.md">instance</a></td>
<td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject"><strong>IWbemServices :: GetObject</strong></a><br />
[<strong>IWbemServices :: GetObjectAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="describing-an-instance-object-path.md">Instance</a></td>
<td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance"><strong>IWbemServices ::D eleteInstance</strong></a><br />
[<strong>IWbemServices ::D eleteinstanceasync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="script"></a>Script

Les chemins d’accès aux objets peuvent être créés de plusieurs façons :

-   Récupérez la propriété d’une méthode qui retourne un objet [**SWbemObjectPath**](swbemobjectpath.md) .
-   Récupérez la propriété [**SWbemObject \_ . Path**](swbemobject-path-.md) .
-   Créez une variable de chaîne qui contient le chemin d’accès de l’objet.

Le tableau suivant répertorie les objets de script qui requièrent des chemins d’accès aux objets.



<table>
<thead>
<tr class="header">
<th>Objet de script</th>
<th>Méthode</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="swbemservices.md"><strong>M</strong></a></td>
<td><dl><a href="swbemservices-associatorsof.md"><strong>AssociatorsOf</strong></a><br />
[<strong>AssociatorsOfAsync</strong>] (swbemservices-associatorsofasync.md)<br />
[<strong>Supprimer</strong>] (swbemservices-delete.md)<br />
[<strong>DeleteAsync</strong>] (swbemservices-deleteasync.md)<br />
[<strong>ExecMethod</strong>] (swbemservices-execmethod.md)<br />
[<strong>ExecMethodAsync</strong>] (swbemservices-execmethodasync.md)<br />
[<strong>Obtient</strong>] (swbemservices-get.md)<br />
[<strong>GetAsync</strong>] (swbemservices-getasync.md)<br />
[<strong>ReferencesTo</strong>] (swbemservices-referencesto.md)<br />
[<strong>ReferencesToAsync</strong>] (swbemservices-referencestoasync.md)<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="swbemobjectset.md"><strong>SWbemObjectSet</strong></a></td>
<td><dl><a href="swbemobjectset-item.md"><strong>Élément</strong></a><br />
</dl></td>
</tr>
</tbody>
</table>



 

 

 
