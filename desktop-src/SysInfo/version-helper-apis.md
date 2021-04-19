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
# <a name="version-helper-functions"></a>Fonctions d’assistance de version

Les fonctions suivantes peuvent être utilisées pour déterminer la version actuelle du système d’exploitation ou pour déterminer s’il s’agit d’une version Windows ou Windows Server. Ces fonctions fournissent des tests simples qui utilisent la fonction [VerifyVersionInfo](/windows/win32/api/Winbase/nf-winbase-verifyversioninfoa) et les comparaisons plus ou moins recommandées qui sont prouvées comme un moyen fiable de déterminer la version du système d’exploitation.

> [!Note]  
> Ces API sont définies par **versionhelpers. h**, qui est inclus dans le kit de développement logiciel (SDK) Windows 8.1. Ce fichier peut être utilisé avec d’autres versions de Microsoft Visual Studio pour implémenter les mêmes fonctionnalités pour les versions de Windows antérieures à Windows 8.1.

<table>
<thead>
<tr class="header">
<th>Fonction</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxporgreater"><strong>IsWindowsXPOrGreater</strong></a></td>
<td>Indique si la version actuelle du système d’exploitation correspond à la version de Windows XP, ou est supérieure à celle-ci.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp1orgreater"><strong>IsWindowsXPSP1OrGreater</strong></a></td>
<td>Indique si la version actuelle du système d’exploitation correspond à la version de Windows XP avec Service Pack 1 (SP1), ou est supérieure à celle-ci.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp2orgreater"><strong>IsWindowsXPSP2OrGreater</strong></a></td>
<td>Indique si la version actuelle du système d’exploitation correspond à la version de Windows XP avec Service Pack 2 (SP2), ou est supérieure à celle-ci.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp3orgreater"><strong>IsWindowsXPSP3OrGreater</strong></a></td>
<td>Indique si la version actuelle du système d’exploitation correspond à la version de Windows XP avec Service Pack 3 (SP3), ou est supérieure à celle-ci.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistaorgreater"><strong>IsWindowsVistaOrGreater</strong></a></td>
<td>Indique si la version actuelle du système d’exploitation correspond à la version de Windows Vista ou est supérieure à celle-ci.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp1orgreater"><strong>IsWindowsVistaSP1OrGreater</strong></a></td>
<td>Indique si la version actuelle du système d’exploitation correspond à la version de Windows Vista avec Service Pack 1 (SP1), ou est supérieure à celle-ci.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp2orgreater"><strong>IsWindowsVistaSP2OrGreater</strong></a></td>
<td>Indique si la version actuelle du système d’exploitation correspond à la version de Windows Vista avec Service Pack 2 (SP2) ou est supérieure à celle-ci.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7orgreater"><strong>IsWindows7OrGreater</strong></a></td>
<td>Indique si la version actuelle du système d’exploitation correspond à la version de Windows 7, ou est supérieure à celle-ci.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7sp1orgreater"><strong>IsWindows7SP1OrGreater</strong></a></td>
<td>Indique si la version actuelle du système d’exploitation correspond à la version de Windows 7 avec Service Pack 1 (SP1), ou est supérieure à celle-ci.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8orgreater"><strong>IsWindows8OrGreater</strong></a></td>
<td>Indique si la version actuelle du système d’exploitation correspond à la version Windows 8, ou est supérieure à celle-ci.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a></td>
<td>Indique si la version actuelle du système d’exploitation correspond à la version de Windows 8.1, ou est supérieure à celle-ci.<br/> Pour Windows 10, <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a> retourne la valeur false, sauf si l’application contient un manifeste qui inclut une section de compatibilité qui contient les GUID qui désignent Windows 8.1 et/ou Windows 10.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a></td>
<td>Indique si la version actuelle du système d’exploitation correspond à la version Windows 10, ou est supérieure à celle-ci.<br/> Pour Windows 10, <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a> retourne la valeur false, sauf si l’application contient un manifeste qui inclut une section de compatibilité qui contient le GUID qui désigne Windows 10.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsserver"><strong>IsWindowsServer</strong></a></td>
<td>Indique si le système d’exploitation actuel est une version de Windows Server. Les applications qui doivent faire la distinction entre les versions client et serveur de Windows doivent appeler cette fonction.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsversionorgreater"><strong>IsWindowsVersionOrGreater</strong></a></td>
<td>
<blockquote>Vous ne devez utiliser cette fonction que si les autres fonctions d’assistance de version fournies ne correspondent pas à votre scénario.</blockquote>
<br/>Indique si la version actuelle du système d’exploitation correspond à, ou est supérieur à, aux informations de version fournies. Cette fonction est utile pour confirmer une version de Windows Server qui ne partage pas de numéro de version avec une version client.
</td>
</tr>
</tbody>
</table>

## <a name="example"></a>Exemple

Les fonctions inline définies dans le fichier d’en-tête **VersionHelpers. h** vous permettent de vérifier la version du système d’exploitation en retournant une valeur **booléenne** lors du test d’une version de Windows.

Par exemple, si votre application nécessite Windows 8 ou version ultérieure, utilisez le test suivant.

```C++
#include <VersionHelpers.h>
 
if (!IsWindows8OrGreater())
{
   MessageBox(NULL, "You need at least Windows 8", "Version Not Supported", MB_OK);
}
```

## <a name="related-topics"></a>Rubriques connexes

- [OSVERSIONINFOEX](/windows/desktop/api/Winnt/ns-winnt-osversioninfoexa)
