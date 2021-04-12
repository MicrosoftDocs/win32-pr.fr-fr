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
# <a name="retrieving-deleted-objects"></a><span data-ttu-id="98924-106">Récupération des objets supprimés</span><span class="sxs-lookup"><span data-stu-id="98924-106">Retrieving Deleted Objects</span></span>

<span data-ttu-id="98924-107">Les objets supprimés sont stockés dans le conteneur objets supprimés.</span><span class="sxs-lookup"><span data-stu-id="98924-107">Deleted objects are stored in the Deleted Objects container.</span></span> <span data-ttu-id="98924-108">Le conteneur objets supprimés n’est normalement pas visible, mais le conteneur objets supprimés peut être lié à par un membre du groupe administrateurs.</span><span class="sxs-lookup"><span data-stu-id="98924-108">The Deleted Objects container is not normally visible, but the Deleted Objects container can be bound to by a member of the administrators group.</span></span> <span data-ttu-id="98924-109">Le contenu du conteneur objets supprimés peut être énuméré et des attributs d’objet supprimés individuels peuvent être obtenus à l’aide de l’interface [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) avec la préférence de recherche **ad \_ SEARCHPREF \_ Tombstone** .</span><span class="sxs-lookup"><span data-stu-id="98924-109">The contents of the Deleted Objects container can be enumerated and individual deleted object attributes can be obtained using the [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) interface with the **ADS\_SEARCHPREF\_TOMBSTONE** search preference.</span></span>

<span data-ttu-id="98924-110">Le conteneur objets supprimés peut être obtenu en liant le **\_ \_ \_ conteneur d’objets supprimés GUID** connu défini dans ntdsapi. h.</span><span class="sxs-lookup"><span data-stu-id="98924-110">The Deleted Objects container can be obtained by binding to the well-known GUID **GUID\_DELETED\_OBJECTS\_CONTAINER** defined in Ntdsapi.h.</span></span> <span data-ttu-id="98924-111">Pour plus d’informations sur la liaison à des GUID connus, consultez [liaison à des objets Well-Known à l’aide de WKGUID](binding-to-well-known-objects-using-wkguid.md).</span><span class="sxs-lookup"><span data-stu-id="98924-111">For more information about binding to well-known GUIDs, see [Binding to Well-Known Objects Using WKGUID](binding-to-well-known-objects-using-wkguid.md).</span></span>

<span data-ttu-id="98924-112">Spécifiez l’option de **\_ \_ liaison rapide ADS** lors de la liaison au conteneur objets supprimés.</span><span class="sxs-lookup"><span data-stu-id="98924-112">Specify the **ADS\_FAST\_BIND** option when binding to the Deleted Objects container.</span></span> <span data-ttu-id="98924-113">Cela signifie que les interfaces ADSI utilisées pour travailler avec un objet dans Active Directory Domain Services, telles que [**IADs**](/windows/desktop/api/iads/nn-iads-iads) et [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist), ne peuvent pas être utilisées sur le conteneur objets supprimés.</span><span class="sxs-lookup"><span data-stu-id="98924-113">This means that the ADSI interfaces used to work with an object in Active Directory Domain Services, such as [**IADs**](/windows/desktop/api/iads/nn-iads-iads) and [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist), cannot be used on the Deleted Objects container.</span></span> <span data-ttu-id="98924-114">Pour plus d’informations et pour obtenir un exemple de code qui montre comment effectuer une liaison au conteneur objets supprimés, consultez l’exemple de fonction GetDeletedObjectsContainer ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="98924-114">For more information and a code example that shows how to bind to the Deleted Objects container, see the GetDeletedObjectsContainer example function below.</span></span>

