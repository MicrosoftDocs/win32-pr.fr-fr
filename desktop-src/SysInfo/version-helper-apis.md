---
description: Les fonctions suivantes peuvent être utilisées pour déterminer la version actuelle du système d’exploitation ou pour déterminer s’il s’agit d’une version Windows ou Windows Server.
ms.assetid: 2FAF67CD-CEEA-4096-B482-F5E2DF8D6C34
title: Fonctions d’assistance de version
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 746e6488d949fe6512355d7ef9910c26aaf3b54b
ms.sourcegitcommit: 49df0f62429d21bca96d8704205048267ee0eb59
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "106543982"
---
# <a name="version-helper-functions"></a><span data-ttu-id="ed56c-103">Fonctions d’assistance de version</span><span class="sxs-lookup"><span data-stu-id="ed56c-103">Version Helper functions</span></span>

<span data-ttu-id="ed56c-104">Les fonctions suivantes peuvent être utilisées pour déterminer la version actuelle du système d’exploitation ou pour déterminer s’il s’agit d’une version Windows ou Windows Server.</span><span class="sxs-lookup"><span data-stu-id="ed56c-104">The following functions can be used to determine the current operating system version or identify whether it is a Windows or Windows Server release.</span></span> <span data-ttu-id="ed56c-105">Ces fonctions fournissent des tests simples qui utilisent la fonction [VerifyVersionInfo](/windows/win32/api/Winbase/nf-winbase-verifyversioninfoa) et les comparaisons plus ou moins recommandées qui sont prouvées comme un moyen fiable de déterminer la version du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="ed56c-105">These functions provide simple tests that use the [VerifyVersionInfo](/windows/win32/api/Winbase/nf-winbase-verifyversioninfoa) function and the recommended greater than or equal to comparisons that are proven as a robust means to determine the operating system version.</span></span>

