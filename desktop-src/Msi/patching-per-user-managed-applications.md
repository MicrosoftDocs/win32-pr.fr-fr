---
description: à partir de Windows Installer 3,0, il est possible d’appliquer des correctifs à une application qui a été installée dans un contexte géré par l’utilisateur une fois que le correctif a été inscrit comme ayant des privilèges élevés.
ms.assetid: ebe5f447-9b74-48dc-8192-f2ac90dca490
title: Mise à jour corrective des applications gérées par utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 516af282dc7f149b86d03192303dc1b3da14416d1a6a22a4f3e716f641777500
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979369"
---
# <a name="patching-per-user-managed-applications"></a>Mise à jour corrective des applications gérées par utilisateur

à partir de Windows Installer 3,0, il est possible d’appliquer des correctifs à une application qui a été installée dans un contexte géré par l’utilisateur une fois que le correctif a été inscrit comme ayant des privilèges élevés.

**Windows Installer 2,0 :** Non pris en charge. vous ne pouvez pas appliquer de correctifs aux applications installées dans un contexte géré par utilisateur à l’aide des versions de Windows Installer antérieures à Windows Installer 3,0.

Une application est installée dans l’état géré par l’utilisateur dans les cas suivants.

-   L’installation par utilisateur de l’application a été effectuée à l’aide du déploiement et [stratégie de groupe](/previous-versions/windows/desktop/Policy/group-policy-start-page).
-   L’application a été publiée sur un utilisateur spécifié et installée par la méthode décrite dans [publication d’une application Per-User à installer avec des privilèges élevés](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md).

Des privilèges sont requis pour installer une application dans le contexte géré par l’utilisateur ; par conséquent, les réinstallations de Windows Installer ultérieures ou les réparations de l’application sont également effectuées par le programme d’installation à l’aide de privilèges élevés. Cela signifie que seuls les correctifs de sources approuvées peuvent être appliqués à l’application.

à partir de Windows Installer 3,0, vous pouvez appliquer un correctif à une application gérée par utilisateur une fois que le correctif a été inscrit comme ayant des privilèges élevés. Pour inscrire un correctif comme ayant des privilèges élevés, utilisez la fonction [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) ou la méthode [**SourceListAddSource**](patch-sourcelistaddsource.md) de l’objet [**patch**](patch-object.md) , avec des privilèges élevés. Après avoir inscrit le correctif, vous pouvez appliquer le correctif à l’aide des fonctions [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) ou [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) , des méthodes [**ApplyPatch**](installer-applypatch.md) ou [**ApplyMultiplePatches**](installer-applymultiplepatches.md) de l’objet du [**programme d’installation**](installer-object.md)ou de l’option de [ligne de commande](command-line-options.md)/p.

> [!Note]
> Un correctif peut être enregistré comme ayant des privilèges élevés avant l’installation de l’application. Lorsqu’un correctif a été inscrit, il reste inscrit jusqu’à ce que la dernière application inscrite pour ce correctif soit supprimée.
> 
> Les correctifs appliqués à une application gérée par utilisateur ne peuvent pas être supprimés sans supprimer toute l’application. Les inscriptions de correctifs pour une application gérée par utilisateur sont supprimées lors de la suppression de l’application.

Vous pouvez également utiliser cette méthode pour permettre à un non-administrateur de corriger une application par ordinateur, ou vous pouvez utiliser la mise à jour corrective des privilèges les plus faibles décrite dans mise à [jour corrective du contrôle de compte d’utilisateur (UAC)](user-account-control--uac--patching.md).

## <a name="example-1"></a>Exemple 1

L’exemple de script suivant utilise la méthode [**SourceListAddSource**](patch-sourcelistaddsource.md) pour inscrire un package de correctifs situé dans \\ \\ Server \\ share \\ Products \\ patchs \\ example. msp comme ayant des privilèges élevés. Ce correctif est alors prêt à être appliqué à un produit géré par utilisateur.

``` syntax
const msiInstallContextUserManaged = 1
const msiInstallSourceTypeNetwork = 1

const PatchCode = "{XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}"
const UserSid = "S-X-X-XX-XXXXXXXXX-XXXXXXXXX-XXXXXXXXX-XXXXXXX"
const PatchPath = "\\server\share\products\patches\"
const PatchPackageName = "example.msp"

Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

Set patch = installer.Patch(PatchCode, "", UserSid, msiInstallContextUserManaged)

patch.SourceListAddSource msiInstallSourceTypeNetwork, PatchPath, 0

patch.SourceListInfo("PackageName") = PatchPackageName
```

## <a name="example-2"></a>Exemple 2

L’exemple de code suivant utilise la fonction [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) pour inscrire un package de correctifs situé dans \\ \\ Server \\ share \\ Products \\ patchs \\ example. msp comme ayant des privilèges élevés. Ce correctif est alors prêt à être appliqué à un produit géré par utilisateur.


```C++
#ifndef UNICODE
#define UNICODE
#endif    // UNICODE

#ifndef _WIN32_MSI
#define _WIN32_MSI
#endif    // _WIN32_MSI

#include <windows.h>
#include <msi.h>


/////////////////////////////////////////////////////////////////
// RegisterElevatedPatch
//
// Purpose: register a patch elevated from a network location
//
// Arguments:
//    wszPatchCode <entity type="ndash"/> GUID of patch to be registered
//    wszUserSid   - String SID that specifies the user account
//    wszPatchPath <entity type="ndash"/> Network location of patch
//    wszPatchPackageName <entity type="ndash"/> Package name of patch
//
/////////////////////////////////////////////////////////////////
UINT RegisterElevatedPatch(LPCWSTR wszPatchCode, 
LPCWSTR wszUserSid, 
LPCWSTR wszPatchPath, 
LPCWSTR wszPatchPackageName)
{
// wszUserSid can be NULL
// when wszUserSid is NULL, register patch for current user
// current user must be administrator
if (!wszPatchCode || !wszPatchPath || !wszPatchPackageName)
    return ERROR_INVALID_PARAMETER;

UINT uiReturn = ERROR_SUCCESS;

uiReturn = MsiSourceListAddSourceEx(
/*szPatchCode*/ wszPatchCode,
/*szUserSid*/ wszUserSid,
/*dwContext*/ MSIINSTALLCONTEXT_USERMANAGED,
/*dwOptions*/ MSISOURCETYPE_NETWORK+MSICODE_PATCH,
/*szSource*/ wszPatchPath,
/*dwIndex*/ 0);
if (ERROR_SUCCESS == uiReturn)
{
uiReturn = MsiSourceListSetInfo(
/*szPatchCode*/ wszPatchCode,
/*szUserSid*/ wszUserSid,
/*dwContext*/ MSIINSTALLCONTEXT_USERMANAGED,
/*dwOptions*/ MSISOURCETYPE_NETWORK+MSICODE_PATCH,
/*szProperty*/ L"PackageName",
/*szValue*/ wszPatchPackageName);
if (ERROR_SUCCESS != uiReturn)
{
// Function call failed, return error code
    return uiReturn;
}
}
else
{
// Function call failed, return error code
    return uiReturn;
}

return ERROR_SUCCESS;
}


```



 

 
