---
title: Exemple de code pour la localisation d’un serveur hôte de partition d’annuaire d’applications
description: Cette rubrique contient un exemple de code qui localise un serveur hôte de partition d’annuaire d’applications.
ms.assetid: c161323b-13ce-4986-8b24-b459009ff53c
ms.tgt_platform: multiple
keywords:
- Exemple de code pour localiser un serveur hôte de partition d’annuaire d’applications AD
- Partition de l’annuaire d’applications Active Directory, exemple de code pour localiser un serveur hôte de partition d’annuaire d’applications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03d7a218acf3608c18587b7d9b9c82779f17fd6eb251608a86d99d8acb3b7bd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118693598"
---
# <a name="example-code-for-locating-an-application-directory-partition-host-server"></a>Exemple de code pour la localisation d’un serveur hôte de partition d’annuaire d’applications

Cette rubrique contient un exemple de code qui localise un serveur hôte de partition d’annuaire d’applications.

L’exemple de code C/C++ suivant montre comment utiliser la fonction [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea) pour localiser un contrôleur de domaine qui héberge un réplica d’une partition d’annuaire d’applications. Cet exemple de code montre également comment utiliser la fonction [**DsCrackNames**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dscracknamesa) pour convertir le nom unique d’une partition d’annuaire d’applications en un nom DNS.


```C++
/***************************************************************************

    AppPartitionDNToDNS()

    Converts the distinguished name of an application directory partition to 
    a DNS name for the partition.

    The caller must free the memory allocated to ppszDNS by calling 
    FreeADsMem when it is no longer required.

***************************************************************************/

DWORD AppPartitionDNToDNS(LPCTSTR pszDN, LPTSTR *ppszDNS)
{   
    DWORD dwRet;
    LPCTSTR rgpszNames[] = {pszDN};
    PDS_NAME_RESULT pResults;

    /*
    Convert the distinguished name to a DNS name using only syntactic 
    mapping. The DS_NAME_FLAG_SYNTACTICAL_ONLY flag allows DsCrackNames to 
    be called without binding.
    */
    dwRet = DsCrackNames(NULL, 
        DS_NAME_FLAG_SYNTACTICAL_ONLY,
        DS_FQDN_1779_NAME,
        DS_CANONICAL_NAME,
        1,
        rgpszNames,
        &pResults);

    if(NO_ERROR == dwRet)
    {
        /*
        Allocate the memory and copy the DNS name of the partition.
        */
        DWORD dwBytes = (lstrlen(pResults->rItems[0].pDomain) + 1) * sizeof(TCHAR);
        *ppszDNS = (LPTSTR)AllocADsMem(dwBytes);
        if(*ppszDNS)
        {
            wcsncpy_s(*ppszDNS, pResults->rItems[0].pDomain, dwBytes);

            dwRet = NO_ERROR;
        }
        else
        {
            dwRet = ERROR_NOT_ENOUGH_MEMORY;
        }
        
        // Free the result set.
        DsFreeNameResult(pResults);
    }
    
    return dwRet;
}

/***************************************************************************

    PrintDCFromAppPartition()

    Given the distinguished name of an application directory partition, 
    prints to the console the DNS name of a domain controller that hosts a 
    replica of the application directory partition.

***************************************************************************/

DWORD PrintDCFromAppPartition(LPCTSTR pszAppPartitionDN)
{
    DWORD dwRet;

    /*
    Convert the distinguished name of the partition to a DNS name so that 
    the DNS name can be passed to DsGetDcName.
    */
    LPTSTR pszDNS;
    dwRet = AppPartitionDNToDNS(pszAppPartitionDN, &pszDNS);
    if(NO_ERROR == dwRet)
    {
        PDOMAIN_CONTROLLER_INFO pdci;

        /*
        Get the name of a domain controller that hosts a replica of the 
        application directory partition.
        */
        dwRet = DsGetDcName(NULL, 
            pszDNS, 
            NULL, 
            NULL, 
            DS_ONLY_LDAP_NEEDED, 
            &pdci);

        if(NO_ERROR == dwRet)
        {
            // Print the DNS name of the domain controller.
            _tprintf(pdci->DomainControllerName);
            
            NetApiBufferFree(pdci);
        }

        FreeADsMem(pszDNS);
    }

    return dwRet;
}
```



 

 