> [!Note]  
> <span data-ttu-id="ed56c-106">Ces API sont définies par **versionhelpers. h**, qui est inclus dans le kit de développement logiciel (SDK) Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="ed56c-106">These APIs are defined by **versionhelpers.h**, which is included in the Windows 8.1 software development kit (SDK).</span></span> <span data-ttu-id="ed56c-107">Ce fichier peut être utilisé avec d’autres versions de Microsoft Visual Studio pour implémenter les mêmes fonctionnalités pour les versions de Windows antérieures à Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="ed56c-107">This file can be used with other Microsoft Visual Studio releases to implement the same functionality for Windows versions prior to Windows 8.1.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ed56c-108">Fonction</span><span class="sxs-lookup"><span data-stu-id="ed56c-108">Function</span></span></th>
<th><span data-ttu-id="ed56c-109">Description</span><span class="sxs-lookup"><span data-stu-id="ed56c-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ed56c-110"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxporgreater"><strong>IsWindowsXPOrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="ed56c-110"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxporgreater"><strong>IsWindowsXPOrGreater</strong></a></span></span></td>
<td><span data-ttu-id="ed56c-111">Indique si la version actuelle du système d’exploitation correspond à la version de Windows XP, ou est supérieure à celle-ci.</span><span class="sxs-lookup"><span data-stu-id="ed56c-111">Indicates if the current OS version matches, or is greater than, the Windows XP version.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ed56c-112"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp1orgreater"><strong>IsWindowsXPSP1OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="ed56c-112"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp1orgreater"><strong>IsWindowsXPSP1OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="ed56c-113">Indique si la version actuelle du système d’exploitation correspond à la version de Windows XP avec Service Pack 1 (SP1), ou est supérieure à celle-ci.</span><span class="sxs-lookup"><span data-stu-id="ed56c-113">Indicates if the current OS version matches, or is greater than, the Windows XP with Service Pack 1 (SP1) version.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ed56c-114"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp2orgreater"><strong>IsWindowsXPSP2OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="ed56c-114"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp2orgreater"><strong>IsWindowsXPSP2OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="ed56c-115">Indique si la version actuelle du système d’exploitation correspond à la version de Windows XP avec Service Pack 2 (SP2), ou est supérieure à celle-ci.</span><span class="sxs-lookup"><span data-stu-id="ed56c-115">Indicates if the current OS version matches, or is greater than, the Windows XP with Service Pack 2 (SP2) version.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ed56c-116"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp3orgreater"><strong>IsWindowsXPSP3OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="ed56c-116"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp3orgreater"><strong>IsWindowsXPSP3OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="ed56c-117">Indique si la version actuelle du système d’exploitation correspond à la version de Windows XP avec Service Pack 3 (SP3), ou est supérieure à celle-ci.</span><span class="sxs-lookup"><span data-stu-id="ed56c-117">Indicates if the current OS version matches, or is greater than, the Windows XP with Service Pack 3 (SP3) version.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ed56c-118"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistaorgreater"><strong>IsWindowsVistaOrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="ed56c-118"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistaorgreater"><strong>IsWindowsVistaOrGreater</strong></a></span></span></td>
<td><span data-ttu-id="ed56c-119">Indique si la version actuelle du système d’exploitation correspond à la version de Windows Vista ou est supérieure à celle-ci.</span><span class="sxs-lookup"><span data-stu-id="ed56c-119">Indicates if the current OS version matches, or is greater than, the Windows Vista version.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ed56c-120"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp1orgreater"><strong>IsWindowsVistaSP1OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="ed56c-120"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp1orgreater"><strong>IsWindowsVistaSP1OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="ed56c-121">Indique si la version actuelle du système d’exploitation correspond à la version de Windows Vista avec Service Pack 1 (SP1), ou est supérieure à celle-ci.</span><span class="sxs-lookup"><span data-stu-id="ed56c-121">Indicates if the current OS version matches, or is greater than, the Windows Vista with Service Pack 1 (SP1) version.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ed56c-122"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp2orgreater"><strong>IsWindowsVistaSP2OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="ed56c-122"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp2orgreater"><strong>IsWindowsVistaSP2OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="ed56c-123">Indique si la version actuelle du système d’exploitation correspond à la version de Windows Vista avec Service Pack 2 (SP2) ou est supérieure à celle-ci.</span><span class="sxs-lookup"><span data-stu-id="ed56c-123">Indicates if the current OS version matches, or is greater than, the Windows Vista with Service Pack 2 (SP2) version.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ed56c-124"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7orgreater"><strong>IsWindows7OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="ed56c-124"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7orgreater"><strong>IsWindows7OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="ed56c-125">Indique si la version actuelle du système d’exploitation correspond à la version de Windows 7, ou est supérieure à celle-ci.</span><span class="sxs-lookup"><span data-stu-id="ed56c-125">Indicates if the current OS version matches, or is greater than, the Windows 7 version.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ed56c-126"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7sp1orgreater"><strong>IsWindows7SP1OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="ed56c-126"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7sp1orgreater"><strong>IsWindows7SP1OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="ed56c-127">Indique si la version actuelle du système d’exploitation correspond à la version de Windows 7 avec Service Pack 1 (SP1), ou est supérieure à celle-ci.</span><span class="sxs-lookup"><span data-stu-id="ed56c-127">Indicates if the current OS version matches, or is greater than, the Windows 7 with Service Pack 1 (SP1) version.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ed56c-128"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8orgreater"><strong>IsWindows8OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="ed56c-128"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8orgreater"><strong>IsWindows8OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="ed56c-129">Indique si la version actuelle du système d’exploitation correspond à la version Windows 8, ou est supérieure à celle-ci.</span><span class="sxs-lookup"><span data-stu-id="ed56c-129">Indicates if the current OS version matches, or is greater than, the Windows 8 version.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ed56c-130"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="ed56c-130"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="ed56c-131">Indique si la version actuelle du système d’exploitation correspond à la version de Windows 8.1, ou est supérieure à celle-ci.</span><span class="sxs-lookup"><span data-stu-id="ed56c-131">Indicates if the current OS version matches, or is greater than, the Windows 8.1 version.</span></span><br/> <span data-ttu-id="ed56c-132">Pour Windows 10, <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a> retourne la valeur false, sauf si l’application contient un manifeste qui inclut une section de compatibilité qui contient les GUID qui désignent Windows 8.1 et/ou Windows 10.</span><span class="sxs-lookup"><span data-stu-id="ed56c-132">For Windows 10, <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a> returns false unless the application contains a manifest that includes a compatibility section that contains the GUIDs that designate Windows 8.1 and/or Windows 10.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ed56c-133"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="ed56c-133"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="ed56c-134">Indique si la version actuelle du système d’exploitation correspond à la version Windows 10, ou est supérieure à celle-ci.</span><span class="sxs-lookup"><span data-stu-id="ed56c-134">Indicates if the current OS version matches, or is greater than, the Windows 10 version.</span></span><br/> <span data-ttu-id="ed56c-135">Pour Windows 10, <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a> retourne la valeur false, sauf si l’application contient un manifeste qui inclut une section de compatibilité qui contient le GUID qui désigne Windows 10.</span><span class="sxs-lookup"><span data-stu-id="ed56c-135">For Windows 10, <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a> returns false unless the application contains a manifest that includes a compatibility section that contains the GUID that designates Windows 10.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ed56c-136"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsserver"><strong>IsWindowsServer</strong></a></span><span class="sxs-lookup"><span data-stu-id="ed56c-136"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsserver"><strong>IsWindowsServer</strong></a></span></span></td>
<td><span data-ttu-id="ed56c-137">Indique si le système d’exploitation actuel est une version de Windows Server.</span><span class="sxs-lookup"><span data-stu-id="ed56c-137">Indicates if the current OS is a Windows Server release.</span></span> <span data-ttu-id="ed56c-138">Les applications qui doivent faire la distinction entre les versions client et serveur de Windows doivent appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="ed56c-138">Applications that need to distinguish between server and client versions of Windows should call this function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ed56c-139"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsversionorgreater"><strong>IsWindowsVersionOrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="ed56c-139"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsversionorgreater"><strong>IsWindowsVersionOrGreater</strong></a></span></span></td>
<td>
<blockquote><span data-ttu-id="ed56c-140">Vous ne devez utiliser cette fonction que si les autres fonctions d’assistance de version fournies ne correspondent pas à votre scénario.</span><span class="sxs-lookup"><span data-stu-id="ed56c-140">You should only use this function if the other provided version helper functions do not fit your scenario.</span></span></blockquote>
<br/><span data-ttu-id="ed56c-141">Indique si la version actuelle du système d’exploitation correspond à, ou est supérieur à, aux informations de version fournies.</span><span class="sxs-lookup"><span data-stu-id="ed56c-141">Indicates if the current OS version matches, or is greater than, the provided version information.</span></span> <span data-ttu-id="ed56c-142">Cette fonction est utile pour confirmer une version de Windows Server qui ne partage pas de numéro de version avec une version client.</span><span class="sxs-lookup"><span data-stu-id="ed56c-142">This function is useful in confirming a version of Windows Server that doesn't share a version number with a client release.</span></span>
</td>
</tr>
</tbody>
</table>

