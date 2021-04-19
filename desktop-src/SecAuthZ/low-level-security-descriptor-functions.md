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
# <a name="low-level-security-descriptor-functions"></a><span data-ttu-id="db7e0-103">Fonctions du descripteur de sécurité de bas niveau</span><span class="sxs-lookup"><span data-stu-id="db7e0-103">Low-level Security Descriptor Functions</span></span>

<span data-ttu-id="db7e0-104">Il existe plusieurs paires de fonctions de bas niveau pour la définition et la récupération du [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly)d’un objet.</span><span class="sxs-lookup"><span data-stu-id="db7e0-104">There are several pairs of low-level functions for setting and retrieving an object's [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="db7e0-105">Chacune de ces paires fonctionne uniquement avec un ensemble limité d’objets Windows.</span><span class="sxs-lookup"><span data-stu-id="db7e0-105">Each of these pairs works only with a limited set of Windows objects.</span></span> <span data-ttu-id="db7e0-106">Par exemple, une paire fonctionne avec des objets de fichier et une autre avec des clés de registre.</span><span class="sxs-lookup"><span data-stu-id="db7e0-106">For example, one pair works with file objects and another works with registry keys.</span></span> <span data-ttu-id="db7e0-107">Le tableau suivant présente les fonctions de bas niveau à utiliser avec les différents types d’objets sécurisables.</span><span class="sxs-lookup"><span data-stu-id="db7e0-107">The following table shows the low-level functions to use with the different types of securable objects.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db7e0-108">Type d'objet</span><span class="sxs-lookup"><span data-stu-id="db7e0-108">Object type</span></span></th>
<th><span data-ttu-id="db7e0-109">Fonctions de bas niveau</span><span class="sxs-lookup"><span data-stu-id="db7e0-109">Low-level functions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="db7e0-110"><a href="/windows/desktop/FileIO/file-security-and-access-rights">Fichiers</a></span><span class="sxs-lookup"><span data-stu-id="db7e0-110"><a href="/windows/desktop/FileIO/file-security-and-access-rights">Files</a></span></span></li>
<li><span data-ttu-id="db7e0-111"><a href="/windows/desktop/FileIO/file-security-and-access-rights">Directories</a></span><span class="sxs-lookup"><span data-stu-id="db7e0-111"><a href="/windows/desktop/FileIO/file-security-and-access-rights">Directories</a></span></span></li>
<li><span data-ttu-id="db7e0-112">Boîtes</span><span class="sxs-lookup"><span data-stu-id="db7e0-112">Mailslots</span></span></li>
<li><span data-ttu-id="db7e0-113"><a href="/windows/desktop/ipc/named-pipe-security-and-access-rights">Canaux nommés</a></span><span class="sxs-lookup"><span data-stu-id="db7e0-113"><a href="/windows/desktop/ipc/named-pipe-security-and-access-rights">Named pipes</a></span></span></li>
</ul></td>
<td><span data-ttu-id="db7e0-114">Utilisez les fonctions <a href="/windows/desktop/api/Winbase/nf-winbase-getfilesecuritya"><strong>GetFileSecurity</strong></a> et <a href="/windows/desktop/api/Winbase/nf-winbase-setfilesecuritya"><strong>SetFileSecurity</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="db7e0-114">Use the <a href="/windows/desktop/api/Winbase/nf-winbase-getfilesecuritya"><strong>GetFileSecurity</strong></a> and <a href="/windows/desktop/api/Winbase/nf-winbase-setfilesecuritya"><strong>SetFileSecurity</strong></a> functions.</span></span> <span data-ttu-id="db7e0-115">Ces fonctions utilisent des chaînes de caractères pour identifier l’objet sécurisable, au lieu d’utiliser des handles.</span><span class="sxs-lookup"><span data-stu-id="db7e0-115">These functions use character strings to identify the securable object, instead of using handles.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="db7e0-116"><a href="/windows/desktop/ProcThread/process-security-and-access-rights">Processus</a></span><span class="sxs-lookup"><span data-stu-id="db7e0-116"><a href="/windows/desktop/ProcThread/process-security-and-access-rights">Processes</a></span></span></li>
<li><span data-ttu-id="db7e0-117"><a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Threads</a></span><span class="sxs-lookup"><span data-stu-id="db7e0-117"><a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Threads</a></span></span></li>
<li><span data-ttu-id="db7e0-118"><a href="access-rights-for-access-token-objects.md">Jetons d’accès</a></span><span class="sxs-lookup"><span data-stu-id="db7e0-118"><a href="access-rights-for-access-token-objects.md">Access tokens</a></span></span></li>
<li><span data-ttu-id="db7e0-119"><a href="/windows/desktop/Memory/file-mapping-security-and-access-rights">Objets de mappage de fichiers</a></span><span class="sxs-lookup"><span data-stu-id="db7e0-119"><a href="/windows/desktop/Memory/file-mapping-security-and-access-rights">File-mapping objects</a></span></span></li>
<li><span data-ttu-id="db7e0-120"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Sémaphores</a></span><span class="sxs-lookup"><span data-stu-id="db7e0-120"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Semaphores</a></span></span></li>
<li><span data-ttu-id="db7e0-121"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Événements</a></span><span class="sxs-lookup"><span data-stu-id="db7e0-121"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Events</a></span></span></li>
<li><span data-ttu-id="db7e0-122"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Mutex</a></span><span class="sxs-lookup"><span data-stu-id="db7e0-122"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Mutexes</a></span></span></li>
<li><span data-ttu-id="db7e0-123"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Minuteries waitables</a></span><span class="sxs-lookup"><span data-stu-id="db7e0-123"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Waitable timers</a></span></span></li>
</ul></td>
<td><span data-ttu-id="db7e0-124">Utilisez les fonctions <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity"><strong>GetKernelObjectSecurity</strong></a> et <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity"><strong>SetKernelObjectSecurity</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="db7e0-124">Use the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity"><strong>GetKernelObjectSecurity</strong></a> and <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity"><strong>SetKernelObjectSecurity</strong></a> functions.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="db7e0-125"><a href="/windows/desktop/winstation/window-station-security-and-access-rights">Stations Windows</a></span><span class="sxs-lookup"><span data-stu-id="db7e0-125"><a href="/windows/desktop/winstation/window-station-security-and-access-rights">Window stations</a></span></span></li>
<li><span data-ttu-id="db7e0-126"><a href="/windows/desktop/winstation/desktop-security-and-access-rights">Bureaux</a></span><span class="sxs-lookup"><span data-stu-id="db7e0-126"><a href="/windows/desktop/winstation/desktop-security-and-access-rights">Desktops</a></span></span></li>
</ul></td>
<td><span data-ttu-id="db7e0-127">Utilisez les fonctions <a href="/windows/desktop/api/Winuser/nf-winuser-getuserobjectsecurity"><strong>GetUserObjectSecurity</strong></a> et <a href="/windows/desktop/api/Winuser/nf-winuser-setuserobjectsecurity"><strong>SetUserObjectSecurity</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="db7e0-127">Use the <a href="/windows/desktop/api/Winuser/nf-winuser-getuserobjectsecurity"><strong>GetUserObjectSecurity</strong></a> and <a href="/windows/desktop/api/Winuser/nf-winuser-setuserobjectsecurity"><strong>SetUserObjectSecurity</strong></a> functions.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="db7e0-128"><a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Clés de Registre</a></span><span class="sxs-lookup"><span data-stu-id="db7e0-128"><a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry keys</a></span></span></li>
</ul></td>
<td><span data-ttu-id="db7e0-129">Utilisez les fonctions <a href="/windows/desktop/api/Winreg/nf-winreg-reggetkeysecurity"><strong>RegGetKeySecurity</strong></a> et <a href="/windows/desktop/api/Winreg/nf-winreg-regsetkeysecurity"><strong>RegSetKeySecurity</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="db7e0-129">Use the <a href="/windows/desktop/api/Winreg/nf-winreg-reggetkeysecurity"><strong>RegGetKeySecurity</strong></a> and <a href="/windows/desktop/api/Winreg/nf-winreg-regsetkeysecurity"><strong>RegSetKeySecurity</strong></a> functions.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="db7e0-130"><a href="/windows/desktop/Services/service-security-and-access-rights">Objets de service Windows</a></span><span class="sxs-lookup"><span data-stu-id="db7e0-130"><a href="/windows/desktop/Services/service-security-and-access-rights">Windows service objects</a></span></span></li>
</ul></td>
<td><span data-ttu-id="db7e0-131">Utilisez les fonctions <a href="/windows/desktop/api/Winsvc/nf-winsvc-queryserviceobjectsecurity"><strong>QueryServiceObjectSecurity</strong></a> et <a href="/windows/desktop/api/Winsvc/nf-winsvc-setserviceobjectsecurity"><strong>SetServiceObjectSecurity</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="db7e0-131">Use the <a href="/windows/desktop/api/Winsvc/nf-winsvc-queryserviceobjectsecurity"><strong>QueryServiceObjectSecurity</strong></a> and <a href="/windows/desktop/api/Winsvc/nf-winsvc-setserviceobjectsecurity"><strong>SetServiceObjectSecurity</strong></a> functions.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="db7e0-132">Objets d’imprimante</span><span class="sxs-lookup"><span data-stu-id="db7e0-132">Printer objects</span></span></li>
</ul></td>
<td><span data-ttu-id="db7e0-133">Utilisez la structure <a href="/windows/desktop/printdocs/printer-info-2"><strong>PRINTER_INFO_2</strong></a> avec les fonctions <a href="/windows/desktop/printdocs/getprinter"><strong>GetPrinter</strong></a> et <a href="/windows/desktop/printdocs/setprinter"><strong>SetPrinter</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="db7e0-133">Use the <a href="/windows/desktop/printdocs/printer-info-2"><strong>PRINTER_INFO_2</strong></a> structure with the <a href="/windows/desktop/printdocs/getprinter"><strong>GetPrinter</strong></a> and <a href="/windows/desktop/printdocs/setprinter"><strong>SetPrinter</strong></a> functions.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="db7e0-134"><a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Partages réseau</a></span><span class="sxs-lookup"><span data-stu-id="db7e0-134"><a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Network shares</a></span></span></li>
</ul></td>
<td><span data-ttu-id="db7e0-135">Utilisez le niveau 502 avec les fonctions <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo"><strong>NetShareGetInfo</strong></a> et <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo"><strong>NetShareSetInfo</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="db7e0-135">Use level 502 with the <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo"><strong>NetShareGetInfo</strong></a> and <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo"><strong>NetShareSetInfo</strong></a> functions.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="db7e0-136"><a href="acl-based-access-control.md">Objets privés (objets privés pour l’application de création)</a></span><span class="sxs-lookup"><span data-stu-id="db7e0-136"><a href="acl-based-access-control.md">Private objects (objects private to the creating application)</a></span></span></li>
</ul></td>
<td><span data-ttu-id="db7e0-137">Utilisez les fonctions <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity"><strong>CreatePrivateObjectSecurity</strong></a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity"><strong>DestroyPrivateObjectSecurity</strong></a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity"><strong>GetPrivateObjectSecurity</strong></a> et <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity"><strong>SetPrivateObjectSecurity</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="db7e0-137">Use the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity"><strong>CreatePrivateObjectSecurity</strong></a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity"><strong>DestroyPrivateObjectSecurity</strong></a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity"><strong>GetPrivateObjectSecurity</strong></a> and <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity"><strong>SetPrivateObjectSecurity</strong></a> functions.</span></span></td>
</tr>
</tbody>
</table>



 

 

 
