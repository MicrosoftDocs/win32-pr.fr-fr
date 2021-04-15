---
title: Énumération des réplicas d’un service
description: Cette rubrique contient un exemple de code qui énumère les instances installées d’un service répliqué sur différents ordinateurs hôtes dans une entreprise.
ms.assetid: 9dc3f932-c3e1-4ce1-a945-12d68838304e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 995cd665476a55b6bf717f356fafa54b0d2e10e6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104507862"
---
# <a name="enumerating-the-replicas-of-a-service"></a><span data-ttu-id="c603b-103">Énumération des réplicas d’un service</span><span class="sxs-lookup"><span data-stu-id="c603b-103">Enumerating the Replicas of a Service</span></span>

<span data-ttu-id="c603b-104">Cette rubrique contient un exemple de code qui énumère les instances installées d’un service répliqué sur différents ordinateurs hôtes dans une entreprise.</span><span class="sxs-lookup"><span data-stu-id="c603b-104">This topic includes a code example that enumerates the installed instances of a replicated service on different host computers throughout an enterprise.</span></span> <span data-ttu-id="c603b-105">Pour modifier le mot de passe du compte de service pour chaque instance d’un service répliqué, utilisez cet exemple de code conjointement avec l’exemple de code dans la rubrique [modification du mot de passe du compte d’utilisateur d’un service](changing-the-password-on-a-serviceampaposs-user-account.md) .</span><span class="sxs-lookup"><span data-stu-id="c603b-105">To change the service account password for each instance of a replicated service, use this code example in conjunction with the code example in the [Changing the Password on a Service's User Account](changing-the-password-on-a-serviceampaposs-user-account.md) topic.</span></span>

<span data-ttu-id="c603b-106">L’exemple de code suppose que chaque instance de service a son propre objet de point de connexion de service (SCP) dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="c603b-106">The code example assumes that each service instance has its own service connection point (SCP) object in the directory.</span></span> <span data-ttu-id="c603b-107">Un SCP est un objet de la classe [**serviceConnectionPoint**](/windows/desktop/ADSchema/c-serviceconnectionpoint) .</span><span class="sxs-lookup"><span data-stu-id="c603b-107">An SCP is an object of the [**serviceConnectionPoint**](/windows/desktop/ADSchema/c-serviceconnectionpoint) class.</span></span> <span data-ttu-id="c603b-108">Cette classe possède un attribut **Keywords** , qui est un attribut à valeurs multiples répliqué sur chaque catalogue global (GC) de la forêt.</span><span class="sxs-lookup"><span data-stu-id="c603b-108">This class has a **keywords** attribute, which is a multi-valued attribute replicated to each global catalog (GC) in the forest.</span></span> <span data-ttu-id="c603b-109">L’attribut **Keywords** du SCP de chaque instance contient le GUID du produit du service.</span><span class="sxs-lookup"><span data-stu-id="c603b-109">The **keywords** attribute of each instance's SCP contains the service's product GUID.</span></span> <span data-ttu-id="c603b-110">Cela permet de trouver tous les SCP pour les différentes instances de service en recherchant dans un GC des objets avec un attribut de **Mots clés** qui est égal au GUID du produit.</span><span class="sxs-lookup"><span data-stu-id="c603b-110">This enables finding all of the SCPs for the various service instances by searching a GC for objects with a **keywords** attribute that equals the product GUID.</span></span>

<span data-ttu-id="c603b-111">L’exemple de code obtient un pointeur [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) vers un GC et utilise la méthode [**IDirectorySearch :: ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) pour rechercher le SCP.</span><span class="sxs-lookup"><span data-stu-id="c603b-111">The code example obtains an [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) pointer to a GC, and uses the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) method to search for the SCPs.</span></span> <span data-ttu-id="c603b-112">N’oubliez pas que le catalogue global contient un réplica partiel pour chaque SCP.</span><span class="sxs-lookup"><span data-stu-id="c603b-112">Be aware that the GC contains a partial replica for each SCP.</span></span> <span data-ttu-id="c603b-113">Autrement dit, il contient certains des attributs SCP, mais pas tous.</span><span class="sxs-lookup"><span data-stu-id="c603b-113">That is, it contains some of the SCP attributes, but not all.</span></span> <span data-ttu-id="c603b-114">Dans cet exemple de code, concentrez-vous sur l’attribut **servicednsname** , qui contient le nom DNS du serveur hôte pour cette instance de service.</span><span class="sxs-lookup"><span data-stu-id="c603b-114">In this code example, focus on the **serviceDNSName** attribute, which contains the DNS name of the host server for that service instance.</span></span> <span data-ttu-id="c603b-115">Étant donné que **servicednsname** n’est pas l’un des attributs répliqués dans un catalogue global, l’exemple de code utilise un processus en deux étapes pour le récupérer.</span><span class="sxs-lookup"><span data-stu-id="c603b-115">Because **serviceDNSName** is not one of the attributes replicated in a GC, the code example uses a two-step process to retrieve it.</span></span> <span data-ttu-id="c603b-116">Tout d’abord, elle utilise la recherche de GC pour obtenir le nom unique (DN) du SCP, puis utilise ce DN pour effectuer une liaison directe avec le SCP pour récupérer la propriété **servicednsname** .</span><span class="sxs-lookup"><span data-stu-id="c603b-116">First, it uses the GC search to get the distinguished name (DN) of the SCP, then it uses that DN to bind directly to the SCP to retrieve the **serviceDNSName** property.</span></span>


