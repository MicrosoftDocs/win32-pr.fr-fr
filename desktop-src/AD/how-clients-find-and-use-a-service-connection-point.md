---
title: Comment les clients recherchent et utilisent un point de connexion de service
description: L’exemple de code suivant montre comment une application cliente recherche un point de connexion de service (SCP) dans le catalogue global.
ms.assetid: d3163c22-22fe-4606-8cad-6f3a87f8fc36
ms.tgt_platform: multiple
keywords:
- points de connexion de service Active Directory, comment les clients recherchent et utilisent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edf75a0002f9351903ed1c5eca79f498cb4a078d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462858"
---
# <a name="how-clients-find-and-use-a-service-connection-point"></a><span data-ttu-id="8d611-104">Comment les clients recherchent et utilisent un point de connexion de service</span><span class="sxs-lookup"><span data-stu-id="8d611-104">How Clients Find and Use a Service Connection Point</span></span>

<span data-ttu-id="8d611-105">L’exemple de code suivant montre comment une application cliente recherche un point de connexion de service (SCP) dans le catalogue global.</span><span class="sxs-lookup"><span data-stu-id="8d611-105">The following code example shows how a client application searches the Global Catalog for a Service Connection Point (SCP).</span></span> <span data-ttu-id="8d611-106">Dans cet exemple de code, l’application cliente a une chaîne GUID codée en dur qui identifie le service.</span><span class="sxs-lookup"><span data-stu-id="8d611-106">In this code example, the client application has a hard-coded GUID string that identifies the service.</span></span> <span data-ttu-id="8d611-107">Le programme d’installation du service a stocké la même chaîne GUID comme l’une des valeurs de l’attribut des **Mots clés** SCP à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="8d611-107">The service installer stored the same GUID string as one of the values of the SCPs multi-value **keywords** attribute.</span></span>

<span data-ttu-id="8d611-108">Cet exemple se compose de deux routines.</span><span class="sxs-lookup"><span data-stu-id="8d611-108">This sample consists of two routines.</span></span> <span data-ttu-id="8d611-109">La routine **GetGC** récupère un pointeur [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) pour un catalogue global (GC).</span><span class="sxs-lookup"><span data-stu-id="8d611-109">The **GetGC** routine retrieves an [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) pointer for a Global Catalog (GC).</span></span> <span data-ttu-id="8d611-110">La routine **ScpLocate** utilise les méthodes **IDirectorySearch** pour effectuer une recherche dans le gc.</span><span class="sxs-lookup"><span data-stu-id="8d611-110">The **ScpLocate** routine uses the **IDirectorySearch** methods to search the GC.</span></span>

<span data-ttu-id="8d611-111">Le catalogue global contient un réplica partiel de chaque objet de la forêt, mais ne contient pas tous les attributs SCP requis par le client.</span><span class="sxs-lookup"><span data-stu-id="8d611-111">The GC contains a partial replica of every object in the forest, but does not contain all of the SCP attributes that the client requires.</span></span> <span data-ttu-id="8d611-112">Tout d’abord, le client doit effectuer une recherche dans le GC pour trouver le SCP et récupérer son DN.</span><span class="sxs-lookup"><span data-stu-id="8d611-112">First, the client must search the GC to find the SCP and retrieve its DN.</span></span> <span data-ttu-id="8d611-113">Le client utilise ensuite le DN du SCP pour établir une liaison avec un pointeur [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) sur le SCP.</span><span class="sxs-lookup"><span data-stu-id="8d611-113">Then the client uses the SCP's DN to bind to an [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) pointer on the SCP.</span></span> <span data-ttu-id="8d611-114">Le client appelle ensuite la méthode [**IDirectoryObject :: GetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) pour récupérer le reste des attributs.</span><span class="sxs-lookup"><span data-stu-id="8d611-114">The client then calls the [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) method to retrieve the rest of the attributes.</span></span>


