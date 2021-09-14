---
description: à partir de Windows Installer 3,0, il est possible de désinstaller certains correctifs des applications.
ms.assetid: 11e995b7-30c7-4992-b436-3af289ac3966
title: Désinstallation des correctifs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff9418704bdeeb5ccc57839cbe2416faa5692265
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121565"
---
# <a name="uninstalling-patches"></a>Désinstallation des correctifs

à partir de Windows Installer 3,0, il est possible de désinstaller certains correctifs des applications. Le correctif doit être un [correctif](uninstallable-patches.md)qui peut être désinstallé. lors de l’utilisation d’une version Windows Installer antérieure à la version 3,0, la [suppression des correctifs](removing-patches.md) nécessite la désinstallation du produit correctif et la réinstallation du produit sans appliquer le correctif logiciel.

**Windows Installer 2,0 :** Non pris en charge. les correctifs appliqués à l’aide d’une version de Windows Installer antérieure à Windows Installer 3,0 ne peuvent pas être installés.

Lorsque vous appelez une désinstallation d’un correctif à l’aide d’une des méthodes suivantes, le programme d’installation tente de supprimer le correctif du premier produit visible pour l’application ou l’utilisateur qui demande la désinstallation. Le programme d’installation recherche les produits corrigés dans l’ordre suivant : géré par utilisateur, non géré par utilisateur et par ordinateur.

## <a name="uninstalling-a-patch-using-msipatchremove-on-a-command-line"></a>Désinstallation d’un correctif à l’aide de MSIPATCHREMOVE sur une ligne de commande

Vous pouvez désinstaller les correctifs à partir d’une commande à l’aide de msiexec.exe et des [options de ligne de commande](command-line-options.md). L’exemple de ligne de commande suivant supprime un [correctif logiciel](uninstallable-patches.md), example. msp, d’une application, example.msi à l’aide de la propriété [**MSIPATCHREMOVE**](msipatchremove.md) et de l’option de ligne de commande/i. Lorsque vous utilisez/i, l’application corrigée peut être identifiée par le chemin d’accès au package de l’application (fichier .msi) ou le [Code de produit](product-codes.md)de l’application. Dans cet exemple, le package d’installation de l’application se trouve dans « \\ \\ Server \\ share \\ Products \\ example \\example.msi » et la propriété [**ProductCode**](productcode.md) de l’application est « {0C9840E7-7F0B-C648-10F0-4641926FE463} ». Le package de correctifs se trouve à l’emplacement suivant : « \\ \\ Server \\ share \\ Products \\ example \\ patchs example \\ . msp » et le GUID du code correctif est « {EB8C947C-78B2-85A0-644D-86CEEF8E07C0} ».

**Msiexec/I {0C9840E7-7F0B-C648-10F0-4641926FE463} MSIPATCHREMOVE = {EB8C947C-78B2-85A0-644D-86CEEF8E07C0}/QB**

## <a name="uninstalling-a-patch-using-the-standard-command-line-options"></a>Désinstallation d’un correctif à l’aide des options de ligne de commande standard

à partir de Windows Installer version 3,0, vous pouvez utiliser les [options de ligne de commande standard](standard-installer-command-line-options.md) utilisées par Microsoft Windows les mises à jour du système d’exploitation (update.exe) pour désinstaller les correctifs Windows Installer à partir d’une ligne de commande.

la ligne de commande suivante est l’équivalent de la ligne de commande standard de la ligne de commande Windows Installer utilisée pour désinstaller un correctif à l’aide de la propriété [**MSIPATCHREMOVE**](msipatchremove.md) . L’option/Uninstall utilisée avec l’option/package indique la désinstallation d’un correctif. Le correctif peut être référencé par le chemin d’accès complet au correctif ou par le GUID du code correctif.

**Msiexec/package {0C9840E7-7F0B-C648-10F0-4641926FE463}/Uninstall {EB8C947C-78B2-85A0-644D-86CEEF8E07C0}/passive**

> [!Note]  
> l’option standard/passive n’est pas un équivalent exact de l’option Windows Installer/qb.

 

## <a name="uninstalling-a-patch-using-the-removepatches-method"></a>Désinstallation d’un correctif à l’aide de la méthode RemovePatches

