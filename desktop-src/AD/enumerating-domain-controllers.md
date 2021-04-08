---
title: Énumération des contrôleurs de domaine
description: Dans les versions antérieures de Windows, une application pouvait uniquement obtenir un contrôleur de domaine unique dans un domaine en appelant DsGetDcName.
ms.assetid: bfc92777-6944-406a-8b93-949a1cf3e2c3
ms.tgt_platform: multiple
keywords:
- Active Directory exemples Active Directory, énumération de contrôleurs de domaine Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94384bb8c62edb7b0d45328dabe7765a43e4e610
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671330"
---
# <a name="enumerating-domain-controllers"></a><span data-ttu-id="9842b-104">Énumération des contrôleurs de domaine</span><span class="sxs-lookup"><span data-stu-id="9842b-104">Enumerating Domain Controllers</span></span>

<span data-ttu-id="9842b-105">Dans les versions antérieures de Windows, une application pouvait uniquement obtenir un contrôleur de domaine unique dans un domaine en appelant [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea).</span><span class="sxs-lookup"><span data-stu-id="9842b-105">In earlier versions of Windows, an application could only obtain a single domain controller in a domain by calling [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea).</span></span> <span data-ttu-id="9842b-106">Il n’existait aucun moyen de prédire quel contrôleur de domaine serait récupéré ou d’obtenir une liste des contrôleurs de domaine.</span><span class="sxs-lookup"><span data-stu-id="9842b-106">There was no way to predict which domain controller would be retrieved or to obtain a list of the domain controllers.</span></span> <span data-ttu-id="9842b-107">Windows permet à une application d’énumérer les contrôleurs de domaine dans un domaine à l’aide des fonctions [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena), [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta)et [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) .</span><span class="sxs-lookup"><span data-stu-id="9842b-107">Windows enables an application to enumerate the domain controllers in a domain by using the [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena), [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta), and [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) functions.</span></span>

<span data-ttu-id="9842b-108">Pour énumérer un contrôleur de domaine, appelez [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena).</span><span class="sxs-lookup"><span data-stu-id="9842b-108">To enumerate a domain controller, call [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena).</span></span> <span data-ttu-id="9842b-109">Cette fonction accepte les paramètres qui définissent le domaine à énumérer et d’autres options d’énumération.</span><span class="sxs-lookup"><span data-stu-id="9842b-109">This function takes parameters that define the domain to enumerate and other enumeration options.</span></span> <span data-ttu-id="9842b-110">**DsGetDcOpen** fournit un handle de contexte d’énumération de domaine qui est utilisé pour identifier l’opération d’énumération lorsque [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) et [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) sont appelés.</span><span class="sxs-lookup"><span data-stu-id="9842b-110">**DsGetDcOpen** provides a domain enumeration context handle that is used to identify the enumeration operation when [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) and [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) are called.</span></span>

<span data-ttu-id="9842b-111">La fonction [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) est appelée avec le handle de contexte d’énumération de domaine pour récupérer le contrôleur de domaine suivant dans l’énumération.</span><span class="sxs-lookup"><span data-stu-id="9842b-111">The [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) function is called with the domain enumeration context handle to retrieve the next domain controller in the enumeration.</span></span> <span data-ttu-id="9842b-112">La première fois que cette fonction est appelée, le premier contrôleur de domaine dans l’énumération est récupéré.</span><span class="sxs-lookup"><span data-stu-id="9842b-112">The first time this function is called, the first domain controller in the enumeration is retrieved.</span></span> <span data-ttu-id="9842b-113">La deuxième fois que cette fonction est appelée, le deuxième contrôleur de domaine de l’énumération est récupéré.</span><span class="sxs-lookup"><span data-stu-id="9842b-113">The second time this function is called, the second domain controller in the enumeration is retrieved.</span></span> <span data-ttu-id="9842b-114">Ce processus est répété jusqu’à ce que **DsGetDcNext** retourne l' **erreur \_ aucun \_ autre \_ élément**, ce qui indique la fin de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="9842b-114">This process is repeated until **DsGetDcNext** returns **ERROR\_NO\_MORE\_ITEMS**, that indicates the end of the enumeration.</span></span>

