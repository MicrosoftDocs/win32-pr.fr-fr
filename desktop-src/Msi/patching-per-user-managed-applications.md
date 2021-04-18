---
description: À partir de Windows Installer 3,0, il est possible d’appliquer des correctifs à une application qui a été installée dans un contexte géré par l’utilisateur une fois que le correctif a été inscrit comme ayant des privilèges élevés.
ms.assetid: ebe5f447-9b74-48dc-8192-f2ac90dca490
title: Mise à jour corrective des applications gérées par utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aa6a19933e5c8ab409d510d980b8ed634a630e1
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106522512"
---
# <a name="patching-per-user-managed-applications"></a><span data-ttu-id="6083a-103">Mise à jour corrective des applications gérées par utilisateur</span><span class="sxs-lookup"><span data-stu-id="6083a-103">Patching Per-User Managed Applications</span></span>

<span data-ttu-id="6083a-104">À partir de Windows Installer 3,0, il est possible d’appliquer des correctifs à une application qui a été installée dans un contexte géré par l’utilisateur une fois que le correctif a été inscrit comme ayant des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="6083a-104">Beginning with Windows Installer 3.0, it is possible to apply patches to an application that has been installed in a per-user-managed context after the patch has been registered as having elevated privileges.</span></span>

<span data-ttu-id="6083a-105">**Windows Installer 2,0 :** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6083a-105">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="6083a-106">Vous ne pouvez pas appliquer de correctifs aux applications installées dans un contexte géré par utilisateur à l’aide des versions de Windows Installer antérieures à Windows Installer 3,0.</span><span class="sxs-lookup"><span data-stu-id="6083a-106">You cannot apply patches to applications that are installed in a per-user managed context using versions of Windows Installer earlier than Windows Installer 3.0.</span></span>

<span data-ttu-id="6083a-107">Une application est installée dans l’état géré par l’utilisateur dans les cas suivants.</span><span class="sxs-lookup"><span data-stu-id="6083a-107">An application is installed in the per-user-managed state in the following cases.</span></span>

-   <span data-ttu-id="6083a-108">L’installation par utilisateur de l’application a été effectuée à l’aide du déploiement et [stratégie de groupe](/previous-versions/windows/desktop/Policy/group-policy-start-page).</span><span class="sxs-lookup"><span data-stu-id="6083a-108">The per-user installation of the application was performed using deployment and [Group Policy](/previous-versions/windows/desktop/Policy/group-policy-start-page).</span></span>
-   <span data-ttu-id="6083a-109">L’application a été publiée sur un utilisateur spécifié et installée par la méthode décrite dans [publication d’une application Per-User à installer avec des privilèges élevés](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md).</span><span class="sxs-lookup"><span data-stu-id="6083a-109">The application was advertised to a specified user and installed by the method described in [Advertising a Per-User Application To Be Installed with Elevated Privileges](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md).</span></span>

<span data-ttu-id="6083a-110">Des privilèges sont requis pour installer une application dans le contexte géré par l’utilisateur ; par conséquent, les réinstallations de Windows Installer ultérieures ou les réparations de l’application sont également effectuées par le programme d’installation à l’aide de privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="6083a-110">Privileges are required to install an application in the per-user-managed context; therefore, future Windows Installer reinstallations or repairs of the application are also performed by the installer using elevated privileges.</span></span> <span data-ttu-id="6083a-111">Cela signifie que seuls les correctifs de sources approuvées peuvent être appliqués à l’application.</span><span class="sxs-lookup"><span data-stu-id="6083a-111">This means that only patches from trusted sources can be applied to the application.</span></span>