```C++
//***************************************************************************
//
//  ScpLocate()
//
//  All strings returned by ScpLocate must be freed by the caller using 
//  FreeADsStr after it is finished using them.
//
//***************************************************************************

DWORD ScpLocate (
    LPWSTR *ppszDN,                  // Returns distinguished name of SCP.
    LPWSTR *ppszServiceDNSName,      // Returns service DNS name.
    LPWSTR *ppszServiceDNSNameType,  // Returns type of DNS name.
    LPWSTR *ppszClass,               // Returns name of service class.
    USHORT *pusPort)                 // Returns service port.
{
    HRESULT hr;
    IDirectoryObject *pSCP = NULL;
    ADS_ATTR_INFO *pPropEntries = NULL;
    IDirectorySearch *pSearch = NULL;
    ADS_SEARCH_HANDLE hSearch = NULL;

    // Get an IDirectorySearch pointer for the Global Catalog. 
    hr = GetGCSearch(&pSearch);
    if (FAILED(hr)) 
    {
        fprintf(stderr,"GetGC failed 0x%x",hr);
        goto Cleanup;
    }

    // Set up a deep search.
    // Thousands of objects are not expected in this example, therefore
    // query for 1000 rows per page.
    ADS_SEARCHPREF_INFO SearchPref[2];
    DWORD dwPref = sizeof(SearchPref)/sizeof(ADS_SEARCHPREF_INFO);
    SearchPref[0].dwSearchPref =    ADS_SEARCHPREF_SEARCH_SCOPE;
    SearchPref[0].vValue.dwType =   ADSTYPE_INTEGER;
    SearchPref[0].vValue.Integer =  ADS_SCOPE_SUBTREE;

    SearchPref[1].dwSearchPref =    ADS_SEARCHPREF_PAGESIZE;
    SearchPref[1].vValue.dwType =   ADSTYPE_INTEGER;
    SearchPref[1].vValue.Integer =  1000;

    hr = pSearch->SetSearchPreference(SearchPref, dwPref);
    fprintf (stderr, "SetSearchPreference: 0x%x\n", hr);
    if (FAILED(hr))
    {
        fprintf (stderr, "Failed to set search prefs: hr:0x%x\n", hr);
        goto Cleanup;
    } 

    // Execute the search. From the GC get the distinguished name 
    // of the SCP. Use the DN to bind to the SCP and get the other 
    // properties.
    LPWSTR rgszDN[] = {L"distinguishedName"};

    // Search for a match of the product GUID.
    hr = pSearch->ExecuteSearch(    L"keywords=A762885A-AA44-11d2-81F1-00C04FB9624E",
                                    rgszDN,
                                    1,
                                    &hSearch);

    fprintf (stderr, "ExecuteSearch: 0x%x\n", hr);

    if (FAILED(hr)) 
    {
        fprintf (stderr, "ExecuteSearch failed: hr:0x%x\n", hr);
        goto Cleanup;
    } 

    // Loop through the results. Each row should be an instance of the 
    // service identified by the product GUID.
    // Add logic to select from multiple service instances.
    hr = pSearch->GetNextRow(hSearch);
    if (SUCCEEDED(hr) && hr !=S_ADS_NOMORE_ROWS) 
    {
        ADS_SEARCH_COLUMN Col;

        hr = pSearch->GetColumn(hSearch, L"distinguishedName", &Col);
        *ppszDN = AllocADsStr(Col.pADsValues->CaseIgnoreString);
        pSearch->FreeColumn(&Col);
        hr = pSearch->GetNextRow(hSearch);
    }

    // Bind to the DN to get the other properties.
    LPWSTR lpszLDAPPrefix = L"LDAP://";
    DWORD dwSCPPathLength = wcslen(lpszLDAPPrefix) + wcslen(*ppszDN) + 1;
    LPWSTR pwszSCPPath = new WCHAR[dwSCPPathLength];
    if(pwszSCPPath)
    {
        wcscpy_s(pwszSCPPath, lpszLDAPPrefix);
        wcscat_s(pwszSCPPath, *ppszDN);
    }       
    else
    {
        fprintf(stderr,"Failed to allocate a buffer");
        goto Cleanup;
    }               

    hr = ADsGetObject(  pwszSCPPath,
                        IID_IDirectoryObject,
                        (void**)&pSCP);

    // Free the string buffer
    delete pwszSCPPath;

    if (SUCCEEDED(hr)) 
    {
        // Properties to retrieve from the SCP object.
        LPWSTR rgszAttribs[]=
        {
            {L"serviceClassName"},
            {L"serviceDNSName"},
            {L"serviceDNSNameType"},
            {L"serviceBindingInformation"}
        };

        DWORD dwAttrs = sizeof(rgszAttribs)/sizeof(LPWSTR);
        DWORD dwNumAttrGot;
        hr = pSCP->GetObjectAttributes( rgszAttribs,
                                        dwAttrs,
                                        &pPropEntries,
                                        &dwNumAttrGot);
        if(FAILED(hr)) 
        {
            fprintf (stderr, "GetObjectAttributes Failed. hr:0x%x\n", hr);
            goto Cleanup;
        }

        // Loop through the entries returned by GetObjectAttributes 
        // and save the values in the appropriate buffers. 
        for (int i = 0; i < (LONG)dwAttrs; i++) 
        {
            if ((wcscmp(L"serviceDNSName", pPropEntries[i].pszAttrName)==0) &&
                (pPropEntries[i].dwADsType == ADSTYPE_CASE_IGNORE_STRING)) 
            {
                *ppszServiceDNSName = AllocADsStr(pPropEntries[i].pADsValues->CaseIgnoreString);
            }

            if ((wcscmp(L"serviceDNSNameType", pPropEntries[i].pszAttrName)==0) &&
                (pPropEntries[i].dwADsType == ADSTYPE_CASE_IGNORE_STRING)) 
            {
                *ppszServiceDNSNameType = AllocADsStr(pPropEntries[i].pADsValues->CaseIgnoreString);
            }

            if ((wcscmp(L"serviceClassName", pPropEntries[i].pszAttrName)==0) &&
                (pPropEntries[i].dwADsType == ADSTYPE_CASE_IGNORE_STRING)) 
            {
                *ppszClass = AllocADsStr(pPropEntries[i].pADsValues->CaseIgnoreString);
            }

            if ((wcscmp(L"serviceBindingInformation", pPropEntries[i].pszAttrName)==0) &&
                (pPropEntries[i].dwADsType == ADSTYPE_CASE_IGNORE_STRING)) 
            {
                *pusPort=(USHORT)_wtoi(pPropEntries[i].pADsValues->CaseIgnoreString);
            }
        }
    }

Cleanup:
    if (pSCP) 
    {
        pSCP->Release();
        pSCP = NULL;
    }

    if (pPropEntries)
    {
        FreeADsMem(pPropEntries);
        pPropEntries = NULL;
    }

    if (pSearch)
    {
        if (hSearch)
        {
            pSearch->CloseSearchHandle(hSearch);
            hSearch = NULL;
        }
        
        pSearch->Release();
        pSearch = NULL;
    }

    return hr;
}

//***************************************************************************
//
//  GetGCSearch()
//
//  Retrieves an IDirectorySearch pointer for a Global Catalog (GC)
//
//***************************************************************************

HRESULT GetGCSearch(IDirectorySearch **ppDS)
{
    HRESULT hr;
    IEnumVARIANT *pEnum = NULL;
    IADsContainer *pCont = NULL;
    IDispatch *pDisp = NULL;
    VARIANT var;
    ULONG lFetch;

    *ppDS = NULL;

    // Bind to the GC: namespace container object. The true GC DN 
    // is a single immediate child of the GC: namespace, which must 
    // be obtained using enumeration.
    hr = ADsOpenObject( L"GC:",
                        NULL,
                        NULL,
                        ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
                        IID_IADsContainer,
                        (void**)&pCont);
    if (FAILED(hr)) 
    {
        _tprintf(TEXT("ADsOpenObject failed: 0x%x\n"), hr);
        goto cleanup;
    } 

    // Get an enumeration interface for the GC container. 
    hr = ADsBuildEnumerator(pCont, &pEnum);
    if (FAILED(hr)) 
    {
        _tprintf(TEXT("ADsBuildEnumerator failed: 0x%x\n"), hr);
        goto cleanup;
    } 

    // Now enumerate. There is only one child of the GC: object.
    hr = ADsEnumerateNext(pEnum, 1, &var, &lFetch);
    if (FAILED(hr)) 
    {
        _tprintf(TEXT("ADsEnumerateNext failed: 0x%x\n"), hr);
        goto cleanup;
    } 

    if ((hr == S_OK) && (lFetch == 1))
    {
        pDisp = V_DISPATCH(&var);
        hr = pDisp->QueryInterface( IID_IDirectorySearch, (void**)ppDS); 
    }

cleanup:
    if (pEnum)
    {
        ADsFreeEnumerator(pEnum);
        pEnum = NULL;
    }

    if (pCont)
    {
        pCont->Release();
        pCont = NULL;
    }
    
    if (pDisp)
    {
        pDisp->Release();
        pDisp = NULL;
    }

    return hr;
}
```



 

 