## <a name="example"></a><span data-ttu-id="ed56c-143">Exemple</span><span class="sxs-lookup"><span data-stu-id="ed56c-143">Example</span></span>

<span data-ttu-id="ed56c-144">Les fonctions inline définies dans le fichier d’en-tête **VersionHelpers. h** vous permettent de vérifier la version du système d’exploitation en retournant une valeur **booléenne** lors du test d’une version de Windows.</span><span class="sxs-lookup"><span data-stu-id="ed56c-144">The inline functions defined in the **VersionHelpers.h** header file let you verify the operating system version by returning a **Boolean** value when testing for a version of Windows.</span></span>

<span data-ttu-id="ed56c-145">Par exemple, si votre application nécessite Windows 8 ou version ultérieure, utilisez le test suivant.</span><span class="sxs-lookup"><span data-stu-id="ed56c-145">For example, if your application requires Windows 8 or later, use the following test.</span></span>

```C++
#include <VersionHelpers.h>
 
if (!IsWindows8OrGreater())
{
   MessageBox(NULL, "You need at least Windows 8", "Version Not Supported", MB_OK);
}
```

## <a name="related-topics"></a><span data-ttu-id="ed56c-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ed56c-146">Related topics</span></span>

- [<span data-ttu-id="ed56c-147">OSVERSIONINFOEX</span><span class="sxs-lookup"><span data-stu-id="ed56c-147">OSVERSIONINFOEX</span></span>](/windows/desktop/api/Winnt/ns-winnt-osversioninfoexa)