<span data-ttu-id="6083a-112">À partir de Windows Installer 3,0, vous pouvez appliquer un correctif à une application gérée par utilisateur une fois que le correctif a été inscrit comme ayant des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="6083a-112">Beginning with Windows Installer 3.0, you can apply a patch to a per-user managed application after the patch has been registered as having elevated privileges.</span></span> <span data-ttu-id="6083a-113">Pour inscrire un correctif comme ayant des privilèges élevés, utilisez la fonction [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) ou la méthode [**SourceListAddSource**](patch-sourcelistaddsource.md) de l’objet [**patch**](patch-object.md) , avec des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="6083a-113">To register a patch as having elevated privileges, use the [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) function or the [**SourceListAddSource**](patch-sourcelistaddsource.md) method of the [**Patch**](patch-object.md) object, with elevated privileges.</span></span> <span data-ttu-id="6083a-114">Après avoir inscrit le correctif, vous pouvez appliquer le correctif à l’aide des fonctions [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) ou [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) , des méthodes [**ApplyPatch**](installer-applypatch.md) ou [**ApplyMultiplePatches**](installer-applymultiplepatches.md) de l’objet du [**programme d’installation**](installer-object.md)ou de l’option de [ligne de commande](command-line-options.md)/p.</span><span class="sxs-lookup"><span data-stu-id="6083a-114">After registering the patch, you can apply the patch using the [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) or [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) functions, [**ApplyPatch**](installer-applypatch.md) or [**ApplyMultiplePatches**](installer-applymultiplepatches.md) methods of the [**Installer Object**](installer-object.md), or the /p [command-line option](command-line-options.md).</span></span>

> [!Note]
> <span data-ttu-id="6083a-115">Un correctif peut être enregistré comme ayant des privilèges élevés avant l’installation de l’application.</span><span class="sxs-lookup"><span data-stu-id="6083a-115">A patch can be registered as having elevated privileges before the application is installed.</span></span> <span data-ttu-id="6083a-116">Lorsqu’un correctif a été inscrit, il reste inscrit jusqu’à ce que la dernière application inscrite pour ce correctif soit supprimée.</span><span class="sxs-lookup"><span data-stu-id="6083a-116">When a patch has been registered, it remains registered until the last registered application for this patch is removed.</span></span>
> 
> <span data-ttu-id="6083a-117">Les correctifs appliqués à une application gérée par utilisateur ne peuvent pas être supprimés sans supprimer toute l’application.</span><span class="sxs-lookup"><span data-stu-id="6083a-117">Patches that have been applied to a per-user managed application cannot be removed without removing the entire application.</span></span> <span data-ttu-id="6083a-118">Les inscriptions de correctifs pour une application gérée par utilisateur sont supprimées lors de la suppression de l’application.</span><span class="sxs-lookup"><span data-stu-id="6083a-118">The patch registrations for a per-user managed application are removed on the removal of the application.</span></span>

<span data-ttu-id="6083a-119">Vous pouvez également utiliser cette méthode pour permettre à un non-administrateur de corriger une application par ordinateur, ou vous pouvez utiliser la mise à jour corrective des privilèges les plus faibles décrite dans mise à [jour corrective du contrôle de compte d’utilisateur (UAC)](user-account-control--uac--patching.md).</span><span class="sxs-lookup"><span data-stu-id="6083a-119">You can also use this method to enable a non-administrator to patch a per-machine application, or you can use least-privilege patching described in [User Account Control (UAC) Patching](user-account-control--uac--patching.md).</span></span>

## <a name="example-1"></a><span data-ttu-id="6083a-120">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="6083a-120">Example 1</span></span>

<span data-ttu-id="6083a-121">L’exemple de script suivant utilise la méthode [**SourceListAddSource**](patch-sourcelistaddsource.md) pour inscrire un package de correctifs situé dans \\ \\ Server \\ share \\ Products \\ patchs \\ example. msp comme ayant des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="6083a-121">The following scripting sample uses the [**SourceListAddSource**](patch-sourcelistaddsource.md) method to register a patch package located at \\\\server\\share\\products\\patches\\example.msp as having elevated privileges.</span></span> <span data-ttu-id="6083a-122">Ce correctif est alors prêt à être appliqué à un produit géré par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6083a-122">That patch is then ready to be applied to a per-user managed product.</span></span>

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

## <a name="example-2"></a><span data-ttu-id="6083a-123">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="6083a-123">Example 2</span></span>

<span data-ttu-id="6083a-124">L’exemple de code suivant utilise la fonction [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) pour inscrire un package de correctifs situé dans \\ \\ Server \\ share \\ Products \\ patchs \\ example. msp comme ayant des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="6083a-124">The following code sample uses the [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) function to register a patch package located at \\\\server\\share\\products\\patches\\example.msp as having elevated privileges.</span></span> <span data-ttu-id="6083a-125">Ce correctif est alors prêt à être appliqué à un produit géré par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6083a-125">That patch is then ready to be applied to a per-user managed product.</span></span>


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



 

 
