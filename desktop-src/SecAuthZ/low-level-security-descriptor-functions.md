---
description: Fonctions permettant de définir et d’extraire un descripteur de sécurité d’objets.
ms.assetid: 22bf0d6b-3ec6-4c28-ace4-49e48714f4bf
title: Fonctions du descripteur de sécurité de bas niveau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72406dc2481e4671d8d535327f416a2d003c3a89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532313"
---
# <a name="low-level-security-descriptor-functions"></a>Fonctions du descripteur de sécurité de bas niveau

Il existe plusieurs paires de fonctions de bas niveau pour la définition et la récupération du [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly)d’un objet. Chacune de ces paires fonctionne uniquement avec un ensemble limité d’objets Windows. Par exemple, une paire fonctionne avec des objets de fichier et une autre avec des clés de registre. Le tableau suivant présente les fonctions de bas niveau à utiliser avec les différents types d’objets sécurisables.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Type d'objet</th>
<th>Fonctions de bas niveau</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><a href="/windows/desktop/FileIO/file-security-and-access-rights">Fichiers</a></li>
<li><a href="/windows/desktop/FileIO/file-security-and-access-rights">Directories</a></li>
<li>Boîtes</li>
<li><a href="/windows/desktop/ipc/named-pipe-security-and-access-rights">Canaux nommés</a></li>
</ul></td>
<td>Utilisez les fonctions <a href="/windows/desktop/api/Winbase/nf-winbase-getfilesecuritya"><strong>GetFileSecurity</strong></a> et <a href="/windows/desktop/api/Winbase/nf-winbase-setfilesecuritya"><strong>SetFileSecurity</strong></a> . Ces fonctions utilisent des chaînes de caractères pour identifier l’objet sécurisable, au lieu d’utiliser des handles.</td>
</tr>
<tr class="even">
<td><ul>
<li><a href="/windows/desktop/ProcThread/process-security-and-access-rights">Processus</a></li>
<li><a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Threads</a></li>
<li><a href="access-rights-for-access-token-objects.md">Jetons d’accès</a></li>
<li><a href="/windows/desktop/Memory/file-mapping-security-and-access-rights">Objets de mappage de fichiers</a></li>
<li><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Sémaphores</a></li>
<li><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Événements</a></li>
<li><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Mutex</a></li>
<li><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Minuteries waitables</a></li>
</ul></td>
<td>Utilisez les fonctions <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity"><strong>GetKernelObjectSecurity</strong></a> et <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity"><strong>SetKernelObjectSecurity</strong></a> .</td>
</tr>
<tr class="odd">
<td><ul>
<li><a href="/windows/desktop/winstation/window-station-security-and-access-rights">Stations Windows</a></li>
<li><a href="/windows/desktop/winstation/desktop-security-and-access-rights">Bureaux</a></li>
</ul></td>
<td>Utilisez les fonctions <a href="/windows/desktop/api/Winuser/nf-winuser-getuserobjectsecurity"><strong>GetUserObjectSecurity</strong></a> et <a href="/windows/desktop/api/Winuser/nf-winuser-setuserobjectsecurity"><strong>SetUserObjectSecurity</strong></a> .</td>
</tr>
<tr class="even">
<td><ul>
<li><a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Clés de Registre</a></li>
</ul></td>
<td>Utilisez les fonctions <a href="/windows/desktop/api/Winreg/nf-winreg-reggetkeysecurity"><strong>RegGetKeySecurity</strong></a> et <a href="/windows/desktop/api/Winreg/nf-winreg-regsetkeysecurity"><strong>RegSetKeySecurity</strong></a> .</td>
</tr>
<tr class="odd">
<td><ul>
<li><a href="/windows/desktop/Services/service-security-and-access-rights">Objets de service Windows</a></li>
</ul></td>
<td>Utilisez les fonctions <a href="/windows/desktop/api/Winsvc/nf-winsvc-queryserviceobjectsecurity"><strong>QueryServiceObjectSecurity</strong></a> et <a href="/windows/desktop/api/Winsvc/nf-winsvc-setserviceobjectsecurity"><strong>SetServiceObjectSecurity</strong></a> .</td>
</tr>
<tr class="even">
<td><ul>
<li>Objets d’imprimante</li>
</ul></td>
<td>Utilisez la structure <a href="/windows/desktop/printdocs/printer-info-2"><strong>PRINTER_INFO_2</strong></a> avec les fonctions <a href="/windows/desktop/printdocs/getprinter"><strong>GetPrinter</strong></a> et <a href="/windows/desktop/printdocs/setprinter"><strong>SetPrinter</strong></a> .</td>
</tr>
<tr class="odd">
<td><ul>
<li><a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Partages réseau</a></li>
</ul></td>
<td>Utilisez le niveau 502 avec les fonctions <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo"><strong>NetShareGetInfo</strong></a> et <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo"><strong>NetShareSetInfo</strong></a> .</td>
</tr>
<tr class="even">
<td><ul>
<li><a href="acl-based-access-control.md">Objets privés (objets privés pour l’application de création)</a></li>
</ul></td>
<td>Utilisez les fonctions <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity"><strong>CreatePrivateObjectSecurity</strong></a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity"><strong>DestroyPrivateObjectSecurity</strong></a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity"><strong>GetPrivateObjectSecurity</strong></a> et <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity"><strong>SetPrivateObjectSecurity</strong></a> .</td>
</tr>
</tbody>
</table>



 

 

 
