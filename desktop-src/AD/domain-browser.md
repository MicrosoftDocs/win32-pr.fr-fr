---
title: Explorateur de domaines
description: À l’aide de l’interface IDsBrowseDomainTree, une application peut afficher une boîte de dialogue de navigateur de domaine et obtenir le nom DNS du domaine sélectionné par l’utilisateur.
ms.assetid: 26793c61-469e-4e99-9056-b9fc04336b69
ms.tgt_platform: multiple
keywords:
- Explorateur de domaine AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b16bb932f14544902ab24e8fc1f50daa327bb705
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104031013"
---
# <a name="domain-browser"></a>Explorateur de domaines

À l’aide de l’interface [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) , une application peut afficher une boîte de dialogue de navigateur de domaine et obtenir le nom DNS du domaine sélectionné par l’utilisateur. Une application peut également utiliser l’interface **IDsBrowseDomainTree** pour obtenir des données sur toutes les arborescences de domaine et les domaines d’une forêt.

Une instance de l’interface [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) est créée en appelant [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) avec l’identificateur de classe **CLSID \_ DsDomainTreeBrowser** , comme indiqué ci-dessous.

La méthode [**IDsBrowseDomainTree :: SetComputer**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-setcomputer) peut être utilisée pour spécifier l’ordinateur et les informations d’identification utilisés comme base pour la récupération des données de domaine. Quand **SetComputer** est appelé sur une instance [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) particulière, [**IDsBrowseDomainTree :: FlushCachedDomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-flushcacheddomains) doit être appelé avant que **SetComputer** soit appelé à nouveau.

La méthode [**IDsBrowseDomainTree :: consulter**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-browseto) est utilisée pour afficher la boîte de dialogue Explorateur de domaines. Lorsque l’utilisateur sélectionne un domaine et clique sur le bouton **OK** , **IDsBrowseDomainTree :: consulter** retourne **S \_ OK** et le paramètre *ppszTargetPath* contient le nom du domaine sélectionné. Lorsque la chaîne de nom n’est plus requise, l’appelant doit libérer la chaîne en appelant [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).

L’exemple de code suivant montre comment utiliser l’interface [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) pour afficher la boîte de dialogue Explorateur de domaines.


```C++
#include <shlobj.h>
#include <dsclient.h>

void main(void)
{
    HRESULT     hr;

    hr = CoInitialize(NULL);
    if(FAILED(hr)) 
    {
        return;
    }

    IDsBrowseDomainTree *pDsDomains = NULL;

    hr = ::CoCreateInstance(    CLSID_DsDomainTreeBrowser,
                                NULL,
                                CLSCTX_INPROC_SERVER,
                                IID_IDsBrowseDomainTree,
                                (void **)(&pDsDomains));
    
    if(SUCCEEDED(hr))
    {
        LPOLESTR    pstr;        

        hr = pDsDomains->BrowseTo(  GetDesktopWindow(),
                                    &pstr,
                                    0);
        
        if(S_OK == hr)
        {
            wprintf(pstr);
            wprintf(L"\n");
            CoTaskMemFree(pstr);
        }

        pDsDomains->Release();
    }

    CoUninitialize();
}
```



La méthode [**IDsBrowseDomainTree :: GetDomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains) est utilisée pour obtenir les données de l’arborescence de domaine. Les données de domaine sont fournies dans une structure [**DOMAINTREE**](/windows/desktop/api/Dsclient/ns-dsclient-domain_tree) . La structure **DOMAINTREE** contient la taille de la structure et le nombre d’éléments de domaine dans l’arborescence. La structure **DOMAINTREE** contient également une ou plusieurs structures [**DOMAINDESC**](/windows/desktop/api/Dsclient/ns-dsclient-domaindesc) . Le **DOMAINDESC** contient des données relatives à un élément unique dans l’arborescence de domaine, y compris les données enfants et frères. Les frères d’un domaine peuvent être énumérées en accédant au membre **pdNextSibling** de chaque structure **DOMAINDESC** suivante. Les enfants du domaine peuvent être récupérés de la même manière en accédant au membre **pdChildList** de chaque structure **DOMAINDESC** suivante.

L’exemple de code suivant montre comment obtenir les données de l’arborescence de domaine et y accéder à l’aide de la méthode [**IDsBrowseDomainTree :: GetDomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains) .


```C++
//  Add dsuiext.lib to the project.

#include "stdafx.h"
#include <shlobj.h>
#include <dsclient.h>

//The PrintDomain() function displays the domain name
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

//The WalkDomainTree() function traverses the domain tree and prints the current domain name
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

//  Entry point for application
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



 

 