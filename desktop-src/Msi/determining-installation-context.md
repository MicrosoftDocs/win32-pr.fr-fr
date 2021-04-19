---
description: Une application peut appeler les fonctions MsiEnumProducts ou MsiEnumProductsEx pour énumérer les produits installés ou publiés sur le système.
ms.assetid: 162bda20-0c62-4eac-8c1f-fd107e42c528
title: Détermination du contexte d’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24367e2367f845dfef2e4947a32d9dec84d644cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536720"
---
# <a name="determining-installation-context"></a>Détermination du contexte d’installation

Une application peut appeler les fonctions [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa) ou [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) pour énumérer les produits installés ou publiés sur le système. Cette fonction peut énumérer tous les produits installés dans le [contexte d’installation](installation-context.md)par ordinateur. Il peut énumérer les produits installés dans le contexte par utilisateur pour l’utilisateur actuel. L’application peut récupérer des informations sur le contexte de ces produits en appelant les fonctions [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) ou [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa) .

La Windows Installer peut installer des produits à exécuter avec des privilèges élevés (système) pour les utilisateurs non-administrateurs. Cela requiert l’autorisation d’un utilisateur administrateur. Un produit installé avec des privilèges élevés est appelé « géré ». Tous les produits installés par ordinateur sont gérés. Les produits installés par utilisateur sont gérés uniquement si un agent du système local effectue une publication en empruntant l’identité d’un utilisateur. Il s’agit de la méthode utilisée par le déploiement de logiciel via [stratégie de groupe](/previous-versions/windows/desktop/Policy/group-policy-start-page). Les applications par utilisateur installées alors que les stratégies [AlwaysInstallElevated a](alwaysinstallelevated.md) sont définies ne sont pas considérées comme gérées. En appelant [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda), une application peut vérifier si un produit particulier est géré.

L’exemple suivant montre comment une application détermine le contexte à l’aide de [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa), [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)et [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda).


```C++
#ifndef UNICODE
#define UNICODE
#endif //UNICODE

#ifndef _WIN32_MSI
#define _WIN32_MSI 200
#endif //_WIN32_MSI

#include <stdio.h>
#include <windows.h>
#include <msi.h>
#pragma comment(lib, "msi.lib")

const int cchGUID = 38;

UINT DetermineContextForAllProducts()
{
    WCHAR wszProductCode[cchGUID+1] = {0};
    WCHAR wszAssignmentType[10] = {0};
    DWORD cchAssignmentType = 
            sizeof(wszAssignmentType)/sizeof(wszAssignmentType[0]);
    DWORD dwIndex = 0;

    DWORD cchProductName = MAX_PATH;
    WCHAR* lpProductName = new WCHAR[cchProductName];
    if (!lpProductName)
    {
        return ERROR_OUTOFMEMORY;
    }

    UINT uiStatus = ERROR_SUCCESS;

    // enumerate all visible products
    do
    {
        uiStatus = MsiEnumProducts(dwIndex,
                          wszProductCode);
        if (ERROR_SUCCESS == uiStatus)
        {
            cchAssignmentType = 
                sizeof(wszAssignmentType)/sizeof(wszAssignmentType[0]);
            BOOL fPerMachine = FALSE;
            BOOL fManaged = FALSE;

            // Determine assignment type of product
            // This indicates whether the product
            // instance is per-user or per-machine
            if (ERROR_SUCCESS == 
                MsiGetProductInfo(wszProductCode,INSTALLPROPERTY_ASSIGNMENTTYPE,wszAssignmentType,&cchAssignmentType))
            {
                if (L'1' == wszAssignmentType[0])
                    fPerMachine = TRUE;
            }
            else
            {
                // This halts the enumeration and fails. Alternatively the error
                // could be logged and enumeration continued for the
                // remainder of the products
                uiStatus = ERROR_FUNCTION_FAILED;
                break;
            }

            // determine the "managed" status of the product.
            // If fManaged is TRUE, product is installed managed
            // and runs with elevated privileges.
            // If fManaged is FALSE, product installation operations
            // run as the user.
            if (ERROR_SUCCESS != MsiIsProductElevated(wszProductCode,
                                         &fManaged))
            {
                // This halts the enumeration and fails. Alternatively the error
                // could be logged and enumeration continued for the
                // remainder of the products
                uiStatus = ERROR_FUNCTION_FAILED;
                break;
            }

            // obtain the user friendly name of the product
            UINT uiReturn = MsiGetProductInfo(wszProductCode,INSTALLPROPERTY_PRODUCTNAME,lpProductName,&cchProductName);
            if (ERROR_MORE_DATA == uiReturn)
            {
                // try again, but with a larger product name buffer
                delete [] lpProductName;

                // returned character count does not include
                // terminating NULL
                ++cchProductName;

                lpProductName = new WCHAR[cchProductName];
                if (!lpProductName)
                {
                    uiStatus = ERROR_OUTOFMEMORY;
                    break;
                }

                uiReturn = MsiGetProductInfo(wszProductCode,INSTALLPROPERTY_PRODUCTNAME,lpProductName,&cchProductName);
            }

            if (ERROR_SUCCESS != uiReturn)
            {
                // This halts the enumeration and fails. Alternatively the error
                // could be logged and enumeration continued for the
                // remainder of the products
                uiStatus = ERROR_FUNCTION_FAILED;
                break;
            }

            // output information
            wprintf(L" Product %s:\n", lpProductName);
            wprintf(L"\t%s\n", wszProductCode);
                        wprintf(L"\tInstalled %s %s\n", 
                fPerMachine ? L"per-machine" : L"per-user",
                fManaged ? L"managed" : L"non-managed");
        }
        dwIndex++;
    }
    while (ERROR_SUCCESS == uiStatus);

    if (lpProductName)
    {
        delete [] lpProductName;
        lpProductName = NULL;
    }

    return (ERROR_NO_MORE_ITEMS == uiStatus) ? ERROR_SUCCESS : uiStatus;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa)
</dt> <dt>

[**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)
</dt> <dt>

[**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa)
</dt> <dt>

[**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda)
</dt> <dt>

[Installation d’un package avec des privilèges élevés pour un non-administrateur](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
</dt> <dt>

[Publication d’une application Per-User à installer avec des privilèges élevés](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
</dt> <dt>

[Contexte d’installation](installation-context.md)
</dt> </dl>

 

 
