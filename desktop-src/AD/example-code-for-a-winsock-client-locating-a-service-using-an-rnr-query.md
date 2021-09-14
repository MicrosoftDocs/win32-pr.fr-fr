---
title: Exemple de code pour la localisation d’un service à l’aide d’une requête RnR
description: L’exemple de code suivant localise l’exemple de service Winsock et s’y connecte.
ms.assetid: c05c7f69-d510-4feb-b426-1ae3a3ed5e16
ms.tgt_platform: multiple
keywords:
- Exemple de code pour la localisation d’un service à l’aide d’une AD de requête RnR
- Windows Inscription et résolution des sockets Active Directory, exemple de code, localisation d’un service à l’aide d’une requête RnR
- Recherche d’un service à l’aide d’une requête RnR AD, exemple de code
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee1202c981de8b4f1e0bd4f4299b1aabf1be520d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007701"
---
# <a name="example-code-for-locating-a-service-using-an-rnr-query"></a>Exemple de code pour la localisation d’un service à l’aide d’une requête RnR

L’exemple de code suivant localise l’exemple de service Winsock et s’y connecte.


```C++
#include "stdafx.h"
#include "shlobj.h"
#include "dsclient.h"


//  The PrintDomain() function displays the domain name.
void PrintDomain(DOMAINDESC *pDomainDesc, DWORD dwIndentLevel)
{
    DWORD i;
    
    // Display the domain name.
    for(i = 0; i < dwIndentLevel; i++)
    {
        wprintf(L"  ");
    }
    wprintf(pDomainDesc->pszName);
    wprintf(L"\n");
}

//  The WalkDomainTree() function prints the current domain name and walks the tree.
void WalkDomainTree(DOMAINDESC *pDomainDesc, DWORD dwIndentLevel = 0)
{
    DOMAINDESC  *pCurrent;

    // Walk through the current item and any siblings it may have.
    for(pCurrent = pDomainDesc; 
        NULL != pCurrent; 
        pCurrent = pCurrent->pdNextSibling)
    {
        // Print the current domain name.
        PrintDomain(pCurrent, dwIndentLevel);
        
        // Walk the child tree, if one exists.
        if(NULL != pCurrent->pdChildList)
        {
            WalkDomainTree(pCurrent->pdChildList, 
                dwIndentLevel + 1);
        }
    }
}

//  Entry point for the application.
int main(void)
{
    HRESULT hr;
    IDsBrowseDomainTree *pBrowseTree;
    CoInitialize(NULL);

    hr = CoCreateInstance(CLSID_DsDomainTreeBrowser,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IDsBrowseDomainTree,
                          (void**)&pBrowseTree);

    if(SUCCEEDED(hr))
    {
        DOMAINTREE  *pDomTreeStruct;

        hr = pBrowseTree->GetDomains(&pDomTreeStruct, 
                                     DBDTF_RETURNFQDN);
        if(SUCCEEDED(hr))
        {
            WalkDomainTree(&pDomTreeStruct->aDomains[0]);
            hr = pBrowseTree->FreeDomains(&pDomTreeStruct);
        }
        
        pBrowseTree->Release();
    }
    
    CoUninitialize();
}
```



 

 




