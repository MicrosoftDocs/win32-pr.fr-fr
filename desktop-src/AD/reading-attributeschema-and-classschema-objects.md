---
title: Lecture des objets attributeSchema et classSchema
description: Cette rubrique fournit des exemples de code et des instructions pour lire directement à partir des objets attributeSchema et classSchema dans le conteneur de schéma.
ms.assetid: a60558e1-88a1-493c-9340-a90143b11f60
ms.tgt_platform: multiple
keywords:
- Lecture des objets attributeSchema et classSchema Active Directory
- objets Active Directory, lire les objets attributeSchema et classSchema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 910d387809f7be8af22d494974021e5e6a47d0ab
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101433"
---
# <a name="reading-attributeschema-and-classschema-objects"></a>Lecture des objets attributeSchema et classSchema

Cette rubrique fournit des exemples de code et des instructions pour lire directement à partir des objets **attributeSchema** et **classSchema** dans le conteneur de schéma. N’oubliez pas que, dans la plupart des cas de programmation, lorsque vous devez lire des données sur une définition de classe ou d’attribut, il est plus efficace de lire les données à partir du schéma abstrait, comme décrit dans [lecture du schéma abstrait](reading-the-abstract-schema.md).

Les interfaces et les techniques utilisées pour lire le conteneur de schéma sont celles utilisées pour lire un objet dans Active Directory Domain Services. Les instructions sont les suivantes :

-   Pour effectuer une liaison au conteneur de schéma, obtenez son nom unique qui peut être extrait par la liaison à rootDSE et la lecture de la propriété **schemaNamingContext** , comme décrit dans [liaison sans serveur et RootDSE](serverless-binding-and-rootdse.md).
-   Utilisez un pointeur [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) pour le conteneur de schéma pour énumérer les objets **attributeSchema** et **classSchema** .
-   Utilisez l’interface [**IADs**](/windows/desktop/api/iads/nn-iads-iads) ou [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) pour récupérer les propriétés d’un objet **attributeSchema** et **classSchema** .
-   Utilisez les fonctions [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject) ou [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject) pour établir une liaison directe avec un objet **attributeSchema** ou **classSchema** .
-   Si vous lisez plusieurs objets **attributeSchema** ou **classSchema** , vous pouvez augmenter les performances en les liant à un pointeur [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) sur le conteneur de schéma et en utilisant la méthode [**IADsContainer. GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) pour établir une liaison avec les objets de classe et d’attribut individuels. Cela est plus efficace que d’effectuer des appels répétés de [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject) ou [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject) pour la liaison à la classe individuelle et aux objets d’attribut. Utilisez l’attribut **CN** pour générer le chemin d’accès relatif pour l’appel de **IADsContainer. GetObject** (par exemple, « CN = utilisateur » pour l’objet **classSchema** pour la classe d’utilisateur).
-   Utilisez un pointeur [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) pour le conteneur de schéma pour interroger le schéma des attributs ou des classes qui correspondent à un filtre de recherche.

Pour obtenir un exemple de code qui illustre différentes méthodes de recherche d’objets de schéma, consultez l' [exemple de code pour rechercher des objets de schéma](example-code-for-searching-for-schema-objects.md).

L’exemple de code C++ suivant est lié à un pointeur [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) sur le conteneur de schéma, puis utilise les fonctions [**ADsBuildEnumerator**](/windows/desktop/api/adshlp/nf-adshlp-adsbuildenumerator) et [**ADsEnumerateNext**](/windows/desktop/api/adshlp/nf-adshlp-adsenumeratenext) pour énumérer son contenu. Sachez que l’énumération comprend tous les objets **attributeSchema** et **classSchema** , ainsi qu’un objet de sous- **schéma** unique, qui est le schéma abstrait.

Pour chaque objet énuméré, l’exemple de code utilise la propriété [**IADs. Class**](/windows/desktop/ADSI/iads-property-methods) pour déterminer s’il s’agit d’un objet **attributeSchema** ou **classSchema** . L’exemple de code montre comment lire les propriétés qui ne sont pas disponibles dans le schéma abstrait.


