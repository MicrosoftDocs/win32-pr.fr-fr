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
# <a name="determining-installation-context"></a><span data-ttu-id="ffa08-103">Détermination du contexte d’installation</span><span class="sxs-lookup"><span data-stu-id="ffa08-103">Determining Installation Context</span></span>

<span data-ttu-id="ffa08-104">Une application peut appeler les fonctions [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa) ou [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) pour énumérer les produits installés ou publiés sur le système.</span><span class="sxs-lookup"><span data-stu-id="ffa08-104">An application can call the [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa) or [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) functions to enumerate products that are installed or advertised on the system.</span></span> <span data-ttu-id="ffa08-105">Cette fonction peut énumérer tous les produits installés dans le [contexte d’installation](installation-context.md)par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ffa08-105">This function can enumerate all the products installed in the per-machine [installation context](installation-context.md).</span></span> <span data-ttu-id="ffa08-106">Il peut énumérer les produits installés dans le contexte par utilisateur pour l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="ffa08-106">It can enumerate the products installed in the per-user context for the current user.</span></span> <span data-ttu-id="ffa08-107">L’application peut récupérer des informations sur le contexte de ces produits en appelant les fonctions [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) ou [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa) .</span><span class="sxs-lookup"><span data-stu-id="ffa08-107">The application can retrieve information about the context of these products by calling the [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) or [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa) functions.</span></span>

<span data-ttu-id="ffa08-108">La Windows Installer peut installer des produits à exécuter avec des privilèges élevés (système) pour les utilisateurs non-administrateurs.</span><span class="sxs-lookup"><span data-stu-id="ffa08-108">The Windows Installer can install products to run with elevated (system) privileges for non-administrator users.</span></span> <span data-ttu-id="ffa08-109">Cela requiert l’autorisation d’un utilisateur administrateur.</span><span class="sxs-lookup"><span data-stu-id="ffa08-109">This requires the permission of an administrator user.</span></span> <span data-ttu-id="ffa08-110">Un produit installé avec des privilèges élevés est appelé « géré ».</span><span class="sxs-lookup"><span data-stu-id="ffa08-110">A product that is installed with elevated privileges is called "managed."</span></span> <span data-ttu-id="ffa08-111">Tous les produits installés par ordinateur sont gérés.</span><span class="sxs-lookup"><span data-stu-id="ffa08-111">All products installed per-machine are managed.</span></span> <span data-ttu-id="ffa08-112">Les produits installés par utilisateur sont gérés uniquement si un agent du système local effectue une publication en empruntant l’identité d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ffa08-112">Products installed per-user are only managed if a local system agent performs an advertisement while impersonating a user.</span></span> <span data-ttu-id="ffa08-113">Il s’agit de la méthode utilisée par le déploiement de logiciel via [stratégie de groupe](/previous-versions/windows/desktop/Policy/group-policy-start-page).</span><span class="sxs-lookup"><span data-stu-id="ffa08-113">This is the method used by software deployment through [Group Policy](/previous-versions/windows/desktop/Policy/group-policy-start-page).</span></span> <span data-ttu-id="ffa08-114">Les applications par utilisateur installées alors que les stratégies [AlwaysInstallElevated a](alwaysinstallelevated.md) sont définies ne sont pas considérées comme gérées.</span><span class="sxs-lookup"><span data-stu-id="ffa08-114">Per-user applications installed while the [AlwaysInstallElevated](alwaysinstallelevated.md) policies are set are not considered managed.</span></span> <span data-ttu-id="ffa08-115">En appelant [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda), une application peut vérifier si un produit particulier est géré.</span><span class="sxs-lookup"><span data-stu-id="ffa08-115">By calling [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda), an application can check whether a particular product is managed.</span></span>

<span data-ttu-id="ffa08-116">L’exemple suivant montre comment une application détermine le contexte à l’aide de [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa), [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)et [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda).</span><span class="sxs-lookup"><span data-stu-id="ffa08-116">The following sample demonstrates how an application determines context by using [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa), [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa), and [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="ffa08-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ffa08-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffa08-118">**MsiEnumProducts**</span><span class="sxs-lookup"><span data-stu-id="ffa08-118">**MsiEnumProducts**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumproductsa)
</dt> <dt>

[<span data-ttu-id="ffa08-119">**MsiGetProductInfo**</span><span class="sxs-lookup"><span data-stu-id="ffa08-119">**MsiGetProductInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)
</dt> <dt>

[<span data-ttu-id="ffa08-120">**MsiGetProductInfoEx**</span><span class="sxs-lookup"><span data-stu-id="ffa08-120">**MsiGetProductInfoEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa)
</dt> <dt>

[<span data-ttu-id="ffa08-121">**MsiIsProductElevated**</span><span class="sxs-lookup"><span data-stu-id="ffa08-121">**MsiIsProductElevated**</span></span>](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda)
</dt> <dt>

[<span data-ttu-id="ffa08-122">Installation d’un package avec des privilèges élevés pour un non-administrateur</span><span class="sxs-lookup"><span data-stu-id="ffa08-122">Installing a Package with Elevated Privileges for a Non-Admin</span></span>](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
</dt> <dt>

[<span data-ttu-id="ffa08-123">Publication d’une application Per-User à installer avec des privilèges élevés</span><span class="sxs-lookup"><span data-stu-id="ffa08-123">Advertising a Per-User Application To Be Installed with Elevated Privileges</span></span>](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
</dt> <dt>

[<span data-ttu-id="ffa08-124">Contexte d’installation</span><span class="sxs-lookup"><span data-stu-id="ffa08-124">Installation Context</span></span>](installation-context.md)
</dt> </dl>

 

 