-   [<span data-ttu-id="98924-115">Énumération des objets supprimés</span><span class="sxs-lookup"><span data-stu-id="98924-115">Enumerating Deleted Objects</span></span>](#enumerating-deleted-objects)
-   [<span data-ttu-id="98924-116">Recherche d’un objet supprimé spécifique</span><span class="sxs-lookup"><span data-stu-id="98924-116">Finding a Specific Deleted Object</span></span>](#finding-a-specific-deleted-object)
    -   [<span data-ttu-id="98924-117">GetDeletedObjectsContainer</span><span class="sxs-lookup"><span data-stu-id="98924-117">GetDeletedObjectsContainer</span></span>](#getdeletedobjectscontainer)
    -   [<span data-ttu-id="98924-118">EnumDeletedObjects</span><span class="sxs-lookup"><span data-stu-id="98924-118">EnumDeletedObjects</span></span>](#enumdeletedobjects)
    -   [<span data-ttu-id="98924-119">FindDeletedObjectByGUID</span><span class="sxs-lookup"><span data-stu-id="98924-119">FindDeletedObjectByGUID</span></span>](#finddeletedobjectbyguid)

## <a name="enumerating-deleted-objects"></a><span data-ttu-id="98924-120">Énumération des objets supprimés</span><span class="sxs-lookup"><span data-stu-id="98924-120">Enumerating Deleted Objects</span></span>

<span data-ttu-id="98924-121">L’interface [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) est utilisée pour rechercher des objets supprimés.</span><span class="sxs-lookup"><span data-stu-id="98924-121">The [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) interface is used to search for deleted objects.</span></span>

<span data-ttu-id="98924-122">**Pour énumérer les objets supprimés**</span><span class="sxs-lookup"><span data-stu-id="98924-122">**To enumerate deleted objects**</span></span>

1.  <span data-ttu-id="98924-123">Obtenez l’interface [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) pour le conteneur objets supprimés.</span><span class="sxs-lookup"><span data-stu-id="98924-123">Obtain the [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) interface for the Deleted Objects container.</span></span> <span data-ttu-id="98924-124">Pour ce faire, vous devez lier au conteneur objets supprimés et demander l’interface **IDirectorySearch** .</span><span class="sxs-lookup"><span data-stu-id="98924-124">This is accomplished by binding to the Deleted Objects container and requesting the **IDirectorySearch** interface.</span></span> <span data-ttu-id="98924-125">Pour plus d’informations et pour obtenir un exemple de code qui montre comment effectuer une liaison au conteneur objets supprimés, consultez l’exemple de fonction **GetDeletedObjectsContainer** suivant.</span><span class="sxs-lookup"><span data-stu-id="98924-125">For more information and a code example that shows how to bind to the Deleted Objects container, see the following **GetDeletedObjectsContainer** function example.</span></span>
2.  <span data-ttu-id="98924-126">Définissez la préférence de recherche de l' **\_ \_ \_ étendue de recherche SEARCHPREF ADS** sur la **\_ portée ad \_ onelevel** à l’aide de la méthode [**IDirectorySearch :: SetSearchPreference**](/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="98924-126">Set the **ADS\_SEARCHPREF\_SEARCH\_SCOPE** search preference to **ADS\_SCOPE\_ONELEVEL** using the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="98924-127">Vous pouvez également utiliser la préférence de **\_ sous- \_ arborescence étendue ADS** , mais le conteneur objets supprimés n’est qu’un niveau. par conséquent, l’utilisation de la **sous- \_ \_ arborescence étendue ADS** est redondante.</span><span class="sxs-lookup"><span data-stu-id="98924-127">The **ADS\_SCOPE\_SUBTREE** preference can also be used, but the Deleted Objects container is only one level, so using **ADS\_SCOPE\_SUBTREE** is redundant.</span></span>
3.  <span data-ttu-id="98924-128">Définissez la préférence de recherche **ad \_ SEARCHPREF \_ Tombstone** sur **true**.</span><span class="sxs-lookup"><span data-stu-id="98924-128">Set the **ADS\_SEARCHPREF\_TOMBSTONE** search preference to **TRUE**.</span></span> <span data-ttu-id="98924-129">La recherche inclut alors les objets supprimés.</span><span class="sxs-lookup"><span data-stu-id="98924-129">This causes the search to include deleted objects.</span></span>
4.  <span data-ttu-id="98924-130">Définissez la préférence de recherche de **\_ \_ pages ADS SEARCHPREF** sur une valeur inférieure ou égale à 1000.</span><span class="sxs-lookup"><span data-stu-id="98924-130">Set the **ADS\_SEARCHPREF\_PAGESIZE** search preference to a value less than, or equal to, 1000.</span></span> <span data-ttu-id="98924-131">Cela est facultatif, mais si cela n’est pas fait, il n’est pas possible de récupérer plus de 1000 objets supprimés.</span><span class="sxs-lookup"><span data-stu-id="98924-131">This is optional, but if this is not done, no more than 1000 deleted objects can be retrieved.</span></span>
5.  <span data-ttu-id="98924-132">Définissez le filtre de recherche dans l’appel de [**IDirectorySearch :: ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) sur « (IsDeleted =**true**) ».</span><span class="sxs-lookup"><span data-stu-id="98924-132">Set the search filter in the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) call to "(isDeleted=**TRUE**)".</span></span> <span data-ttu-id="98924-133">La recherche récupère alors uniquement les objets dont l’attribut **IsDeleted** a la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="98924-133">This causes the search to only retrieve objects with the **isDeleted** attribute set to **TRUE**.</span></span>

<span data-ttu-id="98924-134">Pour obtenir un exemple de code qui montre comment énumérer les objets supprimés, consultez l’exemple de fonction **EnumDeletedObjects** suivant.</span><span class="sxs-lookup"><span data-stu-id="98924-134">For a code example code that shows how to enumerate deleted objects, see the following **EnumDeletedObjects** function example.</span></span>

<span data-ttu-id="98924-135">Vous pouvez affiner la recherche en ajoutant au filtre de recherche, comme indiqué dans [dialecte LDAP](/windows/desktop/ADSI/ldap-dialect).</span><span class="sxs-lookup"><span data-stu-id="98924-135">The search can be refined further by adding to the search filter as shown in [LDAP Dialect](/windows/desktop/ADSI/ldap-dialect).</span></span> <span data-ttu-id="98924-136">Par exemple, pour rechercher tous les objets supprimés dont le nom commence par « Jeff », le filtre de recherche est défini sur « (& (isDeleted =**true**) (CN = Jeff \* )) ».</span><span class="sxs-lookup"><span data-stu-id="98924-136">For example, to search for all of the deleted objects with a name that begins with "Jeff", the search filter would be set to "(&(isDeleted=**TRUE**)(cn=Jeff\*))".</span></span>

<span data-ttu-id="98924-137">Comme les objets supprimés ont la plupart de leurs attributs supprimés lorsqu’ils sont supprimés, il n’est pas possible de lier directement à un objet supprimé.</span><span class="sxs-lookup"><span data-stu-id="98924-137">Because deleted objects have most of their attributes removed when they are deleted, it is not possible to bind directly to a deleted object.</span></span> <span data-ttu-id="98924-138">L’option de **\_ \_ liaison rapide ADS** doit être spécifiée lors de la liaison à un objet supprimé.</span><span class="sxs-lookup"><span data-stu-id="98924-138">The **ADS\_FAST\_BIND** option must be specified when binding to a deleted object.</span></span> <span data-ttu-id="98924-139">Cela signifie que les interfaces ADSI utilisées pour travailler avec un objet Active Directory Domain Services, comme [**IADs**](/windows/desktop/api/iads/nn-iads-iads) et [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist), ne peuvent pas être utilisées sur un conteneur d’objets supprimé.</span><span class="sxs-lookup"><span data-stu-id="98924-139">This means that the ADSI interfaces used to work with an Active Directory Domain Services object, such as [**IADs**](/windows/desktop/api/iads/nn-iads-iads) and [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist), cannot be used on a deleted object container.</span></span>

## <a name="finding-a-specific-deleted-object"></a><span data-ttu-id="98924-140">Recherche d’un objet supprimé spécifique</span><span class="sxs-lookup"><span data-stu-id="98924-140">Finding a Specific Deleted Object</span></span>

<span data-ttu-id="98924-141">Il est également possible de rechercher un objet supprimé spécifique.</span><span class="sxs-lookup"><span data-stu-id="98924-141">It is also possible to find a specific deleted object.</span></span> <span data-ttu-id="98924-142">Si l’attribut **objectGUID** de l’objet est connu, il peut être utilisé pour Rechercher l’objet avec cet **objectGUID** spécifique.</span><span class="sxs-lookup"><span data-stu-id="98924-142">If the **objectGUID** of the object is known, it can be used to search for the object with that specific **objectGUID**.</span></span> <span data-ttu-id="98924-143">Pour plus d’informations et pour obtenir un exemple de code qui montre comment rechercher un objet supprimé spécifique, consultez **FindDeletedObjectByGUID** ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="98924-143">For more information and a code example that shows how to find a specific deleted object, see **FindDeletedObjectByGUID** below.</span></span>

### <a name="getdeletedobjectscontainer"></a><span data-ttu-id="98924-144">GetDeletedObjectsContainer</span><span class="sxs-lookup"><span data-stu-id="98924-144">GetDeletedObjectsContainer</span></span>

<span data-ttu-id="98924-145">L’exemple de code C++ suivant montre comment effectuer une liaison au conteneur objets supprimés.</span><span class="sxs-lookup"><span data-stu-id="98924-145">The following C++ code example shows how to bind to the Deleted Objects container.</span></span>


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



### <a name="enumdeletedobjects"></a><span data-ttu-id="98924-146">EnumDeletedObjects</span><span class="sxs-lookup"><span data-stu-id="98924-146">EnumDeletedObjects</span></span>

<span data-ttu-id="98924-147">L’exemple de code C++ suivant montre comment énumérer les objets dans le conteneur objets supprimés.</span><span class="sxs-lookup"><span data-stu-id="98924-147">The following C++ code example shows how to enumerate the objects in the Deleted Objects container.</span></span>


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



### <a name="finddeletedobjectbyguid"></a><span data-ttu-id="98924-148">FindDeletedObjectByGUID</span><span class="sxs-lookup"><span data-stu-id="98924-148">FindDeletedObjectByGUID</span></span>

<span data-ttu-id="98924-149">L’exemple de code C++ suivant montre comment rechercher un objet supprimé spécifique dans la propriété **objectGUID** de l’objet.</span><span class="sxs-lookup"><span data-stu-id="98924-149">The following C++ code example shows how to find a specific deleted object from the object's **objectGUID** property.</span></span>


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



 

 