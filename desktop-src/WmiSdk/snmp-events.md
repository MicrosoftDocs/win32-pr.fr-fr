---
description: Le fournisseur SNMP prend en charge l’écriture dans les fichiers journaux et dans le débogueur.
ms.assetid: 66627927-2eee-4d56-a74b-f86147ad7711
ms.tgt_platform: multiple
title: Événements SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8efec74902039b9e196844e9d7fadbda01cd6036
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625345"
---
# <a name="snmp-events"></a>Événements SNMP

Le fournisseur SNMP prend en charge l’écriture dans les fichiers journaux et dans le débogueur.

> [!Note]  
> Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

Un certain nombre de clés de Registre et de valeurs définissent le niveau et le type de journalisation en cours de génération :

-   Débogage

    La clé de Registre **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ WBEM \\ Provider \\ Logging** contient la valeur de journalisation qui indique si les informations peuvent être écrites dans le débogueur. La valeur de journalisation est définie sur 0 pour désactiver la sortie de débogage ou 1 pour l’activer. La journalisation est une valeur de Registre \_ DWORD.

-   Journalisation

    La clé de Registre WBEMSNMP de la clé de Registre **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ WBEM \\ \\ \\** Provider contient toutes les informations de journalisation spécifiques au fournisseur SNMP. Le tableau suivant répertorie les valeurs associées à cette clé.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Type</td>
<td><strong>REG_SZ</strong><br/> Prend l’une des valeurs suivantes :<br/> &quot;Fichier &quot; = (valeur par défaut) envoie la sortie de débogage à un fichier.<br/> &quot;Debugger &quot; = envoie la sortie de débogage au débogueur.<br/></td>
</tr>
<tr class="even">
<td>MaxFileSize</td>
<td><strong>REG_DWORD</strong><br/> Prend des valeurs entières comprises entre 1024 et 2 ^ 32-1. La valeur correspond à la taille maximale autorisée, en octets, pour le fichier journal. Si la valeur est inférieure à 1024, le mécanisme de journalisation utilise la valeur 1024. Une taille minimale de 8 Ko est recommandée pour cette valeur. Lorsque le fichier atteint la taille spécifiée par MaxFileSize, le nom de fichier est précédé d’un caractère « ~ » et un nouveau fichier est créé. Par conséquent, l’espace disque maximal requis pour la journalisation est le double de cette valeur.<br/></td>
</tr>
<tr class="odd">
<td>Fichier</td>
<td><strong>REG_SZ</strong><br/> Définit le nom du fichier dans lequel la sortie de débogage est envoyée lorsque le type de journalisation est défini sur « file ». La valeur par défaut est' <WBEMLOGS> \wbemsnmp.log. ' Si le <WBEMLOGS> Répertoire ne peut pas être déterminé à partir de la section du Registre WMI, la valeur par défaut est « c:\wbemsnmp.log ». Si un partage est utilisé, tel que \\ machine\share\wbemsnmp.log ou M:\wbemsnmp.log où M : est \\ machine\share, le compte système local sur lequel WMI s’exécute doit disposer de droits d’accès en lecture/écriture au \\ machine\share.<br/></td>
</tr>
<tr class="even">
<td>Level</td>
<td><strong>REG_DWORD</strong><br/> Prend des valeurs entières comprises entre 0 et 2 ^ 32-1. La valeur est un masque logique constitué de 32 bits. Les masques de bits suivants sont combinés pour définir le type de sortie de débogage générée :<br/>
<ul>
<li>0 : fournisseur de classes SNMP appels de méthode <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a></li>
<li>1 : implémentation du fournisseur de classes SNMP</li>
<li>2 : fournisseur d’instance SNMP appels de méthode <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a></li>
<li>3 : implémentation du fournisseur d’instance SNMP</li>
<li>4 : bibliothèque de classes SNMP</li>
<li>5 : STOCKAGE SMIR SNMP</li>
<li>6 : corrélation SNMP</li>
<li>7 : code de mappage de type SNMP</li>
<li>8 : code de thread SNMP</li>
<li>9 : interfaces et implémentations du fournisseur d’événements SNMP</li>
</ul>
Définissez niveau sur (2 ^ 0 + 2 ^ 8 =) 257 pour les opérations impliquant des appels aux méthodes <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> du fournisseur de classes SNMP, et des opérations utilisant le code de thread SNMP.<br/></td>
</tr>
</tbody>
</table>



 

 

 




