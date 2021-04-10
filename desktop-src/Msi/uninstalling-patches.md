---
description: À partir de Windows Installer 3,0, il est possible de désinstaller certains correctifs des applications.
ms.assetid: 11e995b7-30c7-4992-b436-3af289ac3966
title: Désinstallation des correctifs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff9418704bdeeb5ccc57839cbe2416faa5692265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210923"
---
# <a name="uninstalling-patches"></a><span data-ttu-id="dfae7-103">Désinstallation des correctifs</span><span class="sxs-lookup"><span data-stu-id="dfae7-103">Uninstalling Patches</span></span>

<span data-ttu-id="dfae7-104">À partir de Windows Installer 3,0, il est possible de désinstaller certains correctifs des applications.</span><span class="sxs-lookup"><span data-stu-id="dfae7-104">Beginning with Windows Installer 3.0, it is possible to uninstall some patches from applications.</span></span> <span data-ttu-id="dfae7-105">Le correctif doit être un [correctif](uninstallable-patches.md)qui peut être désinstallé.</span><span class="sxs-lookup"><span data-stu-id="dfae7-105">The patch must be an [uninstallable patch](uninstallable-patches.md).</span></span> <span data-ttu-id="dfae7-106">Lors de l’utilisation d’une version Windows Installer antérieure à la version 3,0, la [suppression des correctifs](removing-patches.md) nécessite la désinstallation du produit correctif et la réinstallation du produit sans appliquer le correctif logiciel.</span><span class="sxs-lookup"><span data-stu-id="dfae7-106">When using a Windows Installer version less than version 3.0, [removing patches](removing-patches.md) requires uninstalling the patch product and reinstalling the product without applying the patch.</span></span>

<span data-ttu-id="dfae7-107">**Windows Installer 2,0 :** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="dfae7-107">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="dfae7-108">Les correctifs appliqués à l’aide d’une version de Windows Installer antérieure à Windows Installer 3,0 ne peuvent pas être installés.</span><span class="sxs-lookup"><span data-stu-id="dfae7-108">Patches applied using a version of Windows Installer that is earlier than Windows Installer 3.0 are not uninstallable.</span></span>

<span data-ttu-id="dfae7-109">Lorsque vous appelez une désinstallation d’un correctif à l’aide d’une des méthodes suivantes, le programme d’installation tente de supprimer le correctif du premier produit visible pour l’application ou l’utilisateur qui demande la désinstallation.</span><span class="sxs-lookup"><span data-stu-id="dfae7-109">When you invoke an uninstallation of a patch by any of the following methods, the installer attempts to remove the patch from the first product visible to the application or user requesting the uninstallation.</span></span> <span data-ttu-id="dfae7-110">Le programme d’installation recherche les produits corrigés dans l’ordre suivant : géré par utilisateur, non géré par utilisateur et par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="dfae7-110">The installer searches for patched products in the following order: per-user managed, per-user unmanaged, per-machine.</span></span>

## <a name="uninstalling-a-patch-using-msipatchremove-on-a-command-line"></a><span data-ttu-id="dfae7-111">Désinstallation d’un correctif à l’aide de MSIPATCHREMOVE sur une ligne de commande</span><span class="sxs-lookup"><span data-stu-id="dfae7-111">Uninstalling a patch using MSIPATCHREMOVE on a command line</span></span>

