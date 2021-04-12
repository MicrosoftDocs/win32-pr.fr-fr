---
title: Récupération des objets supprimés
description: Les objets supprimés sont stockés dans le conteneur objets supprimés.
ms.assetid: dc9a6466-204b-4a78-b0f3-9c03c13a374b
ms.tgt_platform: multiple
keywords:
- Récupération des objets supprimés
- objet AD, récupération des objets supprimés
- Active Directory, utiliser, récupérer des objets supprimés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62b2062c747e38bc0b3a9b1b793a102006c11512
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462834"
---
# <a name="retrieving-deleted-objects"></a>Récupération des objets supprimés

Les objets supprimés sont stockés dans le conteneur objets supprimés. Le conteneur objets supprimés n’est normalement pas visible, mais le conteneur objets supprimés peut être lié à par un membre du groupe administrateurs. Le contenu du conteneur objets supprimés peut être énuméré et des attributs d’objet supprimés individuels peuvent être obtenus à l’aide de l’interface [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) avec la préférence de recherche **ad \_ SEARCHPREF \_ Tombstone** .

Le conteneur objets supprimés peut être obtenu en liant le **\_ \_ \_ conteneur d’objets supprimés GUID** connu défini dans ntdsapi. h. Pour plus d’informations sur la liaison à des GUID connus, consultez [liaison à des objets Well-Known à l’aide de WKGUID](binding-to-well-known-objects-using-wkguid.md).

Spécifiez l’option de **\_ \_ liaison rapide ADS** lors de la liaison au conteneur objets supprimés. Cela signifie que les interfaces ADSI utilisées pour travailler avec un objet dans Active Directory Domain Services, telles que [**IADs**](/windows/desktop/api/iads/nn-iads-iads) et [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist), ne peuvent pas être utilisées sur le conteneur objets supprimés. Pour plus d’informations et pour obtenir un exemple de code qui montre comment effectuer une liaison au conteneur objets supprimés, consultez l’exemple de fonction GetDeletedObjectsContainer ci-dessous.