<span data-ttu-id="9842b-115">La fonction [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) énumère les contrôleurs de domaine dans deux groupes.</span><span class="sxs-lookup"><span data-stu-id="9842b-115">The [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) function will enumerate the domain controllers in two groups.</span></span> <span data-ttu-id="9842b-116">Le premier groupe contient les contrôleurs de domaine qui couvrent le site de l’ordinateur sur lequel la fonction est exécutée et le deuxième groupe contient les contrôleurs de domaine qui ne couvrent pas le site de l’ordinateur sur lequel la fonction est exécutée.</span><span class="sxs-lookup"><span data-stu-id="9842b-116">The first group contains the domain controllers that cover the site of the computer where the function is executed and the second group contains the domain controllers that do not cover the site of the computer where the function is executed.</span></span> <span data-ttu-id="9842b-117">Si l' **indicateur \_ DS Notify après les \_ \_ \_ enregistrements de site** est spécifié dans le paramètre *OptionFlags* dans [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena), la fonction **DsGetDcNext** retourne une marque d' **erreur \_ \_ détectée** après que tous les contrôleurs de domaine spécifiques au site ont été récupérés.</span><span class="sxs-lookup"><span data-stu-id="9842b-117">If the **DS\_NOTIFY\_AFTER\_SITE\_RECORDS** flag is specified in the *OptionFlags* parameter in [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena), the **DsGetDcNext** function will return **ERROR\_FILEMARK\_DETECTED** after all of the site-specific domain controllers have been retrieved.</span></span> <span data-ttu-id="9842b-118">**DsGetDcNext** commencera par énumérer le deuxième groupe, qui contient tous les contrôleurs de domaine du domaine, y compris les contrôleurs de domaine spécifiques au site contenus dans le premier groupe.</span><span class="sxs-lookup"><span data-stu-id="9842b-118">**DsGetDcNext** will then begin enumerating the second group, which contains all domain controllers in the domain, including the site-specific domain controllers contained in the first group.</span></span>

<span data-ttu-id="9842b-119">Les contrôleurs de domaine qui gèrent le site de l’ordinateur sur lequel la fonction est exécutée sont répertoriés en premier, suivis des contrôleurs de domaine qui ne couvrent pas le site de l’ordinateur sur lequel la fonction est exécutée.</span><span class="sxs-lookup"><span data-stu-id="9842b-119">Domain controllers that handle the site of the computer where the function is executed are enumerated first followed by the domain controllers that do not cover the site of the computer where the function is executed.</span></span> <span data-ttu-id="9842b-120">Un contrôleur de domaine est considéré comme un site si le contrôleur de domaine est configuré pour résider dans ce site ou si le contrôleur de domaine se trouve dans un site le plus proche du site en question en termes de coût de liaison inter-site configuré.</span><span class="sxs-lookup"><span data-stu-id="9842b-120">A domain controller is said to cover a site if the domain controller is configured to reside in that site or if the domain controller resides in a site that is nearest to the site in question in terms of the configured inter-site link cost.</span></span> <span data-ttu-id="9842b-121">S’il existe des contrôleurs de domaine dans le groupe de contrôleurs de domaine qui couvrent et le groupe de contrôleurs de domaine qui ne couvrent pas le site de l’ordinateur, les contrôleurs de domaine sont retournés dans le groupe dans l’ordre des priorités et des poids configurés dans DNS.</span><span class="sxs-lookup"><span data-stu-id="9842b-121">If there are any domain controllers in both the group of domain controllers that cover and the group of domain controllers that do not cover the computer site, domain controllers are returned within the group in order of their configured priorities and weights that are specified in DNS.</span></span> <span data-ttu-id="9842b-122">Les contrôleurs de domaine qui ont une priorité numérique inférieure sont retournés dans un groupe en premier.</span><span class="sxs-lookup"><span data-stu-id="9842b-122">Domain controllers that have lower numeric priority are returned within a group first.</span></span> <span data-ttu-id="9842b-123">Si, dans un groupe lié à un site, il existe un sous-groupe de plusieurs contrôleurs de domaine avec la même priorité, les contrôleurs de domaine sont retournés dans un ordre aléatoire pondéré dans lequel les contrôleurs de domaine avec une pondération plus élevée ont plus de probabilité d’être renvoyés en premier.</span><span class="sxs-lookup"><span data-stu-id="9842b-123">If within a site-related group there is a subgroup of several domain controllers with the same priority, domain controllers are returned in a weighted random order where domain controllers with higher weight have more probability to be returned first.</span></span> <span data-ttu-id="9842b-124">Les sites, les priorités et les pondérations sont configurés par l’administrateur de domaine pour obtenir des performances et un équilibrage de charge efficaces entre plusieurs contrôleurs de domaine disponibles dans le domaine.</span><span class="sxs-lookup"><span data-stu-id="9842b-124">The sites, priorities, and weights are configured by the domain administrator to achieve effective performance and load balancing among multiple domain controllers available in the domain.</span></span> <span data-ttu-id="9842b-125">Pour cette raison, les applications qui utilisent les fonctions [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena) / [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) / [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) tirent automatiquement parti de ces optimisations.</span><span class="sxs-lookup"><span data-stu-id="9842b-125">Because of this, applications that use the [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena)/[**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta)/[**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) functions automatically take advantage of these optimizations.</span></span>