<span data-ttu-id="dfae7-112">Vous pouvez désinstaller les correctifs à partir d’une commande à l’aide de msiexec.exe et des [options de ligne de commande](command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="dfae7-112">You can uninstall patches from a command by using msiexec.exe and the [Command Line Options](command-line-options.md).</span></span> <span data-ttu-id="dfae7-113">L’exemple de ligne de commande suivant supprime un [correctif logiciel](uninstallable-patches.md), example. msp, d’une application, example.msi à l’aide de la propriété [**MSIPATCHREMOVE**](msipatchremove.md) et de l’option de ligne de commande/i.</span><span class="sxs-lookup"><span data-stu-id="dfae7-113">The following sample command line removes an [uninstallable patch](uninstallable-patches.md), example.msp, from an application, example.msi, using the [**MSIPATCHREMOVE**](msipatchremove.md) property and the /i command line option.</span></span> <span data-ttu-id="dfae7-114">Lorsque vous utilisez/i, l’application corrigée peut être identifiée par le chemin d’accès au package de l’application (fichier. msi) ou le [Code du produit](product-codes.md)de l’application.</span><span class="sxs-lookup"><span data-stu-id="dfae7-114">When using /i, the patched application can be identified by the path to the application's package (.msi file) or the application's [product code](product-codes.md).</span></span> <span data-ttu-id="dfae7-115">Dans cet exemple, le package d’installation de l’application se trouve dans « \\ \\ Server \\ share \\ Products \\ example \\example.msi » et la propriété [**ProductCode**](productcode.md) de l’application est « {0C9840E7-7F0B-C648-10F0-4641926FE463} ».</span><span class="sxs-lookup"><span data-stu-id="dfae7-115">In this example, the application's installation package is located at "\\\\server\\share\\products\\example\\example.msi" and the application's [**ProductCode**](productcode.md) property is "{0C9840E7-7F0B-C648-10F0-4641926FE463}".</span></span> <span data-ttu-id="dfae7-116">Le package de correctifs se trouve à l’emplacement suivant : « \\ \\ Server \\ share \\ Products \\ example \\ patchs example \\ . msp » et le GUID du code correctif est « {EB8C947C-78B2-85A0-644D-86CEEF8E07C0} ».</span><span class="sxs-lookup"><span data-stu-id="dfae7-116">The patch package is located at "\\\\server\\share\\products\\example\\patches\\example.msp" and the patch code GUID is "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".</span></span>

<span data-ttu-id="dfae7-117">**Msiexec/I {0C9840E7-7F0B-C648-10F0-4641926FE463} MSIPATCHREMOVE = {EB8C947C-78B2-85A0-644D-86CEEF8E07C0}/QB**</span><span class="sxs-lookup"><span data-stu-id="dfae7-117">**Msiexec /I {0C9840E7-7F0B-C648-10F0-4641926FE463} MSIPATCHREMOVE={EB8C947C-78B2-85A0-644D-86CEEF8E07C0} /qb**</span></span>

## <a name="uninstalling-a-patch-using-the-standard-command-line-options"></a><span data-ttu-id="dfae7-118">Désinstallation d’un correctif à l’aide des options de ligne de commande standard</span><span class="sxs-lookup"><span data-stu-id="dfae7-118">Uninstalling a patch using the standard command line options</span></span>

<span data-ttu-id="dfae7-119">À partir de Windows Installer version 3,0, vous pouvez utiliser les [options de ligne de commande standard](standard-installer-command-line-options.md) utilisées par les mises à jour du système d’exploitation Microsoft Windows (update.exe) pour désinstaller Windows Installer correctifs à partir d’une ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="dfae7-119">Beginning with Windows Installer version 3.0, you can use the [standard command line options](standard-installer-command-line-options.md) used by Microsoft Windows Operating System Updates (update.exe) to uninstall Windows Installer patches from a command line.</span></span>

<span data-ttu-id="dfae7-120">La ligne de commande suivante est l’équivalent de la ligne de commande standard de la ligne de commande Windows Installer utilisée pour désinstaller un correctif à l’aide de la propriété [**MSIPATCHREMOVE**](msipatchremove.md) .</span><span class="sxs-lookup"><span data-stu-id="dfae7-120">The following command line is the standard command line equivalent of the Windows Installer command line used to uninstall a patch using the [**MSIPATCHREMOVE**](msipatchremove.md) property.</span></span> <span data-ttu-id="dfae7-121">L’option/Uninstall utilisée avec l’option/package indique la désinstallation d’un correctif.</span><span class="sxs-lookup"><span data-stu-id="dfae7-121">The /uninstall option used with the /package option denotes the uninstallation of a patch.</span></span> <span data-ttu-id="dfae7-122">Le correctif peut être référencé par le chemin d’accès complet au correctif ou par le GUID du code correctif.</span><span class="sxs-lookup"><span data-stu-id="dfae7-122">The patch can be referenced by the full path to the patch or by the patch code GUID.</span></span>

<span data-ttu-id="dfae7-123">**Msiexec/package {0C9840E7-7F0B-C648-10F0-4641926FE463}/Uninstall {EB8C947C-78B2-85A0-644D-86CEEF8E07C0}/passive**</span><span class="sxs-lookup"><span data-stu-id="dfae7-123">**Msiexec /package {0C9840E7-7F0B-C648-10F0-4641926FE463} /uninstall {EB8C947C-78B2-85A0-644D-86CEEF8E07C0} /passive**</span></span>

> [!Note]  
> <span data-ttu-id="dfae7-124">L’option standard/passive n’est pas un équivalent exact de l’option Windows Installer/QB.</span><span class="sxs-lookup"><span data-stu-id="dfae7-124">The /passive standard option is not an exact equivalent of the Windows Installer /qb option.</span></span>

 

## <a name="uninstalling-a-patch-using-the-removepatches-method"></a><span data-ttu-id="dfae7-125">Désinstallation d’un correctif à l’aide de la méthode RemovePatches</span><span class="sxs-lookup"><span data-stu-id="dfae7-125">Uninstalling a patch using the RemovePatches method</span></span>

<span data-ttu-id="dfae7-126">Vous pouvez désinstaller les correctifs à partir d’un script à l’aide de l' [Interface Windows Installer Automation](automation-interface.md).</span><span class="sxs-lookup"><span data-stu-id="dfae7-126">You can uninstall patches from script by using the Windows Installer [Automation Interface](automation-interface.md).</span></span> <span data-ttu-id="dfae7-127">L’exemple de script suivant supprime un [correctif logiciel](uninstallable-patches.md), example. msp, d’une application, example.msi à l’aide de la méthode [**RemovePatches**](installer-removepatches.md) de l’objet [installer](installer-object.md) .</span><span class="sxs-lookup"><span data-stu-id="dfae7-127">The following scripting sample removes an [uninstallable patch](uninstallable-patches.md), example.msp, from an application, example.msi, using the [**RemovePatches**](installer-removepatches.md) method of the [Installer](installer-object.md) object.</span></span> <span data-ttu-id="dfae7-128">Chaque correctif en cours de désinstallation peut être représenté soit par le chemin d’accès complet au package de correctifs, soit par le GUID du code correctif.</span><span class="sxs-lookup"><span data-stu-id="dfae7-128">Each patch being uninstalled can be represented by either the full path to the patch package or the patch code GUID.</span></span> <span data-ttu-id="dfae7-129">Dans cet exemple, le package d’installation de l’application se trouve dans « \\ \\ Server \\ share \\ Products \\ example \\example.msi » et la propriété [**ProductCode**](productcode.md) de l’application est « {0C9840E7-7F0B-C648-10F0-4641926FE463} ».</span><span class="sxs-lookup"><span data-stu-id="dfae7-129">In this example, the application's installation package is located at "\\\\server\\share\\products\\example\\example.msi" and the application's [**ProductCode**](productcode.md) property is "{0C9840E7-7F0B-C648-10F0-4641926FE463}".</span></span> <span data-ttu-id="dfae7-130">Le package de correctifs se trouve à l’emplacement suivant : « \\ \\ Server \\ share \\ Products \\ example \\ patchs example \\ . msp » et le GUID du code correctif est « {EB8C947C-78B2-85A0-644D-86CEEF8E07C0} ».</span><span class="sxs-lookup"><span data-stu-id="dfae7-130">The patch package is located at "\\\\server\\share\\products\\example\\patches\\example.msp" and the patch code GUID is "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".</span></span>


```VB
const msiInstallTypeSingleInstance = 2
const PatchList = "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}"
const Product = "{0C9840E7-7F0B-C648-10F0-4641926FE463}"

Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

installer.RemovePatches(PatchList, Product, msiInstallTypeSingleInstance, "")
```



## <a name="uninstalling-a-patch-using-addremove-programs"></a><span data-ttu-id="dfae7-131">Désinstallation d’un correctif à l’aide d’ajout/suppression de programmes</span><span class="sxs-lookup"><span data-stu-id="dfae7-131">Uninstalling a patch using Add/Remove Programs</span></span>

<span data-ttu-id="dfae7-132">Avec Windows XP, vous pouvez désinstaller les correctifs à l’aide de la fonction Ajout/suppression de programmes.</span><span class="sxs-lookup"><span data-stu-id="dfae7-132">With Windows XP, you can uninstall patches using Add/Remove programs.</span></span>

## <a name="uninstalling-a-patch-using-the-msiremovepatches-function"></a><span data-ttu-id="dfae7-133">Désinstallation d’un correctif à l’aide de la fonction MsiRemovePatches</span><span class="sxs-lookup"><span data-stu-id="dfae7-133">Uninstalling a patch using the MsiRemovePatches function</span></span>

<span data-ttu-id="dfae7-134">Vos applications peuvent désinstaller les correctifs d’autres applications à l’aide des [fonctions Windows Installer](installer-functions.md).</span><span class="sxs-lookup"><span data-stu-id="dfae7-134">Your applications can uninstall patches from other applications by using the [Windows Installer Functions](installer-functions.md).</span></span> <span data-ttu-id="dfae7-135">L’exemple de code suivant supprime un [correctif logiciel](uninstallable-patches.md), example. msp, d’une application, example.msi à l’aide de la fonction [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) .</span><span class="sxs-lookup"><span data-stu-id="dfae7-135">The following code example removes an [uninstallable patch](uninstallable-patches.md), example.msp, from an application, example.msi, using the [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) function.</span></span> <span data-ttu-id="dfae7-136">Un correctif peut être référencé par le chemin d’accès complet au package correctif ou le GUID du code correctif.</span><span class="sxs-lookup"><span data-stu-id="dfae7-136">A patch can be referenced by the full path to the patch package or the patch code GUID.</span></span> <span data-ttu-id="dfae7-137">Dans cet exemple, le package d’installation de l’application se trouve dans « \\ \\ Server \\ share \\ Products \\ example \\example.msi » et la propriété [**ProductCode**](productcode.md) de l’application est « {0C9840E7-7F0B-C648-10F0-4641926FE463} ».</span><span class="sxs-lookup"><span data-stu-id="dfae7-137">In this example, the application's installation package is located at "\\\\server\\share\\products\\example\\example.msi" and the application's [**ProductCode**](productcode.md) property is "{0C9840E7-7F0B-C648-10F0-4641926FE463}".</span></span> <span data-ttu-id="dfae7-138">Le package de correctifs se trouve à l’emplacement suivant : « \\ \\ Server \\ share \\ Products \\ example \\ patchs example \\ . msp » et le GUID du code correctif est « {EB8C947C-78B2-85A0-644D-86CEEF8E07C0} ».</span><span class="sxs-lookup"><span data-stu-id="dfae7-138">The patch package is located at "\\\\server\\share\\products\\example\\patches\\example.msp" and the patch code GUID is "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".</span></span>


```C++
    UINT uiReturn = MsiRemovePatches(
          /*szPatchList=*/TEXT("\\server\\share\\products\\example\\patches\\example.msp"),
          /*szProductCode=*/  TEXT("{0C9840E7-7F0B-C648-10F0-4641926FE463}"),
          /*eUninstallType=*/ INSTALLTYPE_SINGLE_INSTANCE,
          /*szPropertyList=*/ NULL);
```



## <a name="uninstalling-a-patch-from-all-applications-using-msiremovepatches-function"></a><span data-ttu-id="dfae7-139">Désinstallation d’un correctif de toutes les applications à l’aide de la fonction MsiRemovePatches</span><span class="sxs-lookup"><span data-stu-id="dfae7-139">Uninstalling a patch from all applications using MsiRemovePatches function</span></span>

<span data-ttu-id="dfae7-140">Un seul correctif peut mettre à jour plusieurs produits sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="dfae7-140">A single patch can update more than one product on the computer.</span></span> <span data-ttu-id="dfae7-141">Une application peut utiliser [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) pour énumérer tous les produits sur l’ordinateur et déterminer si un correctif a été appliqué à une instance particulière du produit.</span><span class="sxs-lookup"><span data-stu-id="dfae7-141">An application can use [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) to enumerate all the products on the computer and determine whether a patch has been applied to a particular instance of the product.</span></span> <span data-ttu-id="dfae7-142">L’application peut ensuite désinstaller le correctif à l’aide de [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa).</span><span class="sxs-lookup"><span data-stu-id="dfae7-142">The application can then uninstall the patch using [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa).</span></span> <span data-ttu-id="dfae7-143">Par exemple, un seul correctif peut mettre à jour plusieurs produits si le correctif met à jour un fichier dans un composant qui est partagé par plusieurs produits et le correctif est distribué pour mettre à jour les deux produits.</span><span class="sxs-lookup"><span data-stu-id="dfae7-143">For example, a single patch can update multiple products if the patch updates a file in a component that is shared by multiple products and the patch is distributed to update both products.</span></span>

<span data-ttu-id="dfae7-144">L’exemple suivant montre comment une application peut utiliser le Windows Installer pour supprimer un correctif de toutes les applications qui sont disponibles pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dfae7-144">The following example demonstrates how an application can use the Windows Installer to remove a patch from all applications that are available to the user.</span></span> <span data-ttu-id="dfae7-145">Elle ne supprime pas le correctif logiciel des applications installées par utilisateur pour un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dfae7-145">It does not remove the patch from applications installed per-user for another user.</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif //UNICODE

#ifndef _WIN32_MSI
#define _WIN32_MSI 300
#endif //_WIN32_MSI

#include <stdio.h>
#include <windows.h>
#include <msi.h>

#pragma comment(lib, "msi.lib")

const int cchGUID = 38;

///////////////////////////////////////////////////////////////////
// RemovePatchFromAllVisibleapplications:
//
// Arguments:
//    wszPatchToRemove - GUID of patch to remove
//
///////////////////////////////////////////////////////////////////
//
UINT RemovePatchFromAllVisibleapplications(LPCWSTR wszPatchToRemove)
{
    if (!wszPatchToRemove)
        return ERROR_INVALID_PARAMETER;

    UINT uiStatus = ERROR_SUCCESS;
    DWORD dwIndex = 0;
    WCHAR wszapplicationCode[cchGUID+1] = {0};

    DWORD dwapplicationSearchContext = MSIINSTALLCONTEXT_ALL;
    MSIINSTALLCONTEXT dwInstallContext = MSIINSTALLCONTEXT_NONE;

    do
    {
        // Enumerate all visible applications in all contexts for the caller.
        // NULL for szUserSid defaults to using the caller's SID
        uiStatus = MsiEnumProductsEx(/*szapplicationCode*/NULL,
         /*szUserSid*/NULL,
         dwapplicationSearchContext,
         dwIndex,
         wszapplicationCode,
         &dwInstallContext,
         /*szSid*/NULL,
         /*pcchSid*/NULL);

        if (ERROR_SUCCESS == uiStatus)
        {
            // check to see if the provided patch is
            // registered for this application instance
            UINT uiPatchStatus = MsiGetPatchInfoEx(wszPatchToRemove,
             wszapplicationCode,
             /*szUserSid*/NULL,
             dwInstallContext,
             INSTALLPROPERTY_PATCHSTATE,
             NULL,
             NULL);

            if (ERROR_SUCCESS == uiPatchStatus)
            {
                // patch is registered to this application; remove patch
                wprintf(L"Removing patch %s from application %s...\n",
                 wszPatchToRemove, wszapplicationCode);
                                
                UINT uiRemoveStatus = MsiRemovePatches(
                 wszPatchToRemove,
                 wszapplicationCode,
                 INSTALLTYPE_SINGLE_INSTANCE,
                 L"");

                if (ERROR_SUCCESS != uiRemoveStatus)
                {
                    // This halts the enumeration and fails. Alternatively
                    // you could output an error and continue the
                    // enumeration
                     return ERROR_FUNCTION_FAILED;
                }
            }
            else if (ERROR_UNKNOWN_PATCH != uiPatchStatus)
            {
                // Some other error occurred during processing. This
                // halts the enumeration and fails. Alternatively you
                // could output an error and continue the enumeration
                 return ERROR_FUNCTION_FAILED;
            }
            // else patch was not applied to this application
            // (ERROR_UNKNOWN_PATCH returned)
        }

        dwIndex++;
    }
    while (uiStatus == ERROR_SUCCESS);

    if (ERROR_NO_MORE_ITEMS != uiStatus)
        return ERROR_FUNCTION_FAILED;

    return ERROR_SUCCESS;
}
```



## <a name="related-topics"></a><span data-ttu-id="dfae7-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dfae7-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfae7-147">Séquencement des correctifs</span><span class="sxs-lookup"><span data-stu-id="dfae7-147">Patch Sequencing</span></span>](sequencing-patches.md)
</dt> <dt>

[<span data-ttu-id="dfae7-148">Suppression des correctifs</span><span class="sxs-lookup"><span data-stu-id="dfae7-148">Removing Patches</span></span>](removing-patches.md)
</dt> <dt>

[<span data-ttu-id="dfae7-149">Correctifs désinstallés</span><span class="sxs-lookup"><span data-stu-id="dfae7-149">Uninstallable Patches</span></span>](uninstallable-patches.md)
</dt> <dt>

[<span data-ttu-id="dfae7-150">Actions personnalisées de désinstallation des correctifs</span><span class="sxs-lookup"><span data-stu-id="dfae7-150">Patch Uninstall Custom Actions</span></span>](patch-uninstall-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="dfae7-151">**MSIPATCHREMOVE**</span><span class="sxs-lookup"><span data-stu-id="dfae7-151">**MSIPATCHREMOVE**</span></span>](msipatchremove.md)
</dt> <dt>

[<span data-ttu-id="dfae7-152">**MsiEnumapplicationsEx**</span><span class="sxs-lookup"><span data-stu-id="dfae7-152">**MsiEnumapplicationsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[<span data-ttu-id="dfae7-153">**MsiGetPatchInfoEx**</span><span class="sxs-lookup"><span data-stu-id="dfae7-153">**MsiGetPatchInfoEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[<span data-ttu-id="dfae7-154">**MsiRemovePatches**</span><span class="sxs-lookup"><span data-stu-id="dfae7-154">**MsiRemovePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 