-   [Énumération des objets supprimés](#enumerating-deleted-objects)
-   [Recherche d’un objet supprimé spécifique](#finding-a-specific-deleted-object)
    -   [GetDeletedObjectsContainer](#getdeletedobjectscontainer)
    -   [EnumDeletedObjects](#enumdeletedobjects)
    -   [FindDeletedObjectByGUID](#finddeletedobjectbyguid)

## <a name="enumerating-deleted-objects"></a>Énumération des objets supprimés

L’interface [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) est utilisée pour rechercher des objets supprimés.

**Pour énumérer les objets supprimés**

1.  Obtenez l’interface [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) pour le conteneur objets supprimés. Pour ce faire, vous devez lier au conteneur objets supprimés et demander l’interface **IDirectorySearch** . Pour plus d’informations et pour obtenir un exemple de code qui montre comment effectuer une liaison au conteneur objets supprimés, consultez l’exemple de fonction **GetDeletedObjectsContainer** suivant.
2.  Définissez la préférence de recherche de l' **\_ \_ \_ étendue de recherche SEARCHPREF ADS** sur la **\_ portée ad \_ onelevel** à l’aide de la méthode [**IDirectorySearch :: SetSearchPreference**](/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference) . Vous pouvez également utiliser la préférence de **\_ sous- \_ arborescence étendue ADS** , mais le conteneur objets supprimés n’est qu’un niveau. par conséquent, l’utilisation de la **sous- \_ \_ arborescence étendue ADS** est redondante.
3.  Définissez la préférence de recherche **ad \_ SEARCHPREF \_ Tombstone** sur **true**. La recherche inclut alors les objets supprimés.
4.  Définissez la préférence de recherche de **\_ \_ pages ADS SEARCHPREF** sur une valeur inférieure ou égale à 1000. Cela est facultatif, mais si cela n’est pas fait, il n’est pas possible de récupérer plus de 1000 objets supprimés.
5.  Définissez le filtre de recherche dans l’appel de [**IDirectorySearch :: ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) sur « (IsDeleted =**true**) ». La recherche récupère alors uniquement les objets dont l’attribut **IsDeleted** a la valeur **true**.

Pour obtenir un exemple de code qui montre comment énumérer les objets supprimés, consultez l’exemple de fonction **EnumDeletedObjects** suivant.

Vous pouvez affiner la recherche en ajoutant au filtre de recherche, comme indiqué dans [dialecte LDAP](/windows/desktop/ADSI/ldap-dialect). Par exemple, pour rechercher tous les objets supprimés dont le nom commence par « Jeff », le filtre de recherche est défini sur « (& (isDeleted =**true**) (CN = Jeff \* )) ».

Comme les objets supprimés ont la plupart de leurs attributs supprimés lorsqu’ils sont supprimés, il n’est pas possible de lier directement à un objet supprimé. L’option de **\_ \_ liaison rapide ADS** doit être spécifiée lors de la liaison à un objet supprimé. Cela signifie que les interfaces ADSI utilisées pour travailler avec un objet Active Directory Domain Services, comme [**IADs**](/windows/desktop/api/iads/nn-iads-iads) et [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist), ne peuvent pas être utilisées sur un conteneur d’objets supprimé.

## <a name="finding-a-specific-deleted-object"></a>Recherche d’un objet supprimé spécifique

Il est également possible de rechercher un objet supprimé spécifique. Si l’attribut **objectGUID** de l’objet est connu, il peut être utilisé pour Rechercher l’objet avec cet **objectGUID** spécifique. Pour plus d’informations et pour obtenir un exemple de code qui montre comment rechercher un objet supprimé spécifique, consultez **FindDeletedObjectByGUID** ci-dessous.

### <a name="getdeletedobjectscontainer"></a>GetDeletedObjectsContainer

L’exemple de code C++ suivant montre comment effectuer une liaison au conteneur objets supprimés.


```C++
//***************************************************************************
//
//  GetDeletedObjectsContainer()
//
//  Binds to the Deleted Object container.
//
//***************************************************************************

HRESULT GetDeletedObjectsContainer(IADsContainer **ppContainer)
{
    if(NULL == ppContainer)
    {
        return E_INVALIDARG;
    }

    HRESULT hr;
    IADs *pRoot;

    *ppContainer = NULL;

    // Bind to the rootDSE object.
    hr = ADsOpenObject(L"LDAP://rootDSE",
                    NULL,
                    NULL,
                    ADS_SECURE_AUTHENTICATION,
                    IID_IADs,
                    (LPVOID*)&pRoot);
    if(SUCCEEDED(hr))
    {
        VARIANT var;
        
        VariantInit(&var);

        // Get the current domain DN.
        hr = pRoot->Get(CComBSTR("defaultNamingContext"), &var);
        if(SUCCEEDED(hr))
        {
            // Build the binding string.
            LPWSTR pwszFormat = L"LDAP://<WKGUID=%s,%s>";
            LPWSTR pwszPath;

            pwszPath = new WCHAR[wcslen(pwszFormat) + wcslen(GUID_DELETED_OBJECTS_CONTAINER_W) + wcslen(var.bstrVal)];
            if(NULL != pwszPath)
            {
                swprintf_s(pwszPath, pwszFormat, GUID_DELETED_OBJECTS_CONTAINER_W, var.bstrVal);

                // Bind to the object.
                hr = ADsOpenObject(pwszPath,
                                NULL,
                                NULL,
                                ADS_FAST_BIND | ADS_SECURE_AUTHENTICATION,
                                IID_IADsContainer,
                                (LPVOID*)ppContainer);

                delete pwszPath;
            }
            else
            {
                hr = E_OUTOFMEMORY;
            }

            VariantClear(&var);        
        }

        pRoot->Release(); 
    }

    return hr;
}

```



### <a name="enumdeletedobjects"></a>EnumDeletedObjects

L’exemple de code C++ suivant montre comment énumérer les objets dans le conteneur objets supprimés.


```C++
//***************************************************************************
//
//  EnumDeletedObjects()
//
//  Enumerates all of the objects in the Deleted Objects container.
//
//***************************************************************************

HRESULT EnumDeletedObjects()
{
    HRESULT hr;
    IADsContainer *pDeletedObjectsCont = NULL;
    IDirectorySearch *pSearch = NULL;

    hr = GetDeletedObjectsContainer(&pDeletedObjectsCont);
    if(FAILED(hr))
    {
        goto cleanup;
    }

    hr = pDeletedObjectsCont->QueryInterface(IID_IDirectorySearch, (LPVOID*)&pSearch);    
    if(FAILED(hr))
    {
        goto cleanup;
    }

    ADS_SEARCH_HANDLE hSearch;

    // Only search for direct child objects of the container.
    ADS_SEARCHPREF_INFO rgSearchPrefs[3];
    rgSearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_SEARCH_SCOPE;
    rgSearchPrefs[0].vValue.dwType = ADSTYPE_INTEGER;
    rgSearchPrefs[0].vValue.Integer = ADS_SCOPE_ONELEVEL;

    // Search for deleted objects.
    rgSearchPrefs[1].dwSearchPref = ADS_SEARCHPREF_TOMBSTONE;
    rgSearchPrefs[1].vValue.dwType = ADSTYPE_BOOLEAN;
    rgSearchPrefs[1].vValue.Boolean = TRUE;

    // Set the page size.
    rgSearchPrefs[2].dwSearchPref = ADS_SEARCHPREF_PAGESIZE;
    rgSearchPrefs[2].vValue.dwType = ADSTYPE_INTEGER;
    rgSearchPrefs[2].vValue.Integer = 1000;

    // Set the search preference
    hr = pSearch->SetSearchPreference(rgSearchPrefs, ARRAYSIZE(rgSearchPrefs));
    if(FAILED(hr))
    {
        goto cleanup;
    }

    // Set the search filter.
    LPWSTR pszSearch = L"(cn=*)";

    // Set the attributes to retrieve.
    LPWSTR rgAttributes[] = {L"cn", L"distinguishedName", L"lastKnownParent"};

    // Execute the search
    hr = pSearch->ExecuteSearch(    pszSearch,
                                    rgAttributes,
                                    ARRAYSIZE(rgAttributes),
                                    &hSearch);
    if(SUCCEEDED(hr))
    {    
        // Call IDirectorySearch::GetNextRow() to retrieve the next row of data
        while(S_OK == (hr = pSearch->GetNextRow(hSearch)))
        {
            ADS_SEARCH_COLUMN col;
            UINT i;
            
            // Enumerate the retrieved attributes.
            for(i = 0; i < ARRAYSIZE(rgAttributes); i++)
            {
                hr = pSearch->GetColumn(hSearch, rgAttributes[i], &col);
                if(SUCCEEDED(hr))
                {
                    switch(col.dwADsType)
                    {
                        case ADSTYPE_CASE_IGNORE_STRING:
                        case ADSTYPE_DN_STRING:
                        case ADSTYPE_PRINTABLE_STRING:
                        case ADSTYPE_NUMERIC_STRING:
                        case ADSTYPE_OCTET_STRING:
                            wprintf(L"%s: ", rgAttributes[i]); 
                            for(DWORD x = 0; x < col.dwNumValues; x++)
                            {
                                wprintf(col.pADsValues[x].CaseIgnoreString); 
                                if((x + 1) < col.dwNumValues)
                                {
                                    wprintf(L","); 
                                }
                            }
                            wprintf(L"\n"); 
                            break;
                    }

                    pSearch->FreeColumn(&col);
                }
            }

            wprintf(L"\n");
        }

        // Close the search handle to cleanup.
        pSearch->CloseSearchHandle(hSearch);
    }

cleanup:

    if(pDeletedObjectsCont)
    {
        pDeletedObjectsCont->Release();
    }

    if(pSearch)
    {
        pSearch->Release();
    }

    return hr;
}

```



### <a name="finddeletedobjectbyguid"></a>FindDeletedObjectByGUID

L’exemple de code C++ suivant montre comment rechercher un objet supprimé spécifique dans la propriété **objectGUID** de l’objet.


```C++
HRESULT FindDeletedObjectByGUID(IADs *padsDomain, GUID *pguid)
{
    HRESULT hr;
    IDirectorySearch *pSearch = NULL;
    LPWSTR pwszGuid = NULL;

    hr = padsDomain->QueryInterface(IID_IDirectorySearch, (LPVOID*)&pSearch);    
    if(FAILED(hr))
    {
        goto cleanup;
    }

    ADS_SEARCH_HANDLE hSearch;

    // Search the entire tree.
    ADS_SEARCHPREF_INFO rgSearchPrefs[2];
    rgSearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_SEARCH_SCOPE;
    rgSearchPrefs[0].vValue.dwType = ADSTYPE_INTEGER;
    rgSearchPrefs[0].vValue.Integer = ADS_SCOPE_SUBTREE;

    // Search for deleted objects.
    rgSearchPrefs[1].dwSearchPref = ADS_SEARCHPREF_TOMBSTONE;
    rgSearchPrefs[1].vValue.dwType = ADSTYPE_BOOLEAN;
    rgSearchPrefs[1].vValue.Boolean = TRUE;

    // Set the search preference.
    hr = pSearch->SetSearchPreference(rgSearchPrefs, 2);
    if(FAILED(hr))
    {
        goto cleanup;
    }

    // Set the search filter.
    hr = ADsEncodeBinaryData((LPBYTE)pguid, sizeof(GUID), &pwszGuid);
    if(FAILED(hr))
    {
        goto cleanup;
    }

    LPWSTR pwszFormat = L"(objectGUID=%s)";

    LPWSTR pwszSearch = new WCHAR[lstrlenW(pwszFormat) + lstrlenW(pwszGuid) + 1];
    if(NULL == pwszSearch)
    {
        goto cleanup;
    }
    
    swprintf_s(pwszSearch, pwszFormat, pwszGuid);
    
    FreeADsMem(pwszGuid);

    // Set the attributes to retrieve.
    LPWSTR rgAttributes[] = {L"cn", L"distinguishedName", L"lastKnownParent"};

    // Execute the search.
    hr = pSearch->ExecuteSearch(    pwszSearch,
                                    rgAttributes,
                                    3,
                                    &hSearch);
    if(SUCCEEDED(hr))
    {    
        // Call IDirectorySearch::GetNextRow() to retrieve the next row of data.
        while(S_OK == (hr = pSearch->GetNextRow(hSearch)))
        {
            ADS_SEARCH_COLUMN col;
            UINT i;
            
            // Enumerate the retrieved attributes.
            for(i = 0; i < ARRAYSIZE(rgAttributes); i++)
            {
                hr = pSearch->GetColumn(hSearch, rgAttributes[i], &col);
                if(SUCCEEDED(hr))
                {
                    switch(col.dwADsType)
                    {
                        case ADSTYPE_CASE_IGNORE_STRING:
                        case ADSTYPE_DN_STRING:
                        case ADSTYPE_PRINTABLE_STRING:
                        case ADSTYPE_NUMERIC_STRING:
                            wprintf(L"%s: ", rgAttributes[i]); 
                            for(DWORD x = 0; x < col.dwNumValues; x++)
                            {
                                wprintf(col.pADsValues[x].CaseIgnoreString); 
                                if((x + 1) < col.dwNumValues)
                                {
                                    wprintf(L","); 
                                }
                            }
                            wprintf(L"\n"); 
                            break;

                        case ADSTYPE_OCTET_STRING:
                            wprintf(L"%s: ", rgAttributes[i]); 
                            for(DWORD x = 0; x < col.dwNumValues; x++)
                            {
                                GUID guid;
                                LPBYTE pb = col.pADsValues[x].OctetString.lpValue;
                                WCHAR wszGUID[MAX_PATH];

                                // Convert the octet string into a GUID.
                                guid.Data1 = *((long*)pb);
                                pb += sizeof(guid.Data1);
                                guid.Data2 = *((short*)pb);
                                pb += sizeof(guid.Data2);
                                guid.Data3 = *((short*)pb);
                                pb += sizeof(guid.Data3);
                                CopyMemory(&guid.Data4, pb, sizeof(guid.Data4));

                                // Convert the GUID into a string.
                                StringFromGUID2(guid, wszGUID, MAX_PATH);
                                wprintf(wszGUID);

                                if((x + 1) < col.dwNumValues)
                                {
                                    wprintf(L","); 
                                }
                                OutputDebugStringW(wszGUID);
                                OutputDebugStringW(L"\n");

                                {
                                    DWORD a;

                                    for(a = 0, *wszGUID = 0; a < col.pADsValues[x].OctetString.dwLength; a++)
                                    {
                                        swprintf_s(wszGUID + lstrlenW(wszGUID), L"%02X", *(LPBYTE)(col.pADsValues[x].OctetString.lpValue + a));
                                    }

                                    OutputDebugStringW(wszGUID);
                                    OutputDebugStringW(L"\n");
                                }
                            }
                            wprintf(L"\n"); 
                            break;

                    }

                    pSearch->FreeColumn(&col);
                }
            }

            wprintf(L"\n");
        }

        // Close the search handle to cleanup.
        pSearch->CloseSearchHandle(hSearch);
    }

cleanup:

    if(pwszSearch)
    {
        delete pwszSearch;
    }
    
    if(pSearch)
    {
        pSearch->Release();
    }

    return hr;
}
```



 

 