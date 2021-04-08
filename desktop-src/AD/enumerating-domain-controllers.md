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
# <a name="enumerating-domain-controllers"></a>Énumération des contrôleurs de domaine

Dans les versions antérieures de Windows, une application pouvait uniquement obtenir un contrôleur de domaine unique dans un domaine en appelant [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea). Il n’existait aucun moyen de prédire quel contrôleur de domaine serait récupéré ou d’obtenir une liste des contrôleurs de domaine. Windows permet à une application d’énumérer les contrôleurs de domaine dans un domaine à l’aide des fonctions [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena), [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta)et [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) .

Pour énumérer un contrôleur de domaine, appelez [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena). Cette fonction accepte les paramètres qui définissent le domaine à énumérer et d’autres options d’énumération. **DsGetDcOpen** fournit un handle de contexte d’énumération de domaine qui est utilisé pour identifier l’opération d’énumération lorsque [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) et [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) sont appelés.

La fonction [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) est appelée avec le handle de contexte d’énumération de domaine pour récupérer le contrôleur de domaine suivant dans l’énumération. La première fois que cette fonction est appelée, le premier contrôleur de domaine dans l’énumération est récupéré. La deuxième fois que cette fonction est appelée, le deuxième contrôleur de domaine de l’énumération est récupéré. Ce processus est répété jusqu’à ce que **DsGetDcNext** retourne l' **erreur \_ aucun \_ autre \_ élément**, ce qui indique la fin de l’énumération.

La fonction [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) énumère les contrôleurs de domaine dans deux groupes. Le premier groupe contient les contrôleurs de domaine qui couvrent le site de l’ordinateur sur lequel la fonction est exécutée et le deuxième groupe contient les contrôleurs de domaine qui ne couvrent pas le site de l’ordinateur sur lequel la fonction est exécutée. Si l' **indicateur \_ DS Notify après les \_ \_ \_ enregistrements de site** est spécifié dans le paramètre *OptionFlags* dans [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena), la fonction **DsGetDcNext** retourne une marque d' **erreur \_ \_ détectée** après que tous les contrôleurs de domaine spécifiques au site ont été récupérés. **DsGetDcNext** commencera par énumérer le deuxième groupe, qui contient tous les contrôleurs de domaine du domaine, y compris les contrôleurs de domaine spécifiques au site contenus dans le premier groupe.

Les contrôleurs de domaine qui gèrent le site de l’ordinateur sur lequel la fonction est exécutée sont répertoriés en premier, suivis des contrôleurs de domaine qui ne couvrent pas le site de l’ordinateur sur lequel la fonction est exécutée. Un contrôleur de domaine est considéré comme un site si le contrôleur de domaine est configuré pour résider dans ce site ou si le contrôleur de domaine se trouve dans un site le plus proche du site en question en termes de coût de liaison inter-site configuré. S’il existe des contrôleurs de domaine dans le groupe de contrôleurs de domaine qui couvrent et le groupe de contrôleurs de domaine qui ne couvrent pas le site de l’ordinateur, les contrôleurs de domaine sont retournés dans le groupe dans l’ordre des priorités et des poids configurés dans DNS. Les contrôleurs de domaine qui ont une priorité numérique inférieure sont retournés dans un groupe en premier. Si, dans un groupe lié à un site, il existe un sous-groupe de plusieurs contrôleurs de domaine avec la même priorité, les contrôleurs de domaine sont retournés dans un ordre aléatoire pondéré dans lequel les contrôleurs de domaine avec une pondération plus élevée ont plus de probabilité d’être renvoyés en premier. Les sites, les priorités et les pondérations sont configurés par l’administrateur de domaine pour obtenir des performances et un équilibrage de charge efficaces entre plusieurs contrôleurs de domaine disponibles dans le domaine. Pour cette raison, les applications qui utilisent les fonctions [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena) / [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) / [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) tirent automatiquement parti de ces optimisations.

Lorsque l’énumération est terminée ou n’est plus nécessaire, l’énumération doit être fermée en appelant [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) avec le handle de contexte d’énumération de domaine.

Pour réinitialiser l’énumération, il est nécessaire de fermer l’énumération actuelle en appelant [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) , puis de rouvrir l’énumération en appelant à nouveau [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena) .

## <a name="example"></a>Exemple

L’exemple de code suivant montre comment utiliser ces fonctions pour énumérer les contrôleurs de domaine dans le domaine local.


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



 

 