<span data-ttu-id="9842b-126">Lorsque l’énumération est terminée ou n’est plus nécessaire, l’énumération doit être fermée en appelant [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) avec le handle de contexte d’énumération de domaine.</span><span class="sxs-lookup"><span data-stu-id="9842b-126">When the enumeration is complete or is no longer required, the enumeration must be closed by calling [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) with the domain enumeration context handle.</span></span>

<span data-ttu-id="9842b-127">Pour réinitialiser l’énumération, il est nécessaire de fermer l’énumération actuelle en appelant [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) , puis de rouvrir l’énumération en appelant à nouveau [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena) .</span><span class="sxs-lookup"><span data-stu-id="9842b-127">To reset the enumeration, it is necessary to close the current enumeration by calling [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) and then reopen the enumeration by calling [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena) again.</span></span>

## <a name="example"></a><span data-ttu-id="9842b-128">Exemple</span><span class="sxs-lookup"><span data-stu-id="9842b-128">Example</span></span>

<span data-ttu-id="9842b-129">L’exemple de code suivant montre comment utiliser ces fonctions pour énumérer les contrôleurs de domaine dans le domaine local.</span><span class="sxs-lookup"><span data-stu-id="9842b-129">The following code example shows how to use these functions to enumerate the domain controllers in the local domain.</span></span>


```C++
DWORD dwRet;
PDOMAIN_CONTROLLER_INFO pdcInfo;

// Get a domain controller for the domain this computer is on.
dwRet = DsGetDcName(NULL, NULL, NULL, NULL, 0, &pdcInfo);
if(ERROR_SUCCESS == dwRet)
{
    HANDLE hGetDc;
    
    // Open the enumeration.
    dwRet = DsGetDcOpen(    pdcInfo->DomainName,
                            DS_NOTIFY_AFTER_SITE_RECORDS,
                            NULL,
                            NULL,
                            NULL,
                            0,
                            &hGetDc);
    if(ERROR_SUCCESS == dwRet)
    {
        LPTSTR pszDnsHostName;

        /*
        Enumerate each domain controller and print its name to the 
        debug window.
        */
        while(TRUE)
        {
            ULONG ulSocketCount;
            LPSOCKET_ADDRESS rgSocketAddresses;

            dwRet = DsGetDcNext(
                hGetDc, 
                &ulSocketCount, 
                &rgSocketAddresses, 
                &pszDnsHostName);
            
            if(ERROR_SUCCESS == dwRet)
            {
                OutputDebugString(pszDnsHostName);
                OutputDebugString(TEXT("\n"));
                
                // Free the allocated string.
                NetApiBufferFree(pszDnsHostName);

                // Free the socket address array.
                LocalFree(rgSocketAddresses);
            }
            else if(ERROR_NO_MORE_ITEMS == dwRet)
            {
                // The end of the list has been reached.
                break;
            }
            else if(ERROR_FILEMARK_DETECTED == dwRet)
            {
                /*
                DS_NOTIFY_AFTER_SITE_RECORDS was specified in 
                DsGetDcOpen and the end of the site-specific 
                records was reached.
                */
                OutputDebugString(
                  TEXT("End of site-specific domain controllers\n"));
                continue;
            }
            else
            {
                // Some other error occurred.
                break;
            }
        }
        
        // Close the enumeration.
        DsGetDcClose(hGetDc);
    }
    
    // Free the DOMAIN_CONTROLLER_INFO structure. 
    NetApiBufferFree(pdcInfo);
}
```



 

 