vous pouvez désinstaller les correctifs à partir d’un script à l’aide de l' [Interface Windows Installer Automation](automation-interface.md). L’exemple de script suivant supprime un [correctif logiciel](uninstallable-patches.md), example. msp, d’une application, example.msi à l’aide de la méthode [**RemovePatches**](installer-removepatches.md) de l’objet [installer](installer-object.md) . Chaque correctif en cours de désinstallation peut être représenté soit par le chemin d’accès complet au package de correctifs, soit par le GUID du code correctif. Dans cet exemple, le package d’installation de l’application se trouve dans « \\ \\ Server \\ share \\ Products \\ example \\example.msi » et la propriété [**ProductCode**](productcode.md) de l’application est « {0C9840E7-7F0B-C648-10F0-4641926FE463} ». Le package de correctifs se trouve à l’emplacement suivant : « \\ \\ Server \\ share \\ Products \\ example \\ patchs example \\ . msp » et le GUID du code correctif est « {EB8C947C-78B2-85A0-644D-86CEEF8E07C0} ».


```VB
const msiInstallTypeSingleInstance = 2
const PatchList = "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}"
const Product = "{0C9840E7-7F0B-C648-10F0-4641926FE463}"

Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

installer.RemovePatches(PatchList, Product, msiInstallTypeSingleInstance, "")
```



## <a name="uninstalling-a-patch-using-addremove-programs"></a>Désinstallation d’un correctif à l’aide d’ajout/suppression de programmes

avec Windows XP, vous pouvez désinstaller les correctifs à l’aide de la fonction ajout/suppression de programmes.

## <a name="uninstalling-a-patch-using-the-msiremovepatches-function"></a>Désinstallation d’un correctif à l’aide de la fonction MsiRemovePatches

vos applications peuvent désinstaller les correctifs d’autres applications à l’aide des [fonctions Windows Installer](installer-functions.md). L’exemple de code suivant supprime un [correctif logiciel](uninstallable-patches.md), example. msp, d’une application, example.msi à l’aide de la fonction [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) . Un correctif peut être référencé par le chemin d’accès complet au package correctif ou le GUID du code correctif. Dans cet exemple, le package d’installation de l’application se trouve dans « \\ \\ Server \\ share \\ Products \\ example \\example.msi » et la propriété [**ProductCode**](productcode.md) de l’application est « {0C9840E7-7F0B-C648-10F0-4641926FE463} ». Le package de correctifs se trouve à l’emplacement suivant : « \\ \\ Server \\ share \\ Products \\ example \\ patchs example \\ . msp » et le GUID du code correctif est « {EB8C947C-78B2-85A0-644D-86CEEF8E07C0} ».


```C++
    UINT uiReturn = MsiRemovePatches(
          /*szPatchList=*/TEXT("\\server\\share\\products\\example\\patches\\example.msp"),
          /*szProductCode=*/  TEXT("{0C9840E7-7F0B-C648-10F0-4641926FE463}"),
          /*eUninstallType=*/ INSTALLTYPE_SINGLE_INSTANCE,
          /*szPropertyList=*/ NULL);
```



## <a name="uninstalling-a-patch-from-all-applications-using-msiremovepatches-function"></a>Désinstallation d’un correctif de toutes les applications à l’aide de la fonction MsiRemovePatches

Un seul correctif peut mettre à jour plusieurs produits sur l’ordinateur. Une application peut utiliser [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) pour énumérer tous les produits sur l’ordinateur et déterminer si un correctif a été appliqué à une instance particulière du produit. L’application peut ensuite désinstaller le correctif à l’aide de [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa). Par exemple, un seul correctif peut mettre à jour plusieurs produits si le correctif met à jour un fichier dans un composant qui est partagé par plusieurs produits et le correctif est distribué pour mettre à jour les deux produits.

l’exemple suivant montre comment une application peut utiliser le Windows Installer pour supprimer un correctif de toutes les applications qui sont disponibles pour l’utilisateur. Elle ne supprime pas le correctif logiciel des applications installées par utilisateur pour un autre utilisateur.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Séquencement des correctifs](sequencing-patches.md)
</dt> <dt>

[Suppression des correctifs](removing-patches.md)
</dt> <dt>

[Correctifs désinstallés](uninstallable-patches.md)
</dt> <dt>

[Actions personnalisées de désinstallation des correctifs](patch-uninstall-custom-actions.md)
</dt> <dt>

[**MSIPATCHREMOVE**](msipatchremove.md)
</dt> <dt>

[**MsiEnumapplicationsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 