```C++
//  Add activeds.lib to the project.
//  Add adsiid.lib to the project.

#include "stdafx.h"
#include <windows.h>
#include <stdio.h>
#include <ole2.h>
#include <activeds.h>
#include <atlbase.h>

//  Forward declarations.
void ProcessAttribute(IADs *pChild);
void ProcessClass(IADs *pChild);

//  Entry point for the application.
int wmain(int argc, WCHAR* argv[])
{
    HRESULT hr;

    hr = CoInitialize(NULL);
    if(SUCCEEDED(hr))
    {
        CComBSTR sbstrDSPath;
        CComVariant svar;
        IADs *pRootDSE = NULL;
        IADsContainer *pSchema = NULL;  
        IEnumVARIANT *pEnum = NULL;
        ULONG lFetch;
        CComBSTR sbstrClass; 
        DWORD dwClasses = 0, dwAttributes = 0, dwUnknownClass = 0;

        //  Bind to rootDSE to get the schemaNamingContext property.
        hr = ADsGetObject(L"LDAP://rootDSE", IID_IADs, (void**)&pRootDSE);
        if (FAILED(hr)) 
        {
            wprintf(L"ADsGetObject failed: 0x%x\n", hr);
            goto cleanup;
        }

        hr = pRootDSE->Get(CComBSTR("schemaNamingContext"), &svar);
        sbstrDSPath = "LDAP://";
        sbstrDSPath += svar.bstrVal;

        //  Bind to the actual schema container.
        wprintf(L"Binding to %s\n", sbstrDSPath);
        hr = ADsGetObject(sbstrDSPath, IID_IADsContainer, (void**) &pSchema);
        if (FAILED(hr)) 
        {
            wprintf(L"ADsGetObject to schema failed: 0x%x\n", hr);
            goto cleanup;
        }

        //  Enumerate the attribute and class objects in the schema container.
        hr = ADsBuildEnumerator(pSchema, &pEnum);
        if (FAILED(hr)) 
        {
            wprintf(L"ADsBuildEnumerator failed: 0x%x\n", hr);
            goto cleanup;
        }

        hr = ADsEnumerateNext(pEnum, 1, &svar, &lFetch);
        while(S_OK == hr && 1 == lFetch)
        {
            IADs *pChild = NULL;

            //  Get an IADs pointer on the child object.
            hr = V_DISPATCH(&svar)->QueryInterface(IID_IADs, (void**) &pChild);
            if (SUCCEEDED(hr)) 
            {
                //  Verify that this is a class, attribute, or subSchema object.
                hr = pChild->get_Class(&sbstrClass);
                if (SUCCEEDED(hr)) 
                {
                    //  Get data. This depends on type of schema element.
                    if (_wcsicmp(L"classSchema", sbstrClass) == 0)
                    {
                        dwClasses++;
                        wprintf(L"%s\n", sbstrClass);
                        ProcessClass(pChild);
                        wprintf(L"\n");
                    }
                    else if (_wcsicmp(L"attributeSchema", sbstrClass) == 0)
                    {
                        dwAttributes++;
                        wprintf(L"%s\n", sbstrClass);
                        ProcessAttribute(pChild);
                        wprintf(L"\n");
                    }
                    else if (_wcsicmp(L"subSchema", sbstrClass) == 0) 
                    {
                        wprintf(L"abstract schema");
                        wprintf(L"\n");
                    }
                    else
                    {
                        dwUnknownClass++;
                    }
                }

                pChild->Release();
            }

            hr = ADsEnumerateNext(pEnum, 1, &svar, &lFetch);
        }

        wprintf(L"Classes: %u\nAttributes: %u\nUnknown: %u\n", dwClasses, dwAttributes, dwUnknownClass);

cleanup:
        if (pRootDSE)
        {
            pRootDSE->Release();
        }

        if (pEnum)
        {
            ADsFreeEnumerator(pEnum);
        }

        if (pSchema)
        {
            pSchema->Release();
        }

    }    

    CoUninitialize();

    return 0;
}


//  PrintGUIDFromVariant
//  Prints a GUID in string format.
void PrintGUIDFromVariant(VARIANT varGUID)
{
    HRESULT hr;
    void HUGEP *pArray;
    WCHAR szGUID[40];
    LPGUID pGUID;

    DWORD dwLen = sizeof(GUID);

    hr = SafeArrayAccessData(V_ARRAY(&varGUID), &pArray);
    if(SUCCEEDED(hr))
    {
        pGUID = (LPGUID)pArray;

        //  Convert GUID to string.
        StringFromGUID2(*pGUID, szGUID, 40); 

        //  Print GUID.
        wprintf(L",%s",szGUID);

        SafeArrayUnaccessData(V_ARRAY(&varGUID));
    }
}


// PrintADSPropertyValue
void PrintADSPropertyValue(VARIANT var, BSTR bstrPropName, HRESULT hr) 
{
    if (E_ADS_PROPERTY_NOT_FOUND == hr)
    {
        wprintf(L"-- not set --\n");
    }
    else if (FAILED(hr))
    {
        wprintf(L"get %s failed: 0x%x\n", bstrPropName, hr);
    }
    else 
    {
        switch (var.vt) 
        {
        case VT_BSTR:
            wprintf(L"%s\n", var.bstrVal);
            break;

        case VT_I4:
            wprintf(L"%u\n", var.iVal);
            break;

        case VT_BOOL:
            wprintf(L"%s\n", var.boolVal ? L"TRUE" : L"FALSE");
            break;

        default:
            wprintf(L"-- ??? --\n");
        }
    }
}

//  ProcessAttribute
//  Gets information about an attributeClass object.
void ProcessAttribute(IADs *pChild)
{
    HRESULT hr;
    CComVariant svar;
    CComBSTR sbstrPropName;

    //  Get the attribute Common-Name (cn) property. 
    sbstrPropName = "cn";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the attribute lDAPDisplayName.
    sbstrPropName = "lDAPDisplayName";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class linkID. 
    sbstrPropName = "linkID";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the attribute schemaIDGUID. 
    sbstrPropName = "schemaIDGUID";
    hr = pChild->Get(sbstrPropName, &svar);
    if (E_ADS_PROPERTY_NOT_FOUND == hr)
    {
        wprintf(L"-- not set --\n");
    }
    else if(SUCCEEDED(hr))
    {
        PrintGUIDFromVariant(svar);
    }

    //  Get the attribute attributeSecurityGUID. 
    sbstrPropName = "attributeSecurityGUID";
    hr = pChild->Get(sbstrPropName, &svar);
    if (E_ADS_PROPERTY_NOT_FOUND == hr)
    {
        wprintf(L"-- not set --\n");
    }
    else if (SUCCEEDED(hr))
    {
        PrintGUIDFromVariant(svar);
    }

    //  Get the attribute attributeSyntax property. 
    sbstrPropName = "attributeSyntax";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the attribute's oMSyntax property. 
    sbstrPropName = "oMSyntax";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);
}


//  ProcessClass
//  Gets information about a schema class.
void ProcessClass(IADs *pChild)
{
    HRESULT hr;
    CComVariant svar;
    CComBSTR sbstrPropName;

    //  Get the class cn.
    sbstrPropName = "cn";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class lDAPDisplayName.
    sbstrPropName = "lDAPDisplayName";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class schemaIDGUID. 
    sbstrPropName = "schemaIDGUID";
    hr = pChild->Get(sbstrPropName, &svar);
    if (FAILED(hr))
    {
        wprintf(L",get schemaIDGUID failed: 0x%x", hr);
    }
    else 
    {
        PrintGUIDFromVariant(svar);
    }

    //  Get the class adminDescription property. 
    sbstrPropName = "adminDescription";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class adminDisplayName property. 
    sbstrPropName = "adminDisplayName";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class rDNAttID. 
    sbstrPropName = "rDNAttID";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class defaultHidingValue. 
    sbstrPropName = "defaultHidingValue";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class defaultObjectCategory. 
    sbstrPropName = "defaultObjectCategory";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class systemOnly value.
    sbstrPropName = "systemOnly";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class defaultSecurityDescriptor.
    sbstrPropName = "defaultSecurityDescriptor";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);
}
```



 

 