```C++
HRESULT EnumerateServiceInstances(
       LPWSTR szQuery,                // Search string filter.
       LPWSTR *pszAttribs,            // An array of attributes 
                                      // to retrieve.
       DWORD dwAttribs,               // # of attributes requested.
       DWORD *pdwAttribs,             // # of attributes retrieved.
       ADS_ATTR_INFO **ppPropEntries  // Returns a pointer to the 
                                      // retrieved attributes.
        )
{
HRESULT hr;
IEnumVARIANT *pEnum = NULL;
IADsContainer *pCont = NULL;
VARIANT var;
IDispatch *pDisp = NULL;
BSTR  bstrPath = NULL;
ULONG lFetch;
IADs *pADs = NULL;
int iRows=0;
static IDirectorySearch *pSearch = NULL;
static ADS_SEARCH_HANDLE hSearch = NULL;

// Parameters for IDirectoryObject.
IDirectoryObject *pSCP = NULL;
 
// Structures and parameters for IDirectorySearch.
DWORD               dwPref;
ADS_SEARCH_COLUMN   Col;
ADS_SEARCHPREF_INFO SearchPref[2];
 
// First time through; set up the search.
if (pSearch == NULL) 
{
    // Bind to the GC: namespace container object. The GC DN 
    // is a single immediate child of the GC: namespace, which must 
    // be obtained through enumeration.
    hr = ADsGetObject(L"GC:", 
        IID_IADsContainer, 
        (void**) &pCont );
    if (FAILED(hr)) {
        _tprintf(TEXT("ADsGetObject(GC) failed: 0x%x\n"), hr);
        goto Cleanup;
    }
 
    // Obtain an enumeration interface for the GC container. 
    hr = ADsBuildEnumerator(pCont,&pEnum);
    if (FAILED(hr)) {
        _tprintf(TEXT("ADsBuildEnumerator failed: 0x%x\n"), hr);
        goto Cleanup;
    }
 
    // Enumerate. There is only one child of the GC: object.
    hr = ADsEnumerateNext(pEnum,1,&var,&lFetch);
    if (( hr == S_OK ) && ( lFetch == 1 ) ) 
    {
        pDisp = V_DISPATCH(&var);
        hr = pDisp->QueryInterface( IID_IADs, (void**)&pADs);
        if (hr == S_OK) 
            hr = pADs->get_ADsPath(&bstrPath);
    }
    if (FAILED(hr)) {
        _tprintf(TEXT("Enumeration failed: 0x%x\n"), hr);
        goto Cleanup;
    }
 
    // Now bstrPath contains the ADsPath for the current GC.  
    // Bind the GC to get the search interface.
    hr = ADsGetObject(bstrPath, 
                      IID_IDirectorySearch, 
                      (void**)&pSearch);
    if (FAILED(hr)) {
        _tprintf(TEXT("Failed to bind search root: 0x%x\n"), hr);
        goto Cleanup;
    } 
 
    // Set up a deep search.
    // Thousands of objects are not expected
    // in this example; request 1000 rows per page.
    dwPref=sizeof(SearchPref)/sizeof(ADS_SEARCHPREF_INFO);
    SearchPref[0].dwSearchPref =    ADS_SEARCHPREF_SEARCH_SCOPE;
    SearchPref[0].vValue.dwType =   ADSTYPE_INTEGER;
    SearchPref[0].vValue.Integer =  ADS_SCOPE_SUBTREE;
 
    SearchPref[1].dwSearchPref =    ADS_SEARCHPREF_PAGESIZE;
    SearchPref[1].vValue.dwType =   ADSTYPE_INTEGER;
    SearchPref[1].vValue.Integer =  1000;
 
    hr = pSearch->SetSearchPreference(SearchPref, dwPref);
    if (FAILED(hr))    {
        _tprintf(TEXT("Failed to set search prefs: 0x%x\n"), hr);
        goto Cleanup;
    } 
 
    // Execute the search. From the GC, get the distinguished name 
    // of the SCP. Use the DN to bind to the SCP and get the other 
    // properties.
    hr = pSearch->ExecuteSearch(szQuery, pszAttribs, 1, &hSearch);
    if (FAILED(hr)) {
        _tprintf(TEXT("ExecuteSearch failed: 0x%x\n"), hr);
        goto Cleanup;
    } 
}
 
// Get the next row.
hr = pSearch->GetNextRow(hSearch);
 
// Process the row.
if (SUCCEEDED(hr) && hr !=S_ADS_NOMORE_ROWS) 
{
    // Get the distinguished name of the object in this row.
    hr = pSearch->GetColumn(hSearch, L"distinguishedName", &Col);
    if FAILED(hr) { 
        _tprintf(TEXT("GetColumn failed: 0x%x\n"), hr);
        goto Cleanup;
    }
    // Bind to the DN to get the properties.
    if (Col.dwADsType == ADSTYPE_CASE_IGNORE_STRING)
    {
        LPWSTR szSCPPath = 
          new WCHAR[7 + lstrlenW(Col.pADsValues->CaseIgnoreString) + 1];
        wcscpy_s(szSCPPath, L"LDAP://");
        wcscat_s(szSCPPath, Col.pADsValues->CaseIgnoreString);
        hr = ADsGetObject(szSCPPath, 
                          IID_IDirectoryObject,
                          (void**)&pSCP);
        delete szSCPPath;
        if (SUCCEEDED(hr)) 
        {
            hr = pSCP->GetObjectAttributes(pszAttribs, dwAttribs,
                          ppPropEntries, pdwAttribs);
            if(FAILED(hr)) {
                _tprintf(TEXT("GetObjectAttributes Failed."), hr);
                goto Cleanup;
            }
        }
    }
    pSearch->FreeColumn(&Col);}
 
Cleanup:
if (bstrPath)
    SysFreeString(bstrPath);
if (pSCP) 
    pSCP->Release();
if (pCont) 
    pCont->Release();
if (pEnum)
    ADsFreeEnumerator(pEnum);
if (pADs) 
    pADs->Release();
if (pDisp)
    pDisp->Release();
 
return hr;
 
}
```



 

 